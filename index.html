<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Linear Induction Motor — Interactive Explainer</title>
<link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Rajdhani:wght@300;400;600;700&family=Orbitron:wght@400;700;900&display=swap" rel="stylesheet">
<style>
  :root {
    --bg:       #050a12;
    --panel:    #080f1c;
    --border:   #0d2240;
    --cyan:     #00e5ff;
    --blue:     #1565ff;
    --green:    #00ff9d;
    --orange:   #ff6d00;
    --red:      #ff1744;
    --yellow:   #ffe500;
    --text:     #c8dff0;
    --dim:      #3a5a78;
    --glow:     0 0 18px rgba(0,229,255,0.5);
    --glow-g:   0 0 18px rgba(0,255,157,0.5);
  }

  * { margin:0; padding:0; box-sizing:border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Rajdhani', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ── Scanline overlay ── */
  body::before {
    content:'';
    position:fixed; inset:0;
    background: repeating-linear-gradient(
      0deg, transparent, transparent 2px,
      rgba(0,0,0,0.08) 2px, rgba(0,0,0,0.08) 4px
    );
    pointer-events:none; z-index:9999;
  }

  /* ── Header ── */
  header {
    text-align:center;
    padding: 48px 24px 24px;
    position:relative;
  }
  header::after {
    content:'';
    display:block;
    width:600px; max-width:90%; height:1px;
    margin:24px auto 0;
    background: linear-gradient(90deg, transparent, var(--cyan), transparent);
  }
  .tag {
    font-family:'Share Tech Mono'; font-size:11px;
    color:var(--cyan); letter-spacing:4px;
    text-transform:uppercase; margin-bottom:12px;
    opacity:.7;
  }
  h1 {
    font-family:'Orbitron'; font-size:clamp(22px,4vw,46px);
    font-weight:900; color:#fff;
    text-shadow: 0 0 30px rgba(0,229,255,0.6);
    letter-spacing:2px;
    line-height:1.1;
  }
  h1 span { color:var(--cyan); }
  .subtitle {
    margin-top:10px; font-size:15px;
    color:var(--dim); letter-spacing:1px;
  }

  /* ── Layout ── */
  .main {
    max-width:1100px; margin:0 auto;
    padding:0 20px 60px;
    display:flex; flex-direction:column; gap:28px;
  }

  /* ── Cards ── */
  .card {
    background:var(--panel);
    border:1px solid var(--border);
    border-radius:4px;
    padding:24px;
    position:relative;
    overflow:hidden;
  }
  .card::before {
    content:''; position:absolute;
    top:0; left:0; right:0; height:2px;
    background:linear-gradient(90deg, var(--blue), var(--cyan));
  }
  .card-title {
    font-family:'Orbitron'; font-size:12px;
    color:var(--cyan); letter-spacing:3px;
    text-transform:uppercase; margin-bottom:20px;
    display:flex; align-items:center; gap:10px;
  }
  .card-title::after {
    content:''; flex:1; height:1px;
    background:var(--border);
  }

  /* ── Canvas Stage ── */
  #stage {
    width:100%; height:340px;
    display:block; border-radius:2px;
    cursor:default;
  }

  /* ── Controls ── */
  .controls {
    display:grid;
    grid-template-columns: repeat(auto-fit, minmax(200px,1fr));
    gap:16px;
  }
  .ctrl {
    background:#040810;
    border:1px solid var(--border);
    border-radius:3px;
    padding:16px;
  }
  .ctrl-label {
    font-family:'Share Tech Mono'; font-size:10px;
    color:var(--dim); letter-spacing:2px;
    margin-bottom:10px; text-transform:uppercase;
  }
  .ctrl-value {
    font-family:'Orbitron'; font-size:22px;
    color:var(--cyan); margin-bottom:12px;
  }
  .ctrl-value span { font-size:11px; color:var(--dim); }

  input[type=range] {
    -webkit-appearance:none; width:100%; height:3px;
    background:var(--border); border-radius:2px; outline:none;
    cursor:pointer;
  }
  input[type=range]::-webkit-slider-thumb {
    -webkit-appearance:none;
    width:14px; height:14px; border-radius:50%;
    background:var(--cyan);
    box-shadow: var(--glow);
    cursor:pointer;
  }

  .btn-row { display:flex; gap:10px; flex-wrap:wrap; }
  .btn {
    font-family:'Orbitron'; font-size:10px;
    letter-spacing:2px; padding:10px 20px;
    border:1px solid var(--cyan); background:transparent;
    color:var(--cyan); cursor:pointer; border-radius:2px;
    transition:all .2s; text-transform:uppercase;
  }
  .btn:hover, .btn.active {
    background:var(--cyan); color:#000;
    box-shadow:var(--glow);
  }
  .btn.danger { border-color:var(--red); color:var(--red); }
  .btn.danger:hover { background:var(--red); color:#fff; }

  /* ── Phase canvas ── */
  #phaseCanvas {
    width:100%; height:120px; display:block;
  }

  /* ── Info grid ── */
  .info-grid {
    display:grid;
    grid-template-columns:repeat(auto-fit, minmax(220px,1fr));
    gap:16px;
  }
  .info-box {
    background:#040810;
    border:1px solid var(--border);
    border-left:3px solid var(--cyan);
    padding:16px; border-radius:2px;
  }
  .info-box.green  { border-left-color:var(--green); }
  .info-box.orange { border-left-color:var(--orange); }
  .info-box.yellow { border-left-color:var(--yellow); }

  .info-box h3 {
    font-family:'Orbitron'; font-size:11px;
    color:var(--dim); letter-spacing:2px;
    margin-bottom:8px; text-transform:uppercase;
  }
  .info-box p {
    font-size:14px; line-height:1.6;
    color:var(--text);
  }
  .info-box .formula {
    font-family:'Share Tech Mono';
    font-size:15px; color:var(--cyan);
    margin:8px 0; padding:8px;
    background:rgba(0,229,255,0.05);
    border:1px solid rgba(0,229,255,0.15);
    border-radius:2px; display:inline-block;
  }

  /* ── Step-by-step ── */
  .steps { display:flex; flex-direction:column; gap:0; }
  .step {
    display:flex; gap:20px;
    padding:18px 0;
    border-bottom:1px solid var(--border);
    opacity:.4;
    transition:opacity .5s, transform .4s;
  }
  .step.active { opacity:1; }
  .step-num {
    font-family:'Orbitron'; font-size:28px;
    font-weight:900; color:var(--border);
    min-width:44px; line-height:1;
    transition:color .5s;
  }
  .step.active .step-num { color:var(--cyan); text-shadow:var(--glow); }
  .step-body h3 {
    font-family:'Orbitron'; font-size:13px;
    color:#fff; margin-bottom:6px; letter-spacing:1px;
  }
  .step-body p { font-size:14px; line-height:1.6; color:var(--dim); }
  .step.active .step-body p { color:var(--text); }

  /* ── Metrics bar ── */
  .metrics {
    display:flex; gap:24px; flex-wrap:wrap;
    padding:16px;
    background:#040810;
    border:1px solid var(--border);
    border-radius:3px;
  }
  .metric { flex:1; min-width:120px; }
  .metric-label {
    font-family:'Share Tech Mono'; font-size:9px;
    color:var(--dim); letter-spacing:2px;
    text-transform:uppercase; margin-bottom:4px;
  }
  .metric-val {
    font-family:'Orbitron'; font-size:20px;
    color:var(--green); font-weight:700;
  }
  .metric-val.warn { color:var(--orange); }
  .metric-val.danger { color:var(--red); }

  /* ── Legend ── */
  .legend {
    display:flex; gap:20px; flex-wrap:wrap;
    margin-top:12px;
  }
  .leg { display:flex; align-items:center; gap:8px; font-size:13px; }
  .leg-dot {
    width:10px; height:10px; border-radius:50%;
    flex-shrink:0;
  }

  footer {
    text-align:center; padding:24px;
    font-family:'Share Tech Mono'; font-size:10px;
    color:var(--dim); letter-spacing:2px;
    border-top:1px solid var(--border);
  }
