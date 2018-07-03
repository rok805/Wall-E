R 프로그램 수업 필기
================

### 패키지 사용

``` r
install.packages() ## 패키지를 다운로드, 설치
update.packages() ## 현재 설치된 패키지 업데이트
library() ## 패키지를 로드하여 사용할 준비
```

### 대입과 할당

-   변수 &lt;- "수치나 계산식 등" 대입&할당 한다. 변수선언 필요없음.

``` r
2+3
```

    ## [1] 5

``` r
x<-2
y<-3
x+y
```

    ## [1] 5

### 변수 작성 규칙

-   변수명의 대소문자를 구분한다.
-   변수명 숫자나 기호로 시작하면 안된다.

<br>

### R 함수

``` r
plus <- function(x,y)
  return(x+y)
plus(10,20)
```

    ## [1] 30

### 데이터 유형

``` r
x<-8
class(x) ## class는 데이터의 유형을 리턴해준다.
```

    ## [1] "numeric"

``` r
y<- "Kim"
class(x)
```

    ## [1] "numeric"

``` r
z<-factor(c("T","F","TF"))
class(z)
```

    ## [1] "factor"

``` r
w<-as.logical(c(1,0,1,0))
w
```

    ## [1]  TRUE FALSE  TRUE FALSE

<br> \#\#\# TRUE/FALSE 값

``` r
3&0 # 참 곱하기 거짓이므로 FALSE
```

    ## [1] FALSE

``` r
3&1 # 참 곱하기 참이므로 TRUE
```

    ## [1] TRUE

``` r
3|0 # OR 연산자. 3이 참으므로 TRUE
```

    ## [1] TRUE

``` r
3|1 # TRUE
```

    ## [1] TRUE

``` r
!0 # 0, 거짓의 부정(!)이므로 TRUE
```

    ## [1] TRUE

``` r
!1 # 1, 참의 부정(!)이므로 FALSE
```

    ## [1] FALSE

![and\_or 연산자](image/and_or.PNG)

<br> - 파란 부분의 1은 모든 수로 바꿔도 TRUE 다.

<br>

### NA, NULL 형

``` r
cat(1, NA, 2) # NA: Not Available
```

    ## 1 NA 2

``` r
cat(1, NULL, 2) # NULL: 아예 존재하지 않음.
```

    ## 1 2

``` r
sum(1, NA, 2)
```

    ## [1] NA

``` r
sum(1, NULL, 2)
```

    ## [1] 3

``` r
# sum(1,2,NA) # 에러 발생
sum(1,2,NA,na.rm=T) #na.rm 옵션으로 NA를 제거한 후 sum() 을 수행
```

    ## [1] 3

<br>

### 날짜 형태 지정하기

``` r
#install.packages("lubridate") # 날짜 관련 패키지 설치
library(lubridate) # 라이브러리 등록
```

    ## 
    ## Attaching package: 'lubridate'

    ## The following object is masked from 'package:base':
    ## 
    ##     date

``` r
Sys.Date() #  날짜를 보여주는 함수
```

    ## [1] "2018-07-04"

``` r
Sys.time() # 날짜와 시간 모두 보여주는 함수
```

    ## [1] "2018-07-04 08:06:00 KST"

``` r
date() # 미국식 날짜와 시간을 보여준다.
```

    ## [1] "Wed Jul 04 08:06:00 2018"

``` r
as.Date("01-11-2014")
```

    ## [1] "0001-11-20"

``` r
date <- now() # 현재시각 객체 생성
date
```

    ## [1] "2018-07-04 08:06:00 KST"

``` r
year(date)
```

    ## [1] 2018

``` r
month(date,label=T) # label=T : level 출력
```

    ## [1] 7
    ## Levels: 1 < 2 < 3 < 4 < 5 < 6 < 7 < 8 < 9 < 10 < 11 < 12

``` r
month(date,label=F) # level 을 출력하지 않음.
```

    ## [1] 7

``` r
day(date)
```

    ## [1] 4

``` r
wday(date, label = T) # 요일을 이름으로 출력한다.
```

    ## [1] 수
    ## Levels: 일 < 월 < 화 < 수 < 목 < 금 < 토

``` r
wday(date, label = F) # 요일을 숫자로 출력한다.(일요일=1로 시작한다)
```

    ## [1] 4

