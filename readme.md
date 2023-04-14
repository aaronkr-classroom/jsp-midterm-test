# Midterm Test / 중간고사

중간고사는 2가지 부분으로 이루어집니다.

1. 온라인 퀴즈 ([스터디 가이드](https://ut-nodejs.github.io/midterm.html))
2. 중간 프로젝트 (아래 지시사항 참조)

![Midterm Test](https://github.com/ut-nodejs/ut-nodejs.github.io/blob/master/img/in-slides/tests/midterm-index.png)

이 시험은 **OPEN BOOK**입니다. 인터넷, 책, 노트 등을 포함한 모든 자료를 사용할 수 있습니다. 시험 중에 다른 학생과 통신하거나 다른 자료를 사용할 수 없습니다.

이 중간 프로젝트는 온라인 퀴즈와 함께 **최종 성적의 15%** 를 차지합니다.

- 온라인 퀴즈: **5%**
- 중간 프로젝트: **10%**
- 총점: **15%**

---

## **TEST:** Instructions / **시험:** 지시사항

### **Unit 2** Capstone / 유닛 2 캡스톤

1. 익스프레스 웹 서버를 만들어 주어진 웹 페이지를 표시하세요.
2. `layout.ejs`를 사용하여 EJS partials와 페이지를 나누세요.
3. `homeController`는 모든 애플리케이션 라우트(GET 및 POST)를 처리하고 `errorController`는 모든 애플리케이션 오류를 처리합니다.

Express 웹 서버를 만들어 주어진 웹 페이지를 표시하도록 하세요. `layout.ejs`를 사용하여 EJS partials와 페이지를 나누세요.

브라우저에서 주어진 파일을 미리 보려면 `views` 폴더에서 파일을 마우스 오른쪽 버튼으로 클릭하고 **"경로 복사"** 를 선택한 다음 브라우저의 주소 표시줄에 붙여 넣으세요.

수업에서 작업한 것처럼 이 웹 사이트는 다섯 개의 페이지로 구성됩니다.

- `index.html` - GET 메소드로 접근 가능
- `transportation.html` - GET 메소드로 접근 가능
- `contact.html` - GET과 POST 메소드로 접근 가능
- `thanks.html` - POST 메소드 후에 접근 가능
- `error.html` - 에러 발생 시 접근 가능

HTML 파일만 제공되었기 때문에 EJS 파일을 만들고 페이지를 표시하는 라우트를 설정해야 합니다.

`views` 폴더에 `layout.ejs` 파일을 만들어 레이아웃을 설정합니다. `layout.ejs` 파일에 HTML `head`와 `body` 태그를 포함시킵니다. `head` 태그에는 `meta` 태그와 `title` 태그를 자신의 정보로 업데이트합니다.

`partials` 폴더와 다음 부분을 만들어야합니다.

- `header.ejs` - 모든 페이지에 사용되는 헤더
- `navigation.ejs` - 모든 페이지에 사용되는 네비게이션 메뉴
- `footer.ejs` - 모든 페이지에 사용되는 푸터
- `confetti.ejs` - thanks 페이지에 사용되는 confetti

---

### Detailed Steps / 자세한 단계

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

### Given files / 주어진 파일

```bash
|___/views                    # <CHANGE> .ejs로 확장자 변경
| |___index.html                # GET 메소드로 접근 가능
| |___transportation.html       # GET 메소드로 접근 가능
| |___contact.html              # GET과 POST 메소드로 접근 가능
| |___thanks.html               # POST 메소드 후에 접근 가능
| |___error.html                # 에러 발생 시 접근 가능

|___/public                   # <NO CHANGES> 안 바뀜
| |___css
| | |___style.css
| | |___style.small.css         # 반응형 웹 디자인을 위한 CSS
| | |___bootstrap.min.css       # 부트스트랩 CSS
| | |___bootstrap.min.css.map   # 부트스트랩 CSS 맵
| | |___confetti.css            # thanks.html에 사용된 CSS
| |___img
| | |___dribbble_404.gif        # error.html에 사용된 이미지
| |___js
| | |___functions.js            # 반응형 메뉴를 위한 JS
| | |___bootstrap.bundle.min.js # 케러셀을 위한 부트스트랩 JS
| | |___bootstrap.bundle.min.js.map
```

---

### Requirements / 요구사항

다음 파일과 폴더가 프로젝트에 있어야 합니다.

```bash
|___/views
| |___/partials               # <NEW>
| | |___header.ejs              # 모든 페이지에 사용되는 헤더
| | |___footer.ejs              # 모든 페이지에 사용되는 푸터
| | |___navigation.ejs          # 모든 페이지에 사용되는 네비게이션 바
| | |___confetti.ejs            # thanks.html에 사용되는 confetti
| |___layout.ejs              # <NEW> 모든 페이지의 레이아웃
| |___index.ejs                 # GET 메소드로 접근 가능
| |___transportation.ejs        # GET 메소드로 접근 가능
| |___contact.ejs               # GET과 POST 메소드로 접근 가능
| |___thanks.ejs                # POST 메소드 후에 접근 가능
| |___error.ejs                 # 에러 발생 시 접근 가능

|___/public                   # <NO CHANGES> 안 바뀜
| |___css
| | |___style.css
| | |___style.small.css         # 반응형 웹 디자인을 위한 CSS
| | |___bootstrap.min.css       # 부트스트랩 CSS
| | |___bootstrap.min.css.map   # 부트스트랩 CSS 맵
| | |___confetti.css            # thanks.html에 사용된 CSS
| |___img
| | |___dribbble_404.gif        # error.html에 사용된 이미지
| |___js
| | |___functions.js            # 반응형 메뉴를 위한 JS
| | |___bootstrap.bundle.min.js # 케러셀을 위한 부트스트랩 JS
| | |___bootstrap.bundle.min.js.map

|___/controllers              # <NEW>
| |___homeController.js         # 모든 라우트를 처리하는 컨트롤러
| |___errorController.js        # 모든 에러를 처리하는 컨트롤러

|___main.js                   # <NEW> Express 서버를 설정하는 파일
|___package.json              # <NEW> npm init을 통해 생성된 파일
|___package-lock.json
```

---

## **BONUS:** Optional (if time) / **보너스:** 선택사항 (시간이 남는다면)

### **Unit 3** Capstone / 유닛 3 캡스톤

시간이 남는다면 다음 기능을 구현해보세요 (보너스 점수):

1. MongoDB와 Mongoose를 프로젝트에 추가하여 연락처 양식 데이터를 저장하세요.
2. `models` 폴더에 구독자 모델을 만들어 뉴스레터를 구독하는 사람들의 이메일 주소를 저장하세요.
3. `/contact`에 POST 요청을 처리하는 `subscribersController`를 만드세요.

---

### Detailed Steps / 자세한 단계

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

---

### Subscriber Table Starter Code / 구독자 테이블 시작 코드

```js
// views/subscribers.ejs
<h1 class="mb-3">Subscribers</h1>
<table class="table table-hover">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">Name</th>
      <th scope="col">Email</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob Thornton</td>
      <td>@jaket</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>Larry the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>
</table>
```

---

### Additional Files / 추가 파일

보너스 섹션을 작업하기로 결정하면 다음 파일을 프로젝트에 추가해야 합니다.

```bash
|___/models
| |___subscriber.js             # <NEW> Subscriber 모델

|___/controllers
| |___subscribersController.js  # <NEW> Subscriber 컨트롤러

|___/views
| |___subscribers.ejs           # <NEW> Subscriber 페이지
```

`main.js`를 수정하여 데이터베이스에 연결하고 새 라우트를 처리해야 합니다.