</style>
</head>
<body>

<header>
  <div class="tag">EEE-206 · BUET · Section B2 Group 5</div>
  <h1>LINEAR <span>INDUCTION</span> MOTOR</h1>
  <p class="subtitle">Interactive Working Principle Visualizer</p>
</header>

<div class="main">

  <!-- ══ MAIN ANIMATION ══ -->
  <div class="card">
    <div class="card-title">01 · Motor Cross-Section — Live Simulation</div>
    <canvas id="stage"></canvas>
    <div class="legend">
      <div class="leg"><div class="leg-dot" style="background:#ff4444"></div>Phase A (Red)</div>
      <div class="leg"><div class="leg-dot" style="background:#44ff88"></div>Phase B (Green)</div>
      <div class="leg"><div class="leg-dot" style="background:#4488ff"></div>Phase C (Blue)</div>
      <div class="leg"><div class="leg-dot" style="background:#ffe500"></div>Travelling Magnetic Field</div>
      <div class="leg"><div class="leg-dot" style="background:#ff6d00"></div>Induced Eddy Currents</div>
      <div class="leg"><div class="leg-dot" style="background:#00e5ff"></div>Rotor (Aluminium Sheet)</div>
    </div>
  </div>

  <!-- ══ CONTROLS ══ -->
  <div class="card">
    <div class="card-title">02 · Control Panel</div>
    <div class="controls">
      <div class="ctrl">
        <div class="ctrl-label">Supply Frequency</div>
        <div class="ctrl-value" id="freqDisplay">50 <span>Hz</span></div>
        <input type="range" id="freqSlider" min="10" max="100" value="50">
      </div>
      <div class="ctrl">
        <div class="ctrl-label">Pole Configuration</div>
        <div class="ctrl-value" id="poleDisplay">2 <span>Poles</span></div>
        <div class="btn-row" style="margin-top:4px">
          <button class="btn active" id="btn2pole" onclick="setPoles(2)">2-Pole</button>
          <button class="btn" id="btn4pole" onclick="setPoles(4)">4-Pole</button>
        </div>
      </div>
      <div class="ctrl">
        <div class="ctrl-label">Direction</div>
        <div class="ctrl-value" id="dirDisplay">→ <span>Forward</span></div>
        <div class="btn-row" style="margin-top:4px">
          <button class="btn" onclick="reverseDirection()">⇄ Reverse Phase</button>
        </div>
      </div>
      <div class="ctrl">
        <div class="ctrl-label">Simulation</div>
        <div class="ctrl-value" id="stateDisplay">▶ <span>Running</span></div>
        <div class="btn-row" style="margin-top:4px">
          <button class="btn" id="pauseBtn" onclick="togglePause()">⏸ Pause</button>
          <button class="btn danger" onclick="resetSim()">↺ Reset</button>
        </div>
      </div>
    </div>
  </div>

  <!-- ══ LIVE METRICS ══ -->
  <div class="card">
    <div class="card-title">03 · Real-Time Parameters</div>
    <div class="metrics">
      <div class="metric">
        <div class="metric-label">Sync Speed (Vs)</div>
        <div class="metric-val" id="mVs">—</div>
      </div>
      <div class="metric">
        <div class="metric-label">Rotor Speed (v)</div>
        <div class="metric-val" id="mV">—</div>
      </div>
      <div class="metric">
        <div class="metric-label">Slip (s)</div>
        <div class="metric-val" id="mSlip">—</div>
      </div>
      <div class="metric">
        <div class="metric-label">Pole Pitch (τ)</div>
        <div class="metric-val" id="mTau">—</div>
      </div>
      <div class="metric">
        <div class="metric-label">Thrust Force</div>
        <div class="metric-val" id="mForce">—</div>
      </div>
      <div class="metric">
        <div class="metric-label">Frequency</div>
        <div class="metric-val" id="mFreq">—</div>
      </div>
    </div>
  </div>

  <!-- ══ PHASE WAVEFORMS ══ -->
  <div class="card">
    <div class="card-title">04 · Three-Phase Supply Waveforms</div>
    <canvas id="phaseCanvas"></canvas>
  </div>

  <!-- ══ STEP BY STEP ══ -->
  <div class="card">
    <div class="card-title">05 · Working Principle — Step by Step</div>
    <div class="steps">
      <div class="step active" id="s0">
        <div class="step-num">01</div>
        <div class="step-body">
          <h3>Three-Phase AC Supply Energizes the Stator</h3>
          <p>The stator (primary) is connected to a balanced three-phase AC supply. The three coils — Phase A, B, and C — are displaced 120° electrically from each other and carry sinusoidal currents that are 120° apart in time.</p>
        </div>
      </div>
      <div class="step" id="s1">
        <div class="step-num">02</div>
        <div class="step-body">
          <h3>Travelling Magnetic Field is Produced</h3>
          <p>The combined effect of the three displaced currents creates a resultant magnetic field that moves linearly from one end of the stator to the other — the "travelling wave." Its speed is the synchronous speed: <strong>Vs = 2τf</strong>.</p>
        </div>
      </div>
      <div class="step" id="s2">
        <div class="step-num">03</div>
        <div class="step-body">
          <h3>EMF & Eddy Currents Induced in Rotor</h3>
          <p>The moving magnetic field cuts through the aluminium rotor sheet, inducing an EMF by Faraday's Law. This drives eddy currents (shown in orange) circulating within the rotor plate in the plane perpendicular to the field.</p>
        </div>
      </div>
      <div class="step" id="s3">
        <div class="step-num">04</div>
        <div class="step-body">
          <h3>Lenz's Law → Linear Thrust</h3>
          <p>By Lenz's Law, the induced eddy currents create their own magnetic field opposing the change. The interaction between the stator's travelling field and the rotor's induced field produces a linear thrust force, pushing the rotor in the direction of field travel.</p>
        </div>
      </div>
      <div class="step" id="s4">
        <div class="step-num">05</div>
        <div class="step-body">
          <h3>Rotor Moves — Slip Always Exists</h3>
          <p>The rotor accelerates but can never reach synchronous speed (Vs). If it did, there would be no relative motion, no induced EMF, no current, and no thrust. The difference is called <strong>slip: s = (Vs − v) / Vs</strong>.</p>
        </div>
      </div>
      <div class="step" id="s5">
        <div class="step-num">06</div>
        <div class="step-body">
          <h3>Speed & Torque Control</h3>
          <p>Speed is varied by changing frequency or switching between 2-pole and 4-pole configurations. Doubling the poles halves the synchronous speed, doubling the torque (τ = PAG / ωsync). Try the controls above!</p>
        </div>
      </div>
    </div>
  </div>

  <!-- ══ FORMULA CARDS ══ -->
  <div class="card">
    <div class="card-title">06 · Key Equations</div>
    <div class="info-grid">
      <div class="info-box">
        <h3>Synchronous Speed</h3>
        <div class="formula">Vs = 2τf &nbsp;(m/s)</div>
        <p>τ = pole pitch (m), f = frequency (Hz). Not dependent on number of poles — only pole pitch and frequency.</p>
      </div>
      <div class="info-box green">
        <h3>Slip</h3>
        <div class="formula" style="color:var(--green)">s = (Vs − v) / Vs</div>
        <p>LIMs have higher slip than rotary motors due to end effects and larger air gaps, reducing efficiency.</p>
      </div>
      <div class="info-box orange">
        <h3>Magnetic Field Speed</h3>
        <div class="formula" style="color:var(--orange)">nm = 120f / P</div>
        <p>P = number of poles. Changing from 2-pole to 4-pole halves the magnetic field speed.</p>
      </div>
      <div class="info-box yellow">
        <h3>Induced Torque</h3>
        <div class="formula" style="color:var(--yellow)">τ = PAG / ωsync</div>
        <p>PAG = air gap power. At constant PAG, halving ωsync (4-pole) doubles the thrust force.</p>
      </div>
    </div>
  </div>

