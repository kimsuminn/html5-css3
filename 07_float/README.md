# float

- 박스를 옆으로 나열 할 때 사용함
- 왼쪽이나 오른쪽으로 배치
- 이미지와 텍스트를 함께 배치하거나 레이아웃 구성시에 사용함
- 배치된 요소의 부모 박스가 배치된 요소들보다 크기값이 작아질 경우 배치된 요소들은 자동으로 다음 라인으로 넘어감

```html
<div class="allbox">
  <div class="item b1">1</div>
  <div class="item b2">2</div>
  <div class="item b3">3</div>
  <div class="item b4">4</div>
</div>
```

```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.allbox {
  width: 860px;
  margin: 50px auto;
}

.item {
  width: 200px;
  height: 200px;
  border: 1px solid #000;
  text-align: center;
  align-content: center;
  float: left;
  margin-right: 20px;
}

.b4 {
  margin-right: 0;
  clear: left;
}
```

`clear: left;`: flaot을 제거할 때 사용하며 left, right, both 중 입력 가능