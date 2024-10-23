# overflow

부모박스에 내용물이 넘치는 경우 어떻게 보여질지 결정하는 속성

### visible

`overflow: visible;`

overflow 기본값

### hidden

`overflow: hidden;`

폭 값이 존재할 때 내용물을 보이지 않도록 해줌

### scroll

`overflow: scroll;`

- 내용물이 넘치는 경우 스크롤을 생성하여 볼 수 있도록 해줌
- 내용물이 넘치지 않아도 스크롤바가 생성됨 (스크롤은 생성되지 않음)

### scroll 꾸미기

```css
.box {
  width: 200px;
  height: 300px;
  border: 2px solid #000;
  float: left;
  margin: 10px;
  padding: 10px;
  overflow: scroll;
}

.box::-webkit-scrollbar {
  width: 0;
}
```

### overflow-x, overflow-y

- overflow-y: y축(세로)의 넘치는 내용물을 어떻게 보여줄지 결정하는 속성
- overflow-x: x축(가로)의 넘치는 내용물을 어떻게 보여줄지 결정하는 속성

### overflow:hidden; 활용

```css
.box {
  width: 700px;
  background-color: #afa;
  margin: auto;
  overflow: hidden;
  /* 부모 박스의 height 값을 모를때 */
}

.left {
  width: 350px;
  height: 400px;
  background-color: #5fa;
  float: left;
}

.right {
  width: 300px;
  height: 400px;
  background-color: #2af;
  float: right;
}
```

```html
<style>
  *{
    padding: 0;
    margin: 0;
  }

  .allbox {
    width: 700px;
    /* height: 500px; */
    border: 1px solid #000;
    margin: auto;
    overflow: hidden;
  }

  .box {
    width: 250px;
    height: 30px;
    background-color: #5af;
    margin: 30px auto;
  }

  .a {
    overflow: hidden;
    /* 마진 겹침 현상이 생겼을 때 사용 */
  }
</style>

<div class="allbox">
  <div class="box"></div>
  <div class="a"></div>
  <div class="box"></div>
</div>
```