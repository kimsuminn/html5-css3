# display

### display
요소의 성질을 결정하는 속성

#### block
- 박스와 같이 쌓이는 성격
- 모든 css 적용 가능
- 부모 전체의 폭을 사용하는 성격을 갖고 있음

#### inline
- 글자와 같이 나열되는 성격을 갖고 있음
- 내용물에 따라 폭이 결정됨
- 크기와 margin 상하 부여가 안됨

#### inline-block
- 인라인과 블럭의 합성속성
- 글자와 같이 옆으로 나열됨
- block과 같이 모든 css 적용이 가능함

### display 속성 사용

- block: 요소의 성질을 block 형태로 변경
- inline: 요소의 성질을 inline 형태로 변경
- inline-block: 요소의 성질을 inline-block 형태로 변경
- none: 요소를 제외, 스크립트와 같이 많이 사용함

#### img 설정

```css
img {
  display: block;
}
```

- 이미지는 block 처리를 해서 사용하는 게 편함
- block 처리를 해도 부모요소의 폭을 모두 사용하지 않음

```css
figure {
  width: fit-content;
  height: fit-content;
}
```

- img 태그를 figure 태그로 감싸고있을 때 위와 같이 설정해주면 이미지의 크기를 따로 찾아 볼 필요없이 이미지의 크기만큼 사이즈를 맞춰줌
- 기본값이 아니라 편의를 위해 사용하는 값