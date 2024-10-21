# HTML 이미지 태그

- [img](#img)
- [figure](#figure)
- [img url 연결](#img-url-연결)

&nbsp;
&nbsp;

## img
- 이미지를 나타내줄 수 있는 태그
- 단독태그
- 인라인 성질

### 이미지 확장자

#### jpg
- 가장 대표적인 이미지 표현 방식
- 이미지의 색상을 가장 잘 표현할 수 있는 확장자
- 투명한 배경 X

#### png
- 이미지의 색상을 유지하며 투명한 배경을 나타낼 수 있는 확장자
- jpg보다 용량이 무거움

#### gif
- 움직이는 이미지 표현시 사용
- 투명한 배경도 가능

#### webp
- 기존의 이미지를 웹 환경에 최적화시켜 압축시킨 확장자

```html
<img src="파일경로" alt="이미지 대체문">
```

### src, href

#### src
- 외부 리소스를 html 문서에 직접 포함할 때 사용
- 즉시 로드하여 문서에 포함시키기 때문에 페이지 출력이 일시적으로 중단될 수 있음
  - 파싱 : 데이터를 추출해서 분석하는 능력
- 이미지, 스크립트, 영상, iframe

#### href
- 현재 문서와 외부 리소스 간의 링크를 설정하는 데 사용
- 페이지 출력이 중단되지 않고 필요할 때만 리소스를 가져와서 사용
- a, css

&nbsp;

## figure
- 시멘틱 태그의 종류 중에 하나
- 이미지, 영상, 그래픽 등의 멀티미디어 콘텐츠와 그에 대한 설명을 그룹화 하는 데 사용
- 블럭요소의 성질을 갖고있음

### figcation
- 컨텐츠에 대한 설명을 넣을 때 사용
- 선택적으로 사용 가능
- 컨텐츠의 첫 번째 또는 마지막에 배치를 해야 함
- 대부분의 브라우저에서 지원하므로 웹 페이지의 접근성과 SEO 향상에 기여

```html
<!-- figure는 각각의 이미지를 넣어서 사용하는 것이 좋다 -->
<figure>
    <figcaption>png 이미지</figcaption>
    <img src="./img/png.jpg" alt="png">
</figure>
```
&nbsp;

## img url 연결

```html
<img src="https://i.namu.wiki/i/hWLEwQhnjvdoRZQhrgHMKAZjiSVPO5D86_nBD6OCVLHamm0dM7Ssv2KTfYgjJj-V_X3hMsgV-LeIgI7lmbqzhA.webp" alt="url 연결">
```

- 잘 사용하지 않음
- 해당 주소의 이미지가 내려갔을 때 이미지를 사용할 수 없어짐
- 저작권 문제

&nbsp;

[제일위로](#html-이미지-태그)