</div><!-- /main -->

<footer>
  THREE-PHASE LINEAR INDUCTION MOTOR &nbsp;·&nbsp; EEE-206 BUET &nbsp;·&nbsp; SECTION B2 GROUP 5 &nbsp;·&nbsp; 2022
</footer>

<script>
// ════════════════════════════════════════════════════════════
// STATE
// ════════════════════════════════════════════════════════════
let freq       = 50;
let poles      = 2;
let direction  = 1;      // 1 or -1
let paused     = false;
let t          = 0;      // animation time (seconds)
let rotorX     = 0;      // rotor displacement (pixels)
let SLIP       = 0.12;

const POLE_PITCH_PX = 120; // visual pole pitch in pixels

// Computed
function Vs_px() { return direction * 2 * POLE_PITCH_PX * (freq / 50); }
function rotorSpeed_px() { return Vs_px() * (1 - SLIP); }

// ════════════════════════════════════════════════════════════
// MAIN CANVAS
// ════════════════════════════════════════════════════════════
const stage = document.getElementById('stage');
const ctx   = stage.getContext('2d');

function resizeStage() {
  stage.width  = stage.offsetWidth;
  stage.height = stage.offsetHeight;
}

function drawStage(ts) {
  const W = stage.width, H = stage.height;
  ctx.clearRect(0, 0, W, H);

  // Background grid
  ctx.strokeStyle = 'rgba(13,34,64,0.7)';
  ctx.lineWidth = 1;
  for (let x = 0; x < W; x += 40) { ctx.beginPath(); ctx.moveTo(x,0); ctx.lineTo(x,H); ctx.stroke(); }
  for (let y = 0; y < H; y += 40) { ctx.beginPath(); ctx.moveTo(0,y); ctx.lineTo(W,y); ctx.stroke(); }

  const statorTop = H * 0.08;
  const statorH   = H * 0.42;
  const rotorTop  = statorTop + statorH + H * 0.06;
  const rotorH    = H * 0.13;
  const coreH     = statorH * 0.28;

  // ── Stator core (top) ──
  const coreGrad = ctx.createLinearGradient(0, statorTop, 0, statorTop + coreH);
  coreGrad.addColorStop(0,   '#1a2d45');
  coreGrad.addColorStop(0.5, '#0d1f35');
  coreGrad.addColorStop(1,   '#060e1c');
  ctx.fillStyle = coreGrad;
  ctx.fillRect(40, statorTop, W - 80, coreH);
  ctx.strokeStyle = '#0d2240'; ctx.lineWidth = 1;
  ctx.strokeRect(40, statorTop, W - 80, coreH);

  // Lamination lines on core
  ctx.strokeStyle = 'rgba(0,229,255,0.06)'; ctx.lineWidth = 1;
  for (let x = 50; x < W - 50; x += 8) {
    ctx.beginPath(); ctx.moveTo(x, statorTop + 2); ctx.lineTo(x, statorTop + coreH - 2); ctx.stroke();
  }

  // ── Stator slots and coils ──
  const nSlots  = poles * 6;
  const slotW   = (W - 100) / nSlots;
  const slotTop = statorTop + coreH;
  const slotH   = statorH - coreH;

  for (let i = 0; i < nSlots; i++) {
    const sx = 50 + i * slotW;
    const phase = i % 3; // 0=A, 1=B, 2=C
    const phaseAngle = (t * freq * 2 * Math.PI) - (i / nSlots) * poles * Math.PI;
    const curr = Math.sin(phaseAngle + (direction < 0 ? Math.PI : 0));

    // Slot body
    ctx.fillStyle = 'rgba(5,10,18,0.9)';
    ctx.fillRect(sx + 2, slotTop, slotW - 4, slotH - 2);
    ctx.strokeStyle = '#0a1c30'; ctx.lineWidth = 1;
    ctx.strokeRect(sx + 2, slotTop, slotW - 4, slotH - 2);

    // Coil wires - colored by phase
    const colors = ['#ff4444','#44ff88','#4488ff'];
    const alpha  = 0.3 + 0.7 * Math.abs(curr);
    ctx.strokeStyle = colors[phase].replace(')', `,${alpha})`).replace('rgb','rgba').replace('#','rgba(').replace('rgba(','rgba(');
    // simple colored wire representation
    const colRGB = phase===0?`255,68,68`: phase===1?`68,255,136`:`68,136,255`;
    ctx.strokeStyle = `rgba(${colRGB},${alpha})`;
    ctx.lineWidth   = 3;

    // Dot or cross to show current direction
    const cx2 = sx + slotW / 2;
    const cy2 = slotTop + slotH / 2;
    const r   = Math.min(slotW * 0.28, 8);

    ctx.beginPath();
    ctx.arc(cx2, cy2, r, 0, Math.PI * 2);
    ctx.strokeStyle = `rgba(${colRGB},${Math.min(1, alpha + 0.2)})`;
    ctx.fillStyle   = `rgba(${colRGB},0.08)`;
    ctx.fill(); ctx.stroke();

    if (curr > 0.1) {
      // Dot (current toward viewer)
      ctx.beginPath(); ctx.arc(cx2, cy2, r * 0.35, 0, Math.PI * 2);
      ctx.fillStyle = `rgba(${colRGB},${alpha})`; ctx.fill();
    } else if (curr < -0.1) {
      // Cross (current away)
      ctx.beginPath();
      ctx.moveTo(cx2 - r * 0.6, cy2 - r * 0.6); ctx.lineTo(cx2 + r * 0.6, cy2 + r * 0.6);
      ctx.moveTo(cx2 + r * 0.6, cy2 - r * 0.6); ctx.lineTo(cx2 - r * 0.6, cy2 + r * 0.6);
      ctx.strokeStyle = `rgba(${colRGB},${alpha})`; ctx.lineWidth = 2; ctx.stroke();
    }
  }

  // ── Travelling magnetic field ──
  const fieldWave = (x) => {
    const fieldX = ((x / (W - 100)) * poles - t * freq * 0.5 * direction) * Math.PI * 2;
    return Math.sin(fieldX);
  };

  // Field gradient glow between stator bottom and rotor
  const gap = rotorTop - slotTop - slotH + 2;
  const gapY = slotTop + slotH;

  for (let x = 50; x < W - 50; x += 3) {
    const fv    = fieldWave(x - 50);
    const alpha = Math.abs(fv) * 0.55;
    const ySize = gap * 0.7 + Math.abs(fv) * gap * 0.3;
    const grad  = ctx.createLinearGradient(0, gapY, 0, gapY + ySize);
    grad.addColorStop(0,   `rgba(255,229,0,${alpha * 0.8})`);
    grad.addColorStop(0.5, `rgba(255,180,0,${alpha * 0.4})`);
    grad.addColorStop(1,   `rgba(255,120,0,0)`);
    ctx.fillStyle = grad;
    ctx.fillRect(x, gapY, 3, ySize);
  }

  // Field wave line
  ctx.beginPath();
  ctx.lineWidth = 2;
  for (let x = 50; x < W - 50; x++) {
    const fv = fieldWave(x - 50);
    const fy = gapY + gap * 0.5 + fv * gap * 0.4;
    x === 50 ? ctx.moveTo(x, fy) : ctx.lineTo(x, fy);
  }
  ctx.strokeStyle = 'rgba(255,229,0,0.85)';
  ctx.shadowBlur  = 12; ctx.shadowColor = '#ffe500';
  ctx.stroke();
  ctx.shadowBlur = 0;

  // ── Rotor plate ──
  const rx = 40;
  const rw = W - 80;
  const rotorGrad = ctx.createLinearGradient(0, rotorTop, 0, rotorTop + rotorH);
  rotorGrad.addColorStop(0,   '#1a3a5a');
  rotorGrad.addColorStop(0.4, '#0d2a45');
  rotorGrad.addColorStop(1,   '#050f1e');
  ctx.fillStyle = rotorGrad;
  ctx.beginPath();
  ctx.roundRect(rx, rotorTop, rw, rotorH, 3);
  ctx.fill();

  // Rotor border glow
  ctx.strokeStyle = 'rgba(0,229,255,0.6)';
  ctx.lineWidth   = 1.5;
  ctx.shadowBlur  = 10; ctx.shadowColor = '#00e5ff';
  ctx.stroke();
  ctx.shadowBlur = 0;

  // ALUMINIUM label
  ctx.fillStyle   = 'rgba(0,229,255,0.4)';
  ctx.font        = '10px "Share Tech Mono"';
  ctx.letterSpacing = '3px';
  ctx.textAlign   = 'center';
  ctx.fillText('ALUMINIUM ROTOR (SECONDARY)', W / 2, rotorTop + rotorH / 2 + 4);

  // Rotor velocity arrow
  const arrowX = W / 2;
  const arrowY = rotorTop + rotorH + 18;
  const arrowLen = 60 * direction * (1 - SLIP);
  ctx.beginPath();
  ctx.moveTo(arrowX - arrowLen, arrowY);
  ctx.lineTo(arrowX + arrowLen, arrowY);
  const tip = arrowX + arrowLen;
  ctx.moveTo(tip, arrowY);
  ctx.lineTo(tip - 10 * Math.sign(arrowLen), arrowY - 6);
  ctx.moveTo(tip, arrowY);
  ctx.lineTo(tip - 10 * Math.sign(arrowLen), arrowY + 6);
  ctx.strokeStyle = '#00e5ff'; ctx.lineWidth = 2;
  ctx.shadowBlur  = 8; ctx.shadowColor = '#00e5ff';
  ctx.stroke(); ctx.shadowBlur = 0;
  ctx.fillStyle = 'rgba(0,229,255,0.7)';
  ctx.font      = '10px "Share Tech Mono"';
  ctx.fillText('v (rotor)', W / 2, arrowY + 14);

  // ── Eddy currents on rotor ──
  const nEddies = 8;
  for (let i = 0; i < nEddies; i++) {
    const ex   = 80 + ((i / nEddies) * (W - 160) + rotorX * direction * 0.15) % (W - 160);
    const ey   = rotorTop + rotorH * 0.45;
    const fv   = fieldWave(ex - 50);
    const er   = 14 + Math.abs(fv) * 10;
    const ealpha = 0.2 + Math.abs(fv) * 0.6;
    const angle  = t * freq * 2 * Math.PI * 1.5 * direction + i * Math.PI * 2 / nEddies;

    // Elliptical eddy current loop
    ctx.beginPath();
    ctx.ellipse(ex, ey, er, er * 0.45, 0, 0, Math.PI * 2);
    ctx.strokeStyle = `rgba(255,109,0,${ealpha})`;
    ctx.lineWidth   = 1.5;
    ctx.shadowBlur  = 8; ctx.shadowColor = '#ff6d00';
    ctx.stroke(); ctx.shadowBlur = 0;

    // Arrow on eddy current
    const ax = ex + er * Math.cos(angle);
    const ay = ey + er * 0.45 * Math.sin(angle);
    const adx = -Math.sin(angle) * direction;
    const ady = Math.cos(angle) * 0.45;
    const al  = Math.sqrt(adx*adx + ady*ady);
    ctx.beginPath();
    ctx.moveTo(ax, ay);
    ctx.lineTo(ax + (adx/al)*8, ay + (ady/al)*8);
    ctx.strokeStyle = `rgba(255,109,0,${ealpha + 0.1})`;
    ctx.lineWidth = 1.5; ctx.stroke();
  }

  // ── Labels ──
  ctx.font      = '11px "Share Tech Mono"';
  ctx.textAlign = 'left';
  ctx.fillStyle = 'rgba(100,160,220,0.5)';
  ctx.fillText('STATOR (PRIMARY) — LAMINATED CORE + 3Φ WINDINGS', 50, statorTop - 8);

  // ── Synchronous speed arrow ──
  const fArrY = gapY + gap * 0.5;
  const fLen  = 80 * direction;
  const fax   = W * 0.75;
  ctx.beginPath();
  ctx.moveTo(fax - fLen, fArrY);
  ctx.lineTo(fax + fLen, fArrY);
  const ftip = fax + fLen;
  ctx.moveTo(ftip, fArrY);
  ctx.lineTo(ftip - 10 * Math.sign(fLen), fArrY - 7);
  ctx.moveTo(ftip, fArrY);
  ctx.lineTo(ftip - 10 * Math.sign(fLen), fArrY + 7);
  ctx.strokeStyle = 'rgba(255,229,0,0.7)'; ctx.lineWidth = 2;
  ctx.shadowBlur  = 8; ctx.shadowColor = '#ffe500';
  ctx.stroke(); ctx.shadowBlur = 0;
  ctx.fillStyle   = 'rgba(255,229,0,0.7)';
  ctx.font        = '10px "Share Tech Mono"';
  ctx.textAlign   = 'center';
  ctx.fillText('Vs (field)', fax, fArrY - 12);
}

