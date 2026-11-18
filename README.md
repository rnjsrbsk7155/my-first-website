
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MUTE ME - Your Color, Your Mood</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=Noto+Sans+KR:wght@300;400;500;600&display=swap');

:root {
 --bg:#faf7f5;
 --paper:#fffdfb;
 --rose:#b78e92;
 --mauve:#8d737f;
 --deep:#70585e;
 --line:#eadfdb;
 --soft:#f1e8e4;
 --text:#443b3b;
}

* {
 box-sizing:border-box;
 margin:0;
 padding:0;
}

body {
 font-family:'Noto Sans KR',sans-serif;
 background:var(--bg);
 color:var(--text);
 line-height:1.7;
}

button,input {font:inherit;}
button {cursor:pointer;}
a {text-decoration:none;color:inherit;}

header {
 position:sticky;
 top:0;
 z-index:100;
 background:#faf7f5f5;
 border-bottom:1px solid var(--line);
}

.nav {
 max-width:1150px;
 margin:auto;
 padding:18px 5%;
 display:flex;
 justify-content:space-between;
 align-items:center;
}

.logo {
 font-family:'DM Serif Display',serif;
 font-size:30px;
 color:var(--mauve);
 letter-spacing:3px;
}

.logo small {
 display:block;
 font:8px 'Noto Sans KR';
 text-align:center;
 letter-spacing:3px;
}

nav {
 display:flex;
 gap:25px;
 font-size:12px;
}

nav a:hover {color:var(--rose);}

section {padding:85px 8%;}

.container {
 max-width:1150px;
 margin:auto;
}

.hero {
 min-height:560px;
 display:grid;
 grid-template-columns:1fr 1fr;
 background:#e9ded9;
}

.hero-text {
 padding:80px 10%;
 display:flex;
 flex-direction:column;
 justify-content:center;
}

.kicker {
 color:var(--rose);
 font-size:11px;
 letter-spacing:3px;
}

.hero h1 {
 font:clamp(55px,7vw,85px)/1.05 'DM Serif Display';
 color:#735c61;
 margin:25px 0;
}

