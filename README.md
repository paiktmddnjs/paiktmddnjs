<style>
body {
  /* text-align: center; */
}

.app {
  padding: 1rem;
}

.row {
  display: flex;
  position: relative;
  flex-wrap: wrap;
}

.panel {
  width: 100%;
  position: relative;
  max-width: 911px;
}

@media (min-width: 1350px) {
  .panel {
    width: calc(100% - 1000px);
  }
}

.result {
  width: 100vw;
  max-width: 911px;
  position: relative;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.result img {
  max-width: 100%;
}


@media (min-width: 1350px) {
  .result {
    min-width: 1000px;
    width: 1000px;
    position: fixed;
    right: 0;
    top: 10;
    height: 100vh;
    width: 400px;
    overflow-y: auto;
    background: #fff;
    box-sizing: border-box;
    z-index: 999;
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: center;
  }
}

.result .url {
  max-width: 100%;
  margin: 20px auto;
  background: #eee;
  color: blue;
  padding: 1rem;
  font-size: 16px;
  border-radius: 8px;
  word-break: break-all;
  text-align: left;
  cursor: pointer;
}

.result .copy-btn {
  border: none;
  background: #494949;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 0.25rem;
  font-size: 1rem;
  font-weight: bold;
  cursor: pointer;
}

.result .copy-btn:hover {
  background: #5a5a5a;
}

.options {
  border: 1px solid #e7e7e7;
  flex-wrap: wrap;
  display: flex;
  justify-content: space-between;
}

.group {
  text-align: left;
  width: 100%;
  flex: 0 0 100%;
  margin: 0.75rem 0rem;
}

.group label {
  margin-left: 1rem;
}

@media (min-width: 1700px) {
  .group {
    width: 49%;
    flex: 0 0 49%;
  }
}

.desc {
  margin: 0px;
  color: #979797;
  font-size: 13px;
  margin-left: 1rem;
}

.desc a {
  color: #979797;
}

.group-head {
  padding: 4px 0px 4px 16px;
  width: calc(100% - 16px);
  flex: 0 0 calc(100% - 16px);
  background: #494949;
  color: white;
  margin: 0px;
}
</style>

## Hi there 👋

<!--
**paiktmddnjs/paiktmddnjs** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:


- :coffee: I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
## :coffee: 나의 프로젝트명 (Project Name) : Servlet와 JSP을 이용한 MVC 패턴 기반으로 회원가입, 조회 등을 구현하는 웹 어플리케이션!!


## 📘 개요 (Overview)

- 본 프로젝트는 **Servlet과 JSP를 이용한 MVC 패턴 기반의 웹 애플리케이션**으로,  
	회원 관리(로그인·회원가입) 및 게시판 CRUD 기능을 중심으로 구성되었습니다.  
	Oracle 데이터베이스와 JDBC를 통해 데이터 연동을 수행하며,  
	Eclipse + Tomcat 환경에서 실행 가능합니다.


## 🧱 기술 스택 (Tech Stack)
| 구분 | 사용 기술 |
|------|------------|
| Frontend | HTML, CSS, JavaScript, JSP |
| Backend | Java (Servlet, JDBC)|
| Server| Apache Tomcat |
| Database | Oracle |
| Tools | Eclipse, Git, GitHub |


## 🛠️ 설치 및 실행 (Installation & Run)
# 1. 프로젝트 클론
git clone https://github.com/paiktmddnjs/JSP/tree/main/jspProject


# 2. 이클립스(Eclipse)에서 Import
- File > Import > Existing Projects into Workspace
- 복제한 프로젝트 폴더 선택 후 Import


# 3. 데이터베이스(Oracle) 설정
- Oracle 실행 후 데이터베이스 및 테이블 생성
- src/main/webapp/WEB-INF/classes/sql 폴더 내 SQL 스크립트의 각 테이블 생성
- JDBC 연결 정보(application.properties 또는 JDBCTemplate.java) 수정


# 4. Tomcat 서버 설정
- Eclipse > Servers > New > Server > Apache Tomcat 선택
- 프로젝트를 서버에 Add 후 실행


# 5. 웹 애플리케이션 실행
- 브라우저에서 접속
http://localhost:8080/jspProject



## 📂 프로젝트 구조 (Directory Structure)
project/
 ├── src/main/java
                ┣ 📂common
                     ┗ 📜JDBCTemplate.java
                ┣ 📂controller
                ┣ 📂board
                      ┣ 📜DeleteDetailForm.java
                      ┣ 📜DetailController.java
                      ┣ 📜DetailUpdateView.java
                      ┣ 📜EnrollFromController.java
                      ┣ 📜InsertBoardController.java
                      ┣ 📜ListController.java
                      ┗ 📜UpdateFormController.java
                ┣ 📂member
                       ┣ 📜DeleteController.java
                       ┣ 📜EnrollFromController.java
                       ┣ 📜InsertController.java
                       ┣ 📜LoginController.java
                       ┣ 📜LogoutController.java
                       ┣ 📜MyPageController.java
                       ┣ 📜UpdateController.java
                       ┗ 📜UpdatePwdController.java
                ┗ 📂reply
                        ┣ 📜insertReplyController.java
                        ┗ 📜ReplyController.java
                ┣ 📂model
                ┣ 📂dao
                        ┣ 📜BoardDao.java
                        ┣ 📜FileDao.java
                        ┣ 📜MemberDao.java
                        ┗ 📜ReplyDao.java
                ┗ 📂vo
                        ┣ 📜Board.java
                        ┣ 📜FileUpload.java
                        ┣ 📜Member.java
                        ┗ 📜Reply.java
                ┗ 📂service
                        ┣ 📜BoardService.java
                        ┣ 📜FileService.java
                        ┣ 📜MemberService.java
                        ┗ 📜ReplyService.java
                ┗ 📂db
                ┣ 📂driver
                        ┗ 📜driver.properties
                ┗ 📂sql
                        ┣ 📜board-mapper.xml
                        ┣ 📜file-mapper.xml
                        ┣ 📜member-mapper.xml
                        ┗ 📜reply-mapper.xml                 # 공용 유틸 (JDBCTemplate 등)

              
 ├── webapp/
     ├── WEB-INF/
        ├── views/                                                 # JSP 뷰 페이지
            ┣ 📂board
                  ┣ 📜detailView.jsp
                  ┣ 📜enrollFrom.jsp
                  ┣ 📜listView.jsp
                  ┗ 📜updateForm.jsp
            ┣ 📂common
                  ┣ 📜error.jsp
                  ┗ 📜menubar.jsp
            ┗ 📂member
                  ┣ 📜enrollForm.jsp
                  ┗ 📜myPage.jsp
        └── web.xml                                                # 배포 서술자
     ├── resources/                                                 # CSS, JS, 이미지
     └── index.jsp                                                  # 메인 페이지
 └── README.md

 


## 🌟 주요 기능 (Key Features)
✅ 회원가입 / 로그인 / 로그아웃 / 게시판 등록, 조회/ 댓글 등록 / 파일 첨부 기능
✅ 게시글 등록, 조회, 수정, 삭제 (CRUD)
✅ Oracle DB 연동을 통한 데이터 관리
✅ MVC 패턴 기반 구조로 모듈화된 개발
✅ JSP include를 통한 공통 레이아웃 구성

## 📸 화면 미리보기 (Preview)

| 기능 | 미리보기 |
|------|-----------|
| 로그인 화면 | ![Login Page](./assets/login.gif) |
| 회원가입 화면 | ![Register Page](./assets/register.png) |
| 게시판 목록 | ![Board List](./assets/board-list.jpg) |
| 게시글 작성 | ![Post Write](./assets/post-write.gif) |


## 💡 학습 포인트 (Learning Points)

- JSP & Servlet 기반 MVC 구조 설계 방법 학습
- JDBC를 통한 데이터베이스 연결 및 SQL 처리 로직 구현
- Tomcat 서버를 활용한 배포 및 실행 환경 이해
- JSP 내 JSTL / EL 사용으로 동적 페이지 구현

