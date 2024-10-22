# div

- [블럭요소와 인라인요소](#블럭요소와-인라인요소)
- [박스크기에 영향을 주는 스타일](#박스크기에-영향을-주는-스타일)
  - [box-sizing: border-box](#box-sizing-border-box)
  - [width, height](#width-height)
  - [테두리](#테두리)
  - [여백](#여백)
  - [border-radius](#border-radius)
- [실측 사이즈 계산](#실측-사이즈-계산)


&nbsp;

## 블럭요소와 인라인요소

### 블럭요소
- 박스와 같이 쌓이면서 나타나는 성격
- 크기를 직접적으로 부여하지 않을 경우 사이즈가 auto 처리
  - auto : 태그를 감싸고 있는 부모박스의 크기를 100% 사용
- 모든 CSS 적용 가능
- div : 공간 분할 태그

### 인라인요소
- 글자와 같이 나열되며 나타나는 성격
- 내용의 폭값, 화면의 일부를 차지하는 태그
- width, height, margin-top, margin-bottom 적용 X
- span 태그

&nbsp;

## 박스크기에 영향을 주는 스타일

### box-sizing: border-box

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

- 크기에 대한 속성 값
- 패딩, 안쪽 선을 폭 값 안으로 포함
- border-box를 해제하고 싶다면 content-box를 사용하면 됨

### width, height

```css
.box {
  width: 300px;
  height: 300px;
}
```

#### width
- 가로폭, 넓이
- auto, %, px, v..

#### height
- 세로폭, 높이
- auto, %, px, v..

#### width의 auto와 height의 auto는 완전히 다름

- width : auto > 부모 박스의 전체 크기를 사용
- height : auto > 내용물의 크기를 100% 사용

### 테두리

#### 안쪽선

```css
.box {
  border: 5px solid pink;
}
```

- 선의 굵기, 선의 종류, 선의 색상(선택사항)을 입력해 줘야 함
- border-위치 -> 개별적으로 사용 가능
- 세 군데에 border를 넣고 밑의 border는 빼고 싶다면, border를 네 군데에 넣고 `border-bottom: none` 처리를 해주면 됨

#### 바깥선

```css
.box {
  outline: 5px solid red;
}
```

- 선의 굵기, 선의 종류, 선의 색상(선택사항)을 입력해 줘야 함
- 위치를 개별적으로 부여할 수 없음

### 여백

#### padding

```css
.box {
  padding: 30px;
}
```

- 안쪽 여백: 안쪽으로 내용물과 박스 사이의 여백을 주는 것
  - 1개 값: 4면 전체 적용
  - 2개 값: 상하 좌우
  - 3개 값: 상 좌우 하
  - 4개 값: 상 우 하 좌 (시계방향)
- 위치별로 개별 부여가 가능함
  - `padding-위치: 값;`

#### margin

```css
.box {
  margin: 100px auto;
}
```

- 바깥 여백: 바깥으로 혹은 다른 요소와의 여백을 주는 것
  - 1개 값: 4면 전체 적용
  - 2개 값: 상하 좌우
  - 3개 값: 상 좌우 하
  - 4개 값: 상 우 하 좌 (시계방향)
- 위치별로 개별 부여가 가능함
  - `margin-위치: 값;`

#### auto
- 좌우 너비를 계산 후 중심 배치
- 남은 여백을 미는 값
- 블럭요소를 부모 박스 내에서 수평에서의 가운데 정렬시 사용함
- 상단 하단 여백에는 0px 계산
- 반드시 폭값이 존재해야 사용 가능함
- `margin-left: auto;`: 왼쪽으로 밀기

### border-radius

```css
.box {
  border-radius: 100%;
}
```

- 모서리를 둥글게 표현
  - 1개 값: 4개의 각 모두
  - 2개 값: 좌상우하 우상좌하
  - 3개 값: 좌상우하 우상 좌하
  - 4개 값: 좌상 시계 방향순으로 모두
- 개별적으로 부여가 가능함

&nbsp;

## 실측 사이즈 계산

```css
.box {
  width: 300px;
  height: 300px;
  border: 5px solid black;
  padding: 30px;
  margin: 30px;
}
```

- width: 300px + border(5px + 5px) + padding(30px + 30px) + margin(30px + 30px) = 430
- height: width랑 같은 방법

#### box-sizing: border-box;

- 크기에 대한 속성 값
- 패딩, 안쪽 선을 폭 값 안으로 포함해줌
  - 실측 사이즈를 계산할 때 기존에 부여한 값에다가 margin값만 더해주면 됨

&nbsp;

[제일위로](#div)