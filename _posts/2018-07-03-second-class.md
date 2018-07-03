---
layout: post
title: 두번째 수업_경희대
description: "Just about everything you'll need to style in the theme: headings, paragraphs, blockquotes, tables, code blocks, and more."
modified: 2018-07-03
tags: [second_class]
image:
  feature: abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
---

### 1. 분석 모형의 성능

#### 1.1 분류 모형
- 정분류율
- 오분류율
- 소수 집단 정분류율
- 소수 집단 오분류율
- 민감도, 특이도
- 정확도
- 재현율(도)
- F값

##### 시각화 평가 척도(지표)를 만들어 보자~ 해서 만든 것이 

    -첫번째 **ROC** 곡선 그래프 : AUC의 값이 클 수록 좋다. AUC= ROC 곡선 하의 면적 계산 값.
    -두번째 이익 도표(Gain Chart) : 표본이 적어도 TP를 많이 추출해내는 모형이 비용면에서 더 우수하다.
    -세번째 리프트 도표(향상도): 이익 도표랑 같다고 보면 된다.

#### 1.2 추정 모형
 - MSE : 오차제곱평균
 - MAE : 절대오차평균
 - MAPE : 절대 퍼센티지 오차평균
-> 값이 낮을수록 좋다.

#### 각 모형에 따라서 평가 지표가 존재하기도 합니다.
- 회귀모형의 R-Squared 값 : 모형의 설명력을 나타내는 척도.