``` r
date <- date -days(2) # 이틀 빼기
date
```

    ## [1] "2018-07-02 08:06:00 KST"

``` r
month(date) <- 2  # 2 month로 바꿔준다
date
```

    ## [1] "2018-02-02 08:06:00 KST"

``` r
date+years(1) #1년 추가하기
```

    ## [1] "2019-02-02 08:06:00 KST"

``` r
date+months(1) #1개월 추가하기
```

    ## [1] "2018-03-02 08:06:00 KST"

``` r
date+hours(1) #1시간 추가하기
```

    ## [1] "2018-02-02 09:06:00 KST"

``` r
date+minutes(1) #1분 추가하기
```

    ## [1] "2018-02-02 08:07:00 KST"

``` r
date+seconds(1) #1초 추가하기
```

    ## [1] "2018-02-02 08:06:01 KST"

``` r
date<-hm("22:30") #시간 분 지정하기
date
```

    ## [1] "22H 30M 0S"

``` r
date <- hms("22:30:15"); #시간 분 초 지정하기
date
```

    ## [1] "22H 30M 15S"

<br>

### 데이터의 구조

스칼라(1행1열) -&gt; 벡터(1열의 행렬) -&gt; 행렬(n*n) -&gt; 배열(n*n\*n) =&gt; 구성인자가 동일한 데이터 타입이여야한다. 리스트 -&gt; 데이터 프레임 =&gt; 구성인자가 동일하지 않은 데이터타입의 입력이 가능하다.

내가 가진 데이터에 맞게 구조를 선택하는 것이 가장 좋다. 메모리 낭비를 줄일 수 있다.

### 벡터

``` r
x <- c(1,2,3,4,5)
x[2]
```

    ## [1] 2

``` r
x[4] <- 0  # 4번째 원소 제거
x
```

    ## [1] 1 2 3 0 5

``` r
x <- c(x,4)
x
```

    ## [1] 1 2 3 0 5 4

### 리스트

``` r
test <- list("kim",c(3,4,5),c('T','F','T'))
test
```

    ## [[1]]
    ## [1] "kim"
    ## 
    ## [[2]]
    ## [1] 3 4 5
    ## 
    ## [[3]]
    ## [1] "T" "F" "T"

``` r
son <-list(son.name=c('a','b'), son.gender=c('m','m'), son.age=c(23,43),son.mom=c('y'))
data.frame(son) # 한번 만들어 본다.
```

    ##   son.name son.gender son.age son.mom
    ## 1        a          m      23       y
    ## 2        b          m      43       y

``` r
son[[2]]
```

    ## [1] "m" "m"

``` r
son[[3]][2]
```

    ## [1] 43

``` r
names(son) <- c("name",'gender','age','mom')
son[1:2]
```

    ## $name
    ## [1] "a" "b"
    ## 
    ## $gender
    ## [1] "m" "m"

### 행렬

``` r
x <- matrix(c(1,2,3,4),nrow=2, ncol=2)
matrix(c(1,2,3,4))
```

    ##      [,1]
    ## [1,]    1
    ## [2,]    2
    ## [3,]    3
    ## [4,]    4

``` r
matrix(c(1,2,3,4), nrow=2, ncol=2,byrow =TRUE) # 열부터 값을 채움
```

    ##      [,1] [,2]
    ## [1,]    1    2
    ## [2,]    3    4

``` r
r1<-c(1,4,7)
r2<-c(2,5,8)
r3<-c(3,6,9)
rbind(r1,r2,r3) # 행이름은 벡터명이 된다.
```

    ##    [,1] [,2] [,3]
    ## r1    1    4    7
    ## r2    2    5    8
    ## r3    3    6    9

``` r
cbind(r1,r2,r3) # 열이름이 벡터명이 된다.
```

    ##      r1 r2 r3
    ## [1,]  1  2  3
    ## [2,]  4  5  6
    ## [3,]  7  8  9

``` r
array(1:6)  
```

    ## [1] 1 2 3 4 5 6

``` r
array(1:6, c(2,3))  
```

    ##      [,1] [,2] [,3]
    ## [1,]    1    3    5
    ## [2,]    2    4    6

