---
description: 추후 작성 필요
---

# 내가 했던 실수를 기록함

#### 1. 맥 종료시, mysql 서버 중단 해야함. 중단하지 않아서 timeout 으로 mysql rock 걸리는 현상 발견.\(mysql.server stop\)

{% embed url="https://km0830.tistory.com/5" %}

#### 

#### 2. mysql을 업데이트 했더니 아래와 같은 오류 발생. 삽질 반복.. 며칠동안 고생... 

* the server quit without updating pid
* MySQL server has gone away
* Can't connect to local MySQL server through socket '/tmp/mysql.sock' \(2\)

위 에러들이 반복적으로 나오면서 mysql 서버를 킬 수 없었음. 결국 제일 큰 문제는 mysql 버전 업데이트를 진행하면서 pid가 업데이트 되지 않아 버전 문제로 오류가 발생했던 것. 해결방법을 찾기까지 며칠동안 삽질을 반복했지만 해결해서 매우 다행. 다음에는 실수 안하도록 조심해야지. 참고한 사이트들!!

{% embed url="https://m.blog.naver.com/PostView.nhn?blogId=playhoos&logNo=221505255355&proxyReferer=https%3A%2F%2Fwww.google.com%2F" %}

{% embed url="https://manage.accuwebhosting.com/knowledgebase/2342/How-to-Fix-MySQL-Error-The-server-quit-without-updating-PID-file.html" %}







