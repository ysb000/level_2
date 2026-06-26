# 26/06/22~ HTML + CSS 
## HTML CSS로 웹&앱 문서 제작하는 순서
1. 제작 문서에 맞게 의미있는 HTML 태그 구성하기
2. CSS 파일을 style 폴더에 별도 생성하기
3. 1번에서 제작한 태그 중 디자인하려는 대상확인하기
4. 3번 대상을 선택자로 작성하고 디자인 목적에 맞게 속성:값 작성하기
## 선택자 {속성:값;}
## 선택자 {속성:값; 속성:값;}
# 선택자 종류
## 태그 선택자
* 태그명을 선택자로 사용하는 선택자
* `<h1></h1>` -> `h1 {속성:값;}`
## 클래스 선택자
* 반복되는 클래스명을 사용하는 선택자
* `<h1 class="title"></h1>` -> `.title {속성:값;}`
## 자식 선택자
* 특정 부모 안 자식을 사용하는 선택자
* `<h1><span></span></h1>` -> `h1 > span {속성:값;}`
## 형제 선택자 + or ~
* `<div> <a>1</a> <em>2</em> <del>3</del> </div>` 
* `div > a + em {}` 해석: 부모 div의 자식a의  인접형제 em 선택
* `div > a ~ del {}` 해석: 부모 div의 자식 a의 형제 del 선택
* `+`는 바로 옆에 있는 형제 태그만 인식한다.
* `~`는 바로 옆 형제 포함 그 뒤에 모든 형제태그들을 인식한다.
# 자주 쓰는 웹 글꼴 주소
## 노토산스 Noto Sans KR
* <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@100..900&display=swap" rel="stylesheet">
## 프리텐다드 pretendard
* <link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard-dynamic-subset.min.css" />
# css 속성과 값, 활용
## background
* `background-color`: 배경색상, 실제 배경색이 없어도 **영역구분용**으로 많이 사용
* `background- image:url()`: 배경 이미지, url() 안에는 **상대경로**로 작성하기
* `background-repeat`:배경 이미지 반복 설정, 배경이미지가 **작은 경우만** 체크하기
* `background-size`: 배경 이미지 크기 설정, 배경 이미지가 들어간 요소보다 이미지가 작거나 클 경우
* `background-position`: 배경 이미지 위치 설정, **size와 함께 무조건 함께 사용하기, x y 순서로 작성**
* `background-attachment`: 배경 이미지 스크롤 속성, 스크롤 이동시 이미지 고정시키고 싶을때만 사용
* (위) 배경속성 작성 시 주의사항, 배경이미지는 일반 이미지 태그와 다르게 요소의 크기가 자동으로 연장되지 않으므로 **반드시 width, height 크기를 함께 작성해야 합니다.**
## font
`font-family`:글꼴 설정, 2개 이상 글꼴 작성하기
`font-size`: 글자 크기, px-> em으로 전환해서 작성하기
`font-weight`:글자 굵기, 보통(400) +-100 설정
`letter-spacing`: 자간, -2% ->-0.02em
`line-height`: 행간, 100% -> 1
`color`: 글자색상
## box
* `border`: **두께 모양 색상** 순서로 작성 예)1px solid #000; 세미콜론은 맨뒤
* `padding`: 피그마의 오토레이아웃 패딩과 동일, **부모와 자식 사이 안쪽 여백**
* `margin`: 피그마의 오토레이아웃 간격과 동일 **형제와 형제 사이 바깥쪽 여백**
* `width`: 가로 크기(px, %, vw 단위 사용 가능)
    * 피그마 w 내용에 맞추기 설정 시 예) width:max-content;
    * 피그마 채우기 설정 시 예)width:100%;
    * 피그마 W 고정값(숫자 직접 입력 시) 설정 시 예) width:500px;   
* `height`: 세로크기(위 설명과 같음)
* `border-redius`:모서리 둥글기(피그마의 모서리반경과 같음), px 단위 사용
## layout
## 수평, 수직 정렬하기
* ` text-align`: 수평정렬(left, center, right, justify(양쪽?))
* `line-height`: 글자가 1줄이고 높이가 고정되어있을 때 높이값 px를 넣어 수직 중앙정렬 설정