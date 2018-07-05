---
layout: post
title: 네번째 수업 필기_경희대
description: "Just about everything you'll need to style in the theme: headings, paragraphs, blockquotes, tables, code blocks, and more."
modified: 2018-07-05
tags: [fourth_class]
---

# 회귀분석
- 변수들 간의 관계를 설명하는 통계적모형을 생성하는 기법

정형 데이터 분석 -> 결과변수의 유무에 따라 지도/비지도 학습으로 나뉨.
지도 학습에는 분류, 추정, 예측이 있고, 이 중 추정을 보도록하자.

- 추정 (결과변수가 연속형=숫자=실수)
    - 데이터 분석 기법
    - 데이터 수집 
    - 데이터 전처리 
    - 분석 : 회귀분석
    - 모델링 : 회귀 모형
    - 분석결과 해석 : 회귀계수, 결정계수, R제곱.
    - 예측


**우선적으로 상관관계와 인과관계에 대해 알아보면**
1.상관관계 : 원인과 결과가 불명확한 관계
2.인과관계 : 상관관계가 있는 전제하에 인과관계를 분석하는데, 원인과 결과가 명확한 관계를 말함.

** 회귀분석은 인과관계를 입증할 수 있음 **
    - 회귀분석은 상관관계를 보고 인과관계를 규명하고자 하여 시작한 것이기 때문
    

### 주요 개념
1. 독립변수, 입력변수, 설명변수 = 회귀분석에서 영향을 주는 변수
2. 종속변수, 반응변수, 출력변수 = 회귀분석에서 영향을 받는 변수


### 회귀분석의 종류
- y가 1개 
1. 단순회귀(x가 1개)
    - 간명성: 간결하고 선명하여 실생활에서 많이 쓰인다. 간단하게 금방 결과가 나오니까.
2. 다중회귀(x가 여러개)
- 독립변수가 범주형인 경우 더미변수로 치환을 하여 분석을 하면 된다. (ex 상/중/하)
- y가 2개 이상 <= 고급.
1. 이항회귀(ex 로지스틱 이항회귀분석) : y가 2개 이상 범주형이여야함.
2. 다항회귀(ex 로지스틱 다항회귀분석) : y가 3개 이상 범주형이여야함

### 회귀분석의 활용
1. 지역별 매출 또는 점유율 추정
2. 고객 이탈 예측
 - 로지스틱 회귀분석

### 선형 회귀분석 기초
  - 하나의 독립 변수와 하나의 종속 변수 간의 선형 관계를 찾는 것
  - 독립변수(x)와 종속변수(y) 값들이 주어진 경우, 이 점들을 가장 잘 설명할 수 있는 일차식을 도출
  
![](/assets/img/180705_단순회귀식.PNG)


2018-07-05-fourth-class
================

회귀분석
========

-   변수들 간의 관계를 설명하는 통계적모형을 생성하는 기법

정형 데이터 분석 -&gt; 결과변수의 유무에 따라 지도/비지도 학습으로 나뉨. 지도 학습에는 분류, 추정, 예측이 있고, 이 중 추정을 보도록하자.

-   추정 (결과변수가 연속형=숫자=실수)
    -   데이터 분석 기법
    -   데이터 수집
    -   데이터 전처리
    -   분석 : 회귀분석
    -   모델링 : 회귀 모형
    -   분석결과 해석 : 회귀계수, 결정계수, R제곱.
    -   예측

**우선적으로 상관관계와 인과관계에 대해 알아보면** 1.상관관계 : 원인과 결과가 불명확한 관계 2.인과관계 : 상관관계가 있는 전제하에 인과관계를 분석하는데, 원인과 결과가 명확한 관계를 말함.

\*\* 회귀분석은 인과관계를 입증할 수 있음 \*\* - 회귀분석은 상관관계를 보고 인과관계를 규명하고자 하여 시작한 것이기 때문

### 주요 개념

1.  독립변수, 입력변수, 설명변수 = 회귀분석에서 영향을 주는 변수
2.  종속변수, 반응변수, 출력변수 = 회귀분석에서 영향을 받는 변수

### 회귀분석의 종류

-   y가 1개

1.  단순회귀(x가 1개)
    -   간명성: 간결하고 선명하여 실생활에서 많이 쓰인다. 간단하게 금방 결과가 나오니까.
2.  다중회귀(x가 여러개)

-   독립변수가 범주형인 경우 더미변수로 치환을 하여 분석을 하면 된다. (ex 상/중/하)
-   y가 2개 이상 &lt;= 고급.

1.  이항회귀(ex 로지스틱 이항회귀분석) : y가 2개 이상 범주형이여야함.
2.  다항회귀(ex 로지스틱 다항회귀분석) : y가 3개 이상 범주형이여야함

### 회귀분석의 활용

1.  지역별 매출 또는 점유율 추정
2.  고객 이탈 예측

-   로지스틱 회귀분석

### 선형 회귀분석 기초

-   하나의 독립 변수와 하나의 종속 변수 간의 선형 관계를 찾는 것
-   독립변수(x)와 종속변수(y) 값들이 주어진 경우, 이 점들을 가장 잘 설명할 수 있는 일차식을 도출

    -식을 통해 절편, 기울기, 오차항을 확인할 수 있다.

### R square 결정계수.

