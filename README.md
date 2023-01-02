
<!--
**miaarosie/miaarosie** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
# Team Project2
## Keyboar-der / K-Manager
수수료내역, 매출 등 다양한 형태의 정산데이터와 주문관련 데이터 등 <br>
다양한 서비스를 제공하는 판매자 맞춤형 오픈마켓 시스템 웹사이트 제작

### 1. 프로젝트 기간 :calendar:
---
+ 프로젝트 기간 : 2022년 11월 15일 ~ 2022년 12월 23일
+ 팀원 수 : 6명

![20230102_121021](https://user-images.githubusercontent.com/114273783/210192719-41f99cb2-27b0-4ec8-a9b5-2826f0206d2e.png)

### 2. 주요기능 :pushpin:
---
+ 소비자(FO)

  + 메인 : 회원가입 / 로그인,로그아웃 / 아이디,비밀번호찾기
  + 상품 : 상품전체조회 / 상품주문 / 상품결제 / 상품주문취소
  + 주문 : 주문내역 전체조회 / 주문내역 상세조회
  
+ 판매자(PO)

  + 메인 : 회원가입(이메일인증) / 로그인,로그아웃 / 정산,상품,판매현황,공지사항조회
  + 주문 : 전체주문내역조회 / 구매확정내역조회 / 배송관리
  + 상품 : 상품전체조회 / 상품추가,수정,삭제
  + 쿠폰 : 쿠폰전체조회 / 만료쿠폰조회 / 사용가능쿠폰조회 / 쿠폰등록,수정 / 쿠폰사용내역조회
  + 정산 : 정산내역조회 / 정산상세내역조회 / 전자세금계산서관리 / 수수료내역정산예정금 조회
  + 판매자정보 : 판매자정보수정 / 정산금 잔액관리 / 판매자탈퇴 / 1:1문의게시판(글등록,조회)
  
+ 관리자(BO)

  + 메인 : 로그인,로그아웃 / 전체매출통계 / 전체상품통계
  + 주문 : 전체주문내역조회
  + 정산 : 수수료매출조회 / 입점업체 정산금관리
  + 쿠폰 : 쿠폰전체조회 / 만료쿠폰조회 / 사용가능쿠폰조회 / 쿠폰등록,수정 / 쿠폰사용내역조회
  + 통계 : 업체별 매출통계 / 상품별 매출통계

### 3. 개발환경 :computer:
***
+ OS : Window10
+ FW : Spring Framework
+ WAS : Apache Tomcat 8.5
+ DB  : Oracle DB
+ Front-end : HTML5 / CSS / JavaScript / jQuery / Ajax / Gson
+ Back-end : JDK1.8 / JSP / JSTL
+ Developer Tools : STS / Sql Developer / VS Code
+ GitHub

### 4. 담당역할 :information_desk_person:
---
+ 소비자(FO)

  + 로그인, 로그아웃 / 회원가입(이메일인증) / 아이디 및 비밀번호 찾기(이메일인증)
+ 판매자(PO) 

  + 구매확정내역조회 / 구매확정내역 엑셀파일다운로드
  + 전체정산내역조회 / 전체정산내역 엑셀파일다운로드
  + 1:1문의 등록 및 답변 조회
+ 관리자(BO)

  + 1:1 문의 글 조회 및 답변등록 및 관리

### 5. 기능구현 :mag_right:
---
#### 소비자(FO)

+ 회원가입 페이지
![20230102_134435](https://user-images.githubusercontent.com/114273783/210195794-5a487d43-8b8d-47bf-85eb-ea671e24c6ce.png)
:pencil2: 기능구현 설명 <br>
``` 
  모든 약관에 동의 후 넘어간 회원가입 페이지에서 Ajax를 활용하여 아이디와 이메일 중복체크를 진행 후, 
  다음 주소API를 사용하여 주소를 입력받고 JavaScript를 활용하여 입력받은 값에 대하여 모든 유효성 검사를 실행 후,
  조건이 충족되었을 때만 가입버튼이 활성화 되도록 기능구현을 하였습니다.
  googleSMTP서버를 사용하여 가입하기 버튼을 클릭 하였을 때 입력한 이메일로 인증메일이 발송되도록 진행하였고,
  이메일인증을 완료했을 때에만 로그인이 가능하도록 기능구현을 실행하였습니다.
```   
+ 로그인 / 로그아웃 페이지 
![20230102_140252](https://user-images.githubusercontent.com/114273783/210196500-a7eb1f61-0ac7-4a83-b3f7-4255dcf0b484.png)<br>
:pencil2: 기능구현 설명 <br>
```
  소비자 로그인 페이지 화면입니다.
  메인 상단 버튼을 통해 로그인 모달창이 띄워지도록 하였고, 회원가입 이메일 인증을 한 계정만 로그인이 가능하게 기능구현을 하였습니다.
  만약 이메일인증이 안된 계정일 경우, 메인페이지로 이동하게 설정하였습니다.
```  
  
+ 아이디 찾기 페이지
![20230102_133413](https://user-images.githubusercontent.com/114273783/210195376-45a7b3ff-11b3-49a5-8b1a-57695314b593.png)

:pencil2: 기능구현 설명 <br>
```
  소비자가 회원가입 시 입력한 이름과 핸드폰 번호와 인증을 실행한 이메일주소를 JavaScript를 사용하여 유효성 검사 실행 후 
  조건이 충족되었을 때 아이디찾기 버튼이 활성화 되도록 기능구현을 하였고,
  Ajax를 사용하여 입력받은 세가지의 정보가 모두 일치한 계정의 아이디를 찾을 수 있도록 기능구현을 하였습니다.
```

+ 비밀번호 찾기 페이지

![20230102_133116](https://user-images.githubusercontent.com/114273783/210195250-06a3b9fd-6525-46f0-b55c-ffa3ac76d7ba.png)

:pencil2: 기능구현 설명 <br>
