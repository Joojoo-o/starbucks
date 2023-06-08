# 📌 favicon 이미지

> 홈페이지의 타이틀 옆에 뜨는 이미지

#### 📍 favicon 이미지를 자동 생성

- favicon 이미지는 파일을 HTML과 따로 연결해 주지 않아도 자동으로 연결된다.
  **favicon.ico** 으로 파일명을 생성하였을 경우에만 적용된다.

- 프로젝트의 루트 경로에 오픈하여 주면 바로 해석하여 이미지를 연결한다.
  (폴더(images) 안에 favicon.ico 파일을 넣으면 X,
  폴더를 생성하지 X, favicon.ico 파일을 바로 생성하여야 한다.)
  <br>

#### 📍 favicon 이미지를 HTML에 연결해주기

- favicon 이미지를 png파일로 더 선명하게 보여주기 위해 직접 연결도 가능하다.

```
[HTML]
<head>영역의 <title>아래에 작성한다.

<link rel="icon" href="./favicon.png">

```

<br>

---

# 📌 오픈그래프

> 웹 페이지가 소셜미디어(페이스북 등)로 공유될 때 우선적으로 활용되는 정보를 지정한다.

HTML의 head부분에 작성하며,
title아래, link위인 두 태그의 사이에 작성한다.

#### og:type

페이지의 유형
(website, video.movie)

#### og:site_name

속한 사이트의 이름

#### og:title

페이지의 이름 (제목)

#### og:description

페이지의 간단한 설명
(설명은 최대한 간결하게, 장황하게 적지 X)

#### og:image

페이지의 대표 이미지 주소(url)

#### og:url

페이지 주소 (url)

사용 예시)

```
🔎 <meta property="og:type" content="website" />
*meta 태그에 property의 속성이 있고,
*og는 오픈그래프의 약어이며,
*오픈 그래프의: 타입은 웹사이트이다. 라는 뜻이다.

🔎 <meta property="og:site_name" content="Starbucks" />
사이트의 네임은 Starbucks이다.

🔎 <meta property="og:title" content="Starbucks Coffee Korea" />
타이틀 이름은 Starbucks Coffee Korea이다.

🔎 <meta property="og:description" content="스타벅스는 세계에서 가장 큰 ...이다." />
오픈 그래프의 설명은 "스타벅스는 세계에서 가장 큰 ... 이다." 이다.

🔎 <meta property="og:image" content="./images/starbucks_seo.jpg" />
오픈그래프의 이미지는 해당 경로에서 가져온다.

🔎 <meta property="og:url" content="https://starbucks.co.kr" />
오픈 그래프의 주소 경로는 https://starbucks.co.kr 이다.
```

meta 태그는 명확한 정보를 나타내는 것을 제외한 것들을 meta로 표시한다.
이러한 정보들을 **meta정보** 라고도 부른다.

그 외 더 많은 오픈그래프의 속성들이 있다.
(기본 정보들만 정의 해도 괜찮다.)

참고 사이트: https://ogp.me/

## 📍 트위터 카드

> 웹페이지가 트위터로 공유될 때 우선적으로 활용되는 정보를 저장한다.

#### twitter:card

페이지(카드)의 유형
(summary, player)
일반적인 웹사이트는 summary를 사용한다.

#### twitter:site

속한 사이트의 이름

#### twitter:title

페이지의 이름 (제목)

#### twitter:description

페이지의 간단한 설명

#### twitter:image

페이지의 대표 이미지 주소 (url)

#### twitter:url

페이지 주소 (url)
<br>
더 많은 트위터 카드 참고 사이트 : https://developer.twitter.com/en/docs/twitter-for-websites/cards/guides/getting-started
<br>

---

# 📌 Google Fonts 폰트설정

> 각각의 브라우저에 같은 폰트가 설정될 수 있도록 해준다. (유료폰트 사용 시 주의)

\*구글 폰트의 대부분 폰트는 무료이지만, 라이센스를 항상 확인하는 습관 기르기.
<br>

1. 구글에 Google Fonts 검색