``` r
array(1:8, c(2,2,2))
```

    ## , , 1
    ## 
    ##      [,1] [,2]
    ## [1,]    1    3
    ## [2,]    2    4
    ## 
    ## , , 2
    ## 
    ##      [,1] [,2]
    ## [1,]    5    7
    ## [2,]    6    8

``` r
arr <-c(1:24)
dim(arr) <- c(3,4,2)
```

### 데이터프레임 생성

``` r
char1 <- c('A','A','B','B','C')
char1
```

    ## [1] "A" "A" "B" "B" "C"

``` r
num1<-c(1,1,2,2,3)
num1
```

    ## [1] 1 1 2 2 3

``` r
test1<-data.frame(char1,num1) #열이름에 벡터이름이 붙는다.


test3 <- rbind(test1,c('C',4))
test2 <- cbind(test1,married=c(T,T,F,F,T))
```

### 데이터 파일 R로 불러오기

``` r
#.csv 파일 내보내기
write.csv(test2,file="test2.csv",row.names = F)
#.txt파일 불러오기
# read.table(file="", header = T/F, sep="", stringsAsFactors = T/F)
#read.csv("test2.csv",header = T,sep=",",stringAsFactor=,encoding = "utf-8") # stringAsFactor 은 불러오는 텍스트를 팩터(범주)로 인식할건지.
txt1 <- read.csv("r_temp/R라뷰_개정판용 실습 데이터 모음/factor_test.txt")
factor1 <- factor(txt1$blood)
factor1
```

    ##  [1] O  A  O  B  AB A  B  O  B  B 
    ## Levels: A AB B O

``` r
summary(factor1)
```

    ##  A AB  B  O 
    ##  2  1  4  3

``` r
sex1 <- factor(txt1$sex)
summary(sex1)
```

    ## 남 여 
    ##  7  3

``` r
input <- scan(what = "") # what="" 는 문자 입력시.
fruits <- read.table("r_temp/R라뷰_개정판용 실습 데이터 모음/fruits.txt",header=T) # 첫열이 변수명.
fruits2 <- read.table("r_temp/R라뷰_개정판용 실습 데이터 모음/fruits.txt") # header 구분없이 다 불러온다.
fruits2 <- read.table("r_temp/R라뷰_개정판용 실습 데이터 모음/fruits.txt",skip=2) # skip=건너뛸 행 수.
fruits2 <- read.table("r_temp/R라뷰_개정판용 실습 데이터 모음/fruits.txt",nrows=2) # nrows=갖고 오고픈 행의 수.
fruits3 <- read.table("r_temp/R라뷰_개정판용 실습 데이터 모음/fruits.txt",header=F,skip=2,nrows=2)#첫 행이 변수명이 아니고! 위에서부터 두줄 생략하고! 위에서부터 두줄만 딱 갖고온다. 변수명은 없어서 임의로 V(variable)이됨.
fruit4 <- read.csv("r_temp/R라뷰_개정판용 실습 데이터 모음/fruits_4.csv",header=T)
label <- c('NO', 'NAME', 'PRICE', 'QTY')
fruit4 <- read.csv('r_temp/R라뷰_개정판용 실습 데이터 모음/fruits_4.csv')
```

### 파일 이름확인하기.

``` r
list.files() # 현재 워킹디렉토리의 파일을 보여준다.
```

    ##  [1] "aaaaa.md"                     "aaaaa.Rmd"                   
    ##  [3] "aaaaa_files"                  "dbguide.R"                   
    ##  [5] "desktop.ini"                  "dplyr_0.7.4"                 
    ##  [7] "ezPDFPlayer3.0"               "FeedbackHub"                 
    ##  [9] "FIFA ONLINE 4"                "FIFA ONLINE3"                
    ## [11] "GitHub"                       "image"                       
    ## [13] "My Music"                     "My Pictures"                 
    ## [15] "My Videos"                    "R"                           
    ## [17] "r_temp"                       "Rtraining"                   
    ## [19] "Sample9"                      "SPSSInc"                     
    ## [21] "test2.csv"                    "댓글.xlsx"                   
    ## [23] "사용자 지정 Office 서식 파일" "스팸 데이터.xlsx"            
    ## [25] "이청록150301.jpg"             "카카오톡 받은 파일"          
    ## [27] "필기노트.R"

``` r
# list.files(recursive=T)#하위파일까지 보여줌.
# list.files(all.files=T)#숨김파일까지 모조리 보여준다.
```
