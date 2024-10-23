# 여러가지 선택자

- [후손선택자와 자식선택자](#후손선택자와-자식선택자)
- [동위선택자](#동위선택자)
- [반응선택자](#반응선택자)
- [구조선택자](#구조선택자)
- [형태구조선택자](#형태구조선택자)
- [속성선택자](#속성선택자)
- [문자선택자](#문자선택자)
- [:not(), :has(), :is()](#not-has-is)
- [가상요소선택자](#가상요소선택자)

&nbsp;

## 후손선택자와 자식선택자

### 후손선택자
- 해당 요소의 하위 요소에 있는 특정한 요소를 모두 선택하는 선택자
- 선택자a 선택자b

### 자식선택자
- 해당 요소의 바로 밑에 위치하는 특정한 요소를 모두 선택하는 선택자
- 선택자a > 선택자b

★★★★★ 중첩사용 가능함

```html
<style>
  .box h2 {
    /* 후손선택자 */
  }

  .box > h2 {
    /* 자식선택자 */
  }
</style>

<div class="box">
  <h1>제목-1</h1>
  <h2>제목-2</h2>
  <div class="box2">
    <h2>제목-2</h2>
    <ul>
      <li>리스트-1</li>
      <li>리스트-2</li>
      <li><a href="#">리스트-3</a></li>
    </ul>
    <a href="#">a</a>
  </div>
</div>
```

&nbsp;

## 동위선택자
동위관계에 있는 요소중에 해당 요소보다 뒤에 존재하는 특정한 요소를 선택할 때 사용

### 선택자a + 선택자b
선택자 바로 뒤에 위치하는 선택자b를 선택

### 선택자a ~ 선택자b
선택자a 뒤에 위치하는 모든 선택자b를 모두 선택

```html
<style>
  .item h1 + h2 {
    /* h1 바로 뒤에 위치하는 h2를 선택 */
  }

  .item h1 ~ h3 {
    /* h1 뒤에 위치하는 h3를 모두 선택 */
  }

  .item h1 ~ * {
    /* h1 뒤에 위치하는 모든 요소를 선택 */
  }
</style>

<div class="item">
  <a href="https://www.naver.com">a태그</a>
  <h1>제목-1</h1>
  <h2>제목-2</h2>
  <h2>제목-2</h2>
  <h2>제목-2</h2>
  <h3>제목-3</h3>
  <h3>제목-3</h3>
  <h3>제목-3</h3>
  <h3>제목-3</h3>
</div>
```

&nbsp;

## 반응선택자
특정한 행동을 취했을 때 사용하는 선택자

- `:hover` : 특정한 요소에 마우스를 올렸을 때
- `:active` : 특정한 요소를 클릭한 순간
- `:visited` : 방문한 링크에 스타일 적용
- `:focus` : 요소에 초점이 맞춰진 경우 -> 보통 input 박스에 커서가 깜빡이는 경우

```html
<style>
  .item h2:hover {
    /* h2에 마우스를 올렸을 때 */
  }

  .item h1:active {
    /* h1을 클릭한 순간 */
  }

  .item a:visited {
    /* a 태그를 클릭하여 다른 페이지를 방문한 후 */
  }

  .item input:focus {
    /* input 태그에 초점이 맞춰졌을 때 */
  }
</style>

<div class="item">
  <a href="https://www.naver.com">a태그</a>
  <h1>제목-1</h1>
  <h2>제목-2</h2>
  <h2>제목-2</h2>
  <h2>제목-2</h2>
  <h3>제목-3</h3>
  <h3>제목-3</h3>
  <h3>제목-3</h3>
  <h3>제목-3</h3>
  <input type="text">
</div>
```

&nbsp;

## 구조선택자
부모요소의 안에서 특정한 위치의 요소를 선택할 때 사용함 -> 자식요소의 위치로 선택함

- `선택자:first-child`: 부모 아래의 첫 번째 자식을 선택
- `선택자:last-child`: 부모 아래의 마지막 번째 자식을 선택
- `선택자:nth-child(순번)`: 부모 아래의 순번째에 자식을 선택
  - (2n): 짝수, (2n+1): 홀수

```css
ul li:first-child {
  /* ul의 후손 중 첫번째 li를 선택 */
}

ul li:last-child {
  /* ul의 후손 중 마지막 li를 선택 */
}

ul li:nth-child(3) {
  /* ul의 후손 중 세 번째 li를 선택 */
}

ul li:nth-child(2n) {
  /* ul의 후손 중 짝수 번째 li를 선택 */
}

ul li:nth-last-child(1) {
  /* ul의 후손 중 뒤에서 첫 번째 li를 선택 */
}
```

&nbsp;

## 형태구조선택자
부모 요소 아래에 있는 요소들을 태그의 형태로 구분하여 선택함

```html
<style>
  .list h2:first-of-type {
    /* h2 중 첫 번째를 선택 */
  }

  .list h1:last-of-type {
    /* h1 중 마지막 번째를 선택 */
  }

  .list h3:nth-of-type(2) {
    /* h3 중 세 번째를 선택 */
  }

  .list h1:nth-last-of-type(3) {
    /* h1 중 뒤에서 세 번째를 선택 */
  }
</style>

<div class="list">
  <h1>타이틀-1</h1>
  <h2>타이틀-2</h2>
  <h3>타이틀-3</h3>
  <h1>타이틀-1</h1>
  <h2>타이틀-2</h2>
  <h3>타이틀-3</h3>
  <h1>타이틀-1</h1>
  <h2>타이틀-2</h2>
  <h3>타이틀-3</h3>
</div>
```

&nbsp;

## 속성선택자
특정한 속성이나 특정한 속성 값을 갖고 있는 html 요소를 선택시 사용

- `[속성이름="속성값"]`: 속성 이름을 제시하고 일반적인 속성을 불러 값을 설정할 때
- `[속성이름$="속성값"]`: 특정한 속성명이 존재할 때 속성명의 접미사로 끝나게 되는 속성 값을 설정할 때 (ex. .확장자)
- `[속성이름*="속성값"]`: 특정 문자가 들어간 속성값을 불러 올 때

```html
<style>
  input[type="text"] {
    
  }

  img[src$="png"] {

  }

  div[class*="header"] {

  }

  input[type="password"]:focus {
    /* 반응선택자와 중첩하여 사용가능 */
  }
</style>

<input type="text" class="t">
<input type="password" class="pw">

<img src="img/img.png" alt="img">

<div class="header">
  <div class="header_i">
    <div class="header_nav"></div>
    <div class="header_search"></div>
  </div>
</div>
```

&nbsp;

## 문자선택자

- `::first-letter`: 특정한 선택자의 첫 번째 글자를 선택
- `::first-line`: 특정한 선택자의 첫 줄을 선택

```html
<style>
  p::first-letter {
    font-size: 30px;
    color: red;
  }

  p::first-line {
    background-color: seagreen;
  }
</style>

<p>
  Lorem ipsum dolor, sit amet consectetur adipisicing elit. <br>
  Nobis nemo repellat reprehenderit maxime debitis quod repudiandae dicta eaque. <br>
  At dolorem doloremque asperiores similique, magni obcaecati debitis ut accusamus sequi perspiciatis.
</p>
```

&nbsp;

## :not(), :has(), :is()

### 부정선택자 :not()
선택한 요소를 제외시킬 때 사용

```html
<style>
  ul li:not(:nth-child(3), .t) {
    /* ul의 후손 li 중 세 번째와 클래스명이 t인 것을 제외하고 선택 */
  }
</style>
<ul>
  <li>menu1</li>
  <li class="t">menu2</li>
  <li>menu3</li>
  <li>menu4</li>
  <li>menu5</li>
</ul>
<ul>
  <li>menu1</li>
  <li>menu2</li>
  <li>menu3</li>
  <li>menu4</li>
  <li>menu5</li>
</ul>
```

### :has()
특정 자식요소를 포함하는 부모 요소를 선택할 수 있는 선택자

```html
<style>
  ul:has(.t) li {
    /* 클래스명이 t인 자식을 포함하는 ul의 후손 li를 선택 */
  }
</style>
<ul>
  <li>menu1</li>
  <li class="t">menu2</li>
  <li>menu3</li>
  <li>menu4</li>
  <li>menu5</li>
</ul>
<ul>
  <li>menu1</li>
  <li>menu2</li>
  <li>menu3</li>
  <li>menu4</li>
  <li>menu5</li>
</ul>
```

### :is()
여러 선택자를 하나로 묶어 간단하게 작성할 수 있는 기능적 선택자

```html
<style>
  .box > :is(h1, h2, h3) {
    /* .box의 자식 중 h1, h2, h3를 선택 */
  }
</style>

<div class="box">
  <h1>타이틀</h1>
  <h2>타이틀</h2>
  <h3>타이틀</h3>
  <h4>타이틀</h4>
</div>
```

&nbsp;

## 가상요소선택자

- `::before`: 특정한 요소의 앞에 삽입
- `::after`: 특정한 요소의 뒤에 삽입
- content : '내용' -> 반드시 포함
- 주로 메뉴 사이에 선을 넣을 때 많이 사용함

```html
<style>
  ul li {
    float: left;
    margin: 0 8px;
    list-style: none;
  }

  ul li:not(:last-child)::after {
    content: '';
    display: inline-block;
    width: 1px;
    height: 12px;
    background-color: #000;
    margin-left: 16px;
  }
</style>

<ul>
  <li><a href="#">menu-1</a></li>
  <li><a href="#">menu-2</a></li>
  <li><a href="#">menu-3</a></li>
  <li><a href="#">menu-4</a></li>
  <li><a href="#">menu-5</a></li>
</ul>
```

&nbsp;

[제일위로](#여러가지-선택자)