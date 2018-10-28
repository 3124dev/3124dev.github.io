---
layout: post
title:  "Git usage"
date:   2018-10-28 21:32:00 +0900
categories: git
---

1. 준비
초심자인 나의 git은 언제나 누군가의 git을 clone하며 시작된다...
(물론 아주 가끔씩 `git init`으로 시작하는 경우가 있겠지만)
[설명이 필요한 argument는 설명을 괄호로 묶었다]

`git -clone [Clone대상의 url]`

그 후 가장 좋은 시도는 실수를 방지하기 위한 branch
혼자 급하다고 branch먼저 안따고 코드부터 보다가 commit을 앞두고 후회하지말자 휴벝

생성
`git branch [브랜치 이름]`

체크아웃 : 처음 checkout을 보고 호텔의 경우를 생각하여 혼란스러웠는데.. git은 이렇게 branch를 선택한다.
`git checkout [브랜치 이름]`


2. 작업
여기까지 해두면 얼마간은 편하게 commit만 두들기게 된다.
`git add [commit할 대상을 선택한다]` (추적, 저장을 원하는 파일을 더한다고 하면 나로서는 이해하기 어려워서 나름의 정리를 했다.)
보통은 통으로 모든 디렉토리와 파일을 추척하기위해
`git add .` 또는 `git add -a`를 애용한다.

이렇게 add를 완료하면 수정또는 추가한 코드를 commit하여 상태를 저장한다.
`git commit -m "[커밋하는 내용에 대한 설명]"`

커밋 작업중에 수정사항을 add했는지 기억이 가물가물 하면
`git status`를 통해 파일들의 staging 상태를 체크해볼 수 있다.
변경했으나 staged가 아닌 파일의 내용을 보고싶으면
`git diff`를 입력하면 친절하게 나오지만, 이런 확인은 더 친절한 source tree를 이용한다


3. 완료
`git push origin [만들어둔 브랜치]`

`git checkout master`

`git pull origin master`

`git checkout [내 브랜치]`

`git merge master`
Conflict내용 확인 후
`git checkout master`

`git merge [내 브랜치]`

`git pull origin master`