- 폰트의 용량
  폰트의 용량이 크므로, 하나의 페이지에서 폰트를 남발하지 않아야 한다.
  (특정 폰트와 두께만 사용하여야 한다.)

2. 원하는 폰트 이름 검색 후 `<link>`와 `@import` 중 선택하여 복사한다.

- `<link>` 태그는 링크 방식으로 병렬로 외부의 css파일을 가져온다.
- `@import` 는 직렬로 css파일에서 외부의 css파일을 가져온다.

대부분 link 태그를 주로 사용한다.

3. HTML에 복사한 font가 main.css의 파일을 link한 것 보다
   먼저 가져와지도록 그 앞에 붙여넣는다.

```
css를 연결한 것 보다 앞의 위치인 이곳에 붙여넣기를 한다.
<link rel="stylesheet" href="./css/main.css" />
```

4. CSS에서 폰트가 적용이 되도록 사이트의 CSS rules to specify families부분을 복사한 후
   CSS의 body부분에 붙여 넣는다.

<br>

---

# 📌 Google Material Icons

#### 📍 Google Material Icons란?

자주사용하는 특정한 이미지나 아이콘들을
Google Material Icons를 이용하여 코드로 삽입할 수 있다.

예) 돋보기, 플러스, 화살표 등... 의 아이콘 과 이미지들

1. 구글에 Google Material Icons를 검색
2. HTML의 link태그, span태그와 CSS의 style태그를
   원하는 것을 복사 후 붙여넣기
3. head에 link를 복붙한 후 아래내용을 적으면 다양한 아이콘을 사용할 수 있다.
   ❓❓❓❓
   head에 붙여넣는 link는 어떠한 걸 복붙 한 후에 구글 아이콘의 이름을 적어야 하나?
   `<link rel="preconnect" href="https://fonts.googleapis.com" />`이것만 넣어주면 아래 처럼 이름만 바꿔도 아이콘 적용이 되나?
   ❓❓❓❓

```
<div class="material-icons">이 사이에 Google font에서 원하는 아이콘의 이름을 적으면 적용이 된다.</div>

👉<div class="material-icons">upload</div>
화살표 아이콘
👉<div class="material-icons">search</div>
돋보기 아이콘

```

💡 아이콘의 이미지 사이즈는 font-size 코드를 통해 설정할 수 있다.

<br>

---

# 📌 헤더와 드롭다운 메뉴 (로고)

## 📍 헤더

> 로고와 서브 메뉴, 메인 메뉴가 있는 영역

#### `<header>` 태그

기능은 없지만,
해더 영역이라는 의미만 가진다.
\*div태그로 header태그를 대신해도 괜찮다.

#### img태그의 특징

img태그는 인라인요소이다.

인라인 요소의 특징
글자를 다루는 요소이다.
글자는 baseline이 존재한다. (소문자를 작성할 때 baseline대로 똑바르게 작성)
인라인은 글자를 취급하기 때문에 baseline을 기준으로 아래에 약간의 공간이 생긴다.
(jyp등의 글자가 삐져나오는 공간이 있기 때문이다.)

💡 **img의 인라인 요소를 블록요소로 바꾸기**

```
[CSS]
body의 아래에 작성한다.

img {
  display: block;
}
이미지의 화면 출력은 블록요소로 한다.

위의 코드를 작성하면 기존 img가 가진 인라인 요소가 블록 요소로 변경되어
아래 공간이 생기지 않게 된다.
```

#### 📍 가운데 배치

가운데 정렬이 아닌 배치를 할 때

💡 css에서 **위아래 가운데 배치**를 하기 위해서는 필수요소들이 있다.

1. position
   (부모요소에 relative와 자식요소에 absolute가 적용되어야한다.)
2. top
3. bottom
4. height
5. margin: auto 0;

💡 위 4가지를 모두 작성하여야 하며,
**좌우 가운데 배치**를 하기 위해서는 아래와 같이 작성되어야 한다.

1. position
2. right
3. left
4. width
5. margin: 0 auto;
