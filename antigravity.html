<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Antigravity Interface</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Syne:wght@400;700;800&family=Space+Mono:wght@400;700&display=swap');

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #060a12;
    --glow: #00f0ff;
    --glow2: #a259ff;
    --glow3: #ff4ecd;
    --text: #e8f4ff;
    --card-bg: rgba(10, 20, 40, 0.6);
  }

  body {
    background: var(--bg);
    min-height: 100vh;
    font-family: 'Syne', sans-serif;
    color: var(--text);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    cursor: none;
    user-select: none;
  }

  /* Starfield */
  .stars {
    position: fixed; inset: 0; z-index: 0; pointer-events: none;
  }
  .star {
    position: absolute;
    border-radius: 50%;
    background: white;
    animation: twinkle var(--dur) ease-in-out infinite alternate;
  }
  @keyframes twinkle {
    from { opacity: var(--min-op); transform: scale(1); }
    to { opacity: 1; transform: scale(1.6); }
  }

  /* Custom cursor */
  #cursor {
    position: fixed;
    width: 18px; height: 18px;
    border-radius: 50%;
    background: var(--glow);
    box-shadow: 0 0 16px 6px rgba(0,240,255,0.55);
    pointer-events: none;
    z-index: 9999;
    transform: translate(-50%, -50%);
    transition: width 0.15s, height 0.15s, background 0.2s, box-shadow 0.2s;
    mix-blend-mode: screen;
  }
  #cursor.big {
    width: 48px; height: 48px;
    background: rgba(0,240,255,0.18);
    box-shadow: 0 0 40px 16px rgba(0,240,255,0.35);
  }

  /* Scene */
  .scene {
    position: relative;
    z-index: 2;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 12px;
  }

  h1 {
    font-size: clamp(1.6rem, 4vw, 2.8rem);
    font-weight: 800;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    background: linear-gradient(90deg, var(--glow), var(--glow2), var(--glow3));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 4px;
    filter: drop-shadow(0 0 18px rgba(0,240,255,0.3));
  }

  .subtitle {
    font-family: 'Space Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.22em;
    color: rgba(200,230,255,0.38);
    text-transform: uppercase;
    margin-bottom: 52px;
  }

  /* Floating cards grid */
  .cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 28px;
  }

  .card {
    position: relative;
    width: 160px;
    height: 160px;
    border-radius: 22px;
    background: var(--card-bg);
    border: 1px solid rgba(0,240,255,0.12);
    backdrop-filter: blur(14px);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 10px;
    cursor: none;
    transition: border-color 0.3s;
    will-change: transform;
    animation: floatBase var(--float-dur, 4s) ease-in-out infinite alternate;
    animation-delay: var(--float-delay, 0s);
    box-shadow:
      0 8px 40px rgba(0,0,0,0.55),
      0 0 0 0px rgba(0,240,255,0);
  }

  @keyframes floatBase {
    from { transform: translateY(0px) rotate(var(--tilt-from, -1deg)); }
    to   { transform: translateY(var(--float-amt, -18px)) rotate(var(--tilt-to, 1.5deg)); }
  }

  .card::before {
    content: '';
    position: absolute;
    inset: -1px;
    border-radius: 23px;
    background: linear-gradient(135deg, var(--c1, var(--glow)), var(--c2, var(--glow2)));
    opacity: 0;
    transition: opacity 0.35s;
    z-index: -1;
  }

  .card:hover::before { opacity: 1; }
  .card:hover {
    border-color: transparent;
    box-shadow:
      0 20px 60px rgba(0,0,0,0.7),
      0 0 60px var(--glow-color, rgba(0,240,255,0.25));
  }

  .card-icon {
    font-size: 2.4rem;
    line-height: 1;
    filter: drop-shadow(0 0 10px var(--icon-glow, rgba(0,240,255,0.7)));
    transition: transform 0.3s, filter 0.3s;
  }
  .card:hover .card-icon {
    transform: scale(1.25) translateY(-4px);
    filter: drop-shadow(0 0 22px var(--icon-glow, rgba(0,240,255,0.9)));
  }

  .card-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.62rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: rgba(200,230,255,0.6);
    transition: color 0.3s;
  }
  .card:hover .card-label { color: rgba(255,255,255,0.92); }

  /* Repulsion particles */
  .particle {
    position: fixed;
    border-radius: 50%;
    pointer-events: none;
    z-index: 1;
    mix-blend-mode: screen;
  }

  /* Orb behind */
  .orb {
    position: fixed;
    border-radius: 50%;
    filter: blur(80px);
    pointer-events: none;
    z-index: 0;
    animation: orbFloat 9s ease-in-out infinite alternate;
    opacity: 0.22;
  }
  .orb1 { width: 420px; height: 420px; background: var(--glow2); top: -100px; left: -80px; animation-delay: 0s; }
  .orb2 { width: 340px; height: 340px; background: var(--glow); bottom: -80px; right: -60px; animation-delay: -4s; }
  @keyframes orbFloat {
    from { transform: translate(0, 0) scale(1); }
    to   { transform: translate(40px, 30px) scale(1.12); }
  }

  /* Hint text */
  .hint {
    margin-top: 48px;
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    color: rgba(200,230,255,0.22);
    text-transform: uppercase;
    animation: pulseHint 2.5s ease-in-out infinite;
  }
  @keyframes pulseHint {
    0%,100% { opacity: 0.22; }
    50% { opacity: 0.55; }
  }

  /* Scan line overlay */
  body::after {
    content: '';
    position: fixed; inset: 0;
    background: repeating-linear-gradient(
      to bottom,
      transparent 0px,
      transparent 3px,
      rgba(0,0,0,0.07) 3px,
      rgba(0,0,0,0.07) 4px
    );
    pointer-events: none;
    z-index: 100;
  }
