<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>이지스: 사관 아카데미 — 세계관 소개</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+KR:wght@300;400;600;700&family=Black+Han+Sans&family=Noto+Sans+KR:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #080a0f;
    --bg2: #0d1018;
    --surface: #111520;
    --surface2: #181e2e;
    --border: rgba(255,255,255,0.06);
    --red: #c0392b;
    --red-bright: #e74c3c;
    --gold: #b8963e;
    --gold-light: #d4af5a;
    --blue: #1a3a6e;
    --blue-light: #2a5298;
    --text: #e8e4dc;
    --text-dim: #8a8680;
    --text-muted: #4a4844;
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body { background: var(--bg); color: var(--text); font-family: 'Noto Serif KR', serif; font-weight: 300; line-height: 1.9; overflow-x: hidden; }
  body::before { content: ''; position: fixed; inset: 0; background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E"); pointer-events: none; z-index: 0; opacity: 0.4; }

  .hero { position: relative; min-height: 100vh; display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center; padding: 6rem 2rem 4rem; overflow: hidden; }
  .hero-bg { position: absolute; inset: 0; background: radial-gradient(ellipse 80% 60% at 50% 40%, rgba(26,58,110,0.25) 0%, transparent 70%), radial-gradient(ellipse 40% 30% at 50% 60%, rgba(192,57,43,0.12) 0%, transparent 60%), var(--bg); z-index: 0; }
  .hero-cracks { position: absolute; inset: 0; z-index: 1; pointer-events: none; }
  .hero-cracks svg { width: 100%; height: 100%; opacity: 0.18; }
  .crack-line { stroke: var(--red-bright); stroke-width: 1; fill: none; filter: drop-shadow(0 0 6px #e74c3c); animation: crackPulse 4s ease-in-out infinite; }
  .crack-line:nth-child(2) { animation-delay: 1.4s; opacity: 0.6; }
  .crack-line:nth-child(3) { animation-delay: 2.8s; opacity: 0.4; }
  @keyframes crackPulse { 0%, 100% { opacity: 0.7; filter: drop-shadow(0 0 4px #e74c3c); } 50% { opacity: 1; filter: drop-shadow(0 0 12px #e74c3c) drop-shadow(0 0 24px #c0392b); } }
  .hero-content { position: relative; z-index: 2; }
  .hero-eyebrow { font-family: 'Noto Sans KR', sans-serif; font-size: 0.7rem; font-weight: 500; letter-spacing: 0.4em; color: var(--gold); text-transform: uppercase; margin-bottom: 1.8rem; opacity: 0; animation: fadeUp 0.8s 0.2s forwards; }
  .hero-title { font-family: 'Black Han Sans', sans-serif; font-size: clamp(2.4rem, 7vw, 6.5rem); letter-spacing: -0.01em; line-height: 1; color: var(--text); margin-bottom: 0.4rem; opacity: 0; animation: fadeUp 0.9s 0.4s forwards; }
  .hero-title span { background: linear-gradient(135deg, var(--red-bright) 0%, var(--gold-light) 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; }
  .hero-sub { font-family: 'Black Han Sans', sans-serif; font-size: clamp(1rem, 3vw, 1.6rem); color: var(--text-dim); letter-spacing: 0.08em; margin-bottom: 3rem; opacity: 0; animation: fadeUp 0.9s 0.6s forwards; }
  .hero-divider { width: 1px; height: 60px; background: linear-gradient(to bottom, transparent, var(--gold), transparent); margin: 0 auto 2.4rem; opacity: 0; animation: fadeUp 0.8s 0.8s forwards; }
  .hero-desc { max-width: 620px; font-size: 0.95rem; color: var(--text-dim); line-height: 2; opacity: 0; animation: fadeUp 0.9s 1s forwards; }
  .hero-desc em { color: var(--red-bright); font-style: normal; }
  .scroll-hint { position: absolute; bottom: 2.5rem; left: 50%; transform: translateX(-50%); z-index: 2; display: flex; flex-direction: column; align-items: center; gap: 0.5rem; opacity: 0; animation: fadeUp 0.8s 1.6s forwards; }
  .scroll-hint span { font-family: 'Noto Sans KR', sans-serif; font-size: 0.6rem; letter-spacing: 0.3em; color: var(--text-muted); }
  .scroll-dot { width: 1px; height: 40px; background: linear-gradient(to bottom, var(--text-muted), transparent); animation: scrollPulse 2s ease-in-out infinite; }
  @keyframes scrollPulse { 0%, 100% { transform: scaleY(1); opacity: 0.4; } 50% { transform: scaleY(0.6); opacity: 1; } }
  @keyframes fadeUp { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }

  nav { position: sticky; top: 0; z-index: 100; background: rgba(8,10,15,0.85); backdrop-filter: blur(16px); border-bottom: 1px solid var(--border); }
  .nav-inner { max-width: 1100px; margin: 0 auto; padding: 0 2rem; display: flex; align-items: center; height: 52px; overflow-x: auto; scrollbar-width: none; }
  .nav-inner::-webkit-scrollbar { display: none; }
  .nav-logo { font-family: 'Black Han Sans', sans-serif; font-size: 1rem; color: var(--gold); margin-right: 2.5rem; white-space: nowrap; flex-shrink: 0; letter-spacing: 0.05em; }
  .nav-link { font-family: 'Noto Sans KR', sans-serif; font-size: 0.72rem; font-weight: 500; letter-spacing: 0.15em; color: var(--text-dim); text-decoration: none; padding: 0 1.2rem; height: 100%; display: flex; align-items: center; white-space: nowrap; flex-shrink: 0; transition: color 0.2s; border-bottom: 2px solid transparent; position: relative; top: 1px; }
  .nav-link:hover { color: var(--text); }
  .nav-link.active { color: var(--gold); border-bottom-color: var(--gold); }

  main { max-width: 1100px; margin: 0 auto; padding: 0 2rem; }
  .section { padding: 5rem 0; border-bottom: 1px solid var(--border); }
  .section:last-child { border-bottom: none; }
  .section-label { font-family: 'Noto Sans KR', sans-serif; font-size: 0.65rem; letter-spacing: 0.45em; color: var(--red-bright); text-transform: uppercase; margin-bottom: 1rem; display: flex; align-items: center; gap: 0.8rem; }
  .section-label::after { content: ''; flex: 1; max-width: 60px; height: 1px; background: var(--red-bright); opacity: 0.4; }
  .section-title { font-family: 'Black Han Sans', sans-serif; font-size: clamp(1.8rem, 4vw, 2.8rem); color: var(--text); line-height: 1.15; margin-bottom: 2.5rem; }
  .section-title .accent { color: var(--gold-light); }

  .overview-grid { display: grid; grid-template-columns: 1fr 1fr; border: 1px solid var(--border); background: var(--surface); }
  .overview-cell { padding: 2.4rem; border-right: 1px solid var(--border); border-bottom: 1px solid var(--border); transition: background 0.3s; }
  .overview-cell:nth-child(2n) { border-right: none; }
  .overview-cell:nth-last-child(-n+2) { border-bottom: none; }
  .overview-cell:hover { background: var(--surface2); }
  .cell-icon { font-size: 1.4rem; margin-bottom: 0.8rem; display: block; }
  .cell-title { font-family: 'Black Han Sans', sans-serif; font-size: 1rem; color: var(--gold-light); margin-bottom: 0.6rem; letter-spacing: 0.04em; }
  .cell-text { font-size: 0.85rem; color: var(--text-dim); line-height: 1.85; }

  .awakened-split { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5px; background: var(--border); }
  .awakened-card { background: var(--surface); padding: 3rem 2.5rem; position: relative; overflow: hidden; transition: background 0.3s; }
  .awakened-card:hover { background: var(--surface2); }
  .awakened-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px; }
  .card-esper::before { background: linear-gradient(90deg, var(--red), transparent); }
  .card-guide::before { background: linear-gradient(90deg, var(--blue-light), transparent); }
  .card-type { font-family: 'Noto Sans KR', sans-serif; font-size: 0.6rem; letter-spacing: 0.5em; text-transform: uppercase; margin-bottom: 1.2rem; }
  .card-esper .card-type { color: var(--red-bright); }
  .card-guide .card-type { color: #4a7fc1; }
  .card-name { font-family: 'Black Han Sans', sans-serif; font-size: 2rem; margin-bottom: 1.4rem; line-height: 1; color: var(--text); }
  .card-body { font-size: 0.87rem; color: var(--text-dim); line-height: 1.9; margin-bottom: 1.8rem; }
  .danger-tag { display: inline-block; padding: 0.3rem 0.9rem; font-family: 'Noto Sans KR', sans-serif; font-size: 0.65rem; letter-spacing: 0.2em; border: 1px solid; margin-top: 0.4rem; }
  .card-esper .danger-tag { border-color: var(--red); color: var(--red-bright); background: rgba(192,57,43,0.08); }
  .card-guide .danger-tag { border-color: #2a5298; color: #6a9fd8; background: rgba(42,82,152,0.1); }

  .district-list { display: flex; flex-direction: column; border: 1px solid var(--border); }
  .district-item { display: grid; grid-template-columns: 80px 1fr; border-bottom: 1px solid var(--border); transition: background 0.25s; cursor: default; }
  .district-item:last-child { border-bottom: none; }
  .district-item:hover { background: var(--surface2); }
  .district-num { display: flex; align-items: center; justify-content: center; font-family: 'Black Han Sans', sans-serif; font-size: 1.6rem; color: var(--text-muted); background: var(--surface); border-right: 1px solid var(--border); padding: 1.8rem 1rem; transition: color 0.25s; }
  .district-item:hover .district-num { color: var(--gold); }
  .district-item.zone5 .district-num { color: var(--red); }
  .district-body { padding: 1.8rem 2rem; }
  .district-name { font-family: 'Black Han Sans', sans-serif; font-size: 0.95rem; color: var(--text); margin-bottom: 0.4rem; letter-spacing: 0.04em; }
  .district-item.zone5 .district-name { color: var(--red-bright); }
  .district-desc { font-size: 0.84rem; color: var(--text-dim); line-height: 1.8; }
  .district-tag { display: inline-block; padding: 0.2rem 0.7rem; font-family: 'Noto Sans KR', sans-serif; font-size: 0.58rem; letter-spacing: 0.2em; margin-bottom: 0.5rem; border-radius: 2px; }
  .tag-safe { background: rgba(26,58,110,0.3); color: #7aa5d4; border: 1px solid #2a5298; }
  .tag-free { background: rgba(192,57,43,0.15); color: var(--red-bright); border: 1px solid var(--red); }

  .faction-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1px; background: var(--border); }
  .faction-card { background: var(--surface); padding: 2.4rem 2rem; position: relative; overflow: hidden; transition: background 0.3s; }
  .faction-card:hover { background: var(--surface2); }
  .faction-card::after { content: attr(data-symbol); position: absolute; right: 1rem; bottom: 1rem; font-family: 'Black Han Sans', sans-serif; font-size: 4rem; opacity: 0.04; line-height: 1; pointer-events: none; }
  .faction-label { font-family: 'Noto Sans KR', sans-serif; font-size: 0.6rem; letter-spacing: 0.4em; margin-bottom: 0.8rem; }
  .faction-aegis .faction-label { color: var(--blue-light); }
  .faction-academy .faction-label { color: var(--gold); }
  .faction-liberty .faction-label { color: var(--red-bright); }
  .faction-name { font-family: 'Black Han Sans', sans-serif; font-size: 1.3rem; color: var(--text); margin-bottom: 1rem; line-height: 1.2; }
  .faction-desc { font-size: 0.83rem; color: var(--text-dim); line-height: 1.85; }
  .faction-keyword { margin-top: 1.5rem; display: flex; flex-wrap: wrap; gap: 0.5rem; }
  .kw { font-family: 'Noto Sans KR', sans-serif; font-size: 0.6rem; letter-spacing: 0.15em; padding: 0.25rem 0.65rem; border-radius: 2px; }
  .faction-aegis .kw { background: rgba(42,82,152,0.2); color: #7aa5d4; border: 1px solid rgba(42,82,152,0.4); }
  .faction-academy .kw { background: rgba(184,150,62,0.15); color: var(--gold-light); border: 1px solid rgba(184,150,62,0.3); }
  .faction-liberty .kw { background: rgba(192,57,43,0.15); color: #e07060; border: 1px solid rgba(192,57,43,0.3); }

  .nexus-block { background: var(--surface); border: 1px solid var(--border); border-left: 3px solid var(--red); padding: 3rem; position: relative; overflow: hidden; }
  .nexus-block::before { content: 'CLASSIFIED'; position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%) rotate(-12deg); font-family: 'Black Han Sans', sans-serif; font-size: 5rem; color: var(--red); opacity: 0.04; pointer-events: none; white-space: nowrap; }
  .nexus-header { display: flex; align-items: center; gap: 1rem; margin-bottom: 1.5rem; }
  .nexus-dot { width: 8px; height: 8px; border-radius: 50%; background: var(--red-bright); box-shadow: 0 0 8px var(--red-bright); animation: blink 2s ease-in-out infinite; flex-shrink: 0; }
  @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0.2; } }
  .nexus-title { font-family: 'Black Han Sans', sans-serif; font-size: 1.4rem; color: var(--text); }
  .nexus-subtitle { font-family: 'Noto Sans KR', sans-serif; font-size: 0.65rem; letter-spacing: 0.3em; color: var(--red-bright); opacity: 0.8; }
  .nexus-body { font-size: 0.87rem; color: var(--text-dim); line-height: 1.9; }
  .nexus-body strong { color: var(--text); font-weight: 600; }
  .nexus-body .redact { color: var(--red-bright); }

  footer { border-top: 1px solid var(--border); padding: 3rem 2rem; text-align: center; }
  .footer-logo { font-family: 'Black Han Sans', sans-serif; font-size: 1.4rem; color: var(--gold); margin-bottom: 0.5rem; letter-spacing: 0.1em; }
  .footer-sub { font-family: 'Noto Sans KR', sans-serif; font-size: 0.65rem; letter-spacing: 0.3em; color: var(--text-muted); }

  p { margin-bottom: 1rem; }
  p:last-child { margin-bottom: 0; }
  .reveal { opacity: 0; transform: translateY(24px); transition: opacity 0.7s ease, transform 0.7s ease; }
  .reveal.visible { opacity: 1; transform: translateY(0); }

  @media (max-width: 700px) {
    .overview-grid { grid-template-columns: 1fr; }
    .overview-cell:nth-child(2n) { border-right: 1px solid var(--border); }
    .overview-cell:nth-last-child(-n+2) { border-bottom: 1px solid var(--border); }
    .overview-cell:last-child { border-bottom: none; }
    .awakened-split { grid-template-columns: 1fr; }
    .faction-grid { grid-template-columns: 1fr; }
    .district-item { grid-template-columns: 60px 1fr; }
    .nexus-block { padding: 2rem; }
  }
</style>
</head>
<body>

<section class="hero" id="top">
  <div class="hero-bg"></div>
  <div class="hero-cracks">
    <svg viewBox="0 0 1400 800" preserveAspectRatio="xMidYMid slice">
      <path class="crack-line" d="M700 0 L680 120 L720 200 L660 350 L700 500 L640 700 L700 800"/>
      <path class="crack-line" d="M680 120 L580 160 L500 140 L380 200 L300 180"/>
      <path class="crack-line" d="M660 350 L760 380 L820 340 L940 400 L1000 370 L1100 420"/>
    </svg>
  </div>
  <div class="hero-content">
    <p class="hero-eyebrow">World Setting Bible</p>
    <h1 class="hero-title"><span>이지스: 사관 아카데미</span></h1>
    <p class="hero-sub">AEGIS</p>
    <div class="hero-divider"></div>
    <p class="hero-desc">
      차원의 균열이 열리고, 이계의 크리처가 쏟아지며,<br>
      <em>각성자들이 무기가 된 시대</em>.<br>
      진실을 은폐하려는 자들과 이를 폭로하려는 자들의<br>
      보이지 않는 전쟁이 시작된다.
    </p>
  </div>
  <div class="scroll-hint">
    <span>SCROLL</span>
    <div class="scroll-dot"></div>
  </div>
</section>

<nav>
  <div class="nav-inner">
    <span class="nav-logo">AEGIS</span>
    <a href="#overview" class="nav-link">세계 개요</a>
    <a href="#awakened" class="nav-link">각성자</a>
    <a href="#district" class="nav-link">도시 구조</a>
    <a href="#faction" class="nav-link">주요 세력</a>
    <a href="#nexus" class="nav-link">넥서스</a>
  </div>
</nav>

<main>

  <section class="section reveal" id="overview">
    <p class="section-label">World Overview</p>
    <h2 class="section-title">세계 <span class="accent">개요</span></h2>
    <div class="overview-grid">
      <div class="overview-cell">
        <span class="cell-icon">🌌</span>
        <p class="cell-title">열극 (熱隙)</p>
        <p class="cell-text">차원의 균열. 이계의 에너지 <strong>열소(熱素)</strong>를 끊임없이 유출하며 크리처를 쏟아낸다. 발생 원인과 생태는 정부에 의해 철저히 은폐되어 있다.</p>
      </div>
      <div class="overview-cell">
        <span class="cell-icon">⚡</span>
        <p class="cell-title">각성 (覺醒)</p>
        <p class="cell-text">열소에 반응해 초자연적 능력을 얻은 상태. 각성 시기는 예측 불가능하며, 만 13세부터 만 40세까지 매년 의무 검사를 받아야 한다.</p>
      </div>
      <div class="overview-cell">
        <span class="cell-icon">🏛</span>
        <p class="cell-title">이지스 아카데미</p>
        <p class="cell-text">정부가 각성자를 통제하기 위해 설립한 유일한 교육 기관. 각성 확인 시 48시간 내 강제 이송되며, 본인의 의사는 묻지 않는다.</p>
      </div>
      <div class="overview-cell">
        <span class="cell-icon">🔥</span>
        <p class="cell-title">보이지 않는 전쟁</p>
        <p class="cell-text">정부는 각성자를 무기이자 선전 도구로 삼고, 혁명군 리버티 벨은 그들의 해방을 위해 싸운다. 전쟁은 전장이 아닌 아카데미의 복도 속에서도 벌어진다.</p>
      </div>
    </div>
  </section>

  <section class="section reveal" id="awakened">
    <p class="section-label">Awakened</p>
    <h2 class="section-title">각성자 <span class="accent">분류</span></h2>
    <div class="awakened-split">
      <div class="awakened-card card-esper">
        <p class="card-type">Esper</p>
        <h3 class="card-name">에스퍼</h3>
        <p class="card-body">내면에 잠재된 감정에 따라 능력이 발현되는 각성자. 염력, 원소 조작, 신체 강화, 감각 확장, 공간 왜곡 등 다양한 형태로 나타난다. 능력 사용은 신체적·정신적으로 큰 부담을 주며, 한계를 초과하면 이성을 잃고 파괴 본능만 남은 괴물로 폭주한다.</p>
        <span class="danger-tag">폭주 시 → NOVA 상태 (영구·불가역)</span>
      </div>
      <div class="awakened-card card-guide">
        <p class="card-type">Guide</p>
        <h3 class="card-name">가이드</h3>
        <p class="card-body">에스퍼의 정신적 파장을 안정시켜 폭주를 막는 각성자. 능력을 <strong>가이딩</strong>이라 부르며, 신체 접촉으로 가장 효율적으로 발휘된다. 에스퍼의 안정뿐 아니라 집중력과 능력 정밀도를 향상시키는 시너지도 낸다. 그러나 무분별한 가이딩은 정신을 황폐화시킨다.</p>
        <span class="danger-tag">과부하 시 → BLANK 상태 (회복 필요)</span>
      </div>
    </div>
    <div style="margin-top:1px;background:var(--surface);border:1px solid var(--border);border-top:none;padding:1.8rem 2.5rem;">
      <p style="font-family:'Noto Sans KR',sans-serif;font-size:0.68rem;letter-spacing:0.3em;color:var(--gold);margin-bottom:0.7rem;">PAIR SYSTEM</p>
      <p style="font-size:0.87rem;color:var(--text-dim);line-height:1.9;">졸업 후 에스퍼와 가이드의 정신 파장 싱크로율을 측정해 효율이 가장 높은 한 쌍을 <strong style="color:var(--text);">페어(Pair)</strong>로 지정한다. 모든 훈련과 임무를 함께하는 파트너. 정부는 이를 통해 각성자들이 서로를 상호 감시하게 만든다.</p>
    </div>
  </section>

  <section class="section reveal" id="district">
    <p class="section-label">City Structure</p>
    <h2 class="section-title">도시 <span class="accent">구조</span></h2>
    <div class="district-list">
      <div class="district-item">
        <div class="district-num">1</div>
        <div class="district-body"><span class="district-tag tag-safe">요새 중심부</span><p class="district-name">권력자·부유층 거주 구역</p><p class="district-desc">이지스 군 본부 위치. 최다 병력과 고등급 가이드 배치. 완벽한 안전과 사치를 누리는 공간.</p></div>
      </div>
      <div class="district-item">
        <div class="district-num">2</div>
        <div class="district-body"><span class="district-tag tag-safe">상업·교육 구역</span><p class="district-name">이지스 아카데미 위치</p><p class="district-desc">중상위층 거주. 3구역 주민도 자녀 교육을 위해 무리해서라도 이곳으로 보내는 경우가 많다.</p></div>
      </div>
      <div class="district-item">
        <div class="district-num">3</div>
        <div class="district-body"><span class="district-tag tag-safe">생산 구역</span><p class="district-name">공장 운영 · 물자 공급</p><p class="district-desc">중위~중하위층 거주. 생활 물자 생산·공급. 2구역과의 왕래가 비교적 자유롭다.</p></div>
      </div>
      <div class="district-item">
        <div class="district-num">4</div>
        <div class="district-body"><span class="district-tag tag-safe">유흥 구역</span><p class="district-name">부유층 향락 · 하위층 거주</p><p class="district-desc">부유층을 위한 시설이 집중된 만큼 역설적으로 일정 수준의 안전이 보장된다. 낮에는 조용하다.</p></div>
      </div>
      <div class="district-item zone5">
        <div class="district-num">5</div>
        <div class="district-body"><span class="district-tag tag-free">장벽 외부 · 자유 구역</span><p class="district-name">버려진 자들의 땅 — 리버티 벨 거점</p><p class="district-desc">크리처의 위협에 가장 직접 노출된 무법지대. 그러나 정부의 감시와 통제가 닿지 않는 유일한 자유의 땅. 리버티 벨은 이곳의 지형을 활용해 정부군에 맞선다.</p></div>
      </div>
    </div>
  </section>

  <section class="section reveal" id="faction">
    <p class="section-label">Factions</p>
    <h2 class="section-title">주요 <span class="accent">세력</span></h2>
    <div class="faction-grid">
      <div class="faction-card faction-aegis" data-symbol="이">
        <p class="faction-label">Government Force</p>
        <h3 class="faction-name">통합 방위군<br>이지스</h3>
        <p class="faction-desc">정부의 각성자 군단. 에스퍼(센티넬)와 가이드로 구성. 대중에게는 영웅으로 포장되나 실상은 철저히 통제된 무기다. 우수 졸업생은 의원 직속 호위대나 특수 작전부대에 배치된다.</p>
        <div class="faction-keyword"><span class="kw">미디어 통제</span><span class="kw">영웅화 작업</span><span class="kw">페어 시스템</span></div>
      </div>
      <div class="faction-card faction-academy" data-symbol="아">
        <p class="faction-label">Control Institution</p>
        <h3 class="faction-name">이지스<br>아카데미</h3>
        <p class="faction-desc">정부가 각성자를 길러내는 유일한 교육 기관. 극도로 강압적인 계급 구조. 명령 불복종 체벌 공식 허용. 각성 확인 즉시 강제 입학되며 졸업 후 이지스에 편입된다.</p>
        <div class="faction-keyword"><span class="kw">강제 입학</span><span class="kw">계급 차등</span><span class="kw">세뇌 교육</span></div>
      </div>
      <div class="faction-card faction-liberty" data-symbol="리">
        <p class="faction-label">Revolutionary Force</p>
        <h3 class="faction-name">리버티 벨<br>Liberty Bell</h3>
        <p class="faction-desc">정부의 비인도적 통치에 반발해 조직된 무장 혁명 단체. 5구역 거점. 아카데미에 요원을 위장 잠입시키고, 인간성을 잃지 않은 각성자를 빼내는 <strong>리트리버(Retriever)</strong> 작전을 수행한다.</p>
        <div class="faction-keyword"><span class="kw">게릴라전</span><span class="kw">리트리버 작전</span><span class="kw">넥서스 제거 보유</span></div>
      </div>
    </div>
  </section>

  <section class="section reveal" id="nexus">
    <p class="section-label">Classified Intelligence</p>
    <h2 class="section-title">넥서스 <span class="accent">(Nexus)</span></h2>
    <div class="nexus-block">
      <div class="nexus-header">
        <div class="nexus-dot"></div>
        <div>
          <p class="nexus-title">생체 통제 칩</p>
          <p class="nexus-subtitle">최고 사령부 기밀 — 전원 이식 대상</p>
        </div>
      </div>
      <p class="nexus-body"><strong>공식 명목:</strong> 가이딩 필요 수치를 실시간으로 측정하고 신체 상태를 모니터링해 폭주를 방지하는 장치. 모든 이지스 군인과 아카데미 생도의 신체에 이식된다.</p>
      <br>
      <p class="nexus-body"><strong>실제 기능:</strong> <span class="redact">원격 기폭 장치.</span> 노바 상태처럼 통제 불능에 빠지거나, 반역의 기미를 보일 경우 즉각 뇌·척수를 파괴하여 <span class="redact">'크리처 교전 중 전사'</span>로 위장 처리된다. 이 진실은 최고 사령부만이 알고 있다.</p>
      <br>
      <p class="nexus-body" style="color:var(--text-muted);font-size:0.8rem;">※ 리버티 벨은 자체적으로 넥서스 제거 방법을 보유하고 있다.</p>
    </div>
  </section>

</main>

<footer>
  <p class="footer-logo">AEGIS</p>
  <p class="footer-sub">© 이지스: 사관 아카데미 세계관 바이블 — All Rights Reserved</p>
</footer>

<script>
  const reveals = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); io.unobserve(e.target); } });
  }, { threshold: 0.08 });
  reveals.forEach(el => io.observe(el));

  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('.nav-link');
  const navIO = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) { navLinks.forEach(l => l.classList.remove('active')); const link = document.querySelector(`.nav-link[href="#${e.target.id}"]`); if (link) link.classList.add('active'); } });
  }, { threshold: 0.4 });
  sections.forEach(s => navIO.observe(s));
</script>
</body>
</html>
