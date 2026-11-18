
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MUTE ME | Your Color, Your Mood</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=Noto+Sans+KR:wght@300;400;500;600;700&display=swap');

:root {
  --bg:#FAF8F6;
  --white:#FFFFFF;
  --rose:#B88D91;
  --mauve:#8D737F;
  --brown:#75635D;
  --gray:#A69A95;
  --line:#EAE2DE;
  --light:#F1E9E5;
  --ink:#453D3B;
}

* {
  margin:0;
  padding:0;
  box-sizing:border-box;
}

html {scroll-behavior:smooth;}

body {
  background:var(--bg);
  color:var(--ink);
  font-family:'Noto Sans KR',sans-serif;
}

button,input {font:inherit;}

a {
  color:inherit;
  text-decoration:none;
}

img {
  display:block;
  max-width:100%;
}

/* HEADER */

header {
  height:76px;
  background:#FAF8F6F2;
  backdrop-filter:blur(12px);
  border-bottom:1px solid var(--line);
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding:0 7%;
  position:sticky;
  top:0;
  z-index:100;
}

.logo {
  font-family:'DM Serif Display',serif;
  font-size:31px;
  letter-spacing:2px;
  color:var(--mauve);
}

.logo small {
  display:block;
  font-family:'Noto Sans KR',sans-serif;
  font-size:8px;
  letter-spacing:3px;
  text-align:center;
  margin-top:-5px;
}

nav {
  display:flex;
  gap:26px;
}

nav a {
  font-size:12px;
  letter-spacing:1px;
  color:#655A56;
}

nav a:hover {color:var(--rose);}

.menu-btn {
  display:none;
  border:0;
  background:none;
  font-size:24px;
  cursor:pointer;
}

/* COMMON */

.section {
  padding:100px 8%;
  scroll-margin-top:75px;
}

.inner {
  max-width:1200px;
  margin:auto;
}

.eyebrow {
  font-size:10px;
  letter-spacing:4px;
  color:var(--rose);
  margin-bottom:15px;
  font-weight:600;
}

.section-heading {
  text-align:center;
  margin-bottom:50px;
}

.section-heading h2 {
  font-family:'DM Serif Display',serif;
  font-size:39px;
  font-weight:400;
  margin-bottom:12px;
}

.section-heading p {
  font-size:13px;
  line-height:1.9;
  color:#998D88;
}

/* HOME */

.hero {
  min-height:640px;
  display:grid;
  grid-template-columns:1.05fr .95fr;
  background:#EAE0DC;
}

.hero-text {
  padding:100px 10% 80px 15%;
  display:flex;
  flex-direction:column;
  justify-content:center;
}

.hero-text .mini {
  font-size:11px;
  letter-spacing:4px;
  color:#96767A;
  margin-bottom:25px;
}

.hero-text h1 {
  font-family:'DM Serif Display',serif;
  font-size:76px;
  font-weight:400;
  line-height:1.05;
  color:#6C5358;
}

.hero-text h1 span {
  font-style:italic;
  color:#A98286;
}

.hero-text p {
  font-size:14px;
  line-height:2;
  color:#766A66;
  margin-top:25px;
}

.hero-btn {
  width:fit-content;
  margin-top:32px;
  padding:14px 29px;
  border:1px solid #A98286;
  color:#765B60;
  font-size:11px;
  letter-spacing:2px;
  transition:.3s;
}

.hero-btn:hover {
  background:#A98286;
  color:white;
}