// ════════════════════════════════════════════════════════════
// PHASE WAVEFORM CANVAS
// ════════════════════════════════════════════════════════════
const pCvs = document.getElementById('phaseCanvas');
const pCtx = pCvs.getContext('2d');

function resizePhase() {
  pCvs.width  = pCvs.offsetWidth;
  pCvs.height = pCvs.offsetHeight;
}

function drawPhase() {
  const W = pCvs.width, H = pCvs.height;
  pCtx.clearRect(0, 0, W, H);

  // Grid
  pCtx.strokeStyle = 'rgba(13,34,64,0.6)'; pCtx.lineWidth = 1;
  for (let y = 0; y < H; y += H/4) { pCtx.beginPath(); pCtx.moveTo(0,y); pCtx.lineTo(W,y); pCtx.stroke(); }
  pCtx.strokeStyle = 'rgba(13,34,64,0.4)';
  for (let x = 0; x < W; x += 60) { pCtx.beginPath(); pCtx.moveTo(x,0); pCtx.lineTo(x,H); pCtx.stroke(); }

  // Midline
  pCtx.strokeStyle = 'rgba(0,229,255,0.15)'; pCtx.lineWidth = 1;
  pCtx.beginPath(); pCtx.moveTo(0, H/2); pCtx.lineTo(W, H/2); pCtx.stroke();

  const phases = [
    { offset: 0,              color: '#ff4444', label:'A' },
    { offset: (2*Math.PI/3),  color: '#44ff88', label:'B' },
    { offset: (4*Math.PI/3),  color: '#4488ff', label:'C' },
  ];

  // Current time marker
  const markerX = (W * 0.8);

  phases.forEach(ph => {
    pCtx.beginPath();
    for (let px = 0; px < W; px++) {
      const phT = (t * freq * 2 * Math.PI) - (px / W) * 4 * Math.PI + ph.offset * direction;
      const y   = H/2 - Math.sin(phT) * (H * 0.38);
      px === 0 ? pCtx.moveTo(px, y) : pCtx.lineTo(px, y);
    }
    pCtx.strokeStyle = ph.color; pCtx.lineWidth = 1.8;
    pCtx.shadowBlur  = 6; pCtx.shadowColor = ph.color;
    pCtx.stroke(); pCtx.shadowBlur = 0;

    // Label at right
    const lT = (t * freq * 2 * Math.PI) + ph.offset * direction;
    const ly = H/2 - Math.sin(lT) * (H * 0.38);
    pCtx.fillStyle = ph.color; pCtx.font = '10px "Share Tech Mono"';
    pCtx.textAlign = 'left';
    pCtx.fillText(`φ${ph.label}`, W - 28, ly + 4);
  });

  // Moving time cursor
  const curT = W * ((t * freq * 0.2) % 1);
  pCtx.beginPath();
  pCtx.moveTo(curT, 0); pCtx.lineTo(curT, H);
  pCtx.strokeStyle = 'rgba(0,229,255,0.4)'; pCtx.lineWidth = 1;
  pCtx.setLineDash([4,4]); pCtx.stroke(); pCtx.setLineDash([]);
}

