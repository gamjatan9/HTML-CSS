# [과제] 넷플릭스 사이트 클론

### ▶︎ 목표
HTML과 CSS를 활용하여 웹 사이트 만들기.<br/>
클론 사이트 주소: https://www.netflix.com/kr/browse/genre/839338 

### ▶︎ 조건
1. Flex Box 또는 Grid CSS 를 이용해서 영화를 나열 <br/>
2. 영화에 마우스로 호버 하면 영화 이미지의 사이즈가 커짐

### ▶︎ 결과 캡처
<img width="1512" alt="favicon" src="https://github.com/gamjatan9/HTML-CSS/assets/122338050/a65c71a3-18a4-4af9-9e2c-c7abd79c1a07">
<img alt="fullScreen2" src="https://github.com/gamjatan9/HTML-CSS/assets/122338050/3e785c42-e618-4f52-8e1c-61bfccb282c8">
<img alt="fullScreen2" src="https://github.com/gamjatan9/HTML-CSS/assets/122338050/c2233b62-1a3a-4831-8883-66831c93fda9">
<img alt="fullScreen2" src="https://github.com/gamjatan9/HTML-CSS/assets/122338050/94829f97-849d-4719-9cf5-5d60f6e8c8ae">
<br/>

### ▶︎ 주요 코드
- Flex Box 정렬
  styles/collections.css
```css
.collections {
    display: flex;
    flex-direction: column;
    margin-top: 150px;
    position: relative;
}
```
-  영화에 마우스로 호버 하면 영화 이미지의 사이즈가 커짐
```css
.contents-items {
    position: relative;
    display: flex;
    overflow: hidden; /* 너비 넘어간 부분 숨기기 */
}

.item {
    padding: 0px 10px;
}
.item img {
    width: 410px;
    height: 220px;
    transition: transform 0.2s ease-in-out; /* 부드러운 변화 */
}
.item:hover img{ /* 호버 시 1.3배 확대, 위에가 잘려서 아래로 20px 내려가게 함  */
    transform: scale(1.3) translateY(20px); 
}
```
<img width="1400" alt="스크린샷" src="https://github.com/gamjatan9/HTML-CSS/assets/122338050/b5fb5621-c8bc-45ea-aa75-fca32371e7b7" />

- 마지막 영화 행 블러처리
  - collections.css
```css
.blur {
    position: absolute;
    bottom: 300px;
    transform: translateY(0%);
    width: 100%;
    height: 400px;
    backdrop-filter: blur(10px); /* 블러 효과 적용, 숫자는 블러 정도 조절 */
    background-color: #1818188a; /* 배경 색상 및 투명도 설정 */
    border-radius: 20px; 

}
```

### ▶︎ Figma 클론
<img alt="fullScreen2" src="https://github.com/gamjatan9/HTML-CSS/assets/122338050/e5da77f7-7ab6-4b00-8923-464abc199a5a">

