<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>GitHub Profile Preview — lakshayaraanaa</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet" />
<style>
  :root {
    --bg: #050810;
    --surface: #0d1117;
    --surface2: #161b22;
    --border: #21262d;
    --react: #61DAFB;
    --react2: #00b4d8;
    --accent: #ff6b6b;
    --gold: #f9c74f;
    --green: #39d353;
    --text: #e6edf3;
    --muted: #7d8590;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    font-family: 'Space Mono', monospace;
    color: var(--text);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Animated bg grid */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(97,218,251,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(97,218,251,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .wrapper {
    position: relative;
    z-index: 1;
    max-width: 860px;
    margin: 0 auto;
    padding: 40px 24px 80px;
  }

  /* ─── HERO ─── */
  .hero {
    text-align: center;
    padding: 60px 0 50px;
    position: relative;
  }

  .hero::after {
    content: '';
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 500px;
    height: 500px;
    background: radial-gradient(circle, rgba(97,218,251,0.08) 0%, transparent 70%);
    pointer-events: none;
    z-index: -1;
  }

  .avatar-wrap {
    display: inline-block;
    position: relative;
    margin-bottom: 24px;
  }

  .avatar {
    width: 110px;
    height: 110px;
    border-radius: 50%;
    border: 3px solid var(--react);
    box-shadow: 0 0 30px rgba(97,218,251,0.3), 0 0 60px rgba(97,218,251,0.1);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 52px;
    background: var(--surface2);
    animation: pulse-ring 3s ease-in-out infinite;
  }

  @keyframes pulse-ring {
    0%, 100% { box-shadow: 0 0 20px rgba(97,218,251,0.3), 0 0 50px rgba(97,218,251,0.1); }
    50% { box-shadow: 0 0 40px rgba(97,218,251,0.5), 0 0 80px rgba(97,218,251,0.2); }
  }

  .status-dot {
    position: absolute;
    bottom: 6px;
    right: 6px;
    width: 18px;
    height: 18px;
    background: var(--green);
    border-radius: 50%;
    border: 3px solid var(--bg);
    animation: blink 2s ease-in-out infinite;
  }

  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.4; }
  }

  .hero-name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2.2rem, 5vw, 3.4rem);
    font-weight: 800;
    letter-spacing: -1px;
    background: linear-gradient(135deg, #61DAFB 0%, #ffffff 50%, #61DAFB 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    line-height: 1.1;
    margin-bottom: 10px;
  }

  .hero-title {
    font-family: 'Space Mono', monospace;
    font-size: 0.95rem;
    color: var(--react);
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-bottom: 20px;
    opacity: 0.9;
  }

  .hero-bio {
    color: var(--muted);
    font-size: 0.85rem;
    line-height: 1.8;
    max-width: 500px;
    margin: 0 auto 28px;
  }

  /* Typing effect */
  .typed {
    display: inline-block;
    font-family: 'Space Mono', monospace;
    font-size: 0.85rem;
    color: var(--react);
    border-right: 2px solid var(--react);
    white-space: nowrap;
    overflow: hidden;
    animation: typing 4s steps(40) infinite, blink-caret 0.8s step-end infinite;
    max-width: 380px;
  }

  @keyframes typing {
    0% { width: 0 }
    40% { width: 100% }
    80% { width: 100% }
    100% { width: 0 }
  }
  @keyframes blink-caret {
    from, to { border-color: transparent }
    50% { border-color: var(--react) }
  }

  /* ─── BADGES ─── */
  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    margin-top: 24px;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    border-radius: 999px;
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
    border: 1px solid;
    transition: all 0.2s ease;
    cursor: default;
  }

  .badge:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 20px rgba(97,218,251,0.2);
  }

  .badge-react { color: #61DAFB; border-color: rgba(97,218,251,0.3); background: rgba(97,218,251,0.08); }
  .badge-js { color: #f9c74f; border-color: rgba(249,199,79,0.3); background: rgba(249,199,79,0.08); }
  .badge-node { color: #4ade80; border-color: rgba(74,222,128,0.3); background: rgba(74,222,128,0.08); }
  .badge-open { color: #c084fc; border-color: rgba(192,132,252,0.3); background: rgba(192,132,252,0.08); }

  /* ─── DIVIDER ─── */
  .divider {
    display: flex;
    align-items: center;
    gap: 16px;
    margin: 40px 0;
  }
  .divider-line { flex: 1; height: 1px; background: linear-gradient(90deg, transparent, var(--border), transparent); }
  .divider-text { color: var(--muted); font-size: 0.7rem; letter-spacing: 3px; text-transform: uppercase; }

  /* ─── CODE BLOCK ─── */
  .code-block {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
    margin-bottom: 32px;
    box-shadow: 0 8px 32px rgba(0,0,0,0.4);
  }

  .code-header {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 12px 18px;
    background: rgba(255,255,255,0.03);
    border-bottom: 1px solid var(--border);
  }

  .dot { width: 12px; height: 12px; border-radius: 50%; }
  .dot-red { background: #ff5f57; }
  .dot-yellow { background: #febc2e; }
  .dot-green { background: #28c840; }

  .code-filename {
    margin-left: 8px;
    font-size: 0.75rem;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
  }

  .code-body {
    padding: 24px 28px;
    font-size: 0.82rem;
    line-height: 2;
    font-family: 'Space Mono', monospace;
  }

  .kw { color: #ff7b72; }
  .fn { color: #d2a8ff; }
  .str { color: #a5d6ff; }
  .key { color: #79c0ff; }
  .cmt { color: #484f58; font-style: italic; }
  .arr { color: #61DAFB; }
  .num { color: #f9c74f; }

  /* ─── SECTION TITLE ─── */
  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .section-title span { color: var(--react); }

  /* ─── TECH GRID ─── */
  .tech-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(130px, 1fr));
    gap: 12px;
    margin-bottom: 32px;
  }

  .tech-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px 12px;
    text-align: center;
    transition: all 0.25s ease;
    cursor: default;
    position: relative;
    overflow: hidden;
  }

  .tech-card::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, var(--glow-color, rgba(97,218,251,0.05)), transparent);
    opacity: 0;
    transition: opacity 0.25s;
  }

  .tech-card:hover { transform: translateY(-4px); border-color: rgba(97,218,251,0.3); }
  .tech-card:hover::before { opacity: 1; }

  .tech-icon { font-size: 2rem; margin-bottom: 8px; display: block; }
  .tech-name { font-size: 0.72rem; color: var(--muted); letter-spacing: 1px; text-transform: uppercase; }
  .tech-level {
    height: 3px;
    background: var(--border);
    border-radius: 99px;
    margin-top: 10px;
    overflow: hidden;
  }
  .tech-level-bar {
    height: 100%;
    border-radius: 99px;
    background: linear-gradient(90deg, var(--react), var(--react2));
    animation: grow 1.5s ease forwards;
  }
  @keyframes grow { from { width: 0 } }

  /* ─── PROJECTS ─── */
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-bottom: 32px;
  }

  @media (max-width: 560px) { .projects-grid { grid-template-columns: 1fr; } }

  .project-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 22px;
    transition: all 0.25s ease;
    position: relative;
    overflow: hidden;
    cursor: pointer;
  }

  .project-card::after {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--card-color1, var(--react)), var(--card-color2, var(--react2)));
  }

  .project-card:hover { transform: translateY(-4px); box-shadow: 0 12px 40px rgba(0,0,0,0.4); border-color: rgba(97,218,251,0.2); }

  .project-emoji { font-size: 1.8rem; margin-bottom: 10px; display: block; }
  .project-name {
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 1rem;
    color: var(--text);
    margin-bottom: 8px;
  }
  .project-desc { font-size: 0.75rem; color: var(--muted); line-height: 1.7; margin-bottom: 14px; }
  .project-tags { display: flex; gap: 6px; flex-wrap: wrap; }
  .project-tag {
    font-size: 0.65rem;
    padding: 3px 8px;
    border-radius: 999px;
    background: rgba(97,218,251,0.1);
    color: var(--react);
    border: 1px solid rgba(97,218,251,0.2);
    letter-spacing: 0.5px;
  }

  /* ─── STATS ─── */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
    margin-bottom: 32px;
  }

  @media (max-width: 500px) { .stats-row { grid-template-columns: 1fr; } }

  .stat-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 24px 16px;
    text-align: center;
    transition: all 0.25s ease;
  }

  .stat-card:hover { transform: translateY(-3px); border-color: rgba(97,218,251,0.3); }

  .stat-number {
    font-family: 'Syne', sans-serif;
    font-size: 2rem;
    font-weight: 800;
    background: linear-gradient(135deg, var(--react), #fff);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    display: block;
    line-height: 1;
    margin-bottom: 8px;
  }

  .stat-label { font-size: 0.7rem; color: var(--muted); letter-spacing: 2px; text-transform: uppercase; }

  /* ─── CONTRIBUTION GRAPH ─── */
  .contrib-section { margin-bottom: 32px; }

  .contrib-grid {
    display: grid;
    grid-template-columns: repeat(52, 1fr);
    gap: 3px;
    margin-top: 16px;
  }

  .contrib-day {
    aspect-ratio: 1;
    border-radius: 2px;
    background: var(--surface2);
    transition: transform 0.1s;
  }

  .contrib-day:hover { transform: scale(1.4); z-index: 10; position: relative; }

  .c1 { background: rgba(57, 211, 83, 0.2); }
  .c2 { background: rgba(57, 211, 83, 0.4); }
  .c3 { background: rgba(57, 211, 83, 0.65); }
  .c4 { background: rgba(57, 211, 83, 0.9); }

  /* ─── CONNECT ─── */
  .connect-links {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 20px;
  }

  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 22px;
    border-radius: 8px;
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
    text-decoration: none;
    border: 1px solid;
    transition: all 0.2s ease;
    font-family: 'Space Mono', monospace;
    color: inherit;
  }

  .btn-github { border-color: rgba(255,255,255,0.2); color: var(--text); background: rgba(255,255,255,0.05); }
  .btn-github:hover { background: rgba(255,255,255,0.1); transform: translateY(-2px); }
  .btn-portfolio { border-color: rgba(97,218,251,0.4); color: var(--react); background: rgba(97,218,251,0.08); }
  .btn-portfolio:hover { background: rgba(97,218,251,0.15); transform: translateY(-2px); box-shadow: 0 4px 20px rgba(97,218,251,0.2); }

  /* ─── FOOTER ─── */
  .footer {
    margin-top: 60px;
    text-align: center;
    padding-top: 32px;
    border-top: 1px solid var(--border);
  }

  .footer-quote {
    font-family: 'Syne', sans-serif;
    font-size: 1.2rem;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 10px;
  }

  .footer-quote em {
    font-style: normal;
    color: var(--react);
  }

  .footer-sub { font-size: 0.72rem; color: var(--muted); letter-spacing: 2px; text-transform: uppercase; }

  /* ─── COPY MD BUTTON ─── */
  .copy-section {
    background: var(--surface2);
    border: 1px dashed rgba(97,218,251,0.3);
    border-radius: 12px;
    padding: 20px;
    text-align: center;
    margin-top: 40px;
  }

  .copy-title { font-size: 0.8rem; color: var(--muted); margin-bottom: 12px; letter-spacing: 1px; }

  .copy-btn {
    background: linear-gradient(135deg, rgba(97,218,251,0.15), rgba(97,218,251,0.05));
    border: 1px solid rgba(97,218,251,0.4);
    color: var(--react);
    padding: 10px 28px;
    border-radius: 8px;
    font-family: 'Space Mono', monospace;
    font-size: 0.8rem;
    cursor: pointer;
    transition: all 0.2s;
    letter-spacing: 1px;
  }

  .copy-btn:hover { background: rgba(97,218,251,0.2); transform: translateY(-2px); }

  textarea.md-output {
    width: 100%;
    background: #0a0e17;
    border: 1px solid var(--border);
    border-radius: 8px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    font-size: 0.72rem;
    padding: 16px;
    margin-top: 16px;
    resize: vertical;
    min-height: 200px;
    display: none;
    line-height: 1.6;
  }

  textarea.md-output.visible { display: block; }
</style>
</head>
<body>
<div class="wrapper">

  <!-- HERO -->
  <div class="hero">
    <div class="avatar-wrap">
      <div class="avatar">⚛️</div>
      <div class="status-dot"></div>
    </div>

    <div class="hero-name">Lakshay</div>
    <div class="hero-title">⚛ React Developer &amp; Full-Stack Engineer</div>
    <div class="hero-bio">
      I craft fast, beautiful web experiences with React &amp; modern JavaScript.<br/>
      Turning ideas into pixel-perfect, high-performance products.
    </div>

    <div class="typed">const passion = "Building things that matter";</div>

    <div class="badges">
      <span class="badge badge-react">⚛ React Dev</span>
      <span class="badge badge-js">⚡ JavaScript</span>
      <span class="badge badge-node">🌿 Node.js</span>
      <span class="badge badge-open">🔓 Open Source</span>
    </div>
  </div>

  <div class="divider">
    <div class="divider-line"></div>
    <div class="divider-text">// who i am</div>
    <div class="divider-line"></div>
  </div>

  <!-- CODE BLOCK -->
  <div class="code-block">
    <div class="code-header">
      <div class="dot dot-red"></div>
      <div class="dot dot-yellow"></div>
      <div class="dot dot-green"></div>
      <span class="code-filename">lakshay.config.js</span>
    </div>
    <div class="code-body">
      <span class="kw">const</span> <span class="key">developer</span> = {<br/>
      &nbsp;&nbsp;<span class="key">name</span>: <span class="str">"Lakshay"</span>,<br/>
      &nbsp;&nbsp;<span class="key">title</span>: <span class="str">"React Developer &amp; Full-Stack Engineer"</span>,<br/>
      &nbsp;&nbsp;<span class="key">location</span>: <span class="str">"India 🇮🇳"</span>,<br/>
      &nbsp;&nbsp;<span class="key">github</span>: <span class="str">"@lakshayaraanaa"</span>,<br/>
      &nbsp;&nbsp;<span class="key">stack</span>: [<br/>
      &nbsp;&nbsp;&nbsp;&nbsp;<span class="str">"React"</span>, <span class="str">"Next.js"</span>, <span class="str">"Node.js"</span>,<br/>
      &nbsp;&nbsp;&nbsp;&nbsp;<span class="str">"Express"</span>, <span class="str">"MongoDB"</span>, <span class="str">"JavaScript"</span><br/>
      &nbsp;&nbsp;],<br/>
      &nbsp;&nbsp;<span class="key">currentProject</span>: <span class="str">"BuyByBest — E-Commerce Platform"</span>,<br/>
      &nbsp;&nbsp;<span class="key">learning</span>: [<span class="str">"TypeScript"</span>, <span class="str">"Docker"</span>, <span class="str">"System Design"</span>],<br/>
      &nbsp;&nbsp;<span class="key">available</span>: <span class="arr">true</span>, <span class="cmt">// open to opportunities!</span><br/>
      &nbsp;&nbsp;<span class="key">funFact</span>: <span class="str">"I turn coffee into React components ☕"</span><br/>
      }<br/><br/>
      <span class="kw">export default</span> <span class="fn">developer</span>;
    </div>
  </div>

  <div class="divider">
    <div class="divider-line"></div>
    <div class="divider-text">// my stack</div>
    <div class="divider-line"></div>
  </div>

  <!-- TECH GRID -->
  <div class="section-title"><span>⚡</span> Technologies I Use</div>
  <div class="tech-grid">
    <div class="tech-card"><span class="tech-icon">⚛️</span><div class="tech-name">React</div><div class="tech-level"><div class="tech-level-bar" style="width:95%"></div></div></div>
    <div class="tech-card"><span class="tech-icon">🟨</span><div class="tech-name">JavaScript</div><div class="tech-level"><div class="tech-level-bar" style="width:92%"></div></div></div>
    <div class="tech-card"><span class="tech-icon">🌿</span><div class="tech-name">Node.js</div><div class="tech-level"><div class="tech-level-bar" style="width:80%"></div></div></div>
    <div class="tech-card"><span class="tech-icon">🚂</span><div class="tech-name">Express</div><div class="tech-level"><div class="tech-level-bar" style="width:78%"></div></div></div>
    <div class="tech-card"><span class="tech-icon">🍃</span><div class="tech-name">MongoDB</div><div class="tech-level"><div class="tech-level-bar" style="width:75%"></div></div></div>
    <div class="tech-card"><span class="tech-icon">🎨</span><div class="tech-name">CSS3</div><div class="tech-level"><div class="tech-level-bar" style="width:88%"></div></div></div>
    <div class="tech-card"><span class="tech-icon">🔲</span><div class="tech-name">HTML5</div><div class="tech-level"><div class="tech-level-bar" style="width:95%"></div></div></div>
    <div class="tech-card"><span class="tech-icon">🐙</span><div class="tech-name">Git</div><div class="tech-level"><div class="tech-level-bar" style="width:82%"></div></div></div>
  </div>

  <div class="divider">
    <div class="divider-line"></div>
    <div class="divider-text">// my work</div>
    <div class="divider-line"></div>
  </div>

  <!-- PROJECTS -->
  <div class="section-title"><span>🚀</span> Featured Projects</div>
  <div class="projects-grid">
    <div class="project-card" style="--card-color1:#61DAFB;--card-color2:#00b4d8;">
      <span class="project-emoji">🛒</span>
      <div class="project-name">BuyByBest — Frontend</div>
      <div class="project-desc">A modern, responsive e-commerce frontend built with JavaScript. Smooth UX, product catalog, cart system.</div>
      <div class="project-tags">
        <span class="project-tag">JavaScript</span>
        <span class="project-tag">HTML/CSS</span>
        <span class="project-tag">E-Commerce</span>
      </div>
    </div>
    <div class="project-card" style="--card-color1:#4ade80;--card-color2:#22d3ee;">
      <span class="project-emoji">⚙️</span>
      <div class="project-name">BuyByBest — Backend</div>
      <div class="project-desc">Robust REST API powering BuyByBest. Auth, product management, order processing & more.</div>
      <div class="project-tags">
        <span class="project-tag">Node.js</span>
        <span class="project-tag">Express</span>
        <span class="project-tag">MongoDB</span>
      </div>
    </div>
    <div class="project-card" style="--card-color1:#c084fc;--card-color2:#f472b6;">
      <span class="project-emoji">🌐</span>
      <div class="project-name">My Portfolio</div>
      <div class="project-desc">Personal portfolio showcasing projects, skills, and journey. Clean design with smooth interactions.</div>
      <div class="project-tags">
        <span class="project-tag">JavaScript</span>
        <span class="project-tag">Portfolio</span>
        <span class="project-tag">Responsive</span>
      </div>
    </div>
    <div class="project-card" style="--card-color1:#f9c74f;--card-color2:#ff6b6b;">
      <span class="project-emoji">🔮</span>
      <div class="project-name">Coming Soon...</div>
      <div class="project-desc">Always building something new. Follow me on GitHub to stay updated on my latest experiments!</div>
      <div class="project-tags">
        <span class="project-tag">React</span>
        <span class="project-tag">TypeScript</span>
        <span class="project-tag">WIP</span>
      </div>
    </div>
  </div>

  <div class="divider">
    <div class="divider-line"></div>
    <div class="divider-text">// my numbers</div>
    <div class="divider-line"></div>
  </div>

  <!-- STATS -->
  <div class="section-title"><span>📊</span> GitHub Stats</div>
  <div class="stats-row">
    <div class="stat-card">
      <span class="stat-number">3+</span>
      <div class="stat-label">Repos</div>
    </div>
    <div class="stat-card">
      <span class="stat-number">JS</span>
      <div class="stat-label">Top Language</div>
    </div>
    <div class="stat-card">
      <span class="stat-number">∞</span>
      <div class="stat-label">Coffee Consumed</div>
    </div>
  </div>

  <!-- STATS IMAGE EMBEDS -->
  <div style="display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-bottom:16px;">
    <div style="background:var(--surface2);border:1px solid var(--border);border-radius:12px;padding:16px;text-align:center;">
      <img src="https://github-readme-stats.vercel.app/api?username=lakshayaraanaa&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=61DAFB&icon_color=61DAFB&text_color=ffffff" style="width:100%;border-radius:8px;" onerror="this.style.display='none';this.parentElement.innerHTML='<p style=\'color:var(--muted);font-size:0.75rem;padding:20px;\'>📊 GitHub Stats Card<br/>(visible on GitHub)</p>'" />
    </div>
    <div style="background:var(--surface2);border:1px solid var(--border);border-radius:12px;padding:16px;text-align:center;">
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=lakshayaraanaa&theme=tokyonight&hide_border=true&background=0D1117&ring=61DAFB&fire=ff6b6b&currStreakLabel=61DAFB" style="width:100%;border-radius:8px;" onerror="this.style.display='none';this.parentElement.innerHTML='<p style=\'color:var(--muted);font-size:0.75rem;padding:20px;\'>🔥 Streak Stats Card<br/>(visible on GitHub)</p>'" />
    </div>
  </div>

  <div style="text-align:center;margin-bottom:32px;">
    <div style="background:var(--surface2);border:1px solid var(--border);border-radius:12px;padding:16px;display:inline-block;">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=lakshayaraanaa&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=61DAFB&text_color=ffffff" style="border-radius:8px;max-width:400px;width:100%;" onerror="this.style.display='none';this.parentElement.innerHTML='<p style=\'color:var(--muted);font-size:0.75rem;padding:20px;\'>💻 Top Languages Card<br/>(visible on GitHub)</p>'" />
    </div>
  </div>

  <div class="divider">
    <div class="divider-line"></div>
    <div class="divider-text">// connect</div>
    <div class="divider-line"></div>
  </div>

  <!-- CONNECT -->
  <div class="section-title"><span>📫</span> Let's Connect</div>
  <div style="text-align:center;">
    <p style="color:var(--muted);font-size:0.82rem;line-height:1.8;margin-bottom:20px;max-width:460px;margin-left:auto;margin-right:auto;">
      Open to collaborations, freelance projects &amp; full-time opportunities.<br/>
      Let's build something amazing together!
    </p>
    <div class="connect-links">
      <a href="https://github.com/lakshayaraanaa" class="connect-btn btn-github">🐙 GitHub</a>
      <a href="https://github.com/lakshayaraanaa/my-portfolio" class="connect-btn btn-portfolio">🌐 Portfolio</a>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="footer-quote">"First, solve the problem. Then, <em>write the code.</em>"</div>
    <div class="footer-sub">⚛ Built with React &bull; Powered by coffee &bull; lakshayaraanaa</div>
  </div>

  <!-- COPY MD SECTION -->
  <div class="copy-section">
    <div class="copy-title">📋 Get the README.md code to paste into your GitHub profile repo</div>
    <button class="copy-btn" onclick="toggleMd()">Show README.md Code</button>
    <textarea class="md-output" id="mdout" readonly>
<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=28&duration=3000&pause=1000&color=61DAFB&center=true&vCenter=true&width=650&lines=Hey!+I'm+Lakshay+%F0%9F%91%8B;React+Developer+%E2%9A%9B;Full-Stack+Engineer+%F0%9F%9A%80;Building+BuyByBest+%F0%9F%9B%92" alt="Typing SVG" />
</h1>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=lakshayaraanaa&label=Profile%20Views&color=61DAFB&style=flat-square" />
  <img src="https://img.shields.io/github/followers/lakshayaraanaa?label=Followers&style=flat-square&color=61DAFB" />
  <img src="https://img.shields.io/badge/Available%20for%20Work-Yes-39d353?style=flat-square" />
</p>

---

## ⚛️ About Me

```javascript
const developer = {
  name:           "Lakshay",
  title:          "React Developer & Full-Stack Engineer",
  location:       "India 🇮🇳",
  github:         "@lakshayaraanaa",
  stack:          ["React", "Next.js", "Node.js", "Express", "MongoDB", "JavaScript"],
  currentProject: "BuyByBest — E-Commerce Platform",
  learning:       ["TypeScript", "Docker", "System Design"],
  available:      true, // open to opportunities!
  funFact:        "I turn coffee into React components ☕"
}

export default developer;
```

---

## ⚡ Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" />
  <img src="https://img.shields.io/badge/Express.js-404D59?style=for-the-badge&logo=express&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/VS_Code-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white" />
</p>

---

## 🚀 Featured Projects

<table align="center">
  <tr>
    <td align="center" width="50%">
      <h3>🛒 BuyByBest — Frontend</h3>
      <p>Modern, responsive e-commerce frontend. Product catalog, cart, smooth UX.</p>
      <a href="https://github.com/lakshayaraanaa/BuyByBest-FrontEnd">
        <img src="https://img.shields.io/badge/View%20Repo-61DAFB?style=for-the-badge&logo=github&logoColor=black" />
      </a>
      <br/><br/>
      <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
      <img src="https://img.shields.io/badge/HTML-E34F26?style=flat-square&logo=html5&logoColor=white" />
      <img src="https://img.shields.io/badge/CSS-1572B6?style=flat-square&logo=css3&logoColor=white" />
    </td>
    <td align="center" width="50%">
      <h3>⚙️ BuyByBest — Backend</h3>
      <p>Robust REST API. Auth, product management, order processing.</p>
      <a href="https://github.com/lakshayaraanaa/BuyByBest-BackEnd">
        <img src="https://img.shields.io/badge/View%20Repo-4ade80?style=for-the-badge&logo=github&logoColor=black" />
      </a>
      <br/><br/>
      <img src="https://img.shields.io/badge/Node.js-43853D?style=flat-square&logo=node.js&logoColor=white" />
      <img src="https://img.shields.io/badge/Express-404D59?style=flat-square&logo=express&logoColor=white" />
      <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=flat-square&logo=mongodb&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td align="center" width="50%" colspan="2">
      <h3>🌐 My Portfolio</h3>
      <p>Personal portfolio showcasing projects, skills, and journey as a developer.</p>
      <a href="https://github.com/lakshayaraanaa/my-portfolio">
        <img src="https://img.shields.io/badge/View%20Portfolio-c084fc?style=for-the-badge&logo=github&logoColor=white" />
      </a>
    </td>
  </tr>
</table>

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=lakshayaraanaa&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=61DAFB&icon_color=61DAFB&text_color=ffffff" width="48%" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=lakshayaraanaa&theme=tokyonight&hide_border=true&background=0D1117&ring=61DAFB&fire=ff6b6b&currStreakLabel=61DAFB" width="48%" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=lakshayaraanaa&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=61DAFB&text_color=ffffff" width="40%" />
</p>

---

## 🏆 Trophies

<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=lakshayaraanaa&theme=tokyonight&no-frame=true&column=6&margin-w=10" />
</p>

---

## 🐍 Contribution Snake

<p align="center">
  <img src="https://raw.githubusercontent.com/lakshayaraanaa/lakshayaraanaa/output/github-contribution-grid-snake-dark.svg" />
</p>

---

## 📫 Let's Connect

<p align="center">
  Open to collaborations, freelance projects & full-time opportunities.<br/>
  Let's build something amazing together!
</p>

<p align="center">
  <a href="https://github.com/lakshayaraanaa">
    <img src="https://img.shields.io/badge/GitHub-lakshayaraanaa-100000?style=for-the-badge&logo=github&logoColor=white" />
  </a>
  <a href="https://github.com/lakshayaraanaa/my-portfolio">
    <img src="https://img.shields.io/badge/Portfolio-View%20Site-61DAFB?style=for-the-badge&logo=react&logoColor=white" />
  </a>
</p>

---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=61DAFB&height=100&section=footer" />
</p>

<p align="center">
  <b>⚛ "First, solve the problem. Then, write the code." ⚛</b><br/>
  <sub>Built with ❤️ by Lakshay | @lakshayaraanaa</sub>
</p>
    </textarea>
    <button class="copy-btn" id="copyBtn" onclick="copyMd()" style="margin-top:10px;display:none;">📋 Copy to Clipboard</button>
  </div>

</div>

<script>
  function toggleMd() {
    const ta = document.getElementById('mdout');
    const copyBtn = document.getElementById('copyBtn');
    ta.classList.toggle('visible');
    copyBtn.style.display = ta.classList.contains('visible') ? 'inline-block' : 'none';
    document.querySelector('.copy-btn').textContent = ta.classList.contains('visible') ? 'Hide Code' : 'Show README.md Code';
  }

  function copyMd() {
    const ta = document.getElementById('mdout');
    ta.select();
    document.execCommand('copy');
    document.getElementById('copyBtn').textContent = '✅ Copied!';
    setTimeout(() => document.getElementById('copyBtn').textContent = '📋 Copy to Clipboard', 2000);
  }

  // Animate contribution graph
  const grid = document.createElement('div');
  const levels = ['', 'c1', 'c2', 'c3', 'c4'];
  const pattern = [0,0,1,2,3,4,3,2,1,0,0,1,3,4,2,0,1,2,4,3,1,0,2,3,4,1,2,3,0,1,4,2,3,1,0,2,4,3,1,2,0,3,4,2,1,3,2,4,1,0,3,2];
  for (let i = 0; i < 52 * 7; i++) {
    const day = document.createElement('div');
    day.className = 'contrib-day ' + (levels[pattern[i % pattern.length]] || '');
    grid.appendChild(day);
  }
</script>
</body>
</html>
