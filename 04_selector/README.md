# 기초선택자

- [전체선택자](#전체선택자)
- [태그선택자](#태그선택자)
- [아이디선택자](#아이디선택자)
- [클래스선택자](#클래스선택자)

&nbsp;

## 전체선택자
- html 내에 등장하는 모든 형태를 선택하는 선택자
- 주로 초기화 값, 기본설정 값을 입력할 때 사용함

```css
* {
  padding: 0; /* 안쪽 여백 */
  margin: 0; /* 바깥쪽 여백 */ 
}
```

&nbsp;

## 태그선택자
- html 내에 등장하는 특정한 태그를 모두 선택하는 선택자
- 태그에 대한 기본설정 값을 입력할 때 사용함

```css
p {
  margin-bottom: 50px;
}

h3 {
  color: green;
}
```

&nbsp;

## 아이디선택자
- 특정한 이름을 부여하여 선택하는 선택자로 html 화면 내에서는 하나의 이름만 사용 가능
- 주로 큰 단락, 부모 박스에 많이 사용함

```html
<h3 id="title">아이디 선택자</h3>
```

```css
h3#title {
  color: red;
}
```

&nbsp;

## 클래스선택자
- 특정한 이름을 부여하여 선택하는 선택자로 html 화면 내에서 여러 개의 이름을 사용 가능
- 주로 작은 단락, 자식 박스에 많이 사용함
- 변화가 잦은 요소

```html
<h3 class="text a b c">클래스 선택자</h3>
```

```css
h3.text {
  color: blue;
}

.a {
  background-color: sandybrown;
}

.b {
  color: gold;
}
```

★ 클래스 선택자에 같은 속성이 들어가는 경우 더 나중에 선택한 클래스 선택자가 우선

★ 아이디 선택자와 클래스 선택자에 같은 속성이 들어가는 경우 아이디 선택자가 우선

&nbsp;

[제일위로](#기초선택자)