---
layout: post
title: git 명령어
description: "기초적이고 자주 사용하는 명령어"
modified: 2018-07-03
tags: [git-command]
image:
  feature: abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
---

git config --global user.name "rok805"
git config --global user.email "rok805@gmail.com"

git init : 현재 로컬저장소를 초기화

git clone " 원격저장소 경로" : 로컬 저장소에 원격 저장소의 리포지터리를 가져옴.

git add 파일 이름 : 커밋하기위한 추가 
git commit -m "커밋 메세지" : add 한 파일들의 커밋
git push origin master    # origin(remote) 에서 master 브랜치로 푸쉬(업로드).....
