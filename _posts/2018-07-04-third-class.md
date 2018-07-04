---
layout: post
title: 세번째 수업 필기_경희대
description: "Just about everything you'll need to style in the theme: headings, paragraphs, blockquotes, tables, code blocks, and more."
modified: 2018-07-04
tags: [second_class]
---

`세번째 수업` 이새봄 임시강사님.

복습을 하였다. 학습하는 과정이 a,b,c 를 배우면 다음날 b~c부터 시작해서 d,e,f 과정을 나가는 방식이 교육생들에게 좋다고 교수님이 말씀하셨다.
망각을 방지하며 교육의 효율을 올리시려는 노인성 박사님.


세번째 수업
================

``` r
# 데이터 프레임을 엑셀파일로 내보내기
#install.packages("xlsx") # xlsx 패키지 설치
library(xlsx)
name <- c('apple','banana','peach')
price <- c(300,200,100)
item <- data.frame(NAME=name, PRICE=price)
#write.xlsx(item, "item.xlsx", sheetName="Sheet1",row.names=F) item 을 item.xlsx 파일로 내보냄

# write.xlsx(x, file, sheetName="Sheet1", 
#            col.names=TRUE, row.names=TRUE, append=FALSE, showNA=TRUE, password=NULL)
# SheetName 은 엑셀의 시트네임, col,row.names 는 열,행 이름을 넣을 것인가에 대한 내용.

#list.files() # 디렉토리에 xlsx이 잘 들어왔나 확인해 보자.
```

### R 프로그램 기초 문법 - 함수

``` r
vec1 <- 1:5
vec2 <-  c('a','b','c','d','e')
max(vec1) # vec1 벡터의 최댓값을 보여준다.
```

    ## [1] 5

``` r
mean(vec1) # 평균값 구함.
```

    ## [1] 3

``` r
min(vec1) # 최솟값
```

    ## [1] 1

``` r
sd(vec1) # 표준편차
```

    ## [1] 1.581139

### aggregate 함수 (그룹화+함수 적용)

`아주 중요하고 많이 쓰인다.`

``` r
#install.packages("googleVis")
library(googleVis) # 엄청난 시각화 에 활용할 수 있음.
```

    ## Warning: package 'googleVis' was built under R version 3.5.1

``` r
Fruits # googleVis 속에 들어있는 데이터.
```

    ##     Fruit Year Location Sales Expenses Profit       Date
    ## 1  Apples 2008     West    98       78     20 2008-12-31
    ## 2  Apples 2009     West   111       79     32 2009-12-31
    ## 3  Apples 2010     West    89       76     13 2010-12-31
    ## 4 Oranges 2008     East    96       81     15 2008-12-31
    ## 5 Bananas 2008     East    85       76      9 2008-12-31
    ## 6 Oranges 2009     East    93       80     13 2009-12-31
    ## 7 Bananas 2009     East    94       78     16 2009-12-31
    ## 8 Oranges 2010     East    98       91      7 2010-12-31
    ## 9 Bananas 2010     East    81       71     10 2010-12-31

``` r
aggregate(Sales~Year, Fruits, sum) # 연도별 판매량의 합계를 나타낸다.
```

    ##   Year Sales
    ## 1 2008   279
    ## 2 2009   298
    ## 3 2010   268

``` r
aggregate(Sales~Fruit,Fruits,sum) # 과일별 판매량의 합계를 나타낸다.
```

    ##     Fruit Sales
    ## 1  Apples   298
    ## 2 Bananas   260
    ## 3 Oranges   287

``` r
aggregate(Sales~Fruit+Year+Location,Fruits,max) # 과일, 연도, 장소별 판매량의 최댓값을 나타낸다.
```

    ##     Fruit Year Location Sales
    ## 1 Bananas 2008     East    85
    ## 2 Oranges 2008     East    96
    ## 3 Bananas 2009     East    94
    ## 4 Oranges 2009     East    93
    ## 5 Bananas 2010     East    81
    ## 6 Oranges 2010     East    98
    ## 7  Apples 2008     West    98
    ## 8  Apples 2009     West   111
    ## 9  Apples 2010     West    89

### 조건문 if

``` r
a<-4
if(a==4){
  print('this is 4')
}
```

    ## [1] "this is 4"

