---
description: 20.01.16일 작성
---

# 셋팅 방법\(vue, express, mysql 연동\)

1.  front end의 폴더에 vue 프로젝트 생성.\(vue-cli 이용 -&gt; release 3버전\)
2. webpack 개발서버 구동\(npm run serve -&gt; vue프로젝트 서버
3. 플러그인 추가 \(vue router: router.js에 필요한 라우터 경로를 셋팅해주면 됨., vuex: vuex 설정파일인 store.js에 vuex의 구성요소가 잡혀있음. 이 파일에 필요한 것을 셋팅하면 됨\)
4. 상용 빌드 \(배포를 위하여\) -&gt; 'npm run build' 실행. 빌드를 실행하면 vue-cli가 모든 소스를 핸들링하여 줌.
5. backend의 폴더에 express 셋팅을 위해 app.js 파일 생성. 해당 파일에 port를 3000으로 해서 셋팅. 이렇게 해줌으로써 express 서버가 켜져있으면  localhost:3000으로 접속 가능.
6. 이제 vue, express 서버가 각각 생성됨. 
7. 두 서버를 합치는 작업을 진행해야함.
8. babel.config.js 파일과 형제 파일 생성 \(vue.config.js 파일 생성\)
9. vue.config.js에 배포 파일 위치 지정 및 server의 주소\(url\)을 vue 프로젝트의 port 3000으로 셋팅.
10. backend 폴더에서 npm init으로 package.json 생성.
11. backend 폴더안에 routes/index.js 파일에 빌드를 했을 때 떨어질 파일 경로셋팅. \(현재 프로젝트는 express 라우터로 접근하면 public에 있는 index.html을 전달하게 셋팅되어 있음.\)
12. vue-router와 express 를 연동 하려면 추가적으로 connect-history-api-fallback 모듈이 필요함. 따라서 npm install로 추가 셋팅 필요.
13. 이제 연동 끝.
14. database  셋팅 방법을 참고하여 mysql 를 다운받은 후 app.js에 connection 객체를 이용하여 연동.
15. node.js 를 통한 REST API 구축.
16. GET\(조회\), POST\(등록\), PUT\(수정\), DELETE\(삭제\) 기능 추가.
17. 이제 정말 끝!!

힘들었던 점. vue는 nosql을 이용한 mongodb로만 셋팅 되어 있는 게 인터넷에 많이 올라와 있어서 mysql 과 셋팅하는 부분을 정말 애를 많이 먹었다. 다음에 또 다른 프로젝트를 할 때 까먹지 않도록 기록하는 습관을 들여야 겠다. 다음에는 삽질을 적게 할 수 있길...



