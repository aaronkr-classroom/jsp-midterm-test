# **UT-NodeJS** Midterm Checklist / 중간고사 체크리스트

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