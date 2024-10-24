# color

색상 입력 방식에는 6가지가 있음

### 단어
- 색상의 이름 단어로 입력하는 방식
- 아주 기초적인 단색인 경우에는 괜찮지만 그 외에는 좋은 방법이 아님

```css
body {
  background-color: lightblue;
}
```

### hex 컬러코드
- 6자리의 웹 코드를 입력하는 방식
- 반복되는 두 자리는 한 자리로 줄여서 표현 가능

```css
body {
  background-color: #faf;
}
```

### rgb
- red, green, blue의 숫자값, 256 가지의 색상을 조합하여 표현하는 방식

```css
body {
  background-color: rgb(120, 140, 240);
}
```

### rgba
- rgb 표현 방식에 alpha 값을 추가한 방식
- alpha: 색상에 대한 투명도를 나타냄. 0에서 1 사이의 소수점이나 퍼센트 값 입력

```css
body {
  background-color: rgba(150, 100, 240, .4);
}
```

### hsl
- hue, saturation, lightness의 양 값을 입력하는 방식
- hue: 색조, saturation: 채도, lightness: 명암
- 실무에서는 거의 사용되지 않음

```css
body {
  background-color: hsl(200, 85%, 70%);
}
```

### hsla
- hsl 표현 방식에 alpha 값을 추가한 방식

```css
body {
  background-color: hsla(220, 80%, 60%, .7);
}
```

&nbsp;

★ alpha와 opacity는 다르다!

alpha는 색상의 투명도를 정하는 것이고 opacity는 요소 자체를 모두 투명하게 만들어줌

&nbsp;

### 그림자 넣기

```html
<style>
  h1 {
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.335);
    /* 
      박스에 그림자를 부여하는 속성 
        x축, y축, 그림자 크기, 그림자 색상 순으로 입력
    */

    text-shadow: 2px 2px 0px #f00;
    /* 
      글자에 그림자를 부여하는 속성
        x축, y축, 그림자 크기, 그림자 색상 순으로 입력
    */
  }
</style>

<h1>Box</h1>
```

&nbsp;

[제일위로](#color)