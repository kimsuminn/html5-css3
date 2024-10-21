# CSS 글자 속성

- [글자속성](#글자속성)
- [a태그 사용시 기본설정값](#a-태그-사용시-기본설정값)

&nbsp;

## 글자속성

### 글자색상

```css
.text {
  color: green;
}
```

단어, hex(컬러코드), rgb.. 

### 글자사이즈

```css
.text {
  font-size: 40px;
}
```

- px, em, rem, pt, v.. 단위
- html 기본 폰트 사이즈 16px

### 글자굵기

```css
.text {
  font-weight: bold;
}
```

- 100 ~ 900 (100 ~ 300: 가늘게, 400 ~ 600: 중간, 700 ~ 900 : 굵게)
- lighter, normal, bold -> 원래 굵게 디자인된 글자나 가늘게 디자인된 글자는 변경이 안됨

### 글자스타일

```css 
.text {
  font-style: italic;
}
```

### 글꼴

```css
.text {
  font-family: "맑은고딕";
}
```

- 내 컴퓨터에 저장된 글자 표현
- 웹 폰트 제외

### 자간 행간

```css
.text {
  letter-spacing: 30px; /* 자간 */
  line-height: 1.5; /* 행간 */
}
```

- 자간 : 글자 사이의 간격 (px, %, em.. )
- 행간 : 글자 줄 사이의 간격 (px, %, 배율)

### 글자변형

```css
.text {
  text-transform: capitalize;
}
```

- capitalize : 띄어쓰기 했을 때 첫 글자만 대문자
- uppercase : 모두 대문자
- lowercase : 모두 소문자

### 글자쓰기방식

```css
.text {
  writing-mode: horizontal-tb
}
```

- horizontal-tb : 초기값, 가로 텍스트
- vertical-rl : 오른쪽에서 왼쪽, 세로 텍스트
- vertical-lr : 왼쪽에서 오른쪽, 세로 텍스트

### 글자정렬

```css
.text {
  text-align: center; /* 글자수평정렬 */
  align-content: center; /* 글자수직정렬 */
}
```

- 글자 수평정렬 : left, right, center
- 글자 수직정렬 : start, center, end
  - 높이값이 필수로 있어야함

### 글자선

```css
.text {
  text-decoration: underline wavy red;
}
```

선의 위치, 선의 종류(생략 가능), 선의 색상(생략 가능)

&nbsp;

## a 태그 사용시 기본설정값

```css
a {
  color: inherit; /* inherit : 부모의 속성값을 상속 */
  text-decoration: none;
}
```

&nbsp;

[제일위로](#css-글자-속성)