### 조건문 if 와 else

``` r
a<-3
if(a==4){
  print('this is 4')
}else print('this is not 4')
```

    ## [1] "this is not 4"

### 조건문 elseif

``` r
a<-2
if(a==3){
  print('this is 3')
}else if(a==2){
  print('this is 2')
}
```

    ## [1] "this is 2"

### 조건문 ifelse : if 와 else 구문을 한줄로 끝낼 수 있다.

``` r
a <-2
ifelse(a==3, "this is 3", "this is not 3")
```

    ## [1] "this is not 3"

### 반복문 for(a==

``` r
for(i in 1:10){
  print(i)
  if(i==3) break;  # break는 중괄호를 나오게 한다. 즉 break를 만나면 정지하라는 소리.
}
```

    ## [1] 1
    ## [1] 2
    ## [1] 3

``` r
x<-c(1,2,3) 
for(i in 1:length(x)){  # length와 같이 쓰는걸 권장하신다. SB교수님.
  print(i)
}
```

    ## [1] 1
    ## [1] 2
    ## [1] 3

### 연습문제

``` r
answer <- '여'
# 1.1) if 문을 사용
if(answer=='여') print('hi yeo')
```

    ## [1] "hi yeo"

``` r
# 1.2) ifelse 문을 사용
ifelse(answer=='여',print('hi yeo'),print('hi nam'))
```

    ## [1] "hi yeo"

    ## [1] "hi yeo"

``` r
#2) 
fruits <- c('사과', '바나나 ','체리',' 포도', '딸기', '수박', '파인애플', '망고', '메론')
for(i in 1:length(fruits)){ # 과일 인덱스를 하나씩
  print(i)
}
```

    ## [1] 1
    ## [1] 2
    ## [1] 3
    ## [1] 4
    ## [1] 5
    ## [1] 6
    ## [1] 7
    ## [1] 8
    ## [1] 9

``` r
for(i in fruits){ # 과일이름을 하나씩 출력
  print(i)
}
```

    ## [1] "사과"
    ## [1] "바나나 "
    ## [1] "체리"
    ## [1] " 포도"
    ## [1] "딸기"
    ## [1] "수박"
    ## [1] "파인애플"
    ## [1] "망고"
    ## [1] "메론"

``` r
for(i in 1:length(fruits)){ # 1:length()를 사용
  print(fruits[i])
}
```

    ## [1] "사과"
    ## [1] "바나나 "
    ## [1] "체리"
    ## [1] " 포도"
    ## [1] "딸기"
    ## [1] "수박"
    ## [1] "파인애플"
    ## [1] "망고"
    ## [1] "메론"

### R 함수 작성

``` r
say <- function(x){ # x는 인자값.
  print('this is what you said')
  print(x)
}
say('sa rang hae yo ~')
```

    ## [1] "this is what you said"
    ## [1] "sa rang hae yo ~"

``` r
final.score <- function(a,b,c,d){ # 네 점수를 넣고 평균값을 출력하는 함수.
  print('your mean score is ')
  print((a+b+c+d)/4)
}
final.score(37,68,38,100)
```

    ## [1] "your mean score is "
    ## [1] 60.75

### return : 함수 밖으로 값을 리턴함. 출력함.

``` r
cal.profit <- function(sales,cost){
  profit<-sales-cost
  return(profit)
}
cal.profit(45000,28500)
```

    ## [1] 16500

### 함수 작성 연습문제

``` r
askGender <- function(){
  answer <- readline("type gender: 1:man, 2:woman") #readline 은 scan과 비슷하게 사용자에게 입력을 받는 함수.
  if(answer==1){
    print("hi man")
  }else print("hi woman")
}
# askGender() 사용자 입력을 시작으로 출력까지 함수가 실행된다.

enter <- function(){
  who <- readline()
  cat(who,' is coming')
}
# enter() 사용자 입력을 시작으로 출력까지 함수가 실행된다.
```

### paste 함수

``` r
number <- 1:9
alphabet <- c('a','b')
paste(number, alphabet) # 짝 지어서 쌍을 만든다. 짝이 안맞아도 끝날때까지.
```

    ## [1] "1 a" "2 b" "3 a" "4 b" "5 a" "6 b" "7 a" "8 b" "9 a"
