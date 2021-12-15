---
layout: post
title: "Google Analytics추가"
comments: true
---
# 1.Google Analytics에서 트랙킹 id 얻기
우선 https://analytics.google.com/analytics/web/ 로 접속하여 가입을 한다.
그 후 속성설정에서 속성 이름에 자신의 블로그 주소를 입력하고, 보고서 시간대와 표시통화를 선택해준다.
그 뒤에, Google Analytics 가장 하단에 있는 관리를 눌러 사용자 관리 화면을 띄운뒤, 데이터 스트림에 들어가, 현재 blog주소를 찾아 들어가 트래킹id를 획득한다.
# 2.트랙킹 아이디 등록
conig.yml에 들어가
```python
analytics:
  provider               : "google-gtag" 
                          # false (default), "google", "google-universal", "google-gtag", "custom"
  google:
    tracking_id          : "(트랙킹코드)"
    anonymize_ip         : # true, false (default)
```
해당 코드를 입력 후 저장한다.
