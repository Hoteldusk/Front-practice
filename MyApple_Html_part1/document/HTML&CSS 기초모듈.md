# HTML&CSS 기초모듈

- HTML 은 Markup Language 자료가 어디에 어떻게 배치되어있나 표현하기 위한 언어
- a태그 : anchor href에 기입된 링크이동
- img 태그 : src 에 이미지경로를 집어넣으면 이미지가 출력
- li태그 : list item => ul 이나 ol 하위 태그
- ul태그 : unordered list => list item이 번호없이 출력
- ol태그 : ordered lsit => list item이 번호있이 출력

```html
<!-- 이미지를 클릭했을때 링크로 이동하기 html-->
<a href="link"><img src="imagePath" /></a>
```

## CSS (Cascading Style Shteet)

- 태그안에 css 적용가능 style="margin-left:30px;" => margin-left : 왼쪽여백
- 이미지 가운데 정렬하는 방법

```css
.image {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
```

- 폰트지정 (font-family)
- 글자 자간조절 (letter-spacing)
- 글자 정렬 (text-align)

```css
.text {
  font-family: "monospace";
  letter-spacing: -1px;
  text-align: center;
}
```

- 일부 글자만 스타일링 하려면?
- spantag를 사용하자 span : 글자를 감쌀수 있는 별 뜻 없는 태그

```html
<p><span>Full-Stack</span>Developer</p>
```

- 글자를 굵게 표현하고싶다면? => text-weigth 를 100~900 까지조정 or strong 태그사용
- css적용방법

```html
<link rel="stylesheet" type="text/css" href="css파일경로" />
```

- css 클래스 이름의 중복은 피하자(이상현상 방지)
- css Selector(선택자)종류 : (클래스. {} // 태그 {} // #아이디 {})
- 스타일이 겹칠경우 우선순위가 존재함 : HTML 에서의 style 지정 > #아이디 {} > 클래스. {} > 태그 {}

## float를 이용한 layout

- 최초 div 클래스이름은 container로 생성 (전체 width 결정)
- 모든 div는 display:block 이라는 속성을 내장함(가로행을 전부 차지)
- float : left, right => 태그 공간을 붕 띄워서 배치시킴, 이러면 한 가로줄에 다수의 div를 배치할 수 있으나, 속성을 주지않은 다음 태그의 공간이 가려져버림
- float 다음요소에 clear : left, right, both 로 해결가능

## Selector 문법

- selector 문법 > : ~안에 있는 직계자식
- selector 문법 공백 : ~안에 있는 모든 자식

## margin collapse 현상

- box 2개가 테두리가 겹칠경우 margin이 합쳐지는 현상
- 해결방법 : 한 쪽 box에 padding 을 1px 주면 해결