// ════════════════════════════════════════════════════════════
// STEP HIGHLIGHT
// ════════════════════════════════════════════════════════════
let currentStep = 0;
function updateSteps() {
  const step = Math.floor(t * 0.5) % 6;
  if (step !== currentStep) {
    document.getElementById(`s${currentStep}`).classList.remove('active');
    document.getElementById(`s${step}`).classList.add('active');
    currentStep = step;
  }
}

// ════════════════════════════════════════════════════════════
// METRICS UPDATE
// ════════════════════════════════════════════════════════════
function updateMetrics() {
  const tau     = 0.24;        // pole pitch in meters (visual)
  const Vs      = 2 * tau * freq;
  const v       = Vs * (1 - SLIP);
  const slip    = SLIP;
  const force_n = Math.round(Vs * 12 * (1 - SLIP * 0.5));

  const set = (id, val, cls='') => {
    const el = document.getElementById(id);
    el.textContent = val;
    el.className   = 'metric-val ' + cls;
  };

  set('mVs',    Vs.toFixed(2)  + ' m/s');
  set('mV',     v.toFixed(2)   + ' m/s');
  set('mSlip',  (slip * 100).toFixed(1) + ' %', slip > 0.2 ? 'warn' : '');
  set('mTau',   tau.toFixed(2) + ' m');
  set('mForce', force_n        + ' N');
  set('mFreq',  freq            + ' Hz');

  document.getElementById('freqDisplay').innerHTML = freq + ' <span>Hz</span>';
  document.getElementById('poleDisplay').innerHTML = poles + ' <span>Poles</span>';
  const dirTxt = direction > 0 ? '→ <span>Forward</span>' : '← <span>Reverse</span>';
  document.getElementById('dirDisplay').innerHTML = dirTxt;
}

