
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>YOUR COLOR - 퍼스널 컬러 뷰티 큐레이션</title>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html { scroll-behavior: smooth; }

body {
  font-family: 'Pretendard', 'Arial', sans-serif;
  background: #fffaf8;
  color: #514b4a;
}

header {
  background: white;
  padding: 20px 7%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: sticky;
  top: 0;
  z-index: 100;
  box-shadow: 0 2px 12px #00000008;
}

.logo {
  font-size: 24px;
  font-weight: 900;
  color: #c58e98;
  letter-spacing: 2px;
}

nav {
  display: flex;
  gap: 23px;
}

nav a {
  text-decoration: none;
  color: #625b59;
  font-size: 13px;
}

nav a:hover { color: #c58e98; }

/* 메인 화면 */

.hero {
  text-align: center;
  padding: 105px 20px;
  background: linear-gradient(135deg, #f7e9e8, #e9f0e9);
}

.hero .sub {
  color: #ad8288;
  letter-spacing: 4px;
  font-size: 12px;
  margin-bottom: 22px;
}

.hero h1 {
  font-size: 43px;
  color: #65565a;
  margin-bottom: 18px;
}

.hero h1 span { color: #c58e98; }

.hero p {
  font-size: 15px;
  color: #807675;
  line-height: 1.9;
}

.main-button {
  display: inline-block;
  margin-top: 30px;
  padding: 13px 27px;
  background: #c58e98;
  color: white;
  text-decoration: none;
  border-radius: 30px;
  font-size: 13px;
}

/* 공통 */

.container {
  max-width: 1150px;
  margin: auto;
  padding: 75px 20px;
}

.section-title {
  text-align: center;
  margin-bottom: 38px;
}

.section-title h2 {
  font-size: 27px;
  margin-bottom: 12px;
  letter-spacing: 1px;
}

.section-title p {
  color: #a49a98;
  font-size: 14px;
  line-height: 1.7;
}

/* 퍼스널 컬러 */

.tone-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(145px, 1fr));
  gap: 15px;
}

.tone-card {
  background: white;
  border: 1px solid #f1e5e2;
  padding: 22px 10px;
  text-align: center;
  border-radius: 18px;
  cursor: pointer;
  transition: .25s;
}

.tone-card:hover,
.tone-card.active {
  border-color: #c58e98;
  background: #fff0f2;
  transform: translateY(-4px);
}

.tone-card .emoji {
  font-size: 30px;
  margin-bottom: 12px;
}

.tone-card h3 {
  font-size: 16px;
  margin-bottom: 8px;
}

.tone-card small {
  color: #a49a98;
}

.color-dots {
  display: flex;
  justify-content: center;
  gap: 7px;
  margin-top: 14px;
}

.dot {
  width: 20px;
  height: 20px;
  border-radius: 50%;
}

/* 계절별 트렌드 */

.trend-section {
  background: #f5efeb;
  padding: 75px 20px;
}

.trend-container {
  max-width: 1100px;
  margin: auto;
}

.trend-label {
  text-align: center;
  color: #a67f77;
  font-size: 12px;
  letter-spacing: 3px;
  margin-bottom: 12px;
}

.season-buttons {
  display: flex;
  justify-content: center;
  gap: 12px;
  flex-wrap: wrap;
  margin-bottom: 35px;
}

.season-buttons button {
  padding: 12px 25px;
  background: white;
  border: 1px solid #e7dcd6;
  border-radius: 30px;
  cursor: pointer;
  color: #766c69;
  font-size: 14px;
  transition: .2s;
}

.season-buttons button.active,
.season-buttons button:hover {
  background: #92786f;
  color: white;
  border-color: #92786f;
}

.trend-main {
  display: grid;
  grid-template-columns: 1fr 1fr;
  background: white;
  border-radius: 24px;
  overflow: hidden;
  box-shadow: 0 8px 25px #00000008;
}

.trend-visual {
  min-height: 330px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  gap: 15px;
  padding: 30px;
}

.trend-visual .season-emoji {
  font-size: 85px;
}

.trend-visual h3 {
  font-size: 28px;
  color: #645651;
}

.trend-visual p {
  font-size: 13px;
  color: #827773;
}

.trend-content {
  padding: 45px 35px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.trend-content .badge {
  display: inline-block;
  width: fit-content;
  background: #f5e8e5;
  color: #a77c76;
  padding: 7px 13px;
  border-radius: 20px;
  font-size: 12px;
  margin-bottom: 18px;
}

.trend-content h3 {
  font-size: 27px;
  margin-bottom: 15px;
}

.trend-content > p {
  font-size: 14px;
  line-height: 1.9;
  color: #857b78;
  margin-bottom: 20px;
}

.trend-content h4 {
  font-size: 14px;
  margin-bottom: 12px;
}

.trend-colors {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
}

.trend-color {
  text-align: center;
  font-size: 11px;
  color: #817774;
}

.trend-color span {
  display: block;
  width: 42px;
  height: 42px;
  border-radius: 50%;
  margin-bottom: 7px;
}

.trend-tip {
  background: #fff9f6;
  border-radius: 14px;
  padding: 15px;
  margin-top: 20px;
  font-size: 13px;
  line-height: 1.8;
  color: #927b75;
}

/* 뮤트 & 뉴트럴 */

.popular-section {
  padding: 75px 20px;
  background: white;
}

.popular-container {
  max-width: 1100px;
  margin: auto;
}

.popular-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.popular-card {
  background: #faf5f2;
  border-radius: 18px;
  overflow: hidden;
}

.popular-card .visual {
  height: 155px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 60px;
}

.popular-card .info {
  padding: 23px;
}

.popular-card h3 {
  margin-bottom: 10px;
  font-size: 18px;
}

.popular-card p {
  color: #8d817d;
  font-size: 13px;
  line-height: 1.8;
}

.popular-card .keywords {
  color: #b17e86;
  margin-top: 12px;
  font-size: 12px;
  font-weight: bold;
}

/* 화장품 추천 */

.products {
  background: #f8f3f0;
  padding: 75px 20px;
}

.search {
  display: block;
  width: min(400px, 100%);
  margin: 0 auto 30px;
  padding: 14px 18px;
  border: 1px solid #eadbd8;
  border-radius: 30px;
  outline: none;
}

.filter {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 10px;
  margin-bottom: 35px;
}

.filter button {
  border: 1px solid #eadbd8;
  background: white;
  color: #716563;
  padding: 10px 20px;
  border-radius: 30px;
  cursor: pointer;
}

.filter button.active,
.filter button:hover {
  background: #c58e98;
  color: white;
  border-color: #c58e98;
}

.product-grid {
  max-width: 1150px;
  margin: auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 22px;
}

.product-card {
  background: white;
  border-radius: 18px;
  overflow: hidden;
  transition: .25s;
}

.product-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px #0000000d;
}

.product-image {
  height: 170px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 65px;
}

.product-info {
  padding: 20px;
}

.product-info .tag {
  display: inline-block;
  background: #f9e9eb;
  color: #bd8290;
  font-size: 11px;
  padding: 5px 10px;
  border-radius: 15px;
  margin-bottom: 10px;
}

.product-info h3 {
  font-size: 17px;
  margin-bottom: 8px;
}

.product-info p {
  font-size: 13px;
  color: #9a908e;
  line-height: 1.6;
}

.product-info .color-name {
  margin-top: 12px;
  color: #bd8290;
  font-weight: bold;
  font-size: 13px;
}

/* 안내 */

.guide {
  background: white;
  border-radius: 20px;
  padding: 35px;
  margin-top: 45px;
  text-align: center;
}

.guide h2 { margin-bottom: 15px; }

.guide p {
  line-height: 1.9;
  color: #857b79;
  font-size: 14px;
}

footer {
  text-align: center;
  background: #f2e6e4;
  padding: 35px 15px;
  color: #947f80;
  font-size: 12px;
  line-height: 2;
}

@media(max-width:700px) {
  header {
    padding: 17px;
    flex-direction: column;
    gap: 15px;
  }

  nav {
    gap: 14px;
  }

  nav a { font-size: 12px; }

  .hero h1 { font-size: 30px; }

  .trend-main { grid-template-columns: 1fr; }

  .trend-visual { min-height: 240px; }

  .trend-content { padding: 30px 25px; }

  .popular-grid { grid-template-columns: 1fr; }
}
</style>
</head>

<body>

<header>
  <div class="logo">YOUR COLOR ♡</div>
  <nav>
    <a href="#home">HOME</a>
    <a href="#tone">PERSONAL COLOR</a>
    <a href="#trend">SEASON TREND</a>
    <a href="#products">BEAUTY</a>
  </nav>
</header>

<!-- 메인 -->

<section class="hero" id="home">
  <div class="sub">FIND YOUR OWN BEAUTY</div>
  <h1>당신만의 컬러를 <span>찾아보세요</span></h1>
  <p>
    나에게 어울리는 색상부터 계절별 뷰티 트렌드까지!<br>
    퍼스널 컬러를 통해 나만의 아름다움을 발견해 보세요.
  </p>
  <a href="#tone" class="main-button">나의 컬러 찾기 ♡</a>
</section>

<!-- 퍼스널 컬러 -->

<section class="container" id="tone">
  <div class="section-title">
    <h2>PERSONAL COLOR</h2>
    <p>나의 퍼스널 컬러를 선택해 보세요 ♡</p>
  </div>
  <div class="tone-grid" id="toneGrid"></div>
</section>

<!-- 계절별 트렌드 -->

<section class="trend-section" id="trend">
  <div class="trend-container">
    <div class="section-title">
      <div class="trend-label">SEASONAL BEAUTY TREND</div>
      <h2>계절별 퍼스널 컬러 트렌드</h2>
      <p>계절이 바뀌면 뷰티 트렌드도 달라져요.<br>
      지금 유행하는 컬러와 메이크업을 확인해 보세요.</p>
    </div>

    <div class="season-buttons">
      <button onclick="selectSeason('spring')">🌷 봄</button>
      <button onclick="selectSeason('summer')">☀️ 여름</button>
      <button class="active" onclick="selectSeason('autumn')">🍂 가을</button>
      <button onclick="selectSeason('winter')">❄️ 겨울</button>
    </div>

    <div class="trend-main">
      <div class="trend-visual" id="seasonVisual">
        <div class="season-emoji">🍂</div>
        <h3>AUTUMN MOOD</h3>
        <p>Soft & Muted Colors</p>
      </div>

      <div class="trend-content">
        <span class="badge" id="seasonBadge">CURRENT SEASON · FALL</span>
        <h3 id="seasonTitle">가을 뮤트 트렌드</h3>
        <p id="seasonDesc">
          차분하고 부드러운 색감이 매력적인 가을!
          채도가 낮은 로즈, 모브, 브라운 계열의
          뮤트 컬러가 잘 어울리는 계절이에요.
        </p>

        <h4>COLOR PALETTE</h4>
        <div class="trend-colors" id="seasonColors"></div>

        <div class="trend-tip" id="seasonTip">
          ♡ 추천 메이크업 : 말린 장미 립, 모브 브라운 아이섀도우,
          로즈 베이지 블러셔로 차분하고 분위기 있는 메이크업을 연출해 보세요.
        </div>
      </div>
    </div>
  </div>
</section>

<!-- 뮤트 & 뉴트럴 트렌드 -->

<section class="popular-section">
  <div class="popular-container">
    <div class="section-title">
      <h2>MUTE & NEUTRAL TREND</h2>
      <p>최근 주목받는 뮤트와 뉴트럴 계열의 컬러 스타일</p>
    </div>

    <div class="popular-grid">

      <div class="popular-card">
        <div class="visual" style="background:#e7d5d0">🌹</div>
        <div class="info">
          <h3>가을 뮤트</h3>
          <p>
            부드럽고 차분한 분위기를 연출하는 컬러.
            말린 장미와 로즈 브라운 계열이 대표적이에요.
          </p>
          <div class="keywords">#말린장미 #로즈브라운 #모브</div>
        </div>
      </div>

      <div class="popular-card">
        <div class="visual" style="background:#e7dcd2">🤎</div>
        <div class="info">
          <h3>뉴트럴톤</h3>
          <p>
            웜과 쿨의 균형이 특징인 컬러.
            로즈 베이지와 토프 브라운으로 자연스러운 분위기를 연출해요.
          </p>
          <div class="keywords">#로즈베이지 #토프 #누드</div>
        </div>
      </div>

      <div class="popular-card">
        <div class="visual" style="background:#dcd2d8">☁️</div>
        <div class="info">
          <h3>소프트 뮤트</h3>
          <p>
            선명한 원색보다 채도가 낮고 부드러운 색감.
            은은하고 자연스러운 메이크업에 잘 어울려요.
          </p>
          <div class="keywords">#더스티핑크 #그레이지 #모브</div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- 화장품 추천 -->

<section class="products" id="products">
  <div class="section-title">
    <h2 id="productTitle">RECOMMENDED BEAUTY</h2>
    <p id="productDescription">퍼스널 컬러에 어울리는 화장품을 추천해 드려요.</p>
  </div>

  <input class="search" id="search"
    placeholder="🔍 화장품 이름 또는 색상 검색">

  <div class="filter" id="filters">
    <button class="active" data-type="전체">전체</button>
    <button data-type="립">립</button>
    <button data-type="블러셔">블러셔</button>
    <button data-type="아이섀도우">아이섀도우</button>
    <button data-type="베이스">베이스</button>
  </div>

  <div class="product-grid" id="productGrid"></div>

  <div class="guide">
    <h2>♡ COLOR TIP</h2>
    <p>
      퍼스널 컬러는 화장품을 선택할 때 참고할 수 있는 가이드예요.<br>
      같은 톤이라도 개인의 취향과 피부 표현에 따라 어울리는 색상은 달라질 수 있어요.<br>
      다양한 컬러를 직접 경험하며 나만의 스타일을 찾아보세요!
    </p>
  </div>
</section>

<footer>
  <h2>YOUR COLOR ♡</h2>
  Find your color, Find your beauty.<br>
  퍼스널 컬러 기반 뷰티 큐레이션 홈페이지
</footer>

<script>

// 퍼스널 컬러 데이터

const tones = [
  {
    name:"봄웜톤", emoji:"🌷", desc:"밝고 따뜻한 생기 있는 컬러",
    colors:["#F6B7A5","#F5CE91","#E98F82"],
    products:[
      ["립","코랄 피치 립","맑은 코랄과 피치 계열","#F3A18B","💄"],
      ["블러셔","살구 블러셔","생기 있는 살구빛","#F5B18C","🌸"],
      ["아이섀도우","피치 브라운 팔레트","따뜻한 피치와 골드","#DDA77A","🎨"],
      ["베이스","내추럴 글로우 베이스","자연스러운 윤광 표현","#F3D5BE","✨"]
    ]
  },
  {
    name:"여름쿨톤", emoji:"🫧", desc:"부드럽고 맑은 핑크 계열",
    colors:["#D7B7CF","#B7C7DD","#E6B8C7"],
    products:[
      ["립","로즈 핑크 립","차분한 장미빛 핑크","#CB8CA9","💄"],
      ["블러셔","라벤더 블러셔","은은한 라벤더 핑크","#D5B5D8","🌸"],
      ["아이섀도우","모브 팔레트","부드러운 모브와 회색빛","#B59BAB","🎨"],
      ["베이스","쿨 핑크 베이스","맑은 피부 표현","#E9D6DC","✨"]
    ]
  },
  {
    name:"가을웜톤", emoji:"🍂", desc:"깊고 차분한 어텀 컬러",
    colors:["#B86F4B","#C99565","#9B6548"],
    products:[
      ["립","브릭 레드 립","벽돌빛 레드와 칠리","#A94F39","💄"],
      ["블러셔","누드 베이지 블러셔","차분한 베이지 브라운","#C48C69","🌸"],
      ["아이섀도우","어텀 브라운 팔레트","골드와 딥 브라운","#9C704B","🎨"],
      ["베이스","웜 베이지 베이스","따뜻한 베이지 표현","#D6B18F","✨"]
    ]
  },
  {
    name:"겨울쿨톤", emoji:"❄️", desc:"선명하고 시크한 쿨 컬러",
    colors:["#A52B59","#795A91","#C4A8D8"],
    products:[
      ["립","베리 레드 립","선명한 베리와 플럼","#A52C59","💄"],
      ["블러셔","쿨 핑크 블러셔","또렷한 쿨 핑크","#D77EAA","🌸"],
      ["아이섀도우","플럼 그레이 팔레트","실버와 플럼 계열","#87718F","🎨"],
      ["베이스","쿨 뉴트럴 베이스","맑은 피부 표현","#DCCEDB","✨"]
    ]
  },
  {
    name:"뉴트럴톤", emoji:"🤍", desc:"웜과 쿨의 조화로운 컬러",
    colors:["#C99B92","#B99A83","#D6B6A9"],
    products:[
      ["립","로즈 베이지 립","차분한 로즈 누드","#BB887F","💄"],
      ["블러셔","밀크티 블러셔","자연스러운 로즈 베이지","#CBA398","🌸"],
      ["아이섀도우","토프 브라운 팔레트","균형 잡힌 브라운","#A58E85","🎨"],
      ["베이스","뉴트럴 베이지 베이스","균형 잡힌 베이지 표현","#D8C2B4","✨"]
    ]
  },
  {
    name:"뮤트톤", emoji:"☁️", desc:"채도가 낮은 부드러운 컬러",
    colors:["#B99A99","#A89A9E","#C4AAA0"],
    products:[
      ["립","뮤트 로즈 립","톤 다운된 로즈 컬러","#B58388","💄"],
      ["블러셔","더스티 핑크 블러셔","차분한 말린 장미빛","#C59DA3","🌸"],
      ["아이섀도우","그레이 브라운 팔레트","부드러운 회갈색","#9D8C88","🎨"],
      ["베이스","소프트 베이지 베이스","자연스러운 표현","#D5C2B8","✨"]
    ]
  },
  {
    name:"가을 뮤트", emoji:"🍁", desc:"차분하고 부드러운 가을 컬러",
    colors:["#B58388","#A58B82","#C49B8E"],
    products:[
      ["립","말린 장미 립","로즈 브라운과 더스티 로즈","#A96F76","💄"],
      ["블러셔","로즈 베이지 블러셔","은은한 말린 장미빛","#C39796","🌸"],
      ["아이섀도우","모브 브라운 팔레트","회색빛 모브와 브라운","#927A78","🎨"],
      ["베이스","뮤트 베이지 베이스","차분한 뉴트럴 베이지","#D6BDB0","✨"]
    ]
  }
];

// 계절별 트렌드 데이터

const seasons = {
  spring: {
    emoji:"🌷",
    name:"SPRING MOOD",
    badge:"SPRING BEAUTY TREND",
    title:"봄웜 & 소프트 뉴트럴",
    desc:"따뜻하고 생기 있는 봄에는 피치, 코랄, 크림 베이지 등 맑고 부드러운 색상이 잘 어울려요. 자연스러운 혈색과 화사한 분위기를 표현해 보세요.",
    bg:"#F8E8E2",
    colors:[
      ["피치","#F2B39D"],
      ["코랄","#E88D79"],
      ["크림","#EBD5B8"],
      ["살구","#E6AC85"]
    ],
    tip:"♡ 추천 메이크업 : 피치 코랄 립, 살구 블러셔, 골드 펄 아이섀도우로 생기 있고 화사한 메이크업을 연출해 보세요."
  },

  summer: {
    emoji:"☀️",
    name:"SUMMER MOOD",
    badge:"SUMMER BEAUTY TREND",
    title:"여름쿨 & 라이트 뮤트",
    desc:"시원한 여름에는 라벤더, 소프트 핑크, 모브 등 맑고 차분한 컬러가 잘 어울려요. 투명하고 청량한 분위기를 표현하는 것이 포인트예요.",
    bg:"#E9EDF5",
    colors:[
      ["라벤더","#C7B6D9"],
      ["소프트핑크","#E4BBCB"],
      ["모브","#AB91A8"],
      ["스카이블루","#B7CADB"]
    ],
    tip:"♡ 추천 메이크업 : 라벤더 블러셔, 모브 립, 은은한 핑크 아이섀도우로 시원하고 맑은 메이크업을 완성해 보세요."
  },

  autumn: {
    emoji:"🍂",
    name:"AUTUMN MOOD",
    badge:"CURRENT SEASON · FALL",
    title:"가을 뮤트 & 뉴트럴",
    desc:"차분하고 부드러운 색감이 매력적인 가을! 특히 말린 장미, 모브, 로즈 브라운 등 채도가 낮은 뮤트 계열과 뉴트럴 컬러를 중심으로 분위기 있는 메이크업을 연출해 보세요.",
    bg:"#EDE0D6",
    colors:[
      ["말린장미","#B58388"],
      ["모브","#A58B96"],
      ["로즈베이지","#C49B91"],
      ["그레이지","#A99B91"],
      ["브라운","#927264"]
    ],
    tip:"♡ 추천 메이크업 : 말린 장미 립, 모브 브라운 아이섀도우, 로즈 베이지 블러셔를 활용해 차분하고 분위기 있는 가을 뮤트 메이크업을 완성해 보세요."
  },

  winter: {
    emoji:"❄️",
    name:"WINTER MOOD",
    badge:"WINTER BEAUTY TREND",
    title:"겨울쿨 & 딥 뉴트럴",
    desc:"차가운 겨울에는 베리, 플럼, 딥 로즈 등 깊고 선명한 컬러가 매력적이에요. 차분한 뉴트럴 색상을 함께 활용하면 세련된 분위기를 연출할 수 있어요.",
    bg:"#E5E3EC",
    colors:[
      ["베리","#9F365C"],
      ["플럼","#745B85"],
      ["딥로즈","#A66D80"],
      ["차콜","#69636D"]
    ],
    tip:"♡ 추천 메이크업 : 베리 립, 플럼 아이섀도우, 차분한 로즈 블러셔로 세련되고 또렷한 겨울 메이크업을 연출해 보세요."
  }
};

// 퍼스널 컬러 출력

let selected = 0;
let category = "전체";

const toneGrid = document.getElementById("toneGrid");
const productGrid = document.getElementById("productGrid");

function renderTones() {
  toneGrid.innerHTML = tones.map((tone,i)=>`
    <div class="tone-card ${i===selected?'active':''}"
      onclick="selectTone(${i})">
      <div class="emoji">${tone.emoji}</div>
      <h3>${tone.name}</h3>
      <small>${tone.desc}</small>
      <div class="color-dots">
        ${tone.colors.map(c=>`<span class="dot" style="background:${c}"></span>`).join("")}
      </div>
    </div>
  `).join("");
}

function selectTone(i) {
  selected = i;
  category = "전체";
  document.getElementById("search").value = "";

  document.querySelectorAll("#filters button").forEach(b=>{
    b.classList.toggle("active",b.dataset.type==="전체");
  });

  renderTones();
  renderProducts();
}

// 계절 선택

function selectSeason(key) {
  const season = seasons[key];

  document.querySelectorAll(".season-buttons button").forEach(b=>{
    b.classList.toggle("active",
      b.getAttribute("onclick").includes(key));
  });

  document.getElementById("seasonVisual").style.background = season.bg;

  document.getElementById("seasonVisual").innerHTML = `
    <div class="season-emoji">${season.emoji}</div>
    <h3>${season.name}</h3>
    <p>Seasonal Color Collection</p>
  `;

  document.getElementById("seasonBadge").textContent = season.badge;
  document.getElementById("seasonTitle").textContent = season.title;
  document.getElementById("seasonDesc").textContent = season.desc;
  document.getElementById("seasonTip").textContent = season.tip;

  document.getElementById("seasonColors").innerHTML =
    season.colors.map(c=>`
      <div class="trend-color">
        <span style="background:${c[1]}"></span>
        ${c[0]}
      </div>
    `).join("");
}

// 화장품 출력

function renderProducts() {
  const tone = tones[selected];
  const keyword = document.getElementById("search").value.toLowerCase();

  document.getElementById("productTitle").textContent =
    tone.name + " 추천 화장품 ♡";

  document.getElementById("productDescription").textContent =
    tone.desc + "에 어울리는 컬러를 모아봤어요.";

  const items = tone.products.filter(p=>
    (category==="전체" || p[0]===category) &&
    (p[1]+p[2]+p[0]).toLowerCase().includes(keyword)
  );

  if(items.length===0) {
    productGrid.innerHTML =
      "<p style='grid-column:1/-1;text-align:center;padding:40px'>검색 결과가 없어요.</p>";
    return;
  }

  productGrid.innerHTML = items.map(p=>`
    <div class="product-card">
      <div class="product-image" style="background:${p[3]}22">
        ${p[4]}
      </div>
      <div class="product-info">
        <span class="tag">${p[0]}</span>
        <h3>${p[1]}</h3>
        <p>${p[2]}</p>
        <div class="color-name">
          <span class="dot" style="display:inline-block;vertical-align:middle;background:${p[3]}"></span>
          추천 컬러
        </div>
      </div>
    </div>
  `).join("");
}

// 화장품 필터

document.querySelectorAll("#filters button").forEach(button=>{
  button.addEventListener("click",()=>{
    category=button.dataset.type;

    document.querySelectorAll("#filters button").forEach(b=>
      b.classList.toggle("active",b===button)
    );

    renderProducts();
  });
});

// 검색

document.getElementById("search").addEventListener("input",renderProducts);

// 첫 화면 실행

renderTones();
renderProducts();
selectSeason("autumn");

</script>
</body>
</html>