-   Y의 변동 중에서 회귀식에 의해 설명되는 비율.
-   0과1 사이의 값.
-   SSR/TSS (cf. TSS = SSE + SSR)

### 회귀분석의 기본 가정

-   등분산성 : 오차항은 동일한 분산을 가져야한다.
-   독립성 : 오차항 간의 상관관계는 없어야 한다. (Durbin-Watson 검정통계량)
-   정규성 : 오차항은 평균이 0인 정규분포을 따라야 한다.(Shapiro-Wilks 검정)
-   다중공선성 : 교호성. 다중회귀분석의 경우에 발생하며, 독립변수들간의 상관관계가 없어야 한다.(VIF&gt;2.5이면 의심) 상관성이 높은 독립 변수를 제거한 후 분석을 수행한다.

### 실습 ( 교육용 데이터 autoparts.csv 파일을 받아와서 실습한다.)

#### 데이터 확인과 결측치 확인 작업 : read.csv(), dim() is.na(), complete.cases()

``` r
autoparts <- read.csv("autoparts.csv", header=T)
dim(autoparts) #차원을 확인해 보자
```

    ## [1] 34139    11

``` r
sum(is.na(autoparts)) # NA 가 FALSE인 것들의 합. 즉 NA의 개수를 출력해준다.
```

    ## [1] 0

``` r
sum(complete.cases(autoparts)) # is.na 와 반대로 NA 가 TRUE인 것들이 합을 출력
```

    ## [1] 34139

#### french\_fries 데이터

``` r
#install.packages("reshape2")
library(reshape2)
```

    ## Warning: package 'reshape2' was built under R version 3.5.1

``` r
head(french_fries)
```

    ##    time treatment subject rep potato buttery grassy rancid painty
    ## 61    1         1       3   1    2.9     0.0    0.0    0.0    5.5
    ## 25    1         1       3   2   14.0     0.0    0.0    1.1    0.0
    ## 62    1         1      10   1   11.0     6.4    0.0    0.0    0.0
    ## 26    1         1      10   2    9.9     5.9    2.9    2.2    0.0
    ## 63    1         1      15   1    1.2     0.1    0.0    1.1    5.1
    ## 27    1         1      15   2    8.8     3.0    3.6    1.5    2.3

``` r
french_fries[!(complete.cases(french_fries)),]
```

    ##     time treatment subject rep potato buttery grassy rancid painty
    ## 315    5         3      15   1     NA      NA     NA     NA     NA
    ## 455    7         2      79   1    7.3      NA    0.0    0.7      0
    ## 515    8         1      79   1   10.5      NA    0.0    0.5      0
    ## 520    8         2      16   1    4.5      NA    1.4    6.7      0
    ## 563    8         2      79   2    5.7       0    1.4    2.3     NA

#### 데이터 분리

``` r
# 데이터 프레임 분리 형식 : 데이터프레임[어떤 행을 추출할 것인가, 어느 열을 추출할 것인가]
autoparts1 <- autoparts[autoparts$prod_no=='90784-76001',c(2:11)] 
head(autoparts1)
```

    ##   fix_time a_speed b_speed separation s_separation rate_terms  mpa
    ## 1     85.5   0.611   1.715      242.0        657.6         95 78.2
    ## 2     86.2   0.606   1.708      244.7        657.1         95 77.9
    ## 3     86.0   0.609   1.715      242.7        657.5         95 78.0
    ## 4     86.1   0.610   1.718      241.9        657.3         95 78.2
    ## 5     86.1   0.603   1.704      242.5        657.3         95 77.9
    ## 6     86.3   0.606   1.707      244.5        656.9         95 77.9
    ##   load_time highpressure_time c_thickness
    ## 1      18.1                58        24.7
    ## 2      18.2                58        22.5
    ## 3      18.1                82        24.1
    ## 4      18.1                74        25.1
    ## 5      18.2                56        24.5
    ## 6      18.0                78        22.9

#### 기본 통계 정보 - summary(), boxplot()

``` r
#회귀식에선 이상치(outlier)로 인해 예측정확도가 뚝 떨어지므로 summary 를 활용하여 평균, 최대최소값을 확인해야한다.
summary(autoparts1) # 사분위수, 최댓값, 최솟값, 중앙값.
```

    ##     fix_time         a_speed          b_speed        separation   
    ##  Min.   :  1.00   Min.   :0.4570   Min.   :1.240   Min.   :141.6  
    ##  1st Qu.: 81.00   1st Qu.:0.5980   1st Qu.:1.597   1st Qu.:185.9  
    ##  Median : 82.10   Median :0.6090   Median :1.640   Median :190.7  
    ##  Mean   : 83.14   Mean   :0.6189   Mean   :1.644   Mean   :214.5  
    ##  3rd Qu.: 85.40   3rd Qu.:0.6520   3rd Qu.:1.676   3rd Qu.:248.7  
    ##  Max.   :148.60   Max.   :0.8080   Max.   :2.528   Max.   :294.5  
    ##   s_separation     rate_terms         mpa          load_time    
    ##  Min.   :623.3   Min.   :76.00   Min.   :24.80   Min.   : 0.00  
    ##  1st Qu.:651.6   1st Qu.:81.00   1st Qu.:75.30   1st Qu.:18.10  
    ##  Median :710.3   Median :85.00   Median :76.60   Median :19.20  
    ##  Mean   :685.9   Mean   :84.53   Mean   :74.21   Mean   :18.68  
    ##  3rd Qu.:713.6   3rd Qu.:87.00   3rd Qu.:78.10   3rd Qu.:19.20  
    ##  Max.   :747.3   Max.   :97.00   Max.   :82.10   Max.   :22.30  
    ##  highpressure_time   c_thickness     
    ##  Min.   :   37.00   Min.   :   0.30  
    ##  1st Qu.:   60.00   1st Qu.:  21.80  
    ##  Median :   67.00   Median :  23.80  
    ##  Mean   :   96.36   Mean   :  27.44  
    ##  3rd Qu.:   72.00   3rd Qu.:  25.40  
    ##  Max.   :65534.00   Max.   :6553.40