</style>
</head>
<body>

<div class="orb orb1"></div>
<div class="orb orb2"></div>
<div class="stars" id="stars"></div>
<div id="cursor"></div>

<div class="scene">
  <h1>Antigravity</h1>
  <p class="subtitle">Hover Interface · Zero-G Edition</p>

  <div class="cards" id="cards">
    <div class="card" style="--float-dur:3.8s;--float-delay:0s;--float-amt:-20px;--tilt-from:-2deg;--tilt-to:1.5deg;--c1:#00f0ff;--c2:#a259ff;--glow-color:rgba(0,240,255,0.3);--icon-glow:rgba(0,240,255,0.9);">
      <div class="card-icon">🌊</div>
      <div class="card-label">Flux</div>
    </div>
    <div class="card" style="--float-dur:4.5s;--float-delay:-1.2s;--float-amt:-28px;--tilt-from:1deg;--tilt-to:-2deg;--c1:#a259ff;--c2:#ff4ecd;--glow-color:rgba(162,89,255,0.3);--icon-glow:rgba(162,89,255,0.9);">
      <div class="card-icon">⚡</div>
      <div class="card-label">Charge</div>
    </div>
    <div class="card" style="--float-dur:3.3s;--float-delay:-0.7s;--float-amt:-15px;--tilt-from:-1.5deg;--tilt-to:2.5deg;--c1:#ff4ecd;--c2:#ff9a3c;--glow-color:rgba(255,78,205,0.3);--icon-glow:rgba(255,78,205,0.9);">
      <div class="card-icon">🔮</div>
      <div class="card-label">Void</div>
    </div>
    <div class="card" style="--float-dur:5s;--float-delay:-2s;--float-amt:-22px;--tilt-from:2deg;--tilt-to:-1deg;--c1:#3cffd0;--c2:#00f0ff;--glow-color:rgba(60,255,208,0.3);--icon-glow:rgba(60,255,208,0.9);">
      <div class="card-icon">🛸</div>
      <div class="card-label">Drift</div>
    </div>
    <div class="card" style="--float-dur:4.2s;--float-delay:-3s;--float-amt:-24px;--tilt-from:-0.5deg;--tilt-to:3deg;--c1:#ffd93d;--c2:#ff6b6b;--glow-color:rgba(255,217,61,0.3);--icon-glow:rgba(255,217,61,0.9);">
      <div class="card-icon">🌀</div>
      <div class="card-label">Spin</div>
    </div>
    <div class="card" style="--float-dur:3.6s;--float-delay:-1.8s;--float-amt:-18px;--tilt-from:1.5deg;--tilt-to:-2.5deg;--c1:#ff4ecd;--c2:#a259ff;--glow-color:rgba(255,78,205,0.3);--icon-glow:rgba(255,78,205,0.9);">
      <div class="card-icon">✨</div>
      <div class="card-label">Aether</div>
    </div>
  </div>

  <p class="hint">Move cursor · Watch elements react</p>
</div>

<script>
// ── Stars ──────────────────────────────────────────────
const starsEl = document.getElementById('stars');
for (let i = 0; i < 120; i++) {
  const s = document.createElement('div');
  s.className = 'star';
  const size = Math.random() * 2.2 + 0.4;
  const dur = (Math.random() * 3 + 1.5).toFixed(2);
  const minOp = (Math.random() * 0.15 + 0.04).toFixed(2);
  Object.assign(s.style, {
    width: size + 'px', height: size + 'px',
    left: Math.random() * 100 + '%',
    top: Math.random() * 100 + '%',
    '--dur': dur + 's',
    '--min-op': minOp,
    animationDelay: (Math.random() * 3).toFixed(2) + 's'
  });
  starsEl.appendChild(s);
}

