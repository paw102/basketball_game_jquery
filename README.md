<h1>🏀 Basketball Game Project</h1>

![latestversion](https://img.shields.io/badge/latest_Version-3.0-blue)

---

<h1>📖 프로젝트 소개</h1>

이 프로젝트는 컴퓨터와 사용자가 번갈아 가면서 슛을 시도하여 더 높은 점수를 얻는 쪽이 승리하는 간단한 농구 게임입니다. 초기 버전에서는 `Vanilla JavaScript` 로 구현했으며, 이후 객체화와 함수화 과정을 통해 코드를 개선했습니다. 마지막으로 `jQuery` 를 도입하여 DOM 조작 및 이벤트 처리 방식을 더 간결하게 만들었습니다. 

---


<h2>🕰️ 버전 히스토리</h2>

<h3>✅ 1. 초기 버전 (Vanilla JavaScript)</h3>

DOM 조작: `document.getElementById()`, `document.getElementsByClassName()` 사용 

이벤트 처리: `onclick` 속성을 사용하여 버튼 클릭 이벤트 처리

전역 변수 사용: `userScore`, `comScore`, `shootLeft` 등 전역 변수로 게임 상태 관리

로직 구현: 순차적인 절차 지향 프로그래밍 방식으로 작성

---

<h3>♻️ 2. 리팩토링</h3>

코드 중복 제거: 점수 업데이트, 버튼 활성화/비활성화 등의 기능을 함수화

객체화: `game`, `computer`, `user` 객체를 도입하여 관련 변수를 묶음

- computer 객체 내에 `score`, `percent2` , `percent3` 속성을 대입했고 이는 초기 ver 의 `comScore` , `comPercent2` , `comPercent3` 를 리팩토링 한 사례에 해당함

동적 속성 접근: `computer['percent' + shootType]` 방식으로 속성에 동적으로 접근
- 초기 버전의 어느 부분이 수정 되었는 지를 직접적으로 명시한다면 좀 더 좋은 README 에 해당

AI 로직 추가: 점수 차이에 따라 컴퓨터의 슛 성공 확률이 조정되도록 구현

---

<h3>💡 3. jQuery 도입</h3>

DOM 셀렉션: `$('#user-score'), $('.btn-computer')` 등 CSS 선택자 문법을 사용해 더 직관적인 DOM 접근

이벤트 처리: `.on()` 메서드를 통해 이벤트 바인딩

애니메이션 효과: `.fadeIn()`, `.fadeOut()`과 콜백 함수 사용으로 자연스러운 전환 효과 추가

플러그인 사용: `jquery.animateNumber` 플러그인을 통해 점수판의 숫자 애니메이션 적용

---

<h2>⚙️ 주요 개념 및 원리 (Key Concepts & Principles)</h2>

---

<h3>📌 1. DOM 조작</h3>

`Vanilla JS` 에서는 `innerHTML` 을 사용하여 텍스트를 업데이트했지만, `jQuery` 에서는 `.html()`로 더 간단하게 처리함

버튼 비활성화는 `element.disabled = true` 대신 `.prop('disabled', true)` 로 구현

<h3>💥 2. 이벤트 처리</h3>

초기에는 `onclick` 속성을 사용했으나, `jQuery` 에서는 `.on('click', function() {})` 으로 더 깔끔하게 이벤트를 처리함

이벤트 리스너를 분리하여 코드의 가독성을 높임

<h3>🌍 3. 전역 변수와 지역 변수</h3>

초기에는 모든 게임 상태를 전역 변수로 관리했으나, 객체와 함수의 도입으로 전역 변수 사용을 최소화

`game`, `computer`, `user` 객체를 통해 상태와 관련 로직을 관리함

<h3>🔁 4. 콜백 함수와 비동기 처리</h3>

`.fadeOut()`과 `.fadeIn()` 을 콜백 함수로 연결하여 화면 전환 시 깜빡이는 현상을 제거함

비동기 함수의 제어권 반환과 콜백 함수의 실행 순서를 이해함

---

<h2>🆚 jQuery 적용의 장단점</h2>

---

<h3>✅ 장점</h3>

코드의 간결화: `document.getElementById()` 대신 `$('#id')` 로 간단하게 접근

체이닝(Chaining) : 여러 메서드를 연속적으로 호출하여 코드의 가독성을 높임

크로스 브라우징(Cross-Browsing) : 다양한 브라우저에서 일관된 동작 보장

다양한 플러그인 사용 가능: 추가 기능을 손쉽게 도입할 수 있음

<h3>❌ 단점</h3>

추가적인 라이브러리 로드로 인한 성능 저하 가능성

최신 `JavaScript` 에서는 `querySelector()` 및 `querySelectorAll()` 로 유사한 기능을 제공

---

<h2>📚 배운 점과 앞으로의 과제</h2>

---

<h3>🎯 배운 점</h3>

`Vanilla JS` 와 `jQuery` 의 차이점 및 장단점 이해

`DOM` 조작 및 이벤트 처리의 효율적인 방법 학습

비동기 함수와 콜백 함수의 사용법 익힘

코드 리팩토링을 통해 유지보수성과 가독성 개선

<h3>🚀 앞으로의 과제</h3>

`JavaScript` 의 최신 기능 `ES6+` 을 도입하여 코드 개선

더 복잡한 AI 로직을 추가하여 게임의 재미 요소 강화

CSS 애니메이션과 트랜지션을 사용해 더 자연스러운 사용자 경험 제공

---

<h2>💻 프로젝트 실행 방법</h3>

---

<h3>📥 1. 코드 다운로드</h3>

`$ git clone https://github.com/paw102/basketball_game_jquery.git`

`$ cd basketball_game_jquery`

<h3>🚀 2. 로컬 서버 실행 </h3>

단순히 파일을 브라우저에서 열어도 실행이 가능합니다

또는 `Live Server` 플러그인을 사용하면 더 편리합니다

<h3>🌐 3. 브라우저에서 실행</h3>

`index.html` 파일을 브라우저에서 열어 게임을 시작하세요

---
<h2>🏁 마무리</h2>

---

이 프로젝트는 `JavaScript` 와 `jQuery` 를 사용하여 단계적으로 기능을 개선해 나가는 과정을 통해 더 효율적이고 유지보수하기 쉬운 코드를 작성하는 방법을 배울 수 있었습니다. 앞으로도 최신 기술을 적용하여 더 발전된 프로젝트로 확장해 나가겠습니다.

---

👤 Author: paw102

🗓️ Last Updated: 2025-02-20

---