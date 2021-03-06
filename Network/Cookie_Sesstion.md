## 쿠키(Cookie)와 세션(Session)
### 세션(Session)
+ 일정시간 동안 같은 클라이언트로 부터 들어오는 요구를 구별하기 위해 특정시간(또는 브라우저종료)까지 유지하는 기술
+ 왜 사용되는가(Why)
  - HTTP는 기본적으로 비연결지향 프로토콜이므로 이전상태를 저장하지 않는다.
  - 따라서 클라이언트가 이전 request와 동일한 클라이언트임을 확인하기위해 존재한다
+ 어디에 사용되는가(Where)
  - 로그인 정보유지에 사용
### 쿠키(Cookie)
+ 사용자 정보를 클라이언트 로컬에 직접 저장하는 것
+ 왜 사용되는가(Why)
  - 
+ 어디에 사용되는가(Where)
  - 자동로그인( 아이디,비밀벉호,방문사이트의 정보를 담은 임시파일로써 저장되어 해당 웹서버에 재방문시 자동으로 로그인됨)
  - 팝업 창 제어(ex.오늘 더이상 이창을 보지 않음)
  - 쇼핑몰 장바구니 상품 유지

### 차이점
+ 저장위치
> 쿠키 : 클라이언트 로컬에 파일로 저장 
> 세션 : 서버
+ 보안
> 쿠키 : 보안에 취약 
> 세션 : 쿠키를 이용해서 세션id만 저장하고 서버에서 처리하므로 보안성 높음
+ 라이프 사이클
> 쿠키 : 사용자가 삭제해야함 
> 세션 : 브라우저종료(또는 특정시간 도달)시 삭제

*캐시*
+ 이미지,css,js파일 등이 클라이언트 브라우저에 저장되는 것
+ 자원이 아껴지며, 웹페이지 로딩 속도가 향상됨
+ 한번 캐시에 저장되면 서버가 변경되어도 사용자는 변경되지 않을 수도 있음
 - 이경우, 캐시를 지워주거나 서버에서 클라이언트로 응답을 보낼 때 header에 캐시 만료시간을 명시해서 해결가능
