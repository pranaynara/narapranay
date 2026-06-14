<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nara Pranay — GitHub Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --navy: #0D1B2A;
    --navy-mid: #1A2C42;
    --navy-light: #243B55;
    --gold: #C9A84C;
    --gold-light: #E8C96A;
    --gold-pale: #F5E6C0;
    --white: #FFFFFF;
    --off-white: #F8F9FA;
    --text-primary: #1A1A2E;
    --text-secondary: #4A5568;
    --text-muted: #718096;
    --border: #E2E8F0;
    --border-dark: #CBD5E0;
    --accent-teal: #2C7873;
    --accent-teal-light: #EAF5F3;
    --badge-bg: #EFF6FF;
    --badge-border: #BFDBFE;
    --badge-text: #1E40AF;
  }

  body {
    font-family: 'Inter', sans-serif;
    background: var(--off-white);
    color: var(--text-primary);
    line-height: 1.7;
    min-height: 100vh;
  }

  /* ── HERO ── */
  .hero {
    background: var(--navy);
    position: relative;
    overflow: hidden;
    padding: 0;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -60px; right: -60px;
    width: 320px; height: 320px;
    border: 1px solid rgba(201,168,76,0.15);
    border-radius: 50%;
  }
  .hero::after {
    content: '';
    position: absolute;
    bottom: -80px; left: -40px;
    width: 240px; height: 240px;
    border: 1px solid rgba(201,168,76,0.1);
    border-radius: 50%;
  }

  .hero-inner {
    max-width: 900px;
    margin: 0 auto;
    padding: 64px 40px 56px;
    display: flex;
    align-items: center;
    gap: 48px;
    position: relative;
    z-index: 1;
  }

  .hero-avatar {
    flex-shrink: 0;
    width: 140px;
    height: 140px;
    border-radius: 50%;
    border: 3px solid var(--gold);
    object-fit: cover;
    display: block;
  }

  .hero-avatar-placeholder {
    width: 140px; height: 140px;
    border-radius: 50%;
    border: 3px solid var(--gold);
    background: var(--navy-mid);
    display: flex; align-items: center; justify-content: center;
    font-size: 44px; font-weight: 700;
    color: var(--gold);
    flex-shrink: 0;
    letter-spacing: -1px;
  }

  .hero-text {}

  .hero-eyebrow {
    font-size: 12px;
    font-weight: 500;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 10px;
  }

  .hero-name {
    font-size: 42px;
    font-weight: 700;
    color: var(--white);
    line-height: 1.1;
    margin-bottom: 8px;
  }

  .hero-title {
    font-size: 16px;
    font-weight: 400;
    color: rgba(255,255,255,0.65);
    margin-bottom: 20px;
    line-height: 1.5;
  }

  .hero-links {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .hero-link {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 7px 16px;
    border: 1px solid rgba(201,168,76,0.4);
    border-radius: 6px;
    color: var(--gold-light);
    text-decoration: none;
    font-size: 13px;
    font-weight: 500;
    transition: background 0.2s, border-color 0.2s;
  }
  .hero-link:hover {
    background: rgba(201,168,76,0.12);
    border-color: var(--gold);
  }
  .hero-link svg { width: 14px; height: 14px; fill: currentColor; flex-shrink: 0; }

  /* ── GOLD RULE ── */
  .gold-rule {
    height: 3px;
    background: linear-gradient(90deg, var(--gold) 0%, var(--gold-light) 50%, transparent 100%);
    max-width: 900px;
    margin: 0 auto;
  }

  /* ── LAYOUT ── */
  .container {
    max-width: 900px;
    margin: 0 auto;
    padding: 0 40px;
  }

  section {
    padding: 52px 0;
    border-bottom: 1px solid var(--border);
  }
  section:last-child { border-bottom: none; }

  .section-label {
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 6px;
  }

  .section-title {
    font-size: 26px;
    font-weight: 700;
    color: var(--text-primary);
    margin-bottom: 28px;
  }

  /* ── ABOUT ── */
  .about-text {
    font-size: 16px;
    line-height: 1.85;
    color: var(--text-secondary);
    max-width: 760px;
  }
  .about-text strong { color: var(--text-primary); font-weight: 600; }

  /* ── KEY ACHIEVEMENTS ── */
  .achievement-banner {
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-mid) 100%);
    border-radius: 12px;
    padding: 32px 36px;
    margin-bottom: 28px;
    border: 1px solid rgba(201,168,76,0.25);
    position: relative;
    overflow: hidden;
  }
  .achievement-banner::before {
    content: '★';
    position: absolute;
    right: 30px; top: 20px;
    font-size: 80px;
    color: rgba(201,168,76,0.07);
    line-height: 1;
  }
  .achievement-banner-title {
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 8px;
  }
  .achievement-banner-text {
    font-size: 17px;
    font-weight: 600;
    color: var(--white);
    line-height: 1.5;
  }
  .achievement-banner-sub {
    font-size: 14px;
    color: rgba(255,255,255,0.55);
    margin-top: 6px;
  }

  .achievements-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }
  .achievement-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 20px 22px;
    display: flex;
    gap: 14px;
    align-items: flex-start;
  }
  .achievement-icon {
    width: 36px; height: 36px;
    border-radius: 8px;
    background: var(--gold-pale);
    display: flex; align-items: center; justify-content: center;
    font-size: 17px;
    flex-shrink: 0;
    color: #8B6914;
  }
  .achievement-card-title {
    font-size: 14px;
    font-weight: 600;
    color: var(--text-primary);
    margin-bottom: 3px;
  }
  .achievement-card-sub {
    font-size: 13px;
    color: var(--text-muted);
    line-height: 1.5;
  }

  /* ── TIMELINE (Experience) ── */
  .timeline { position: relative; padding-left: 28px; }
  .timeline::before {
    content: '';
    position: absolute;
    left: 0; top: 8px; bottom: 0;
    width: 1px;
    background: var(--border-dark);
  }

  .timeline-group { margin-bottom: 36px; }
  .timeline-group:last-child { margin-bottom: 0; }

  .timeline-dot {
    position: absolute;
    left: -28px;
    width: 10px; height: 10px;
    border-radius: 50%;
    background: var(--gold);
    border: 2px solid var(--white);
    box-shadow: 0 0 0 2px var(--border-dark);
    margin-top: 5px;
  }

  .timeline-item {
    position: relative;
    margin-bottom: 24px;
  }
  .timeline-item:last-child { margin-bottom: 0; }

  .timeline-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 4px;
    margin-bottom: 2px;
  }

  .timeline-role {
    font-size: 15px;
    font-weight: 600;
    color: var(--text-primary);
  }
  .timeline-period {
    font-size: 12px;
    font-weight: 500;
    color: var(--text-muted);
    white-space: nowrap;
    padding-top: 2px;
  }
  .timeline-org {
    font-size: 13px;
    font-weight: 500;
    color: var(--accent-teal);
    margin-bottom: 6px;
  }
  .timeline-bullets {
    font-size: 13px;
    color: var(--text-secondary);
    list-style: none;
    padding: 0;
  }
  .timeline-bullets li {
    padding: 2px 0 2px 14px;
    position: relative;
    line-height: 1.6;
  }
  .timeline-bullets li::before {
    content: '–';
    position: absolute;
    left: 0;
    color: var(--gold);
    font-weight: 700;
  }

  .timeline-year-marker {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--gold);
    background: #FFF8E8;
    border: 1px solid #F0D98B;
    border-radius: 4px;
    padding: 2px 10px;
    display: inline-block;
    margin-bottom: 18px;
  }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }
  .project-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 22px;
    position: relative;
    overflow: hidden;
  }
  .project-card::after {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--navy) 0%, var(--gold) 100%);
  }
  .project-label {
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--text-muted);
    margin-bottom: 8px;
  }
  .project-title {
    font-size: 15px;
    font-weight: 700;
    color: var(--text-primary);
    margin-bottom: 8px;
    line-height: 1.4;
  }
  .project-desc {
    font-size: 13px;
    color: var(--text-secondary);
    line-height: 1.65;
    margin-bottom: 14px;
  }
  .project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }
  .tag {
    font-size: 11px;
    font-weight: 500;
    padding: 3px 10px;
    border-radius: 20px;
    background: var(--badge-bg);
    color: var(--badge-text);
    border: 1px solid var(--badge-border);
    font-family: 'JetBrains Mono', monospace;
  }
  .tag.teal { background: var(--accent-teal-light); color: #1A5C55; border-color: #9BD0CC; }
  .tag.gold { background: #FFF8E8; color: #7A5C10; border-color: #F0D98B; }
  .tag.pub {
    background: #FFF1F0;
    color: #9B1C1C;
    border: 1px solid #FCA5A5;
    font-size: 10px;
    letter-spacing: 1px;
    text-transform: uppercase;
    font-family: 'Inter', sans-serif;
    font-weight: 600;
  }

  .project-date {
    font-size: 11px;
    color: var(--text-muted);
    margin-top: 8px;
  }

  /* ── SKILLS ── */
  .skills-section {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }
  .skill-group {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 20px 22px;
  }
  .skill-group-title {
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
    color: var(--navy);
    margin-bottom: 12px;
    padding-bottom: 10px;
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .skill-group-title span {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--gold);
    display: inline-block;
  }
  .skill-pills {
    display: flex;
    flex-wrap: wrap;
    gap: 7px;
  }
  .skill-pill {
    font-size: 12px;
    font-weight: 500;
    padding: 4px 12px;
    border-radius: 20px;
    background: var(--off-white);
    border: 1px solid var(--border-dark);
    color: var(--text-secondary);
  }

  /* ── EDUCATION ── */
  .edu-card {
    display: flex;
    gap: 20px;
    padding: 22px 0;
    border-bottom: 1px solid var(--border);
  }
  .edu-card:last-child { border-bottom: none; padding-bottom: 0; }
  .edu-year {
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    color: var(--text-muted);
    min-width: 90px;
    padding-top: 3px;
  }
  .edu-info {}
  .edu-degree {
    font-size: 15px;
    font-weight: 600;
    color: var(--text-primary);
    margin-bottom: 3px;
  }
  .edu-school {
    font-size: 14px;
    font-weight: 500;
    color: var(--accent-teal);
    margin-bottom: 4px;
  }
  .edu-note {
    font-size: 13px;
    color: var(--text-muted);
  }

  /* ── PUBLICATION ── */
  .pub-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 22px;
    position: relative;
    border-left: 4px solid var(--gold);
  }
  .pub-title {
    font-size: 15px;
    font-weight: 600;
    color: var(--text-primary);
    margin-bottom: 8px;
    line-height: 1.5;
  }
  .pub-venue {
    font-size: 13px;
    color: var(--accent-teal);
    font-weight: 500;
    margin-bottom: 6px;
  }
  .pub-details {
    font-size: 13px;
    color: var(--text-muted);
    margin-bottom: 10px;
  }
  .pub-bullets {
    font-size: 13px;
    color: var(--text-secondary);
    list-style: none;
    padding: 0;
  }
  .pub-bullets li {
    padding: 2px 0 2px 14px;
    position: relative;
  }
  .pub-bullets li::before {
    content: '·';
    position: absolute;
    left: 2px;
    color: var(--gold);
    font-weight: 900;
    font-size: 16px;
    line-height: 1.3;
  }

  /* ── CERTIFICATES ── */
  .cert-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 14px;
  }
  .cert-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px 18px;
    display: flex;
    gap: 12px;
    align-items: flex-start;
  }
  .cert-icon {
    width: 32px; height: 32px;
    border-radius: 7px;
    display: flex; align-items: center; justify-content: center;
    font-size: 15px;
    flex-shrink: 0;
  }
  .cert-icon.vol { background: #EFF6FF; color: #1D4ED8; }
  .cert-icon.pro { background: #F0FDF4; color: #166534; }
  .cert-title {
    font-size: 13px;
    font-weight: 600;
    color: var(--text-primary);
    margin-bottom: 2px;
    line-height: 1.4;
  }
  .cert-issuer {
    font-size: 12px;
    color: var(--text-muted);
  }

  /* ── INTERNSHIP ── */
  .intern-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 22px;
    border-left: 4px solid var(--accent-teal);
  }
  .intern-title {
    font-size: 15px; font-weight: 600; color: var(--text-primary); margin-bottom: 4px;
  }
  .intern-org {
    font-size: 14px; font-weight: 500; color: var(--accent-teal); margin-bottom: 4px;
  }
  .intern-period {
    font-size: 12px; color: var(--text-muted); margin-bottom: 10px;
  }
  .intern-desc {
    font-size: 13px; color: var(--text-secondary); line-height: 1.65;
  }

  /* ── DOMAINS ── */
  .domains-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
  }
  .domain-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 20px;
    text-align: center;
  }
  .domain-icon {
    font-size: 28px;
    margin-bottom: 10px;
    display: block;
  }
  .domain-name {
    font-size: 13px;
    font-weight: 700;
    color: var(--text-primary);
    margin-bottom: 4px;
  }
  .domain-sub {
    font-size: 12px;
    color: var(--text-muted);
  }

  /* ── FOOTER ── */
  .footer {
    background: var(--navy);
    padding: 40px;
    text-align: center;
  }
  .footer-name {
    font-size: 22px;
    font-weight: 700;
    color: var(--white);
    margin-bottom: 6px;
  }
  .footer-sub {
    font-size: 14px;
    color: rgba(255,255,255,0.5);
    margin-bottom: 20px;
  }
  .footer-links {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 28px;
  }
  .footer-link {
    color: var(--gold-light);
    text-decoration: none;
    font-size: 13px;
    padding: 6px 14px;
    border: 1px solid rgba(201,168,76,0.3);
    border-radius: 5px;
  }
  .footer-link:hover { border-color: var(--gold); }
  .footer-copy {
    font-size: 12px;
    color: rgba(255,255,255,0.25);
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 640px) {
    .hero-inner { flex-direction: column; text-align: center; padding: 40px 24px; }
    .hero-links { justify-content: center; }
    .container { padding: 0 20px; }
    .projects-grid, .skills-section, .achievements-grid, .cert-grid, .domains-grid {
      grid-template-columns: 1fr;
    }
    .hero-name { font-size: 30px; }
  }
