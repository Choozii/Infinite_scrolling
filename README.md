# Infinite scroll

무한 스크롤 연습용 코드
reference : web dev simplified

### 실행 방법

- npm install
- npm run

### 코드 구조

- App.js
	- 마지막 책 여부에 따라(useRef) 콜백 함수 내부에서 스크롤 끝 감지(IntersectionObserver) 후 페이지 값을 바꿔주는 로직
	- 화면 렌더링
	- loading, error 시 해당 문구 화면에 출력
  
- useBookSearch(custom hook)
	-  api call using axios
	- 상태값 받아와서 리턴

### 새롭게 배운 것!

- cancelToken : 새로운 요청이 발생하면 이전의 요청은 취소해줌! 불필요한 api 콜을 줄일 수 있다. 해당 플젝에서는 검색 api를 콜할 때 사용했음
- IntersectionObserver : 관찰하고자 하는 엘리먼트가 어떤 엘리먼트나 뷰포트에서 보이는 지 안 보이는 지를 감지. scroll과는 다르게 비동기적으로 실행되기 때문에 더 효율적이라고 한다!
