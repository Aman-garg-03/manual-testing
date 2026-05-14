<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Aman — Roadmap v2 · Alternating Learning Pattern · May 2025</title>
<meta name="description" content="Aman's revised SDET/AI-QA roadmap with alternating revision-and-new-concept weekly cadence, 
Udemy course references, and a 15-week path to interview-ready."/>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Sora:wght@300;400;600;700;800&family=JetBrains+Mono:wght@400;600&display=swap"
 rel="stylesheet"/>
<style>
:root {
  --bg:#07090f; --s1:#0d1117; --s2:#131923; --s3:#192030; --border:#1e2d42;
  --gold:#f5a623; --teal:#00d4aa; --red:#ff5c5c; --blue:#4fa3ff;
  --purple:#a78bfa; --green:#4ade80; --orange:#fb923c; --pink:#f472b6;
  --text:#cdd9eb; --muted:#5d7290; --dim:#3a4d66;
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;}
body{background:var(--bg);color:var(--text);font-family:'Sora',sans-serif;font-size:14px;line-height:1.75;
-webkit-font-smoothing:antialiased;}
a{color:var(--teal);text-decoration:none;}
a:hover{text-decoration:underline;}

/* ── Skip link for a11y ── */
.skip-link{position:absolute;left:-9999px;top:0;background:var(--gold);color:#000;padding:8px 14px;
    z-index:1000;font-weight:700;}
.skip-link:focus{left:8px;top:8px;}

/* ── TOP NAV ── */
.topnav{
  position:sticky;top:0;z-index:50;background:rgba(7,9,15,0.92);
  backdrop-filter:blur(8px);border-bottom:1px solid var(--border);
  display:flex;flex-wrap:wrap;gap:6px 14px;padding:10px 28px;align-items:center;
  font-family:'JetBrains Mono',monospace;font-size:11px;
}
.topnav strong{color:var(--gold);margin-right:12px;letter-spacing:1px;}
.topnav a{color:var(--muted);}
.topnav a:hover{color:var(--teal);text-decoration:none;}