``` r
#시각적으로 이상치를 확인하기 위해 boxplot()을 사용한다.
boxplot(autoparts1)
```

![](/assets/img/unnamed-chunk-4-1.png)

``` r
# 두개의 변수에서 이상치를 볼 수 있다. 이상치가 너무 크니까 상자그림이 납작해 보인다.


# 이상치를 제거해본다
autoparts2 <- autoparts1[autoparts1$c_thickness<1000,]
nrow(autoparts)
```

    ## [1] 34139

#### 히스토그램 : 데이터 분포

``` r
hist(autoparts2$c_thickness, breaks=10) # breaks로 구간설정 가능. 값이 커질수록 막대가 많아진다고 생각하면 쉽다.
```

![](/assets/img/unnamed-chunk-5-1.png)

#### 회귀 모형 만들기 실습 : lm(), summary(lm())

``` r
women
```

    ##    height weight
    ## 1      58    115
    ## 2      59    117
    ## 3      60    120
    ## 4      61    123
    ## 5      62    126
    ## 6      63    129
    ## 7      64    132
    ## 8      65    135
    ## 9      66    139
    ## 10     67    142
    ## 11     68    146
    ## 12     69    150
    ## 13     70    154
    ## 14     71    159
    ## 15     72    164

``` r
m<-lm(weight~height, data=women) # lm(종속변수~독립변수, data=데이터)
m
```

    ## 
    ## Call:
    ## lm(formula = weight ~ height, data = women)
    ## 
    ## Coefficients:
    ## (Intercept)       height  
    ##      -87.52         3.45

``` r
# 비즈니스적 사고: 몸무게가 10이면 키가 -값이 나옴. 그러니까 비즈니스에 대한 이해가 중요하다.


# summary()를 이용한 모델의 통계적 유의성을 살펴보자.
summary(m)
```

    ## 
    ## Call:
    ## lm(formula = weight ~ height, data = women)
    ## 
    ## Residuals:
    ##     Min      1Q  Median      3Q     Max 
    ## -1.7333 -1.1333 -0.3833  0.7417  3.1167 
    ## 
    ## Coefficients:
    ##              Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept) -87.51667    5.93694  -14.74 1.71e-09 ***
    ## height        3.45000    0.09114   37.85 1.09e-14 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 1.525 on 13 degrees of freedom
    ## Multiple R-squared:  0.991,  Adjusted R-squared:  0.9903 
    ## F-statistic:  1433 on 1 and 13 DF,  p-value: 1.091e-14

``` r
# p 값으로 통계적 유의하다고 할지 말지를 결정한다.
# 모델의 설명력을 나타내는 R-squared 값 확인
# Adjusted R-squared : 독립변수가 많아질수록 값이 커지는 현상을 방지.
```

#### 그래프로 그리기 plot()

``` r
plot(women$height, women$weight) # 데이터 산점도 plot(x,y)
abline(m, col='red') # 모델의 직선을 산점도에 입힌다.
```

![](/assets/img/unnamed-chunk-7-1.png)


#### m 모형으로 데이터 예측

``` r
# 키의 단위가 cm 가 아니라서 해석할 때 헷갈렸다.
new.data <- data.frame(height=c(75,76)) # 데이터프레임의 컬럼명과 예측하려는 독립변수의 이름이 같아야한다 ! 그래야 인식함.
predict(m, newdata=new.data)
```

    ##        1        2 
    ## 171.2333 174.6833

``` r
m
```

    ## 
    ## Call:
    ## lm(formula = weight ~ height, data = women)
    ## 
    ## Coefficients:
    ## (Intercept)       height  
    ##      -87.52         3.45

#### 신뢰구간 예측

점추정시 불확실하니까 구간추정을 해봄. interval = "confidence"를 입력하자.

``` r
new.data <- data.frame(height=c(75,76))
predict(m, newdata = new.data, interval = "confidence")
```

    ##        fit      lwr      upr
    ## 1 171.2333 169.0885 173.3781
    ## 2 174.6833 172.3565 177.0102

#### autoparts 데이터 예측

``` r
head(autoparts2)
```

    ##   fix_time a_speed b_speed separation s_separation rate_terms  mpa
    ## 1     85.5   0.611   1.715      242.0        657.6         95 78.2
    ## 2     86.2   0.606   1.708      244.7        657.1         95 77.9
    ## 3     86.0   0.609   1.715      242.7        657.5         95 78.0
    ## 4     86.1   0.610   1.718      241.9        657.3         95 78.2
    ## 5     86.1   0.603   1.704      242.5        657.3         95 77.9
    ## 6     86.3   0.606   1.707      244.5        656.9         95 77.9
    ##   load_time highpressure_time c_thickness
    ## 1      18.1                58        24.7
    ## 2      18.2                58        22.5
    ## 3      18.1                82        24.1
    ## 4      18.1                74        25.1
    ## 5      18.2                56        24.5
    ## 6      18.0                78        22.9