.hero-photo {
  min-height:500px;
  background:
    linear-gradient(#00000008,#00000008),
    url('https://jbeauty.fi/cdn/shop/collections/Romand-Hanbok_1.jpg?v=1726837387')
    center/cover;
}

/* TREND BAR */

.trend-bar {
  background:#75635D;
  color:white;
  text-align:center;
  padding:17px;
  font-size:11px;
  letter-spacing:2px;
}

.trend-bar span {
  color:#E6C5C4;
  font-weight:bold;
}

/* PERSONAL COLOR */

.tone-grid {
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:17px;
}

.tone-card {
  background:white;
  border:1px solid var(--line);
  padding:27px;
  cursor:pointer;
  transition:.3s;
}

.tone-card:hover,
.tone-card.active {
  border-color:var(--rose);
  transform:translateY(-4px);
  box-shadow:0 10px 25px #75635D12;
}

.tone-icon {
  font-size:28px;
  margin-bottom:17px;
}

.tone-card h3 {
  font-size:18px;
  margin-bottom:9px;
}

.tone-card p {
  font-size:12px;
  color:#A09590;
  line-height:1.8;
}

.swatches {
  display:flex;
  gap:7px;
  margin-top:20px;
}

.swatches span {
  width:26px;
  height:26px;
  border-radius:50%;
}

.tone-result {
  margin-top:35px;
  padding:30px;
  background:#F1E9E5;
}

.tone-result h3 {
  font-size:19px;
  margin-bottom:10px;
}

.tone-result p {
  font-size:13px;
  color:#82746E;
  line-height:1.9;
}

/* MAGAZINE */

.magazine {
  background:#EDE5E0;
}

.mag-cover {
  display:grid;
  grid-template-columns:1fr 1fr;
  background:#F8F4F0;
  min-height:470px;
  overflow:hidden;
}

.mag-cover-img {
  background:
    url('https://koreanskincare.nl/cdn/shop/files/SPRINGFEVER_FAMILY1.jpg?v=1734607333')
    center/cover;
  min-height:450px;
}

.mag-cover-text {
  padding:55px 12%;
  display:flex;
  flex-direction:column;
  justify-content:center;
}

.mag-cover-text .issue {
  font-size:11px;
  letter-spacing:3px;
  color:var(--rose);
}

.mag-cover-text h2 {
  font-family:'DM Serif Display',serif;
  font-size:53px;
  font-weight:400;
  line-height:1.1;
  margin:22px 0;
  color:#715B5D;
}

.mag-cover-text p {
  font-size:13px;
  color:#877B76;
  line-height:2;
}

.mag-cover-text .read {
  margin-top:24px;
  font-size:11px;
  letter-spacing:2px;
  color:#A77E83;
}

/* MAGAZINE ARTICLES */

.article-grid {
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:20px;
  margin-top:30px;
}

.article {
  background:white;
}

.article-img {
  height:210px;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:65px;
}

.article-body {
  padding:25px;
}

.article-body small {
  font-size:10px;
  letter-spacing:2px;
  color:var(--rose);
}

.article-body h3 {
  font-size:18px;
  margin:12px 0;
}

.article-body p {
  font-size:12px;
  color:#928681;
  line-height:1.9;
}

/* SEASON */

.season-section {
  background:white;
}

.season-tabs {
  display:flex;
  justify-content:center;
  gap:10px;
  flex-wrap:wrap;
  margin-bottom:30px;
}

.season-tabs button {
  background:white;
  border:1px solid var(--line);
  padding:12px 25px;
  border-radius:30px;
  color:#776A65;
  cursor:pointer;
  font-size:12px;
}

.season-tabs button.active,
.season-tabs button:hover {
  background:#8D737F;
  border-color:#8D737F;
  color:white;
}

.season-display {
  display:grid;
  grid-template-columns:1fr 1fr;
  background:#F5EFEC;
  min-height:360px;
}

.season-art {
  display:flex;
  align-items:center;
  justify-content:center;
  flex-direction:column;
  padding:40px;
  background:#EADDD7;
}

.season-art .emoji {
  font-size:85px;
}

.season-art h3 {
  font-family:'DM Serif Display',serif;
  font-size:34px;
  margin-top:15px;
  color:#765B60;
}

.season-info {
  padding:45px;
  display:flex;
  flex-direction:column;
  justify-content:center;
}

.season-info .label {
  font-size:10px;
  letter-spacing:3px;
  color:var(--rose);
}

.season-info h3 {
  font-size:27px;
  margin:16px 0;
}

.season-info p {
  font-size:13px;
  line-height:2;
  color:#877B76;
}

.season-palette {
  display:flex;
  gap:10px;
  margin-top:25px;
  flex-wrap:wrap;
}

.palette-item {
  font-size:10px;
  text-align:center;
  color:#877B76;
}

.palette-item span {
  display:block;
  width:36px;
  height:36px;
  border-radius:50%;
  margin-bottom:7px;
}

/* RANKING */

.ranking {
  background:#F7F2EF;
}

.rank-tabs {
  display:flex;
  justify-content:center;
  gap:12px;
  margin-bottom:38px;
  flex-wrap:wrap;
}

.rank-tabs button {
  padding:12px 26px;
  border:1px solid #E3D8D3;
  background:white;
  cursor:pointer;
  color:#776A65;
  font-size:12px;
}

.rank-tabs button.active {
  background:#8D737F;
  color:white;
  border-color:#8D737F;
}

.rank-grid {
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:22px;
}

.rank-card {
  background:white;
  position:relative;
  transition:.3s;
}

.rank-card:hover {
  transform:translateY(-5px);
}

.rank-number {
  position:absolute;
  top:15px;
  left:15px;
  z-index:2;
  background:#75635D;
  color:white;
  width:35px;
  height:35px;
  display:flex;
  align-items:center;
  justify-content:center;
  font-family:'DM Serif Display',serif;
  font-size:17px;
}

.rank-image {
  height:250px;
  background:#F4EEEA;
  overflow:hidden;
  display:flex;
  justify-content:center;
  align-items:center;
}

.rank-image img {
  width:100%;
  height:100%;
  object-fit:contain;
  mix-blend-mode:multiply;
  transition:.4s;
}

.rank-card:hover .rank-image img {
  transform:scale(1.04);
}

.rank-info {
  padding:23px;
}

.rank-info .category {
  font-size:10px;
  color:var(--rose);
  letter-spacing:2px;
}

.rank-info h3 {
  font-size:16px;
  margin:10px 0;
  line-height:1.5;
}

.rank-info .shade {
  font-size:12px;
  color:#9B817D;
  margin-bottom:12px;
}

.rank-info p {
  font-size:11px;
  color:#978C87;
  line-height:1.8;
}

.rank-note {
  text-align:center;
  font-size:11px;
  color:#968984;
  line-height:1.9;
  margin-top:30px;
}

/* PRODUCT PICK */

.product-pick {
  background:white;
}

.product-search {
  width:min(420px,100%);
  display:block;
  margin:0 auto 30px;
  border:1px solid var(--line);
  border-radius:30px;
  padding:14px 20px;
  outline:none;
  font-size:13px;
}

.product-filter {
  display:flex;
  justify-content:center;
  flex-wrap:wrap;
  gap:9px;
  margin-bottom:35px;
}

.product-filter button {
  border:1px solid var(--line);
  padding:10px 18px;
  background:white;
  cursor:pointer;
  font-size:12px;
  color:#796D68;
}

.product-filter button.active {
  background:#B88D91;
  color:white;
}

.product-grid {
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:20px;
}

.product-card {
  border:1px solid var(--line);
  background:white;
}

.product-photo {
  height:235px;
  background:#F6F1EE;
  overflow:hidden;
}

.product-photo img {
  width:100%;
  height:100%;
  object-fit:contain;
  mix-blend-mode:multiply;
}

.product-details {
  padding:22px;
}

.product-details .brand {
  font-size:10px;
  color:var(--rose);
  letter-spacing:2px;
}

.product-details h3 {
  font-size:16px;
  margin:10px 0;
}

.product-details .shade {
  font-size:12px;
  color:#927A75;
}

.product-details p {
  font-size:11px;
  line-height:1.8;
  color:#9A8F89;
  margin-top:12px;
}

/* FOOTER */

footer {
  background:#75635D;
  color:#F5EDE8;
  text-align:center;
  padding:55px 20px;
}

.footer-logo {
  font-family:'DM Serif Display',serif;
  font-size:34px;
  letter-spacing:4px;
  margin-bottom:12px;
}

footer p {
  font-size:11px;
  color:#D4C6C0;
  line-height:2;
}

/* RESPONSIVE */

@media(max-width:800px) {
  header {padding:0 5%;}

  .menu-btn {display:block;}

  nav {
    display:none;
    position:absolute;
    top:76px;
    left:0;
    width:100%;
    background:var(--bg);
    padding:25px;
    flex-direction:column;
    gap:20px;
    border-bottom:1px solid var(--line);
  }

  nav.open {display:flex;}

  .hero {grid-template-columns:1fr;}

  .hero-text {padding:75px 9%;}

  .hero-text h1 {font-size:60px;}

  .hero-photo {min-height:350px;}

  .section {padding:70px 6%;}

  .tone-grid {grid-template-columns:repeat(2,1fr);}

  .mag-cover {grid-template-columns:1fr;}

  .mag-cover-img {min-height:300px;}

  .mag-cover-text {padding:40px 9%;}

  .mag-cover-text h2 {font-size:43px;}

  .article-grid {grid-template-columns:1fr;}

  .season-display {grid-template-columns:1fr;}

  .season-art {min-height:250px;}

  .rank-grid,.product-grid {grid-template-columns:repeat(2,1fr);}
}

@media(max-width:500px) {
  .hero-text h1 {font-size:49px;}

  .tone-grid {grid-template-columns:1fr 1fr;}

  .rank-grid,.product-grid {grid-template-columns:1fr;}

  .section-heading h2 {font-size:31px;}

  .rank-image {height:270px;}
}
</style>
</head>

<body>

<!-- HEADER -->

<header>
  <a href="#home" class="logo">
    MUTE ME
    <small>YOUR COLOR, YOUR MOOD</small>
  </a>

  <button class="menu-btn" onclick="toggleMenu()">☰</button>

  <nav id="nav">
    <a href="#home" onclick="closeMenu()">HOME</a>
    <a href="#personal" onclick="closeMenu()">COLOR</a>
    <a href="#magazine" onclick="closeMenu()">MAGAZINE</a>
    <a href="#ranking" onclick="closeMenu()">RANKING</a>
    <a href="#products" onclick="closeMenu()">PRODUCT</a>
  </nav>
</header>

<!-- HOME -->

<section class="hero" id="home">
  <div class="hero-text">
    <div class="mini">MUTE ME BEAUTY JOURNAL · 2026</div>

    <h1>
      Find Your<br>
      <span>Muted</span><br>
      Mood.
    </h1>

    <p>
      나에게 어울리는 컬러를 발견하는 시간.<br>
      퍼스널 컬러부터 최신 뷰티 트렌드까지<br>
      MUTE ME에서 나만의 아름다움을 찾아보세요.
    </p>

    <a href="#magazine" class="hero-btn">
      EXPLORE THE MAGAZINE →
    </a>
  </div>

  <div class="hero-photo"></div>
</section>

<div class="trend-bar">
  MUTE ME EDITOR'S PICK &nbsp; | &nbsp;
  <span>2026 AUTUMN : MUTE & NEUTRAL MOOD</span>
</div>

<!-- PERSONAL COLOR -->

<section class="section" id="personal">
  <div class="inner">
    <div class="section-heading">
      <div class="eyebrow">FIND YOUR COLOR</div>
      <h2>Personal Color</h2>
      <p>
        나의 분위기와 어울리는 컬러를 찾아보세요.<br>
        원하는 톤을 선택하면 어울리는 실제 화장품을 추천해 드려요.
      </p>
    </div>

    <div class="tone-grid" id="toneGrid"></div>

    <div class="tone-result" id="toneResult">
      <h3>나만의 컬러를 선택해 보세요 ♡</h3>
      <p>퍼스널 컬러를 선택하면 제품 추천이 나타납니다.</p>
    </div>
  </div>
</section>

<!-- MAGAZINE -->

<section class="section magazine" id="magazine">
  <div class="inner">
    <div class="section-heading">
      <div class="eyebrow">MUTE ME EDITORIAL</div>
      <h2>Beauty Magazine</h2>
      <p>
        이번 시즌의 컬러, 분위기, 메이크업을<br>
        매거진처럼 만나보세요.
      </p>
    </div>

    <div class="mag-cover">
      <div class="mag-cover-img"></div>

      <div class="mag-cover-text">
        <div class="issue">ISSUE NO. 01 · NOVEMBER 2026</div>

        <h2>
          The Art of<br>
          Muted Beauty
        </h2>

        <p>
          선명한 컬러보다 은은하게 스며드는 색감.<br>
          말린 장미, 모브 브라운, 로즈 베이지.<br>
          올가을은 뮤트와 뉴트럴 컬러로<br>
          나만의 분위기를 완성해 보세요.
        </p>

        <div class="read">MUTE ME EDITORIAL</div>
      </div>
    </div>

    <div class="article-grid">

      <article class="article">
        <div class="article-img" style="background:#E7D5D0">
          🌹
        </div>
        <div class="article-body">
          <small>COLOR STORY 01</small>
          <h3>가을 뮤트의 매력</h3>
          <p>
            채도를 낮춘 말린 장미와 모브 계열.
            부드럽고 차분한 색감으로 자연스러운 분위기를 만들어 보세요.
          </p>
        </div>
      </article>

      <article class="article">
        <div class="article-img" style="background:#E9DDD1">
          🤎
        </div>
        <div class="article-body">
          <small>COLOR STORY 02</small>
          <h3>뉴트럴 컬러의 발견</h3>
          <p>
            웜과 쿨의 경계를 넘나드는 로즈 베이지와 토프.
            다양한 피부 톤에 맞춰 활용하기 좋은 컬러예요.
          </p>
        </div>
      </article>

      <article class="article">
        <div class="article-img" style="background:#DED7DB">
          ☁️
        </div>
        <div class="article-body">
          <small>MAKEUP STORY 03</small>
          <h3>소프트 블러 메이크업</h3>
          <p>
            경계를 부드럽게 풀어낸 블러 립과 은은한 치크.
            자연스러운 피부 표현과 조화를 이루는 메이크업이에요.
          </p>
        </div>
      </article>

    </div>
  </div>
</section>

<!-- SEASONAL TREND -->

<section class="section season-section" id="season">
  <div class="inner">
    <div class="section-heading">
      <div class="eyebrow">SEASONAL COLOR REPORT</div>
      <h2>Season Trend</h2>
      <p>계절을 선택하고 시즌별 추천 컬러를 확인해 보세요.</p>
    </div>

    <div class="season-tabs">
      <button class="active" onclick="changeSeason('autumn',this)">🍂 AUTUMN</button>
      <button onclick="changeSeason('winter',this)">❄️ WINTER</button>
      <button onclick="changeSeason('spring',this)">🌷 SPRING</button>
      <button onclick="changeSeason('summer',this)">☀️ SUMMER</button>
    </div>

    <div class="season-display">
      <div class="season-art" id="seasonArt">
        <div class="emoji">🍂</div>
        <h3>AUTUMN MOOD</h3>
      </div>

      <div class="season-info">
        <div class="label" id="seasonLabel">2026 AUTUMN EDITION</div>
        <h3 id="seasonTitle">가을 뮤트 & 뉴트럴</h3>
        <p id="seasonDesc">
          차분한 로즈와 모브, 그레이지 컬러가 중심이 되는 계절.
          부드러운 음영과 자연스러운 혈색으로 분위기를 완성해 보세요.
        </p>

        <div class="season-palette" id="seasonPalette"></div>
      </div>
    </div>
  </div>
</section>

<!-- RANKING -->

<section class="section ranking" id="ranking">
  <div class="inner">
    <div class="section-heading">
      <div class="eyebrow">HOT BEAUTY PRODUCTS</div>
      <h2>Beauty Ranking</h2>
      <p>
        지금 주목받는 뷰티 제품을 확인해 보세요.<br>
        제품의 브랜드와 색상 번호까지 한눈에!
      </p>
    </div>

    <div class="rank-tabs">
      <button class="active" onclick="showRanking('lip',this)">LIP RANKING</button>
      <button onclick="showRanking('cheek',this)">CHEEK RANKING</button>
      <button onclick="showRanking('pact',this)">PACT RANKING</button>
    </div>

    <div class="rank-grid" id="rankGrid"></div>

    <div class="rank-note" id="rankNote"></div>
  </div>
</section>

<!-- PRODUCT PICK -->

<section class="section product-pick" id="products">
  <div class="inner">
    <div class="section-heading">
      <div class="eyebrow">CURATED FOR YOUR COLOR</div>
      <h2>Product Pick</h2>
      <p>
        퍼스널 컬러별 실제 화장품 추천.<br>
        브랜드와 제품 호수를 확인하고 나에게 맞는 컬러를 찾아보세요.
      </p>
    </div>

    <input
      type="text"
      class="product-search"
      id="productSearch"
      placeholder="🔍 브랜드, 제품명, 컬러 검색"
    >

    <div class="product-filter" id="productFilters">
      <button class="active" onclick="filterProducts('전체',this)">전체</button>
      <button onclick="filterProducts('봄웜톤',this)">봄웜</button>
      <button onclick="filterProducts('여름쿨톤',this)">여름쿨</button>
      <button onclick="filterProducts('가을웜톤',this)">가을웜</button>
      <button onclick="filterProducts('겨울쿨톤',this)">겨울쿨</button>
      <button onclick="filterProducts('뉴트럴톤',this)">뉴트럴</button>
      <button onclick="filterProducts('뮤트톤',this)">뮤트</button>
    </div>

    <div class="product-grid" id="productGrid"></div>
  </div>
</section>

<!-- FOOTER -->

<footer>
  <div class="footer-logo">MUTE ME</div>
  <p>
    YOUR COLOR, YOUR MOOD.<br>
    Find your color. Discover your beauty.<br><br>
    MUTE ME BEAUTY JOURNAL © 2026
  </p>
</footer>

<script>

// 이미지 주소

const images = {
  romand:
  "https://jbeauty.fi/cdn/shop/collections/Romand-Hanbok_1.jpg?v=1726837387",

  etude:
  "https://kozmetikumbolt.cdn.shoprenter.hu/custom/kozmetikumbolt/image/data/ETUDE/etude-house-fixing-tint-05-midnight-mauve-koreashop.webp?lastmod=1720647745.1703838527",

  vdl:
  "https://cloudflare.lipscosme.com/image/d449b6c3b758ac06ce434b31-1715403442.png?auto=avif%2Cwebp&fio=1&orient=1&width=430",

  lily:
  "https://merryseasons.com.au/cdn/shop/files/01_54c2f855-516e-4f60-aef0-0e48015508b4_1024x1024.jpg?v=1777191533",

  peripera:
  "https://cdn.hstatic.net/products/200000977139/m__h_ng_peripera_pure_blushed_sunshine_cheek__24_mauve_cream__1__a1e3635e2c424b1b826df7928312a58a_master.png",

  ipkn:
  "https://images-cdn.ubuy.co.in/675a97298ed2d27a25620741-ipkn-personal-tone-correcting-blur-pact.jpg",

  abouttone:
  "https://thumbnail8.coupangcdn.com/thumbnails/remote/492x492ex/image/vendor_inventory/c6f6/120be2a06d78bcce3446641de86826865d3d9213e8cc676282a2ff5af475.png",

  innisfree:
  "https://cdn.makeupshop.ro/imagini-makeup/produse/original/no-sebum-mineral-pact-4-5zpzlun0.jpg"
};

// 퍼스널 컬러 데이터

const tones = [
  {
    name:"봄웜톤",
    icon:"🌷",
    desc:"화사하고 생기 있는 피치 & 코랄",
    colors:["#F3B69D","#EFA18C","#E8C99D"],
    text:"따뜻하고 밝은 컬러가 특징이에요. 피치, 코랄, 살구 계열의 립과 블러셔로 생기 있는 메이크업을 완성해 보세요."
  },
  {
    name:"여름쿨톤",
    icon:"🫧",
    desc:"맑고 부드러운 핑크 & 라벤더",
    colors:["#D8B8CD","#BBA7C8","#C5D2E1"],
    text:"차분하고 부드러운 쿨 컬러가 잘 어울려요. 로즈 핑크, 모브, 라벤더로 맑고 은은한 분위기를 연출해 보세요."
  },
  {
    name:"가을웜톤",
    icon:"🍁",
    desc:"깊고 따뜻한 브라운 & 브릭",
    colors:["#A86F50","#C18C67","#8D604A"],
    text:"깊이감 있는 웜 컬러가 특징이에요. 브릭, 칠리, 테라코타, 브라운 계열을 활용해 분위기 있는 메이크업을 연출해 보세요."
  },
  {
    name:"겨울쿨톤",
    icon:"❄️",
    desc:"선명하고 깊은 베리 & 플럼",
    colors:["#A43D63","#775B87","#D0B5D7"],
    text:"선명하고 대비감 있는 쿨 컬러가 특징이에요. 베리, 플럼, 와인 계열로 또렷한 포인트 메이크업을 연출해 보세요."
  },
  {
    name:"뉴트럴톤",
    icon:"🤍",
    desc:"웜과 쿨의 균형, 로즈 & 베이지",
    colors:["#C49A8F","#B7A196","#D6BDAE"],
    text:"웜과 쿨의 성향이 균형을 이루는 컬러예요. 로즈 베이지, 토프, 누드 계열로 자연스럽게 연출해 보세요."
  },
  {
    name:"뮤트톤",
    icon:"☁️",
    desc:"부드럽고 차분한 저채도 컬러",
    colors:["#B58E91","#A49496","#C5ADA1"],
    text:"채도가 낮고 부드러운 색감이 특징이에요. 말린 장미, 모브 브라운, 더스티 핑크로 은은한 분위기를 완성해 보세요."
  }
];

// 퍼스널 컬러별 제품 추천

const products = [
  {
    tone:"봄웜톤",brand:"VDL",
    name:"치크스테인 블러셔",
    shade:"01 Bouncing Peach",
    type:"치크",
    img:images.vdl,
    desc:"맑은 피치 컬러로 화사한 혈색 표현"
  },
  {
    tone:"봄웜톤",brand:"rom&nd",
    name:"더 쥬시 래스팅 틴트",
    shade:"23 Peach Peach Me",
    type:"립",
    img:images.romand,
    desc:"밝고 따뜻한 피치 계열 추천"
  },
  {
    tone:"여름쿨톤",brand:"ETUDE",
    name:"픽싱 틴트",
    shade:"05 Midnight Mauve",
    type:"립",
    img:images.etude,
    desc:"차분한 모브 핑크 계열"
  },
  {
    tone:"여름쿨톤",brand:"peripera",
    name:"맑게 물든 선샤인 치크",
    shade:"024 Mauve Cream",
    type:"치크",
    img:images.peripera,
    desc:"부드러운 모브 컬러"
  },
  {
    tone:"가을웜톤",brand:"ETUDE",
    name:"픽싱 틴트",
    shade:"04 Ginger Milk Tea",
    type:"립",
    img:images.etude,
    desc:"밀크티 베이지 브라운 계열"
  },
  {
    tone:"가을웜톤",brand:"VDL",
    name:"치크스테인 블러셔",
    shade:"01 Bouncing Peach",
    type:"치크",
    img:images.vdl,
    desc:"부드러운 피치 베이지"
  },
  {
    tone:"겨울쿨톤",brand:"rom&nd",
    name:"더 쥬시 래스팅 틴트",
    shade:"03 Bare Grape",
    type:"립",
    img:images.romand,
    desc:"차분한 쿨 로즈 계열"
  },
  {
    tone:"겨울쿨톤",brand:"peripera",
    name:"맑게 물든 선샤인 치크",
    shade:"024 Mauve Cream",
    type:"치크",
    img:images.peripera,
    desc:"쿨한 모브 핑크 계열"
  },
  {
    tone:"뉴트럴톤",brand:"ETUDE",
    name:"픽싱 틴트",
    shade:"01 Analog Rose",
    type:"립",
    img:images.etude,
    desc:"균형 잡힌 로즈 컬러"
  },
  {
    tone:"뉴트럴톤",brand:"lilybyred",
    name:"러브빔 치크밤",
    shade:"06 Fluffy Peach",
    type:"치크",
    img:images.lily,
    desc:"자연스러운 피치 컬러"
  },
  {
    tone:"뮤트톤",brand:"ETUDE",
    name:"픽싱 틴트",
    shade:"05 Midnight Mauve",
    type:"립",
    img:images.etude,
    desc:"그레이시 모브 핑크"
  },
  {
    tone:"뮤트톤",brand:"peripera",
    name:"맑게 물든 선샤인 치크",
    shade:"024 Mauve Cream",
    type:"치크",
    img:images.peripera,
    desc:"채도를 낮춘 말린 장미빛"
  },
  {
    tone:"뮤트톤",brand:"ABOUT_TONE",
    name:"블러 파우더 팩트",
    shade:"01 Fair",
    type:"팩트",
    img:images.abouttone,
    desc:"부드러운 블러 피부 표현"
  }
];

// 계절별 트렌드

const seasons = {
  autumn:{
    emoji:"🍂",
    name:"AUTUMN MOOD",
    bg:"#EADDD2",
    title:"가을 뮤트 & 뉴트럴",
    desc:"말린 장미, 모브 브라운, 로즈 베이지, 그레이지. 차분한 저채도 컬러를 중심으로 부드러운 음영 메이크업을 연출해 보세요.",
    colors:[
      ["말린 장미","#B58388"],
      ["모브","#A58B96"],
      ["로즈 베이지","#C49B91"],
      ["그레이지","#A99B91"],
      ["브라운","#927264"]
    ]
  },
  winter:{
    emoji:"❄️",
    name:"WINTER MOOD",
    bg:"#E4E1EA",
    title:"겨울쿨 & 딥 뉴트럴",
    desc:"베리, 플럼, 딥 로즈, 차콜 등 깊이감 있는 색상이 포인트예요. 선명한 립과 부드러운 피부 표현을 조합해 보세요.",
    colors:[
      ["베리","#A33B5F"],
      ["플럼","#795E88"],
      ["딥 로즈","#A66D80"],
      ["차콜","#69636D"]
    ]
  },
  spring:{
    emoji:"🌷",
    name:"SPRING MOOD",
    bg:"#F5E5DF",
    title:"봄웜 & 소프트 뉴트럴",
    desc:"피치, 코랄, 살구, 크림 베이지 등 따뜻하고 밝은 컬러로 화사하고 생기 있는 메이크업을 연출해 보세요.",
    colors:[
      ["피치","#F2B39D"],
      ["코랄","#E88D79"],
      ["크림","#EBD5B8"],
      ["살구","#E6AC85"]
    ]
  },
  summer:{
    emoji:"☀️",
    name:"SUMMER MOOD",
    bg:"#E6EAF1",
    title:"여름쿨 & 라이트 뮤트",
    desc:"라벤더, 소프트 핑크, 모브, 스카이 블루 등 시원하고 부드러운 컬러를 활용해 투명한 분위기를 완성해 보세요.",
    colors:[
      ["라벤더","#C7B6D9"],
      ["핑크","#E4BBCB"],
      ["모브","#AB91A8"],
      ["블루","#B7CADB"]
    ]
  }
};

// 랭킹 데이터

const rankings = {
  lip:[
    {
      rank:"01",
      brand:"ETUDE",
      name:"Fixing Tint",
      shade:"#05 Midnight Mauve",
      img:images.etude,
      desc:"차분한 모브 컬러의 픽싱 틴트. 4g"
    },
    {
      rank:"02",
      brand:"MIAEL",
      name:"Light Veil Tint",
      shade:"Spring Light Warm-tone",
      img:images.romand,
      desc:"가벼운 베일 느낌의 웜톤 틴트"
    },
    {
      rank:"03",
      brand:"rom&nd",
      name:"The Juicy Lasting Tint",
      shade:"#03 Bare Grape",
      img:images.romand,
      desc:"촉촉한 광택감의 쿨 로즈 계열 틴트. 3.5g"
    }
  ],

  cheek:[
    {
      rank:"01",
      brand:"VDL",
      name:"Cheek Stain Blusher",
      shade:"#01 Bouncing Peach",
      img:images.vdl,
      desc:"부드러운 피치 계열 파우더 치크. 6g"
    },
    {
      rank:"02",
      brand:"lilybyred",
      name:"Luvbeam Cheek Balm",
      shade:"#06 Fluffy Peach",
      img:images.lily,
      desc:"사랑스러운 피치 컬러의 치크밤. 3.5g"
    },
    {
      rank:"03",
      brand:"peripera",
      name:"Pure Blushed Sunshine Cheek",
      shade:"#024 Mauve Cream",
      img:images.peripera,
      desc:"차분한 모브 컬러의 파우더 블러셔. 4.2g"
    }
  ],

  pact:[
    {
      rank:"01",
      brand:"IPKN&",
      name:"Personal Tone Correcting Blur Pact",
      shade:"Lavender · 5.5g",
      img:images.ipkn,
      desc:"전체 파우더·컴팩트 순위 5위. 라벤더 컬러 팩트"
    },
    {
      rank:"02",
      brand:"ABOUT_TONE",
      name:"Blur Powder Pact",
      shade:"01 Fair · 9g",
      img:images.abouttone,
      desc:"전체 파우더·컴팩트 순위 7위. 블러 파우더 팩트"
    },
    {
      rank:"03",
      brand:"innisfree",
      name:"No-Sebum Mineral Pact",
      shade:"8.5g",
      img:images.innisfree,
      desc:"전체 파우더·컴팩트 순위 9위. 노세범 컴팩트"
    }
  ]
};

// 메뉴

function toggleMenu(){
  document.getElementById("nav").classList.toggle("open");
}

function closeMenu(){
  document.getElementById("nav").classList.remove("open");
}

// 톤 카드

const toneGrid=document.getElementById("toneGrid");
const toneResult=document.getElementById("toneResult");

toneGrid.innerHTML=tones.map((t,i)=>`
  <div class="tone-card" onclick="selectTone(${i})">
    <div class="tone-icon">${t.icon}</div>
    <h3>${t.name}</h3>
    <p>${t.desc}</p>
    <div class="swatches">
      ${t.colors.map(c=>`<span style="background:${c}"></span>`).join("")}
    </div>
  </div>
`).join("");

function selectTone(i){
  const t=tones[i];

  document.querySelectorAll(".tone-card").forEach((card,index)=>{
    card.classList.toggle("active",index===i);
  });

  toneResult.innerHTML=`
    <h3>${t.icon} ${t.name} COLOR GUIDE</h3>
    <p>${t.text}</p>
    <br>
    <button onclick="filterProducts('${t.name}',document.querySelectorAll('#productFilters button')[${i+1}])"
      style="border:0;background:#8D737F;color:white;padding:12px 22px;cursor:pointer">
      ${t.name} 제품 보러가기 →
    </button>
  `;
}

// 계절 변경

function changeSeason(key,btn){
  const s=seasons[key];

  document.querySelectorAll(".season-tabs button").forEach(b=>{
    b.classList.remove("active");
  });

  btn.classList.add("active");

  document.getElementById("seasonArt").style.background=s.bg;
  document.getElementById("seasonArt").innerHTML=`
    <div class="emoji">${s.emoji}</div>
    <h3>${s.name}</h3>
  `;

  document.getElementById("seasonLabel").textContent=key.toUpperCase()+" SEASONAL COLOR";
  document.getElementById("seasonTitle").textContent=s.title;
  document.getElementById("seasonDesc").textContent=s.desc;

  document.getElementById("seasonPalette").innerHTML=
    s.colors.map(c=>`
      <div class="palette-item">
        <span style="background:${c[1]}"></span>
        ${c[0]}
      </div>
    `).join("");
}

// 랭킹 출력

function showRanking(key,btn){
  document.querySelectorAll(".rank-tabs button").forEach(b=>{
    b.classList.remove("active");
  });

  btn.classList.add("active");

  const list=rankings[key];

  document.getElementById("rankGrid").innerHTML=list.map(item=>`
    <div class="rank-card">
      <div class="rank-number">${item.rank}</div>
      <div class="rank-image">
        <img src="${item.img}" alt="${item.brand} ${item.name}"
          onerror="this.style.display='none';this.parentElement.innerHTML='<span style=font-size:65px>💄</span>'">
      </div>
      <div class="rank-info">
        <div class="category">${key.toUpperCase()} · RANKING</div>
        <h3>${item.brand} ${item.name}</h3>
        <div class="shade">${item.shade}</div>
        <p>${item.desc}</p>
      </div>
    </div>
  `).join("");

  const notes={
    lip:"출처: 화해 트렌딩 립 스테인 순위 · 2026.11.17 업데이트 · 상위 3개 제품",
    cheek:"출처: 화해 트렌딩 블러셔 순위 · 2026.11.17 업데이트 · 상위 3개 제품",
    pact:"출처: 화해 트렌딩 파우더·컴팩트 순위 · 2026.11.18 업데이트 · 팩트형 제품의 원 순위 5·7·9위"
  };

  document.getElementById("rankNote").textContent=
    notes[key]+" | 플랫폼과 집계 기간에 따라 순위는 달라질 수 있습니다.";
}

// 제품 추천

let currentFilter="전체";

function renderProducts(){
  const keyword=document.getElementById("productSearch").value.toLowerCase();

  const filtered=products.filter(p=>{
    const matchTone=currentFilter==="전체"||p.tone===currentFilter;
    const matchText=(p.brand+p.name+p.shade+p.tone+p.type).toLowerCase().includes(keyword);
    return matchTone&&matchText;
  });

  document.getElementById("productGrid").innerHTML=
    filtered.length ? filtered.map(p=>`
      <div class="product-card">
        <div class="product-photo">
          <img src="${p.img}" alt="${p.brand} ${p.name} ${p.shade}"
            onerror="this.style.display='none';this.parentElement.innerHTML='<span style=font-size:65px;display:grid;place-items:center;height:100%>💗</span>'">
        </div>
        <div class="product-details">
          <div class="brand">${p.brand} · ${p.tone}</div>
          <h3>${p.name}</h3>
          <div class="shade">${p.shade}</div>
          <p>${p.desc}</p>
        </div>
      </div>
    `).join("") :
    "<p style='grid-column:1/-1;text-align:center;padding:40px'>검색 결과가 없습니다.</p>";
}

function filterProducts(tone,btn){
  currentFilter=tone;

  document.querySelectorAll("#productFilters button").forEach(b=>{
    b.classList.remove("active");
  });

  btn.classList.add("active");
  document.getElementById("productSearch").value="";

  renderProducts();

  document.getElementById("products").scrollIntoView({behavior:"smooth"});
}

document.getElementById("productSearch").addEventListener("input",renderProducts);

// 초기 화면

changeSeason("autumn",document.querySelector(".season-tabs button"));
showRanking("lip",document.querySelector(".rank-tabs button"));
renderProducts();

</script>

</body>
</html>