/* ── HERO ── */
.hero{
  padding:56px 48px 44px;
  background:linear-gradient(150deg,#080d16 0%,#060a12 100%);
  border-bottom:1px solid var(--border);position:relative;overflow:hidden;
}
.hero::before{content:'';position:absolute;width:600px;height:600px;border-radius:50%;
  background:radial-gradient(circle,rgba(0,212,170,0.06) 0%,transparent 65%);top:-200px;right:-150px;}
.hero::after{content:'';position:absolute;width:400px;height:400px;border-radius:50%;
  background:radial-gradient(circle,rgba(167,139,250,0.05) 0%,transparent 65%);bottom:-100px;left:-50px;}
.hero-tag{font-family:'JetBrains Mono',monospace;font-size:10px;letter-spacing:3px;color:var(--teal);
text-transform:uppercase;margin-bottom:16px;}
.hero h1{font-size:clamp(28px,4vw,50px);font-weight:800;color:#fff;line-height:1.1;margin-bottom:12px;}
.hero h1 em{color:var(--gold);font-style:normal;}
.hero h1 span{color:var(--teal);}
.hero-sub{color:var(--muted);font-size:13px;max-width:720px;line-height:1.7;}
.hero-meta{display:flex;flex-wrap:wrap;gap:10px;margin-top:24px;}
.meta-chip{background:var(--s2);border:1px solid var(--border);border-radius:8px;
  padding:6px 14px;font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--text);}
.meta-chip span{color:var(--gold);}
.meta-chip.ok{border-color:rgba(0,212,170,0.3);color:var(--teal);}
.meta-chip.new{border-color:rgba(167,139,250,0.3);color:var(--purple);}

/* ── SECTIONS ── */
.section{padding:52px 48px;border-bottom:1px solid var(--border);}
@media(max-width:640px){.section,.hero{padding:32px 20px;}.topnav{padding:10px 16px;}}
.sec-tag{font-family:'JetBrains Mono',monospace;font-size:9px;letter-spacing:3px;
text-transform:uppercase;color:var(--teal);margin-bottom:6px;}
.sec-title{font-size:22px;font-weight:700;color:#fff;margin-bottom:6px;}
.sec-sub{color:var(--muted);font-size:13px;margin-bottom:28px;}

/* ── CALLOUTS ── */
.callout{border-radius:12px;padding:20px 24px;margin-bottom:20px;font-size:13px;line-height:1.7;}
.callout.amber{background:rgba(245,166,35,0.07);border:1px solid rgba(245,166,35,0.2);}
.callout.red{background:rgba(255,92,92,0.07);border:1px solid rgba(255,92,92,0.2);}
.callout.teal{background:rgba(0,212,170,0.06);border:1px solid rgba(0,212,170,0.18);}
.callout.blue{background:rgba(79,163,255,0.06);border:1px solid rgba(79,163,255,0.18);}
.callout.purple{background:rgba(167,139,250,0.06);border:1px solid rgba(167,139,250,0.18);}
.callout-title{font-weight:700;font-size:13px;margin-bottom:8px;}
.callout.amber .callout-title{color:var(--gold);}
.callout.red .callout-title{color:var(--red);}
.callout.teal .callout-title{color:var(--teal);}
.callout.blue .callout-title{color:var(--blue);}
.callout.purple .callout-title{color:var(--purple);}
.callout p,.callout li{color:var(--muted);}
.callout ul{padding-left:18px;}
.callout ul li{margin-bottom:4px;}

/* ── GRID ── */
.g2{display:grid;grid-template-columns:1fr 1fr;gap:14px;}
.g3{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;}
@media(max-width:780px){.g2,.g3{grid-template-columns:1fr;}}

/* ── STAT CARDS ── */
.stat-card{background:var(--s1);border:1px solid var(--border);border-radius:12px;padding:22px 24px;text-align:center;}
.stat-num{font-size:32px;font-weight:800;color:#fff;font-family:'JetBrains Mono',monospace;line-height:1;}
.stat-num.teal{color:var(--teal);} .stat-num.gold{color:var(--gold);}
.stat-num.red{color:var(--red);} .stat-num.purple{color:var(--purple);}
.stat-label{font-size:11px;color:var(--muted);margin-top:8px;line-height:1.4;}

/* ── PATTERN LEGEND ── */
.legend{display:flex;flex-wrap:wrap;gap:10px;margin-bottom:18px;}
.legend-item{display:flex;align-items:center;gap:8px;font-size:11px;font-family:'JetBrains Mono',monospace;
  background:var(--s2);border:1px solid var(--border);border-radius:8px;padding:6px 12px;color:var(--muted);}
.dot{width:10px;height:10px;border-radius:50%;display:inline-block;}
.dot.rev{background:var(--gold);} .dot.new{background:var(--purple);}
.dot.prac{background:var(--teal);} .dot.fund{background:var(--blue);}

/* ── WEEK CARD ── */
.week{
  background:var(--s1);border:1px solid var(--border);border-radius:14px;
  margin-bottom:18px;overflow:hidden;
}
.week-header{
  padding:16px 22px;display:flex;flex-wrap:wrap;align-items:center;gap:12px;
  border-bottom:1px solid var(--border);
}
.week-header.rev{background:linear-gradient(90deg,rgba(245,166,35,0.10),transparent 70%);}
.week-header.new{background:linear-gradient(90deg,rgba(167,139,250,0.10),transparent 70%);}
.week-header.mix{background:linear-gradient(90deg,rgba(0,212,170,0.08),rgba(167,139,250,0.08) 80%);}
.week-num{font-family:'JetBrains Mono',monospace;font-size:10px;color:var(--muted);min-width:56px;letter-spacing:1px;}
.week-mode{
  font-family:'JetBrains Mono',monospace;font-size:10px;letter-spacing:2px;text-transform:uppercase;
  padding:4px 10px;border-radius:6px;font-weight:600;
}
.mode-rev{background:rgba(245,166,35,0.12);color:var(--gold);border:1px solid rgba(245,166,35,0.25);}
.mode-new{background:rgba(167,139,250,0.12);color:var(--purple);border:1px solid rgba(167,139,250,0.25);}
.mode-mix{background:rgba(0,212,170,0.12);color:var(--teal);border:1px solid rgba(0,212,170,0.25);}
.week-title{font-weight:700;font-size:15px;color:#fff;}
.week-date{margin-left:auto;font-family:'JetBrains Mono',monospace;font-size:10px;color:var(--gold);
  background:rgba(245,166,35,0.08);border:1px solid rgba(245,166,35,0.15);padding:3px 10px;border-radius:6px;}
.week-body{padding:22px 24px;}

/* Two-column inner: revise | new */
.duo{display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-top:14px;}
@media(max-width:780px){.duo{grid-template-columns:1fr;}}
.col{background:var(--s2);border:1px solid var(--border);border-radius:10px;padding:16px 18px;}
.col h4{font-size:12px;font-family:'JetBrains Mono',monospace;letter-spacing:1.5px;text-transform:uppercase;
  margin-bottom:10px;display:flex;align-items:center;gap:8px;}
.col.rev h4{color:var(--gold);}
.col.new h4{color:var(--purple);}
.col.prac h4{color:var(--teal);}
.col ul{list-style:none;padding:0;}
.col ul li{font-size:12.5px;color:var(--muted);padding:5px 0;display:flex;gap:8px;align-items:flex-start;line-height:1.55;}
.col ul li::before{content:'›';color:var(--dim);flex-shrink:0;margin-top:1px;}
.col ul li strong{color:var(--text);}

/* Topic pills */
.topic-row{display:flex;flex-wrap:wrap;gap:6px;margin:10px 0 6px;}
.topic{padding:3px 10px;border-radius:6px;font-size:10.5px;font-family:'JetBrains Mono',monospace;font-weight:600;}
.t-rev{background:rgba(245,166,35,0.10);color:var(--gold);border:1px solid rgba(245,166,35,0.2);}
.t-new{background:rgba(167,139,250,0.10);color:var(--purple);border:1px solid rgba(167,139,250,0.2);}
.t-prac{background:rgba(0,212,170,0.08);color:var(--teal);border:1px solid rgba(0,212,170,0.18);}
.t-fund{background:rgba(79,163,255,0.10);color:var(--blue);border:1px solid rgba(79,163,255,0.2);}

/* Udemy block */
.udemy{
  background:linear-gradient(135deg,rgba(167,139,250,0.06),rgba(244,114,182,0.04));
  border:1px solid rgba(167,139,250,0.22);border-radius:10px;padding:14px 18px;margin-top:14px;
}
.udemy-title{font-family:'JetBrains Mono',monospace;font-size:10px;letter-spacing:2px;text-transform:uppercase;
  color:var(--pink);margin-bottom:8px;display:flex;align-items:center;gap:8px;}
.udemy-title::before{content:'▶';color:var(--pink);}
.udemy-list{list-style:none;padding:0;}
.udemy-list li{font-size:12px;color:var(--muted);padding:5px 0;border-bottom:1px dashed rgba(167,139,250,0.12);}
.udemy-list li:last-child{border-bottom:none;}
.udemy-list li strong{color:var(--text);}
.udemy-list li .instr{color:var(--purple);font-family:'JetBrains Mono',monospace;font-size:10.5px;}
.udemy-list li .sec{color:var(--teal);font-size:11px;display:block;margin-top:2px;}

/* Practical task box */
.practical{
  background:rgba(0,212,170,0.05);border:1px solid rgba(0,212,170,0.18);
  border-radius:10px;padding:14px 18px;margin-top:12px;
}
.practical-title{font-family:'JetBrains Mono',monospace;font-size:10px;letter-spacing:2px;text-transform:uppercase;
  color:var(--teal);margin-bottom:8px;display:flex;align-items:center;gap:8px;}
.practical-title::before{content:'⚡';}
.practical p{font-size:12.5px;color:var(--muted);margin-bottom:6px;}
.practical strong{color:var(--text);}

/* Deliverables */
.deliverables{display:flex;flex-wrap:wrap;gap:8px;margin-top:14px;}
.del{font-size:11px;font-family:'JetBrains Mono',monospace;padding:4px 12px;border-radius:20px;font-weight:600;}
.del-gh{background:rgba(79,163,255,0.1);color:var(--blue);border:1px solid rgba(79,163,255,0.2);}
.del-skill{background:rgba(0,212,170,0.08);color:var(--teal);border:1px solid rgba(0,212,170,0.15);}
.del-job{background:rgba(245,166,35,0.1);color:var(--gold);border:1px solid rgba(245,166,35,0.2);}

/* Timeline */
.timeline{display:flex;gap:0;margin:24px 0;border-radius:12px;overflow:hidden;border:1px solid var(--border);}
.tl-seg{flex:1;padding:14px 16px;text-align:center;}
.tl-seg:not(:last-child){border-right:1px solid var(--border);}
.tl-seg.b1{background:rgba(245,166,35,0.07);}
.tl-seg.b2{background:rgba(167,139,250,0.07);}
.tl-seg.b3{background:rgba(0,212,170,0.06);}
.tl-seg.b4{background:rgba(79,163,255,0.06);}
.tl-label{font-family:'JetBrains Mono',monospace;font-size:9px;letter-spacing:2px;text-transform:uppercase;color:var(--muted);margin-bottom:4px;}
.tl-period{font-weight:700;font-size:12px;color:#fff;}
.tl-desc{font-size:10px;color:var(--muted);margin-top:4px;}
@media(max-width:600px){.timeline{flex-direction:column;}.tl-seg:not(:last-child){border-right:none;border-bottom:1px solid var(--border);}}

/* Tables */
.data-table{width:100%;border-collapse:collapse;font-size:12px;}
.data-table th{text-align:left;padding:10px 14px;font-family:'JetBrains Mono',monospace;font-size:10px;letter-spacing:1.5px;text-transform:uppercase;color:var(--muted);border-bottom:1px solid var(--border);}
.data-table td{padding:11px 14px;border-bottom:1px solid rgba(30,45,66,0.5);color:var(--muted);vertical-align:top;}
.data-table td strong{color:var(--text);}
.data-table tr:last-child td{border-bottom:none;}

/* Verdict */
.verdict{background:linear-gradient(135deg,#0a1020,#0d1520);border:1px solid var(--border);
  border-radius:16px;padding:32px 36px;text-align:center;}
.verdict p{color:var(--muted);font-size:14px;line-height:1.8;max-width:700px;margin:0 auto 16px;}
.verdict p:first-child{color:var(--text);font-size:16px;font-weight:600;}

/* Print */
@media print{
  body{background:#fff;color:#000;}
  .topnav,.hero::before,.hero::after{display:none;}
  .section,.hero{padding:24px;border-color:#ccc;}
  .week,.col,.callout,.udemy,.practical,.stat-card,.verdict{
    background:#fff !important;border:1px solid #999 !important;color:#000 !important;break-inside:avoid;
  }
  .week-title,.sec-title,.hero h1,h4,strong{color:#000 !important;}
  .topic,.del,.meta-chip,.week-mode,.week-date{border-color:#999 !important;color:#000 !important;background:#f0f0f0 !important;}
  a{color:#0040a0 !important;text-decoration:underline;}
}
</style>
</head>
<body>

<a class="skip-link" href="#main">Skip to main content</a>

<!-- ═══ TOP NAV ═══ -->
<nav class="topnav" aria-label="Section navigation">
  <strong>ROADMAP v2</strong>
  <a href="#pattern">Pattern</a>
  <a href="#timeline">Timeline</a>
  <a href="#blockA">Block A</a>
  <a href="#blockB">Block B</a>
  <a href="#blockC">Block C</a>
  <a href="#blockD">Block D</a>
  <a href="#udemy-master">Udemy Map</a>
  <a href="#playlists">Playlists</a>
  <a href="#skills">Skill Map</a>
</nav>

<main id="main">

<!-- ═══ HERO ═══ -->
<header class="hero">
  <div class="hero-tag">⟳ Roadmap v2 · Alternating Cadence · May 2025 → Sep 2025</div>
  <h1>Aman's <em>Alternating</em> Reset Plan<br><span>Revise · Learn · Build · Repeat</span></h1>
  <p class="hero-sub">
    Same 15-week deadline. Smarter weekly rhythm. Each week alternates a <strong style="color:var(--gold);">revision block</strong> (familiar tech, low friction) with a <strong style="color:var(--purple);">new-concept block</strong> (modern stack, deliberate practice), then anchors both with a <strong style="color:var(--teal);">practical build</strong>. Burn-out down. Retention up. Portfolio compounds week over week.
  </p>
  <div class="hero-meta">
    <div class="meta-chip ok">✓ Alternating Cadence</div>
    <div class="meta-chip new">★ Udemy Course Map Included</div>
    <div class="meta-chip ok">✓ Mobile + Print Friendly</div>
    <div class="meta-chip"><span>Start:</span> May 14, 2025</div>
    <div class="meta-chip"><span>Interview-Ready:</span> Sep 1, 2025</div>
  </div>
</header>

<!-- ═══ THE PATTERN ═══ -->
<section class="section" id="pattern">
  <div class="sec-tag">Section 01</div>
  <h2 class="sec-title">The Alternating Learning Pattern</h2>
  <p class="sec-sub">Why this structure beats a linear "learn-everything-then-build" plan.</p>

  <div class="legend">
    <div class="legend-item"><span class="dot rev"></span> REVISION — existing/decayed skills</div>
    <div class="legend-item"><span class="dot new"></span> NEW CONCEPT — fresh framework/tool</div>
    <div class="legend-item"><span class="dot prac"></span> PRACTICAL BUILD — pushed to GitHub</div>
    <div class="legend-item"><span class="dot fund"></span> FUNDAMENTAL — Linux/SQL/HTTP/CI</div>
  </div>

  <div class="g2">
    <div class="callout purple">
      <div class="callout-title">🧠 Why Alternate</div>
      <ul>
        <li><strong>Cognitive variety</strong> — switching between familiar and novel content reduces fatigue and improves long-term recall (interleaved practice effect).</li>
        <li><strong>Momentum protection</strong> — revision weeks deliver fast wins; new-concept weeks deliver curiosity and growth.</li>
        <li><strong>Skill bridging</strong> — practising a new tool right after revising the equivalent old tool (e.g., Selenium → Playwright) makes patterns transfer naturally.</li>
        <li><strong>Burst-mode friendly</strong> — revision weeks survive lower-energy days; new-concept weeks get the high-energy bursts.</li>
      </ul>
    </div>
    <div class="callout teal">
      <div class="callout-title">📐 The Weekly Recipe</div>
      <ul>
        <li><strong>40% Revision</strong> — sharpen one decayed/known skill (Selenium, Java, BDD, SQL).</li>
        <li><strong>40% New Concept</strong> — one fresh tool/framework, primarily through Udemy.</li>
        <li><strong>20% Practical Build</strong> — combine both into a small artifact pushed to GitHub the same week.</li>
        <li>Every <strong>4th week</strong> = consolidation: no new content, only build + polish + push.</li>
      </ul>
    </div>
  </div>

  <div class="callout blue" style="margin-top:8px;">
    <div class="callout-title">📈 Gradual Complexity Curve</div>
    <p>Each block raises the bar one notch — Block A: scripts. Block B: frameworks + CI. Block C: distributed/AI/Docker stacks. Block D: interview-grade explanations of everything built. New tools are introduced only after the foundation tool of the same family is at 6/10 confidence.</p>
  </div>
</section>

<!-- ═══ TIMELINE ═══ -->
<section class="section" id="timeline">
  <div class="sec-tag">Section 02</div>
  <h2 class="sec-title">15-Week Map · Alternating Mode per Week</h2>
  <p class="sec-sub">Yellow = revision-led · Purple = new-concept-led · Teal = mixed/build week.</p>

  <div class="timeline" role="list" aria-label="Block timeline">
    <div class="tl-seg b1" role="listitem"><div class="tl-label">Block A</div><div class="tl-period">Wk 1–4</div><div class="tl-desc">Foundation Revival<br>+ Git/Linux/SQL</div></div>
    <div class="tl-seg b2" role="listitem"><div class="tl-label">Block B</div><div class="tl-period">Wk 5–8</div><div class="tl-desc">API · CI · Playwright<br>+ AI/LLM</div></div>
    <div class="tl-seg b3" role="listitem"><div class="tl-label">Block C</div><div class="tl-period">Wk 9–11</div><div class="tl-desc">Docker · Perf · LLM<br>Eval + Portfolio</div></div>
    <div class="tl-seg b4" role="listitem"><div class="tl-label">Block D</div><div class="tl-period">Wk 12–15</div><div class="tl-desc">Mocks · Apps<br>Light DSA</div></div>
  </div>

  <table class="data-table" aria-label="Per-week alternating mode summary">
    <thead><tr><th>Wk</th><th>Mode</th><th>Revise</th><th>New Concept</th><th>Build</th></tr></thead>
    <tbody>
      <tr><td>01</td><td><span class="topic t-rev">REVISION</span></td><td>Selenium core, Java refresh</td><td>Git advanced workflow</td><td>Repo scaffold + first push</td></tr>
      <tr><td>02</td><td><span class="topic t-new">NEW</span></td><td>POM pattern</td><td>TestNG advanced + Linux CLI</td><td>Script 1 (saucedemo)</td></tr>
      <tr><td>03</td><td><span class="topic t-rev">REVISION</span></td><td>BDD/Cucumber</td><td>SQL + HTTP fundamentals</td><td>Script 2 (BDD framework)</td></tr>
      <tr><td>04</td><td><span class="topic t-prac">BUILD</span></td><td>Polish all 3 scripts</td><td>—</td><td>Script 3 + README + portfolio v1</td></tr>
      <tr><td>05</td><td><span class="topic t-new">NEW</span></td><td>Java collections/OOP</td><td>Postman + Rest Assured</td><td>API test suite</td></tr>
      <tr><td>06</td><td><span class="topic t-rev">REVISION</span></td><td>Maven + test reports</td><td>GitHub Actions CI/CD</td><td>Green CI badge live</td></tr>
      <tr><td>07</td><td><span class="topic t-new">NEW</span></td><td>Locator strategies</td><td>Playwright + TypeScript</td><td>Playwright repo #2</td></tr>
      <tr><td>08</td><td><span class="topic t-mix" style="background:rgba(0,212,170,0.12);color:var(--teal);border:1px solid rgba(0,212,170,0.25);">MIX</span></td><td>Prompt patterns at work</td><td>LLM fundamentals</td><td>3 GenAI work-stories doc</td></tr>
      <tr><td>09</td><td><span class="topic t-new">NEW</span></td><td>Selenium Grid concept</td><td>Docker fundamentals</td><td>Dockerised Selenium suite</td></tr>
      <tr><td>10</td><td><span class="topic t-new">NEW</span></td><td>API testing recap</td><td>k6 + LLM evals (deepeval)</td><td>Load test + 1 LLM eval</td></tr>
      <tr><td>11</td><td><span class="topic t-prac">BUILD</span></td><td>All repos audit</td><td>—</td><td>Resume + LinkedIn + AI case study</td></tr>
      <tr><td>12</td><td><span class="topic t-rev">REVISION</span></td><td>Framework architecture talk-through</td><td>Light DSA (arrays/strings)</td><td>2 mocks + 5 applications</td></tr>
      <tr><td>13</td><td><span class="topic t-rev">REVISION</span></td><td>API + CI + Docker explanations</td><td>HashMap/2-pointer DSA</td><td>2 mocks + 5 applications</td></tr>
      <tr><td>14</td><td><span class="topic t-prac">BUILD</span></td><td>Behavioural stories (STAR)</td><td>—</td><td>10+ applications</td></tr>
      <tr><td>15</td><td><span class="topic t-prac">BUILD</span></td><td>System-design lite (test strategy)</td><td>—</td><td>10+ applications, offer prep</td></tr>
    </tbody>
  </table>
</section>

<!-- ═══ BLOCK A ═══ -->
<section class="section" id="blockA">
  <div class="sec-tag">Section 03 · Block A</div>
  <h2 class="sec-title">Block A — Foundation Revival (Weeks 1–4)</h2>
  <p class="sec-sub">May 14 – Jun 8 · Alternating revise → new → revise → build.</p>

  <!-- WEEK 1 -->
  <article class="week" id="w1">
    <header class="week-header rev">
      <span class="week-num">WEEK 01</span>
      <span class="week-mode mode-rev">Revision-Led</span>
      <span class="week-title">Selenium Core Revival + Git Advanced</span>
      <span class="week-date">May 14–20</span>
    </header>
    <div class="week-body">
      <p style="color:var(--muted);font-size:13px;">Slow start by design. Re-awaken muscle memory on familiar ground (Selenium), and pair it with one new mental model (Git branching) that pays off all year.</p>
      <div class="duo">
        <div class="col rev">
          <h4>🔁 Revise (Selenium / Java)</h4>
          <ul>
            <li>WebDriver setup, WebDriverManager, ChromeOptions</li>
            <li>Locators: id, name, css, relative XPath (<code>contains</code>, <code>starts-with</code>)</li>
            <li>Waits: implicit vs explicit vs fluent — and why <strong>Thread.sleep is wrong</strong></li>
            <li>Type the code from scratch — do <strong>not</strong> copy-paste</li>
          </ul>
        </div>
        <div class="col new">
          <h4>✨ New (Git Workflow)</h4>
          <ul>
            <li>feature/dev/main branching strategy</li>
            <li>Merge vs rebase — when to use each</li>
            <li>PR creation, conflict resolution, <code>.gitignore</code></li>
            <li><code>git stash</code>, <code>git log --oneline</code>, tagging</li>
          </ul>
        </div>
      </div>
      <div class="udemy">
        <div class="udemy-title">Udemy — Recommended This Week</div>
        <ul class="udemy-list">
          <li><strong>Selenium WebDriver with Java -Basics to Advanced+ Frameworks</strong> <span class="instr">— Rahul Shetty</span>
            <span class="sec">▸ Sections 1–6 (Setup, Locators, XPath, Waits). 1.5×–1.75× speed.</span></li>
          <li><strong>Git Complete: The definitive, step-by-step guide to Git</strong> <span class="instr">— Jason Taylor</span>
            <span class="sec">▸ Sections 3–7 (Branching, Merging, Rebase, Conflict Resolution).</span></li>
        </ul>
      </div>
      <div class="practical">
        <div class="practical-title">Practical Build</div>
        <p>Create a fresh GitHub repo <strong>sdet-portfolio-2025</strong>. Scaffold a Maven project. Practise the Git branching flow by raising a PR to yourself and merging. <strong>Push at least 1 commit.</strong></p>
      </div>
      <div class="deliverables">
        <span class="del del-gh">Repo created</span>
        <span class="del del-skill">Git workflow understood</span>
        <span class="del del-skill">Selenium hands moving</span>
      </div>
    </div>
  </article>

  <!-- WEEK 2 -->
  <article class="week" id="w2">
    <header class="week-header new">
      <span class="week-num">WEEK 02</span>
      <span class="week-mode mode-new">New-Concept-Led</span>
      <span class="week-title">TestNG + POM (refresh) + Linux CLI (new)</span>
      <span class="week-date">May 21–27</span>
    </header>
    <div class="week-body">
      <p style="color:var(--muted);font-size:13px;">First visible artifact week — POM is familiar, TestNG advanced annotations get re-learned, and Linux is the genuinely new layer woven in daily.</p>
      <div class="duo">
        <div class="col rev">
          <h4>🔁 Revise (POM + TestNG basics)</h4>
          <ul>
            <li>POM with <code>@FindBy</code> + <code>PageFactory</code></li>
            <li>TestNG annotations in correct firing order</li>
            <li>Hard vs soft assertions</li>
            <li>Build LoginPage + ProductsPage on saucedemo</li>
          </ul>
        </div>
        <div class="col new">
          <h4>✨ New (TestNG Advanced + Linux)</h4>
          <ul>
            <li><code>@DataProvider</code>, parallel groups, <code>testng.xml</code></li>
            <li>Listeners (ITestListener) for screenshots on failure</li>
            <li>Linux: <code>cd / ls / chmod / chown</code>, pipes, <code>grep / find</code></li>
            <li>Write a tiny bash script that runs <code>mvn test</code> and copies the report</li>
          </ul>
        </div>
      </div>
      <div class="udemy">
        <div class="udemy-title">Udemy — Recommended This Week</div>
        <ul class="udemy-list">
          <li><strong>Selenium WebDriver with Java -Basics to Advanced+ Frameworks</strong> <span class="instr">— Rahul Shetty</span>
            <span class="sec">▸ Sections on TestNG, Page Object Model, DataProvider, Listeners.</span></li>
          <li><strong>Linux Command Line Basics</strong> <span class="instr">— Ahmed Alkabary</span> · or · <strong>Linux Mastery</strong> <span class="instr">— Ziyad Yehia</span>
            <span class="sec">▸ Modules 1–4: Filesystem, Permissions, Pipes, grep/find. ~4 hrs total.</span></li>
        </ul>
      </div>
      <div class="practical">
        <div class="practical-title">Practical Build · Script 1</div>
        <p>Saucedemo automation with POM + TestNG: valid login, invalid login (DataProvider), add-to-cart, sort. README with how-to-run + screenshot. <strong>Push to GitHub.</strong></p>
      </div>
      <div class="deliverables"><span class="del del-gh">Script 1 pushed</span><span class="del del-skill">Linux comfortable</span></div>
    </div>
  </article>

  <!-- WEEK 3 -->
  <article class="week" id="w3">
    <header class="week-header rev">
      <span class="week-num">WEEK 03</span>
      <span class="week-mode mode-rev">Revision-Led</span>
      <span class="week-title">BDD/Cucumber Refresh + SQL & HTTP (new fundamentals)</span>
      <span class="week-date">May 28 – Jun 3</span>
    </header>
    <div class="week-body">
      <div class="duo">
        <div class="col rev">
          <h4>🔁 Revise (BDD / Cucumber)</h4>
          <ul>
            <li>Gherkin syntax: Given / When / Then / And / But</li>
            <li>Step definitions, hooks (<code>@Before</code>, <code>@After</code>)</li>
            <li><code>@CucumberOptions</code> runner, tags, scenario outline</li>
          </ul>
        </div>
        <div class="col new">
          <h4>✨ New (SQL + HTTP)</h4>
          <ul>
            <li>SQL: SELECT, WHERE, INNER/LEFT JOIN, GROUP BY, subqueries</li>
            <li>How a QA uses SQL to validate DB state after a test</li>
            <li>HTTP: methods, status codes (2xx/3xx/4xx/5xx), headers</li>
            <li>REST principles, idempotency, JSON payloads</li>
          </ul>
        </div>
      </div>
      <div class="udemy">
        <div class="udemy-title">Udemy — Recommended This Week</div>
        <ul class="udemy-list">
          <li><strong>BDD with Cucumber, Selenium, Java, Junit & Live Project</strong> <span class="instr">— Rahul Shetty</span>
            <span class="sec">▸ Sections 1–7 (Gherkin, Hooks, Tags, Runner, Reusability).</span></li>
          <li><strong>The Complete SQL Bootcamp</strong> <span class="instr">— Jose Portilla</span>
            <span class="sec">▸ Sections on SELECT, JOINs, GROUP BY, subqueries (skip Postgres install — use sqlfiddle).</span></li>
          <li><strong>HTTP &amp; REST API Concepts (Postman section bonus)</strong> <span class="instr">— Valentin Despa</span>
            <span class="sec">▸ "HTTP Fundamentals" + "REST API Basics" modules.</span></li>
        </ul>
      </div>
      <div class="practical">
        <div class="practical-title">Practical Build · Script 2</div>
        <p>BDD framework on saucedemo: <code>login.feature</code> + <code>cart.feature</code>, step defs, hooks for screenshot on failure. <strong>Push.</strong></p>
      </div>
      <div class="deliverables"><span class="del del-gh">Script 2 pushed</span><span class="del del-skill">SQL solid</span><span class="del del-skill">HTTP solid</span></div>
    </div>
  </article>

  <!-- WEEK 4 -->
  <article class="week" id="w4">
    <header class="week-header mix">
      <span class="week-num">WEEK 04</span>
      <span class="week-mode mode-mix">Build / Consolidation</span>
      <span class="week-title">E2E Script 3 + Portfolio v1 Polish</span>
      <span class="week-date">Jun 4–8</span>
    </header>
    <div class="week-body">
      <p style="color:var(--muted);font-size:13px;"><strong>No new tools this week.</strong> Consolidation is the multiplier — the brain locks in what was learnt over weeks 1–3 by using it.</p>
      <div class="duo">
        <div class="col prac">
          <h4>⚡ Build (E2E + DB Validation)</h4>
          <ul>
            <li>Full checkout flow: Login → 2 items → Checkout → Confirmation</li>
            <li>Add a SQL validation step (against a free demo DB) for one scenario</li>
            <li>Capture screenshots on failure via TestNG listener</li>
          </ul>
        </div>
        <div class="col rev">
          <h4>🔁 Polish (Portfolio v1)</h4>
          <ul>
            <li>Single repo, clean folder structure</li>
            <li>Top-level README: stack, how-to-run, scenarios covered, screenshot</li>
            <li>Tag <code>v0.1.0</code> as the first portfolio milestone</li>
          </ul>
        </div>
      </div>
      <div class="practical">
        <div class="practical-title">Output</div>
        <p>Three working scripts on GitHub with one tagged release. <strong>Block A complete.</strong></p>
      </div>
      <div class="deliverables"><span class="del del-gh">3 scripts live</span><span class="del del-gh">v0.1.0 tagged</span><span class="del del-skill">Block A done</span></div>
    </div>
  </article>
</section>

<!-- ═══ BLOCK B ═══ -->
<section class="section" id="blockB">
  <div class="sec-tag">Section 04 · Block B</div>
  <h2 class="sec-title">Block B — Modern Stack + AI (Weeks 5–8)</h2>
  <p class="sec-sub">Jun 9 – Jul 6 · The differentiator block. New tools dominate, with revision keeping fundamentals warm.</p>

  <!-- WEEK 5 -->
  <article class="week" id="w5">
    <header class="week-header new">
      <span class="week-num">WEEK 05</span>
      <span class="week-mode mode-new">New-Concept-Led</span>
      <span class="week-title">API Testing — Postman + Rest Assured (new) · Java OOP refresh</span>
      <span class="week-date">Jun 9–15</span>
    </header>
    <div class="week-body">
      <div class="duo">
        <div class="col rev">
          <h4>🔁 Revise (Java OOP for Rest Assured)</h4>
          <ul>
            <li>Collections: List, Map, Set — used heavily in JSON parsing</li>
            <li>Static vs instance, builder pattern (Rest Assured uses it)</li>
            <li>Try-with-resources, exception hierarchy</li>
          </ul>
        </div>
        <div class="col new">
          <h4>✨ New (API Automation)</h4>
          <ul>
            <li>Postman: collections, environments, pre-request scripts, Newman CLI</li>
            <li>Rest Assured: <code>given().when().then()</code> chain</li>
            <li>Auth: Bearer tokens, Basic, OAuth2 concept</li>
            <li>Response assertions on body fields, schema validation</li>
          </ul>
        </div>
      </div>
      <div class="udemy">
        <div class="udemy-title">Udemy — Recommended This Week</div>
        <ul class="udemy-list">
          <li><strong>Postman: The Complete Guide - REST API Testing</strong> <span class="instr">— Valentin Despa</span>
            <span class="sec">▸ Sections 1–8 (Requests, Collections, Variables, Scripts, Newman). Highly rated.</span></li>
          <li><strong>REST Assured API Automation, Postman &amp; API Testing</strong> <span class="instr">— Rahul Shetty</span>
            <span class="sec">▸ Sections on Rest Assured basics, JSON path, schema validation.</span></li>
          <li><strong>Java Programming Masterclass updated to Java 17</strong> <span class="instr">— Tim Buchalka</span>
            <span class="sec">▸ Only the Collections + OOP refresher sections — skip the rest.</span></li>
        </ul>
      </div>
      <div class="practical">
        <div class="practical-title">Practical Build</div>
        <p>Add an <code>/api</code> module to your repo with 5+ Rest Assured tests on reqres.in. Export a Postman collection beside it. <strong>Push.</strong></p>
      </div>
      <div class="deliverables"><span class="del del-gh">API tests pushed</span><span class="del del-skill">Postman fluent</span></div>
    </div>
  </article>

  <!-- WEEK 6 -->
  <article class="week" id="w6">
    <header class="week-header rev">
      <span class="week-num">WEEK 06</span>
      <span class="week-mode mode-rev">Revision-Led</span>
      <span class="week-title">Maven + Reports (revise) · GitHub Actions CI (new)</span>
      <span class="week-date">Jun 16–22</span>
    </header>
    <div class="week-body">
      <div class="duo">
        <div class="col rev">
          <h4>🔁 Revise (Maven, Reports)</h4>
          <ul>
            <li><code>pom.xml</code> structure, dependency scopes, surefire plugin</li>
            <li>Extent Reports / Allure setup</li>
            <li>Profiles for smoke/regression</li>
          </ul>
        </div>
        <div class="col new">
          <h4>✨ New (CI/CD)</h4>
          <ul>
            <li>What CI/CD means in QA context</li>
            <li>GitHub Actions YAML: <code>on</code>, <code>jobs</code>, <code>steps</code>, <code>uses</code>, <code>run</code></li>
            <li>Run Maven tests headless on push, upload report artifact</li>
            <li>Jenkins — concept-only (declarative pipeline syntax)</li>
          </ul>
        </div>
      </div>
      <div class="udemy">
        <div class="udemy-title">Udemy — Recommended This Week</div>
        <ul class="udemy-list">
          <li><strong>The Complete GitHub Actions &amp; Workflows Guide</strong> <span class="instr">— Maximilian Schwarzmüller</span>
            <span class="sec">▸ Sections 1–6 (Workflow basics, Jobs, Artifacts, Triggers).</span></li>
          <li><strong>Jenkins, From Zero To Hero</strong> <span class="instr">— Eduardo Janicas</span>
            <span class="sec">▸ Concept overview + Declarative Pipeline section only (no install needed).</span></li>
        </ul>
      </div>
      <div class="practical">
        <div class="practical-title">Practical Build</div>
        <p>Add <code>.github/workflows/ci.yml</code> to the repo. On every push to main: install JDK, run <code>mvn test</code> (headless Chrome), upload Surefire report as artifact. <strong>Green badge in README.</strong></p>
      </div>
      <div class="deliverables"><span class="del del-gh">CI green badge live</span></div>
    </div>
  </article>

  <!-- WEEK 7 -->
  <article class="week" id="w7">
    <header class="week-header new">
      <span class="week-num">WEEK 07</span>
      <span class="week-mode mode-new">New-Concept-Led</span>
      <span class="week-title">Playwright + TypeScript (new) · Locator strategy (revise)</span>
      <span class="week-date">Jun 23–29</span>
    </header>
    <div class="week-body">
      <div class="duo">
        <div class="col rev">
          <h4>🔁 Revise (Locator Strategy)</h4>
          <ul>
            <li>Why role-based / accessible locators &gt; XPath</li>
            <li>Compare Selenium <code>By.xpath</code> vs Playwright <code>getByRole</code></li>
            <li>Test stability principles (no brittle selectors)</li>
          </ul>
        </div>
        <div class="col new">
          <h4>✨ New (Playwright + TS)</h4>
          <ul>
            <li>Node + npm + TypeScript basics</li>
            <li>Playwright install, project init, codegen tool</li>
            <li><code>getByRole / getByText / getByLabel</code>, auto-wait</li>
            <li><code>playwright.config.ts</code>, HTML reporter, screenshots/video on failure</li>
            <li>Page Object pattern in Playwright style</li>
          </ul>
        </div>
      </div>
      <div class="udemy">
        <div class="udemy-title">Udemy — Recommended This Week</div>
        <ul class="udemy-list">
          <li><strong>Playwright: Web Automation Testing From Zero to Hero</strong> <span class="instr">— Artem Bondar</span>
            <span class="sec">▸ Sections 1–8 (Setup, Locators, Assertions, POM, Config, Reports). The leading Playwright course.</span></li>
          <li><strong>Understanding TypeScript</strong> <span class="instr">— Maximilian Schwarzmüller</span>
            <span class="sec">▸ Only Sections 1–3 (Basics, Types, Classes) — enough for Playwright.</span></li>
        </ul>
      </div>
      <div class="practical">
        <div class="practical-title">Practical Build · Repo #2</div>
        <p>New repo <strong>playwright-ts-portfolio</strong>. Re-implement saucedemo login + cart in Playwright + TS. Add GitHub Actions CI. <strong>Push.</strong></p>
      </div>
      <div class="deliverables"><span class="del del-gh">Playwright repo live</span><span class="del del-gh">CI on Playwright</span></div>
    </div>
  </article>

  <!-- WEEK 8 -->
  <article class="week" id="w8">
    <header class="week-header mix">
      <span class="week-num">WEEK 08</span>
      <span class="week-mode mode-mix">Mixed</span>
      <span class="week-title">AI/LLM Fundamentals (new) · Formalize GenAI Work Story (revise)</span>
      <span class="week-date">Jun 30 – Jul 6</span>
    </header>
    <div class="week-body">
      <div class="duo">
        <div class="col rev">
          <h4>🔁 Revise (Your Own GenAI Use)</h4>
          <ul>
            <li>List every Copilot/LLM use-case from the past 6 months at work</li>
            <li>Convert each into a STAR story (Situation/Task/Action/Result)</li>
            <li>Identify the 3 strongest as resume bullets</li>
          </ul>
        </div>
        <div class="col new">
          <h4>✨ New (LLM Concepts)</h4>
          <ul>
            <li>Tokens, context window, temperature, top-p, hallucination</li>
            <li>Prompt engineering: Role + Context + Task + Format</li>
            <li>Few-shot vs zero-shot, chain-of-thought</li>
            <li>RAG concept (high-level)</li>
            <li>Tools landscape: Copilot, Cursor, Claude, ChatGPT</li>
          </ul>
        </div>
      </div>
      <div class="udemy">
        <div class="udemy-title">Udemy — Recommended This Week</div>
        <ul class="udemy-list">
          <li><strong>ChatGPT &amp; LangChain: The Complete Developer's Masterclass</strong> <span class="instr">— Stephen Grider</span>
            <span class="sec">▸ Only Sections 1–3 (LLM basics, Prompting, Tokens). Skip LangChain build for now.</span></li>
          <li><strong>The Complete Prompt Engineering for AI Bootcamp</strong> <span class="instr">— Mike Taylor &amp; James Phoenix</span>
            <span class="sec">▸ Sections on prompt structure, few-shot, formatting outputs.</span></li>
          <li><strong>AI for QA / Testing with ChatGPT &amp; AI Tools</strong> <span class="instr">— Rahul Shetty</span>
            <span class="sec">▸ Watch end-to-end (it's short) — gives ready-made interview vocabulary.</span></li>
        </ul>
      </div>
      <div class="practical">
        <div class="practical-title">Practical Build</div>
        <p>Create <code>AI_QA_CASE_STUDY.md</code> in your repo with 3–4 STAR-format GenAI stories from your job. <strong>Push.</strong> This becomes the AI section of your resume.</p>
      </div>
      <div class="deliverables"><span class="del del-skill">LLM vocabulary fluent</span><span class="del del-gh">AI case study live</span></div>
    </div>
  </article>
</section>

<!-- ═══ BLOCK C ═══ -->
<section class="section" id="blockC">
  <div class="sec-tag">Section 05 · Block C</div>
  <h2 class="sec-title">Block C — Advanced Skills + Portfolio Lock (Weeks 9–11)</h2>
  <p class="sec-sub">Jul 7 – Jul 27 · Differentiation skills + final polish.</p>

  <!-- WEEK 9 -->
  <article class="week" id="w9">
    <header class="week-header new">
      <span class="week-num">WEEK 09</span>
      <span class="week-mode mode-new">New-Concept-Led</span>
      <span class="week-title">Docker (new) · Selenium Grid (revise concept)</span>
      <span class="week-date">Jul 7–13</span>
    </header>
    <div class="week-body">
      <div class="duo">
        <div class="col rev">
          <h4>🔁 Revise (Grid Concept)</h4>
          <ul>
            <li>Why parallel execution matters</li>
            <li>Hub/Node model conceptually</li>
            <li>TestNG parallel attribute</li>
          </ul>
        </div>
        <div class="col new">
          <h4>✨ New (Docker)</h4>
          <ul>
            <li>Containers vs VMs, image vs container</li>
            <li><code>docker run / ps / logs / exec / stop</code></li>
            <li>Writing a Dockerfile for the Java test project</li>
            <li>docker-compose for Selenium Hub + Chrome node</li>
          </ul>
        </div>
      </div>
      <div class="udemy">
        <div class="udemy-title">Udemy — Recommended This Week</div>
        <ul class="udemy-list">
          <li><strong>Docker Mastery: with Kubernetes + Swarm</strong> <span class="instr">— Bret Fisher</span>
            <span class="sec">▸ Sections 1–6 only (Container basics, Images, Compose). Skip K8s/Swarm for now.</span></li>
          <li><strong>Selenium Grid 4 Tutorial with Docker, Selenoid &amp; Cloud</strong> <span class="instr">— Rahul Shetty / Karthik KK</span>
            <span class="sec">▸ Selenium Grid + Docker integration sections.</span></li>
        </ul>
      </div>
      <div class="practical">
        <div class="practical-title">Practical Build</div>
        <p>Add <code>Dockerfile</code> + <code>docker-compose.yml</code> to your Selenium repo. Spin hub + 1 chrome node. Run tests in parallel against the grid. <strong>Push.</strong></p>
      </div>
      <div class="deliverables"><span class="del del-gh">Dockerised suite</span><span class="del del-skill">Grid working</span></div>
    </div>
  </article>

  <!-- WEEK 10 -->
  <article class="week" id="w10">
    <header class="week-header new">
      <span class="week-num">WEEK 10</span>
      <span class="week-mode mode-new">New-Concept-Led</span>
      <span class="week-title">Performance (k6, new) · LLM Eval (deepeval, new) · API recap</span>
      <span class="week-date">Jul 14–20</span>
    </header>
    <div class="week-body">
      <div class="duo">
        <div class="col rev">
          <h4>🔁 Revise (API + Test Types)</h4>
          <ul>
            <li>Recap Rest Assured suite — make sure CI is still green</li>
            <li>Test pyramid revisited: unit / integration / e2e / perf</li>
          </ul>
        </div>
        <div class="col new">
          <h4>✨ New (Perf + LLM Eval)</h4>
          <ul>
            <li>Load vs stress vs spike vs endurance vs soak</li>
            <li>k6 install + first script against a public API</li>
            <li>Throughput, P95/P99 response time, error rate</li>
            <li>deepeval / promptfoo: writing one LLM correctness test</li>
            <li>Hallucination + relevance + bias evaluation concepts</li>
          </ul>
        </div>
      </div>
      <div class="udemy">
        <div class="udemy-title">Udemy — Recommended This Week</div>
        <ul class="udemy-list">
          <li><strong>k6 Performance Testing for Beginners</strong> <span class="instr">— search latest top-rated · or ·</strong> Performance Testing using JMeter — Rahul Shetty</span>
            <span class="sec">▸ Concepts + first scripted test. JMeter sections are interchangeable for vocabulary.</span></li>
          <li><strong>LangChain + LLM Testing / Evaluation modules</strong> <span class="instr">— in Stephen Grider's course</span>
            <span class="sec">▸ Skip code-along; absorb concepts of eval datasets and scoring.</span></li>
        </ul>
      </div>
      <div class="practical">
        <div class="practical-title">Practical Build</div>
        <p>Add a <code>/perf</code> folder with one k6 script + an <code>/llm-evals</code> folder with one deepeval test. <strong>Push.</strong> Even tiny examples become unique resume bullets.</p>
      </div>
      <div class="deliverables"><span class="del del-skill">k6 script written</span><span class="del del-skill">LLM eval written</span></div>
    </div>
  </article>

  <!-- WEEK 11 -->
  <article class="week" id="w11">
    <header class="week-header mix">
      <span class="week-num">WEEK 11</span>
      <span class="week-mode mode-mix">Build / Consolidation</span>
      <span class="week-title">Portfolio Lock + Resume + LinkedIn</span>
      <span class="week-date">Jul 21–27</span>
    </header>
    <div class="week-body">
      <p style="color:var(--muted);font-size:13px;"><strong>No new content.</strong> Convert everything built into job-search assets.</p>
      <ul class="col" style="border:none;background:transparent;padding:0;">
        <li style="color:var(--muted);font-size:13px;padding:6px 0;">▸ <strong>Repo audit:</strong> every repo has clean README, passing CI badge, no half-merged branches.</li>
        <li style="color:var(--muted);font-size:13px;padding:6px 0;">▸ <strong>Resume rebuild:</strong> tailor for SDET / AI-QA. Lead with stack (Selenium 4, Playwright, Rest Assured, Docker, GitHub Actions, k6, GenAI). For each bullet — what + stack + impact.</li>
        <li style="color:var(--muted);font-size:13px;padding:6px 0;">▸ <strong>LinkedIn:</strong> headline → "SDET · AI-QA · Selenium · Playwright · GenAI Testing". Link both repos. Publish AI case study as an article.</li>
      </ul>
      <div class="udemy">
        <div class="udemy-title">Udemy — Optional</div>
        <ul class="udemy-list">
          <li><strong>The Complete Job Interviewing Skills Masterclass</strong> <span class="instr">— Chris Croft / TJ Walker</span>
            <span class="sec">▸ Resume + LinkedIn-focused modules.</span></li>
        </ul>
      </div>
      <div class="deliverables"><span class="del del-job">Resume v1</span><span class="del del-job">LinkedIn updated</span><span class="del del-gh">All repos polished</span></div>
    </div>
  </article>
</section>

<!-- ═══ BLOCK D ═══ -->
<section class="section" id="blockD">
  <div class="sec-tag">Section 06 · Block D</div>
  <h2 class="sec-title">Block D — Interview Prep + Applications (Weeks 12–15)</h2>
  <p class="sec-sub">Jul 28 – Aug 31 · No new tools. Convert build into interview performance.</p>

  <div class="g2">
    <article class="week" id="w12">
      <header class="week-header rev">
        <span class="week-num">WEEKS 12–13</span>
        <span class="week-mode mode-rev">Revise + Mock</span>
        <span class="week-title">Mock Interviews Begin · Light DSA</span>
        <span class="week-date">Jul 28 – Aug 10</span>
      </header>
      <div class="week-body">
        <div class="topic-row">
          <span class="topic t-rev">Framework architecture talk-through</span>
          <span class="topic t-rev">Test design Qs</span>
          <span class="topic t-new">DSA: Arrays, Strings</span>
          <span class="topic t-new">DSA: HashMap, 2-pointer</span>
        </div>
        <ul class="col" style="background:transparent;border:none;padding:0;">
          <li style="color:var(--muted);font-size:13px;padding:5px 0;">▸ 2 mocks/week (peers / Pramp / Interviewing.io free credits).</li>
          <li style="color:var(--muted);font-size:13px;padding:5px 0;">▸ 5 applications/week — Browserstack, Freshworks, Postman, Razorpay, Zoho, Atlassian India, Series B/C startups.</li>
          <li style="color:var(--muted);font-size:13px;padding:5px 0;">▸ 5 easy DSA questions/week. No grinding.</li>
        </ul>
        <div class="udemy">
          <div class="udemy-title">Udemy — Recommended</div>
          <ul class="udemy-list">
            <li><strong>Master the Coding Interview: Data Structures + Algorithms</strong> <span class="instr">— Andrei Neagoie</span>
              <span class="sec">▸ Arrays, Strings, HashMaps, Two Pointer sections only.</span></li>
            <li><strong>Selenium WebDriver Interview Questions Preparation Course</strong> <span class="instr">— Rahul Shetty</span>
              <span class="sec">▸ Watch as a refresher for screening questions.</span></li>
          </ul>
        </div>
      </div>
    </article>

    <article class="week" id="w14">
      <header class="week-header mix">
        <span class="week-num">WEEKS 14–15</span>
        <span class="week-mode mode-mix">Application Push</span>
        <span class="week-title">Full Volume + Behavioural Polish</span>
        <span class="week-date">Aug 11 – Aug 31</span>
      </header>
      <div class="week-body">
        <div class="topic-row">
          <span class="topic t-prac">10+ applications/week</span>
          <span class="topic t-rev">STAR behavioural stories</span>
          <span class="topic t-rev">Salary negotiation prep</span>
        </div>
        <ul class="col" style="background:transparent;border:none;padding:0;">
          <li style="color:var(--muted);font-size:13px;padding:5px 0;">▸ Tracker spreadsheet — company, role, date, status, next step.</li>
          <li style="color:var(--muted);font-size:13px;padding:5px 0;">▸ Continue 2 mocks/week. By now answers should be near-automatic.</li>
          <li style="color:var(--muted);font-size:13px;padding:5px 0;">▸ Salary script for the 8–10 LPA target band.</li>
        </ul>
        <div class="udemy">
          <div class="udemy-title">Udemy — Optional</div>
          <ul class="udemy-list">
            <li><strong>Salary Negotiation - How to Ask for and Receive a Pay Raise</strong> <span class="instr">— Various top-rated</span>
              <span class="sec">▸ One sitting before first offer call.</span></li>
          </ul>
        </div>
      </div>
    </article>
  </div>

  <div class="callout teal" style="margin-top:18px;">
    <div class="callout-title">🎯 Sep 1 Onward · Active Interview Phase</div>
    <ul>
      <li>Active interviews begin Sep 1. August applications start converting.</li>
      <li>Apply broadly: Browserstack, Freshworks, Postman, Razorpay, Zoho, Atlassian India, Hasura, Setu, Groww, PhonePe, Juspay, any Series B/C product startup remote/Bangalore/Hyderabad/Pune.</li>
      <li><strong>Mid-October — papers down</strong> after offer-in-hand and notice negotiated.</li>
    </ul>
  </div>
</section>

<!-- ═══ UDEMY MASTER MAP ═══ -->
<section class="section" id="udemy-master">
  <div class="sec-tag">Section 07</div>
  <h2 class="sec-title">Udemy Master Course Map</h2>
  <p class="sec-sub">All recommended courses in one place — search exact titles in your enterprise Udemy. Use 1.5–1.75× speed; watch only the listed sections; build alongside.</p>

  <table class="data-table">
    <thead><tr><th>Skill Area</th><th>Course Title</th><th>Instructor</th><th>Use For</th><th>Wks</th></tr></thead>
    <tbody>
      <tr><td><strong>Selenium / Java</strong></td><td>Selenium WebDriver with Java -Basics to Advanced+ Frameworks</td><td>Rahul Shetty</td><td>Core revival, POM, TestNG, framework design</td><td>1, 2</td></tr>
      <tr><td><strong>Selenium (alt)</strong></td><td>Selenium WebDriver with Java &amp; Cucumber BDD</td><td>Naveen AutomationLabs</td><td>Alternate teaching style, BDD examples</td><td>1–3</td></tr>
      <tr><td><strong>Git</strong></td><td>Git Complete: The definitive, step-by-step guide</td><td>Jason Taylor</td><td>Branching, merging, rebase, PRs</td><td>1</td></tr>
      <tr><td><strong>Linux CLI</strong></td><td>Linux Mastery: Master the Linux Command Line in 11.5 Hours</td><td>Ziyad Yehia</td><td>Filesystem, permissions, pipes, shell scripting</td><td>2, 5</td></tr>
      <tr><td><strong>BDD / Cucumber</strong></td><td>BDD with Cucumber, Selenium, Java, Junit &amp; Live Project</td><td>Rahul Shetty</td><td>Gherkin, hooks, runner, tags</td><td>3</td></tr>
      <tr><td><strong>SQL</strong></td><td>The Complete SQL Bootcamp</td><td>Jose Portilla</td><td>SELECT, JOINs, GROUP BY, subqueries</td><td>3</td></tr>
      <tr><td><strong>HTTP / REST + Postman</strong></td><td>Postman: The Complete Guide - REST API Testing</td><td>Valentin Despa</td><td>HTTP fundamentals, Postman mastery, Newman</td><td>3, 5</td></tr>
      <tr><td><strong>Rest Assured</strong></td><td>REST Assured API Automation, Postman &amp; API Testing</td><td>Rahul Shetty</td><td>Rest Assured chain, JSON path, schema</td><td>5</td></tr>
      <tr><td><strong>Java OOP refresh</strong></td><td>Java Programming Masterclass updated to Java 17</td><td>Tim Buchalka</td><td>Collections, OOP — only the relevant sections</td><td>5</td></tr>
      <tr><td><strong>CI/CD</strong></td><td>The Complete GitHub Actions &amp; Workflows Guide</td><td>Maximilian Schwarzmüller</td><td>YAML workflows, jobs, artifacts</td><td>6</td></tr>
      <tr><td><strong>Jenkins (concept)</strong></td><td>Jenkins, From Zero To Hero</td><td>Eduardo Janicas</td><td>Declarative pipeline syntax for interviews</td><td>6</td></tr>
      <tr><td><strong>Playwright</strong></td><td>Playwright: Web Automation Testing From Zero to Hero</td><td>Artem Bondar</td><td>Modern UI automation in TS</td><td>7</td></tr>
      <tr><td><strong>TypeScript</strong></td><td>Understanding TypeScript</td><td>Maximilian Schwarzmüller</td><td>Just enough TS for Playwright</td><td>7</td></tr>
      <tr><td><strong>LLM basics</strong></td><td>ChatGPT &amp; LangChain: The Complete Developer's Masterclass</td><td>Stephen Grider</td><td>LLM concepts, tokens, prompting</td><td>8, 10</td></tr>
      <tr><td><strong>Prompt Engineering</strong></td><td>The Complete Prompt Engineering for AI Bootcamp</td><td>Mike Taylor &amp; James Phoenix</td><td>Structured prompting, formats, few-shot</td><td>8</td></tr>
      <tr><td><strong>AI for QA</strong></td><td>AI for QA / Testing with ChatGPT &amp; AI Tools</td><td>Rahul Shetty</td><td>Interview vocabulary, AI in test workflows</td><td>8</td></tr>
      <tr><td><strong>Docker</strong></td><td>Docker Mastery: with Kubernetes + Swarm</td><td>Bret Fisher</td><td>Containers, images, compose</td><td>9</td></tr>
      <tr><td><strong>Selenium Grid + Docker</strong></td><td>Selenium Grid 4 Tutorial with Docker, Selenoid &amp; Cloud</td><td>Karthik KK / Rahul Shetty</td><td>Parallel execution patterns</td><td>9</td></tr>
      <tr><td><strong>Performance</strong></td><td>Performance Testing using JMeter from Scratch (or k6 equivalent)</td><td>Rahul Shetty</td><td>Concepts + first script</td><td>10</td></tr>
      <tr><td><strong>DSA (light)</strong></td><td>Master the Coding Interview: Data Structures + Algorithms</td><td>Andrei Neagoie</td><td>Arrays/Strings/HashMaps/2-pointer</td><td>12–13</td></tr>
      <tr><td><strong>Interview prep</strong></td><td>Selenium WebDriver Interview Questions Preparation Course</td><td>Rahul Shetty</td><td>Screening question fluency</td><td>12–15</td></tr>
    </tbody>
  </table>

  <div class="callout amber" style="margin-top:18px;">
    <div class="callout-title">📺 How to Consume Udemy Efficiently</div>
    <ul>
      <li><strong>1.5×–1.75× speed</strong> always. Slow down only for hands-on coding sections.</li>
      <li>Watch the section, <strong>then build the same thing</strong> against saucedemo / your own repo. Never watch &gt;90 min without coding.</li>
      <li>Use the Q&amp;A tab when stuck — many answers are already there.</li>
      <li>Bookmark the <strong>code resources</strong> attached to each section; treat them as cheatsheets.</li>
      <li>Skip introduction / "what is testing" sections in courses you've already worked with.</li>
    </ul>
  </div>
</section>

<!-- ═══ PLAYLISTS ═══ -->
<section class="section" id="playlists">
  <div class="sec-tag">Section 08</div>
  <h2 class="sec-title">Curated YouTube Playlists (Free Reinforcement)</h2>
  <p class="sec-sub">30 min/day max. Pair with Udemy — these clarify concepts when a Udemy section feels dense.</p>

  <div class="g3">
    <div class="stat-card" style="text-align:left;">
      <div style="font-weight:700;color:#fff;font-size:13px;margin-bottom:6px;">Naveen AutomationLabs</div>
      <div style="color:var(--muted);font-size:12px;line-height:1.6;">Selenium 4, Playwright, Java collections, framework design. Search: <em>"Selenium 4 Playlist"</em>, <em>"Playwright Series"</em>.</div>
    </div>
    <div class="stat-card" style="text-align:left;">
      <div style="font-weight:700;color:#fff;font-size:13px;margin-bottom:6px;">Rahul Shetty Academy (YT)</div>
      <div style="color:var(--muted);font-size:12px;line-height:1.6;">Free intros to most paid courses. Use to "preview" before committing to Udemy section.</div>
    </div>
    <div class="stat-card" style="text-align:left;">
      <div style="font-weight:700;color:#fff;font-size:13px;margin-bottom:6px;">Execute Automation</div>
      <div style="color:var(--muted);font-size:12px;line-height:1.6;">Strong Playwright + TypeScript playlist; CI/CD with Playwright walkthroughs.</div>
    </div>
    <div class="stat-card" style="text-align:left;">
      <div style="font-weight:700;color:#fff;font-size:13px;margin-bottom:6px;">TechWorld with Nana</div>
      <div style="color:var(--muted);font-size:12px;line-height:1.6;">Best free Docker + GitHub Actions + Jenkins explainers. Watch the <em>"Docker Tutorial for Beginners"</em> full video.</div>
    </div>
    <div class="stat-card" style="text-align:left;">
      <div style="font-weight:700;color:#fff;font-size:13px;margin-bottom:6px;">Coding with John / Amigoscode</div>
      <div style="color:var(--muted);font-size:12px;line-height:1.6;">Java fundamentals refreshers — collections, streams, OOP.</div>
    </div>
    <div class="stat-card" style="text-align:left;">
      <div style="font-weight:700;color:#fff;font-size:13px;margin-bottom:6px;">freeCodeCamp.org</div>
      <div style="color:var(--muted);font-size:12px;line-height:1.6;">Long-form: <em>"Linux Crash Course"</em>, <em>"SQL Tutorial - Full Course for Beginners"</em>, <em>"Playwright Full Course"</em>.</div>
    </div>
    <div class="stat-card" style="text-align:left;">
      <div style="font-weight:700;color:#fff;font-size:13px;margin-bottom:6px;">Krish Naik / Andrej Karpathy</div>
      <div style="color:var(--muted);font-size:12px;line-height:1.6;">For LLM internals. Karpathy's <em>"Intro to Large Language Models"</em> 1-hour talk is the single best LLM concept video.</div>
    </div>
    <div class="stat-card" style="text-align:left;">
      <div style="font-weight:700;color:#fff;font-size:13px;margin-bottom:6px;">ByteByteGo</div>
      <div style="color:var(--muted);font-size:12px;line-height:1.6;">5–10 min animated explainers — HTTP, REST vs gRPC, CI/CD pipelines, Docker. Great for interview revision.</div>
    </div>
    <div class="stat-card" style="text-align:left;">
      <div style="font-weight:700;color:#fff;font-size:13px;margin-bottom:6px;">Testing Mini Bytes</div>
      <div style="color:var(--muted);font-size:12px;line-height:1.6;">Indian SDET interview-question walk-throughs — useful in Block D mock prep.</div>
    </div>
  </div>
</section>

<!-- ═══ SKILL MAP ═══ -->
<section class="section" id="skills">
  <div class="sec-tag">Section 09</div>
  <h2 class="sec-title">Skill Confidence Map · May → September</h2>
  <p class="sec-sub">Where each skill stands today vs target. The alternating cadence is what makes the new-skill targets achievable.</p>

  <table class="data-table">
    <thead><tr><th>Skill</th><th>Now (May 14)</th><th>Target (Sep 1)</th><th>Block</th><th>Mode</th></tr></thead>
    <tbody>
      <tr><td><strong>Selenium / Java</strong></td><td>3/10 (decay)</td><td>7.5/10</td><td>A</td><td>REVISE</td></tr>
      <tr><td><strong>TestNG / JUnit</strong></td><td>3/10</td><td>7/10</td><td>A</td><td>REVISE</td></tr>
      <tr><td><strong>BDD / Cucumber</strong></td><td>3/10</td><td>7/10</td><td>A</td><td>REVISE</td></tr>
      <tr><td><strong>Git advanced</strong></td><td>4/10</td><td>8/10</td><td>A</td><td>NEW</td></tr>
      <tr><td><strong>Linux CLI</strong></td><td>2/10</td><td>7/10</td><td>A+B</td><td>NEW</td></tr>
      <tr><td><strong>SQL (QA context)</strong></td><td>2/10</td><td>6/10</td><td>A</td><td>NEW</td></tr>
      <tr><td><strong>HTTP / REST</strong></td><td>3/10</td><td>8/10</td><td>A+B</td><td>NEW</td></tr>
      <tr><td><strong>Postman + Rest Assured</strong></td><td>4/10</td><td>7.5/10</td><td>B</td><td>NEW</td></tr>
      <tr><td><strong>GitHub Actions CI/CD</strong></td><td>1/10</td><td>6.5/10</td><td>B</td><td>NEW</td></tr>
      <tr><td><strong>Playwright + TS</strong></td><td>0/10</td><td>6/10</td><td>B</td><td>NEW</td></tr>
      <tr><td><strong>AI / LLM fundamentals</strong></td><td>3/10</td><td>7/10</td><td>B</td><td>NEW</td></tr>
      <tr><td><strong>GenAI applied (work)</strong></td><td>7/10</td><td>8/10</td><td>B</td><td>FORMALIZE</td></tr>
      <tr><td><strong>Docker</strong></td><td>0/10</td><td>5.5/10</td><td>C</td><td>NEW</td></tr>
      <tr><td><strong>Performance (k6)</strong></td><td>1/10</td><td>5/10</td><td>C</td><td>NEW</td></tr>
      <tr><td><strong>LLM Eval (deepeval)</strong></td><td>1/10</td><td>5/10</td><td>C</td><td>NEW</td></tr>
      <tr><td><strong>DSA (light)</strong></td><td>1.5/10</td><td>3/10 (enough)</td><td>D</td><td>NEW</td></tr>
    </tbody>
  </table>
</section>

<!-- ═══ WEEKLY SYSTEM ═══ -->
<section class="section" id="rules">
  <div class="sec-tag">Section 10</div>
  <h2 class="sec-title">Weekly Non-Negotiables (Burst-Mode Friendly)</h2>
  <div class="g2">
    <div class="callout teal">
      <div class="callout-title">✅ Every Week — Must Hit (Blocks A–C)</div>
      <ul>
        <li><strong>1 GitHub commit</strong> minimum.</li>
        <li><strong>4 hrs skill work</strong> — split across 2 sessions max.</li>
        <li><strong>1 Udemy section</strong> from this week's recommendation.</li>
        <li><strong>1 fundamental practiced</strong> (Linux/SQL/HTTP/Docker/CI).</li>
        <li><strong>30 min curated content</strong> — playlists above only.</li>
      </ul>
    </div>
    <div class="callout red">
      <div class="callout-title">❌ Hard Limits</div>
      <ul>
        <li>No new Udemy course outside the map until current week's section is done.</li>
        <li>No DSA beyond 5 easy/week before Block D.</li>
        <li>No applying before GitHub repo is live (Week 4+).</li>
        <li>No comparing GitHub graphs on LinkedIn.</li>
        <li>No adding tools to the plan — the stack is locked.</li>
      </ul>
    </div>
  </div>
  <div class="callout amber" style="margin-top:14px;">
    <div class="callout-title">📊 Monthly Check-In (14th of each month)</div>
    <ul>
      <li>Hit weekly minimums 3 of 4 weeks? If no — what blocked it?</li>
      <li>What's new on GitHub since last month?</li>
      <li>How many applications? Responses? Patterns?</li>
      <li>Which topic can I now explain confidently that I couldn't last month?</li>
    </ul>
  </div>
</section>

<!-- ═══ HOW TO SHARE ═══ -->
<section class="section" id="share">
  <div class="sec-tag">Section 11</div>
  <h2 class="sec-title">How to Share &amp; View This Document</h2>
  <p class="sec-sub">This file is a single self-contained HTML document — no build step, no external assets beyond Google Fonts. Multiple viewing options below.</p>

  <div class="g2">
    <div class="callout blue">
      <div class="callout-title">👁 View Locally</div>
      <ul>
        <li>Double-click the file — it opens in any modern browser (Chrome, Edge, Firefox, Safari).</li>
        <li>Works offline (fonts fall back to system fonts if no internet).</li>
        <li>Mobile-responsive — open on phone via cloud drive link.</li>
      </ul>
    </div>
    <div class="callout purple">
      <div class="callout-title">📤 Share with Others</div>
      <ul>
        <li><strong>Email/Chat:</strong> attach the <code>.html</code> file directly — recipient just double-clicks.</li>
        <li><strong>OneDrive / Google Drive:</strong> upload &amp; share view link (set permission to "Anyone with link can view").</li>
        <li><strong>GitHub Pages:</strong> push to a public repo, enable Pages on the main branch, share the <code>github.io</code> URL.</li>
        <li><strong>PDF export:</strong> <kbd>Ctrl/Cmd + P</kbd> → <em>Save as PDF</em>. Print styles already optimized for clean output.</li>
      </ul>
    </div>
  </div>
  <div class="callout teal" style="margin-top:14px;">
    <div class="callout-title">♿ Accessibility Built In</div>
    <ul>
      <li>Semantic HTML5 landmarks (<code>nav</code>, <code>header</code>, <code>main</code>, <code>section</code>, <code>article</code>).</li>
      <li>Skip-to-content link for keyboard users.</li>
      <li>Sticky in-page navigation for fast section jumping.</li>
      <li>High-contrast palette; print stylesheet for B&amp;W output.</li>
      <li>Mobile-first responsive grid down to 320px width.</li>
    </ul>
  </div>
</section>

<!-- ═══ VERDICT ═══ -->
<section class="section" id="verdict" style="border-bottom:none;">
  <div class="sec-tag">Section 12</div>
  <h2 class="sec-title">The Closing Note</h2>

  <div class="verdict">
    <p>The accident cost weeks. The new cadence buys back retention.</p>
    <p>Alternating revision and new-concept weeks does two things at once: it keeps the brain fresh by avoiding monotony, and it locks each new tool against an existing one — Selenium against Playwright, Postman against Rest Assured, JMeter against k6. Pattern recognition replaces brute memorization.</p>
    <p>The Udemy map removes "what should I learn next?" friction. Open the week, open the listed section, watch at 1.5×, build alongside, push by Sunday. Repeat for 15 weeks.</p>
    <p style="color:var(--gold);font-weight:600;">Week 1 is the only hard week. Open the laptop today.</p>
  </div>

  <div class="g3" style="margin-top:24px;">
    <div class="stat-card"><div class="stat-num teal">15</div><div class="stat-label">Weeks of alternating cadence</div></div>
    <div class="stat-card"><div class="stat-num purple">21</div><div class="stat-label">Curated Udemy course references</div></div>
    <div class="stat-card"><div class="stat-num gold">Today</div><div class="stat-label">When Week 1 begins</div></div>
  </div>

  <p style="text-align:center;font-family:'JetBrains Mono',monospace;font-size:10px;color:var(--dim);margin-top:40px;">
    Aman · Roadmap v2 · Alternating Cadence · May 14, 2025 — next checkpoint Jun 14, 2025
  </p>
</section>

</main>
</body>
</html>
