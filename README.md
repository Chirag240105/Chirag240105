<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chirag Pandey — GitHub Profile README</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0b0f1a;
    --surface: #111827;
    --border: #1e2d40;
    --accent: #38bdf8;
    --accent2: #818cf8;
    --green: #34d399;
    --text: #e2e8f0;
    --muted: #64748b;
    --card: #141e2e;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Mono', monospace;
    min-height: 100vh;
    padding: 48px 24px;
    line-height: 1.6;
  }

  .wrapper {
    max-width: 860px;
    margin: 0 auto;
  }

  /* ── HERO ── */
  .hero {
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 48px 40px 36px;
    background: var(--card);
    position: relative;
    overflow: hidden;
    margin-bottom: 24px;
    animation: fadeUp .6s ease both;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 320px; height: 320px;
    background: radial-gradient(circle, rgba(56,189,248,.12) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero::after {
    content: '';
    position: absolute;
    bottom: -60px; left: -60px;
    width: 260px; height: 260px;
    background: radial-gradient(circle, rgba(129,140,248,.09) 0%, transparent 70%);
    pointer-events: none;
  }

  .badge-row {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    margin-bottom: 20px;
  }

  .badge {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    font-weight: 500;
    padding: 4px 10px;
    border-radius: 20px;
    border: 1px solid;
    letter-spacing: .04em;
    text-transform: uppercase;
  }

  .badge-blue  { color: var(--accent);  border-color: rgba(56,189,248,.3);  background: rgba(56,189,248,.06); }
  .badge-purple{ color: var(--accent2); border-color: rgba(129,140,248,.3); background: rgba(129,140,248,.06); }
  .badge-green { color: var(--green);   border-color: rgba(52,211,153,.3);  background: rgba(52,211,153,.06); }

  .hero-name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2rem, 5vw, 3rem);
    font-weight: 800;
    letter-spacing: -.02em;
    line-height: 1.1;
    margin-bottom: 12px;
    background: linear-gradient(135deg, #e2e8f0 30%, var(--accent) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero-tagline {
    font-size: 14px;
    color: var(--muted);
    max-width: 520px;
    margin-bottom: 28px;
  }

  .divider {
    height: 1px;
    background: var(--border);
    margin: 28px 0;
  }

  /* ── GRID ── */
  .grid-2 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-bottom: 16px;
    animation: fadeUp .6s .15s ease both;
  }

  @media(max-width: 600px){ .grid-2 { grid-template-columns: 1fr; } }

  .card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 24px;
    transition: border-color .2s;
  }

  .card:hover { border-color: rgba(56,189,248,.35); }

  .card-label {
    font-family: 'Syne', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: .1em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 14px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .card-label::before {
    content: '';
    display: inline-block;
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 6px var(--accent);
  }

  /* ── ABOUT LIST ── */
  .about-list { list-style: none; }
  .about-list li {
    font-size: 13px;
    color: var(--text);
    padding: 7px 0;
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: flex-start;
    gap: 10px;
  }
  .about-list li:last-child { border-bottom: none; }
  .about-list .icon { width: 18px; flex-shrink: 0; color: var(--accent); }

  /* ── TECH PILLS ── */
  .pill-group { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px; }
  .pill-section { margin-bottom: 14px; }
  .pill-section:last-child { margin-bottom: 0; }
  .pill-title {
    font-size: 11px;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: .06em;
    margin-bottom: 8px;
  }
  .pill {
    font-size: 12px;
    padding: 4px 12px;
    border-radius: 8px;
    border: 1px solid var(--border);
    color: var(--text);
    background: var(--surface);
    transition: border-color .2s, color .2s;
  }
  .pill:hover { border-color: var(--accent2); color: var(--accent2); }

  /* ── PROJECTS ── */
  .projects-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-bottom: 16px;
    animation: fadeUp .6s .3s ease both;
  }
  @media(max-width: 600px){ .projects-row { grid-template-columns: 1fr; } }

  .project-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 24px;
    transition: border-color .2s, transform .2s;
    position: relative;
    overflow: hidden;
  }
  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    opacity: 0;
    transition: opacity .2s;
  }
  .project-card:hover { border-color: var(--accent2); transform: translateY(-2px); }
  .project-card:hover::before { opacity: 1; }

  .project-title {
    font-family: 'Syne', sans-serif;
    font-size: 15px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 8px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .project-desc {
    font-size: 12px;
    color: var(--muted);
    line-height: 1.7;
    margin-bottom: 12px;
  }

  /* ── CONNECT ── */
  .connect-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 24px;
    animation: fadeUp .6s .45s ease both;
    margin-bottom: 16px;
  }

  .connect-grid {
    display: grid;
    grid-template-columns: repeat(3,1fr);
    gap: 12px;
    margin-top: 16px;
  }
  @media(max-width:500px){ .connect-grid { grid-template-columns: 1fr 1fr; } }

  .connect-item {
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 14px;
    text-align: center;
    transition: border-color .2s, background .2s;
    cursor: pointer;
    text-decoration: none;
    color: var(--text);
    display: block;
  }
  .connect-item:hover { border-color: var(--accent); background: rgba(56,189,248,.04); }
  .connect-item .ci-label { font-size: 12px; color: var(--muted); margin-top: 6px; }
  .connect-item .ci-value { font-size: 12px; color: var(--accent); margin-top: 2px; word-break: break-all; }

  /* ── QUOTE ── */
  .quote-bar {
    background: var(--card);
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent2);
    border-radius: 0 12px 12px 0;
    padding: 16px 20px;
    font-family: 'Syne', sans-serif;
    font-size: 14px;
    font-weight: 600;
    color: var(--accent2);
    animation: fadeUp .6s .6s ease both;
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* ── FOOTER NOTE ── */
  .copy-note {
    margin-top: 32px;
    font-size: 12px;
    color: var(--muted);
    text-align: center;
    border-top: 1px solid var(--border);
    padding-top: 20px;
  }
  .copy-note code {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 2px 8px;
    border-radius: 6px;
    font-size: 11px;
  }
