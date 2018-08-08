# README

**Web Published: nykim@nykim.net**

_Last Modified: 2018-08-07_

## Tree Structure

- css/
  - scss/
    - base/
      - common.scss
      - reset.scss
    - helpers/
      - mediaQueries.scss
      - mixins.scss
      - variables.scss
    - layout/
      - main.scss
    - style.scss
  - style.css
- images/
- js/
- index.html

## Markup Contents

- 전체를 #wrapper 라는 div 로 감싸고 있습니다.
- #wrapper 는 페이지 역할에 따라 고유의 클래스(예: .login)를 갖습니다.
  - .login: 로그인 페이지
  - .user-infomration: 사용자 정보 입력
  - .wallet-setting: 지갑 설정
- 대부분의 페이지 구조는 .page-header 와 .page-body 로 이루어집니다.
- .page-header 에는 해당 페이지의 타이틀이나 네비게이션 등이 들어갑니다.
- .page-body 에는 콘텐츠가 들어갑니다.

## CSS Guide

### 1.fonts

- 기본 폰트는 '나눔스퀘어체'를 사용하며, /\_font.scss 에서 정의합니다.
  - 400: Regular
  - 600: Bold
  - 800: ExtraBold
- 보조 폰트는 ''를 사용하며, /\_font.scss 에서 정의합니다.
  - 300: Light
  - 800: Bold

### 2.variables

- \_variables.scss 에서 정의하고 있는 변수는 다음과 같습니다.
  - layout
  - z-idnex : z-index 값이 필요한 요소 별로 z-index 변수를 개별 생성합니다. 이는 z-index 를 사용하고 있는 요소가 무엇인지 한눈에 파악하고 일괄 관리하기 위함입니다.
  - path : 상대경로를 사용하는 경우 여기에 정의한 path 변수를 사용합니다.
  - font-weight

### 3.common style

- 공통으로 사용하는 스타일은 modules/ 폴더 내 개별 scss 에서 정의합니다.

  1.  **Button**

  - btn-style01 : 양옆이 둥그런 파란색 버튼
  - btn-style02 : btn-style01 과 동일하되, active 클래스가 붙지 않으면 회색
  - btn-style03 : 링크처럼 생긴 버튼 (예: 회원가입)

  2.  **Input**

  - input-style01 : 연한 배경 인풋
  - select-style01 : 셀렉트 박스 형태를 가진, 오른쪽에 화살표가 있는 인풋

  3.  **Select**

  - 셀렉트의 경우, ui 만 input 으로 표시하며 유저가 터치 시 별도로 드롭 박스를 보여줍니다. (미확정)

  * select-style01 : input-style01 과 동일
  * select-style02: input-style02 와 동일

  4.  **Radio**

  - radio-type01 : 모서리가 살짝 둥근 라디오
