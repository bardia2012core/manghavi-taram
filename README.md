<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>تولدت مبارک نوشین 🎶</title>
  <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;700;900&display=swap" rel="stylesheet" />
  <style>
    :root {
      --deep:   #0a1628;
      --ocean:  #0d2b55;
      --mid:    #1a4a8a;
      --bright: #2e7fd8;
      --glint:  #7ec8e3;
      --foam:   #c8eaf5;
      --gold:   #e8c96b;
      --rose:   #e879a0;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }
    html, body { width: 100%; height: 100%; overflow: hidden; }

    body {
      font-family: 'Vazirmatn', sans-serif;
      background: var(--deep);
      color: var(--foam);
    }

    /* ══════ PAGES ══════ */
    .page {
      position: fixed;
      inset: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      opacity: 0;
      pointer-events: none;
      transition: opacity .6s ease;
      z-index: 1;
    }
    .page.active {
      opacity: 1;
      pointer-events: all;
    }

    /* ══════ CANVAS BG ══════ */
    #bg-canvas {
      position: fixed;
      inset: 0;
      z-index: 0;
    }

    /* ══════ SCROLLING TICKER ══════ */
    .ticker-wrap {
      position: fixed;
      left: 0; right: 0;
      z-index: 2;
      overflow: hidden;
      pointer-events: none;
    }
    .ticker-wrap.top    { top: 0; }
    .ticker-wrap.bottom { bottom: 0; }
    .ticker-wrap.mid1   { top: 28%; }
    .ticker-wrap.mid2   { top: 56%; }

    .ticker-inner {
      display: flex;
      width: max-content;
      animation: ticker 18s linear infinite;
      gap: 0;
    }
    .ticker-inner.rev { animation-direction: reverse; animation-duration: 22s; }

    .ticker-item {
      padding: 6px 18px;
      font-size: 1.3rem;
      white-space: nowrap;
      opacity: .55;
      letter-spacing: .05em;
    }

    .ticker-wrap.top    .ticker-item,
    .ticker-wrap.bottom .ticker-item {
      background: rgba(14,43,85,.7);
      border-top: 1px solid rgba(126,200,227,.15);
      border-bottom: 1px solid rgba(126,200,227,.15);
      font-size: .95rem;
    }
    .ticker-wrap.mid1 .ticker-item,
    .ticker-wrap.mid2 .ticker-item {
      background: transparent;
      font-size: 1.6rem;
    }

    @keyframes ticker {
      from { transform: translateX(0); }
      to   { transform: translateX(-50%); }
    }

    /* ══════ MAIN PAGE ══════ */
    .main-center {
      position: relative;
      z-index: 3;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 2.5rem;
      text-align: center;
      padding: 2rem;
    }

    .name-title {
      font-size: clamp(4.5rem, 15vw, 9rem);
      font-weight: 900;
      line-height: 1;
      background: linear-gradient(135deg, var(--foam) 0%, var(--glint) 45%, var(--gold) 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      letter-spacing: -.02em;
      animation: fadeUp .8s both;
    }
    .name-sub {
      font-size: clamp(.9rem, 2.5vw, 1.2rem);
      color: var(--glint);
      font-weight: 300;
      letter-spacing: .15em;
      animation: fadeUp .8s .2s both;
    }

    /* ══════ BUTTONS ══════ */
    .btn-row {
      display: flex;
      gap: 1.5rem;
      flex-wrap: wrap;
      justify-content: center;
      animation: fadeUp .8s .4s both;
    }

    .btn {
      border: none;
      border-radius: 999px;
      font-family: 'Vazirmatn', sans-serif;
      font-weight: 700;
      cursor: pointer;
      transition: transform .2s, box-shadow .2s, font-size .4s, padding .4s;
      position: relative;
      overflow: hidden;
    }
    .btn::after {
      content: "";
      position: absolute;
      inset: 0;
      background: rgba(255,255,255,.12);
      opacity: 0;
      transition: opacity .2s;
    }
    .btn:hover::after { opacity: 1; }
    .btn:active { transform: scale(.96) !important; }

    .btn-yes {
      background: linear-gradient(135deg, #2e7fd8, #1a4a8a);
      color: #fff;
      box-shadow: 0 4px 20px rgba(46,127,216,.5);
      padding: 1rem 2.5rem;
      font-size: 1.2rem;
    }
    .btn-yes:hover { transform: translateY(-4px) scale(1.04); box-shadow: 0 8px 30px rgba(46,127,216,.7); }

    .btn-no {
      background: linear-gradient(135deg, #1e3a5f, #0d2b55);
      color: var(--glint);
      border: 1px solid rgba(126,200,227,.35);
      box-shadow: 0 4px 12px rgba(0,0,0,.3);
      padding: 1rem 2.5rem;
      font-size: 1.2rem;
    }
    .btn-no:hover { transform: translateY(-2px); }

    /* ══════ CONGRATS PAGE ══════ */
    .congrats-box {
      position: relative;
      z-index: 3;
      max-width: 640px;
      margin: 2rem;
      background: linear-gradient(135deg, rgba(30,58,95,.8), rgba(13,43,85,.85));
      border: 1px solid rgba(232,201,107,.35);
      border-radius: 2.5rem;
      padding: 3.5rem 2.5rem;
      text-align: center;
      backdrop-filter: blur(18px);
      box-shadow: 0 30px 80px rgba(0,0,0,.5), inset 0 1px 0 rgba(255,255,255,.08);
      animation: popIn .7s cubic-bezier(.34,1.56,.64,1) both;
    }

    .congrats-title {
      font-size: clamp(1.8rem, 6vw, 3rem);
      font-weight: 900;
      color: var(--gold);
      margin-bottom: 1.5rem;
      line-height: 1.3;
    }

    .congrats-text {
      font-size: clamp(.95rem, 2.5vw, 1.15rem);
      line-height: 2.1;
      font-weight: 300;
      color: var(--foam);
    }
    .congrats-text strong { color: var(--gold); font-weight: 700; }

    .congrats-emoji {
      font-size: 2rem;
      letter-spacing: .4rem;
      margin: 1.5rem 0 0;
      display: block;
      animation: pulse 2s ease-in-out infinite;
    }

    /* corner ornaments */
    .orn {
      position: absolute;
      font-size: 1.4rem;
      opacity: .5;
    }
    .orn.tr { top: 1.2rem; left: 1.2rem; }
    .orn.tl { top: 1.2rem; right: 1.2rem; }
    .orn.br { bottom: 1.2rem; left: 1.2rem; }
    .orn.bl { bottom: 1.2rem; right: 1.2rem; }

    /* falling confetti on congrats */
    .confetti-piece {
      position: fixed;
      animation: confettiFall linear infinite;
      pointer-events: none;
      z-index: 4;
      font-size: 1.3rem;
    }

    /* ══════ ANIMATIONS ══════ */
    @keyframes fadeUp {
      from { opacity:0; transform:translateY(28px); }
      to   { opacity:1; transform:translateY(0); }
    }
    @keyframes popIn {
      from { opacity:0; transform:scale(.7); }
      to   { opacity:1; transform:scale(1); }
    }
    @keyframes pulse {
      0%,100% { transform:scale(1); }
      50%      { transform:scale(1.06); }
    }
    @keyframes confettiFall {
      from { transform:translateY(-8vh) rotate(0deg); opacity:1; }
      to   { transform:translateY(108vh) rotate(720deg); opacity:0; }
    }

    /* ══════ RESPONSIVE ══════ */
    @media (max-width:480px) {
      .btn-row { flex-direction: column; align-items: center; }
      .congrats-box { padding: 2.5rem 1.5rem; }
    }
  </style>
</head>
<body>

<!-- CANVAS -->
<canvas id="bg-canvas"></canvas>

<!-- TICKERS (always visible) -->
<!-- Top bar: Yazdi text -->
<div class="ticker-wrap top">
  <div class="ticker-inner" id="t-top"></div>
</div>
<!-- Mid row 1: emojis fish/music -->
<div class="ticker-wrap mid1">
  <div class="ticker-inner rev" id="t-mid1"></div>
</div>
<!-- Mid row 2: emojis art/yazdi -->
<div class="ticker-wrap mid2">
  <div class="ticker-inner" id="t-mid2"></div>
</div>
<!-- Bottom bar: birthday text -->
<div class="ticker-wrap bottom">
  <div class="ticker-inner rev" id="t-bot"></div>
</div>

<!-- ════ PAGE 1: MAIN ════ -->
<div class="page active" id="page-main">
  <div class="main-center">
    <span class="name-sub">✦ تبریک تولد ✦</span>
    <h1 class="name-title">نوشین</h1>
    <span class="name-sub">هنرمند · موزیسین · روح آزاد</span>
    <div class="btn-row" id="btn-row">
      <button class="btn btn-yes" id="btn-yes" onclick="goYes()">منو بزن</button>
      <button class="btn btn-no"  id="btn-no"  onclick="goNo()">منو نزن</button>
    </div>
  </div>
</div>

<!-- ════ PAGE 2: CONGRATS ════ -->
<div class="page" id="page-congrats">
  <div class="congrats-box">
    <span class="orn tl">✦</span><span class="orn tr">✦</span>
    <span class="orn bl">🐟</span><span class="orn br">🐠</span>

    <h2 class="congrats-title">نوشین عزیزم،<br>تولدت مبارک 🎂</h2>
    <p class="congrats-text">
      امیدوارم این سال‌گرد زندگیت
      مثل <strong>موج دریا</strong> پر از انرژی باشه،<br>
      مثل <strong>نت‌های موسیقی</strong> هماهنگ و زیبا،<br>
      و مثل <strong>کاشی‌های رنگارنگ یزدی</strong>
      لبریز از هنر و رنگ.<br><br>
      تو یه نفر خاصی نوشین،<br>
      و هر روزت باید به همین خاصی باشه. 💙
    </p>
    <span class="congrats-emoji">🎉 🐟 🎵 🌟 🎶 🐠 🎊</span>
  </div>
</div>

<script>
  /* ══════════════════════════════
     TICKER CONTENT
  ══════════════════════════════ */
  const topItems  = ['✦ یزد شهر بادگیرها','✦ کاشی‌کاری فیروزه‌ای','✦ باقلوای یزدی','✦ گردوی یزد','✦ معماری بی‌نظیر','✦ شب‌های ستاره‌باران','✦ دل‌انگیزترین شهر ایران'];
  const mid1Items = ['🐟','🐠','🐡','🎵','🎶','🎸','🎹','🎺','🐙','🌊','🦈','🎵','🐟'];
  const mid2Items = ['🕌','✦','🌹','⭐','🎨','🖌️','🎭','🎪','🌙','🌸','🎯','🔮','🕌'];
  const botItems  = ['🎂 تولدت مبارک نوشین','🎉 امروز روز توئه','🌟 بهترین تولد','💙 دوستت داریم','🎵 روزت پر از موسیقی','🐟 شاد باش','🌊 زندگیت مثل دریا'];

  function buildTicker(id, items, repeat=4) {
    const el = document.getElementById(id);
    const full = Array(repeat).fill(items).flat();
    el.innerHTML = full.map(t => `<span class="ticker-item">${t}</span>`).join('');
  }
  buildTicker('t-top',  topItems,  6);
  buildTicker('t-mid1', mid1Items, 8);
  buildTicker('t-mid2', mid2Items, 8);
  buildTicker('t-bot',  botItems,  6);

  /* ══════════════════════════════
     OCEAN CANVAS
  ══════════════════════════════ */
  const canvas = document.getElementById('bg-canvas');
  const ctx    = canvas.getContext('2d');
  let W, H;

  function resize() {
    W = canvas.width  = window.innerWidth;
    H = canvas.height = window.innerHeight;
  }
  resize();
  window.addEventListener('resize', resize);

  const pts = Array.from({length:60}, () => ({
    x: Math.random() * 2000,
    y: Math.random() * 2000,
    r: Math.random() * 1.8 + .4,
    a: Math.random() * Math.PI * 2,
    s: Math.random() * .25 + .05
  }));

  const wavesCfg = [
    { amp:35, freq:.007, speed:.012, color:'rgba(46,127,216,.07)', y:.5 },
    { amp:22, freq:.011, speed:.020, color:'rgba(126,200,227,.05)', y:.62 },
    { amp:14, freq:.017, speed:.028, color:'rgba(46,127,216,.04)', y:.76 }
  ];

  let T = 0;
  function draw() {
    ctx.clearRect(0,0,W,H);
    const g = ctx.createLinearGradient(0,0,0,H);
    g.addColorStop(0,'#0a1628'); g.addColorStop(.5,'#0d2346'); g.addColorStop(1,'#060e1a');
    ctx.fillStyle = g;
    ctx.fillRect(0,0,W,H);

    wavesCfg.forEach(w => {
      ctx.beginPath();
      ctx.moveTo(0, w.y*H);
      for(let x=0; x<=W; x+=4) {
        ctx.lineTo(x, w.y*H + Math.sin(x*w.freq + T*w.speed*60)*w.amp);
      }
      ctx.lineTo(W,H); ctx.lineTo(0,H); ctx.closePath();
      ctx.fillStyle = w.color;
      ctx.fill();
    });

    pts.forEach(p => {
      p.a += p.s * .01;
      const px = (p.x + Math.sin(p.a)*18) % W;
      const py = (p.y + Math.cos(p.a*.7)*12 + T*.15) % (H+40);
      ctx.beginPath();
      ctx.arc(px, py, p.r, 0, Math.PI*2);
      ctx.fillStyle = `rgba(126,200,227,${.12 + Math.sin(p.a)*.08})`;
      ctx.fill();
    });

    T++;
    requestAnimationFrame(draw);
  }
  draw();

  /* ══════════════════════════════
     BUTTON LOGIC
  ══════════════════════════════ */
  let noCount = 0;

  function showPage(id) {
    document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
    document.getElementById(id).classList.add('active');
  }

  function goYes() {
    launchConfetti();
    showPage('page-congrats');
  }

  function goNo() {
    noCount++;
    if (noCount >= 3) {
      launchConfetti();
      showPage('page-congrats');
      return;
    }

    const btnYes = document.getElementById('btn-yes');
    const btnNo  = document.getElementById('btn-no');

    // Scale factors: each "no" makes yes bigger and no smaller
    const yesSizes = [1.0, 1.55, 2.2];
    const noSizes  = [1.0, 0.65, 0.38];
    const yesPads  = ['1rem 2.5rem', '1.3rem 3.2rem', '1.7rem 4rem'];
    const noPads   = ['1rem 2.5rem', '.7rem 1.6rem', '.45rem 1rem'];

    const i = noCount; // 1 or 2

    btnYes.style.fontSize   = yesSizes[i] * 1.2 + 'rem';
    btnYes.style.padding    = yesPads[i];
    btnYes.style.boxShadow  = `0 ${4+i*6}px ${20+i*20}px rgba(46,127,216,${.5+i*.2})`;

    btnNo.style.fontSize    = noSizes[i] * 1.2 + 'rem';
    btnNo.style.padding     = noPads[i];
    btnNo.style.opacity     = (1 - i * 0.3).toString();

    // Wiggle the yes button to tease
    btnYes.style.animation = 'none';
    void btnYes.offsetWidth;
    btnYes.style.animation = 'wiggle .4s ease';
  }

  /* ══════════════════════════════
     CONFETTI
  ══════════════════════════════ */
  function launchConfetti() {
    const syms = ['🎵','🐟','⭐','🎶','🐠','✦','🌊','♫','🐡','🎉','💙','🌟'];
    for(let i=0; i<22; i++) {
      const c = document.createElement('div');
      c.className = 'confetti-piece';
      c.textContent = syms[i % syms.length];
      c.style.cssText = `
        left:${Math.random()*100}%;
        font-size:${.8 + Math.random()*1.2}rem;
        animation-duration:${3 + Math.random()*4}s;
        animation-delay:${Math.random()*2}s;
      `;
      document.body.appendChild(c);
      setTimeout(() => c.remove(), 8000);
    }
  }
</script>

<style>
  @keyframes wiggle {
    0%   { transform: rotate(0deg) scale(1); }
    25%  { transform: rotate(-4deg) scale(1.06); }
    50%  { transform: rotate(4deg) scale(1.06); }
    75%  { transform: rotate(-2deg) scale(1.03); }
    100% { transform: rotate(0deg) scale(1); }
  }
</style>
</body>
</html>