</style>
</head>
<body>

<!-- ░░ HERO ░░ -->
<header class="hero">
  <div class="hero-inner">
    <div class="hero-avatar-placeholder">NP</div>
    <div class="hero-text">
      <p class="hero-eyebrow">Electronics &amp; Communication Engineering</p>
      <h1 class="hero-name">Nara Pranay</h1>
      <p class="hero-title">
        IEEE Leader · Embedded Systems · VLSI &amp; Digital Design · Content &amp; Communications · Student Community Builder
      </p>
      <div class="hero-links">
        <a class="hero-link" href="mailto:n.pranay2005@gmail.com">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M20 4H4C2.9 4 2 4.9 2 6v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4-8 5-8-5V6l8 5 8-5v2z"/></svg>
          n.pranay2005@gmail.com
        </a>
        <a class="hero-link" href="https://www.linkedin.com/in/nara-pranay" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M19 3a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h14m-.5 15.5v-5.3a3.26 3.26 0 0 0-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.79v8.37h2.79v-4.93c0-.77.62-1.4 1.39-1.4a1.4 1.4 0 0 1 1.4 1.4v4.93h2.79M6.88 8.56a1.68 1.68 0 0 0 1.68-1.68c0-.93-.75-1.69-1.68-1.69a1.69 1.69 0 0 0-1.69 1.69c0 .93.76 1.68 1.69 1.68m1.39 9.94v-8.37H5.5v8.37h2.77z"/></svg>
          LinkedIn
        </a>
        <a class="hero-link" href="https://github.com/nara-pranay" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.09-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z"/></svg>
          GitHub
        </a>
        <a class="hero-link" href="https://www.linkedin.com/in/nara-pranay" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 15v-4H7l5-8v4h4l-5 8z"/></svg>
          Hyderabad, India
        </a>
      </div>
    </div>
  </div>
  <div class="gold-rule"></div>
