# 2. HTML과 CSS

## 2-1. HTML

Hyper Text Markup Languge의 약어, 마크업 구성에 가장 많이 사용되는 언어.<br>
content, start tag, end tag로 나눌 수 있고, 이를 합쳐서 element(요소) 라고 부름.

- HTML 구성
  - Void 요소 : end 가 없는 엘리먼트
  - Content와 Element : 내용
  - Attributes : 속성
  - 인라인 엘리먼트와 블록 엘리먼트 : 인라인은 필요한 사이즈, 블록은 위치한 세로줄 전체 사이즈로 잡히는 엘리먼트 특성
  - 콘텐츠 모델
    - Metadata Content : 콘첸츠 표시, 다른 문서 설정하는 엘리먼트 (link, meta..)
    - Flow Content : 본문에 사용되는 대부분의 엘리먼트 (h1, p, div..)
    - Sectioning Content : 아웃라인을 정의하고 엘리먼트의 범위를 정의하는 엘리먼트 (article, aside, nav, section..)
    - Pharsing Content : 텍스트
  - Heading Content : 섹션 헤더를 정의하는 엘리먼트 (h1 ~ h6)
  - Embedded Content : 외부 자원을 가져오거나 삽입할 때 사용하는 엘리먼트 (audio, canvas, iframe, img..)
  - Interactive Content : 유저와 상호작용을 위해 설계된 엘리먼트 (svg, canvas, img..)
  - DOCTYPE은 사용하면 HTML5로 작성한 문서임을 나타낸다
- 시멘틱(Semantic)
  - 엘리먼트를 시멘틱하게 작성해야한다 의미 있는 태그를 상황에 따라 사용한다는 뜻
- SEO(Search Engine Optimization)
  - 사이트를 찾기 쉽도록 개선하는 작업을 검색 엔진 최적화

1.  시맨틱하게 HTML 작성하기
2.  <title> 잘 작성하기
3.  <meta name="description"> 을 이용해 페이지 설명을 추가하기
4.  <meta charset="UTF-8"/>를 사용해 인코딩 방식을 지정하기
5.  open grahp, twitter 태그를 사용해 사용자 접근성 높히기

## 2-2. CSS

Cascading Style Sheets의 약자로 문서를 표시하는 방법으로 스타일이나 레이아웃을 지정한다

- 상속 : css의 프로퍼티 중에서는 상위 요소에서 자식 요소까지 상속되는 프로퍼티가 있음. (font, color..)
- 프로퍼티와 엘리먼트의 종류에 영향받지 않고 부모 요소의 프로퍼티를 상속받고 싶다면 명시적으로 inherit 값을 지정한다
- 전체 선택자 : \*
- 타입 선택자 : div, p...
- id 선택자
- class 선택자
- 속성 선택자
  | 연산자 | 설명 |
  | --- | --- |
  | = | 값이 정확하게 일치할 때 선택 |
  | ~= | 값이 정확하게 일치할 때 선택 |
  | \\ | 값이 일치하거나 값 뒤(하이픈)을 작성할 때 선택 |
  | ^= | 접두사로 값을 가질 때 선택 |
  | $= | 접미사로 값을 가질 때 선택 |
  | \*= | 값이 포함된 모든 요소를 선택 |

- 우선순위와 명시도
  - 마지막에 작성된 스타일이 적용된다
  - 명시도가 높은 선택자의 스타일이 적용된다
- 박스 모델
  - 박스모델은 content, padding, border, margin 영역으로 이루어진다
  - box-sizing -> 요소의 너비와 높이를 계산하는 방식을 지정한다
  - content-box: content 영역만 기준으로 계산
  - border-box: padding, border, content 영역을 합한 영역을 기준으로 계산
- 여백 상쇄

  - 인접한 같은 레벨의 블록 요소에 상하 여백이 겹치면 여백이 하나로 합쳐지는 현상
  - 여백은 단순하게 너비나 높이에 더하여 계산될 것 같지만 실제로는 그렇게 동작하지 않기 때문에 발생한다
  - 인접한 여백 중 큰 여백으로 상쇄된다
  - diplay 값이 flex/grid or position 값이 absolute 일 때, float인 상태일 때 적용되지 않는다

- flex
- 반응형 웹을 위한 미디어쿼리
  - 콘텐츠 자체를 변경하지 않고 장치의 해상도, 뷰포트의 너비, 미디어의 유형 같은 조건에 따라 스타일을 지정할 수 있다
  - 미디어 타입과 미디어 기능을 기준으로 동작한다
  - 미디어 타입에는 모든 장치, 인쇄 미디어, 화면 있다

```
 @media screen {
 }
```

```
@media (min-width: 700px) and (orientation: landscape) {
}
```

- 웹 접근성 : 장애, 노령으로 인한 신체 변화, 여러 기기 환경을 사용하는 모든 사람이 웹 사이트와 도구 등을 사용할 수 있도록 개발하는 것
- 웹 접근성 지침

1.  속어, 약어 사용을 지양하라
2.  콘텐츠의 제목과 단락을 명확하게 구분하자
3.  키보드 동작을 제공하자 (role, tabe-index, 키보드 이벤트 리스너 추가)
4.  Focus하는 지점을 명확하게 하자 (css outilne)
5.  멀티미디어 요소에 접근성을 부여하자 (img에 alt 설명 추가)