``` r
m <- lm(c_thickness~fix_time, data=autoparts2)
new.data <- data.frame(fix_time=c(86,88,87,89))
predict(m, newdata = new.data)
```

    ##        1        2        3        4 
    ## 23.62751 23.47857 23.55304 23.40409

다중 선형 회귀 분석
-------------------

-   독립변수가 2개 이상인 경우에 다중 선형 회귀 분석을 이용한다.

``` r
autoparts <- read.csv("autoparts.csv",header=T)
autoparts1 <- autoparts[autoparts$prod_no=='90784-76001',c(2:11)]
autoparts2 <- autoparts1[autoparts1$c_thickness<1000,]
m <- lm(c_thickness~fix_time+a_speed, data=autoparts2) # 독립변수 2개를 설정한 경우.
m <- lm(c_thickness~., data=autoparts2)
summary(m)
```

    ## 
    ## Call:
    ## lm(formula = c_thickness ~ ., data = autoparts2)
    ## 
    ## Residuals:
    ##      Min       1Q   Median       3Q      Max 
    ## -24.8428  -0.6105  -0.0214   0.5606  29.6508 
    ## 
    ## Coefficients:
    ##                     Estimate Std. Error  t value Pr(>|t|)    
    ## (Intercept)        7.146e+02  3.367e+00  212.225  < 2e-16 ***
    ## fix_time           6.010e-02  5.331e-03   11.273  < 2e-16 ***
    ## a_speed           -1.738e+01  4.223e-01  -41.152  < 2e-16 ***
    ## b_speed            1.952e+00  1.516e-01   12.876  < 2e-16 ***
    ## separation        -7.592e-01  3.635e-03 -208.873  < 2e-16 ***
    ## s_separation      -7.468e-01  3.673e-03 -203.317  < 2e-16 ***
    ## rate_terms         1.133e-02  3.597e-03    3.151  0.00163 ** 
    ## mpa               -1.520e-01  1.458e-03 -104.253  < 2e-16 ***
    ## load_time         -1.523e-01  8.381e-03  -18.171  < 2e-16 ***
    ## highpressure_time -2.174e-05  8.738e-06   -2.488  0.01284 *  
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 1.796 on 21757 degrees of freedom
    ## Multiple R-squared:  0.7841, Adjusted R-squared:  0.784 
    ## F-statistic:  8782 on 9 and 21757 DF,  p-value: < 2.2e-16

-   모형
-   통계적 유의성은 p 값으로 확인.
    -   각 회귀계수 별로 p 값을 확인하여 회귀계수가 유의한지 판단한다.
    -   전체 모형의 유의성을 알기위해 F 통계량을 통한 p 값을 통해 판단한다.
-   통계적 설명력은 R-squared 값으로 확인.
    -   R-squared 값이 0.784로 약 78% 정도의 설명력을 갖는다고 할 수 있다.
#### m 모형으로 데이터 예측

``` r
# 키의 단위가 cm 가 아니라서 해석할 때 헷갈렸다.
new.data <- data.frame(height=c(75,76)) # 데이터프레임의 컬럼명과 예측하려는 독립변수의 이름이 같아야한다 ! 그래야 인식함.
predict(m, newdata=new.data)
```

    ##        1        2 
    ## 171.2333 174.6833

``` r
m
```

    ## 
    ## Call:
    ## lm(formula = weight ~ height, data = women)
    ## 
    ## Coefficients:
    ## (Intercept)       height  
    ##      -87.52         3.45

#### 신뢰구간 예측

점추정시 불확실하니까 구간추정을 해봄. interval = "confidence"를 입력하자.

``` r
new.data <- data.frame(height=c(75,76))
predict(m, newdata = new.data, interval = "confidence")
```

    ##        fit      lwr      upr
    ## 1 171.2333 169.0885 173.3781
    ## 2 174.6833 172.3565 177.0102

#### autoparts 데이터 예측

``` r
head(autoparts2)
```

    ##   fix_time a_speed b_speed separation s_separation rate_terms  mpa
    ## 1     85.5   0.611   1.715      242.0        657.6         95 78.2
    ## 2     86.2   0.606   1.708      244.7        657.1         95 77.9
    ## 3     86.0   0.609   1.715      242.7        657.5         95 78.0
    ## 4     86.1   0.610   1.718      241.9        657.3         95 78.2
    ## 5     86.1   0.603   1.704      242.5        657.3         95 77.9
    ## 6     86.3   0.606   1.707      244.5        656.9         95 77.9
    ##   load_time highpressure_time c_thickness
    ## 1      18.1                58        24.7
    ## 2      18.2                58        22.5
    ## 3      18.1                82        24.1
    ## 4      18.1                74        25.1
    ## 5      18.2                56        24.5
    ## 6      18.0                78        22.9

``` r
m <- lm(c_thickness~fix_time, data=autoparts2)
new.data <- data.frame(fix_time=c(86,88,87,89))
predict(m, newdata = new.data)
```

    ##        1        2        3        4 
    ## 23.62751 23.47857 23.55304 23.40409

