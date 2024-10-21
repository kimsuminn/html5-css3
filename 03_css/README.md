# CSS

- [CSS 문법](#css-문법)
- [CSS 적용방식](#css-적용방식)

&nbsp;

## CSS 문법
selector { property : value; }

&nbsp;

## CSS 적용방식

### 1. inline 방식
태그 옆에 직접적으로 부여하는 방식

```html
<h4 style="color: blue;">inline 방식</h4>
```

### 2. 내부 스타일 방식
head 공간에 style 태그를 작성 후 style 태그 내에 css 문법을 작성해서 부여하는 방식

```html
<style>
  h3 {
    color: blue;
  }
</style>
```

### 3. 외부 스타일 방식
head 공간 안에 link 태그를 사용해서 .css 확장자를 연결 후 css 문서에 css 문법을 작성하여 스타일을 적용하는 방식

```html
<link rel="stylesheet" href="./style.css">

<!-- rel : 문서 정보를 입력하는 공간 -->
```