// ── Custom cursor ──────────────────────────────────────
const cursor = document.getElementById('cursor');
let mx = window.innerWidth / 2, my = window.innerHeight / 2;
let cx = mx, cy = my;

document.addEventListener('mousemove', e => { mx = e.clientX; my = e.clientY; });

function tickCursor() {
  cx += (mx - cx) * 0.18;
  cy += (my - cy) * 0.18;
  cursor.style.left = cx + 'px';
  cursor.style.top = cy + 'px';
  requestAnimationFrame(tickCursor);
}
tickCursor();

// ── Card magnetic repulsion ────────────────────────────
const cards = Array.from(document.querySelectorAll('.card'));
const cardStates = cards.map(() => ({ tx: 0, ty: 0, rx: 0, ry: 0, scale: 1 }));

const REPEL_RADIUS = 200;
const REPEL_STRENGTH = 55;
const TILT_STRENGTH = 18;

function lerp(a, b, t) { return a + (b - a) * t; }

function tickCards() {
  cards.forEach((card, i) => {
    const rect = card.getBoundingClientRect();
    const cardCX = rect.left + rect.width / 2;
    const cardCY = rect.top + rect.height / 2;
    const dx = mx - cardCX;
    const dy = my - cardCY;
    const dist = Math.sqrt(dx * dx + dy * dy);

    let targetTX = 0, targetTY = 0, targetRX = 0, targetRY = 0, targetScale = 1;

    if (dist < REPEL_RADIUS) {
      const force = (1 - dist / REPEL_RADIUS);
      const angle = Math.atan2(dy, dx);
      targetTX = -Math.cos(angle) * force * REPEL_STRENGTH;
      targetTY = -Math.sin(angle) * force * REPEL_STRENGTH;
      targetRX = (dy / rect.height) * TILT_STRENGTH * force;
      targetRY = -(dx / rect.width) * TILT_STRENGTH * force;
      targetScale = 1 + force * 0.08;
      cursor.classList.add('big');
    } else {
      cursor.classList.remove('big');
    }

    const st = cardStates[i];
    st.tx = lerp(st.tx, targetTX, 0.1);
    st.ty = lerp(st.ty, targetTY, 0.1);
    st.rx = lerp(st.rx, targetRX, 0.1);
    st.ry = lerp(st.ry, targetRY, 0.1);
    st.scale = lerp(st.scale, targetScale, 0.1);

    card.style.transform =
      `translate(${st.tx.toFixed(2)}px, ${st.ty.toFixed(2)}px) rotateX(${st.rx.toFixed(2)}deg) rotateY(${st.ry.toFixed(2)}deg) scale(${st.scale.toFixed(3)})`;
  });
  requestAnimationFrame(tickCards);
}
tickCards();

// ── Particle burst on click ────────────────────────────
document.addEventListener('click', e => {
  for (let i = 0; i < 14; i++) {
    const p = document.createElement('div');
    p.className = 'particle';
    const size = Math.random() * 8 + 3;
    const hues = ['#00f0ff','#a259ff','#ff4ecd','#3cffd0','#ffd93d'];
    const color = hues[Math.floor(Math.random() * hues.length)];
    const angle = (Math.PI * 2 / 14) * i + Math.random() * 0.4;
    const speed = Math.random() * 90 + 40;
    Object.assign(p.style, {
      width: size + 'px', height: size + 'px',
      background: color,
      boxShadow: `0 0 ${size * 2}px ${color}`,
      left: e.clientX + 'px', top: e.clientY + 'px',
    });
    document.body.appendChild(p);
    const vx = Math.cos(angle) * speed;
    const vy = Math.sin(angle) * speed;
    const startX = e.clientX, startY = e.clientY;
    const dur = Math.random() * 0.4 + 0.5;
    const startTime = performance.now();
    function animP(now) {
      const progress = (now - startTime) / (dur * 1000);
      if (progress >= 1) { p.remove(); return; }
      const ease = 1 - progress * progress;
      p.style.left = (startX + vx * progress) + 'px';
      p.style.top = (startY + vy * progress + 60 * progress * progress) + 'px';
      p.style.opacity = ease;
      p.style.transform = `scale(${ease})`;
      requestAnimationFrame(animP);
    }
    requestAnimationFrame(animP);
  }
});

// ── Perspective on scene ───────────────────────────────
const scene = document.querySelector('.scene');
document.addEventListener('mousemove', e => {
  const ox = (e.clientX / window.innerWidth - 0.5) * 10;
  const oy = (e.clientY / window.innerHeight - 0.5) * -7;
  scene.style.transform = `perspective(900px) rotateY(${ox}deg) rotateX(${oy}deg)`;
});
</script>
</body>
</html>