다중 선형 회귀 분석
-------------------

-   독립변수가 2개 이상인 경우에 다중 선형 회귀 분석을 이용한다.

``` r
autoparts <- read.csv("autoparts.csv",header=T)
autoparts1 <- autoparts[autoparts$prod_no=='90784-76001',c(2:11)]
autoparts2 <- autoparts1[autoparts1$c_thickness<1000,]
m <- lm(c_thickness~fix_time+a_speed, data=autoparts2) # 독립변수 2개를 설정한 경우.
m <- lm(c_thickness~., data=autoparts2)
summary(m)
```

    ## 
    ## Call:
    ## lm(formula = c_thickness ~ ., data = autoparts2)
    ## 
    ## Residuals:
    ##      Min       1Q   Median       3Q      Max 
    ## -24.8428  -0.6105  -0.0214   0.5606  29.6508 
    ## 
    ## Coefficients:
    ##                     Estimate Std. Error  t value Pr(>|t|)    
    ## (Intercept)        7.146e+02  3.367e+00  212.225  < 2e-16 ***
    ## fix_time           6.010e-02  5.331e-03   11.273  < 2e-16 ***
    ## a_speed           -1.738e+01  4.223e-01  -41.152  < 2e-16 ***
    ## b_speed            1.952e+00  1.516e-01   12.876  < 2e-16 ***
    ## separation        -7.592e-01  3.635e-03 -208.873  < 2e-16 ***
    ## s_separation      -7.468e-01  3.673e-03 -203.317  < 2e-16 ***
    ## rate_terms         1.133e-02  3.597e-03    3.151  0.00163 ** 
    ## mpa               -1.520e-01  1.458e-03 -104.253  < 2e-16 ***
    ## load_time         -1.523e-01  8.381e-03  -18.171  < 2e-16 ***
    ## highpressure_time -2.174e-05  8.738e-06   -2.488  0.01284 *  
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 1.796 on 21757 degrees of freedom
    ## Multiple R-squared:  0.7841, Adjusted R-squared:  0.784 
    ## F-statistic:  8782 on 9 and 21757 DF,  p-value: < 2.2e-16

-   모형
-   통계적 유의성은 p 값으로 확인.
    -   각 회귀계수 별로 p 값을 확인하여 회귀계수가 유의한지 판단한다.
    -   전체 모형의 유의성을 알기위해 F 통계량을 통한 p 값을 통해 판단한다.
-   통계적 설명력은 R-squared 값으로 확인.
    -   R-squared 값이 0.784로 약 78% 정도의 설명력을 갖는다고 할 수 있다.



#### 잔차 분석

``` r
plot(m)
```

![](/assets/img/unnamed-chunk-12-1.png)![](/assets/img/unnamed-chunk-12-2.png)![](/assets/img/unnamed-chunk-12-3.png)![](/assets/img/unnamed-chunk-12-4.png) 1. 오차와 예측값 잔차 그림. 오차가 0인걸 기준으로해서 잔차가 어떻게 분포되어있는지, c\_thickness 가 작을때와 클때 어떤지. 잔차=0인 직선몰려 직선인 경우가 가장 좋다. 2. 직선을 이루고 있지 않기때문에 x가 작을 때랑 큰 값을 가질 때는 회귀모형으로 측정하기엔 문제가 있다. 정규 분포를 따르지 않기 때문에. 3. 표준화 잔차. 잔차들을 표준편차로 나누고 제곱근을 씌워 0~1이 값을 가지게 만든다. 기울기가 0인 직선이 이상적이다. 4. 왼쪽에 가까울수록 Leverage 0에 가까울수록 좋고, cook-distance거리 안에 있어야함. 벗어난게 있으면 곤란함.

#### 다중 회귀 분석 예측

-   한개의 데이터를 추정해보기

``` r
new.data = data.frame(fix_time=86.1, a_speed=0.610, b_speed=1.718,
                      separation=241.9,s_separation=657.3,rate_terms=95,
                      mpa=78.2,load_time=18.1,highpressure_time=74)

predict(m, newdata = new.data)
```

    ##        1 
    ## 24.42798

-   두 개의 데이터를 추정해보기

``` r
new.data = data.frame(fix_time=c(86.1,86.1), a_speed=c(0.610,0.603), b_speed=c(1.718,1.704),
                      separation=c(241.9,242.5),s_separation=c(657.3,657.3),rate_terms=c(95,95),
                      mpa=c(78.2,77.9),load_time=c(18.1,18.2),highpressure_time=c(74,56))

predict(m, newdata = new.data)
```

    ##        1        2 
    ## 24.42798 24.09751

#### 신뢰구간 구하기

``` r
new.data = data.frame(fix_time=c(86.1,86.1), a_speed=c(0.610,0.603), b_speed=c(1.718,1.704),
                      separation=c(241.9,242.5),s_separation=c(657.3,657.3),rate_terms=c(95,95),
                      mpa=c(78.2,77.9),load_time=c(18.1,18.2),highpressure_time=c(74,56))

predict(m, newdata = new.data, interval="confidence")
```

    ##        fit      lwr      upr
    ## 1 24.42798 24.33378 24.52218
    ## 2 24.09751 24.00560 24.18941

### 최적 변수 찾기

