<!DOCTYPE html>

<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Calculadora de Proteína — Método Volta pro Eixo</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400;1,600&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;0,9..40,600;1,9..40,400&display=swap" rel="stylesheet">
<style>
:root {
  --bg:     #FAF7F4;
  --bege:   #F0EAE2;
  --bege2:  #E8DDD3;
  --marrom: #3E1F0E;
  --cafe:   #7B5B3A;
  --linha:  #C4A882;
  --llt:    #DDD0BC;
  --body:   #1A1A1A;
  --cinza:  #888;
  --serif:  'Playfair Display', Georgia, serif;
  --sans:   'DM Sans', system-ui, sans-serif;
  --r: 8px;
  --t: .22s ease;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { font-size: 16px; scroll-behavior: smooth; }

body {
font-family: var(–sans);
background: var(–bg);
color: var(–body);
min-height: 100vh;
}

/* grain texture overlay */
body::before {
content: ‘’;
position: fixed;
inset: 0;
background-image: url(“data:image/svg+xml,%3Csvg viewBox=‘0 0 256 256’ xmlns=‘http://www.w3.org/2000/svg’%3E%3Cfilter id=‘noise’%3E%3CfeTurbulence type=‘fractalNoise’ baseFrequency=‘0.9’ numOctaves=‘4’ stitchTiles=‘stitch’/%3E%3C/filter%3E%3Crect width=‘100%25’ height=‘100%25’ filter=‘url(%23noise)’ opacity=‘0.03’/%3E%3C/svg%3E”);
pointer-events: none;
z-index: 0;
}

/* ─── HEADER ─────────────────────────────────────────────── */
.header {
background: var(–marrom);
padding: 48px 40px 40px;
position: relative;
overflow: hidden;
}
.header::after {
content: ‘’;
position: absolute;
bottom: -1px; left: 0; right: 0;
height: 40px;
background: var(–bg);
clip-path: ellipse(55% 100% at 50% 100%);
}
.header-inner {
max-width: 700px;
margin: 0 auto;
position: relative;
z-index: 1;
}
.header-eyebrow {
font-size: .62rem;
font-weight: 700;
letter-spacing: .18em;
text-transform: uppercase;
color: var(–linha);
margin-bottom: 14px;
display: flex;
align-items: center;
gap: 10px;
}
.header-eyebrow::before {
content: ‘’;
width: 28px;
height: 1px;
background: var(–linha);
}
.header-title {
font-family: var(–serif);
font-size: 2.6rem;
color: #FAF7F4;
line-height: 1.15;
margin-bottom: 14px;
font-weight: 700;
}
.header-title em {
font-style: italic;
color: var(–linha);
}
.header-sub {
font-size: .92rem;
color: rgba(245,240,234,.65);
line-height: 1.7;
max-width: 480px;
}

/* ─── MAIN ───────────────────────────────────────────────── */
.main {
max-width: 700px;
margin: 0 auto;
padding: 48px 40px 80px;
position: relative;
z-index: 1;
}

/* ─── FORM CARD ──────────────────────────────────────────── */
.form-card {
background: #fff;
border-radius: 14px;
padding: 36px;
box-shadow: 0 2px 30px rgba(62,31,14,.07), 0 1px 4px rgba(62,31,14,.04);
border: 1px solid var(–llt);
margin-bottom: 32px;
}

.form-title {
font-family: var(–serif);
font-size: 1.2rem;
color: var(–marrom);
margin-bottom: 28px;
font-weight: 600;
display: flex;
align-items: center;
gap: 10px;
}
.form-title span {
display: inline-flex;
align-items: center;
justify-content: center;
width: 28px;
height: 28px;
border-radius: 50%;
background: var(–marrom);
color: var(–linha);
font-size: .75rem;
font-weight: 700;
font-family: var(–sans);
flex-shrink: 0;
}

/* ─── FIELD ──────────────────────────────────────────────── */
.field { margin-bottom: 24px; }
.field:last-child { margin-bottom: 0; }
.field-label {
display: block;
font-size: .72rem;
font-weight: 700;
letter-spacing: .1em;
text-transform: uppercase;
color: var(–cafe);
margin-bottom: 10px;
}
.field-hint {
font-size: .75rem;
color: var(–cinza);
font-weight: 400;
letter-spacing: 0;
text-transform: none;
margin-left: 6px;
}

/* number input */
.weight-wrap {
display: flex;
align-items: center;
gap: 0;
max-width: 200px;
}
.weight-btn {
width: 44px;
height: 50px;
background: var(–bege);
border: 1.5px solid var(–llt);
color: var(–marrom);
font-size: 1.2rem;
font-weight: 600;
cursor: pointer;
transition: var(–t);
display: flex;
align-items: center;
justify-content: center;
flex-shrink: 0;
user-select: none;
}
.weight-btn:first-child { border-radius: var(–r) 0 0 var(–r); }
.weight-btn:last-child { border-radius: 0 var(–r) var(–r) 0; }
.weight-btn:hover { background: var(–marrom); color: var(–linha); border-color: var(–marrom); }
.weight-input {
flex: 1;
height: 50px;
border: 1.5px solid var(–llt);
border-left: none;
border-right: none;
background: #fff;
text-align: center;
font-family: var(–serif);
font-size: 1.4rem;
font-weight: 600;
color: var(–marrom);
outline: none;
min-width: 0;
-moz-appearance: textfield;
}
.weight-input::-webkit-inner-spin-button,
.weight-input::-webkit-outer-spin-button { display: none; }
.weight-input:focus { border-color: var(–linha); background: #fffdf9; }
.weight-unit {
font-size: .7rem;
font-weight: 600;
color: var(–cinza);
letter-spacing: .08em;
padding-left: 8px;
}

/* option grid */
.opt-grid {
display: grid;
gap: 8px;
}
.opt-grid.cols-3 { grid-template-columns: repeat(3, 1fr); }
.opt-grid.cols-2 { grid-template-columns: repeat(2, 1fr); }

.opt-item {
position: relative;
cursor: pointer;
}
.opt-item input[type=“radio”] {
position: absolute;
opacity: 0;
width: 0;
height: 0;
}
.opt-face {
display: flex;
flex-direction: column;
align-items: center;
justify-content: center;
gap: 7px;
padding: 14px 10px;
border: 1.5px solid var(–llt);
border-radius: var(–r);
background: var(–bege);
transition: var(–t);
text-align: center;
cursor: pointer;
}
.opt-face:hover { border-color: var(–linha); background: #fff8f2; }
.opt-item input:checked + .opt-face {
border-color: var(–marrom);
background: #fff8f2;
box-shadow: inset 0 0 0 1px var(–marrom);
}
.opt-icon { font-size: 1.3rem; }
.opt-name {
font-size: .78rem;
font-weight: 600;
color: var(–marrom);
line-height: 1.3;
}
.opt-desc {
font-size: .68rem;
color: var(–cinza);
line-height: 1.4;
}
.opt-item input:checked + .opt-face .opt-name { color: var(–marrom); }

/* ─── CTA BUTTON ─────────────────────────────────────────── */
.calc-btn {
width: 100%;
padding: 18px;
background: var(–marrom);
color: var(–linha);
border: none;
border-radius: var(–r);
font-family: var(–sans);
font-size: .95rem;
font-weight: 700;
letter-spacing: .06em;
text-transform: uppercase;
cursor: pointer;
transition: var(–t);
margin-top: 28px;
position: relative;
overflow: hidden;
}
.calc-btn::after {
content: ‘’;
position: absolute;
inset: 0;
background: linear-gradient(90deg, transparent, rgba(255,255,255,.08), transparent);
transform: translateX(-100%);
transition: .5s ease;
}
.calc-btn:hover { background: var(–cafe); }
.calc-btn:hover::after { transform: translateX(100%); }

/* ─── RESULT ─────────────────────────────────────────────── */
#result {
display: none;
animation: slideUp .5s cubic-bezier(.16,1,.3,1) both;
}
#result.show { display: block; }

@keyframes slideUp {
from { opacity: 0; transform: translateY(24px); }
to   { opacity: 1; transform: translateY(0); }
}

/* hero result */
.result-hero {
background: var(–marrom);
border-radius: 14px;
padding: 36px;
text-align: center;
margin-bottom: 20px;
position: relative;
overflow: hidden;
}
.result-hero::before {
content: ‘’;
position: absolute;
top: -60px; right: -60px;
width: 200px; height: 200px;
border-radius: 50%;
background: rgba(196,168,130,.06);
}
.result-hero::after {
content: ‘’;
position: absolute;
bottom: -40px; left: -40px;
width: 160px; height: 160px;
border-radius: 50%;
background: rgba(196,168,130,.04);
}
.result-label {
font-size: .62rem;
font-weight: 700;
letter-spacing: .16em;
text-transform: uppercase;
color: rgba(196,168,130,.7);
margin-bottom: 10px;
}
.result-number {
font-family: var(–serif);
font-size: 5rem;
color: var(–linha);
line-height: 1;
font-weight: 700;
margin-bottom: 4px;
position: relative;
z-index: 1;
}
.result-unit {
font-size: 1.8rem;
font-weight: 400;
color: rgba(196,168,130,.6);
}
.result-subline {
font-size: .85rem;
color: rgba(245,240,234,.6);
margin-top: 8px;
line-height: 1.6;
}
.result-range {
display: inline-block;
margin-top: 14px;
padding: 7px 18px;
background: rgba(196,168,130,.12);
border: 1px solid rgba(196,168,130,.2);
border-radius: 99px;
font-size: .72rem;
color: var(–linha);
font-weight: 600;
letter-spacing: .06em;
position: relative;
z-index: 1;
}

/* ─── INFO PILLS ─────────────────────────────────────────── */
.info-row {
display: grid;
grid-template-columns: repeat(3, 1fr);
gap: 10px;
margin-bottom: 20px;
}
.info-pill {
background: var(–bege);
border-radius: var(–r);
padding: 14px 12px;
text-align: center;
border: 1px solid var(–llt);
}
.info-pill-label {
font-size: .58rem;
font-weight: 700;
letter-spacing: .12em;
text-transform: uppercase;
color: var(–linha);
margin-bottom: 5px;
}
.info-pill-val {
font-size: .92rem;
font-weight: 600;
color: var(–marrom);
line-height: 1.3;
}

/* ─── DAY PLAN ───────────────────────────────────────────── */
.section-title {
font-family: var(–serif);
font-size: 1.25rem;
color: var(–marrom);
font-weight: 600;
margin: 28px 0 16px;
display: flex;
align-items: center;
gap: 12px;
}
.section-title::after {
content: ‘’;
flex: 1;
height: 1px;
background: var(–llt);
}

.meal-card {
background: #fff;
border-radius: var(–r);
border: 1px solid var(–llt);
margin-bottom: 10px;
overflow: hidden;
transition: box-shadow var(–t);
}
.meal-card:hover { box-shadow: 0 4px 20px rgba(62,31,14,.07); }

.meal-header {
display: flex;
align-items: center;
gap: 14px;
padding: 14px 18px;
cursor: pointer;
user-select: none;
}
.meal-dot {
width: 8px;
height: 8px;
border-radius: 50%;
background: var(–linha);
flex-shrink: 0;
}
.meal-name {
font-size: .8rem;
font-weight: 700;
text-transform: uppercase;
letter-spacing: .08em;
color: var(–cafe);
flex: 1;
}
.meal-prot {
font-family: var(–serif);
font-size: 1.05rem;
font-weight: 600;
color: var(–marrom);
}
.meal-prot-unit { font-size: .7rem; color: var(–cinza); margin-left: 2px; }
.meal-arrow {
color: var(–linha);
font-size: .8rem;
transition: transform var(–t);
}
.meal-card.open .meal-arrow { transform: rotate(90deg); }

.meal-body {
display: none;
padding: 0 18px 16px;
border-top: 1px solid var(–bege2);
}
.meal-card.open .meal-body { display: block; }

.meal-options { display: flex; flex-direction: column; gap: 8px; margin-top: 12px; }
.meal-opt {
display: flex;
gap: 12px;
padding: 11px 14px;
background: var(–bege);
border-radius: 6px;
align-items: flex-start;
border-left: 3px solid transparent;
}
.meal-opt:nth-child(1) { border-left-color: var(–marrom); }
.meal-opt:nth-child(2) { border-left-color: var(–cafe); }
.meal-opt:nth-child(3) { border-left-color: var(–linha); }
.meal-opt-letter {
font-family: var(–serif);
font-size: 1rem;
font-weight: 700;
color: var(–marrom);
flex-shrink: 0;
width: 16px;
margin-top: 1px;
}
.meal-opt:nth-child(2) .meal-opt-letter { color: var(–cafe); }
.meal-opt:nth-child(3) .meal-opt-letter { color: var(–linha); }
.meal-opt-content { flex: 1; }
.meal-opt-name { font-size: .85rem; font-weight: 600; color: var(–marrom); margin-bottom: 2px; }
.meal-opt-desc { font-size: .8rem; color: var(–body); line-height: 1.5; }
.meal-opt-macro { font-size: .7rem; font-weight: 600; color: var(–cafe); margin-top: 4px; }

/* ─── PROGRESS BAR ───────────────────────────────────────── */
.prot-progress {
background: var(–bege);
border-radius: var(–r);
padding: 20px 22px;
margin-bottom: 20px;
border: 1px solid var(–llt);
}
.pp-top {
display: flex;
justify-content: space-between;
align-items: flex-end;
margin-bottom: 12px;
}
.pp-label { font-size: .72rem; font-weight: 700; letter-spacing: .1em; text-transform: uppercase; color: var(–cafe); }
.pp-total { font-family: var(–serif); font-size: 1.1rem; font-weight: 600; color: var(–marrom); }
.pp-bar-bg {
height: 8px;
background: var(–bege2);
border-radius: 99px;
overflow: hidden;
}
.pp-bar-fill {
height: 100%;
background: linear-gradient(90deg, var(–marrom), var(–cafe));
border-radius: 99px;
transition: width 1s cubic-bezier(.16,1,.3,1);
width: 0%;
}
.pp-segments {
display: flex;
gap: 6px;
margin-top: 10px;
flex-wrap: wrap;
}
.pp-seg {
font-size: .68rem;
color: var(–cinza);
background: #fff;
border: 1px solid var(–llt);
border-radius: 99px;
padding: 3px 10px;
font-weight: 500;
}
.pp-seg b { color: var(–marrom); }

/* ─── TIPS ───────────────────────────────────────────────── */
.tip-card {
background: var(–marrom);
border-radius: var(–r);
padding: 20px 22px;
margin-top: 24px;
}
.tip-card p {
font-family: var(–serif);
font-style: italic;
font-size: .95rem;
color: var(–linha);
line-height: 1.7;
}

/* ─── CALLOUT ────────────────────────────────────────────── */
.callout {
background: var(–bege);
border-left: 3px solid var(–marrom);
border-radius: 0 var(–r) var(–r) 0;
padding: 14px 18px;
margin-top: 24px;
}
.callout p {
font-size: .85rem;
color: var(–marrom);
line-height: 1.65;
}

/* ─── FOOTER ─────────────────────────────────────────────── */
.footer {
text-align: center;
padding: 24px 40px 40px;
font-size: .72rem;
color: var(–cinza);
max-width: 700px;
margin: 0 auto;
}
.footer strong { color: var(–cafe); }

/* ─── RESPONSIVE ─────────────────────────────────────────── */
@media (max-width: 600px) {
.header { padding: 36px 22px 36px; }
.header-title { font-size: 1.9rem; }
.main { padding: 32px 18px 60px; }
.form-card { padding: 24px 18px; }
.result-hero { padding: 28px 18px; }
.result-number { font-size: 4rem; }
.opt-grid.cols-3 { grid-template-columns: 1fr; }
.info-row { grid-template-columns: 1fr; }
}
</style>

</head>
<body>

<!-- HEADER -->

<div class="header">
  <div class="header-inner">
    <div class="header-eyebrow">Método Volta pro Eixo · Vic</div>
    <h1 class="header-title">Calculadora de<br><em>Proteína Diária</em></h1>
    <p class="header-sub">Descubra sua meta personalizada de proteína e veja exatamente como bater esse número no seu dia a dia — com os alimentos que você já tem em casa.</p>
  </div>
</div>

<!-- MAIN -->

<div class="main">

  <!-- FORM -->

  <div class="form-card">
    <div class="form-title">
      <span>1</span>
      Suas informações
    </div>

```
<!-- PESO -->
<div class="field">
  <label class="field-label">Seu peso atual <span class="field-hint">em kg</span></label>
  <div class="weight-wrap">
    <button class="weight-btn" onclick="changeWeight(-1)" type="button">−</button>
    <input type="number" class="weight-input" id="weightInput" value="65" min="35" max="180">
    <button class="weight-btn" onclick="changeWeight(1)" type="button">+</button>
    <span class="weight-unit">KG</span>
  </div>
</div>

<!-- OBJETIVO -->
<div class="field">
  <label class="field-label">Seu objetivo principal</label>
  <div class="opt-grid cols-3">
    <label class="opt-item">
      <input type="radio" name="objetivo" value="perda" checked>
      <div class="opt-face">
        <div class="opt-icon">⬇️</div>
        <div class="opt-name">Perder peso</div>
        <div class="opt-desc">com preservação muscular</div>
      </div>
    </label>
    <label class="opt-item">
      <input type="radio" name="objetivo" value="manutencao">
      <div class="opt-face">
        <div class="opt-icon">⚖️</div>
        <div class="opt-name">Manter peso</div>
        <div class="opt-desc">composição corporal</div>
      </div>
    </label>
    <label class="opt-item">
      <input type="radio" name="objetivo" value="ganho">
      <div class="opt-face">
        <div class="opt-icon">💪</div>
        <div class="opt-name">Ganhar massa</div>
        <div class="opt-desc">hipertrofia muscular</div>
      </div>
    </label>
  </div>
</div>

<!-- ATIVIDADE -->
<div class="field">
  <label class="field-label">Nível de atividade física</label>
  <div class="opt-grid cols-2">
    <label class="opt-item">
      <input type="radio" name="atividade" value="sedentario">
      <div class="opt-face">
        <div class="opt-icon">🛋️</div>
        <div class="opt-name">Sedentária</div>
        <div class="opt-desc">sem exercício regular</div>
      </div>
    </label>
    <label class="opt-item">
      <input type="radio" name="atividade" value="leve" checked>
      <div class="opt-face">
        <div class="opt-icon">🚶‍♀️</div>
        <div class="opt-name">Levemente ativa</div>
        <div class="opt-desc">caminhada ou 1–2x/sem</div>
      </div>
    </label>
    <label class="opt-item">
      <input type="radio" name="atividade" value="moderada">
      <div class="opt-face">
        <div class="opt-icon">🏋️‍♀️</div>
        <div class="opt-name">Moderadamente ativa</div>
        <div class="opt-desc">3–4x por semana</div>
      </div>
    </label>
    <label class="opt-item">
      <input type="radio" name="atividade" value="intensa">
      <div class="opt-face">
        <div class="opt-icon">🔥</div>
        <div class="opt-name">Muito ativa</div>
        <div class="opt-desc">5+ vezes por semana</div>
      </div>
    </label>
  </div>
</div>

<button class="calc-btn" onclick="calcular()">CALCULAR MINHA META →</button>
```

  </div>

  <!-- RESULTADO -->

  <div id="result">

```
<!-- HERO NUMBER -->
<div class="result-hero">
  <div class="result-label">Sua meta diária de proteína</div>
  <div class="result-number" id="resultNum">0<span class="result-unit">g</span></div>
  <div class="result-subline" id="resultSubline">de proteína por dia</div>
  <div class="result-range" id="resultRange">Faixa recomendada: 90g – 120g/dia</div>
</div>

<!-- INFO PILLS -->
<div class="info-row">
  <div class="info-pill">
    <div class="info-pill-label">Por kg de peso</div>
    <div class="info-pill-val" id="pillPorKg">1.8g / kg</div>
  </div>
  <div class="info-pill">
    <div class="info-pill-label">Por refeição</div>
    <div class="info-pill-val" id="pillPorRefeicao">~25g cada</div>
  </div>
  <div class="info-pill">
    <div class="info-pill-label">Calorias de prot.</div>
    <div class="info-pill-val" id="pillKcal">~400 kcal</div>
  </div>
</div>

<!-- BARRA DISTRIBUIÇÃO -->
<div class="prot-progress">
  <div class="pp-top">
    <div class="pp-label">Como distribuir ao longo do dia</div>
    <div class="pp-total" id="ppTotal">4 refeições</div>
  </div>
  <div class="pp-bar-bg">
    <div class="pp-bar-fill" id="ppFill"></div>
  </div>
  <div class="pp-segments" id="ppSegs"></div>
</div>

<!-- PLANO DO DIA -->
<div class="section-title">Como bater sua meta hoje</div>

<!-- Café da manhã -->
<div class="meal-card" id="mc-cafe">
  <div class="meal-header" onclick="toggleMeal('mc-cafe')">
    <div class="meal-dot"></div>
    <div class="meal-name">Café da manhã</div>
    <div class="meal-prot" id="mp-cafe">—<span class="meal-prot-unit">g</span></div>
    <div class="meal-arrow">›</div>
  </div>
  <div class="meal-body" id="mb-cafe"></div>
</div>

<!-- Almoço -->
<div class="meal-card" id="mc-almoco">
  <div class="meal-header" onclick="toggleMeal('mc-almoco')">
    <div class="meal-dot"></div>
    <div class="meal-name">Almoço</div>
    <div class="meal-prot" id="mp-almoco">—<span class="meal-prot-unit">g</span></div>
    <div class="meal-arrow">›</div>
  </div>
  <div class="meal-body" id="mb-almoco"></div>
</div>

<!-- Lanche -->
<div class="meal-card" id="mc-lanche">
  <div class="meal-header" onclick="toggleMeal('mc-lanche')">
    <div class="meal-dot"></div>
    <div class="meal-name">Lanche</div>
    <div class="meal-prot" id="mp-lanche">—<span class="meal-prot-unit">g</span></div>
    <div class="meal-arrow">›</div>
  </div>
  <div class="meal-body" id="mb-lanche"></div>
</div>

<!-- Jantar -->
<div class="meal-card" id="mc-jantar">
  <div class="meal-header" onclick="toggleMeal('mc-jantar')">
    <div class="meal-dot"></div>
    <div class="meal-name">Jantar</div>
    <div class="meal-prot" id="mp-jantar">—<span class="meal-prot-unit">g</span></div>
    <div class="meal-arrow">›</div>
  </div>
  <div class="meal-body" id="mb-jantar"></div>
</div>

<!-- LEMBRETE -->
<div class="callout">
  <p>💡 <strong>Dica:</strong> você não precisa bater a meta com perfeição todos os dias. O objetivo é criar um padrão consistente — proteína em todas as refeições principais, semana após semana. Isso já é suficiente pra mover o ponteiro.</p>
</div>

<div class="tip-card">
  <p>"Não conta a semana perfeita. Conta a semana razoável repetida."</p>
</div>

<!-- RECALCULAR -->
<button class="calc-btn" onclick="recalcular()" style="margin-top:24px;background:transparent;color:var(--cafe);border:1.5px solid var(--llt);">↩ Recalcular</button>
```

  </div>
</div>

<!-- FOOTER -->

<div class="footer">
  <p>Calculadora baseada em evidências. Referências: <strong>ISSN Position Stand on Protein (2017)</strong> · <strong>Morton et al. (2018)</strong> · <strong>Stokes et al. (2018)</strong>.<br>
  Este material é educativo e não substitui avaliação nutricional individualizada.</p>
  <p style="margin-top:8px">© Método Volta pro Eixo · <strong>Vic</strong></p>
</div>

<script>
// ─── DADOS ───────────────────────────────────────────────────────────────────

// Fator por objetivo: [min g/kg, max g/kg, central g/kg]
const objetivoFatores = {
  perda:      [1.6, 2.2, 1.9],
  manutencao: [1.4, 1.8, 1.6],
  ganho:      [1.8, 2.4, 2.1]
};

// Multiplicador de atividade (sobre fator central)
const atividadeMult = {
  sedentario: 0.92,
  leve:       1.0,
  moderada:   1.08,
  intensa:    1.16
};

// Labels de objetivo
const objetivoLabels = {
  perda:      'Emagrecimento com preservação muscular',
  manutencao: 'Manutenção da composição corporal',
  ganho:      'Hipertrofia e ganho de massa'
};

// Banco de opções por refeição (cada grupo com 3 opções A/B/C)
// Proteína em gramas por opção
const mealsDB = {
  cafe: [
    { nome: '3 ovos mexidos + pão + fruta', prot: 22, desc: '3 ovos mexidos + 1 fatia pão integral + 1 fruta da estação', macro: '~22g prot · ~26g carb · ~310kcal' },
    { nome: 'Yopro + ½ scoop whey + aveia', prot: 32, desc: 'Yopro (1 pote 160g) + ½ scoop whey + aveia (2 col.) + frutas vermelhas', macro: '~32g prot · ~24g carb · ~275kcal' },
    { nome: 'Crepioca recheada', prot: 26, desc: '2 ovos + 3 col. tapioca granulada — frango desfiado (60g) + creme de ricota light', macro: '~26g prot · ~22g carb · ~300kcal' }
  ],
  almoco: [
    { nome: 'Prato base clássico', prot: 37, desc: 'Frango grelhado (120g) + arroz integral (1 punho) + feijão (½ concha) + salada + azeite', macro: '~37g prot · ~42g carb · ~395kcal' },
    { nome: 'Bowl de peixe', prot: 34, desc: 'Tilápia grelhada (120g) + batata-doce (1 punho) + brócolis refogado + azeite', macro: '~34g prot · ~36g carb · ~355kcal' },
    { nome: 'Atum com quinoa e salada', prot: 36, desc: 'Atum (1 lata 170g) + quinoa cozida (1 punho) + folhas + tomate + pepino + azeite', macro: '~36g prot · ~32g carb · ~345kcal' }
  ],
  lanche: [
    { nome: 'Whey + banana', prot: 23, desc: 'Whey protein (1 scoop) em água ou leite 200ml + 1 banana média', macro: '~23g prot · ~28g carb · ~225kcal' },
    { nome: 'Yopro + fruta', prot: 25, desc: 'Yopro (1 pote 160g) + 1 fruta da estação', macro: '~25g prot · ~18g carb · ~195kcal' },
    { nome: 'Cottage + fruta + castanhas', prot: 20, desc: 'Queijo cottage (4 col. sopa) + 1 fruta + 4 castanhas-do-Pará', macro: '~20g prot · ~16g carb · ~230kcal' }
  ],
  jantar: [
    { nome: 'Omelete + Rap10', prot: 28, desc: 'Omelete (3 ovos) + espinafre + creme de ricota light (2 col.) + 1 Rap10 + salada', macro: '~28g prot · ~26g carb · ~355kcal' },
    { nome: 'Frango + arroz + legumes', prot: 35, desc: 'Frango desfiado (100g) + arroz integral (1 punho) + abobrinha refogada + cenoura + azeite', macro: '~35g prot · ~30g carb · ~340kcal' },
    { nome: 'Atum + batata-doce + salada', prot: 30, desc: 'Atum (1 lata) + batata-doce (1 punho) + mix de folhas + tomate + azeite', macro: '~30g prot · ~34g carb · ~315kcal' }
  ]
};

// ─── LÓGICA ───────────────────────────────────────────────────────────────────

function changeWeight(delta) {
  const inp = document.getElementById('weightInput');
  let val = parseInt(inp.value) + delta;
  val = Math.min(180, Math.max(35, val));
  inp.value = val;
}

function recalcular() {
  document.getElementById('result').classList.remove('show');
  window.scrollTo({ top: 0, behavior: 'smooth' });
  setTimeout(() => {
    document.getElementById('result').style.display = 'none';
  }, 400);
}

function calcular() {
  const peso = parseFloat(document.getElementById('weightInput').value) || 65;
  const obj = document.querySelector('input[name="objetivo"]:checked')?.value || 'perda';
  const atv = document.querySelector('input[name="atividade"]:checked')?.value || 'leve';

  const [minF, maxF, cenF] = objetivoFatores[obj];
  const mult = atividadeMult[atv];

  const meta   = Math.round(peso * cenF * mult);
  const minMeta = Math.round(peso * minF);
  const maxMeta = Math.round(peso * maxF * mult);
  const porKg  = (meta / peso).toFixed(1);
  const kcalProt = meta * 4;

  // distribui: café 25%, almoço 35%, lanche 20%, jantar 20%
  const dist = { cafe: .25, almoco: .35, lanche: .20, jantar: .20 };
  const metas = {
    cafe:   Math.round(meta * dist.cafe),
    almoco: Math.round(meta * dist.almoco),
    lanche: Math.round(meta * dist.lanche),
    jantar: Math.round(meta * dist.jantar)
  };

  // anima número
  animateNumber('resultNum', meta, 'g');

  document.getElementById('resultSubline').textContent =
    `${objetivoLabels[obj]} · ${peso}kg`;
  document.getElementById('resultRange').textContent =
    `Faixa recomendada: ${minMeta}g – ${maxMeta}g / dia`;
  document.getElementById('pillPorKg').textContent = `${porKg}g / kg`;
  document.getElementById('pillPorRefeicao').textContent = `~${Math.round(meta/4)}g cada`;
  document.getElementById('pillKcal').textContent = `~${kcalProt} kcal`;

  // barra
  document.getElementById('ppTotal').textContent = '4 refeições';
  const segs = [
    { label: 'Café', g: metas.cafe },
    { label: 'Almoço', g: metas.almoco },
    { label: 'Lanche', g: metas.lanche },
    { label: 'Jantar', g: metas.jantar }
  ];
  document.getElementById('ppSegs').innerHTML = segs
    .map(s => `<div class="pp-seg"><b>${s.g}g</b> ${s.label}</div>`).join('');
  setTimeout(() => {
    document.getElementById('ppFill').style.width = '100%';
  }, 500);

  // refeições
  renderMeal('cafe',   metas.cafe,   mealsDB.cafe);
  renderMeal('almoco', metas.almoco, mealsDB.almoco);
  renderMeal('lanche', metas.lanche, mealsDB.lanche);
  renderMeal('jantar', metas.jantar, mealsDB.jantar);

  // abre primeiro card automaticamente
  document.getElementById('mc-cafe').classList.remove('open');
  document.getElementById('mb-cafe').style.display = '';

  // mostra resultado
  const res = document.getElementById('result');
  res.classList.remove('show');
  res.style.display = 'block';
  requestAnimationFrame(() => {
    requestAnimationFrame(() => {
      res.classList.add('show');
      setTimeout(() => {
        res.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }, 100);
    });
  });
}

function renderMeal(id, metaG, options) {
  document.getElementById('mp-'+id).innerHTML = `${metaG}<span class="meal-prot-unit">g</span>`;

  // escolhe opção mais próxima da meta
  const best = options.reduce((a, b) =>
    Math.abs(a.prot - metaG) <= Math.abs(b.prot - metaG) ? a : b
  );
  const idx = options.indexOf(best);
  const letters = ['A','B','C'];

  const html = `
    <div style="font-size:.75rem;color:var(--cinza);margin-top:12px;margin-bottom:4px;">
      💡 Opção mais próxima da sua meta destacada — mas todas funcionam.
    </div>
    <div class="meal-options">
      ${options.map((o, i) => `
        <div class="meal-opt" style="${i===idx?'background:#fff8f0;':''}">
          <div class="meal-opt-letter">${letters[i]}</div>
          <div class="meal-opt-content">
            <div class="meal-opt-name">${o.nome} ${i===idx ? '<span style="font-size:.65rem;color:var(--linha);font-weight:700;margin-left:6px;letter-spacing:.06em">✓ RECOMENDADA</span>' : ''}</div>
            <div class="meal-opt-desc">${o.desc}</div>
            <div class="meal-opt-macro">${o.macro}</div>
          </div>
        </div>
      `).join('')}
    </div>
  `;
  document.getElementById('mb-'+id).innerHTML = html;
}

function toggleMeal(id) {
  const card = document.getElementById(id);
  const body = card.querySelector('.meal-body');
  const isOpen = card.classList.contains('open');
  // fecha todos
  document.querySelectorAll('.meal-card').forEach(c => {
    c.classList.remove('open');
    c.querySelector('.meal-body').style.display = '';
  });
  if (!isOpen) {
    card.classList.add('open');
    body.style.display = 'block';
  }
}

function animateNumber(id, target, suffix) {
  const el = document.getElementById(id);
  const start = 0;
  const duration = 900;
  const startTime = performance.now();
  function step(now) {
    const elapsed = now - startTime;
    const progress = Math.min(elapsed / duration, 1);
    const ease = 1 - Math.pow(1 - progress, 3);
    const current = Math.round(start + (target - start) * ease);
    el.innerHTML = `${current}<span class="result-unit">${suffix}</span>`;
    if (progress < 1) requestAnimationFrame(step);
  }
  requestAnimationFrame(step);
}

// Enter key
document.addEventListener('keydown', e => {
  if (e.key === 'Enter') calcular();
});
</script>

</body>
</html>