</header>

<!-- ░░ ABOUT ░░ -->
<div class="container">
  <section>
    <p class="section-label">Profile</p>
    <h2 class="section-title">About Me</h2>
    <p class="about-text">
      I am an <strong>Electronics and Communication Engineering graduate (Class of 2026)</strong> from Vignana Bharathi Institute of Technology, Hyderabad, with a strong foundation in embedded systems, VLSI design, and digital hardware. Over four years of active involvement in IEEE, student governance, and technical events have shaped me into both an engineer and a communicator.
    </p>
    <br>
    <p class="about-text">
      As <strong>Chairperson of IEEE Communications Society, VBIT Student Branch</strong>, I secured a <strong>USD 500 IEEE international grant</strong> and led the ESPire Technical Workshop — an achievement that reflects my ability to combine technical vision with leadership execution. As <strong>President of the Student Activity Centre (SAC), VBIT</strong>, I coordinated institution-wide student events and built cross-functional teams.
    </p>
    <br>
    <p class="about-text">
      My technical interests span <strong>FPGA design, VLSI physical design, embedded systems, and IoT</strong>. I have authored an internationally published conference paper, competed in project expos, and built real-world systems using Raspberry Pi, Arduino, Python, and Verilog. Beyond engineering, I bring expertise in <strong>social media strategy, digital promotions, content creation, and community building</strong> — making me a versatile professional who bridges technical depth with communication excellence.
    </p>
  </section>

  <!-- ░░ KEY ACHIEVEMENTS ░░ -->
  <section>
    <p class="section-label">Recognition</p>
    <h2 class="section-title">Key Achievements</h2>

    <div class="achievement-banner">
      <p class="achievement-banner-title">⭐ Highlight</p>
      <p class="achievement-banner-text">Secured USD 500 IEEE Communications Society International Grant</p>
      <p class="achievement-banner-sub">ESPire Technical Workshop · IEEE ComSoc VBIT SB · January 30–31, 2026 · Led proposal development, budgeting, compliance reporting &amp; hands-on hardware sessions</p>
    </div>

    <div class="achievements-grid">
      <div class="achievement-card">
        <div class="achievement-icon">🏆</div>
        <div>
          <p class="achievement-card-title">2nd Prize — Aakar Project Expo</p>
          <p class="achievement-card-sub">Satellite Image Semantic Segmentation using Deep Transfer Learning · Multi-class pixel-level classification</p>
        </div>
      </div>
      <div class="achievement-card">
        <div class="achievement-icon">📄</div>
        <div>
          <p class="achievement-card-title">International Conference Publication</p>
          <p class="achievement-card-sub">IEEE-affiliated 2nd International Conference on Recent Trends in Electrical, Electronics &amp; Computing Technologies · Vaagdevi Engineering College · Oct 2025</p>
        </div>
      </div>
      <div class="achievement-card">
        <div class="achievement-icon">🎯</div>
        <div>
          <p class="achievement-card-title">IEEE ComSoc Chairperson</p>
          <p class="achievement-card-sub">Led communication strategy, event promotions, and student engagement as head of Communications Society, IEEE VBIT SB</p>
        </div>
      </div>
      <div class="achievement-card">
        <div class="achievement-icon">🏛</div>
        <div>
          <p class="achievement-card-title">President, SAC VBIT</p>
          <p class="achievement-card-sub">Directed institution-level student activities, coordinated between students, faculty and organizing committees across VBIT</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ░░ EXPERIENCE ░░ -->
  <section>
    <p class="section-label">Experience</p>
    <h2 class="section-title">Leadership &amp; Roles — Year by Year</h2>

    <div class="timeline">

      <div class="timeline-year-marker">2025 – 2026</div>

      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-header">
          <span class="timeline-role">Chairperson — IEEE Communications Society</span>
          <span class="timeline-period">Jul 2025 – Jun 2026</span>
        </div>
        <p class="timeline-org">IEEE Communications Society · VBIT Student Branch</p>
        <ul class="timeline-bullets">
          <li>Led communication and outreach for all IEEE ComSoc activities at the branch level</li>
          <li>Secured USD 500 IEEE Communications Society Grant and organised ESPire Technical Workshop (Jan 30–31, 2026)</li>
          <li>Managed proposal development, budgeting, compliance reporting, and stakeholder coordination</li>
          <li>Planned and promoted workshops, technical events, and professional development programs</li>
        </ul>
      </div>

      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-header">
          <span class="timeline-role">President — Student Activity Centre (SAC)</span>
          <span class="timeline-period">Apr 2025 – Jun 2026</span>
        </div>
        <p class="timeline-org">SAC, Vignana Bharathi Institute of Technology</p>
        <ul class="timeline-bullets">
          <li>Directed institution-wide student activities, events, and cultural programs</li>
          <li>Managed cross-departmental communication between students, faculty, and organising committees</li>
          <li>Prepared presentations, activity reports, and documentation for institutional records</li>
        </ul>
      </div>

      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-header">
          <span class="timeline-role">RSM Coordinator</span>
          <span class="timeline-period">Jul 2025 – Jun 2026</span>
        </div>
        <p class="timeline-org">IEEE VBIT Student Branch</p>
        <ul class="timeline-bullets">
          <li>Coordinated resource allocation and supported execution of technical events</li>
          <li>Assisted in documentation, communication, and team coordination activities</li>
        </ul>
      </div>

      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-header">
          <span class="timeline-role">Social Media Promotions Scrutinizer</span>
          <span class="timeline-period">Nov 2025 – Mar 2026</span>
        </div>
        <p class="timeline-org">Avishkar 2K26 · IEEE VBIT SB</p>
        <ul class="timeline-bullets">
          <li>Planned digital campaigns and monitored engagement metrics across all social platforms</li>
        </ul>
      </div>

      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-header">
          <span class="timeline-role">Public Relations Co-Lead</span>
          <span class="timeline-period">Jun 2025 – Jun 2026</span>
        </div>
        <p class="timeline-org">Virinchi, VBIT</p>
        <ul class="timeline-bullets">
          <li>Led public relations and stakeholder communication for VBIT's Virinchi chapter</li>
        </ul>
      </div>

      <div class="timeline-year-marker">2024 – 2025</div>

      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-header">
          <span class="timeline-role">Treasurer — IEEE Communications Society</span>
          <span class="timeline-period">May 2024 – Jun 2025</span>
        </div>
        <p class="timeline-org">IEEE Communications Society · VBIT Student Branch</p>
        <ul class="timeline-bullets">
          <li>Managed society finances, event budgets, and expenditure tracking</li>
          <li>Assisted in preparing financial and activity reports for IEEE compliance</li>
        </ul>
      </div>

      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-header">
          <span class="timeline-role">Social Media Promotions Mentor</span>
          <span class="timeline-period">Jan 2025 – Mar 2025</span>
        </div>
        <p class="timeline-org">Avishkar 2K25 · IEEE VBIT SB</p>
        <ul class="timeline-bullets">
          <li>Guided the social media promotions team in content strategy and digital campaign execution</li>
        </ul>
      </div>

      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-header">
          <span class="timeline-role">SMP Lead — Aashay Film Club</span>
          <span class="timeline-period">Jan 2024 – Oct 2024</span>
        </div>
        <p class="timeline-org">Aashay Film Club · VBIT</p>
        <ul class="timeline-bullets">
          <li>Managed all social media promotions and digital outreach for VBIT's film society</li>
        </ul>
      </div>

      <div class="timeline-year-marker">2023 – 2024</div>

      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-header">
          <span class="timeline-role">Social Media Promotions OC</span>
          <span class="timeline-period">Jan 2024 – Apr 2024</span>
        </div>
        <p class="timeline-org">Avishkar 2K24 · IEEE VBIT SB</p>
        <ul class="timeline-bullets">
          <li>Created and managed promotional content for event marketing across digital channels</li>
        </ul>
      </div>

      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-header">
          <span class="timeline-role">Social Media Promotions</span>
          <span class="timeline-period">Feb 2023 – Mar 2025</span>
        </div>
        <p class="timeline-org">Student Activity Centre (SAC) · VBIT</p>
        <ul class="timeline-bullets">
          <li>Managed social media campaigns for student activities and institution-level events</li>
          <li>Created promotional content and coordinated digital outreach initiatives</li>
        </ul>
      </div>

    </div>
  </section>

  <!-- ░░ INTERNSHIP ░░ -->
  <section>
    <p class="section-label">Industry Exposure</p>
    <h2 class="section-title">Internship</h2>
    <div class="intern-card">
      <p class="intern-title">Virtual Intern — Embedded Systems &amp; IoT Research Program</p>
      <p class="intern-org">IEEE Robotics and Automation Society (RAS) · Hyderabad Section</p>
      <p class="intern-period">March 2025 – April 2025 &nbsp;·&nbsp; 5 Weeks</p>
      <p class="intern-desc">Completed a structured five-week virtual internship focused on embedded systems and IoT research. Gained hands-on exposure to system design principles, engineering workflows, and guided technical training under IEEE RAS Hyderabad Section leadership.</p>
    </div>
  </section>

  <!-- ░░ PROJECTS ░░ -->
  <section>
    <p class="section-label">Work</p>
    <h2 class="section-title">Projects</h2>
    <div class="projects-grid">

      <div class="project-card">
        <p class="project-label">AI / Computer Vision</p>
        <p class="project-title">Deep Transfer Learning for Multi-Class Semantic Segmentation of Satellite Images</p>
        <p class="project-desc">Fine-tuned a deep transfer learning-based semantic segmentation model for satellite imagery using pretrained CNNs, enabling accurate pixel-level land cover classification with performance optimisation through evaluation metrics. Won 2nd Prize at Aakar Project Expo.</p>
        <div class="project-tags">
          <span class="tag pub">IEEE Published</span>
          <span class="tag gold">🏆 2nd Prize — Aakar</span>
          <span class="tag">Python</span>
          <span class="tag">CNN</span>
          <span class="tag">Transfer Learning</span>
          <span class="tag teal">Deep Learning</span>
        </div>
        <p class="project-date">Dec 2025 – Jan 2026</p>
      </div>

      <div class="project-card">
        <p class="project-label">ASIC / VLSI</p>
        <p class="project-title">RTL to GDSII Mini Flow</p>
        <p class="project-desc">Implemented a complete RTL-to-GDSII ASIC design flow covering synthesis, placement, clock tree synthesis, routing, and timing analysis using the Cadence tool environment.</p>
        <div class="project-tags">
          <span class="tag">Verilog</span>
          <span class="tag teal">Cadence Innovus</span>
          <span class="tag">ASIC</span>
          <span class="tag">STA</span>
          <span class="tag">Physical Design</span>
        </div>
        <p class="project-date">Sep 2025 – Dec 2025</p>
      </div>

      <div class="project-card">
        <p class="project-label">Digital Design</p>
        <p class="project-title">16-bit ALU Using Verilog HDL</p>
        <p class="project-desc">Designed and simulated a 16-bit Arithmetic Logic Unit supporting arithmetic and logical operations. Developed RTL modules and verified functionality through testbench simulation using Xilinx Vivado.</p>
        <div class="project-tags">
          <span class="tag">Verilog HDL</span>
          <span class="tag teal">Xilinx Vivado</span>
          <span class="tag">RTL Design</span>
          <span class="tag">Testbench</span>
        </div>
        <p class="project-date">Jul 2025 – Sep 2025</p>
      </div>

      <div class="project-card">
        <p class="project-label">Embedded Systems</p>
        <p class="project-title">Smart Attendance System — RFID &amp; Fingerprint Dual Authentication</p>
        <p class="project-desc">Raspberry Pi-based system integrating RFID and biometric fingerprint authentication with modular Python control logic, SQLite offline storage, and automated Gmail API notifications. Achieved 98.5% authentication accuracy. Presented at IEEE International Conference.</p>
        <div class="project-tags">
          <span class="tag pub">IEEE Published</span>
          <span class="tag">Raspberry Pi</span>
          <span class="tag">Python</span>
          <span class="tag teal">SQLite</span>
          <span class="tag">Gmail API</span>
          <span class="tag">RFID</span>
        </div>
        <p class="project-date">Jan 2025 – Jun 2025</p>
      </div>

      <div class="project-card">
        <p class="project-label">Embedded Systems</p>
        <p class="project-title">Earthquake Detector Using Arduino UNO</p>
        <p class="project-desc">Low-cost real-time seismic detection system using Arduino Uno and ADXL335 accelerometer. Performed sensor calibration and threshold tuning to distinguish seismic activity from noise, with live alerts on a 16×2 LCD.</p>
        <div class="project-tags">
          <span class="tag">Arduino Uno</span>
          <span class="tag teal">ADXL335</span>
          <span class="tag">Sensor Fusion</span>
          <span class="tag">Embedded C</span>
        </div>
        <p class="project-date">Jul 2024 – Dec 2024</p>
      </div>

    </div>
  </section>

  <!-- ░░ PUBLICATION ░░ -->
  <section>
    <p class="section-label">Research</p>
    <h2 class="section-title">International Publication</h2>
    <div class="pub-card">
      <p class="pub-title">Smart Attendance Framework Using RFID and Fingerprint-Based Dual Authentication with Real-Time Email Notifications</p>
      <p class="pub-venue">2nd International Conference on Recent Trends in Electrical, Electronics and Computing Technologies</p>
      <p class="pub-details">IEEE · Vaagdevi Engineering College, Telangana · October 2025</p>
      <ul class="pub-bullets">
        <li>Designed a Raspberry Pi-based embedded authentication system integrating RFID and biometric fingerprint verification</li>
        <li>Implemented Python control logic, SQLite database, and Gmail API notifications achieving 98.5% authentication accuracy</li>
        <li>Presented system architecture and performance evaluation at an IEEE-affiliated international conference</li>
      </ul>
    </div>
  </section>

  <!-- ░░ SKILLS ░░ -->
  <section>
    <p class="section-label">Capabilities</p>
    <h2 class="section-title">Technical &amp; Professional Skills</h2>
    <div class="skills-section">

      <div class="skill-group">
        <p class="skill-group-title"><span></span>VLSI &amp; Digital Design</p>
        <div class="skill-pills">
          <span class="skill-pill">Verilog HDL</span>
          <span class="skill-pill">RTL Design</span>
          <span class="skill-pill">FPGA Design</span>
          <span class="skill-pill">ASIC Design Flow</span>
          <span class="skill-pill">Timing Analysis</span>
          <span class="skill-pill">Physical Design</span>
          <span class="skill-pill">CMOS Basics</span>
          <span class="skill-pill">STA Fundamentals</span>
          <span class="skill-pill">Digital Electronics</span>
        </div>
      </div>

      <div class="skill-group">
        <p class="skill-group-title"><span></span>EDA Tools</p>
        <div class="skill-pills">
          <span class="skill-pill">Cadence Virtuoso</span>
          <span class="skill-pill">Cadence Innovus</span>
          <span class="skill-pill">Xilinx Vivado</span>
          <span class="skill-pill">MATLAB</span>
          <span class="skill-pill">Scilab</span>
          <span class="skill-pill">Arduino IDE</span>
        </div>
      </div>

      <div class="skill-group">
        <p class="skill-group-title"><span></span>Programming</p>
        <div class="skill-pills">
          <span class="skill-pill">Python</span>
          <span class="skill-pill">C</span>
          <span class="skill-pill">Verilog</span>
          <span class="skill-pill">TCL Scripting</span>
          <span class="skill-pill">Shell Scripting</span>
          <span class="skill-pill">Java (Full Stack)</span>
        </div>
      </div>

      <div class="skill-group">
        <p class="skill-group-title"><span></span>Hardware Platforms</p>
        <div class="skill-pills">
          <span class="skill-pill">Raspberry Pi</span>
          <span class="skill-pill">Arduino Uno</span>
          <span class="skill-pill">RFID Modules</span>
          <span class="skill-pill">Biometric Sensors</span>
          <span class="skill-pill">Accelerometers</span>
        </div>
      </div>

      <div class="skill-group">
        <p class="skill-group-title"><span></span>Communications &amp; Media</p>
        <div class="skill-pills">
          <span class="skill-pill">Social Media Management</span>
          <span class="skill-pill">Content Strategy</span>
          <span class="skill-pill">Copywriting</span>
          <span class="skill-pill">Digital Marketing</span>
          <span class="skill-pill">Public Relations</span>
          <span class="skill-pill">Community Engagement</span>
          <span class="skill-pill">Event Promotion</span>
        </div>
      </div>

      <div class="skill-group">
        <p class="skill-group-title"><span></span>Management &amp; Administration</p>
        <div class="skill-pills">
          <span class="skill-pill">Team Leadership</span>
          <span class="skill-pill">Event Coordination</span>
          <span class="skill-pill">Budget Management</span>
          <span class="skill-pill">Technical Documentation</span>
          <span class="skill-pill">Proposal Writing</span>
          <span class="skill-pill">MS Office Suite</span>
          <span class="skill-pill">Stakeholder Communication</span>
        </div>
      </div>

    </div>
  </section>

  <!-- ░░ DOMAINS ░░ -->
  <section>
    <p class="section-label">Expertise Areas</p>
    <h2 class="section-title">Domains</h2>
    <div class="domains-grid">
      <div class="domain-card">
        <span class="domain-icon">🔬</span>
        <p class="domain-name">Embedded Systems</p>
        <p class="domain-sub">Raspberry Pi · Arduino · IoT · Sensor Integration</p>
      </div>
      <div class="domain-card">
        <span class="domain-icon">⚡</span>
        <p class="domain-name">VLSI &amp; Digital Design</p>
        <p class="domain-sub">FPGA · ASIC · RTL-to-GDSII · Cadence · Vivado</p>
      </div>
      <div class="domain-card">
        <span class="domain-icon">🤖</span>
        <p class="domain-name">AI &amp; Computer Vision</p>
        <p class="domain-sub">Deep Learning · CNNs · Transfer Learning · Segmentation</p>
      </div>
      <div class="domain-card">
        <span class="domain-icon">📢</span>
        <p class="domain-name">Social Media &amp; Promotions</p>
        <p class="domain-sub">Content Strategy · Digital Campaigns · Community Building</p>
      </div>
      <div class="domain-card">
        <span class="domain-icon">🏛</span>
        <p class="domain-name">IEEE Leadership</p>
        <p class="domain-sub">Student Governance · Grant Management · Event Administration</p>
      </div>
      <div class="domain-card">
        <span class="domain-icon">📋</span>
        <p class="domain-name">Technical Administration</p>
        <p class="domain-sub">Project Coordination · Documentation · Report Writing</p>
      </div>
    </div>
  </section>

  <!-- ░░ EDUCATION ░░ -->
  <section>
    <p class="section-label">Academic</p>
    <h2 class="section-title">Education</h2>

    <div class="edu-card">
      <span class="edu-year">2022 – 2026</span>
      <div class="edu-info">
        <p class="edu-degree">B.Tech — Electronics &amp; Communication Engineering</p>
        <p class="edu-school">Vignana Bharathi Institute of Technology, Hyderabad</p>
        <p class="edu-note">Relevant Coursework: Digital Electronics · VLSI Design · CMOS Technology · FPGA Design · Embedded Systems · Signals &amp; Systems · Microprocessors &amp; Microcontrollers</p>
      </div>
    </div>

    <div class="edu-card">
      <span class="edu-year">2020 – 2022</span>
      <div class="edu-info">
        <p class="edu-degree">Intermediate — MPC (Mathematics, Physics, Chemistry)</p>
        <p class="edu-school">Sri Chaitanya Junior Kalasala</p>
        <p class="edu-note">Telangana State Board of Intermediate Education</p>
      </div>
    </div>

    <div class="edu-card">
      <span class="edu-year">Until 2020</span>
      <div class="edu-info">
        <p class="edu-degree">Secondary Schooling</p>
        <p class="edu-school">English Union School, India</p>
        <p class="edu-note">Board of Secondary Education</p>
      </div>
    </div>

  </section>

  <!-- ░░ CERTIFICATES ░░ -->
  <section>
    <p class="section-label">Credentials</p>
    <h2 class="section-title">Certificates</h2>
    <div class="cert-grid">

      <div class="cert-card">
        <div class="cert-icon pro">🎓</div>
        <div>
          <p class="cert-title">System Administration Micro-Certification</p>
          <p class="cert-issuer">ServiceNow · Professional</p>
        </div>
      </div>

      <div class="cert-card">
        <div class="cert-icon pro">💻</div>
        <div>
          <p class="cert-title">Java Full Stack — Digital Skills Readiness Program</p>
          <p class="cert-issuer">TalentNext in collaboration with Wipro Limited</p>
        </div>
      </div>

      <div class="cert-card">
        <div class="cert-icon pro">🐍</div>
        <div>
          <p class="cert-title">The Complete Python Course</p>
          <p class="cert-issuer">Professional Certification</p>
        </div>
      </div>

      <div class="cert-card">
        <div class="cert-icon vol">🌐</div>
        <div>
          <p class="cert-title">Leveraging U.S.–India TRUST: Industry-Academia Partnerships in AI &amp; Cybersecurity</p>
          <p class="cert-issuer">World Trade Center Shamshad &amp; U.S. Consulate General, Hyderabad · 29 Jan 2026</p>
        </div>
      </div>

      <div class="cert-card">
        <div class="cert-icon vol">📚</div>
        <div>
          <p class="cert-title">Kaushal Mahotsav — Skill Development &amp; Career Counselling Program</p>
          <p class="cert-issuer">NSDC · 3–4 June 2023</p>
        </div>
      </div>

      <div class="cert-card">
        <div class="cert-icon vol">🤝</div>
        <div>
          <p class="cert-title">IEEE Volunteer &amp; Leadership Certificates</p>
          <p class="cert-issuer">IEEE VBIT SB · ComSoc · Avishkar 2K24, 2K25, 2K26 · SAC · RAS Internship</p>
        </div>
      </div>

    </div>
  </section>

  <!-- ░░ IEEE MEMBERSHIP ░░ -->
  <section>
    <p class="section-label">Affiliations</p>
    <h2 class="section-title">IEEE Memberships</h2>
    <div class="cert-grid">
      <div class="cert-card">
        <div class="cert-icon vol">⚡</div>
        <div>
          <p class="cert-title">IEEE Student Member</p>
          <p class="cert-issuer">Institute of Electrical and Electronics Engineers · Nov 2024 – Present</p>
        </div>
      </div>
      <div class="cert-card">
        <div class="cert-icon vol">💻</div>
        <div>
          <p class="cert-title">IEEE Computer Society — Student Member</p>
          <p class="cert-issuer">IEEE CS · Nov 2024 – Present</p>
        </div>
      </div>
      <div class="cert-card">
        <div class="cert-icon vol">📡</div>
        <div>
          <p class="cert-title">IEEE Communications Society — Student Member</p>
          <p class="cert-issuer">IEEE ComSoc · Nov 2024 – Present</p>
        </div>
      </div>
      <div class="cert-card">
        <div class="cert-icon vol">♀️</div>
        <div>
          <p class="cert-title">IEEE Women in Engineering — Student Member</p>
          <p class="cert-issuer">IEEE WIE · Nov 2024 – Present</p>
        </div>
      </div>
    </div>
  </section>
</div>

<!-- ░░ FOOTER ░░ -->
<footer class="footer">
  <p class="footer-name">Nara Pranay</p>
  <p class="footer-sub">ECE Graduate · Hyderabad, Telangana, India</p>
  <div class="footer-links">
    <a class="footer-link" href="mailto:n.pranay2005@gmail.com">✉ n.pranay2005@gmail.com</a>
    <a class="footer-link" href="https://www.linkedin.com/in/nara-pranay" target="_blank" rel="noopener">LinkedIn</a>
    <a class="footer-link" href="https://github.com/nara-pranay" target="_blank" rel="noopener">GitHub</a>
  </div>
  <p class="footer-copy">© 2026 Nara Pranay · Built with purpose.</p>
</footer>

</body>
</html>