#### 중요변수 찾기

-   여러 독립변수를 이용해 모델을 구성할 수 있지만 그 속엔 모델

#### 모델의 상대적 가치 판정 방법 : AIC

-   낮을수록 좋은 모델.

-   변수 선택법

1.  전진선택법

-   아무 변수도 넣지 않은 모형에서 변수를 추가하며 AIC 값을 보고 선택하는 방법

1.  후진제거법

-   다 들어있는 상태에서 하나씩 변수를 빼면서 AIC 값을 보고 선택하는 방법.

1.  단계별 선택법

-   전진선택법과 후진제거법을 결합한 것으로 변수의 추가 삭제를 반복한다.

``` r
head(swiss)
```

    ##              Fertility Agriculture Examination Education Catholic
    ## Courtelary        80.2        17.0          15        12     9.96
    ## Delemont          83.1        45.1           6         9    84.84
    ## Franches-Mnt      92.5        39.7           5         5    93.40
    ## Moutier           85.8        36.5          12         7    33.77
    ## Neuveville        76.9        43.5          17        15     5.16
    ## Porrentruy        76.1        35.3           9         7    90.57
    ##              Infant.Mortality
    ## Courtelary               22.2
    ## Delemont                 22.2
    ## Franches-Mnt             20.2
    ## Moutier                  20.3
    ## Neuveville               20.6
    ## Porrentruy               26.6

``` r
m <- lm(Fertility ~., data=swiss)
summary(m)
```

    ## 
    ## Call:
    ## lm(formula = Fertility ~ ., data = swiss)
    ## 
    ## Residuals:
    ##      Min       1Q   Median       3Q      Max 
    ## -15.2743  -5.2617   0.5032   4.1198  15.3213 
    ## 
    ## Coefficients:
    ##                  Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)      66.91518   10.70604   6.250 1.91e-07 ***
    ## Agriculture      -0.17211    0.07030  -2.448  0.01873 *  
    ## Examination      -0.25801    0.25388  -1.016  0.31546    
    ## Education        -0.87094    0.18303  -4.758 2.43e-05 ***
    ## Catholic          0.10412    0.03526   2.953  0.00519 ** 
    ## Infant.Mortality  1.07705    0.38172   2.822  0.00734 ** 
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 7.165 on 41 degrees of freedom
    ## Multiple R-squared:  0.7067, Adjusted R-squared:  0.671 
    ## F-statistic: 19.76 on 5 and 41 DF,  p-value: 5.594e-10

1.  회귀계수의 유의성 : 유의수준 95% 하에 'Examination' 변수를 제외한 나머지 독립변수들은 통계적으로 유의하다고 할 수 있다.
2.  회귀모형의 유의성 : p 값이 유의수준보다 높으므로 이 모형은 통계적으로 유의하다고 할 수 없다.
3.  모형의 설명력 : R-squared 값이 0.671로 67.1% 의 통계적인 설명력을 갖는다고 할 수 있다.

#### 전진선택법

``` r
step(m, direction = "forward") # AIC = 190.69, 추정된 모수를 알 수 있다.
```

    ## Start:  AIC=190.69
    ## Fertility ~ Agriculture + Examination + Education + Catholic + 
    ##     Infant.Mortality

    ## 
    ## Call:
    ## lm(formula = Fertility ~ Agriculture + Examination + Education + 
    ##     Catholic + Infant.Mortality, data = swiss)
    ## 
    ## Coefficients:
    ##      (Intercept)       Agriculture       Examination         Education  
    ##          66.9152           -0.1721           -0.2580           -0.8709  
    ##         Catholic  Infant.Mortality  
    ##           0.1041            1.0770

``` r
m<- lm(Fertility~Agriculture, data=swiss) # 당연히 간명성이 높다는 것을 알 수 있다.
summary(m)
```

    ## 
    ## Call:
    ## lm(formula = Fertility ~ Agriculture, data = swiss)
    ## 
    ## Residuals:
    ##      Min       1Q   Median       3Q      Max 
    ## -25.5374  -7.8685  -0.6362   9.0464  24.4858 
    ## 
    ## Coefficients:
    ##             Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept) 60.30438    4.25126  14.185   <2e-16 ***
    ## Agriculture  0.19420    0.07671   2.532   0.0149 *  
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 11.82 on 45 degrees of freedom
    ## Multiple R-squared:  0.1247, Adjusted R-squared:  0.1052 
    ## F-statistic: 6.409 on 1 and 45 DF,  p-value: 0.01492

#### 후진제거법

``` r
m<-lm(Fertility~., data=swiss)
step(m, direction = "backward") # AIC 가  234.09에서 189.86.
```

    ## Start:  AIC=190.69
    ## Fertility ~ Agriculture + Examination + Education + Catholic + 
    ##     Infant.Mortality
    ## 
    ##                    Df Sum of Sq    RSS    AIC
    ## - Examination       1     53.03 2158.1 189.86
    ## <none>                          2105.0 190.69
    ## - Agriculture       1    307.72 2412.8 195.10
    ## - Infant.Mortality  1    408.75 2513.8 197.03
    ## - Catholic          1    447.71 2552.8 197.75
    ## - Education         1   1162.56 3267.6 209.36
    ## 
    ## Step:  AIC=189.86
    ## Fertility ~ Agriculture + Education + Catholic + Infant.Mortality
    ## 
    ##                    Df Sum of Sq    RSS    AIC
    ## <none>                          2158.1 189.86
    ## - Agriculture       1    264.18 2422.2 193.29
    ## - Infant.Mortality  1    409.81 2567.9 196.03
    ## - Catholic          1    956.57 3114.6 205.10
    ## - Education         1   2249.97 4408.0 221.43

    ## 
    ## Call:
    ## lm(formula = Fertility ~ Agriculture + Education + Catholic + 
    ##     Infant.Mortality, data = swiss)
    ## 
    ## Coefficients:
    ##      (Intercept)       Agriculture         Education          Catholic  
    ##          62.1013           -0.1546           -0.9803            0.1247  
    ## Infant.Mortality  
    ##           1.0784

