<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MS SALES JEOPARDY</title>
<link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&family=Orbitron:wght@400;700;900&family=Exo+2:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
:root {
  --bg:#000816;
  --board-bg:#00008b;
  --cell:#0000cd;
  --cell-hover:#1a1aee;
  --cell-done:#001040;
  --gold:#ffd700;
  --cyan:#00e5ff;
  --magenta:#ff00cc;
  --green:#00ff88;
  --red:#ff2244;
  --white:#e8f8ff;
  --dim:#0a2a5a;
  --muted:#1a4a7a;
  --text-dim:#3a6a9a;
  --ff-arcade:'Press Start 2P',monospace;
  --ff-hud:'Orbitron',sans-serif;
  --ff-body:'Exo 2',sans-serif;
}
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box;}
html{font-size:16px;}
body{font-family:var(--ff-body);background:var(--bg);color:var(--white);min-height:100vh;overflow-x:hidden;}

/* SCANLINES */
body::before{content:'';position:fixed;inset:0;z-index:999;pointer-events:none;
background:repeating-linear-gradient(0deg,transparent,transparent 3px,rgba(0,0,0,0.12) 3px,rgba(0,0,0,0.12) 4px);}

/* STARS */
#stars{position:fixed;inset:0;z-index:0;}
.star{position:absolute;border-radius:50%;background:#fff;animation:twinkle linear infinite;}
@keyframes twinkle{0%,100%{opacity:.15;}50%{opacity:.8;}}

/* GRID BG */
.gbg{position:fixed;inset:0;z-index:1;pointer-events:none;
background-image:linear-gradient(rgba(0,80,255,0.04) 1px,transparent 1px),linear-gradient(90deg,rgba(0,80,255,0.04) 1px,transparent 1px);
background-size:60px 60px;}

/* APP */
.app{position:relative;z-index:10;min-height:100vh;display:flex;flex-direction:column;align-items:center;padding:16px;}

/* SCREENS */
.screen{display:none;flex-direction:column;align-items:center;width:100%;}
.screen.on{display:flex;animation:sIn .35s ease;}
@keyframes sIn{from{opacity:0;transform:scale(.97);}to{opacity:1;transform:scale(1);}}

/* ── TITLE ── */
.title-bar{text-align:center;margin-bottom:20px;}
.t1{font-family:var(--ff-arcade);font-size:clamp(14px,3vw,24px);color:var(--gold);
text-shadow:0 0 10px var(--gold),0 0 30px var(--gold);animation:pulse 2s ease-in-out infinite;letter-spacing:2px;}
.t2{font-family:var(--ff-hud);font-size:11px;color:var(--cyan);letter-spacing:6px;margin-top:6px;
text-shadow:0 0 8px var(--cyan);}
@keyframes pulse{0%,100%{text-shadow:0 0 10px var(--gold),0 0 30px var(--gold);}
50%{text-shadow:0 0 6px var(--gold),0 0 15px var(--gold),0 0 60px var(--gold);}}

/* ── HUD ── */
.hud{width:100%;max-width:1100px;display:flex;align-items:center;gap:16px;
margin-bottom:16px;flex-wrap:wrap;justify-content:space-between;}
.hud-team{font-family:var(--ff-arcade);font-size:10px;color:var(--cyan);
border:1px solid var(--cyan);padding:8px 16px;background:rgba(0,229,255,.06);
text-shadow:0 0 8px var(--cyan);}
.hud-score-wrap{text-align:center;}
.hud-score-label{font-family:var(--ff-hud);font-size:9px;color:var(--text-dim);letter-spacing:3px;}
.hud-score{font-family:var(--ff-arcade);font-size:clamp(16px,3vw,26px);color:var(--gold);
text-shadow:0 0 12px var(--gold);}
.hud-pts-bar{display:flex;align-items:center;gap:8px;flex-direction:column;}
.hud-pts-label{font-family:var(--ff-arcade);font-size:8px;color:var(--text-dim);letter-spacing:2px;}
.pts-track{width:200px;height:14px;background:var(--dim);border:1px solid var(--muted);position:relative;overflow:hidden;}
.pts-fill{height:100%;background:linear-gradient(90deg,var(--board-bg),var(--cyan),var(--gold));transition:width .8s ease;}
.pts-goal{font-family:var(--ff-arcade);font-size:8px;color:var(--gold);margin-top:3px;}

/* ── BOARD ── */
.board-wrap{width:100%;max-width:1100px;overflow-x:auto;margin-bottom:20px;}
.board{display:grid;grid-template-columns:repeat(9,1fr);gap:4px;min-width:800px;}

/* Category headers */
.cat-header{background:var(--board-bg);border:2px solid #0000ff;
padding:10px 6px;text-align:center;
font-family:var(--ff-arcade);font-size:clamp(6px,1vw,9px);color:var(--gold);
line-height:1.5;letter-spacing:.5px;min-height:60px;
display:flex;align-items:center;justify-content:center;
text-shadow:0 0 6px var(--gold);
box-shadow:inset 0 0 10px rgba(0,0,255,.3);}

/* Value cells */
.cell{background:var(--cell);border:2px solid #0000ff;
min-height:70px;display:flex;align-items:center;justify-content:center;cursor:pointer;
transition:all .15s;position:relative;overflow:hidden;
box-shadow:inset 0 0 15px rgba(0,0,100,.5);}
.cell::before{content:'';position:absolute;inset:0;
background:linear-gradient(135deg,rgba(255,255,255,.06),transparent);opacity:0;transition:opacity .15s;}
.cell:hover:not(.done) .cell-val{transform:scale(1.1);}
.cell:hover:not(.done)::before{opacity:1;}
.cell:hover:not(.done){background:var(--cell-hover);box-shadow:0 0 20px rgba(0,100,255,.5),inset 0 0 15px rgba(0,100,255,.3);}
.cell:active:not(.done){transform:scale(.97);}
.cell.done{background:var(--cell-done);cursor:default;border-color:#001050;}
.cell.done .cell-val{opacity:0;}
.cell-val{font-family:var(--ff-arcade);font-size:clamp(10px,1.5vw,16px);color:var(--gold);
text-shadow:0 0 8px var(--gold),0 0 20px rgba(255,215,0,.4);
transition:transform .15s;}

/* ── MODAL OVERLAY ── */
.overlay{position:fixed;inset:0;z-index:100;
background:rgba(0,0,20,.92);display:none;
align-items:center;justify-content:center;padding:20px;}
.overlay.on{display:flex;animation:fadeIn .25s ease;}
@keyframes fadeIn{from{opacity:0;}to{opacity:1;}}

.modal{background:var(--board-bg);border:3px solid var(--gold);
max-width:680px;width:100%;padding:32px;position:relative;
box-shadow:0 0 60px rgba(255,215,0,.3),0 0 120px rgba(0,0,255,.4);
animation:modalIn .3s cubic-bezier(.22,1,.36,1);}
@keyframes modalIn{from{transform:scale(.85);}to{transform:scale(1);}}

/* Corner brackets */
.modal::before,.modal::after{content:'';position:absolute;width:20px;height:20px;}
.modal::before{top:0;left:0;border-top:3px solid var(--cyan);border-left:3px solid var(--cyan);}
.modal::after{bottom:0;right:0;border-bottom:3px solid var(--cyan);border-right:3px solid var(--cyan);}

.modal-cat{font-family:var(--ff-arcade);font-size:9px;color:var(--cyan);letter-spacing:3px;margin-bottom:8px;
text-shadow:0 0 8px var(--cyan);}
.modal-val{font-family:var(--ff-arcade);font-size:clamp(22px,4vw,36px);color:var(--gold);
margin-bottom:20px;text-shadow:0 0 15px var(--gold);}
.modal-q{font-family:var(--ff-hud);font-size:clamp(14px,2vw,20px);font-weight:700;
line-height:1.5;margin-bottom:20px;color:var(--white);}
.modal-hint{font-size:13px;color:var(--text-dim);font-family:var(--ff-body);margin-bottom:24px;}

/* Answer area */
.a-grid-modal{display:grid;gap:10px;margin-bottom:16px;}
.a-grid-4m{grid-template-columns:1fr 1fr;}
.a-grid-2m{grid-template-columns:1fr 1fr;}
.a-grid-1m{grid-template-columns:1fr;}

.a-btn{background:rgba(0,0,100,.6);border:2px solid #0033cc;
padding:14px 18px;cursor:pointer;color:var(--white);
font-family:var(--ff-hud);font-size:14px;font-weight:700;
text-align:left;transition:all .15s;display:flex;align-items:flex-start;gap:10px;
border-radius:2px;}
.a-key{font-family:var(--ff-arcade);font-size:9px;color:#4488ff;flex-shrink:0;padding-top:2px;}
.a-btn:hover:not(:disabled){border-color:var(--cyan);background:rgba(0,100,255,.2);}
.a-btn:hover:not(:disabled) .a-key{color:var(--cyan);}
.a-btn.ok{border-color:var(--green);background:rgba(0,255,136,.12);}
.a-btn.ok .a-key{color:var(--green);}
.a-btn.bad{border-color:var(--red);background:rgba(255,34,68,.1);}
.a-btn.bad .a-key{color:var(--red);}
.a-btn:disabled{cursor:default;}

/* TF */
.tf-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-bottom:16px;}
.tf-btn{font-family:var(--ff-arcade);font-size:12px;padding:20px;
text-align:center;border:2px solid;cursor:pointer;background:rgba(0,0,80,.6);transition:all .15s;}
.tf-true{border-color:var(--green);color:var(--green);text-shadow:0 0 8px var(--green);}
.tf-false{border-color:var(--red);color:var(--red);text-shadow:0 0 8px var(--red);}
.tf-btn:hover:not(:disabled){transform:scale(1.04);}
.tf-btn.ok{background:rgba(0,255,136,.15);}
.tf-btn.bad{background:rgba(255,34,68,.12);}
.tf-btn:disabled{cursor:default;transform:none;opacity:.6;}

/* Word guess */
.word-display{display:flex;gap:8px;flex-wrap:wrap;justify-content:center;margin:12px 0 16px;}
.wl{width:36px;height:44px;border-bottom:3px solid var(--cyan);
display:flex;align-items:flex-end;justify-content:center;padding-bottom:4px;
font-family:var(--ff-arcade);font-size:16px;color:var(--gold);transition:all .2s;}
.wl.hit{border-color:var(--green);color:var(--green);animation:lPop .3s ease;}
.wl.miss-reveal{border-color:var(--red);color:var(--red);}
.wl.space{border-bottom:none;width:12px;}
@keyframes lPop{from{transform:scale(1.5);}to{transform:scale(1);}}
.alpha-wrap{display:flex;flex-wrap:wrap;gap:5px;justify-content:center;margin-bottom:14px;max-width:480px;}
.al-btn{font-family:var(--ff-arcade);font-size:9px;width:32px;height:32px;
border:1px solid #0033cc;background:rgba(0,0,80,.6);color:var(--white);
cursor:pointer;transition:all .1s;display:flex;align-items:center;justify-content:center;}
.al-btn:hover:not(:disabled){border-color:var(--cyan);color:var(--cyan);}
.al-btn.al-hit{border-color:var(--green);color:var(--green);background:rgba(0,255,136,.1);}
.al-btn.al-miss{border-color:var(--red);color:var(--red);opacity:.4;}
.al-btn:disabled{cursor:default;}
.word-lives{font-family:var(--ff-arcade);font-size:8px;color:var(--text-dim);
letter-spacing:2px;text-align:center;margin-bottom:8px;}
.word-lives span{color:var(--red);}

/* Feedback */
.fb{width:100%;border:1px solid;padding:11px 16px;
font-family:var(--ff-hud);font-size:13px;font-weight:600;
display:none;align-items:center;gap:10px;margin-bottom:14px;animation:fbIn .2s ease;}
.fb.on{display:flex;}
.fb.ok{border-color:var(--green);background:rgba(0,255,136,.08);color:var(--green);}
.fb.bad{border-color:var(--red);background:rgba(255,34,68,.08);color:#ff8899;}
@keyframes fbIn{from{opacity:0;transform:translateY(4px);}to{opacity:1;transform:none;}}

.modal-close{
  margin-top:8px;font-family:var(--ff-arcade);font-size:9px;
  background:transparent;border:1px solid var(--muted);color:var(--text-dim);
  padding:10px 20px;cursor:pointer;transition:all .15s;letter-spacing:1px;
}
.modal-close:hover{border-color:var(--cyan);color:var(--cyan);}

/* Pts pop */
.pts-pop{position:fixed;pointer-events:none;z-index:500;
font-family:var(--ff-arcade);font-size:20px;color:var(--gold);
text-shadow:0 0 12px var(--gold);animation:ptsUp 1.2s ease forwards;}
@keyframes ptsUp{0%{opacity:1;transform:translateY(0);}70%{opacity:1;transform:translateY(-60px);}100%{opacity:0;transform:translateY(-90px);}}

/* ── NAME ENTRY / RESULT ── */
.result-hero{text-align:center;margin-bottom:24px;}
.result-score{font-family:var(--ff-arcade);font-size:clamp(28px,6vw,52px);color:var(--gold);
text-shadow:0 0 20px var(--gold);animation:pulse 2s infinite;}
.result-pts-lbl{font-family:var(--ff-hud);font-size:10px;color:var(--text-dim);letter-spacing:3px;margin-top:4px;}
.result-pts-banner{margin:16px 0;text-align:center;}
.pts-badge{display:inline-block;font-family:var(--ff-arcade);font-size:clamp(12px,2vw,18px);
padding:12px 28px;border:3px solid;letter-spacing:2px;}
.pts-badge.full{border-color:var(--gold);color:var(--gold);text-shadow:0 0 10px var(--gold);
background:rgba(255,215,0,.1);box-shadow:0 0 30px rgba(255,215,0,.3);}
.pts-badge.partial{border-color:var(--cyan);color:var(--cyan);text-shadow:0 0 10px var(--cyan);}
.pts-badge.low{border-color:var(--red);color:var(--red);}

.result-breakdown{width:100%;max-width:600px;margin-bottom:24px;}
.rb-row{display:flex;justify-content:space-between;align-items:center;
padding:8px 14px;border-bottom:1px solid var(--dim);font-size:13px;font-family:var(--ff-hud);}
.rb-row:last-child{border-bottom:none;}
.rb-cat{color:var(--text-dim);}
.rb-val{font-family:var(--ff-arcade);font-size:10px;color:var(--gold);}

/* Name entry */
.name-box{width:100%;max-width:600px;border:2px solid var(--cyan);padding:20px 24px;
margin-bottom:20px;background:rgba(0,229,255,.03);
box-shadow:0 0 20px rgba(0,229,255,.1);position:relative;}
.name-box::before{content:'INSERT NAME';position:absolute;top:-10px;left:20px;
font-family:var(--ff-arcade);font-size:7px;color:var(--cyan);background:var(--bg);padding:0 8px;
animation:blink 1s infinite;}
@keyframes blink{0%,100%{opacity:1;}49%{opacity:1;}50%,99%{opacity:0;}}
.name-row{display:flex;gap:10px;}
.name-input{flex:1;background:rgba(0,0,0,.5);border:1px solid #0044cc;
padding:12px 16px;color:var(--gold);font-family:var(--ff-arcade);font-size:11px;
letter-spacing:2px;outline:none;text-transform:uppercase;}
.name-input:focus{border-color:var(--cyan);box-shadow:0 0 10px rgba(0,229,255,.2);}
.name-input::placeholder{color:var(--muted);font-size:8px;}

/* Leaderboard */
.lb-head{font-family:var(--ff-arcade);font-size:9px;color:var(--cyan);
text-align:center;margin-bottom:14px;letter-spacing:2px;text-shadow:0 0 8px var(--cyan);}
.lb-row{display:grid;grid-template-columns:36px 1fr auto auto;align-items:center;gap:10px;
padding:10px 14px;margin-bottom:6px;border:1px solid var(--dim);
font-family:var(--ff-hud);position:relative;overflow:hidden;transition:transform .15s;}
.lb-row:hover{transform:translateX(4px);}
.lb-row.g1{border-color:var(--gold);background:rgba(255,215,0,.07);}
.lb-row.g2{border-color:#aaa;background:rgba(170,170,170,.04);}
.lb-row.g3{border-color:#cd7f32;background:rgba(205,127,50,.04);}
.lb-row.new{animation:newRow .5s ease;border-color:var(--cyan);}
@keyframes newRow{from{opacity:0;transform:translateX(-20px);}to{opacity:1;transform:none;}}
.lb-pos{font-family:var(--ff-arcade);font-size:10px;text-align:center;}
.g1 .lb-pos{color:var(--gold);}
.g2 .lb-pos{color:#ccc;}
.g3 .lb-pos{color:#cd7f32;}
.lb-name{font-size:14px;font-weight:700;}
.lb-sub{font-size:10px;color:var(--text-dim);margin-top:2px;}
.lb-sc{font-family:var(--ff-arcade);font-size:11px;color:var(--gold);text-align:right;}
.lb-badge{font-family:var(--ff-arcade);font-size:8px;padding:3px 8px;border-radius:2px;white-space:nowrap;}
.lb-badge.full{background:rgba(255,215,0,.2);color:var(--gold);border:1px solid var(--gold);}
.lb-badge.partial{background:rgba(0,229,255,.1);color:var(--cyan);border:1px solid var(--cyan);}
.lb-badge.low{background:rgba(255,34,68,.1);color:var(--red);border:1px solid var(--red);}
.lb-bar{position:absolute;bottom:0;left:0;height:2px;background:linear-gradient(90deg,#0000ff,var(--cyan));}
.lb-empty{font-family:var(--ff-arcade);font-size:9px;color:var(--text-dim);
text-align:center;padding:24px;letter-spacing:1px;}

/* Buttons */
.px-btn{font-family:var(--ff-arcade);font-size:clamp(9px,1.2vw,11px);letter-spacing:1px;
text-transform:uppercase;border:none;cursor:pointer;padding:13px 26px;
transition:all .1s;outline:none;display:inline-flex;align-items:center;gap:8px;}
.px-btn::after{content:'';display:block;height:3px;background:rgba(0,0,0,.4);
margin-top:3px;margin-bottom:-3px;width:100%;}
.px-gold{background:var(--gold);color:#000;box-shadow:0 0 20px rgba(255,215,0,.4);}
.px-gold:hover{background:#ffe033;box-shadow:0 0 30px rgba(255,215,0,.6);}
.px-ghost{background:transparent;color:var(--cyan);border:2px solid var(--cyan);font-size:9px;padding:10px 20px;
box-shadow:0 0 10px rgba(0,229,255,.15);}
.px-ghost:hover{box-shadow:0 0 20px rgba(0,229,255,.3);}
.px-btn:disabled{opacity:.3;cursor:not-allowed;}

.pixel-hr{width:100%;height:2px;margin:20px 0;
background:repeating-linear-gradient(90deg,var(--dim) 0,var(--dim) 6px,transparent 6px,transparent 10px);}

@media(max-width:700px){
  .a-grid-4m,.tf-grid{grid-template-columns:1fr;}
  .wl{width:28px;height:36px;font-size:12px;}
  .al-btn{width:26px;height:26px;font-size:7px;}
}
</style>
</head>
<body>
<div id="stars"></div>
<div class="gbg"></div>
<div class="overlay" id="overlay">
  <div class="modal" id="modal">
    <div class="modal-cat" id="mCat">KATEGORIE</div>
    <div class="modal-val" id="mVal">200€</div>
    <div class="modal-q" id="mQ">Frage…</div>
    <div class="modal-hint" id="mHint"></div>

    <!-- MC answers -->
    <div id="zone-mc">
      <div class="a-grid-modal" id="aGrid"></div>
    </div>

    <!-- TF answers -->
    <div id="zone-tf" style="display:none">
      <div class="tf-grid">
        <button class="tf-btn tf-true" id="tfT" onclick="pickTF(true)">✓ RICHTIG</button>
        <button class="tf-btn tf-false" id="tfF" onclick="pickTF(false)">✗ FALSCH</button>
      </div>
    </div>

    <!-- Word guess -->
    <div id="zone-word" style="display:none">
      <div class="word-lives">VERSUCHE: <span id="wLives">6</span> ❤</div>
      <div class="word-display" id="wDisp"></div>
      <div class="alpha-wrap" id="alphaWrap"></div>
    </div>

    <div class="fb" id="fb"><span id="fbI"></span><span id="fbT"></span></div>
    <button class="modal-close" id="modalClose" style="display:none" onclick="closeModal()">WEITER →</button>
  </div>
</div>

<div class="app">

  <!-- ══ START ══ -->
  <div class="screen on" id="s-start">
    <div class="title-bar" style="margin-top:10px;">
      <div class="t1">MS SALES<br>JEOPARDY</div>
      <div class="t2">× TELEKOM EDITION × ZIEL: 8.000 € = 8 PUNKTE × MAX: 500 € PRO FRAGE ×</div>
    </div>

    <div style="display:flex;gap:16px;margin-bottom:24px;align-items:flex-start;flex-wrap:wrap;justify-content:center;">
      <div style="border:2px solid var(--gold);padding:16px 28px;text-align:center;
        background:rgba(255,215,0,.05);box-shadow:0 0 20px rgba(255,215,0,.15);">
        <div style="font-family:var(--ff-arcade);font-size:8px;color:var(--text-dim);letter-spacing:2px;margin-bottom:8px;">PUNKTESYSTEM</div>
        <div style="font-family:var(--ff-hud);font-size:13px;line-height:2;color:var(--white);">
          0–499 € = <span style="color:var(--red)">0 Punkte</span><br>
          500–1.999 € = <span style="color:var(--cyan)">1–2 Punkte</span><br>
          2.000–5.999 € = <span style="color:var(--cyan)">3–5 Punkte</span><br>
          6.000–7.999 € = <span style="color:var(--cyan)">6–7 Punkte</span><br>
          8.000 € = <span style="color:var(--gold)">8 PUNKTE ⭐</span>
        </div>
      </div>
      <div style="border:2px solid var(--cyan);padding:16px 24px;background:rgba(0,229,255,.03);">
        <div style="font-family:var(--ff-arcade);font-size:8px;color:var(--text-dim);letter-spacing:2px;margin-bottom:8px;">8 KATEGORIEN</div>
        <div style="font-family:var(--ff-hud);font-size:12px;line-height:1.9;color:var(--white);">
          🔒 Security<br>📋 M365 CSP Lizenzen<br>🤖 Copilot<br>📞 Teams Telefonie<br>
          💼 M365 Modern Work<br>⚙️ CRM/ERP Allgemein<br>🏢 CRM/ERP Kundensituationen<br>☁️ Microsoft Azure<br>🛠️ Dienstleistung & Sales
        </div>
      </div>
    </div>

    <div style="margin-bottom:24px;width:100%;max-width:500px;">
      <div style="font-family:var(--ff-arcade);font-size:8px;color:var(--cyan);letter-spacing:2px;margin-bottom:10px;text-align:center;">TEAMNAME EINGEBEN</div>
      <div style="display:flex;gap:10px;">
        <input class="name-input" id="startName" placeholder="_ _ _ TEAMNAME _ _ _" maxlength="20"
          onkeydown="if(event.key==='Enter') startGame()"
          style="flex:1;background:rgba(0,0,0,.5);border:1px solid #0044cc;padding:12px 16px;color:var(--gold);font-family:var(--ff-arcade);font-size:11px;letter-spacing:2px;outline:none;text-transform:uppercase;">
        <button class="px-btn px-gold" onclick="startGame()">▶ START</button>
      </div>
    </div>

    <div class="pixel-hr"></div>
    <div class="lb-head">─── HALL OF FAME ───</div>
    <div id="lb-start" style="width:100%;max-width:700px;"></div>
    <button class="px-ghost" style="margin-top:12px;" onclick="clearHall()">RESET SCORES</button>
  </div>

  <!-- ══ BOARD ══ -->
  <div class="screen" id="s-board">
    <div class="title-bar" style="margin-bottom:12px;">
      <div class="t1" style="font-size:clamp(12px,2vw,18px);">MS SALES JEOPARDY</div>
    </div>

    <div class="hud">
      <div class="hud-team" id="hudTeam">TEAM</div>
      <div class="hud-score-wrap">
        <div class="hud-score-label">EURO GESAMT</div>
        <div class="hud-score" id="hudScore">0 €</div>
      </div>
      <div class="hud-pts-bar">
        <div class="hud-pts-label">ZIEL: 8.000 €</div>
        <div class="pts-track"><div class="pts-fill" id="ptsFill" style="width:0%"></div></div>
        <div class="pts-goal" id="ptsGoal">0 / 8.000 € → 0 Punkte</div>
      </div>
      <button class="px-ghost" style="font-size:8px;padding:8px 14px;" onclick="finishEarly()">ABSCHLIESSEN</button>
    </div>

    <div class="board-wrap">
      <div class="board" id="board"></div>
    </div>
  </div>

  <!-- ══ RESULT ══ -->
  <div class="screen" id="s-result">
    <div class="result-hero">
      <div class="t1" style="margin-bottom:16px;">ERGEBNIS</div>
      <div class="result-score" id="rScore">0 €</div>
      <div class="result-pts-lbl">GESAMT-EURO</div>
      <div class="result-pts-banner">
        <div class="pts-badge" id="rBadge">0 PUNKTE</div>
      </div>
    </div>

    <div class="result-breakdown" id="rBreakdown"></div>

    <div class="name-box" id="nameBox">
      <div class="name-row">
        <input class="name-input" id="resultName" placeholder="_ _ _ TEAMNAME _ _ _" maxlength="20"
               onkeydown="if(event.key==='Enter') submitScore()" style="flex:1;">
        <button class="px-btn px-gold" style="font-size:9px;padding:12px 18px;" onclick="submitScore()">OK ▶</button>
      </div>
    </div>

    <div class="lb-head">─── HIGHSCORES ───</div>
    <div id="lb-result" style="width:100%;max-width:700px;"></div>

    <div style="display:flex;gap:12px;margin-top:20px;flex-wrap:wrap;justify-content:center;">
      <button class="px-btn px-gold" onclick="startGame()">▶ NOCHMAL</button>
      <button class="px-ghost" onclick="goStart()">MENU</button>
    </div>
  </div>

</div>

<script>
// ═══════════════════════════════════════════════
//  STARS
// ═══════════════════════════════════════════════
(()=>{
  const c=document.getElementById('stars');
  for(let i=0;i<100;i++){
    const s=document.createElement('div');s.className='star';
    const sz=Math.random()*1.5+.5;
    Object.assign(s.style,{width:sz+'px',height:sz+'px',
      left:Math.random()*100+'%',top:Math.random()*100+'%',
      animationDuration:(Math.random()*4+2)+'s',animationDelay:(Math.random()*5)+'s'});
    c.appendChild(s);
  }
})();

// ═══════════════════════════════════════════════
//  QUESTION BANK  (8 categories × 5 values)
// ═══════════════════════════════════════════════
// type: mc (4 options), tf (true/false), word (letter-guess)
// values: 100, 200, 300, 400, 500

const CATEGORIES = [
  { id:'security',  label:'🔒 Security' },
  { id:'lizenzen',  label:'📋 CSP Lizenzen' },
  { id:'copilot',   label:'🤖 Copilot' },
  { id:'teams',     label:'📞 Teams Telefonie' },
  { id:'mw',        label:'💼 Modern Work' },
  { id:'crm_allg',  label:'⚙️ CRM/ERP Allgemein' },
  { id:'crm_sit',   label:'🏢 CRM/ERP Situationen' },
  { id:'azure',     label:'☁️ Azure' },
  { id:'sales',     label:'🛠️ Dienstleistung' },
];

const QUESTIONS = {
  security: [
    { v:100, type:'tf',
      q:'Microsoft Defender for Business ist speziell für Unternehmen bis 300 User konzipiert.',
      correct:true, ex:'Richtig – Defender for Business ist in M365 Business Premium enthalten und bietet EDR für KMU.' },
    { v:200, type:'mc',
      q:'Was ist "Conditional Access" in Microsoft Entra ID?',
      a:['Richtlinien, die Zugriff basierend auf Bedingungen (Gerät, Standort, Risiko) steuern','Ein VPN-Dienst für Remote-Worker','Eine Firewall-Lösung für Azure','Automatisches Software-Update-Management'],
      c:0, ex:'Conditional Access ist das Zero-Trust-Kontrollinstrument: Wer darf von wo mit welchem Gerät auf was zugreifen?' },
    { v:300, type:'mc',
      q:'Welches Feature in Microsoft Defender XDR stoppt laufende Angriffe automatisch, bevor der Administrator eingreifen kann?',
      a:['Automatic Attack Disruption','Secure Score','Microsoft Sentinel Playbooks','Defender for Cloud Apps CASB'],
      c:0, ex:'Automatic Attack Disruption isoliert kompromittierte Geräte und Accounts in Echtzeit – ohne manuelles Eingreifen.' },
    { v:400, type:'mc',
      q:'Was unterscheidet Microsoft Sentinel von Microsoft Defender XDR?',
      a:['Sentinel ist ein Cloud-SIEM/SOAR für erweiterte Log-Analyse; Defender XDR ist die integrierte XDR-Plattform','Sentinel ist günstiger','Defender XDR ersetzt Sentinel vollständig','Sentinel ist nur für Azure VMs'],
      c:0, ex:'Sentinel (SIEM) analysiert Logs aus allen Quellen inkl. Drittanbieter; Defender XDR korreliert Microsoft-eigene Signale.' },
    { v:500, type:'word',
      clue:'Sicherheitskonzept: Niemals vertrauen, immer verifizieren (englisch, zusammengeschrieben, 9 Buchstaben)',
      word:'ZEROTRUST', ex:'Zero Trust ist das zentrale Sicherheitsmodell hinter Microsofts gesamter Security-Strategie.' },
  ],
  lizenzen: [
    { v:100, type:'tf',
      q:'NCE steht für "New Commerce Experience" und ist Microsofts aktuelles Lizenz-Framework für CSP-Partner.',
      correct:true, ex:'Richtig – NCE ist seit 2022 das Standardmodell für alle Microsoft-Lizenzen über den CSP-Kanal.' },
    { v:200, type:'mc',
      q:'Was passiert bei NCE Annual (monthly billing), wenn ein Kunde nach 4 Monaten kündigen will?',
      a:['Er zahlt die verbleibenden 8 Monate als Stornierungsgebühr','Er kann kostenfrei kündigen','Er wechselt automatisch auf Monthly','Microsoft erstattet anteilig'],
      c:0, ex:'Annual Commitment = Bindung für 12 Monate. Die Zahlungsweise (monatlich vs. jährlich) ändert nichts an der Laufzeit.' },
    { v:300, type:'mc',
      q:'Was ist ein "Device SL" (Shared Device License) und wann kommt sie zum Einsatz?',
      a:['Gerätegebundene Lizenz für Shared Workstations (Schichtbetrieb, Kiosk)','Günstige Einzellizenz für Freelancer','Lizenz für Surface-Geräte','Nur für Azure Virtual Desktop'],
      c:0, ex:'Device SL ist ideal für Pflege, Produktion, Einzelhandel – ein Gerät, mehrere Nutzer, keine persönlichen Accounts nötig.' },
    { v:400, type:'mc',
      q:'Welchen Preisaufschlag hat eine NCE Monthly Subscription im Vergleich zur Annual Subscription?',
      a:['ca. 20% Aufschlag','Kein Aufschlag','5% Rabatt','Aufschlag variiert je nach Partner'],
      c:0, ex:'Microsoft berechnet ca. 20% Aufschlag auf Monthly vs. Annual – ein wichtiges Argument für Annual im Kundengespräch.' },
    { v:500, type:'mc',
      q:'Ab welcher User-Zahl können Kunden NICHT mehr mit M365 Business-Plänen lizenziert werden?',
      a:['Ab 301 Usern','Ab 501 Usern','Ab 251 Usern','Keine Grenze – Business geht immer'],
      c:0, ex:'Business-Pläne (Basic/Standard/Premium) sind auf maximal 300 User begrenzt. Ab 301 sind Enterprise-Pläne notwendig.' },
  ],
  copilot: [
    { v:100, type:'tf',
      q:'Microsoft 365 Copilot ist bereits in M365 Business Standard enthalten – ohne zusätzliche Lizenz.',
      correct:false, ex:'Falsch – Copilot ist ein kostenpflichtiges Add-on (ca. 30€/User/Monat) zusätzlich zur Basislizenz.' },
    { v:200, type:'mc',
      q:'Was kann Copilot in Microsoft Word, das klassische Textverarbeitung nicht kann?',
      a:['Dokumente aus einem kurzen Prompt erstellen und vorhandene Texte umschreiben/zusammenfassen','Rechtschreibprüfung durchführen','Tabellen einfügen','PDFs öffnen'],
      c:0, ex:'Copilot in Word generiert Entwürfe, fasst lange Dokumente zusammen und schreibt Texte auf Knopfdruck um.' },
    { v:300, type:'mc',
      q:'Was ist "Copilot Studio" und wofür nutzt ein Unternehmen es?',
      a:['Low-Code-Plattform für eigene KI-Agenten mit Unternehmensdaten','Microsofts eigenes LLM-Trainingstool','Azure OpenAI Playground','Teams-App-Marktplatz'],
      c:0, ex:'Copilot Studio (früher Power Virtual Agents) erlaubt den Bau eigener Agenten ohne tiefe Programmierung – z.B. HR-Bot.' },
    { v:400, type:'mc',
      q:'Welche technischen Voraussetzungen sind für M365 Copilot zwingend notwendig?',
      a:['M365 E3/E5 oder Business Standard/Premium + Microsoft 365 Copilot Add-on + Entra ID','Office 365 E1 reicht aus','Copilot ist standalone ohne Basislizenz buchbar','Azure OpenAI Subscription separat nötig'],
      c:0, ex:'Copilot erfordert eine berechtigte Basislizenz + das Add-on. Ohne Basislizenz ist Copilot nicht buchbar.' },
    { v:500, type:'word',
      clue:'Microsofts KI-Assistent – integriert in alle M365-Apps (ein Wort, 7 Buchstaben)',
      word:'COPILOT', ex:'Microsoft 365 Copilot ist der KI-Assistent auf GPT-4-Basis für alle M365-Anwendungen.' },
  ],
  teams: [
    { v:100, type:'tf',
      q:'Beim Microsoft Calling Plan übernimmt Microsoft selbst die PSTN-Anbindung – kein eigener SBC nötig.',
      correct:true, ex:'Richtig – beim Calling Plan ist Microsoft der Carrier. Direct Routing/Operator Connect nutzen externe Carrier wie Telekom.' },
    { v:200, type:'mc',
      q:'Was ist "Operator Connect" und wie unterscheidet es sich von Direct Routing?',
      a:['Operator Connect = zertifizierter Carrier-Anschluss ohne eigenen SBC; Direct Routing = eigener SBC','Kein Unterschied','Direct Routing ist günstiger','Operator Connect nur für Großkunden'],
      c:0, ex:'Bei Operator Connect verwaltet der zertifizierte Carrier (z.B. Telekom) die Anbindung – einfacher als eigener SBC-Betrieb.' },
    { v:300, type:'mc',
      q:'Was ist "Teams Phone Mobile" und sein Alleinstellungsmerkmal?',
      a:['Mobilnummer des Users = Teams-Nummer – eine SIM, eine Rufnummer','Eine App für Teams auf dem Handy','Teams ohne WLAN nutzbar','Günstigere Calling-Plan-Option'],
      c:0, ex:'Teams Phone Mobile: SIM und Teams-Rufnummer sind identisch – Anrufe landen in Teams UND auf dem Handy.' },
    { v:400, type:'mc',
      q:'Was ist bei der Notruffähigkeit (ELIN) für Teams Direct Routing technisch zwingend?',
      a:['Mapping im SBC zwischen interner Rufnummer und Emergency Location ID (ELIN)','Separate Notfall-SIM','Azure AD Premium P2','Teams Phone Mobile Lizenz'],
      c:0, ex:'ELIN-Mapping im SBC ist Pflicht: Notrufzentralen müssen den genauen physischen Standort des Anrufers ermitteln können.' },
    { v:500, type:'word',
      clue:'Gerät, das Teams mit dem klassischen Telefonnetz (PSTN) verbindet (Abk., 3 Buchstaben)',
      word:'SBC', ex:'SBC = Session Border Controller – verbindet das IP-Netz (Teams) mit dem klassischen PSTN.' },
  ],
  mw: [
    { v:100, type:'tf',
      q:'Microsoft SharePoint ist primär ein E-Mail-Dienst.',
      correct:false, ex:'Falsch – SharePoint ist eine Intranet- und Kollaborationsplattform für Dokumentenmanagement und Teamseiten.' },
    { v:200, type:'mc',
      q:'Was ist der Hauptunterschied zwischen Microsoft Teams und einer normalen Videokonferenzsoftware?',
      a:['Teams ist eine vollständige Kollaborationsplattform (Chat, Files, Apps, Telefonie) – nicht nur Video','Teams hat bessere Videoqualität','Teams ist günstiger','Teams funktioniert nur intern'],
      c:0, ex:'Teams vereint Chat, Meetings, Dateien, Apps und Telefonie in einem – das ist die "One Stop"-Botschaft im Kundengespräch.' },
    { v:300, type:'mc',
      q:'Was ist Microsoft Viva und welche Hauptfunktion hat es?',
      a:['Employee Experience Platform für Engagement, Lernen und Wellbeing','Microsofts CRM-Lösung','Azure Monitoring Tool','Power Platform Komponente'],
      c:0, ex:'Microsoft Viva ist die Employee Experience Platform – integriert in Teams für Onboarding, Learning und Mitarbeiter-Insights.' },
    { v:400, type:'mc',
      q:'Was ermöglicht "Microsoft Loop" im Vergleich zu herkömmlicher Dokumentenarbeit?',
      a:['Echtzeit-Kollaboration mit Loop-Komponenten, die sich in Teams, Outlook und OneNote synchron aktualisieren','Offline-Dokumentenbearbeitung','KI-gestützte Dokumenten-KI','Ersatz für SharePoint'],
      c:0, ex:'Loop-Komponenten (z.B. Tabellen, Aufgaben) leben in allen Apps gleichzeitig und aktualisieren sich überall synchron.' },
    { v:500, type:'mc',
      q:'Was ist "Microsoft Places" und warum ist es für hybride Unternehmen relevant?',
      a:['Intelligentes Büroraummanagement: Buchung von Arbeitsplätzen/Räumen, Anwesenheitsübersicht im Büro','Microsofts Kartendienst','Azure IoT für Gebäudeautomation','Teams-Feature für Standortfreigabe'],
      c:0, ex:'Microsoft Places optimiert hybrides Arbeiten: Wer kommt wann ins Büro? Welcher Raum ist verfügbar? Koordination in Teams.' },
  ],
  crm_allg: [
    { v:100, type:'mc',
      q:'Ist ein CRM (Customer-Relationship-Management) nur für den Vertrieb gedacht?',
      a:[
        'Genau, der Vertrieb (Innen- und Außendienst) steht beim CRM im Fokus.',
        'Nein, Vertrieb ist der Keyuser – aber auch Marketing nutzt die CRM-Daten für Kampagnen.',
        'Nein, neben Vertrieb und Marketing kann ein CRM auch als Ticketsystem für Anfragen, Beschwerden und Störungen von Kunden genutzt werden.',
        'Nein, neben Vertrieb, Service und Marketing kann ein CRM im Standard auch zum Rechnungsschreiben genutzt werden.'
      ],
      c:2, ex:'Ein CRM deckt Vertrieb, Marketing UND Service ab – z.B. als Ticketsystem für eingehende Kundenanfragen und Beschwerden.' },
    { v:200, type:'mc',
      q:'Was sind typische ERP-Projektgrößen (Dienstleistungsanteil) bei Microsoft Finance & Supply Chain (dem großen ERP)?',
      a:['100k – 500k EUR','250k – 750k EUR','750k – 1.500k EUR','1.000k – 2.500k EUR'],
      c:2, ex:'Finance & Supply Chain ist Microsofts großes ERP für Konzerne – typische Dienstleistungsprojekte liegen bei 750k–1.500k EUR.' },
    { v:300, type:'mc',
      q:'Worauf solltet ihr euch im Vertrieb zurzeit am meisten fokussieren?',
      a:[
        'Alte ERP-Systeme – von MS Navision über Branchenlösungen bis zu Eigenentwicklungen: mit "Business Central" haben wir die Antwort und ordentlich DL-Umsatz.',
        'Salesforce-CRM (Sales, Service, Marketing) – die sind gerade in aller Munde.',
        'Field Service Lösungen – Digitalisierung von Außendienst-Prozessen hat bei der aktuellen Wirtschaftslage viel Potenzial.',
        'Middleware Lösungen – z.B. Mulesoft, denn jedes Unternehmen muss seine Systeme verbinden.'
      ],
      c:0, ex:'Alte ERP-Systeme (Navision, Branchenlösungen, Eigenentwicklungen) sind ein riesiger Markt – mit Business Central haben wir die perfekte Antwort.' },
    { v:400, type:'mc',
      q:'Was ist "Copilot for Sales" (früher Viva Sales)?',
      a:['KI-Assistent im CRM: fasst Kundengespräche zusammen, schlägt nächste Schritte vor, aktualisiert CRM automatisch','Separates Sales-Chatbot-Tool','Azure AI Studio für Sales-Modelle','Teams Meeting Add-on'],
      c:0, ex:'Copilot for Sales bringt KI in den Sales-Prozess: Meeting-Zusammenfassungen, CRM-Updates und Gesprächsanalyse automatisch.' },
    { v:500, type:'mc',
      q:'Welche typischen Dienstleister können wir bei Microsoft Business Central Projekten einsetzen?',
      a:[
        'ITVT, NewVision, abtis, Telekom-MMS, objektkultur',
        'ITVT, Medialine, NewVision, abtis, objektkultur',
        'ITVT, NewVision, abtis, Telekom-ISP, objektkultur, ICB',
        'Wir verkaufen nur Lizenzen – um den Dienstleister muss sich der Kunde selbst kümmern.'
      ],
      c:0, ex:'ITVT, NewVision, abtis, Telekom-MMS und objektkultur sind die typischen Partner für Business Central Projekte bei Telekom.' },
  ],
  crm_sit: [
    { v:100, type:'mc',
      q:'Ein global agierendes Unternehmen möchte KI-gestützte Forecasts, Opportunity Scoring und automatisierte Vertriebsanalysen nutzen. Was empfiehlst du?',
      a:[
        'Excel-basierte Lösungen auf Basis O365 haben sich hier bewährt.',
        'Microsoft Dynamics 365 Sales mit Sales Insights oder vergleichbare CRM-Lösungen wie Salesforce bieten solche Funktionen im Standard.',
        'Nur ERP-Systeme können verlässlich Forecasts liefern, weil dort die tatsächlichen Umsätze gespeichert sind.',
        'Keine Standardlösung kann das abbilden.'
      ],
      c:1, ex:'Dynamics 365 Sales mit Sales Insights (oder Salesforce) bieten KI-Forecasts, Opportunity Scoring und Vertriebsanalysen out-of-the-box.' },
    { v:200, type:'mc',
      q:'Ein schnell wachsendes SaaS-Unternehmen (Google Workspace) braucht ein CRM für Lead-Generierung, Marketing Automation und schnellen Vertrieb. ERP-Anforderungen sind minimal.',
      a:[
        'Microsoft Business Central als zentrale Lösung.',
        'Fokus auf Microsoft Dynamics 365 Finance.',
        'Fokus auf Microsoft Dynamics 365 Sales mit Power Platform.',
        'Fokus auf Salesforce Platform aufgrund der starken CRM- und Marketing-DNA.'
      ],
      c:3, ex:'Bei Google-Workspace-Kunden mit starkem CRM/Marketing-Fokus und minimalen ERP-Anforderungen ist Salesforce die natürlichere Empfehlung.' },
    { v:300, type:'mc',
      q:'Euer Gesprächspartner sucht eine Field-Service-Lösung für den technischen Außendienst (Service-Einsätze, Wartung). Was empfiehlst du?',
      a:[
        'MS "Business Central" oder "Finance & Supply Chain" – damit Ersatzteile direkt im ERP bestellt werden können.',
        '"Field Service Lightning" von Salesforce – die haben hier die beste Lösung.',
        '"Field Service" von Microsoft Dynamics 365.',
        'Sehr naheliegend sind Field Service Lösungen von Salesforce und Microsoft, aber auch Business Central bietet – je nach Anforderung – passende Third-Party Apps.'
      ],
      c:3, ex:'Sowohl Dynamics 365 Field Service als auch Salesforce Field Service Lightning sind stark. Business Central hat Third-Party-Optionen. Keine pauschale Antwort!' },
    { v:400, type:'mc',
      q:'Was ist "Dynamics 365 Customer Insights" und wofür wird es genutzt?',
      a:[
        'Kundendaten-Plattform (CDP): vereint Kundendaten aus allen Quellen für 360°-Kundenprofile und Segmentierung.',
        'Email-Marketing-Tool.',
        'Azure Analytics Workspace.',
        'Ersatz für Power BI.'
      ],
      c:0, ex:'Customer Insights ist Microsofts CDP – vereint CRM, ERP und Web-Daten zu vollständigen Kundenprofilen für Marketing und Sales.' },
    { v:500, type:'mc',
      q:'Ein internationaler Konzern plant ein ERP-Rollout in 12 Ländern mit komplexen Intercompany-Verrechnungen, lokalen Steuerregeln und Standardisierungsbedarf. Was wird benötigt?',
      a:[
        '"Business Central" – das sind ganz normale Anforderungen.',
        'Sowohl "Business Central" als auch "Finance & Supply Chain" sind möglich.',
        '"Finance & Supply Chain" als großes ERP wird benötigt.',
        'Keine pauschale Antwort möglich – die genauen Anforderungen müssen in einer Discovery geklärt werden.'
      ],
      c:3, ex:'Bei komplexen internationalen Rollouts mit Intercompany und lokalen Steuerregeln ist keine pauschale Antwort möglich – eine Discovery ist zwingend.' },
  ],
  azure: [
    { v:100, type:'tf',
      q:'Azure ist ausschließlich für große Enterprise-Unternehmen geeignet – KMU nutzen eher AWS.',
      correct:false, ex:'Falsch – Azure ist für alle Unternehmensgrößen verfügbar; in Deutschland besonders stark durch lokale Datacenter-Standorte.' },
    { v:200, type:'mc',
      q:'Was unterscheidet IaaS, PaaS und SaaS in der Praxis?',
      a:['IaaS=virtuelle Infrastruktur (VMs); PaaS=Entwicklungsplattform; SaaS=fertige Anwendung (z.B. M365)','Alle sind gleich','PaaS ist teurer als IaaS','SaaS braucht eigene Hardware'],
      c:0, ex:'Im Kundengespräch: IaaS=Lift&Shift, PaaS=DevOps/Entwicklung, SaaS=Endnutzeranwendungen wie M365 oder Dynamics.' },
    { v:300, type:'mc',
      q:'Was ist "Azure Landing Zone" und warum ist sie wichtig für Cloud-Migrationen?',
      a:['Vorkonfigurierte Azure-Umgebung mit Governance, Netzwerk und Security nach Cloud Adoption Framework','Erster Azure-Testbereich','Azure Sandbox für Entwickler','Name für Azure Free Tier'],
      c:0, ex:'Landing Zones beschleunigen Cloud-Migrationen: Governance, Policies und Netzwerk sind bereits korrekt konfiguriert.' },
    { v:400, type:'mc',
      q:'Was ist "Azure Arc" und welches Kundenproblem löst es?',
      a:['Azure-Management für On-Premises-Server und Multi-Cloud – eine Konsole für alles','Azure Backup-Lösung','Load Balancer für Hybrid-Workloads','VPN-Gateway zwischen On-Prem und Azure'],
      c:0, ex:'Arc löst das Multi-Cloud-/Hybrid-Problem: Alle Server (lokal, AWS, GCP) werden über Azure-Portal einheitlich verwaltet.' },
    { v:500, type:'word',
      clue:'Microsofts cloudbasierter Identitätsdienst – neuer Name seit 2023 (ein Wort, 5 Buchstaben)',
      word:'ENTRA', ex:'Microsoft Entra ID ist der neue Name für Azure Active Directory – zentral für Zero Trust und Identity.' },
  ],
  sales: [
    { v:100, type:'mc',
      q:'An wen wendet sich ein Seller, wenn er einen Lead im Bereich Security identifiziert hat?',
      a:['Werkzeugbox','ISP-Direktleitung','Account Manager Microsoft','Telekom Sales Hotline'],
      c:0, ex:'Die Werkzeugbox ist das zentrale Eingangstor für alle Anfragen – auch für Security-Leads.' },
    { v:200, type:'mc',
      q:'Welche Formate gibt es in der Werkzeugbox für Dienstleistungsanfragen?',
      a:['Orientierungsgespräch und Assessment','Workshop und Webinar','Proof of Concept und Pilot','Sprint und Hackathon'],
      c:0, ex:'Orientierungsgespräch und Assessment sind die zwei Standardformate in der Werkzeugbox.' },
    { v:300, type:'mc',
      q:'Wer unterstützt den Seller bei Dienstleistungsanfragen in der Werkzeugbox?',
      a:['ISP (Interne Servicepartner) und MMS','Nur der Account Manager','Microsoft Partner Support','Werkzeugbox ist self-service'],
      c:0, ex:'ISP und MMS sind die internen Ansprechpartner für Dienstleistungsanfragen in der Werkzeugbox.' },
    { v:400, type:'mc',
      q:'Ein Projekttag kostet intern ca. ___€ – was ist der richtige Wert für Seller bei der Kalkulation?',
      a:['1.480 €','800 €','2.200 €','960 €'],
      c:0, ex:'Der interne Projekttag-Satz beträgt 1.480 € – wichtig für die Einschätzung von Projektaufwänden im Kundengespräch.' },
    { v:500, type:'mc',
      q:'Wie heißt das Cloud-Angebots-Tool, das Seller für die Angebotserstellung nutzen?',
      a:['CAT (Cloud Angebots-Tool)','SAP CRM','Microsoft CPOR','Telekom Order Portal'],
      c:0, ex:'CAT = Cloud Angebots-Tool – das zentrale Tool zur Angebotserstellung für Cloud-Lösungen bei Telekom.' },
  ],
};

// ═══════════════════════════════════════════════
//  STATE
// ═══════════════════════════════════════════════
let teamName='';
let board={}; // { catId_value: true } = answered
let earned={}; // { catId: totalEarned }
let totalScore=0;
let currentQ=null; // {cat, val, q}
let wordState=null;
let scores=[];

// ═══════════════════════════════════════════════
//  STORAGE
// ═══════════════════════════════════════════════
const SK='ms_jeopardy_v2';
async function loadScores(){ try{ const r=await window.storage.get(SK,true); scores=r?JSON.parse(r.value):[]; }catch{ scores=[]; }}
async function saveScores(){ try{ await window.storage.set(SK,JSON.stringify(scores),true); }catch{} }

// ═══════════════════════════════════════════════
//  SCREENS
// ═══════════════════════════════════════════════
function showScreen(id){ document.querySelectorAll('.screen').forEach(s=>s.classList.remove('on')); document.getElementById(id).classList.add('on'); }

async function goStart(){
  await loadScores(); renderLb('lb-start',null);
  showScreen('s-start');
  setTimeout(()=>document.getElementById('startName').focus(),300);
}

// ═══════════════════════════════════════════════
//  GAME START
// ═══════════════════════════════════════════════
function startGame(){
  const n=document.getElementById('startName').value.trim().toUpperCase();
  if(!n){ document.getElementById('startName').focus(); return; }
  teamName=n;
  board={}; earned={}; totalScore=0;
  CATEGORIES.forEach(c=>{ earned[c.id]=0; });
  buildBoard();
  document.getElementById('hudTeam').textContent=n;
  updateHUD();
  showScreen('s-board');
}

// ═══════════════════════════════════════════════
//  BOARD BUILD
// ═══════════════════════════════════════════════
const VALS=[100,200,300,400,500];

function buildBoard(){
  const b=document.getElementById('board');
  b.innerHTML='';
  // Headers
  CATEGORIES.forEach(cat=>{
    const h=document.createElement('div');
    h.className='cat-header';
    h.textContent=cat.label;
    b.appendChild(h);
  });
  // Rows
  VALS.forEach(val=>{
    CATEGORIES.forEach(cat=>{
      const key=cat.id+'_'+val;
      const cell=document.createElement('div');
      cell.className='cell'+(board[key]?' done':'');
      cell.id='cell_'+key;
      const v=document.createElement('div');
      v.className='cell-val';
      v.textContent=val+'€';
      cell.appendChild(v);
      if(!board[key]) cell.onclick=()=>openQ(cat,val);
      b.appendChild(cell);
    });
  });
}

// ═══════════════════════════════════════════════
//  OPEN QUESTION
// ═══════════════════════════════════════════════
function openQ(cat,val){
  const q=QUESTIONS[cat.id].find(x=>x.v===val);
  if(!q) return;
  currentQ={cat,val,q};

  document.getElementById('mCat').textContent=cat.label;
  document.getElementById('mVal').textContent=val+' €';
  document.getElementById('mQ').textContent=q.q;
  document.getElementById('mHint').textContent='';
  document.getElementById('fb').className='fb';
  document.getElementById('modalClose').style.display='none';

  // reset zones
  document.getElementById('zone-mc').style.display='none';
  document.getElementById('zone-tf').style.display='none';
  document.getElementById('zone-word').style.display='none';

  if(q.type==='mc') buildMC(q);
  if(q.type==='tf') buildTF(q);
  if(q.type==='word') buildWord(q);

  document.getElementById('overlay').classList.add('on');
}

function buildMC(q){
  document.getElementById('zone-mc').style.display='';
  const letters=['A','B','C','D'];
  const opts=shuffle(q.a.map((a,i)=>({txt:a,orig:i})));
  const grid=document.getElementById('aGrid');
  const cols=q.a.length===2?'a-grid-2m':'a-grid-4m';
  grid.className='a-grid-modal '+cols;
  grid.innerHTML='';
  opts.forEach((o,i)=>{
    const b=document.createElement('button'); b.className='a-btn';
    b.innerHTML=`<span class="a-key">${letters[i]}</span><span>${o.txt}</span>`;
    b.onclick=()=>pickMC(o.orig===q.c, b, opts, q);
    grid.appendChild(b);
  });
}

function buildTF(q){
  document.getElementById('zone-tf').style.display='';
  document.getElementById('tfT').className='tf-btn tf-true';
  document.getElementById('tfF').className='tf-btn tf-false';
  document.getElementById('tfT').disabled=false;
  document.getElementById('tfF').disabled=false;
}

function buildWord(q){
  document.getElementById('zone-word').style.display='';
  wordState={ word:q.word.toUpperCase(), revealed:new Set(), lives:6 };
  renderWordDisp(); buildAlpha(); updLives();
}

// ═══════════════════════════════════════════════
//  ANSWER HANDLERS
// ═══════════════════════════════════════════════
function pickMC(ok, btn, opts, q){
  document.querySelectorAll('#aGrid .a-btn').forEach((b,i)=>{
    b.disabled=true;
    if(opts[i]&&opts[i].orig===q.c) b.classList.add('ok');
  });
  if(ok){ btn.classList.add('ok'); } else { btn.classList.add('bad'); }
  handleResult(ok, q);
}

function pickTF(answer){
  const q=currentQ.q;
  const ok=(answer===q.correct);
  document.getElementById('tfT').disabled=true;
  document.getElementById('tfF').disabled=true;
  if(q.correct){ document.getElementById('tfT').classList.add('ok'); }
  else { document.getElementById('tfF').classList.add('ok'); }
  if(!ok){ (answer?document.getElementById('tfT'):document.getElementById('tfF')).classList.add('bad'); }
  handleResult(ok,q);
}

function guessLetter(ch){
  if(!wordState||wordState.revealed.has(ch)) return;
  const btn=document.getElementById('al-'+ch);
  if(wordState.word.includes(ch)){
    wordState.revealed.add(ch);
    if(btn){ btn.className='al-btn al-hit'; btn.disabled=true; }
    renderWordDisp();
    const won=wordState.word.split('').every(c=>wordState.revealed.has(c));
    if(won){ document.querySelectorAll('.al-btn').forEach(b=>b.disabled=true); handleResult(true,currentQ.q); }
  } else {
    wordState.lives--;
    if(btn){ btn.className='al-btn al-miss'; btn.disabled=true; }
    updLives();
    if(wordState.lives<=0){
      wordState.word.split('').forEach(c=>wordState.revealed.add(c));
      document.querySelectorAll('.al-btn').forEach(b=>b.disabled=true);
      document.querySelectorAll('.wl:not(.space)').forEach(el=>{ if(!el.classList.contains('hit')) el.classList.add('miss-reveal'); });
      renderWordDisp();
      handleResult(false,currentQ.q);
    }
  }
}

function handleResult(ok,q){
  const val=currentQ.val;
  if(ok){
    totalScore+=val;
    earned[currentQ.cat.id]=(earned[currentQ.cat.id]||0)+val;
    updateHUD();
    showFb(true,`+${val} € → ${q.ex}`);
    popPts('+'+val+'€');
  } else {
    showFb(false,q.ex||'Leider falsch.');
  }
  markDone(currentQ.cat.id, val);
  document.getElementById('modalClose').style.display='';
  // Check if board complete
  if(isBoardDone()) {
    document.getElementById('modalClose').textContent='BOARD COMPLETE → ERGEBNIS';
  }
}

function markDone(catId, val){
  const key=catId+'_'+val;
  board[key]=true;
  const cell=document.getElementById('cell_'+key);
  if(cell){ cell.classList.add('done'); cell.onclick=null; }
}

function closeModal(){
  document.getElementById('overlay').classList.remove('on');
  currentQ=null; wordState=null;
  if(isBoardDone()) showResult();
}

function isBoardDone(){
  return CATEGORIES.every(cat=>VALS.every(v=>board[cat.id+'_'+v]));
}

function finishEarly(){ showResult(); }

// ═══════════════════════════════════════════════
//  WORD HELPERS
// ═══════════════════════════════════════════════
function renderWordDisp(){
  const d=document.getElementById('wDisp'); d.innerHTML='';
  wordState.word.split('').forEach(ch=>{
    const el=document.createElement('div');
    if(ch===' '){ el.className='wl space'; }
    else{
      const isHit=wordState.revealed.has(ch);
      el.className='wl'+(isHit?' hit':'');
      el.textContent=isHit?ch:'';
    }
    d.appendChild(el);
  });
}

function buildAlpha(){
  const g=document.getElementById('alphaWrap'); g.innerHTML='';
  'ABCDEFGHIJKLMNOPQRSTUVWXYZ'.split('').forEach(ch=>{
    const b=document.createElement('button'); b.className='al-btn'; b.id='al-'+ch;
    b.textContent=ch; b.onclick=()=>guessLetter(ch); g.appendChild(b);
  });
}

function updLives(){ document.getElementById('wLives').textContent=wordState.lives; }

// ═══════════════════════════════════════════════
//  HUD
// ═══════════════════════════════════════════════
function updateHUD(){
  document.getElementById('hudScore').textContent=totalScore.toLocaleString('de-DE')+' €';
  const pct=Math.min(totalScore/8000*100,100);
  document.getElementById('ptsFill').style.width=pct+'%';
  const pts=calcPoints(totalScore);
  document.getElementById('ptsGoal').textContent=`${totalScore.toLocaleString('de-DE')} / 8.000 € → ${pts} Punkte`;
}

function calcPoints(score){
  if(score>=8000) return 8;
  if(score>=7000) return 7;
  if(score>=6000) return 6;
  if(score>=5000) return 5;
  if(score>=4000) return 4;
  if(score>=3000) return 3;
  if(score>=2000) return 2;
  if(score>=500)  return 1;
  return 0;
}

// ═══════════════════════════════════════════════
//  FEEDBACK + EFFECTS
// ═══════════════════════════════════════════════
function showFb(ok,txt){
  const el=document.getElementById('fb');
  el.className='fb on '+(ok?'ok':'bad');
  document.getElementById('fbI').textContent=ok?'✓':'✗';
  document.getElementById('fbT').textContent=txt;
}

function popPts(txt){
  const el=document.createElement('div'); el.className='pts-pop';
  el.textContent=txt;
  el.style.left=(30+Math.random()*40)+'%';
  el.style.top='30%';
  document.body.appendChild(el);
  setTimeout(()=>el.remove(),1200);
}

// ═══════════════════════════════════════════════
//  RESULT
// ═══════════════════════════════════════════════
async function showResult(){
  document.getElementById('overlay').classList.remove('on');
  const pts=calcPoints(totalScore);

  document.getElementById('rScore').textContent=totalScore.toLocaleString('de-DE')+' €';

  const badge=document.getElementById('rBadge');
  badge.textContent=pts+' / 8 PUNKTE'+(pts===8?' ⭐':'');
  badge.className='pts-badge '+(pts>=8?'full':pts>=5?'partial':'low');

  // Breakdown
  const bd=document.getElementById('rBreakdown');
  bd.innerHTML='<div style="font-family:var(--ff-arcade);font-size:9px;color:var(--cyan);letter-spacing:2px;margin-bottom:12px;text-align:center;">ERGEBNIS JE KATEGORIE</div>';
  CATEGORIES.forEach(cat=>{
    const catEarned=earned[cat.id]||0;
    const maxPossible=VALS.reduce((s,v)=>s+v,0); // 1500
    const row=document.createElement('div'); row.className='rb-row';
    row.innerHTML=`<span class="rb-cat">${cat.label}</span><span class="rb-val">${catEarned.toLocaleString('de-DE')} €</span>`;
    bd.appendChild(row);
  });
  const total=document.createElement('div'); total.className='rb-row';
  total.style.cssText='border-top:2px solid var(--gold);margin-top:4px;';
  total.innerHTML=`<span style="color:var(--gold);font-family:var(--ff-arcade);font-size:10px;">GESAMT</span><span style="font-family:var(--ff-arcade);font-size:14px;color:var(--gold);">${totalScore.toLocaleString('de-DE')} €</span>`;
  bd.appendChild(total);

  // Pre-fill team name
  document.getElementById('resultName').value=teamName;
  document.getElementById('resultName').disabled=false;
  document.querySelector('#nameBox .px-btn').disabled=false;
  document.querySelector('#nameBox .px-btn').textContent='OK ▶';

  await loadScores();
  renderLb('lb-result',null);
  showScreen('s-result');
}

async function submitScore(){
  const name=document.getElementById('resultName').value.trim().toUpperCase();
  if(!name) return;
  await loadScores();
  const pts=calcPoints(totalScore);
  scores.push({ name, score:totalScore, pts, ts:Date.now() });
  scores.sort((a,b)=>b.score-a.score);
  if(scores.length>50) scores=scores.slice(0,50);
  await saveScores();
  document.getElementById('resultName').disabled=true;
  document.querySelector('#nameBox .px-btn').disabled=true;
  document.querySelector('#nameBox .px-btn').textContent='✓ SAVED';
  renderLb('lb-result',name);
}

// ═══════════════════════════════════════════════
//  LEADERBOARD
// ═══════════════════════════════════════════════
const MEDALS=['🥇','🥈','🥉'];
function renderLb(id, highlight){
  const el=document.getElementById(id); if(!el) return;
  if(!scores.length){ el.innerHTML='<div class="lb-empty">NO RECORDS YET<br>BE THE FIRST!</div>'; return; }
  const topS=scores[0].score||1;
  el.innerHTML=scores.map((s,i)=>{
    const cls=i===0?'g1':i===1?'g2':i===2?'g3':'';
    const medal=i<3?MEDALS[i]:(i+1)+'.';
    const bar=Math.round(s.score/topS*100);
    const isNew=s.name===highlight;
    const bCls=s.pts>=8?'full':s.pts>=5?'partial':'low';
    return `<div class="lb-row ${cls} ${isNew?'new':''}">
      <div class="lb-pos">${medal}</div>
      <div><div class="lb-name">${s.name}</div>
      <div class="lb-sub">${s.score.toLocaleString('de-DE')} € · ${new Date(s.ts).toLocaleDateString('de-DE')}</div></div>
      <div class="lb-badge ${bCls}">${s.pts}/8 PTS</div>
      <div class="lb-bar" style="width:${bar}%"></div>
    </div>`;
  }).join('');
}

async function clearHall(){
  if(!confirm('Alle Scores löschen?')) return;
  scores=[]; try{ await window.storage.delete(SK,true); }catch{}
  renderLb('lb-start',null);
}

// ═══════════════════════════════════════════════
//  UTIL
// ═══════════════════════════════════════════════
function shuffle(a){ return [...a].sort(()=>Math.random()-.5); }

// INIT
goStart();
</script>
</body>
</html>