</style>
</head>
<body>
<div class="wrapper">

  <!-- HERO -->
  <div class="hero">
    <div class="badge-row">
      <span class="badge badge-blue">Full Stack</span>
      <span class="badge badge-purple">AI Enthusiast</span>
      <span class="badge badge-green">Open to Opportunities</span>
    </div>
    <h1 class="hero-name">Chirag Pandey</h1>
    <p class="hero-tagline">
      Building scalable web apps with the MERN stack — exploring AI systems, system design, and real-world problem solving.
    </p>
    <div class="badge-row">
      <span class="badge badge-blue">⚡ MERN Stack</span>
      <span class="badge badge-purple">🤖 AI / ML</span>
      <span class="badge badge-green">🧩 DSA · LeetCode</span>
    </div>
  </div>

  <!-- ABOUT + TECH -->
  <div class="grid-2">
    <div class="card">
      <div class="card-label">About Me</div>
      <ul class="about-list">
        <li><span class="icon">▸</span> Full Stack Web Developer — MERN Stack</li>
        <li><span class="icon">▸</span> Exploring AI Systems &amp; intelligent interfaces</li>
        <li><span class="icon">▸</span> Passionate about Backend, APIs &amp; System Design</li>
        <li><span class="icon">▸</span> Consistent DSA practice on LeetCode</li>
        <li><span class="icon">▸</span> Building production-grade projects from scratch</li>
      </ul>
    </div>

    <div class="card">
      <div class="card-label">Tech Stack</div>
      <div class="pill-section">
        <div class="pill-title">Frontend</div>
        <div class="pill-group">
          <span class="pill">React</span>
          <span class="pill">HTML</span>
          <span class="pill">CSS</span>
          <span class="pill">Tailwind</span>
        </div>
      </div>
      <div class="pill-section">
        <div class="pill-title">Backend &amp; DB</div>
        <div class="pill-group">
          <span class="pill">Node.js</span>
          <span class="pill">Express.js</span>
          <span class="pill">MongoDB</span>
        </div>
      </div>
      <div class="pill-section">
        <div class="pill-title">Languages &amp; Tools</div>
        <div class="pill-group">
          <span class="pill">JavaScript</span>
          <span class="pill">C++</span>
          <span class="pill">Git</span>
          <span class="pill">Postman</span>
        </div>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="projects-row">
    <div class="project-card">
      <div class="project-title">🌾 AgriBridge</div>
      <p class="project-desc">
        A MERN-based marketplace directly connecting farmers with buyers — cutting out middlemen and improving market access. Roadmap includes AI-based demand prediction for smarter supply planning.
      </p>
      <div class="pill-group">
        <span class="pill">React</span>
        <span class="pill">Node.js</span>
        <span class="pill">MongoDB</span>
        <span class="pill">AI (Planned)</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-title">💰 Expense Tracker</div>
      <p class="project-desc">
        Full-stack expense management app with secure authentication, RESTful APIs, and real-time financial overview. Clean UI with data persistence.
      </p>
      <div class="pill-group">
        <span class="pill">MERN</span>
        <span class="pill">JWT Auth</span>
        <span class="pill">REST API</span>
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="connect-card">
    <div class="card-label">Connect With Me</div>
    <div class="connect-grid">
      <a class="connect-item" href="mailto:yourmail@gmail.com">
        <div>📧</div>
        <div class="ci-label">Email</div>
        <div class="ci-value">pandeychirag651@gmail.com
</div>
      </a>
      <a class="connect-item" href="#" target="_blank">
        <div>🔗</div>
        <div class="ci-label">LinkedIn</div>
        <div class="ci-value">https://www.linkedin.com/in/chirag-pandey-b54499328/</div>
      </a>
      <a class="connect-item" href="#" target="_blank">
        <div>💻</div>
        <div class="ci-label">LeetCode</div>
        <div class="ci-value">https://leetcode.com/u/ChiragPandey/</div>
      </a>
    </div>
  </div>

  <!-- QUOTE -->
  <div class="quote-bar">
    "Building things &gt; Watching tutorials."
  </div>

  <div class="copy-note">
    Preview of your GitHub README — copy the markdown from the <code>README.md</code> tab and paste into your GitHub profile repo.
  </div>

</div>
</body>
</html>