#### 단계별선택법

``` r
m<-lm(Fertility~., data=swiss)
step(m, direction = "both") # AIC = 190.69 에서 189.86.
```

    ## Start:  AIC=190.69
    ## Fertility ~ Agriculture + Examination + Education + Catholic + 
    ##     Infant.Mortality
    ## 
    ##                    Df Sum of Sq    RSS    AIC
    ## - Examination       1     53.03 2158.1 189.86
    ## <none>                          2105.0 190.69
    ## - Agriculture       1    307.72 2412.8 195.10
    ## - Infant.Mortality  1    408.75 2513.8 197.03
    ## - Catholic          1    447.71 2552.8 197.75
    ## - Education         1   1162.56 3267.6 209.36
    ## 
    ## Step:  AIC=189.86
    ## Fertility ~ Agriculture + Education + Catholic + Infant.Mortality
    ## 
    ##                    Df Sum of Sq    RSS    AIC
    ## <none>                          2158.1 189.86
    ## + Examination       1     53.03 2105.0 190.69
    ## - Agriculture       1    264.18 2422.2 193.29
    ## - Infant.Mortality  1    409.81 2567.9 196.03
    ## - Catholic          1    956.57 3114.6 205.10
    ## - Education         1   2249.97 4408.0 221.43

    ## 
    ## Call:
    ## lm(formula = Fertility ~ Agriculture + Education + Catholic + 
    ##     Infant.Mortality, data = swiss)
    ## 
    ## Coefficients:
    ##      (Intercept)       Agriculture         Education          Catholic  
    ##          62.1013           -0.1546           -0.9803            0.1247  
    ## Infant.Mortality  
    ##           1.0784

**Examination 데이터를 제거한 모델이 좋은 모델이라고 할 수 있다.**

#### 실습

``` r
m <- lm(c_thickness~., data=autoparts2)
summary(m)
```

    ## 
    ## Call:
    ## lm(formula = c_thickness ~ ., data = autoparts2)
    ## 
    ## Residuals:
    ##      Min       1Q   Median       3Q      Max 
    ## -24.8428  -0.6105  -0.0214   0.5606  29.6508 
    ## 
    ## Coefficients:
    ##                     Estimate Std. Error  t value Pr(>|t|)    
    ## (Intercept)        7.146e+02  3.367e+00  212.225  < 2e-16 ***
    ## fix_time           6.010e-02  5.331e-03   11.273  < 2e-16 ***
    ## a_speed           -1.738e+01  4.223e-01  -41.152  < 2e-16 ***
    ## b_speed            1.952e+00  1.516e-01   12.876  < 2e-16 ***
    ## separation        -7.592e-01  3.635e-03 -208.873  < 2e-16 ***
    ## s_separation      -7.468e-01  3.673e-03 -203.317  < 2e-16 ***
    ## rate_terms         1.133e-02  3.597e-03    3.151  0.00163 ** 
    ## mpa               -1.520e-01  1.458e-03 -104.253  < 2e-16 ***
    ## load_time         -1.523e-01  8.381e-03  -18.171  < 2e-16 ***
    ## highpressure_time -2.174e-05  8.738e-06   -2.488  0.01284 *  
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 1.796 on 21757 degrees of freedom
    ## Multiple R-squared:  0.7841, Adjusted R-squared:  0.784 
    ## F-statistic:  8782 on 9 and 21757 DF,  p-value: < 2.2e-16

``` r
#전진선택법
step(m, direction="forward")
```

    ## Start:  AIC=25500.35
    ## c_thickness ~ fix_time + a_speed + b_speed + separation + s_separation + 
    ##     rate_terms + mpa + load_time + highpressure_time

    ## 
    ## Call:
    ## lm(formula = c_thickness ~ fix_time + a_speed + b_speed + separation + 
    ##     s_separation + rate_terms + mpa + load_time + highpressure_time, 
    ##     data = autoparts2)
    ## 
    ## Coefficients:
    ##       (Intercept)           fix_time            a_speed  
    ##         7.146e+02          6.010e-02         -1.738e+01  
    ##           b_speed         separation       s_separation  
    ##         1.952e+00         -7.592e-01         -7.468e-01  
    ##        rate_terms                mpa          load_time  
    ##         1.133e-02         -1.520e-01         -1.523e-01  
    ## highpressure_time  
    ##        -2.174e-05

