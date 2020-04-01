---
description: 20.01.15일 작성
---

# database 셋팅 방법

1. npm init \(package json에 생성되며 그 안에 필요한 파일들을 넣고 npm install 하면 다 받아줌\)
2. npm start
3. mysql 접속 \(mysql -uroot -p\) 명령어를 입력. \(참고: mysql 로그아웃: quit,  mysql 서버종료: mysql.server stop\)
4. mysql에 접속하여 테스트용 데이터 insert.
5. database 생성 \(ex: test\_db\)
6. database 사용한다고 선언 \(ex: USE test\_db\)
7. 생성한 database에 table 생성
8. table에 데이터 삽입
9. table 확인 \(show tables;\)
10. 중요!!  권한 설정\(UPDATE 문 사용하면 안됨. mysql version 8.0이상부터는 권한생성시 CREATE USER  '사용자'@'localhost' IDENTIFIED BY '비밀번호'; 권한수정시 ALTER USER '사용자'@'localhost' IDENTIFIED WITH MYSQL\_NATIVE\_PASSWORD BY '비밀번호';
11. FLUSH PRIVILEGES;
12. 권한이 잘 설정 되었는지 확인.
13. 추가한 권한으로 db에 잘 접속되는지 확인.
14. database에도 user 권한 부여. \(ex: GRANT ALL PRIVILEGES ON test\_db TO '사용자'@'localhost';
15. FLUSH PRIVILEGES;

