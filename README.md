
<br>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&text=Paiktmddnjs&fontAlign=30&fontSize=30&textBg=true&desc=Welcome%20Paik's%20Project&descAlign=60&descAlignY=50" alt="Paiktmddnjs Banner" />
</div>



<br>
<br>

<div align="center"> ### 💻 Language </div>

<br>

<div align="center">
<img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=Java&logoColor=white"/>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=JavaScript&logoColor=black"/>
<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=HTML5&logoColor=white"/>
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=CSS3&logoColor=white"/>
</div>

<br>
<br>

<div align="center">

![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=paiktmddnjs&show_icons=true&theme=transparent) 
&ensp;
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=paiktmddnjs&layout=compact)
	
</div>


<br>
<br>



  <h1><span>☕</span> 나의 프로젝트명 (Project Name)</h1>
  <p>
    Servlet와 JSP을 이용한 MVC 패턴 기반으로 회원가입, 조회 등을 구현하는 웹 어플리케이션!!
  </p>
  
  <br>


## 📘 개요 (Overview)

- 본 프로젝트는 **Servlet과 JSP를 이용한 MVC 패턴 기반의 웹 애플리케이션**으로,  
	회원 관리(로그인·회원가입) 및 게시판 CRUD 기능을 중심으로 구성되었습니다.  
	Oracle 데이터베이스와 JDBC를 통해 데이터 연동을 수행하며,  
	Eclipse + Tomcat 환경에서 실행 가능합니다.

<br>

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

<br>

## 📂 프로젝트 구조 (Directory Structure)

<pre>
project/
 ├── src/main/java
                ┣ 📂common
                     ┗ 📜JDBCTemplate.java
                ┣ 📂controller
                ┣ 📂board
                      ┣ 📜DeleteDetailForm.java				// 상세 게시판에 대해 삭제하는 서블릿 컨트롤러이다. 
                      ┣ 📜DetailController.java				// 상세 게시판을 출력하기 위한 서블릿 컨트롤러이다.
                      ┣ 📜DetailUpdateView.java				// 상세 게시판을 수정페이지로 가기위한 서블릿 컨트롤러이다.
                      ┣ 📜EnrollFromController.java			// 게시글을 등록하기 위한 서블릿 컨트롤러이다.
                      ┣ 📜InsertBoardController.java		// 게시글을 등록할때 정보를 Oracle로 저장하기위한 서블릿 컨트롤러이다.
                      ┣ 📜ListController.java				// 게시판을 들어갔을때 게시글들이 나오도록 처리하는 서블릿 컨트롤러이다.
                      ┗ 📜UpdateFormController.java			// 상세 페이지를 수정하기 위해 처리하는 서블릿 컨트롤러이다.
                ┣ 📂member
                       ┣ 📜DeleteController.java			// 회원 정보를 삭제 처리를 위한 서블릿 컨트롤러이다.
                       ┣ 📜EnrollFromController.java		// 회원가입을 위한 페이지로 이동을 처리하기 위한 서블릿 컨트롤러이다.
                       ┣ 📜InsertController.java			// 회원가입을 위해 정보를 Oracle로 insert 처리하기 위한 서블릿 컨트롤러이다.
                       ┣ 📜LoginController.java				// 회원의 로그인을 처리하기위한 서블릿 컨트롤러이다.
                       ┣ 📜LogoutController.java			// 로그아웃을 위한 서블릿 컨트롤러이다.
                       ┣ 📜MyPageController.java			// 로그인후 마이페이지로 가기 위한 처리를 하는 서블릿 컨트롤러이다.
                       ┣ 📜UpdateController.java			// 회원정보의 수정을 처리하기 위한 서블릿 컨트롤러이다.			
                       ┗ 📜UpdatePwdController.java			// 마이페이지에서 비밀번로 수정을 처리하기 위한 서블릿 컨트롤러이다.
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
                        ┗ 📜reply-mapper.xml              

              
 ├── webapp/
     ├── WEB-INF/
        ├── views/                                                
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
        └── web.xml                                             
     ├── resources/                                             
     └── index.jsp                                                
 └── README.md
</pre>
 
<br>

## 🌟 주요 기능 (Key Features)
✅ 회원가입 / 로그인 / 로그아웃 / 게시판 등록, 조회/ 댓글 등록 / 파일 첨부 기능 <br>
✅ 게시글 등록, 조회, 수정, 삭제 (CRUD) <br>
✅ Oracle DB 연동을 통한 데이터 관리 <br>
✅ MVC 패턴 기반 구조로 모듈화된 개발 <br>
✅ JSP include를 통한 공통 레이아웃 구성

<br>

## 📸 화면 미리보기 (Preview)

| 기능 | 미리보기 |
|------|-----------|
| 로그인 화면 | ![Login Page](./assets/login.gif) |
| 회원가입 화면 | ![Register Page](./assets/register.png) |
| 회원 탈퇴 | ![Post Write](./assets/post-write.gif) |
| 회원정보 수정 | ![Post Write](./assets/post-write.gif) |
| 게시판 목록 | ![Board List](./assets/board-list.jpg) |
| 게시글 작성 | ![Post Write](./assets/post-write.gif) |
| 게시글 삭제 | ![Post Write](./assets/post-write.gif) |
| 댓글 작성 | ![Post Write](./assets/post-write.gif) |

<br>

## 💡 학습 포인트 (Learning Points)

- JSP & Servlet 기반 MVC 구조 설계 방법 학습
- JDBC를 통한 데이터베이스 연결 및 SQL 처리 로직 구현
- Tomcat 서버를 활용한 배포 및 실행 환경 이해
- JSP 내 JSTL / EL 사용으로 동적 페이지 구현