``` r
#후진제거법
step(m, direction="backward")
```

    ## Start:  AIC=25500.35
    ## c_thickness ~ fix_time + a_speed + b_speed + separation + s_separation + 
    ##     rate_terms + mpa + load_time + highpressure_time
    ## 
    ##                     Df Sum of Sq    RSS   AIC
    ## <none>                            70175 25500
    ## - highpressure_time  1        20  70195 25505
    ## - rate_terms         1        32  70207 25508
    ## - fix_time           1       410  70585 25625
    ## - b_speed            1       535  70710 25664
    ## - load_time          1      1065  71240 25826
    ## - a_speed            1      5462  75637 27130
    ## - mpa                1     35055 105230 34318
    ## - s_separation       1    133330 203505 48674
    ## - separation         1    140717 210892 49450

    ## 
    ## Call:
    ## lm(formula = c_thickness ~ fix_time + a_speed + b_speed + separation + 
    ##     s_separation + rate_terms + mpa + load_time + highpressure_time, 
    ##     data = autoparts2)
    ## 
    ## Coefficients:
    ##       (Intercept)           fix_time            a_speed  
    ##         7.146e+02          6.010e-02         -1.738e+01  
    ##           b_speed         separation       s_separation  
    ##         1.952e+00         -7.592e-01         -7.468e-01  
    ##        rate_terms                mpa          load_time  
    ##         1.133e-02         -1.520e-01         -1.523e-01  
    ## highpressure_time  
    ##        -2.174e-05

``` r
#단계별선택법
step(m, direction="both")
```

    ## Start:  AIC=25500.35
    ## c_thickness ~ fix_time + a_speed + b_speed + separation + s_separation + 
    ##     rate_terms + mpa + load_time + highpressure_time
    ## 
    ##                     Df Sum of Sq    RSS   AIC
    ## <none>                            70175 25500
    ## - highpressure_time  1        20  70195 25505
    ## - rate_terms         1        32  70207 25508
    ## - fix_time           1       410  70585 25625
    ## - b_speed            1       535  70710 25664
    ## - load_time          1      1065  71240 25826
    ## - a_speed            1      5462  75637 27130
    ## - mpa                1     35055 105230 34318
    ## - s_separation       1    133330 203505 48674
    ## - separation         1    140717 210892 49450

    ## 
    ## Call:
    ## lm(formula = c_thickness ~ fix_time + a_speed + b_speed + separation + 
    ##     s_separation + rate_terms + mpa + load_time + highpressure_time, 
    ##     data = autoparts2)
    ## 
    ## Coefficients:
    ##       (Intercept)           fix_time            a_speed  
    ##         7.146e+02          6.010e-02         -1.738e+01  
    ##           b_speed         separation       s_separation  
    ##         1.952e+00         -7.592e-01         -7.468e-01  
    ##        rate_terms                mpa          load_time  
    ##         1.133e-02         -1.520e-01         -1.523e-01  
    ## highpressure_time  
    ##        -2.174e-05

#### 연습문제

\`\`\`{r} 성적과 IQ 간의 회귀식을 통하여 IQ가 125 인 사람의 성적을 예측해 보시오. score &lt;- data.frame(성적=c(90,75,77,83,65,80,83,70,87,79), IQ=c(140,125,120,135,105,123,132,115,128,131), 다니는학원수=c(2,1,1,2,0,3,3,1,4,2), 게임하는시간=c(1,3,0,3,4,1,4,1,0,2), TV시청시간=c(0,3,4,2,4,1,1,3,0,3)) m &lt;- lm(성적~IQ, data=score) summary(m) predict(m, newdata = data.frame(IQ=125))

다니는 학원수가 3개 일경우의 성적 예측
======================================

lm2 &lt;- lm(성적~다니는학원수, data=score) predict(lm2, newdata=data.frame(다니는학원수=3))

여러 독립변수를 통한 성적 예측
==============================

lm3 &lt;- lm(성적~IQ+다니는학원수+게임하는시간+TV시청시간, data=score) lm3

IQ가 130(x1), 학원을 3개(x2) 다니고, 게임 2시간(x3), TV 1시간(x4) == &gt; 예상되는 성적(y)은 ?
==============================================================================================

y = (130*0.4684) + (3*0.7179) + (2*(-0.8390)) + (1*(-1.3854))

\`\`\`

#### 집에 가는 문제

``` r
x <- iris
sepalL <- x$Sepal.Length
sepalW <- x$Sepal.Width
petalL <- x$Petal.Length
petalW <- x$Petal.Width

#꽃받침의 길이를 예측하기 위한 다중 회귀 모형
m <- lm(formula = sepalL~sepalW+petalL+petalW, data=x)
summary(m)
```

    ## 
    ## Call:
    ## lm(formula = sepalL ~ sepalW + petalL + petalW, data = x)
    ## 
    ## Residuals:
    ##      Min       1Q   Median       3Q      Max 
    ## -0.82816 -0.21989  0.01875  0.19709  0.84570 
    ## 
    ## Coefficients:
    ##             Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)  1.85600    0.25078   7.401 9.85e-12 ***
    ## sepalW       0.65084    0.06665   9.765  < 2e-16 ***
    ## petalL       0.70913    0.05672  12.502  < 2e-16 ***
    ## petalW      -0.55648    0.12755  -4.363 2.41e-05 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.3145 on 146 degrees of freedom
    ## Multiple R-squared:  0.8586, Adjusted R-squared:  0.8557 
    ## F-statistic: 295.5 on 3 and 146 DF,  p-value: < 2.2e-16

