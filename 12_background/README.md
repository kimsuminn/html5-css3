# background

### background-color

- 배경 색을 부여하는 속성
- 단어, hex, rgb, transparent(투명)...

```css 
body {
  background-color: transparent;
}
```

### background-img

- 배경 이미지를 불러오는 속성
- 반복되는 성격을 갖고 있음
- `,`로 구분하여 배경 이미지를 2장 이상 적용 가능
  - 먼저 작성한 순서대로 이미지가 상단에 표현되어짐 (레이어를 생각하면됨)

```css
body {
  background-image: url(img/img.jpg);
}
```

### background-repeat

- 배경 이미지의 반복을 결정하는 속성
- `no-repeat`: 반복되지 않은 원본 한 장
- `repeat-x`: 가로 반복
- `repeat-y`: 세로 반복

```css
body {
  background-repeat: no-repeat;
}
```

### background-size

- 배경 이미지의 크기를 정할 때 사용함
  - px, %, cover, contain
  - %는 가로상의 비율을 나타냄
- cover: 화면 상에서 무조건 꽉 차게 표현하며 가로와 세로의 비율을 최대한 유지해줌
- contain: 최대한 원본 이미지의 비율을 유지해주면서 표현

```css
body {
  background-size: cover;
}
```

### background-attachment

- 배경 이미지를 어떤 방식으로 화면에서 표현할지 지정하는 속성
- scroll: 기본 값
- fixed: 스크롤 바가 움직여도 배경 이미지는 고정이 됨
- local: 배경 이미지와 콘텐츠가 스크롤을 했을 때 함께 움직임

### background-position

- 배경 이미지의 위치 지정시 사용 (폭 값이 존재해야 함)
- x y 순서로 입력해야 함
  - 단어, px, %...
  - 단어 x: left, center, right
  - 단어 y: top, center, bottom

```css
body {
  background-position: center center;
}
```

### linear-gradient

- 배경 그라디언트 표현시 사용
- direction과 angle 두 가지 방법으로 표현 가능

#### direction
- `to`로 시작함
- left, right, top, bottom을 조합하여 그라데이션의 방향을 지정
- to left, to right, to top, to bottom : 수평선과 수직선
- to left bottom, to left top, to right bottom, to right top: 대각선

#### angle
- 그라데이션의 방향 각도
- deg 앞에 숫자를 적어 그라데이션의 방향 지정 가능

&nbsp;
그라데이션은 [이 사이트](https://cssgradient.io/)에서 만들어서 사용 가능

```css
body {
  background: linear-gradient(45deg, orange 33%, pink 33% 66%, gold 66% 100%)
}
```

### background-clip

- 배경의 테두리, 패딩, 글자.. 어느 영역까지 배경이 확장되는지 결정
- 글자를 색 대신 배경으로 채우고 싶을 때 사용 가능

```css
body {
  background-clip: text;
}
```

&nbsp;

[제일위로](#background)