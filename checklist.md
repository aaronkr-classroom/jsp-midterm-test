# **UT-NodeJS** Midterm Checklist / 중간고사 체크리스트

## **TEST:** Instructions / **시험:** 지시사항

### **Unit 2** Capstone Detailed Steps / 유닛 2 캡스톤 자세한 단계

- [ ] **(1) `npm init` 명령을 실행하여 Node.js 프로젝트를 시작하세요.**
- [ ] **(2) 프로젝트에 다음 패키지를 설치하세요.**
  - [ ] `http-status-codes`
  - [ ] `express`
  - [ ] `ejs`
  - [ ] `express-ejs-layouts`
- [ ] **(3) `main.js` (또는 `app.js`) 파일을 만들고 Express 서버를 설정하세요.**
- [ ] **(4) `views` 폴더 안에 `partials` 폴더를 만들고 다음 partials를 만드세요.**
  - [ ] `header.ejs` - 모든 페이지에 사용되는 헤더
  - [ ] `footer.ejs` - 모든 페이지에 사용되는 푸터
  - [ ] `navigation.ejs` - 모든 페이지에 사용되는 네비게이션 바
  - [ ] `confetti.ejs` - thanks 페이지에 사용되는 confetti
- [ ] **(5) 주어진 HTML 파일의 확장자를 `.ejs`로 변경하고 `views` 폴더에 `layout.ejs` 파일을 추가하여 레이아웃을 설정합니다.**
  - [ ] `layout.ejs` - 모든 페이지의 레이아웃
    - [ ] `head` - `meta` 태그와 `title` 태그를 자신의 정보로 업데이트합니다.
  - [ ] `index.ejs` - GET 메소드로 접근 가능
  - [ ] `transportation.ejs` - GET 메소드로 접근 가능
  - [ ] `contact.ejs` - GET과 POST 메소드로 접근 가능
  - [ ] `thanks.ejs` - POST 메소드 후에 접근 가능
  - [ ] `error.ejs` - 에러 발생 시 접근
- [ ] **(6) 다음 컨트롤러를 만들어 라우트와 에러를 처리하세요.**
  - [ ] `homeController` - 애플리케이션의 모든 라우트(GET과 POST)를 처리하는 컨트롤러
  - [ ] `errorController` - 애플리케이션 에러를 처리하는 컨트롤러

---

## **BONUS:** Optional (if time) / **보너스:** 선택사항 (시간이 남는다면)

### **Unit 3** Capstone / 유닛 3 캡스톤

- [ ] **(1) 프로젝트에 다음 패키지를 추가하세요.**
  - [ ] `mongodb`
  - [ ] `mongoose`
- [ ] **(2) `main.js`에서 MongoDB 연결과 Mongoose를 설정하세요.**
- [ ] **(3) `models` 폴더를 만들고 `Subscriber` 모델을 만들어 이메일 주소를 저장하세요.**
  - [ ] `name` - 이름을 저장하는 필드
  - [ ] `email` - 이메일 주소를 저장하는 필드
  - [ ] `module.exports`로 모델을 내보내지 않으면 안 됩니다.
- [ ] **(4) `subscribers.ejs` 페이지를 만들어 데이터베이스에 있는 모든 구독자를 반복해서 표시하세요.**
  - [ ] 아래에 구독자를 표시하는 데 도움이 되는 시작 코드가 있습니다. (`error.ejs`를 복사해서 수정해서 구독자를 표시할 수 있습니다.)
- [ ] **(5) `controllers` 폴더에서 `subscribersController`를 만들어 POST 요청을 처리하세요.**
  - [ ] `getAllSubscribers` - 데이터베이스에 있는 모든 구독자를 찾아 표시하세요. 
  - [ ] `getSubscriptionPage` - `contact.ejs`를 렌더링합니다.
    - [ ] `homeController.js`를 수정하여 `contact.ejs`를 렌더링하지 않도록 합니다.
  - [ ] `saveSubscriber` - 이메일 주소를 `Subscriber` 모델에 저장하고 `thanks.ejs` 렌더링.
  - [ ] `main.js`에 새 라우트를 추가하지 않으면 안 됩니다.