Untitled
================

### 회귀모형 성능 평가를 위한 훈련데이터와 검증데이터

-   추정의 성능을 알아보는 지표: k-fold
-   분류의 성능을 알아보는 지표: 정분류율, 민감도, 정확도, ... ... 등

#### K-fold CV(Cross-Validation) 교차검증 : 추정모델의 성능을 평가하는 지표.

-   교차검증의 데이터를 만들기 위한 sample(), split() 함수

``` r
sample(1:10, 5)
```

    ## [1] 10  7  3  4  6

``` r
# List형 데이터 구조를 리턴한다.
# split(iris, iris$Species)
# split(iris, 1:10) # iris의 데이터를 10개로 쪼개어라.
```

``` r
autoparts <- read.csv("autoparts.csv", header = T)
autoparts1 <- autoparts[autoparts$prod_no=='90784-76001',c(2:11)]
autoparts2 <- autoparts1[autoparts1$c_thickness<1000,]

t_index<-sample(1:nrow(autoparts2), size=nrow(autoparts2))
split_index <- split(t_index, 1:10)
```

    ## Warning in split.default(t_index, 1:10): data length is not a multiple of
    ## split variable

``` r
class(split_index)
```

    ## [1] "list"

#### 교차 검증 수행 K-fold CV \*\* 10개로 쪼갬

``` r
mse <- c()
for(i in 1:10){
  test <- autoparts2[split_index[[i]],] # 검증데이터 생성
  train <- autoparts2[-split_index[[i]],] # 훈련데이터 생성
  
  m <- lm(c_thickness~., data = train)
  m_pred <- predict(m, test)
  mse[i] <- mean((test$c_thickness-m_pred)^2) # 오차제곱들의 평균값을 mse에 저장.
}

mean(mse)
```

    ## [1] 3.245292

#### 훈련데이터 70%, 검증데이터 30%로 분리

``` r
t_index <- sample(1:nrow(autoparts2),0.7*nrow(autoparts2))
train <- autoparts2[t_index,]
test <- autoparts2[-t_index,]
nrow(train);nrow(test);
```

    ## [1] 15236

    ## [1] 6531

``` r
m <- lm(c_thickness~., data=train)
m_pred <- predict(m,test)
mse <- (test$c_thickness-m_pred)^2
mean(mse)
```

    ## [1] 2.967725

#### LASSO: 축소 추정법

개념: 기본 오차값 계산 + 패널티 계산. 여기서 패널티 계산 영역은 변수 선택에 영향을 끼친다. 람다값이 너무 커지거나 작아선 안되고 적절한 값을 찾아야함. - 람다 = 0 : 계수는 어떤 값이든 관계없으므로 모든 변수를 선택하여 과대적합이 되어 모델이 복잡해지므로 예측력이 저하된다. - 람다 = 큰 값: 계수가 작아지게 되어 대부분의 변수를 제거하여 과소적합이 되고 모델은 매우 심플해지므로 예측력이 저하된다.

#### mse 가 최소인 최적의 람다값을 찾자 !

``` r
xmat <- as.matrix(autoparts2[1:9])
yvec <- autoparts2$c_thickness
#install.packages("glmnet")
library(glmnet)
```

    ## Loading required package: Matrix

    ## Loading required package: foreach

    ## Loaded glmnet 2.0-16

``` r
fit.lasso <- glmnet(x=xmat, y=yvec, alpha=1, nlambda = 100) # 람다를 100개 만들어 준다.
fit.lasso.cv <- cv.glmnet(x=xmat, y=yvec, nfolds =10, alpha=1) #alpha는 LASSO 수행 옵션
plot(fit.lasso.cv) 
```

![](/assets/img/unnamed-chunk-5-1.png)

#### 최적 LASSO 모형 만들기 및 계수 출력

``` r
fit.lasso.param <- fit.lasso.cv$lambda.min

fit.lasso.tune <- glmnet(x=xmat, y=yvec, alpha=1, lambda=fit.lasso.param)
coef(fit.lasso.tune)
```

    ## 10 x 1 sparse Matrix of class "dgCMatrix"
    ##                              s0
    ## (Intercept)        7.060442e+02
    ## fix_time           5.908511e-02
    ## a_speed           -1.710450e+01
    ## b_speed            1.945219e+00
    ## separation        -7.497086e-01
    ## s_separation      -7.372797e-01
    ## rate_terms         1.045370e-02
    ## mpa               -1.526337e-01
    ## load_time         -1.506828e-01
    ## highpressure_time -1.857361e-05

#### 발표수업

느낀점.