.hero h1 em {color:#ae858a;}

.hero p {
 font-size:13px;
 color:#796c69;
 line-height:2;
}

.btn {
 display:inline-block;
 width:max-content;
 margin-top:25px;
 padding:12px 23px;
 border:1px solid var(--mauve);
 color:var(--deep);
 font-size:11px;
 letter-spacing:2px;
}

.btn:hover {
 background:var(--mauve);
 color:white;
}

.hero-image {
 min-height:450px;
 background:linear-gradient(135deg,#efd8d2,#d9c0bd);
 display:flex;
 align-items:center;
 justify-content:center;
 font-size:100px;
}

.ticker {
 background:var(--deep);
 color:white;
 padding:13px;
 text-align:center;
 font-size:10px;
 letter-spacing:2px;
}

.ticker b {color:#e8c9c7;}

.heading {
 text-align:center;
 margin-bottom:40px;
}

.heading h2 {
 font:42px 'DM Serif Display';
 color:var(--deep);
 margin:10px 0;
}

.heading p {
 font-size:12px;
 color:#887a78;
}

/* 퍼스널 컬러 */

.tones {
 display:grid;
 grid-template-columns:repeat(3,1fr);
 gap:15px;
}

.tone-card {
 background:var(--paper);
 border:1px solid var(--line);
 padding:23px;
 text-align:left;
 transition:.2s;
}

.tone-card:hover,
.tone-card.active {
 border-color:var(--rose);
 transform:translateY(-3px);
 box-shadow:0 10px 25px #70585e15;
}

.tone-card h3 {
 font-size:15px;
 margin:8px 0;
}

.tone-card p {
 font-size:11px;
 color:#887a78;
}

.swatches {
 display:flex;
 gap:8px;
 margin-top:15px;
}

.swatches span {
 width:25px;
 height:25px;
 border-radius:50%;
}

.tone-detail {
 background:var(--soft);
 padding:25px;
 margin-top:20px;
 font-size:12px;
}

.tone-detail h3 {
 font-size:18px;
 margin-bottom:8px;
}

.tone-detail button {
 margin-top:15px;
 padding:10px 18px;
 border:1px solid var(--mauve);
 background:transparent;
 color:var(--deep);
}

/* 매거진 */

.magazine {
 background:#eee5e0;
}

.cover {
 display:grid;
 grid-template-columns:1fr 1fr;
 background:#faf6f2;
}

.cover-image {
 min-height:350px;
 background:linear-gradient(140deg,#d7b9b2,#a7838b);
 display:flex;
 align-items:center;
 justify-content:center;
 font-size:120px;
}

.cover-text {
 padding:50px;
 display:flex;
 flex-direction:column;
 justify-content:center;
}

.cover-text h2 {
 font:55px/1.1 'DM Serif Display';
 color:var(--deep);
 margin:20px 0;
}

.cover-text p {
 font-size:12px;
 color:#887a78;
 line-height:2;
}

.articles {
 display:grid;
 grid-template-columns:repeat(3,1fr);
 gap:18px;
 margin-top:25px;
}

.article {
 background:white;
}

.article-image {
 height:160px;
 display:grid;
 place-items:center;
 font-size:60px;
}

.article-text {padding:20px;}

.article-text small {
 color:var(--rose);
 letter-spacing:2px;
}

.article-text h3 {
 font-size:15px;
 margin:8px 0;
}

.article-text p {
 font-size:11px;
 color:#887a78;
}

/* 계절 트렌드 */

.season-tabs,
.rank-tabs,
.filters {
 display:flex;
 justify-content:center;
 gap:10px;
 flex-wrap:wrap;
 margin-bottom:25px;
}

.pill {
 border:1px solid var(--line);
 background:white;
 padding:10px 20px;
 color:#756866;
 font-size:11px;
}

.pill.active,
.pill:hover {
 background:var(--mauve);
 color:white;
}

.season-panel {
 display:grid;
 grid-template-columns:1fr 1fr;
 background:#f0e6e2;
}

.season-art {
 min-height:300px;
 display:flex;
 flex-direction:column;
 justify-content:center;
 align-items:center;
 background:#e6d4ce;
 font-size:75px;
}

.season-art h3 {
 font:30px 'DM Serif Display';
 color:var(--deep);
}

.season-text {
 padding:40px;
 display:flex;
 flex-direction:column;
 justify-content:center;
}

.season-text h3 {
 font-size:23px;
 margin:10px 0;
}

.season-text p {
 font-size:12px;
 color:#887a78;
}

.palette {
 display:flex;
 gap:15px;
 flex-wrap:wrap;
 margin-top:20px;
}

.palette div {
 text-align:center;
 font-size:10px;
}

.palette span {
 display:block;
 width:30px;
 height:30px;
 border-radius:50%;
 margin:auto auto 5px;
}

/* 랭킹 및 제품 */

.ranking {background:#f4eeeb;}

.product-grid {
 display:grid;
 grid-template-columns:repeat(3,1fr);
 gap:18px;
}

.product-card {
 background:white;
 border:1px solid var(--line);
 position:relative;
}

.rank {
 position:absolute;
 top:12px;
 left:12px;
 background:var(--deep);
 color:white;
 padding:5px 12px;
 z-index:2;
}

.product-image {
 height:220px;
 background:#f4eeeb;
 display:grid;
 place-items:center;
 overflow:hidden;
}

.product-image img {
 width:100%;
 height:100%;
 object-fit:contain;
 padding:12px;
}

.product-info {padding:20px;}

.product-info small {
 color:var(--rose);
 letter-spacing:2px;
}

.product-info h3 {
 font-size:14px;
 margin:8px 0;
}

.product-info p {
 font-size:11px;
 color:#887a78;
}

.favorite {
 margin-top:12px;
 border:1px solid var(--line);
 background:white;
 color:var(--rose);
 padding:6px 12px;
 font-size:11px;
}

.favorite.saved {
 background:#f0dfe0;
}

.search {
 display:block;
 width:min(450px,100%);
 margin:0 auto 25px;
 padding:13px 20px;
 border:1px solid var(--line);
 border-radius:30px;
 outline:none;
}

.note {
 text-align:center;
 font-size:10px;
 color:#887a78;
 margin-top:25px;
}

footer {
 background:var(--deep);
 color:white;
 text-align:center;
 padding:45px;
}

footer h2 {
 font:35px 'DM Serif Display';
 letter-spacing:4px;
}

footer p {
 font-size:10px;
 color:#e0d2cd;
 margin-top:12px;
}

@media(max-width:750px) {
 .nav {flex-wrap:wrap;}
 nav {gap:12px;flex-wrap:wrap;font-size:10px;}
 .hero {grid-template-columns:1fr;}
 .hero-image {min-height:250px;}
 .tones {grid-template-columns:repeat(2,1fr);}
 .cover,.season-panel {grid-template-columns:1fr;}
 .articles {grid-template-columns:1fr;}
 .product-grid {grid-template-columns:repeat(2,1fr);}
 .cover-text {padding:30px;}
}

@media(max-width:480px) {
 section {padding:60px 5%;}
 .heading h2 {font-size:34px;}
 .tones,.product-grid {grid-template-columns:1fr;}
 .season-text {padding:25px;}
}
</style>
</head>

<body>

<header>
 <div class="nav">
  <a href="#home" class="logo">
   MUTE ME
   <small>YOUR COLOR, YOUR MOOD</small>
  </a>
  <nav>
   <a href="#home">HOME</a>
   <a href="#color">COLOR</a>
   <a href="#magazine">MAGAZINE</a>
   <a href="#season">SEASON</a>
   <a href="#ranking">RANKING</a>
   <a href="#products">PRODUCT</a>
  </nav>
 </div>
</header>

<main>

<!-- 메인 화면 -->

<section class="hero" id="home">
 <div class="hero-text">
  <div class="kicker">MUTE ME EDITORIAL · 2026</div>
  <h1>Find Your<br><em>Muted</em><br>Mood.</h1>
  <p>
   나에게 어울리는 색을 발견하는 시간.<br>
   퍼스널 컬러부터 계절별 뷰티 트렌드까지,<br>
   MUTE ME에서 나만의 분위기를 찾아보세요.
  </p>
  <a class="btn" href="#color">DISCOVER YOUR COLOR →</a>
 </div>
 <div class="hero-image">🌸 💄</div>
</section>

<div class="ticker">
 THIS MONTH'S MOOD ·
 <b>MUTED ROSE / SOFT MAUVE / NEUTRAL BEIGE</b>
</div>

<!-- 퍼스널 컬러 -->

<section id="color">
 <div class="container">
  <div class="heading">
   <div class="kicker">FIND YOUR COLOR</div>
   <h2>Personal Color</h2>
   <p>나에게 어울리는 분위기를 선택해 보세요.</p>
  </div>

  <div class="tones" id="toneGrid"></div>
  <div class="tone-detail" id="toneDetail">
   원하는 퍼스널 컬러를 선택해 주세요.
  </div>
 </div>
</section>

<!-- 매거진 -->

<section class="magazine" id="magazine">
 <div class="container">
  <div class="heading">
   <div class="kicker">MUTE ME EDITORIAL</div>
   <h2>Beauty Magazine</h2>
   <p>이번 시즌의 컬러와 메이크업 이야기를 만나보세요.</p>
  </div>

  <div class="cover">
   <div class="cover-image">🌹</div>
   <div class="cover-text">
    <small>THE AUTUMN ISSUE · 2026</small>
    <h2>The Art of<br>Muted Beauty</h2>
    <p>
     선명함보다 은은함이 매력적인 계절.<br>
     말린 장미, 모브 브라운, 로즈 베이지처럼<br>
     차분한 색으로 나만의 분위기를 완성해 보세요.
    </p>
   </div>
  </div>

  <div class="articles">
   <article class="article">
    <div class="article-image" style="background:#ead9d5">🌹</div>
    <div class="article-text">
     <small>COLOR STORY 01</small>
     <h3>가을 뮤트의 매력</h3>
     <p>말린 장미와 모브, 부드러운 브라운으로 차분한 분위기를 연출해요.</p>
    </div>
   </article>

   <article class="article">
    <div class="article-image" style="background:#e9dfd4">🤎</div>
    <div class="article-text">
     <small>COLOR STORY 02</small>
     <h3>뉴트럴 컬러의 발견</h3>
     <p>웜과 쿨의 경계를 넘나드는 베이지와 로즈 토프를 활용해요.</p>
    </div>
   </article>

   <article class="article">
    <div class="article-image" style="background:#ded9df">☁️</div>
    <div class="article-text">
     <small>MAKEUP STORY 03</small>
     <h3>소프트 블러 메이크업</h3>
     <p>블러 립과 은은한 치크, 자연스러운 피부 표현을 만나보세요.</p>
    </div>
   </article>
  </div>
 </div>
</section>

<!-- 계절별 트렌드 -->

<section id="season">
 <div class="container">
  <div class="heading">
   <div class="kicker">SEASONAL COLOR REPORT</div>
   <h2>Season Trend</h2>
   <p>계절을 선택하면 해당 시즌의 추천 컬러를 볼 수 있어요.</p>
  </div>

  <div class="season-tabs">
   <button class="pill active" data-season="autumn">🍂 AUTUMN</button>
   <button class="pill" data-season="winter">❄️ WINTER</button>
   <button class="pill" data-season="spring">🌷 SPRING</button>
   <button class="pill" data-season="summer">☀️ SUMMER</button>
  </div>

  <div class="season-panel">
   <div class="season-art" id="seasonArt">
    <span>🍂</span>
    <h3>AUTUMN MOOD</h3>
   </div>
   <div class="season-text">
    <div class="kicker" id="seasonLabel">AUTUMN EDITION</div>
    <h3 id="seasonTitle">가을 뮤트 & 뉴트럴</h3>
    <p id="seasonDesc">
     말린 장미, 모브 브라운, 로즈 베이지처럼
     차분한 저채도 컬러를 활용해 보세요.
    </p>
    <div class="palette" id="palette"></div>
   </div>
  </div>
 </div>
</section>

<!-- 랭킹 -->

<section class="ranking" id="ranking">
 <div class="container">
  <div class="heading">
   <div class="kicker">EDITOR'S SELECTION</div>
   <h2>Beauty Ranking</h2>
   <p>립, 치크, 팩트별 추천 제품을 확인해 보세요.</p>
  </div>

  <div class="rank-tabs">
   <button class="pill active" data-rank="lip">LIP</button>
   <button class="pill" data-rank="cheek">CHEEK</button>
   <button class="pill" data-rank="pact">PACT</button>
  </div>

  <div class="product-grid" id="rankGrid"></div>

  <p class="note">
   ※ MUTE ME 편집부 추천 순서이며 실시간 판매량 순위가 아닙니다.
   정확한 제품 옵션과 호수는 브랜드 공식 정보를 확인해 주세요.
  </p>
 </div>
</section>

<!-- 제품 추천 -->

<section id="products">
 <div class="container">
  <div class="heading">
   <div class="kicker">CURATED FOR YOUR COLOR</div>
   <h2>Product Pick</h2>
   <p>나의 퍼스널 컬러에 맞는 제품을 찾아보세요.</p>
  </div>

  <input class="search" id="search"
   placeholder="브랜드 · 제품명 · 컬러 검색">

  <div class="filters">
   <button class="pill active" data-filter="전체">전체</button>
   <button class="pill" data-filter="봄웜톤">봄웜</button>
   <button class="pill" data-filter="여름쿨톤">여름쿨</button>
   <button class="pill" data-filter="가을웜톤">가을웜</button>
   <button class="pill" data-filter="겨울쿨톤">겨울쿨</button>
   <button class="pill" data-filter="뉴트럴톤">뉴트럴</button>
   <button class="pill" data-filter="뮤트톤">뮤트</button>
  </div>

  <div class="product-grid" id="productGrid"></div>
 </div>
</section>

</main>

<div class="note">
 MUTE ME는 퍼스널 컬러와 뷰티 제품을 소개하는 큐레이션 사이트입니다.
 제품 추천은 참고용이며 실제 발색은 개인에 따라 다를 수 있습니다.
</div>

<footer>
 <h2>MUTE ME</h2>
 <p>
  YOUR COLOR, YOUR MOOD.<br>
  Find your color. Discover your beauty.<br>
  © 2026 MUTE ME BEAUTY JOURNAL
 </p>
</footer>

<script>

// 퍼스널 컬러 데이터

const tones = [
 {
  name:"봄웜톤 라이트",
  group:"봄웜톤",
  emoji:"🌷",
  desc:"밝고 맑은 피치와 코랄",
  colors:["#F5C5AD","#F2A58D","#F5D7A9"],
  detail:"밝고 따뜻한 피치, 살구, 코랄 컬러로 화사한 분위기를 연출해 보세요."
 },
 {
  name:"봄웜톤 브라이트",
  group:"봄웜톤",
  emoji:"🍑",
  desc:"선명한 코랄과 웜 핑크",
  colors:["#F28D78","#F5A37C","#E86F68"],
  detail:"맑고 선명한 코랄과 오렌지 핑크가 포인트예요."
 },
 {
  name:"여름쿨톤 라이트",
  group:"여름쿨톤",
  emoji:"🫧",
  desc:"맑은 핑크와 라벤더",
  colors:["#E8C9D8","#CFC6E1","#C8D9E7"],
  detail:"라이트 핑크와 라벤더로 맑고 투명한 분위기를 연출해 보세요."
 },
 {
  name:"여름쿨톤 뮤트",
  group:"여름쿨톤",
  emoji:"☁️",
  desc:"차분한 모브와 더스티 로즈",
  colors:["#B99AA9","#C6A7AC","#A99BAE"],
  detail:"모브, 더스티 로즈, 소프트 플럼처럼 회색기가 섞인 컬러가 잘 어울려요."
 },
 {
  name:"가을웜톤 뮤트",
  group:"가을웜톤",
  emoji:"🍂",
  desc:"로즈 브라운과 그레이지",
  colors:["#B68D85","#A98B7D","#B8A49A"],
  detail:"말린 장미, 로즈 브라운, 그레이지로 차분하고 부드러운 분위기를 연출해 보세요."
 },
 {
  name:"가을웜톤 딥",
  group:"가을웜톤",
  emoji:"🤎",
  desc:"브릭과 초콜릿 브라운",
  colors:["#A35F4B","#80513F","#68483D"],
  detail:"브릭, 테라코타, 초콜릿 브라운으로 깊이 있는 음영을 더해 보세요."
 },
 {
  name:"겨울쿨톤 브라이트",
  group:"겨울쿨톤",
  emoji:"💎",
  desc:"베리와 푸시아",
  colors:["#C13E72","#A52D61","#D34B87"],
  detail:"선명한 베리, 푸시아, 체리 레드로 또렷한 포인트를 만들어 보세요."
 },
 {
  name:"겨울쿨톤 딥",
  group:"겨울쿨톤",
  emoji:"🫐",
  desc:"와인과 플럼",
  colors:["#733A58","#65476E","#4C344C"],
  detail:"와인, 플럼, 딥 버건디처럼 깊은 쿨 컬러를 추천해요."
 },
 {
  name:"뉴트럴톤",
  group:"뉴트럴톤",
  emoji:"🤍",
  desc:"로즈 베이지와 토프",
  colors:["#C7A49B","#B9A49B","#D8C2B2"],
  detail:"로즈 베이지, 토프, 뉴트럴 핑크처럼 균형 잡힌 색을 활용해 보세요."
 },
 {
  name:"뮤트톤",
  group:"뮤트톤",
  emoji:"🪞",
  desc:"저채도 소프트 컬러",
  colors:["#B58F91","#A59698","#BDA99E"],
  detail:"뮤트는 웜·쿨과 별개의 온도 구분이 아니라 저채도 색감의 특징이에요. 자신의 웜·쿨 방향과 함께 살펴보세요."
 }
];

// 제품 데이터

const products = [
 {tone:"봄웜톤",brand:"rom&nd",name:"쥬시 래스팅 틴트",shade:"피치 계열 컬러",type:"립",image:"https://jbeauty.fi/cdn/shop/collections/Romand-Hanbok_1.jpg?v=1726837387"},
 {tone:"봄웜톤",brand:"VDL",name:"치크스테인 블러셔",shade:"피치 계열 컬러",type:"치크",image:"https://cloudflare.lipscosme.com/image/d449b6c3b758ac06ce434b31-1715403442.png?auto=avif%2Cwebp&fio=1&orient=1&width=430"},
 {tone:"여름쿨톤",brand:"ETUDE",name:"픽싱 틴트",shade:"05 Midnight Mauve",type:"립",image:"https://kozmetikumbolt.cdn.shoprenter.hu/custom/kozmetikumbolt/image/data/ETUDE/etude-house-fixing-tint-05-midnight-mauve-koreashop.webp"},
 {tone:"여름쿨톤",brand:"peripera",name:"선샤인 치크",shade:"024 Mauve Cream",type:"치크",image:"https://cdn.hstatic.net/products/200000977139/m__h_ng_peripera_pure_blushed_sunshine_cheek__24_mauve_cream__1__a1e3635e2c424b1b826df7928312a58a_master.png"},
 {tone:"가을웜톤",brand:"rom&nd",name:"쥬시 래스팅 틴트",shade:"로즈 브라운 계열",type:"립",image:"https://jbeauty.fi/cdn/shop/collections/Romand-Hanbok_1.jpg?v=1726837387"},
 {tone:"가을웜톤",brand:"VDL",name:"치크스테인 블러셔",shade:"웜 베이지 계열",type:"치크",image:"https://cloudflare.lipscosme.com/image/d449b6c3b758ac06ce434b31-1715403442.png?auto=avif%2Cwebp&fio=1&orient=1&width=430"},
 {tone:"겨울쿨톤",brand:"rom&nd",name:"쥬시 래스팅 틴트",shade:"베리·플럼 계열",type:"립",image:"https://jbeauty.fi/cdn/shop/collections/Romand-Hanbok_1.jpg?v=1726837387"},
 {tone:"겨울쿨톤",brand:"peripera",name:"선샤인 치크",shade:"쿨 핑크 계열",type:"치크",image:"https://cdn.hstatic.net/products/200000977139/m__h_ng_peripera_pure_blushed_sunshine_cheek__24_mauve_cream__1__a1e3635e2c424b1b826df7928312a58a_master.png"},
 {tone:"뉴트럴톤",brand:"ETUDE",name:"픽싱 틴트",shade:"로즈 베이지 계열",type:"립",image:"https://kozmetikumbolt.cdn.shoprenter.hu/custom/kozmetikumbolt/image/data/ETUDE/etude-house-fixing-tint-05-midnight-mauve-koreashop.webp"},
 {tone:"뉴트럴톤",brand:"lilybyred",name:"러브빔 치크밤",shade:"피치·로즈 계열",type:"치크",image:"https://merryseasons.com.au/cdn/shop/files/01_54c2f855-516e-4f60-aef0-0e48015508b4_1024x1024.jpg"},
 {tone:"뮤트톤",brand:"ETUDE",name:"픽싱 틴트",shade:"05 Midnight Mauve",type:"립",image:"https://kozmetikumbolt.cdn.shoprenter.hu/custom/kozmetikumbolt/image/data/ETUDE/etude-house-fixing-tint-05-midnight-mauve-koreashop.webp"},
 {tone:"뮤트톤",brand:"peripera",name:"선샤인 치크",shade:"024 Mauve Cream",type:"치크",image:"https://cdn.hstatic.net/products/200000977139/m__h_ng_peripera_pure_blushed_sunshine_cheek__24_mauve_cream__1__a1e3635e2c424b1b826df7928312a58a_master.png"},
 {tone:"뮤트톤",brand:"IPKN&",name:"퍼스널 톤 코렉팅 블러 팩트",shade:"Lavender",type:"팩트",image:"https://images-cdn.ubuy.co.in/675a97298ed2d27a25620741-ipkn-personal-tone-correcting-blur-pact.jpg"},
 {tone:"가을웜톤",brand:"innisfree",name:"노세범 미네랄 팩트",shade:"기본 컬러",type:"팩트",image:"https://cdn.makeupshop.ro/imagini-makeup/produse/original/no-sebum-mineral-pact-4-5zpzlun0.jpg"}
];

// 랭킹 데이터

const rankings = {
 lip:[2,4,10],
 cheek:[3,5,9],
 pact:[12,13,11]
};

// 계절 데이터

const seasons = {
 autumn:{
  emoji:"🍂",title:"가을 뮤트 & 뉴트럴",
  desc:"말린 장미, 모브 브라운, 로즈 베이지처럼 차분한 저채도 컬러를 활용해 보세요.",
  colors:[["말린 장미","#B58388"],["모브","#A58B96"],["로즈 베이지","#C49B91"],["그레이지","#A99B91"]]
 },
 winter:{
  emoji:"❄️",title:"겨울 쿨 & 딥 컬러",
  desc:"베리, 플럼, 딥 로즈와 같은 깊이 있는 색으로 포인트를 줘보세요.",
  colors:[["베리","#A33B5F"],["플럼","#795E88"],["딥 로즈","#A66D80"],["차콜","#69636D"]]
 },
 spring:{
  emoji:"🌷",title:"봄 웜 & 소프트 컬러",
  desc:"피치, 코랄, 살구, 크림 베이지처럼 따뜻하고 밝은 색으로 화사한 분위기를 연출해 보세요.",
  colors:[["피치","#F2B39D"],["코랄","#E88D79"],["크림","#EBD5B8"],["살구","#E6AC85"]]
 },
 summer:{
  emoji:"☀️",title:"여름 쿨 & 라이트 뮤트",
  desc:"라벤더, 소프트 핑크, 모브 등 시원하고 부드러운 색을 활용해 보세요.",
  colors:[["라벤더","#C7B6D9"],["핑크","#E4BBCB"],["모브","#AB91A8"],["블루","#B7CADB"]]
 }
};

// 톤 화면 출력

function renderTones() {
 const grid=document.getElementById("toneGrid");

 grid.innerHTML=tones.map((t,i)=>`
  <button class="tone-card" data-index="${i}">
   <div>${t.emoji}</div>
   <h3>${t.name}</h3>
   <p>${t.desc}</p>
   <div class="swatches">
    ${t.colors.map(c=>`<span style="background:${c}"></span>`).join("")}
   </div>
  </button>
 `).join("");

 grid.querySelectorAll("button").forEach(btn=>{
  btn.addEventListener("click",()=>{
   const i=Number(btn.dataset.index);
   const t=tones[i];

   grid.querySelectorAll("button").forEach(b=>b.classList.remove("active"));
   btn.classList.add("active");

   document.getElementById("toneDetail").innerHTML=`
    <h3>${t.emoji} ${t.name}</h3>
    <p>${t.detail}</p>
    <button onclick="filterProducts('${t.group}')">
     이 톤의 제품 보기 →
    </button>
   `;
  });
 });
}

// 계절 화면 출력

function renderSeason(key) {
 const s=seasons[key];

 document.getElementById("seasonArt").innerHTML=`
  <span>${s.emoji}</span>
  <h3>${key.toUpperCase()} MOOD</h3>
 `;

 document.getElementById("seasonTitle").textContent=s.title;
 document.getElementById("seasonDesc").textContent=s.desc;

 document.getElementById("palette").innerHTML=
  s.colors.map(c=>`
   <div>
    <span style="background:${c[1]}"></span>
    ${c[0]}
   </div>
  `).join("");

 document.querySelectorAll("[data-season]").forEach(b=>{
  b.classList.toggle("active",b.dataset.season===key);
 });
}

// 제품 카드

function productCard(p,index,ranking=false) {
 const id=products.indexOf(p);

 return `
 <article class="product-card">
  ${ranking?`<div class="rank">${index+1}위</div>`:""}
  <div class="product-image">
   <img src="${p.image}" alt="${p.brand} ${p.name}"
    loading="lazy"
    onerror="this.style.display='none';">
  </div>
  <div class="product-info">
   <small>${p.brand} · ${p.tone}</small>
   <h3>${p.name}</h3>
   <p>${p.shade}</p>
   <p>${p.type}</p>
   ${ranking?"":`
    <button class="favorite" data-id="${id}">♡ 저장</button>
   `}
  </div>
 </article>
 `;
}

// 랭킹 출력

function renderRanking(type) {
 const list=rankings[type];

 document.getElementById("rankGrid").innerHTML=
  list.map((id,i)=>productCard(products[id],i,true)).join("");

 document.querySelectorAll("[data-rank]").forEach(b=>{
  b.classList.toggle("active",b.dataset.rank===type);
 });
}

// 제품 필터 및 검색

let currentFilter="전체";

function filterProducts(filter) {
 currentFilter=filter;

 document.querySelectorAll("[data-filter]").forEach(b=>{
  b.classList.toggle("active",b.dataset.filter===filter);
 });

 renderProducts();
}

function renderProducts() {
 const keyword=document.getElementById("search").value.toLowerCase();

 const list=products.filter(p=>
  (currentFilter==="전체" || p.tone===currentFilter) &&
  [p.brand,p.name,p.shade,p.tone,p.type]
   .join(" ").toLowerCase().includes(keyword)
 );

 document.getElementById("productGrid").innerHTML=
  list.length
   ?list.map(p=>productCard(p,0)).join("")
   :"<p>검색 결과가 없습니다.</p>";

 document.querySelectorAll(".favorite").forEach(btn=>{
  const id=btn.dataset.id;
  let saved=JSON.parse(localStorage.getItem("muteFavorites")||"[]");

  if(saved.includes(id)){
   btn.classList.add("saved");
   btn.textContent="♥ 저장됨";
  }

  btn.addEventListener("click",()=>{
   let arr=JSON.parse(localStorage.getItem("muteFavorites")||"[]");

   if(arr.includes(id)){
    arr=arr.filter(x=>x!==id);
   } else {
    arr.push(id);
   }

   localStorage.setItem("muteFavorites",JSON.stringify(arr));
   btn.classList.toggle("saved",arr.includes(id));
   btn.textContent=arr.includes(id)?"♥ 저장됨":"♡ 저장";
  });
 });
}

// 버튼 이벤트

document.querySelectorAll("[data-season]").forEach(btn=>{
 btn.addEventListener("click",()=>{
  renderSeason(btn.dataset.season);
 });
});

document.querySelectorAll("[data-rank]").forEach(btn=>{
 btn.addEventListener("click",()=>{
  renderRanking(btn.dataset.rank);
 });
});

document.querySelectorAll("[data-filter]").forEach(btn=>{
 btn.addEventListener("click",()=>{
  filterProducts(btn.dataset.filter);
 });
});

document.getElementById("search").addEventListener("input",renderProducts);

// 최초 실행

renderTones();
renderSeason("autumn");
renderRanking("lip");
renderProducts();

</script>
</body>
</html>

