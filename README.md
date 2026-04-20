<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Sai Manikanta — AI & Full-Stack Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --dark-bg:  #0F1F4A;
    --primary:  #1F3C88;
    --btn:      #3656A6;
    --card:     #6B87C9;
    --light-ui: #A5B7E6;
    --bg:       #E3E9F9;
  }

  body {
    font-family: 'Space Grotesk', sans-serif;
    background: var(--bg);
    color: var(--dark-bg);
    min-height: 100vh;
    display: flex;
    justify-content: center;
    padding: 3rem 1.5rem;
  }

  .pw { max-width: 680px; width: 100%; }

  /* Ticker */
  .ticker-wrap {
    overflow: hidden;
    border-top: 0.5px solid var(--light-ui);
    border-bottom: 0.5px solid var(--light-ui);
    margin-bottom: 2.5rem;
    padding: 10px 0;
    background: rgba(255,255,255,0.45);
    border-radius: 6px;
  }
  .ticker {
    display: flex;
    white-space: nowrap;
    animation: tick 18s linear infinite;
  }
  .ticker span {
    font-family: 'Fira Code', monospace;
    font-size: 11px;
    color: var(--btn);
    letter-spacing: 0.06em;
    padding: 0 24px;
  }
  .ticker span.dot { color: var(--primary); padding: 0; }
  @keyframes tick {
    0%   { transform: translateX(0); }
    100% { transform: translateX(-50%); }
  }

  /* Hero */
  .hero {
    display: grid;
    grid-template-columns: 1fr 88px;
    gap: 1.5rem;
    align-items: start;
    margin-bottom: 2.5rem;
  }

  .name-tag {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-family: 'Fira Code', monospace;
    font-size: 11px;
    color: #ffffff;
    background: var(--btn);
    border-radius: 4px;
    padding: 3px 10px;
    margin-bottom: 14px;
  }
  .name-tag .dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--light-ui);
    animation: pulse 2s ease-in-out infinite;
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50%       { opacity: 0.3; }
  }

  .name {
    font-size: 48px;
    font-weight: 700;
    color: var(--dark-bg);
    line-height: 1.05;
    letter-spacing: -2px;
    margin-bottom: 8px;
  }
  .name .accent { color: var(--btn); }

  .role {
    font-family: 'Fira Code', monospace;
    font-size: 12px;
    color: var(--card);
    margin-bottom: 16px;
    letter-spacing: 0.02em;
  }

  .bio {
    font-size: 15px;
    color: var(--btn);
    line-height: 1.75;
    max-width: 400px;
  }

  .avatar {
    width: 88px; height: 88px;
    border-radius: 16px;
    background: var(--primary);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 3px;
    flex-shrink: 0;
  }
  .avatar .initials {
    font-family: 'Space Grotesk', sans-serif;
    font-size: 24px;
    font-weight: 700;
    color: #ffffff;
  }
  .avatar .handle {
    font-family: 'Fira Code', monospace;
    font-size: 10px;
    color: var(--light-ui);
  }

  /* Stat bar */
  .stat-bar {
    display: grid;
    grid-template-columns: repeat(3, minmax(0,1fr));
    gap: 10px;
    margin-bottom: 2.5rem;
  }
  .stat {
    background: var(--primary);
    border-radius: 10px;
    padding: 16px 18px;
  }
  .stat-val {
    font-size: 26px;
    font-weight: 700;
    color: #ffffff;
    line-height: 1;
    margin-bottom: 4px;
  }
  .stat-val .unit { color: var(--light-ui); font-size: 16px; }
  .stat-lbl {
    font-family: 'Fira Code', monospace;
    font-size: 11px;
    color: var(--light-ui);
  }

  /* Section heading */
  .section { margin-bottom: 2.5rem; }
  .section-head {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 1rem;
  }
  .section-num {
    font-family: 'Fira Code', monospace;
    font-size: 11px;
    color: var(--btn);
    min-width: 24px;
  }
  .section-title {
    font-size: 11px;
    font-weight: 500;
    color: var(--btn);
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }
  .section-line {
    flex: 1;
    height: 0.5px;
    background: var(--light-ui);
  }

  /* Build grid */
  .build-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0,1fr));
    gap: 10px;
  }
  .build-item {
    border: 0.5px solid var(--light-ui);
    border-radius: 10px;
    padding: 14px 16px;
    background: #ffffff;
    position: relative;
    overflow: hidden;
    transition: border-color 0.2s;
  }
  .build-item:hover { border-color: var(--primary); }
  .build-item::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px; height: 100%;
    background: var(--primary);
    opacity: 0;
    transition: opacity 0.2s;
  }
  .build-item:hover::before { opacity: 1; }
  .bi-num {
    font-family: 'Fira Code', monospace;
    font-size: 10px;
    color: var(--btn);
    margin-bottom: 6px;
    display: block;
  }
  .bi-text {
    font-size: 13px;
    font-weight: 500;
    color: var(--dark-bg);
    line-height: 1.4;
  }

  /* Stack pills */
  .stack-row {
    display: flex;
    flex-wrap: wrap;
    gap: 7px;
  }
  .stack-pill {
    font-family: 'Fira Code', monospace;
    font-size: 12px;
    padding: 5px 13px;
    border-radius: 100px;
    border: 0.5px solid var(--light-ui);
    background: #ffffff;
    color: var(--btn);
    transition: all 0.15s;
    cursor: default;
    user-select: none;
  }
  .stack-pill:hover {
    background: var(--primary);
    border-color: var(--primary);
    color: #ffffff;
  }

  /* Experience */
  .exp-item {
    display: flex;
    gap: 16px;
    padding: 16px 0;
    border-bottom: 0.5px solid var(--light-ui);
  }
  .exp-item:last-child { border-bottom: none; }
  .exp-index {
    font-family: 'Fira Code', monospace;
    font-size: 11px;
    color: var(--btn);
    padding-top: 2px;
    min-width: 32px;
  }
  .exp-name {
    font-size: 14px;
    font-weight: 600;
    color: var(--dark-bg);
    margin-bottom: 3px;
  }
  .exp-desc {
    font-size: 13px;
    color: var(--btn);
  }

  /* Connect */
  .connect-row {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
  }
  .link-btn {
    font-family: 'Fira Code', monospace;
    font-size: 12px;
    padding: 9px 18px;
    border-radius: 8px;
    border: 0.5px solid var(--light-ui);
    background: #ffffff;
    color: var(--btn);
    text-decoration: none;
    display: inline-flex;
    align-items: center;
    gap: 7px;
    transition: all 0.15s;
  }
  .link-btn:hover {
    background: var(--primary);
    border-color: var(--primary);
    color: #ffffff;
  }
  .link-btn.hi {
    background: var(--primary);
    border-color: var(--primary);
    color: #ffffff;
  }
  .arr { font-size: 14px; line-height: 1; }

  @media (max-width: 500px) {
    .name { font-size: 36px; }
    .hero { grid-template-columns: 1fr; }
    .avatar { display: none; }
    .build-grid { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>
<div class="pw">

  <div class="ticker-wrap">
    <div class="ticker">
      <span>AI Engineer</span><span class="dot">·</span>
      <span>Full-Stack Dev</span><span class="dot">·</span>
      <span>System Builder</span><span class="dot">·</span>
      <span>Startup Founder</span><span class="dot">·</span>
      <span>Open to Collabs</span><span class="dot">·</span>
      <span>Python · Flask · ML · AWS</span><span class="dot">·</span>
      <span>AI Engineer</span><span class="dot">·</span>
      <span>Full-Stack Dev</span><span class="dot">·</span>
      <span>System Builder</span><span class="dot">·</span>
      <span>Startup Founder</span><span class="dot">·</span>
      <span>Open to Collabs</span><span class="dot">·</span>
      <span>Python · Flask · ML · AWS</span><span class="dot">·</span>
    </div>
  </div>

  <div class="hero">
    <div>
      <div class="name-tag">
        <span class="dot"></span>
        available for work
      </div>
      <div class="name">Sai<br>Mani<span class="accent">kanta</span></div>
      <div class="role">// AI &amp; Full-Stack Engineer · Founder @ Mindrevel</div>
      <p class="bio">I design and build intelligent, real-world systems that automate processes, improve safety, and solve business problems using AI, cloud, and software engineering.</p>
    </div>
    <div class="avatar">
      <div class="initials">SM</div>
      <span class="handle">@saichamp</span>
    </div>
  </div>

  <div class="stat-bar">
    <div class="stat">
      <div class="stat-val">4<span class="unit">+</span></div>
      <div class="stat-lbl">domains built</div>
    </div>
    <div class="stat">
      <div class="stat-val">1<span class="unit">x</span></div>
      <div class="stat-lbl">startup founded</div>
    </div>
    <div class="stat">
      <div class="stat-val">10<span class="unit">+</span></div>
      <div class="stat-lbl">tech tools used</div>
    </div>
  </div>

  <div class="section">
    <div class="section-head">
      <span class="section-num">01</span>
      <span class="section-title">What I build</span>
      <div class="section-line"></div>
    </div>
    <div class="build-grid">
      <div class="build-item">
        <span class="bi-num">→ 01</span>
        <div class="bi-text">AI-powered monitoring &amp; analytics systems</div>
      </div>
      <div class="build-item">
        <span class="bi-num">→ 02</span>
        <div class="bi-text">Safety &amp; emergency response platforms</div>
      </div>
      <div class="build-item">
        <span class="bi-num">→ 03</span>
        <div class="bi-text">Social impact &amp; smart city solutions</div>
      </div>
      <div class="build-item">
        <span class="bi-num">→ 04</span>
        <div class="bi-text">Web, mobile &amp; cloud-based applications</div>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-head">
      <span class="section-num">02</span>
      <span class="section-title">Tech stack</span>
      <div class="section-line"></div>
    </div>
    <div class="stack-row">
      <span class="stack-pill">Python</span>
      <span class="stack-pill">Java</span>
      <span class="stack-pill">C</span>
      <span class="stack-pill">SQL</span>
      <span class="stack-pill">Flask</span>
      <span class="stack-pill">Machine Learning</span>
      <span class="stack-pill">OpenCV</span>
      <span class="stack-pill">Firebase</span>
      <span class="stack-pill">Android</span>
      <span class="stack-pill">AWS</span>
      <span class="stack-pill">Git</span>
      <span class="stack-pill">GitHub</span>
    </div>
  </div>

  <div class="section">
    <div class="section-head">
      <span class="section-num">03</span>
      <span class="section-title">Experience</span>
      <div class="section-line"></div>
    </div>
    <div class="exp-item">
      <span class="exp-index">[01]</span>
      <div>
        <div class="exp-name">Founder — Mindrevel</div>
        <div class="exp-desc">Tech services startup · building intelligent, real-world systems</div>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-head">
      <span class="section-num">04</span>
      <span class="section-title">Connect</span>
      <div class="section-line"></div>
    </div>
    <div class="connect-row">
      <a class="link-btn hi" href="https://linkedin.com/in/" target="_blank">
        <span class="arr">↗</span> LinkedIn
      </a>
      <a class="link-btn" href="https://instagram.com/" target="_blank">
        <span class="arr">↗</span> Instagram
      </a>
      <a class="link-btn" href="mailto:" target="_blank">
        <span class="arr">↗</span> Email
      </a>
    </div>
  </div>

</div>
</body>
</html>
