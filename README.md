<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sydney Immersion Guide — Resonate</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,900;1,700&family=DM+Sans:opsz,wght@9..40,300;9..40,400;9..40,500;9..40,600&display=swap" rel="stylesheet">
<style>
  :root {
    --purple-deep: #1B1030;
    --purple-mid: #391B5C;
    --purple-light: #744CA2;
    --teal: #1A7F6C;
    --teal-bright: #3A9483;
    --teal-pale: #8FC7BB;
    --gold: #F5C518;
    --gold-dark: #D4A914;
    --pink: #9E1F64;
    --cream: #FFF1C7;
    --white: #FFFFFF;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--purple-deep);
    color: var(--white);
    overflow-x: hidden;
  }

  /* HERO */
  .hero {
    min-height: 100vh;
    position: relative;
    display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center;
    overflow: hidden;
    background: radial-gradient(ellipse at 65% 10%, #391B5C 0%, #1B1030 50%, #0B362E 100%);
    padding: 0 24px;
  }
  .orb { position: absolute; border-radius: 50%; pointer-events: none; }
  .orb1 { width: 680px; height: 680px; background: radial-gradient(circle, rgba(58,148,131,0.18) 0%, transparent 70%); top: -180px; right: -120px; animation: breathe 9s ease-in-out infinite; }
  .orb2 { width: 500px; height: 500px; background: radial-gradient(circle, rgba(245,197,24,0.12) 0%, transparent 70%); bottom: -160px; left: -100px; animation: breathe 11s ease-in-out infinite 3s; }
  .orb3 { width: 300px; height: 300px; background: radial-gradient(circle, rgba(158,31,100,0.15) 0%, transparent 70%); top: 45%; left: 8%; animation: breathe 7s ease-in-out infinite 1.5s; }
  @keyframes breathe { 0%,100% { transform: scale(1); } 50% { transform: scale(1.1); } }

  .hero-eyebrow {
    background: rgba(245,197,24,0.1); border: 1px solid rgba(245,197,24,0.35);
    color: var(--gold); font-size: 11px; font-weight: 600; letter-spacing: 3px; text-transform: uppercase;
    padding: 8px 20px; border-radius: 100px; margin-bottom: 32px;
    position: relative; z-index: 1;
    animation: riseUp 0.9s cubic-bezier(0.16,1,0.3,1) both;
  }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(58px, 10vw, 118px); font-weight: 900; line-height: 0.93;
    position: relative; z-index: 1;
    animation: riseUp 0.9s cubic-bezier(0.16,1,0.3,1) 0.12s both;
  }
  .hero h1 em { font-style: italic; color: var(--teal-bright); }
  .hero h1 .muted { color: rgba(255,255,255,0.28); }
  .hero-desc {
    font-size: clamp(15px, 1.8vw, 18px); font-weight: 300; color: rgba(255,255,255,0.58);
    margin-top: 28px; max-width: 500px; line-height: 1.75;
    position: relative; z-index: 1;
    animation: riseUp 0.9s cubic-bezier(0.16,1,0.3,1) 0.24s both;
  }
  .season-chips {
    display: flex; gap: 10px; flex-wrap: wrap; justify-content: center;
    margin-top: 24px; position: relative; z-index: 1;
    animation: riseUp 0.9s cubic-bezier(0.16,1,0.3,1) 0.36s both;
  }
  .chip {
    background: rgba(255,255,255,0.07); border: 1px solid rgba(255,255,255,0.13);
    border-radius: 100px; padding: 7px 16px; font-size: 12px; color: rgba(255,255,255,0.62); font-weight: 500;
  }
  .chip strong { color: var(--teal-pale); font-weight: 600; }
  .hero-ctas {
    display: flex; gap: 14px; margin-top: 40px; flex-wrap: wrap; justify-content: center;
    position: relative; z-index: 1;
    animation: riseUp 0.9s cubic-bezier(0.16,1,0.3,1) 0.48s both;
  }
  .btn-gold { background: var(--gold); color: var(--purple-deep); font-weight: 600; font-size: 13.5px; padding: 14px 30px; border-radius: 100px; text-decoration: none; transition: all 0.2s; }
  .btn-gold:hover { background: var(--gold-dark); transform: translateY(-2px); box-shadow: 0 10px 32px rgba(245,197,24,0.28); }
  .btn-outline { border: 1px solid rgba(255,255,255,0.25); color: var(--white); font-size: 13.5px; padding: 14px 30px; border-radius: 100px; text-decoration: none; transition: all 0.2s; }
  .btn-outline:hover { border-color: rgba(255,255,255,0.6); background: rgba(255,255,255,0.04); }
  .scroll-indicator { position: absolute; bottom: 32px; left: 50%; transform: translateX(-50%); display: flex; flex-direction: column; align-items: center; gap: 8px; color: rgba(255,255,255,0.28); font-size: 10px; letter-spacing: 2.5px; text-transform: uppercase; z-index: 1; animation: riseUp 1.2s ease 1s both; }
  .scroll-bar { width: 1px; height: 48px; background: linear-gradient(to bottom, rgba(255,255,255,0.28), transparent); animation: drip 2.2s ease infinite; }
  @keyframes drip { 0% { transform: scaleY(0); transform-origin: top; } 50% { transform: scaleY(1); transform-origin: top; } 51% { transform-origin: bottom; } 100% { transform: scaleY(0); transform-origin: bottom; } }
  @keyframes riseUp { from { opacity: 0; transform: translateY(28px); } to { opacity: 1; transform: none; } }

  /* NAV */
  nav { position: sticky; top: 0; z-index: 100; background: rgba(27,16,48,0.9); backdrop-filter: blur(20px); border-bottom: 1px solid rgba(255,255,255,0.06); padding: 0 40px; display: flex; align-items: center; justify-content: space-between; height: 60px; }
  .nav-brand { font-family: 'Playfair Display', serif; font-size: 17px; font-weight: 700; color: var(--gold); text-decoration: none; }
  .nav-brand span { color: rgba(255,255,255,0.4); }
  .nav-links { display: flex; gap: 28px; list-style: none; }
  .nav-links a { color: rgba(255,255,255,0.5); text-decoration: none; font-size: 12.5px; font-weight: 500; letter-spacing: 0.4px; transition: color 0.2s; }
  .nav-links a:hover { color: var(--gold); }

  /* LAYOUT */
  .container { max-width: 1200px; margin: 0 auto; padding: 0 40px; }
  section.sec { padding: 100px 0; }
  .sec-label { display: flex; align-items: center; gap: 12px; font-size: 10.5px; letter-spacing: 3.5px; text-transform: uppercase; color: var(--gold); font-weight: 600; margin-bottom: 18px; }
  .sec-label::after { content: ''; width: 36px; height: 1px; background: rgba(245,197,24,0.45); }
  .sec-title { font-family: 'Playfair Display', serif; font-size: clamp(34px, 5vw, 56px); font-weight: 700; line-height: 1.1; margin-bottom: 14px; }
  .sec-title em { font-style: italic; color: var(--teal-bright); }
  .sec-sub { font-size: 15.5px; font-weight: 300; color: rgba(255,255,255,0.5); line-height: 1.85; max-width: 540px; margin-bottom: 52px; }

  /* SEASON BANNER */
  .season-banner { background: linear-gradient(135deg, #0B362E 0%, #1B1030 55%, #391B5C 100%); padding: 88px 0; text-align: center; position: relative; overflow: hidden; }
  .season-banner::before { content: '🍂'; font-size: 280px; opacity: 0.05; position: absolute; top: 50%; left: 50%; transform: translate(-50%,-50%); pointer-events: none; }
  .season-inner { max-width: 780px; margin: 0 auto; padding: 0 40px; position: relative; z-index: 1; }
  .season-inner h2 { font-family: 'Playfair Display', serif; font-size: clamp(28px,4vw,44px); font-weight: 700; margin-bottom: 20px; line-height: 1.2; }
  .season-inner h2 em { font-style: italic; color: var(--gold); }
  .season-inner p { font-size: 16px; line-height: 1.9; color: rgba(255,255,255,0.62); font-weight: 300; }
  .season-inner p strong { color: var(--teal-pale); font-weight: 500; }
  .weather-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; margin-top: 44px; text-align: center; }
  .weather-item { background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.08); border-radius: 16px; padding: 20px 14px; }
  .weather-item .wi { font-size: 26px; margin-bottom: 8px; }
  .weather-item .wval { font-size: 20px; font-weight: 700; font-family: 'Playfair Display', serif; color: var(--gold); }
  .weather-item .wlabel { font-size: 10.5px; color: rgba(255,255,255,0.4); letter-spacing: 1px; text-transform: uppercase; margin-top: 4px; }

  /* CARDS */
  .grid-3 { display: grid; grid-template-columns: repeat(auto-fill, minmax(330px, 1fr)); gap: 20px; }
  .grid-2 { display: grid; grid-template-columns: repeat(auto-fill, minmax(440px, 1fr)); gap: 20px; }
  .card { background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.08); border-radius: 20px; overflow: hidden; transition: transform 0.3s, border-color 0.3s, box-shadow 0.3s; }
  .card:hover { transform: translateY(-5px); border-color: rgba(255,255,255,0.16); box-shadow: 0 20px 60px rgba(0,0,0,0.45); }
  .card-bar { height: 3px; }
  .bar-teal { background: linear-gradient(90deg, var(--teal), var(--teal-bright)); }
  .bar-gold { background: linear-gradient(90deg, var(--gold-dark), var(--gold)); }
  .bar-pink { background: linear-gradient(90deg, var(--pink), #B64A7F); }
  .bar-purple { background: linear-gradient(90deg, var(--purple-mid), var(--purple-light)); }
  .card-body { padding: 26px 28px 28px; }
  .card-icon { font-size: 32px; margin-bottom: 14px; display: block; }
  .card-name { font-family: 'Playfair Display', serif; font-size: 21px; font-weight: 700; margin-bottom: 10px; line-height: 1.2; }
  .card-meta { margin-bottom: 13px; display: flex; flex-direction: column; gap: 4px; }
  .card-meta span { font-size: 12px; color: var(--teal-pale); line-height: 1.5; }
  .card-text { font-size: 14px; color: rgba(255,255,255,0.6); line-height: 1.8; margin-bottom: 18px; }
  .card-text strong { color: rgba(255,255,255,0.85); font-weight: 500; }
  .tip-box { background: rgba(245,197,24,0.07); border: 1px solid rgba(245,197,24,0.18); border-radius: 10px; padding: 11px 14px; font-size: 12.5px; color: rgba(245,197,24,0.82); line-height: 1.65; }
  .tip-box strong { color: var(--gold); }

  /* WALK CARDS */
  .walk-card { display: flex; border-radius: 20px; overflow: hidden; background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.08); transition: transform 0.3s, box-shadow 0.3s; }
  .walk-card:hover { transform: translateY(-4px); box-shadow: 0 20px 60px rgba(0,0,0,0.4); }
  .walk-side { width: 5px; flex-shrink: 0; }
  .ws-teal { background: linear-gradient(to bottom, var(--teal), var(--teal-bright)); }
  .ws-gold { background: linear-gradient(to bottom, var(--gold-dark), var(--gold)); }
  .ws-pink { background: linear-gradient(to bottom, var(--pink), #B64A7F); }
  .walk-inner { padding: 26px 30px; flex: 1; }
  .walk-header { display: flex; align-items: flex-start; justify-content: space-between; gap: 16px; margin-bottom: 12px; }
  .walk-name { font-family: 'Playfair Display', serif; font-size: 22px; font-weight: 700; line-height: 1.2; }
  .walk-badge { background: rgba(255,255,255,0.08); border-radius: 8px; padding: 5px 12px; font-size: 11px; font-weight: 600; color: rgba(255,255,255,0.5); letter-spacing: 0.5px; white-space: nowrap; flex-shrink: 0; }
  .walk-stats { display: flex; gap: 20px; margin-bottom: 14px; flex-wrap: wrap; }
  .walk-stat { font-size: 12px; color: var(--teal-pale); }
  .walk-stat span { color: rgba(255,255,255,0.75); font-weight: 500; }
  .walks-stack { display: flex; flex-direction: column; gap: 18px; }

  /* VIVID FEATURE */
  .vivid-block { background: linear-gradient(135deg, rgba(57,27,92,0.6) 0%, rgba(27,16,48,0.8) 50%, rgba(11,54,46,0.4) 100%); border: 1px solid rgba(116,76,162,0.35); border-radius: 24px; padding: 50px; position: relative; overflow: hidden; }
  .vivid-block::before { content: ''; position: absolute; inset: 0; background: radial-gradient(ellipse at 80% 50%, rgba(245,197,24,0.06) 0%, transparent 60%); pointer-events: none; }
  .vivid-inner { position: relative; z-index: 1; }
  .vivid-tag { display: inline-flex; align-items: center; gap: 8px; background: rgba(245,197,24,0.15); border: 1px solid rgba(245,197,24,0.3); color: var(--gold); font-size: 10.5px; font-weight: 600; letter-spacing: 2.5px; text-transform: uppercase; padding: 6px 16px; border-radius: 100px; margin-bottom: 20px; }
  .vivid-block h3 { font-family: 'Playfair Display', serif; font-size: clamp(26px, 4vw, 40px); font-weight: 700; line-height: 1.2; margin-bottom: 16px; }
  .vivid-block h3 em { font-style: italic; color: var(--gold); }
  .vivid-block p { font-size: 15px; color: rgba(255,255,255,0.6); line-height: 1.85; max-width: 700px; font-weight: 300; }
  .vivid-block p strong { color: rgba(255,255,255,0.85); font-weight: 500; }
  .vivid-pills { display: flex; gap: 10px; flex-wrap: wrap; margin-top: 24px; }
  .vivid-pill { background: rgba(255,255,255,0.07); border: 1px solid rgba(255,255,255,0.12); border-radius: 100px; padding: 7px 16px; font-size: 12.5px; color: rgba(255,255,255,0.62); }

  /* TIPS */
  .tips-shell { background: linear-gradient(135deg, rgba(26,127,108,0.1) 0%, rgba(57,27,92,0.18) 100%); border: 1px solid rgba(58,148,131,0.18); border-radius: 24px; padding: 52px; }
  .tips-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); gap: 28px; margin-top: 40px; }
  .tip-item { display: flex; gap: 14px; align-items: flex-start; }
  .tip-ico { width: 42px; height: 42px; flex-shrink: 0; background: rgba(245,197,24,0.1); border: 1px solid rgba(245,197,24,0.22); border-radius: 11px; display: flex; align-items: center; justify-content: center; font-size: 18px; }
  .tip-copy h4 { font-size: 13.5px; font-weight: 600; margin-bottom: 5px; }
  .tip-copy p { font-size: 12.5px; color: rgba(255,255,255,0.48); line-height: 1.7; }
  .tip-copy p strong { color: rgba(255,255,255,0.72); font-weight: 500; }

  /* DIVIDER */
  .divider { height: 1px; background: linear-gradient(90deg, transparent, rgba(255,255,255,0.09), transparent); max-width: 1200px; margin: 0 auto; }

  /* FOOTER */
  footer { background: #0D0A18; border-top: 1px solid rgba(255,255,255,0.05); padding: 40px; text-align: center; color: rgba(255,255,255,0.28); font-size: 13px; }
  footer strong { color: var(--gold); font-weight: 600; }

  /* REVEAL */
  .reveal { opacity: 0; transform: translateY(26px); transition: opacity 0.7s ease, transform 0.7s ease; }
  .reveal.in { opacity: 1; transform: none; }

  /* RESPONSIVE */
  @media (max-width: 720px) {
    .container { padding: 0 20px; }
    section.sec { padding: 70px 0; }
    nav { padding: 0 20px; }
    .nav-links { display: none; }
    .grid-2 { grid-template-columns: 1fr; }
    .weather-grid { grid-template-columns: repeat(2,1fr); }
    .tips-shell { padding: 28px 22px; }
    .vivid-block { padding: 28px 24px; }
    .walk-card { flex-direction: column; }
    .walk-side { width: 100%; height: 5px; }
  }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="orb orb1"></div>
  <div class="orb orb2"></div>
  <div class="orb orb3"></div>
  <div class="hero-eyebrow">🇦🇺 Resonate Immersion Program</div>
  <h1><span class="muted">Welcome</span><br>to <em>Sydney,</em><br><span class="muted">mate.</span></h1>
  <p class="hero-desc">Your field guide to exploring one of the world's greatest harbour cities — written for first-time visitors.</p>
  <div class="season-chips">
    <div class="chip">🌊 World-famous beaches</div>
    <div class="chip">🚢 Iconic harbour</div>
    <div class="chip">☕ World-class coffee</div>
  </div>
  <div class="hero-ctas">
    <a href="#walks" class="btn-gold">Start exploring ↓</a>
    <a href="#walks" class="btn-outline">Coastal walks</a>
  </div>
  <div class="scroll-indicator"><div class="scroll-bar"></div>scroll</div>
</div>

<!-- NAV -->
<nav>
  <a href="#" class="nav-brand">Resonate — Sydney Travel Guide</a>
  <ul class="nav-links">
    <li><a href="#walks">Coastal Walks</a></li>
    <li><a href="#beaches">Beaches</a></li>
    <li><a href="#cafes">Cafés</a></li>
    <li><a href="#experiences">Experiences</a></li>
    <li><a href="#tips">Tips</a></li>
  </ul>
</nav>



<!-- COASTAL WALKS -->
<section class="sec" id="walks">
  <div class="container">
    <div class="sec-label reveal">On Foot</div>
    <h2 class="sec-title reveal">Sydney's <em>coastal walks</em><br>are world-class.</h2>
    <p class="sec-sub reveal">Sydney's coastline is one of the most dramatic in the world. These walks are unmissable — clifftop paths, hidden beaches, and harbour views that will genuinely stop you in your tracks.</p>

    <div class="walks-stack">
      <div class="walk-card reveal">
        <div class="walk-side ws-teal"></div>
        <div class="walk-inner">
          <div class="walk-header">
            <div class="walk-name">🌊 Bondi to Coogee Coastal Walk</div>
            <div class="walk-badge">MUST DO #1</div>
          </div>
          <div class="walk-stats">
            <div class="walk-stat">Distance <span>6 km</span></div>
            <div class="walk-stat">Time <span>2–3 hrs</span></div>
            <div class="walk-stat">Difficulty <span>Easy–Medium</span></div>
            <div class="walk-stat">Start <span>Bondi Beach</span></div>
          </div>
          <p class="card-text">Sydney's most iconic walk, and deservedly so. The trail hugs dramatic sandstone clifftops from Bondi all the way south to Coogee, passing five distinct beaches: <strong>Tamarama</strong> (dramatic and compact — beloved by surfers and models), <strong>Bronte</strong> (family-favourite with great facilities), <strong>Clovelly</strong> (a sheltered inlet ideal for snorkelling), and <strong>Gordons Bay</strong>. Along the way you pass the magnificent <strong>Bronte Baths</strong> — a heritage ocean pool carved into the clifftop rock — and the hauntingly beautiful Waverley Cemetery, which sits directly above the sea. End the walk with a meal at Coogee, or turn back to Bondi for a sundowner at the famous Icebergs Dining Room.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Start at Bondi and walk south to Coogee for the best light. The cliff sections have steps and uneven surfaces — proper shoes over thongs. Buses and taxis easily get you back to the city from Coogee.</div>
        </div>
      </div>

      <div class="walk-card reveal">
        <div class="walk-side ws-gold"></div>
        <div class="walk-inner">
          <div class="walk-header">
            <div class="walk-name">🌿 Spit Bridge to Manly Walk</div>
            <div class="walk-badge">LOCAL FAVOURITE</div>
          </div>
          <div class="walk-stats">
            <div class="walk-stat">Distance <span>10 km</span></div>
            <div class="walk-stat">Time <span>3–4 hrs</span></div>
            <div class="walk-stat">Difficulty <span>Moderate</span></div>
            <div class="walk-stat">Start <span>Spit Bridge</span></div>
          </div>
          <p class="card-text">Less famous than Bondi to Coogee but many locals consider it the better walk. This trail weaves through native Sydney bushland along the harbour's northern shore, with views that constantly shift between open water, hidden coves, and the city skyline in the distance. It feels genuinely like a bush hike — you'll earn it — but several small, secret beaches reward you along the way. <strong>End in Manly</strong> for a meal on the promenade, then catch the Manly Ferry back to Circular Quay for a full harbour cruise to finish the day perfectly.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Take a bus to Spit Bridge, walk to Manly, then ferry home — that way you get the walk AND the iconic harbour cruise. Carry water and snacks; there's only one food stop en route (Clontarf Beach).</div>
        </div>
      </div>

      <div class="walk-card reveal">
        <div class="walk-side ws-pink"></div>
        <div class="walk-inner">
          <div class="walk-header">
            <div class="walk-name">🌉 Walk the Harbour Bridge</div>
            <div class="walk-badge">CLOSEST TO THE OFFICE</div>
          </div>
          <div class="walk-stats">
            <div class="walk-stat">Distance <span>2–4 km</span></div>
            <div class="walk-stat">Time <span>1–2 hrs</span></div>
            <div class="walk-stat">Difficulty <span>Easy</span></div>
            <div class="walk-stat">Start <span>Milsons Point</span></div>
          </div>
          <p class="card-text">Walk across the Harbour Bridge from Milsons Point — steps from the North Sydney office — to the city side. The pedestrian walkway is completely free, and the views from the top of the arch are completely unlike any other perspective of Sydney. Once on the city side, descend into <strong>The Rocks</strong>: Sydney's oldest neighbourhood, full of sandstone laneways, colonial history, weekend markets, rooftop bars, and excellent restaurants tucked into 200-year-old buildings. This is the fastest way to understand both the city's geography and its character in one walk.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Walk over in the morning for the best light on the harbour. The pedestrian path is on the eastern (city) side of the Bridge. The Rocks Market runs Saturdays and Sundays — local food, art, and great coffee.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- BEACHES -->
<section class="sec" id="beaches">
  <div class="container">
    <div class="sec-label reveal">Sun &amp; Surf</div>
    <h2 class="sec-title reveal">The beaches that make<br>Sydney <em>legendary.</em></h2>
    <p class="sec-sub reveal">Sydney's beaches are world-famous for good reason — and there are dozens of them. These are the ones worth making the trip for. Always swim between the red and yellow flags.</p>

    <div class="grid-3">
      <div class="card reveal">
        <div class="card-bar bar-teal"></div>
        <div class="card-body">
          <span class="card-icon">🏄</span>
          <div class="card-name">Bondi Beach</div>
          <div class="card-meta"><span>📍 Campbell Parade, Bondi</span><span>🚌 Bus from Bondi Junction station (~30 min from city)</span></div>
          <p class="card-text">The most famous beach in Australia and one of the most recognisable in the world. Two kilometres of golden sand, a lively beach culture, the famous <strong>Bondi Icebergs saltwater pool</strong> perched on the southern clifftop, and Campbell Parade lined with excellent cafés and restaurants. More than just a beach — it's a whole scene and a cultural institution.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Avoid weekend peak hours. Tuesday or Wednesday morning is ideal — the beach is yours. Have breakfast at Porch and Parlour on the promenade. The Icebergs pool is open to the public for a small fee.</div>
        </div>
      </div>

      <div class="card reveal">
        <div class="card-bar bar-gold"></div>
        <div class="card-body">
          <span class="card-icon">⛵</span>
          <div class="card-name">Manly Beach</div>
          <div class="card-meta"><span>📍 N Steyne, Manly NSW</span><span>🚢 30-min Manly Ferry from Circular Quay — the crossing is half the experience</span></div>
          <p class="card-text">Sydney's other great beach, and the one locals often prefer. Two kilometres of surf backed by Norfolk Island pines and a relaxed promenade of excellent cafés. Manly has a distinct village atmosphere — slower, breezier, and more laid-back than the city. The ferry crossing through the harbour past the Opera House is itself a bucket-list experience costing no more than a bus fare.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Take the ferry at sunset and look back at the Opera House and Harbour Bridge as you return to the city — one of Sydney's great views. Use your Opal card.</div>
        </div>
      </div>

      <div class="card reveal">
        <div class="card-bar bar-purple"></div>
        <div class="card-body">
          <span class="card-icon">🌿</span>
          <div class="card-name">Bronte Beach</div>
          <div class="card-meta"><span>📍 Bronte Rd, Bronte</span><span>🚌 Bus from Bondi Junction (~10 min)</span></div>
          <p class="card-text">The insider pick — smaller and more sheltered than Bondi, yet equally beautiful and far less crowded. Famous for the <strong>Bronte Baths</strong>, a heritage ocean pool where you swim in calm water while waves crash alongside you. A lush grassy park backs the beach, making it perfect for a long, lazy afternoon. This is where actual Sydneysiders go when they want a beach to themselves.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> A natural stop on the Bondi-to-Coogee walk. The ocean baths at Bronte are one of the most unique swim experiences in Sydney. Go in the morning for the calmest water.</div>
        </div>
      </div>

      <div class="card reveal">
        <div class="card-bar bar-teal"></div>
        <div class="card-body">
          <span class="card-icon">🤿</span>
          <div class="card-name">Clovelly Beach</div>
          <div class="card-meta"><span>📍 Clovelly Rd, Clovelly</span><span>🚌 Bus from Bondi Junction</span></div>
          <p class="card-text">Not a surf beach — something more unusual. A narrow, sheltered ocean inlet with crystal-clear, perfectly calm water that's exceptional for snorkelling. The tame <strong>blue grouper fish</strong> that live in the bay have grown almost comfortable with swimmers and are one of Sydney's great wildlife encounters. Quieter and more local-feeling than anywhere else on this coastline.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Bring or hire a snorkel mask. The fish here are genuinely remarkable. A short detour from the Bondi-to-Coogee walk that's absolutely worth the stop.</div>
        </div>
      </div>

      <div class="card reveal">
        <div class="card-bar bar-pink"></div>
        <div class="card-body">
          <span class="card-icon">🌅</span>
          <div class="card-name">Blues Point Reserve</div>
          <div class="card-meta"><span>📍 Blues Point Rd, North Sydney</span><span>🚶 10-min walk from the office — best sunset spot in Sydney</span></div>
          <p class="card-text">Not a beach, but possibly the single most important listing in this guide. This small harbourside park, a 10-minute walk from the North Sydney office, delivers an unobstructed 180° view of both the Harbour Bridge and the Opera House in one frame — the photograph that defines Sydney. After-work picnics here as the sun sets over the city are one of the great simple pleasures Sydney offers. Free, always open, permanently magnificent.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Arrive 30 minutes before sunset. As the light turns gold, both the Bridge and Opera House glow simultaneously. Grab takeaway food and a cold drink from the shops on Miller St beforehand.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- CAFES -->
<section class="sec" id="cafes">
  <div class="container">
    <div class="sec-label reveal">Coffee Culture</div>
    <h2 class="sec-title reveal">Australia invented the<br><em>flat white.</em> Act accordingly.</h2>
    <p class="sec-sub reveal">Sydney's café culture is genuinely world-class — not tourist-brochure world-class, but actually world-class. These are the places that set the standard. Always order a flat white first.</p>

    <div class="grid-3">
      <div class="card reveal">
        <div class="card-bar bar-teal"></div>
        <div class="card-body">
          <span class="card-icon">🌱</span>
          <div class="card-name">The Grounds of Alexandria</div>
          <div class="card-meta"><span>📍 7A/2 Huntley St, Alexandria</span><span>🕐 Daily from 7:00 AM</span></div>
          <p class="card-text">Sydney's most talked-about café, full stop. Set in a converted industrial space with its own working garden, bakery, butcher, and roasting house — it's more of a destination than a café. Fresh pastries baked on-site, beautiful food presentation, and in-house roasted coffee. There's also a resident pig named Kevin Bacon who lives in the garden.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Weekends get very busy — visit on a weekday morning for the best experience and shortest wait. Don't skip whatever fresh pastry is on display.</div>
        </div>
      </div>

      <div class="card reveal">
        <div class="card-bar bar-gold"></div>
        <div class="card-body">
          <span class="card-icon">🥞</span>
          <div class="card-name">bills, Darlinghurst</div>
          <div class="card-meta"><span>📍 433 Liverpool St, Darlinghurst</span><span>🕐 Daily 7:30 AM – 3:00 PM</span></div>
          <p class="card-text">Bill Granger's original sun-drenched café, credited with setting the global standard for Sydney-style brunch. The <strong>ricotta hotcakes with honeycomb butter</strong> are among the most imitated dishes in Australian food history — order them without deliberating. Blonde wood, flowers, natural light, and an atmosphere that makes you want to stay for three hours. A genuine piece of Sydney food culture.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Order the ricotta hotcakes. Non-negotiable. The scrambled eggs (impossibly creamy, done in a double boiler) are also a revelation.</div>
        </div>
      </div>

      <div class="card reveal">
        <div class="card-bar bar-pink"></div>
        <div class="card-body">
          <span class="card-icon">🔬</span>
          <div class="card-name">ONA Coffee, Marrickville</div>
          <div class="card-meta"><span>📍 171 Addison Rd, Marrickville</span><span>🕐 Weekdays from 7:00 AM &nbsp;|&nbsp; Weekends 8:00 AM</span></div>
          <p class="card-text">The gold standard for specialty coffee in Sydney — run by Australia's World Barista Champion. Every cup feels like an education in flavour, origin, and craft. The baristas will happily walk you through the single-origin filter options. Pair with the <strong>Moroccan eggs</strong> for the best breakfast combo in the city. This is where serious coffee people make a pilgrimage.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Ask the barista about the seasonal filter. They know everything and love talking about it. A short Inner West line train ride from the city.</div>
        </div>
      </div>

      <div class="card reveal">
        <div class="card-bar bar-purple"></div>
        <div class="card-body">
          <span class="card-icon">🫖</span>
          <div class="card-name">Brewmance, Crows Nest</div>
          <div class="card-meta"><span>📍 56 Willoughby Rd, Crows Nest</span><span>🕐 Mon–Fri 6:30 AM–3 PM &nbsp;|&nbsp; Sat–Sun 7:30 AM–3 PM</span></div>
          <p class="card-text">Your closest excellent café to the North Sydney office — a 10-minute walk from the building, rated 4.9★ and genuinely deserving of it. Dog-friendly, latte art taken seriously, and an unusually creative menu. The <strong>Earl Grey Matcha latte</strong> is something you won't find anywhere else. Crows Nest village around it has great dinner options to explore after work.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Your default morning coffee stop for the two weeks. Gets busy 8–9 AM so arrive slightly before or after the rush.</div>
        </div>
      </div>

      <div class="card reveal">
        <div class="card-bar bar-teal"></div>
        <div class="card-body">
          <span class="card-icon">🥐</span>
          <div class="card-name">Flour &amp; Stone, Woolloomooloo</div>
          <div class="card-meta"><span>📍 53 Riley St, Woolloomooloo</span><span>🕐 Tue–Fri 7 AM – 3 PM &nbsp;|&nbsp; Sat–Sun 8 AM – 3 PM</span></div>
          <p class="card-text">One of Sydney's most beloved bakeries — cult status, genuinely earned. The pastries here are exceptional: <strong>lamingtons, orange and almond cake, croissants</strong> made with extraordinary care. Frequently cited as Sydney's best bakery by both critics and locals. Small, no-frills, and everything sells out by mid-morning. Worth queueing for.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Arrive early — the best items are gone by 10 AM. The lamington is the signature. Short walk from Kings Cross station.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- EXPERIENCES -->
<section class="sec" id="experiences">
  <div class="container">
    <div class="sec-label reveal">Can't-Miss Experiences</div>
    <h2 class="sec-title reveal">Things you'll still be<br><em>talking about</em> at home.</h2>
    <p class="sec-sub reveal">Beyond the beach and the café — the experiences that make Sydney genuinely unforgettable.</p>

    <div class="grid-2">
      <div class="card reveal">
        <div class="card-bar bar-teal"></div>
        <div class="card-body">
          <span class="card-icon">🎭</span>
          <div class="card-name">Sydney Opera House</div>
          <div class="card-meta"><span>📍 Bennelong Point, Sydney</span><span>🚢 10-min ferry from Milsons Point &nbsp;|&nbsp; Tours daily</span></div>
          <p class="card-text">One of the great buildings of the 20th century — and in person, it's more extraordinary than any photograph. The exterior is free to wander and photograph, but a guided tour of the interior is worth every dollar: the acoustics, the story of Danish architect Jørn Utzon (who never saw the finished building), and the harbour views from the front forecourt are all remarkable. If possible, catch an evening performance — it doesn't matter what it is. The experience of being inside the Opera House at night changes how you understand the city.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> The most dramatic approach is by ferry from Milsons Point — it takes 10 minutes and costs a normal transport fare. Arrive from the water for the full effect.</div>
        </div>
      </div>

      <div class="card reveal">
        <div class="card-bar bar-gold"></div>
        <div class="card-body">
          <span class="card-icon">🦘</span>
          <div class="card-name">Taronga Zoo</div>
          <div class="card-meta"><span>📍 Bradleys Head Rd, Mosman</span><span>🚢 12-min ferry from Circular Quay &nbsp;|&nbsp; Daily 9:30 AM–5 PM</span></div>
          <p class="card-text">A world-class zoo set on a hillside above the harbour, with the Sydney skyline as the literal backdrop for its animals. See Australian wildlife that genuinely doesn't exist anywhere else on Earth: <strong>koalas, kangaroos, wallabies, Tasmanian devils, wombats, and platypuses</strong>. The Koala Encounter — five minutes up close with a koala — must be booked well in advance and sells out weeks ahead. The views from the zoo's upper levels of the harbour and city are spectacular on their own.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Book the Koala Encounter the moment you land ($15 extra — it sells out). Take the cable car down from the top of the zoo for the best harbour view.</div>
        </div>
      </div>

      <div class="card reveal">
        <div class="card-bar bar-pink"></div>
        <div class="card-body">
          <span class="card-icon">🪨</span>
          <div class="card-name">The Rocks &amp; Circular Quay</div>
          <div class="card-meta"><span>📍 The Rocks, Sydney NSW</span><span>🚢 Ferry from Milsons Point, or walk across Harbour Bridge</span></div>
          <p class="card-text">Sydney's oldest surviving neighbourhood, built on the foundations of the original 1788 British colony. Today: sandstone laneways with excellent restaurants in 200-year-old buildings, the <strong>Rocks Market</strong> on weekends (local food, art, produce), fresh oysters at the quayside, and the free Museum of Contemporary Art hosting world-class exhibitions. Sit at Circular Quay and watch ferries dock with the Bridge and Opera House framing everything.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> The Glenmore Hotel rooftop bar has the best Harbour Bridge view of any bar in Sydney. The Rocks Market runs Saturdays and Sundays — excellent for local gifts and fresh produce.</div>
        </div>
      </div>

      <div class="card reveal">
        <div class="card-bar bar-purple"></div>
        <div class="card-body">
          <span class="card-icon">🌸</span>
          <div class="card-name">Royal Botanic Garden</div>
          <div class="card-meta"><span>📍 Mrs Macquaries Rd, Sydney &nbsp;|&nbsp; Free entry always</span><span>🚶 10-min walk from Circular Quay</span></div>
          <p class="card-text">Thirty hectares of garden on the edge of Sydney Harbour, completely free to enter at all times. In April and May, the <strong>Autumn Garden Trail</strong> showcases changing foliage across themed gardens. Walk through to <strong>Mrs Macquaries Point</strong> for the most-photographed view of the Opera House and Harbour Bridge side by side. At dusk, thousands of grey-headed flying foxes leave their roosts in the fig trees to feed — a spectacular and surreal piece of Sydney wildlife right in the CBD.</p>
          <div class="tip-box"><strong>💡 Tip:</strong> Visit at dusk specifically to see the flying foxes depart. It's one of Sydney's great free wildlife experiences and most visitors have no idea it happens.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- TIPS -->
<section class="sec" id="tips">
  <div class="container">
    <div class="sec-label reveal">Before You Step Out</div>
    <h2 class="sec-title reveal">Things every first-timer<br><em>needs to know.</em></h2>

    <div class="tips-shell reveal">
      <div class="tips-grid">
        <div class="tip-item">
          <div class="tip-ico">🚆</div>
          <div class="tip-copy"><h4>Get an Opal Card First</h4><p>Sydney's public transport card covers all trains, buses, and ferries. Tap on and off every journey. Available at 7-Eleven, newsagencies, and the airport. A weekly cap limits how much you can spend in any week.</p></div>
        </div>
        <div class="tip-item">
          <div class="tip-ico">☀️</div>
          <div class="tip-copy"><h4>The UV is No Joke</h4><p>Sydney's UV is high enough to burn fair skin in under 15 minutes — even on cloudy days. <strong>SPF 50+, a hat, sunglasses</strong> — always. You will be outside more than you think.</p></div>
        </div>
        <div class="tip-item">
          <div class="tip-ico">🌊</div>
          <div class="tip-copy"><h4>Swim Between the Flags</h4><p>Red and yellow flags mark the safe, patrolled sections of each beach. Sydney's beaches have rips and currents. <strong>Always swim between the flags, no exceptions.</strong></p></div>
        </div>
        <div class="tip-item">
          <div class="tip-ico">☕</div>
          <div class="tip-copy"><h4>Order a Flat White</h4><p>Not a latte. Not a cappuccino. A <strong>flat white</strong> — strong espresso with silky micro-foamed milk, no froth. Australia's gift to global coffee culture. This is your first order in every café.</p></div>
        </div>
        <div class="tip-item">
          <div class="tip-ico">🍽️</div>
          <div class="tip-copy"><h4>Eat Like a Local</h4><p>Things to try: <strong>fresh oysters, a meat pie, a prawn roll, Tim Tams</strong> (chocolate biscuits — also try the "Tim Tam slam"), and a lamington. Sydney's seafood is world-class.</p></div>
        </div>
        <div class="tip-item">
          <div class="tip-ico">🧥</div>
          <div class="tip-copy"><h4>Pack in Layers</h4><p>April days reach 22°C; evenings drop to 14–15°C. <strong>A light jacket is essential for evenings.</strong> A compact waterproof layer is worth carrying — autumn brings occasional showers.</p></div>
        </div>
        <div class="tip-item">
          <div class="tip-ico">🚢</div>
          <div class="tip-copy"><h4>Ferries are Underrated Transport</h4><p>Sydney's harbour ferry network is a real way to get around — the <strong>Manly Ferry</strong> from Circular Quay is a 30-minute harbour cruise that costs exactly the same as a bus fare. Use it.</p></div>
        </div>
        <div class="tip-item">
          <div class="tip-ico">🦜</div>
          <div class="tip-copy"><h4>Expect Wildlife Everywhere</h4><p>Cockatoos, kookaburras, rainbow lorikeets, ibis, and possums in parks. <strong>Don't feed them</strong> — especially ibis (locally called "bin chickens"). The possums come out at night in most suburbs.</p></div>
        </div>
        <div class="tip-item">
          <div class="tip-ico">💬</div>
          <div class="tip-copy"><h4>Learn Some Aussie</h4><p><strong>"No worries"</strong> = you're welcome / it's fine. <strong>"Mate"</strong> = friend (universal). <strong>"Arvo"</strong> = afternoon. <strong>"Brekkie"</strong> = breakfast. <strong>"Servo"</strong> = petrol station. Sydneysiders are warm and direct.</p></div>
        </div>
      </div>
    </div>
  </div>
</section>

<footer>
  <p>Prepared with care for the <strong>Resonate Head Office Immersion Program</strong> &nbsp;·&nbsp; North Sydney, Australia</p>
  <p style="margin-top:8px; opacity:0.6;">Have an extraordinary two weeks. The city is yours. 🦘 🌉 🌊</p>
</footer>

<script>
  const els = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        setTimeout(() => e.target.classList.add('in'), e.target.dataset.d || 0);
        io.unobserve(e.target);
      }
    });
  }, { threshold: 0.1 });
  els.forEach((el, i) => { el.dataset.d = (i % 5) * 70; io.observe(el); });
</script>

</body>
</html>