// ════════════════════════════════════════════════════════════
// CONTROLS
// ════════════════════════════════════════════════════════════
document.getElementById('freqSlider').addEventListener('input', e => {
  freq = parseInt(e.target.value);
  updateMetrics();
});

function setPoles(p) {
  poles = p;
  SLIP = p === 4 ? 0.18 : 0.12;
  document.getElementById('btn2pole').classList.toggle('active', p === 2);
  document.getElementById('btn4pole').classList.toggle('active', p === 4);
  updateMetrics();
}

function reverseDirection() {
  direction *= -1;
  updateMetrics();
}

let pauseState = false;
function togglePause() {
  pauseState = !pauseState;
  const btn = document.getElementById('pauseBtn');
  const dis = document.getElementById('stateDisplay');
  btn.textContent = pauseState ? '▶ Resume' : '⏸ Pause';
  dis.innerHTML   = pauseState ? '⏸ <span>Paused</span>' : '▶ <span>Running</span>';
}

function resetSim() {
  t        = 0;
  rotorX   = 0;
  pauseState = false;
  direction  = 1;
  freq       = 50;
  poles      = 2;
  SLIP       = 0.12;
  document.getElementById('freqSlider').value = 50;
  document.getElementById('pauseBtn').textContent = '⏸ Pause';
  document.getElementById('stateDisplay').innerHTML = '▶ <span>Running</span>';
  setPoles(2);
  updateMetrics();
}

// ════════════════════════════════════════════════════════════
// ANIMATION LOOP
// ════════════════════════════════════════════════════════════
let lastTS = null;

function loop(ts) {
  if (!lastTS) lastTS = ts;
  const dt = Math.min((ts - lastTS) / 1000, 0.05);
  lastTS = ts;

  if (!pauseState) {
    t      += dt;
    rotorX += rotorSpeed_px() * dt;
  }

  drawStage(t);
  drawPhase();
  updateSteps();
  requestAnimationFrame(loop);
}

// ════════════════════════════════════════════════════════════
// INIT
// ════════════════════════════════════════════════════════════
window.addEventListener('resize', () => { resizeStage(); resizePhase(); });
resizeStage(); resizePhase();
updateMetrics();
requestAnimationFrame(loop);
</script>
</body>
</html>
