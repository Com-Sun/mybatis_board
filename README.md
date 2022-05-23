# mybatis_board

## 멤버

- 조현진
- 조재철

## 필수사항

* Spring MVC 프로젝트로 구현합니다.
* 모든 url 에 MockWebMvc 를 이용한 테스트 코드를 작성합니다.
* MyBatis 로 데이터 Access 를 합니다.
* 입력항목에 대한 Validation 은 화면과 서버에서 모두 확인합니다.
* 사용자(일반사용자, 관리자) 는 SQL 로 직접 데이터를 입력하세요.

## 기능

1. LOGIN
    * 사용자가 ID, PASSWORD 를 입력하여 로그인 기능을 제공합니다.
    * 로그인된 정보는 Session 에 남겨야 합니다.
2. 게시판 내용 (조회, 등록, 수정, 삭제 )
3. 게시판 댓글 ( 조회, 등록, 수정, 삭제 )

## 유스케이스 시나리오

### 기본기능 (5)

* 모든 사용자는 게시판의 목록을 볼 수 있습니다.
    * 게시판 내용의 목록은 번호, 제목, 작성자, (수정자), 작성일시, 댓글 개수 입니다.
    * 목록은 페이지 당 20개씩 보이고 페이지 넘기기를 할 수 있습니다.
* 모든 사용자는 게시판의 내용을 볼 수 있습니다.
    * 게시판 내용은 번호, 제목, 내용, 작성자, 수정자, 작성일시, 수정일시, 댓글 목록 입니다.
* 로그인 한 사용자는 게시판에 내용을 등록할 수 있습니다.
* 게시판 내용을 작성한 사람은 내용을 수정하거나 삭제할 수 있습니다.
* 로그인 한 사용자는 게시판의 내용을 보고 댓글(comment)을 등록할 수 있습니다.
* 관리자는 모든 게시판 내용을 삭제 할 수 있습니다.
* 관리자는 삭제한 게시판 내용을 복구 할 수 있습니다.

### 추가 점수 1 (2)

* 게시판 내용을 등록할 때 파일을 업로드 할 수 있습니다.
* 로그인한 사용자는 게시판 내용의 파일을 다운로드 할 수 있습니다.
* 로그인한 사용자는 게시판 내용에 대해 좋아요를 등록할 수 있습니다.
* 좋아요를 등록한 사용자는 좋아요 취소를 할 수 있습니다.

### 추가 점수 2 (1)

* 로그인한 사용자는 게시판 내용에 대해 답글(reply)을 쓸 수 있습니다.
* 로그인한 사용자는 게시판 내용에 대해 답글에 대한 답글을 등록할 수 있습니다.
* 게시판 목록에서 답글은 최대 5 단계까지 깊이를 제공합니다.

### 추가점수 3 (1)

* 좋아요를 등록 사용자는 좋아요한 게시판 내용 목록을 조회할 수 있습니다.
* 모든 사용자는 제목에 대한 게시판 목록을 검색할 수 있습니다.
    * 검색시 SQL 의 like 를 사용하세요. Wild Key(%) 의 위치에 따라 index 사용여부에 주의 하세요.

### 추가점수 4 (1)

* XSS 공격에 대한 방어를 하세요.
    * [https://github.com/naver/lucy-xss-servlet-filter](https://github.com/naver/lucy-xss-servlet-filter)
    * AbstractAnnotationConfigDispatcherServletInitializer 를 사용하세요.
* 게시판 목록에 조회수를 표시합니다. 동일사용자는 여러번 조회하더라도 조회수가 1개만 추가됩니다.

## 산출물

* 데이터베이스 설계서 (ERD)
* 테이블 생성 DDL
* 동작하는 소스코드
* 테스트 코드


