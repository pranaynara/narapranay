<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Nara Pranay | ECE Engineer & IEEE Leader</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --navy: #0A1628;
      --navy-mid: #112240;
      --navy-card: #1A2F4E;
      --accent: #00C6A2;
      --accent-dim: rgba(0,198,162,0.12);
      --accent-glow: rgba(0,198,162,0.25);
      --gold: #F4B942;
      --white: #E8F0FE;
      --muted: #8BAAC8;
      --border: rgba(0,198,162,0.18);
      --font-display: 'Space Grotesk', sans-serif;
      --font-body: 'Inter', sans-serif;
    }
 
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
 
    html { scroll-behavior: smooth; }
 
    body {
      background: var(--navy);
      color: var(--white);
      font-family: var(--font-body);
      font-size: 15px;
      line-height: 1.7;
    }
 
    /* NAV */
    nav {
      position: sticky; top: 0; z-index: 100;
      background: rgba(10,22,40,0.92);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border);
      display: flex; align-items: center; justify-content: space-between;
      padding: 0 5%;
      height: 62px;
    }
    .nav-logo {
      font-family: var(--font-display);
      font-weight: 700; font-size: 1.1rem;
      color: var(--accent); letter-spacing: -0.5px;
    }
    .nav-links { display: flex; gap: 1.8rem; list-style: none; }
    .nav-links a {
      color: var(--muted); text-decoration: none;
      font-size: 0.82rem; font-weight: 500; letter-spacing: 0.5px; text-transform: uppercase;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--accent); }
 
    /* HERO */
    .hero {
      display: flex; align-items: center; gap: 3rem;
      padding: 5rem 8% 4rem;
      max-width: 1200px; margin: 0 auto;
    }
    .hero-avatar {
      flex-shrink: 0;
      width: 175px; height: 175px;
      border-radius: 50%;
      border: 3px solid var(--accent);
      box-shadow: 0 0 30px var(--accent-glow), 0 0 60px rgba(0,198,162,0.1);
      object-fit: cover;
    }
    .hero-text h1 {
      font-family: var(--font-display);
      font-size: 2.6rem; font-weight: 700; line-height: 1.1;
      color: #fff; letter-spacing: -1px;
    }
    .hero-text h1 span { color: var(--accent); }
    .hero-tagline {
      margin-top: 0.5rem;
      font-size: 1rem; font-weight: 500;
      color: var(--muted); letter-spacing: 0.2px;
    }
    .hero-bio {
      margin-top: 1rem;
      font-size: 0.93rem; color: #A8BFDB; max-width: 600px; line-height: 1.75;
    }
    .hero-links {
      display: flex; gap: 0.9rem; margin-top: 1.4rem; flex-wrap: wrap;
    }
    .hero-links a {
      display: inline-flex; align-items: center; gap: 0.45rem;
      padding: 0.45rem 1rem; border-radius: 6px;
      font-size: 0.82rem; font-weight: 600; text-decoration: none;
      border: 1px solid var(--border);
      color: var(--accent); background: var(--accent-dim);
      transition: background 0.2s, border-color 0.2s, transform 0.15s;
    }
    .hero-links a:hover {
      background: rgba(0,198,162,0.2); border-color: var(--accent); transform: translateY(-1px);
    }
    .hero-links a svg { width: 15px; height: 15px; fill: currentColor; }
 
    /* KEY ACHIEVEMENT BANNER */
    .achievement-banner {
      background: linear-gradient(135deg, rgba(244,185,66,0.12) 0%, rgba(0,198,162,0.08) 100%);
      border: 1px solid rgba(244,185,66,0.3);
      border-left: 4px solid var(--gold);
      border-radius: 8px;
      padding: 1rem 1.4rem;
      margin: 0 8% 2rem;
      max-width: 1200px;
      margin-left: auto; margin-right: auto;
      display: flex; align-items: center; gap: 1rem;
    }
    .achievement-banner .trophy { font-size: 1.5rem; }
    .achievement-banner p { font-size: 0.9rem; color: #E8D5A0; line-height: 1.5; }
    .achievement-banner strong { color: var(--gold); }
 
    /* SECTION LAYOUT */
    .container { max-width: 1200px; margin: 0 auto; padding: 0 8%; }
 
    section { padding: 3.5rem 0; border-top: 1px solid rgba(255,255,255,0.05); }
 
    .section-label {
      display: flex; align-items: center; gap: 0.7rem;
      margin-bottom: 2rem;
    }
    .section-label h2 {
      font-family: var(--font-display);
      font-size: 1.4rem; font-weight: 700; color: #fff;
    }
    .section-label .dot {
      width: 8px; height: 8px; border-radius: 50%;
      background: var(--accent); flex-shrink: 0;
    }
    .section-label .line {
      flex: 1; height: 1px; background: var(--border);
    }
 
    /* ABOUT */
    .about-grid {
      display: grid; grid-template-columns: 1fr 1fr;
      gap: 2rem;
    }
    .about-card {
      background: var(--navy-card);
      border: 1px solid var(--border);
      border-radius: 12px; padding: 1.6rem;
    }
    .about-card h3 {
      font-family: var(--font-display);
      font-size: 0.85rem; font-weight: 600; color: var(--accent);
      letter-spacing: 1.5px; text-transform: uppercase; margin-bottom: 0.8rem;
    }
    .about-card p { font-size: 0.9rem; color: #A8BFDB; }
 
    /* DOMAINS */
    .domains-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 1rem;
    }
    .domain-card {
      background: var(--navy-card);
      border: 1px solid var(--border);
      border-radius: 10px; padding: 1.2rem 1.4rem;
      transition: border-color 0.2s, transform 0.2s;
    }
    .domain-card:hover { border-color: var(--accent); transform: translateY(-2px); }
    .domain-card .icon { font-size: 1.5rem; margin-bottom: 0.5rem; }
    .domain-card h4 { font-size: 0.9rem; font-weight: 600; color: #fff; margin-bottom: 0.3rem; }
    .domain-card p { font-size: 0.78rem; color: var(--muted); }
 
    /* SKILLS */
    .skills-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 1.2rem;
    }
    .skill-group {
      background: var(--navy-card);
      border: 1px solid var(--border);
      border-radius: 10px; padding: 1.3rem;
    }
    .skill-group h4 {
      font-size: 0.78rem; font-weight: 600; color: var(--accent);
      letter-spacing: 1.5px; text-transform: uppercase; margin-bottom: 0.9rem;
    }
    .skill-tags { display: flex; flex-wrap: wrap; gap: 0.4rem; }
    .skill-tag {
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.1);
      color: #C8D8EE; font-size: 0.78rem; font-weight: 500;
      padding: 0.25rem 0.65rem; border-radius: 4px;
    }
 
    /* TIMELINE */
    .timeline { position: relative; padding-left: 1.5rem; }
    .timeline::before {
      content: ''; position: absolute; left: 0; top: 0; bottom: 0;
      width: 2px; background: var(--border);
    }
    .tl-item {
      position: relative; padding-left: 1.8rem; margin-bottom: 2.2rem;
    }
    .tl-item::before {
      content: ''; position: absolute; left: -1.5rem; top: 5px;
      width: 10px; height: 10px; border-radius: 50%;
      background: var(--accent);
      box-shadow: 0 0 0 3px var(--accent-dim);
    }
    .tl-date {
      font-size: 0.75rem; font-weight: 600; color: var(--accent);
      letter-spacing: 0.8px; text-transform: uppercase; margin-bottom: 0.2rem;
    }
    .tl-org {
      font-size: 0.78rem; color: var(--muted); margin-bottom: 0.3rem;
    }
    .tl-title {
      font-family: var(--font-display);
      font-size: 1rem; font-weight: 600; color: #fff; margin-bottom: 0.5rem;
    }
    .tl-body { font-size: 0.87rem; color: #A8BFDB; }
    .tl-body ul { padding-left: 1.1rem; }
    .tl-body ul li { margin-bottom: 0.3rem; }
    .highlight-badge {
      display: inline-block;
      background: rgba(244,185,66,0.15); border: 1px solid rgba(244,185,66,0.4);
      color: var(--gold); font-size: 0.75rem; font-weight: 600;
      padding: 0.2rem 0.6rem; border-radius: 4px; margin-bottom: 0.4rem;
    }
 
    /* PROJECTS */
    .projects-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
      gap: 1.3rem;
    }
    .project-card {
      background: var(--navy-card);
      border: 1px solid var(--border);
      border-radius: 12px; padding: 1.5rem;
      transition: border-color 0.2s, transform 0.2s;
      position: relative;
    }
    .project-card:hover { border-color: var(--accent); transform: translateY(-3px); }
    .project-card .ptype {
      font-size: 0.72rem; font-weight: 600; letter-spacing: 1px; text-transform: uppercase;
      color: var(--accent); margin-bottom: 0.5rem;
    }
    .project-card h3 { font-family: var(--font-display); font-size: 1rem; font-weight: 600; color: #fff; margin-bottom: 0.5rem; }
    .project-card .pdate { font-size: 0.75rem; color: var(--muted); margin-bottom: 0.6rem; }
    .project-card p { font-size: 0.85rem; color: #A8BFDB; line-height: 1.6; }
    .award-badge {
      position: absolute; top: 1rem; right: 1rem;
      background: rgba(244,185,66,0.2); border: 1px solid var(--gold);
      color: var(--gold); font-size: 0.7rem; font-weight: 700;
      padding: 0.15rem 0.5rem; border-radius: 4px;
    }
    .tech-pills { display: flex; flex-wrap: wrap; gap: 0.35rem; margin-top: 0.9rem; }
    .tech-pill {
      background: rgba(0,198,162,0.08); border: 1px solid rgba(0,198,162,0.2);
      color: var(--accent); font-size: 0.72rem; font-weight: 500;
      padding: 0.18rem 0.55rem; border-radius: 4px;
    }
 
    /* PUBLICATIONS */
    .pub-card {
      background: var(--navy-card);
      border: 1px solid var(--border);
      border-left: 3px solid var(--accent);
      border-radius: 10px; padding: 1.4rem 1.6rem;
    }
    .pub-card h3 { font-family: var(--font-display); font-size: 0.98rem; font-weight: 600; color: #fff; margin-bottom: 0.5rem; }
    .pub-card .venue { font-size: 0.8rem; color: var(--accent); margin-bottom: 0.5rem; }
    .pub-card p { font-size: 0.85rem; color: #A8BFDB; }
 
    /* CERTS */
    .cert-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 1rem;
    }
    .cert-card {
      background: var(--navy-card);
      border: 1px solid var(--border);
      border-radius: 10px; padding: 1.1rem 1.3rem;
      display: flex; align-items: flex-start; gap: 0.9rem;
    }
    .cert-icon { font-size: 1.3rem; flex-shrink: 0; }
    .cert-card h4 { font-size: 0.88rem; font-weight: 600; color: #fff; margin-bottom: 0.15rem; }
    .cert-card p { font-size: 0.78rem; color: var(--muted); }
 
    /* ACHIEVEMENTS */
    .ach-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
      gap: 1rem;
    }
    .ach-card {
      background: var(--navy-card);
      border: 1px solid var(--border);
      border-radius: 10px; padding: 1.2rem;
      text-align: center;
    }
    .ach-card .num {
      font-family: var(--font-display);
      font-size: 2rem; font-weight: 700; color: var(--accent);
    }
    .ach-card h4 { font-size: 0.9rem; font-weight: 600; color: #fff; margin: 0.3rem 0 0.3rem; }
    .ach-card p { font-size: 0.8rem; color: var(--muted); }
 
    /* EDUCATION */
    .edu-card {
      background: var(--navy-card);
      border: 1px solid var(--border);
      border-radius: 10px; padding: 1.3rem 1.5rem;
      margin-bottom: 1rem;
      display: flex; align-items: flex-start; gap: 1.2rem;
    }
    .edu-icon { font-size: 1.5rem; flex-shrink: 0; }
    .edu-card h4 { font-size: 0.95rem; font-weight: 600; color: #fff; margin-bottom: 0.2rem; }
    .edu-card .inst { font-size: 0.85rem; color: var(--accent); margin-bottom: 0.2rem; }
    .edu-card .period { font-size: 0.78rem; color: var(--muted); }
    .coursework { margin-top: 0.6rem; display: flex; flex-wrap: wrap; gap: 0.35rem; }
 
    /* FOOTER */
    footer {
      background: var(--navy-mid);
      border-top: 1px solid var(--border);
      text-align: center;
      padding: 2rem 8%;
      font-size: 0.82rem; color: var(--muted);
    }
    footer a { color: var(--accent); text-decoration: none; }
 
    /* GITHUB SETUP SECTION */
    .github-setup {
      background: var(--navy-card);
      border: 1px solid var(--border);
      border-radius: 12px; padding: 1.6rem;
      margin-top: 1.5rem;
    }
    .github-setup h3 { font-family: var(--font-display); font-size: 1rem; font-weight: 600; color: #fff; margin-bottom: 1rem; }
    .step { display: flex; gap: 1rem; margin-bottom: 1rem; align-items: flex-start; }
    .step-num {
      flex-shrink: 0; width: 26px; height: 26px;
      border-radius: 50%; background: var(--accent);
      color: var(--navy); font-weight: 700; font-size: 0.8rem;
      display: flex; align-items: center; justify-content: center;
    }
    .step p { font-size: 0.87rem; color: #A8BFDB; }
    .step code {
      background: rgba(0,0,0,0.3); border: 1px solid var(--border);
      color: var(--accent); padding: 0.15rem 0.45rem; border-radius: 4px;
      font-size: 0.82rem;
    }
 
    @media (max-width: 768px) {
      .hero { flex-direction: column; text-align: center; }
      .hero-links { justify-content: center; }
      .about-grid, .hero { gap: 1.5rem; }
      .hero-avatar { width: 130px; height: 130px; }
      .hero-text h1 { font-size: 1.8rem; }
      .about-grid { grid-template-columns: 1fr; }
      nav { padding: 0 4%; }
      .nav-links { gap: 1rem; }
      .container { padding: 0 5%; }
    }
  </style>
</head>
<body>
 
<!-- NAV -->
<nav>
  <div class="nav-logo">NP</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#publications">Publications</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#certifications">Certs</a></li>
  </ul>
</nav>
 
<!-- HERO -->
<div class="container">
  <div class="hero">
    <img class="hero-avatar" src="profile.png" alt="Nara Pranay" />
    <div class="hero-text">
      <h1>Nara <span>Pranay</span></h1>
      <p class="hero-tagline">ECE Engineer · IEEE Leader · Embedded Systems · VLSI · Content Strategy</p>
      <p class="hero-bio">
        Electronics and Communication Engineering undergraduate (Class of 2026) from VBIT, Hyderabad. IEEE volunteer with 2.5+ years of leadership across technical, community, and media roles. Research-published, grant-secured, and hands-on with embedded systems, FPGA development, and deep learning — equally fluent in hardware and human communication.
      </p>
      <div class="hero-links">
        <a href="mailto:n.pranay2005@gmail.com">
          <svg viewBox="0 0 24 24"><path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
          n.pranay2005@gmail.com
        </a>
        <a href="https://www.linkedin.com/in/nara-pranay" target="_blank">
          <svg viewBox="0 0 24 24"><path d="M19 3a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h14m-.5 15.5v-5.3a3.26 3.26 0 0 0-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.79v8.37h2.79v-4.93c0-.77.62-1.4 1.39-1.4a1.4 1.4 0 0 1 1.4 1.4v4.93h2.79M6.88 8.56a1.68 1.68 0 0 0 1.68-1.68c0-.93-.75-1.69-1.68-1.69a1.69 1.69 0 0 0-1.69 1.69c0 .93.76 1.68 1.69 1.68m1.39 9.94v-8.37H5.5v8.37h2.77z"/></svg>
          LinkedIn
        </a>
        <a href="https://github.com/nara-pranay" target="_blank">
          <svg viewBox="0 0 24 24"><path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.09-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z"/></svg>
          GitHub
        </a>
      </div>
    </div>
  </div>
</div>
 
<!-- KEY ACHIEVEMENT BANNER -->
<div class="container">
  <div class="achievement-banner">
    <span class="trophy">🏆</span>
    <p><strong>Key Achievement:</strong> Secured a <strong>USD 500 IEEE Communications Society Grant</strong> as Chairperson to organize the ESPire Technical Workshop (Jan 30–31, 2026) — led proposal development, budgeting, compliance reporting, and hands-on hardware sessions. &nbsp;|&nbsp; <strong>🥈 2nd Prize — Aakar Project Expo</strong> for Satellite Image Semantic Segmentation.</p>
  </div>
</div>
 
<!-- DOMAINS -->
<div class="container">
  <section id="domains">
    <div class="section-label">
      <div class="dot"></div>
      <h2>Domains</h2>
      <div class="line"></div>
    </div>
    <div class="domains-grid">
      <div class="domain-card">
        <div class="icon">🔌</div>
        <h4>Embedded Systems</h4>
        <p>Raspberry Pi, Arduino, RFID, biometric sensors, real-time systems</p>
      </div>
      <div class="domain-card">
        <div class="icon">⚙️</div>
        <h4>VLSI & FPGA Design</h4>
        <p>Verilog HDL, RTL-to-GDSII, Cadence Innovus, Vivado, ALU design</p>
      </div>
      <div class="domain-card">
        <div class="icon">🤖</div>
        <h4>AI / Deep Learning</h4>
        <p>Transfer learning, semantic segmentation, CNNs, satellite imagery</p>
      </div>
      <div class="domain-card">
        <div class="icon">📡</div>
        <h4>IoT & Connectivity</h4>
        <p>Sensor integration, Gmail API, SQLite, automated notifications</p>
      </div>
      <div class="domain-card">
        <div class="icon">📣</div>
        <h4>Social Media & Marketing</h4>
        <p>Content strategy, digital campaigns, promotions, community growth</p>
      </div>
      <div class="domain-card">
        <div class="icon">🎯</div>
        <h4>Leadership & Management</h4>
        <p>IEEE governance, grant management, event coordination, team leadership</p>
      </div>
    </div>
  </section>
</div>
 
<!-- ABOUT -->
<div class="container">
  <section id="about">
    <div class="section-label">
      <div class="dot"></div>
      <h2>About Me</h2>
      <div class="line"></div>
    </div>
    <div class="about-grid">
      <div class="about-card">
        <h3>Who I Am</h3>
        <p>I'm Nara Pranay, an ECE undergraduate at VBIT, Hyderabad (graduating 2026), with a rare blend of technical depth and communication prowess. Whether it's designing embedded authentication systems, writing Verilog modules, or crafting digital campaigns that reach thousands of students — I bring the same rigour and energy to each domain.</p>
      </div>
      <div class="about-card">
        <h3>What I've Built</h3>
        <p>From a published IEEE research paper on RFID biometric systems achieving 98.5% accuracy, to a USD 500 grant-funded workshop and a 2nd prize at Aakar Expo for satellite segmentation — my work spans hardware, AI, and community impact. I've led teams, secured institutional funding, and represented my college at international conferences.</p>
      </div>
      <div class="about-card">
        <h3>Technical Personality</h3>
        <p>I gravitate toward systems that bridge hardware and intelligence — embedded platforms talking to cloud APIs, FPGAs running custom silicon, or CNNs parsing satellite pixels. I'm comfortable with Verilog at one end and Python at the other, and I believe great engineers also write clearly and communicate convincingly.</p>
      </div>
      <div class="about-card">
        <h3>Community Side</h3>
        <p>2.5+ years of IEEE volunteerism: Chairperson, Treasurer, RSM Coordinator. Led social media for Avishkar 2K24/25/26, served as President of SAC VBIT, and co-led Public Relations for Virinchi. I've built digital communities, run events, and mentored junior volunteers — because technology grows when its people grow.</p>
      </div>
    </div>
  </section>
</div>
 
<!-- KEY ACHIEVEMENTS STATS -->
<div class="container">
  <section id="achievements">
    <div class="section-label">
      <div class="dot"></div>
      <h2>Key Achievements</h2>
      <div class="line"></div>
    </div>
    <div class="ach-grid">
      <div class="ach-card">
        <div class="num">$500</div>
        <h4>IEEE ComSoc Grant</h4>
        <p>Secured institutional funding for ESPire Workshop 2026 as Chairperson</p>
      </div>
      <div class="ach-card">
        <div class="num">🥈</div>
        <h4>Aakar Expo — 2nd Prize</h4>
        <p>Multi-class satellite semantic segmentation using deep transfer learning</p>
      </div>
      <div class="ach-card">
        <div class="num">98.5%</div>
        <h4>Auth Accuracy</h4>
        <p>RFID + Biometric attendance system published at IEEE conference</p>
      </div>
      <div class="ach-card">
        <div class="num">2.5+</div>
        <h4>Years IEEE Leadership</h4>
        <p>Chairperson, Treasurer, RSM Coordinator, multiple event roles</p>
      </div>
      <div class="ach-card">
        <div class="num">1</div>
        <h4>International Publication</h4>
        <p>Published at IEEE-affiliated conference, Vaagdevi Engineering College, 2025</p>
      </div>
      <div class="ach-card">
        <div class="num">5+</div>
        <h4>Roles Held Simultaneously</h4>
        <p>Chairperson, SAC Lead, PR, Film Club, and RSM Coordinator at peak</p>
      </div>
    </div>
  </section>
</div>
 
<!-- EXPERIENCE TIMELINE -->
<div class="container">
  <section id="experience">
    <div class="section-label">
      <div class="dot"></div>
      <h2>Experience & Leadership</h2>
      <div class="line"></div>
    </div>
    <div class="timeline">
 
      <div class="tl-item">
        <div class="tl-date">Jan 2026 – Mar 2026</div>
        <div class="tl-org">Avishkar 2K26 · IEEE - VBIT SB</div>
        <div class="tl-title">Social Media Promotions Scrutinizer</div>
        <div class="tl-body"><p>Planned and monitored digital campaigns, ensured quality and consistency of promotional content across platforms for the flagship annual technical fest.</p></div>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Jul 2025 – Jun 2026</div>
        <div class="tl-org">IEEE Communications Society · IEEE - VBIT SB</div>
        <div class="tl-title">Chairperson</div>
        <div class="tl-body">
          <div class="highlight-badge">🏆 Secured USD 500 IEEE ComSoc Grant</div>
          <ul>
            <li>Led communication and outreach initiatives for IEEE ComSoc activities at VBIT</li>
            <li>Organized ESPire Technical Workshop (Jan 30–31, 2026) — proposal, budgeting, compliance, execution</li>
            <li>Planned and promoted workshops, technical events, and professional development programs</li>
            <li>Coordinated volunteer teams and managed student engagement activities</li>
          </ul>
        </div>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Jul 2025 – Jun 2026</div>
        <div class="tl-org">IEEE - VBIT SB</div>
        <div class="tl-title">RSM Coordinator (Resource & Skill Management)</div>
        <div class="tl-body"><p>Coordinated resource allocation and supported execution of technical events. Assisted in documentation, communication, and team coordination activities across branch-level programs.</p></div>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Jul 2025 – Jun 2026</div>
        <div class="tl-org">SAC · Vignana Bharathi Institute of Technology</div>
        <div class="tl-title">President, Student Activity Centre</div>
        <div class="tl-body"><p>Coordinated institute-level student activities and events. Managed communication between students, faculty, and organizing committees. Prepared presentations, reports, and activity documentation.</p></div>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Jun 2025 – Jun 2026</div>
        <div class="tl-org">Virinchi · VBIT</div>
        <div class="tl-title">Public Relations — Co-Lead</div>
        <div class="tl-body"><p>Managed public-facing communications and stakeholder relationships for VBIT's cultural and technical initiatives.</p></div>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Mar 2025 – Apr 2025</div>
        <div class="tl-org">IEEE Robotics and Automation Society (RAS), Hyderabad Section</div>
        <div class="tl-title">Virtual Intern — ES & IoT Research Program</div>
        <div class="tl-body"><p>Five-week program focused on embedded systems and IoT research. Gained hands-on exposure to system design, engineering workflows, and guided technical training under IEEE RAS Hyderabad Section leadership.</p></div>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Jan 2025 – Mar 2025</div>
        <div class="tl-org">Avishkar 2K25 · IEEE - VBIT SB</div>
        <div class="tl-title">Social Media Promotions Mentor</div>
        <div class="tl-body"><p>Guided the social media promotions team on digital strategy and event publicity. Created and reviewed promotional content and coordinated outreach activities.</p></div>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">May 2024 – Jun 2025</div>
        <div class="tl-org">IEEE Communications Society · IEEE - VBIT SB</div>
        <div class="tl-title">Treasurer</div>
        <div class="tl-body"><p>Managed society finances and event budgets. Maintained financial records, tracked expenditures, and assisted in preparing activity and financial reports.</p></div>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Jan 2024 – Oct 2024</div>
        <div class="tl-org">Aashay Film Club · VBIT</div>
        <div class="tl-title">Social Media Promotions Lead</div>
        <div class="tl-body"><p>Led social media strategy for VBIT's film club. Created engaging content, ran promotional campaigns, and grew the club's digital presence.</p></div>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Jan 2024 – Mar 2024</div>
        <div class="tl-org">Avishkar 2K24 · IEEE - VBIT SB</div>
        <div class="tl-title">Social Media Promotions Organizing Committee</div>
        <div class="tl-body"><p>Created and managed promotional content for event marketing. Supported digital communication and publicity activities for the annual tech fest.</p></div>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Aug 2023 – Jun 2026</div>
        <div class="tl-org">Student Activity Centre · VBIT</div>
        <div class="tl-title">Social Media Promotions</div>
        <div class="tl-body"><p>Managed social media campaigns for student activities and events over three years. Created promotional content and coordinated digital outreach initiatives.</p></div>
      </div>
 
    </div>
  </section>
</div>
 
<!-- PROJECTS -->
<div class="container">
  <section id="projects">
    <div class="section-label">
      <div class="dot"></div>
      <h2>Projects</h2>
      <div class="line"></div>
    </div>
    <div class="projects-grid">
 
      <div class="project-card">
        <div class="award-badge">🥈 Aakar 2nd Prize</div>
        <div class="ptype">AI / Deep Learning</div>
        <h3>Deep Transfer Learning for Multi-Class Satellite Image Segmentation</h3>
        <div class="pdate">Dec 2025 – Jan 2026</div>
        <p>Fine-tuned a deep transfer learning model for semantic segmentation of satellite imagery using pretrained CNNs. Achieved accurate pixel-level land cover classification with optimized performance metrics. Won 2nd Prize at Aakar — Project Expo.</p>
        <div class="tech-pills">
          <span class="tech-pill">Python</span>
          <span class="tech-pill">Deep Learning</span>
          <span class="tech-pill">CNN</span>
          <span class="tech-pill">Transfer Learning</span>
          <span class="tech-pill">Semantic Segmentation</span>
        </div>
      </div>
 
      <div class="project-card">
        <div class="ptype">VLSI / Digital Design</div>
        <h3>RTL to GDSII Mini Flow</h3>
        <div class="pdate">Sep 2025 – Dec 2025</div>
        <p>Implemented a complete RTL-to-GDSII ASIC design flow including synthesis, placement, clock tree synthesis, routing, and timing analysis using Cadence tool environment.</p>
        <div class="tech-pills">
          <span class="tech-pill">Cadence Innovus</span>
          <span class="tech-pill">Verilog HDL</span>
          <span class="tech-pill">STA</span>
          <span class="tech-pill">ASIC Flow</span>
        </div>
      </div>
 
      <div class="project-card">
        <div class="ptype">FPGA / RTL Design</div>
        <h3>16-bit ALU Using Verilog HDL</h3>
        <div class="pdate">Jul 2025 – Sep 2025</div>
        <p>Designed and simulated a 16-bit Arithmetic Logic Unit (ALU) in Verilog HDL supporting arithmetic and logical operations. Developed RTL modules and verified functionality through testbench simulation on Vivado.</p>
        <div class="tech-pills">
          <span class="tech-pill">Verilog HDL</span>
          <span class="tech-pill">Xilinx Vivado</span>
          <span class="tech-pill">RTL Design</span>
          <span class="tech-pill">Testbench</span>
        </div>
      </div>
 
      <div class="project-card">
        <div class="ptype">Embedded Systems / IoT</div>
        <h3>Smart Attendance System — RFID + Fingerprint + Gmail</h3>
        <div class="pdate">Jan 2025 – Jun 2025</div>
        <p>Designed a Raspberry Pi-based smart attendance system integrating RFID and fingerprint biometric authentication. Implemented Python control logic, SQLite offline database, and automated Gmail API notifications — achieving 98.5% authentication accuracy. Published at IEEE conference.</p>
        <div class="tech-pills">
          <span class="tech-pill">Raspberry Pi</span>
          <span class="tech-pill">Python</span>
          <span class="tech-pill">RFID</span>
          <span class="tech-pill">Biometrics</span>
          <span class="tech-pill">SQLite</span>
          <span class="tech-pill">Gmail API</span>
        </div>
      </div>
 
      <div class="project-card">
        <div class="ptype">Embedded Systems / Sensing</div>
        <h3>Earthquake Detector Using Arduino UNO</h3>
        <div class="pdate">Jul 2024 – Dec 2024</div>
        <p>Built a low-cost, real-time seismic activity detection system using Arduino Uno and ADXL335 accelerometer. Performed sensor calibration and threshold tuning to distinguish seismic events from environmental noise, displaying live alerts on a 16×2 LCD.</p>
        <div class="tech-pills">
          <span class="tech-pill">Arduino Uno</span>
          <span class="tech-pill">ADXL335</span>
          <span class="tech-pill">C</span>
          <span class="tech-pill">LCD Display</span>
          <span class="tech-pill">Sensor Calibration</span>
        </div>
      </div>
 
    </div>
  </section>
</div>
 
<!-- PUBLICATIONS -->
<div class="container">
  <section id="publications">
    <div class="section-label">
      <div class="dot"></div>
      <h2>Publications</h2>
      <div class="line"></div>
    </div>
    <div class="pub-card">
      <h3>Smart Attendance Framework Using RFID and Fingerprint-Based Dual Authentication with Real-Time Email Notifications</h3>
      <div class="venue">📄 2nd International Conference on Recent Trends in Electrical, Electronics and Computing Technologies — IEEE | Vaagdevi Engineering College, Telangana | October 2025</div>
      <p>Designed and presented a Raspberry Pi-based embedded authentication system integrating RFID and biometric fingerprint verification. Implemented Python control logic, SQLite database, and Gmail API notifications achieving <strong style="color:var(--accent)">98.5% authentication accuracy</strong>. Presented system architecture and performance evaluation at an IEEE-affiliated international conference.</p>
    </div>
  </section>
</div>
 
<!-- SKILLS -->
<div class="container">
  <section id="skills">
    <div class="section-label">
      <div class="dot"></div>
      <h2>Skills</h2>
      <div class="line"></div>
    </div>
    <div class="skills-grid">
      <div class="skill-group">
        <h4>VLSI & Digital Design</h4>
        <div class="skill-tags">
          <span class="skill-tag">Verilog HDL</span>
          <span class="skill-tag">RTL Design</span>
          <span class="skill-tag">FPGA Design</span>
          <span class="skill-tag">ASIC Flow</span>
          <span class="skill-tag">Timing Analysis</span>
          <span class="skill-tag">STA Fundamentals</span>
          <span class="skill-tag">Physical Design</span>
          <span class="skill-tag">CMOS Basics</span>
          <span class="skill-tag">Digital Electronics</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Embedded Systems & IoT</h4>
        <div class="skill-tags">
          <span class="skill-tag">Raspberry Pi</span>
          <span class="skill-tag">Arduino Uno</span>
          <span class="skill-tag">RFID Integration</span>
          <span class="skill-tag">Biometric Sensors</span>
          <span class="skill-tag">Hardware Interfacing</span>
          <span class="skill-tag">Real-Time Systems</span>
          <span class="skill-tag">SQLite</span>
          <span class="skill-tag">Gmail API</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>EDA & Development Tools</h4>
        <div class="skill-tags">
          <span class="skill-tag">Cadence Virtuoso</span>
          <span class="skill-tag">Cadence Innovus</span>
          <span class="skill-tag">Xilinx Vivado</span>
          <span class="skill-tag">MATLAB</span>
          <span class="skill-tag">Scilab</span>
          <span class="skill-tag">Arduino IDE</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Programming & Scripting</h4>
        <div class="skill-tags">
          <span class="skill-tag">Python</span>
          <span class="skill-tag">C</span>
          <span class="skill-tag">Verilog</span>
          <span class="skill-tag">TCL Scripting</span>
          <span class="skill-tag">Shell Scripting</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>AI & Deep Learning</h4>
        <div class="skill-tags">
          <span class="skill-tag">Transfer Learning</span>
          <span class="skill-tag">CNN</span>
          <span class="skill-tag">Semantic Segmentation</span>
          <span class="skill-tag">Model Fine-Tuning</span>
          <span class="skill-tag">Evaluation Metrics</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Social Media & Marketing</h4>
        <div class="skill-tags">
          <span class="skill-tag">Social Media Management</span>
          <span class="skill-tag">Content Strategy</span>
          <span class="skill-tag">Content Creation</span>
          <span class="skill-tag">Copywriting</span>
          <span class="skill-tag">Digital Marketing</span>
          <span class="skill-tag">Public Relations</span>
          <span class="skill-tag">Community Engagement</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Leadership & Administration</h4>
        <div class="skill-tags">
          <span class="skill-tag">Team Leadership</span>
          <span class="skill-tag">Volunteer Management</span>
          <span class="skill-tag">Event Coordination</span>
          <span class="skill-tag">Grant Management</span>
          <span class="skill-tag">Budget Management</span>
          <span class="skill-tag">Stakeholder Communication</span>
          <span class="skill-tag">Proposal Writing</span>
          <span class="skill-tag">Technical Documentation</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Productivity & Office Tools</h4>
        <div class="skill-tags">
          <span class="skill-tag">MS PowerPoint</span>
          <span class="skill-tag">MS Word</span>
          <span class="skill-tag">MS Excel</span>
          <span class="skill-tag">Report Preparation</span>
          <span class="skill-tag">Technical Writing</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Core ECE Coursework</h4>
        <div class="skill-tags">
          <span class="skill-tag">VLSI Design</span>
          <span class="skill-tag">CMOS Technology</span>
          <span class="skill-tag">Embedded Systems</span>
          <span class="skill-tag">Signals & Systems</span>
          <span class="skill-tag">Microprocessors</span>
          <span class="skill-tag">Microcontrollers</span>
          <span class="skill-tag">FPGA Design</span>
        </div>
      </div>
    </div>
  </section>
</div>
 
<!-- EDUCATION -->
<div class="container">
  <section id="education">
    <div class="section-label">
      <div class="dot"></div>
      <h2>Education</h2>
      <div class="line"></div>
    </div>
 
    <div class="edu-card">
      <div class="edu-icon">🎓</div>
      <div>
        <h4>Bachelor of Technology — Electronics & Communication Engineering</h4>
        <div class="inst">Vignana Bharathi Institute of Technology (VBIT), Hyderabad</div>
        <div class="period">September 2022 – April 2026</div>
        <div class="coursework">
          <span class="skill-tag">VLSI Design</span>
          <span class="skill-tag">Embedded Systems</span>
          <span class="skill-tag">FPGA Design</span>
          <span class="skill-tag">Digital Electronics</span>
          <span class="skill-tag">CMOS Technology</span>
          <span class="skill-tag">Signals & Systems</span>
          <span class="skill-tag">Microprocessors & Microcontrollers</span>
        </div>
      </div>
    </div>
 
    <div class="edu-card">
      <div class="edu-icon">📚</div>
      <div>
        <h4>Intermediate — MPC (Maths, Physics, Chemistry)</h4>
        <div class="inst">Sri Chaitanya Junior Kalasala (Sri Chaitanya College of Education)</div>
        <div class="period">April 2020 – May 2022</div>
      </div>
    </div>
 
    <div class="edu-card">
      <div class="edu-icon">🏫</div>
      <div>
        <h4>Secondary Schooling</h4>
        <div class="inst">English Union High School</div>
        <div class="period">March 2008 – April 2020</div>
      </div>
    </div>
 
  </section>
</div>
 
<!-- CERTIFICATIONS -->
<div class="container">
  <section id="certifications">
    <div class="section-label">
      <div class="dot"></div>
      <h2>Certifications & Licenses</h2>
      <div class="line"></div>
    </div>
    <div class="cert-grid">
 
      <!-- AICTE Virtual Internships -->
      <div class="cert-card">
        <div class="cert-icon">☁️</div>
        <div>
          <h4>AWS Cloud Virtual Internship</h4>
          <p>AICTE · Jul 2024 – Sep 2024</p>
          <p style="font-size:0.72rem;color:var(--muted);margin-top:0.2rem;">ID: 6f92ff1d00c9b4007e16f83b4aacea25</p>
        </div>
      </div>
 
      <div class="cert-card">
        <div class="cert-icon">⛏️</div>
        <div>
          <h4>Celonis Process Mining Virtual Internship</h4>
          <p>AICTE · Sep 2023 – Nov 2023</p>
          <p style="font-size:0.72rem;color:var(--muted);margin-top:0.2rem;">ID: df907133a3b5f56064ff3f03628f1991</p>
        </div>
      </div>
 
      <div class="cert-card">
        <div class="cert-icon">🔧</div>
        <div>
          <h4>Embedded System Developer Virtual Internship</h4>
          <p>AICTE · Jul 2024 – Sep 2024</p>
          <p style="font-size:0.72rem;color:var(--muted);margin-top:0.2rem;">ID: e562e00da6acd0b498f2a7a40e5cc590</p>
        </div>
      </div>
 
      <div class="cert-card">
        <div class="cert-icon">🤖</div>
        <div>
          <h4>Google AI-ML Virtual Internship</h4>
          <p>AICTE · Apr 2024 – Jun 2024</p>
          <p style="font-size:0.72rem;color:var(--muted);margin-top:0.2rem;">ID: ad1d1b6372c0c471685d5ed286acf556</p>
        </div>
      </div>
 
      <div class="cert-card">
        <div class="cert-icon">🐍</div>
        <div>
          <h4>Python Full Stack Developer Virtual Internship</h4>
          <p>AICTE · Oct 2024 – Dec 2024</p>
          <p style="font-size:0.72rem;color:var(--muted);margin-top:0.2rem;">ID: 4bab8065ddc62cb7f33fcc42ea21c5f0</p>
        </div>
      </div>
 
      <!-- Professional Certificates -->
      <div class="cert-card">
        <div class="cert-icon">🖥️</div>
        <div>
          <h4>System Administration Micro-Certification</h4>
          <p>ServiceNow</p>
        </div>
      </div>
 
      <div class="cert-card">
        <div class="cert-icon">☕</div>
        <div>
          <h4>Java Full Stack — Digital Skills Readiness Program</h4>
          <p>TalentNext × Wipro Limited</p>
        </div>
      </div>
 
      <div class="cert-card">
        <div class="cert-icon">🐍</div>
        <div>
          <h4>The Complete Python Course</h4>
          <p>Professional Certification</p>
        </div>
      </div>
 
      <!-- Volunteer Certificates -->
      <div class="cert-card">
        <div class="cert-icon">🌐</div>
        <div>
          <h4>Leveraging U.S.–India TRUST: AI & Cybersecurity</h4>
          <p>World Trade Center Shamshad & U.S. Consulate General, Hyderabad · Jan 29, 2026</p>
        </div>
      </div>
 
      <div class="cert-card">
        <div class="cert-icon">🎓</div>
        <div>
          <h4>Kaushal Mahotsav — Skill Development & Career Counselling</h4>
          <p>NSDC · Jun 3–4, 2023</p>
        </div>
      </div>
 
    </div>
  </section>
</div>
 
<!-- IEEE MEMBERSHIPS -->
<div class="container">
  <section>
    <div class="section-label">
      <div class="dot"></div>
      <h2>IEEE Memberships</h2>
      <div class="line"></div>
    </div>
    <div class="cert-grid">
      <div class="cert-card">
        <div class="cert-icon">📡</div>
        <div><h4>IEEE Student Member</h4><p>Nov 2024 – Present</p></div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">💻</div>
        <div><h4>IEEE Computer Society Student Member</h4><p>Nov 2024 – Present</p></div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">📶</div>
        <div><h4>IEEE Communications Society Student Member</h4><p>Nov 2024 – Present</p></div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">👩‍💻</div>
        <div><h4>IEEE Women in Engineering Student Member</h4><p>Nov 2024 – Present</p></div>
      </div>
    </div>
  </section>
</div>
 
<!-- GITHUB SETUP GUIDE -->
<div class="container">
  <section id="github-setup">
    <div class="section-label">
      <div class="dot"></div>
      <h2>How to Deploy This on GitHub</h2>
      <div class="line"></div>
    </div>
    <div class="github-setup">
      <h3>📦 Step-by-Step GitHub Pages Setup</h3>
      <div class="step">
        <div class="step-num">1</div>
        <p>Create a new GitHub repository named exactly <code>nara-pranay.github.io</code> (your GitHub username must be <code>nara-pranay</code>). Make it public.</p>
      </div>
      <div class="step">
        <div class="step-num">2</div>
        <p>Save this file as <code>index.html</code> and your profile photo as <code>profile.png</code>. Place both in the same folder on your computer.</p>
      </div>
      <div class="step">
        <div class="step-num">3</div>
        <p>Upload both files to your repository: click <code>Add file → Upload files</code>, drag both files in, and commit with message <code>Initial portfolio</code>.</p>
      </div>
      <div class="step">
        <div class="step-num">4</div>
        <p>Go to <code>Settings → Pages → Source</code>. Set branch to <code>main</code>, folder to <code>/ (root)</code>, and click <code>Save</code>.</p>
      </div>
      <div class="step">
        <div class="step-num">5</div>
        <p>Your portfolio will be live at <code>https://nara-pranay.github.io</code> within 2–3 minutes. Share this URL on your LinkedIn, resume, and IEEE profile!</p>
      </div>
      <div class="step">
        <div class="step-num">6</div>
        <p><strong style="color:var(--accent)">Pro tip:</strong> Pin this repository on your GitHub profile, add a custom description, and add topics like <code>portfolio</code>, <code>ece</code>, <code>ieee</code>, <code>vlsi</code>, <code>embedded-systems</code>.</p>
      </div>
    </div>
  </section>
</div>
 
<!-- FOOTER -->
<footer>
  <p style="margin-bottom:0.5rem; font-family:var(--font-display); font-size:1rem; color:#fff;">Nara Pranay</p>
  <p>ECE '26 · VBIT Hyderabad · IEEE Volunteer</p>
  <p style="margin-top:0.5rem;">
    <a href="mailto:n.pranay2005@gmail.com">n.pranay2005@gmail.com</a> &nbsp;·&nbsp;
    <a href="https://www.linkedin.com/in/nara-pranay" target="_blank">LinkedIn</a> &nbsp;·&nbsp;
    <a href="https://github.com/nara-pranay" target="_blank">GitHub</a>
  </p>
  <p style="margin-top:1rem; font-size:0.75rem; color:rgba(139,170,200,0.5);">© 2026 Nara Pranay · Built with ❤️ and clean code</p>
</footer>
 
</body>
</html>
 
