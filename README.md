<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kingsley Bamidele Owadara — AI Ethicist & Policy Advocate</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400;1,700&family=DM+Sans:wght@300;400;500&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #0D0D0D;
    --paper: #F5F0E8;
    --accent: #C8502A;
    --accent2: #1A3A5C;
    --gold: #B8982A;
    --muted: #7A7060;
    --light-rule: #DDD5C4;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--paper);
    color: var(--ink);
    font-family: 'DM Sans', sans-serif;
    font-weight: 300;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ── GRAIN OVERLAY ── */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 9999;
    opacity: 0.6;
  }

  /* ── NAV ── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.2rem 4rem;
    background: rgba(245, 240, 232, 0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--light-rule);
  }

  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.05rem;
    font-weight: 700;
    color: var(--ink);
    letter-spacing: 0.02em;
    text-decoration: none;
  }

  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    text-transform: uppercase;
    letter-spacing: 0.14em;
    color: var(--muted);
    text-decoration: none;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--accent); }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding-top: 80px;
  }

  .hero-left {
    padding: 7rem 4rem 4rem 4rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    border-right: 1px solid var(--light-rule);
    position: relative;
  }

  .hero-eyebrow {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 1.5rem;
    opacity: 0;
    animation: fadeUp 0.8s ease forwards 0.2s;
  }

  .hero-name {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3rem, 5vw, 5.5rem);
    font-weight: 900;
    line-height: 1.0;
    color: var(--ink);
    margin-bottom: 0.4rem;
    opacity: 0;
    animation: fadeUp 0.8s ease forwards 0.4s;
  }

  .hero-name span {
    color: var(--accent);
    font-style: italic;
  }

  .hero-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.1rem, 2vw, 1.4rem);
    font-weight: 400;
    font-style: italic;
    color: var(--muted);
    margin-bottom: 2.5rem;
    opacity: 0;
    animation: fadeUp 0.8s ease forwards 0.6s;
  }

  .hero-desc {
    font-size: 1rem;
    color: var(--ink);
    max-width: 480px;
    line-height: 1.8;
    margin-bottom: 3rem;
    opacity: 0;
    animation: fadeUp 0.8s ease forwards 0.8s;
  }

  .hero-ctas {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
    opacity: 0;
    animation: fadeUp 0.8s ease forwards 1s;
  }

  .btn-primary {
    background: var(--accent);
    color: #fff;
    padding: 0.85rem 2rem;
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    text-decoration: none;
    border: none;
    cursor: pointer;
    transition: background 0.2s, transform 0.2s;
  }
  .btn-primary:hover { background: var(--ink); transform: translateY(-2px); }

  .btn-outline {
    border: 1.5px solid var(--ink);
    color: var(--ink);
    padding: 0.85rem 2rem;
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    text-decoration: none;
    transition: background 0.2s, color 0.2s, transform 0.2s;
  }
  .btn-outline:hover { background: var(--ink); color: var(--paper); transform: translateY(-2px); }

  .hero-right {
    padding: 7rem 4rem 4rem 4rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 2.5rem;
  }

  .stat-block {
    opacity: 0;
    animation: fadeUp 0.8s ease forwards;
  }
  .stat-block:nth-child(1) { animation-delay: 0.5s; }
  .stat-block:nth-child(2) { animation-delay: 0.7s; }
  .stat-block:nth-child(3) { animation-delay: 0.9s; }

  .stat-number {
    font-family: 'Playfair Display', serif;
    font-size: 3.5rem;
    font-weight: 900;
    color: var(--accent);
    line-height: 1;
  }

  .stat-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--muted);
    margin-top: 0.3rem;
  }

  .stat-rule { height: 1px; background: var(--light-rule); }

  /* ── MARQUEE ── */
  .marquee-wrap {
    border-top: 1px solid var(--light-rule);
    border-bottom: 1px solid var(--light-rule);
    overflow: hidden;
    padding: 0.9rem 0;
    background: var(--ink);
  }

  .marquee-inner {
    display: flex;
    gap: 3rem;
    animation: marquee 28s linear infinite;
    white-space: nowrap;
  }

  .marquee-item {
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--paper);
    opacity: 0.7;
    flex-shrink: 0;
  }

  .marquee-dot {
    color: var(--accent);
    opacity: 1;
  }

  @keyframes marquee {
    from { transform: translateX(0); }
    to { transform: translateX(-50%); }
  }

  /* ── SECTIONS ── */
  section { padding: 6rem 4rem; }

  .section-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 0.8rem;
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 3.5vw, 3rem);
    font-weight: 700;
    color: var(--ink);
    line-height: 1.2;
    margin-bottom: 3rem;
  }

  /* ── ABOUT ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5rem;
    align-items: start;
  }

  .about-text p {
    font-size: 1.05rem;
    line-height: 1.9;
    color: #333;
    margin-bottom: 1.5rem;
  }

  .about-text p strong { color: var(--accent); font-weight: 500; }

  .about-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.6rem;
    margin-top: 2rem;
  }

  .tag {
    border: 1px solid var(--light-rule);
    padding: 0.3rem 0.9rem;
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--muted);
    transition: all 0.2s;
  }
  .tag:hover { border-color: var(--accent); color: var(--accent); }

  .about-credentials { display: flex; flex-direction: column; gap: 1.5rem; }

  .credential {
    padding: 1.5rem;
    border-left: 3px solid var(--accent);
    background: rgba(200, 80, 42, 0.04);
  }

  .credential-org {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 0.3rem;
  }

  .credential-role {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--ink);
  }

  .credential-date {
    font-size: 0.82rem;
    color: var(--muted);
    margin-top: 0.2rem;
  }

  /* ── WORK SECTION (dark) ── */
  .work-section {
    background: var(--ink);
    color: var(--paper);
    padding: 6rem 4rem;
  }

  .work-section .section-label { color: var(--gold); }
  .work-section .section-title { color: var(--paper); }

  .work-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2px;
  }

  .work-card {
    padding: 2.5rem 2rem;
    border: 1px solid rgba(245,240,232,0.1);
    position: relative;
    overflow: hidden;
    transition: background 0.3s;
    cursor: default;
  }

  .work-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: var(--accent);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.4s ease;
  }

  .work-card:hover::before { transform: scaleX(1); }
  .work-card:hover { background: rgba(200,80,42,0.08); }

  .work-num {
    font-family: 'Playfair Display', serif;
    font-size: 3rem;
    font-weight: 900;
    color: rgba(245,240,232,0.08);
    position: absolute;
    top: 1rem; right: 1.5rem;
    line-height: 1;
  }


  .work-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem;
    font-weight: 700;
    color: var(--paper);
    margin-bottom: 0.8rem;
  }

  .work-desc {
    font-size: 0.88rem;
    line-height: 1.7;
    color: rgba(245,240,232,0.6);
  }

  /* ── IMPACT ── */
  .impact-section { background: var(--paper); }

  .impact-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1px;
    background: var(--light-rule);
    border: 1px solid var(--light-rule);
    margin-bottom: 5rem;
  }

  .impact-cell {
    background: var(--paper);
    padding: 2.5rem 2rem;
    text-align: center;
  }

  .impact-num {
    font-family: 'Playfair Display', serif;
    font-size: 3rem;
    font-weight: 900;
    color: var(--accent2);
    line-height: 1;
  }

  .impact-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--muted);
    margin-top: 0.5rem;
  }

  /* ── PUBLICATIONS ── */
  .pub-list { display: flex; flex-direction: column; gap: 1px; background: var(--light-rule); }

  .pub-item {
    background: var(--paper);
    padding: 1.8rem 2rem;
    display: grid;
    grid-template-columns: auto 1fr auto;
    gap: 2rem;
    align-items: start;
    transition: background 0.2s;
  }
  .pub-item:hover { background: #EDE8DF; }

  .pub-year {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    color: var(--accent);
    padding-top: 0.2rem;
    min-width: 36px;
  }

  .pub-title {
    font-family: 'Playfair Display', serif;
    font-size: 1rem;
    font-weight: 700;
    color: var(--ink);
    margin-bottom: 0.3rem;
  }

  .pub-venue {
    font-size: 0.82rem;
    color: var(--muted);
  }

  .pub-arrow {
    color: var(--accent);
    font-size: 1.2rem;
    padding-top: 0.1rem;
    opacity: 0;
    transition: opacity 0.2s, transform 0.2s;
  }
  .pub-item:hover .pub-arrow { opacity: 1; transform: translateX(4px); }

  /* ── SPEAKING ── */
  .speaking-section { background: var(--accent2); color: var(--paper); }
  .speaking-section .section-label { color: var(--gold); }
  .speaking-section .section-title { color: var(--paper); }

  .speaking-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1.5rem;
  }

  .speaking-card {
    padding: 2rem;
    border: 1px solid rgba(245,240,232,0.12);
    transition: border-color 0.2s, background 0.2s;
  }
  .speaking-card:hover {
    border-color: var(--gold);
    background: rgba(184,152,42,0.06);
  }

  .speaking-year {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.15em;
    color: var(--gold);
    margin-bottom: 0.5rem;
  }

  .speaking-event {
    font-family: 'Playfair Display', serif;
    font-size: 1rem;
    font-weight: 700;
    color: var(--paper);
    margin-bottom: 0.3rem;
    line-height: 1.3;
  }

  .speaking-venue {
    font-size: 0.82rem;
    color: rgba(245,240,232,0.55);
  }

  /* ── CONTACT ── */
  .contact-section {
    background: var(--paper);
    text-align: center;
    border-top: 1px solid var(--light-rule);
  }

  .contact-section .section-title { margin-bottom: 1rem; }

  .contact-desc {
    font-size: 1rem;
    color: var(--muted);
    max-width: 500px;
    margin: 0 auto 2.5rem;
    line-height: 1.8;
  }

  .contact-links {
    display: flex;
    justify-content: center;
    gap: 1.5rem;
    flex-wrap: wrap;
    margin-top: 3rem;
  }

  .contact-link {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--muted);
    text-decoration: none;
    border-bottom: 1px solid var(--light-rule);
    padding-bottom: 2px;
    transition: color 0.2s, border-color 0.2s;
  }
  .contact-link:hover { color: var(--accent); border-color: var(--accent); }

  /* ── FOOTER ── */
  footer {
    padding: 2rem 4rem;
    border-top: 1px solid var(--light-rule);
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: var(--ink);
  }

  footer p {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.1em;
    color: rgba(245,240,232,0.35);
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .reveal {
    opacity: 0;
    transform: translateY(24px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.visible { opacity: 1; transform: translateY(0); }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    section { padding: 4rem 1.5rem; }
    .hero { grid-template-columns: 1fr; }
    .hero-left { padding: 7rem 1.5rem 2rem; border-right: none; border-bottom: 1px solid var(--light-rule); }
    .hero-right { padding: 2rem 1.5rem 4rem; flex-direction: row; flex-wrap: wrap; gap: 1.5rem; }
    .stat-rule { display: none; }
    .about-grid { grid-template-columns: 1fr; gap: 2.5rem; }
    .work-grid { grid-template-columns: 1fr; }
    .impact-grid { grid-template-columns: 1fr 1fr; }
    .speaking-grid { grid-template-columns: 1fr; }
    .work-section, .speaking-section { padding: 4rem 1.5rem; }
    #media { padding: 4rem 1.5rem !important; }
    #media > div:last-child { grid-template-columns: 1fr !important; }
    footer { flex-direction: column; gap: 0.5rem; text-align: center; padding: 1.5rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">K. B. Owadara</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#work">Work</a></li>
    <li><a href="#impact">Impact</a></li>
    <li><a href="#publications">Writing</a></li>
    <li><a href="#speaking">Speaking</a></li>
    <li><a href="#media">Media</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" id="top">
  <div class="hero-left">
    <p class="hero-eyebrow">Lagos, Nigeria · AI Ethics · Policy · Law</p>
    <h1 class="hero-name">Kingsley<br><span>Owadara</span></h1>
    <p class="hero-title">AI Ethicist, Lawyer & Policy Architect</p>
    <p class="hero-desc">
      Founder of the Pan-Africa Center for AI Ethics. I work at the intersection of
      artificial intelligence, data governance, and human rights — building frameworks
      that ensure technology serves people, not the other way around.
    </p>
    <div class="hero-ctas">
      <a href="#work" class="btn-primary">Explore My Work</a>
      <a href="mailto:k.owadara@pacfaie.org" class="btn-outline">Get in Touch</a>
    </div>
  </div>

  <div class="hero-right">
    <div class="stat-block">
      <div class="stat-number">1,500+</div>
      <div class="stat-label">Practitioners trained across Africa</div>
    </div>
    <div class="stat-rule"></div>
    <div class="stat-block">
      <div class="stat-number">34</div>
      <div class="stat-label">Countries reached through AI Ethics Summer School</div>
    </div>
    <div class="stat-rule"></div>
    <div class="stat-block">
      <div class="stat-number">20+</div>
      <div class="stat-label">International conferences & keynotes</div>
    </div>
  </div>
</section>

<!-- MARQUEE -->
<div class="marquee-wrap">
  <div class="marquee-inner">
    <span class="marquee-item">AI Ethics</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">Data Governance</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">Pan-Africa Center for AI Ethics</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">Nigeria National AI Policy</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">NIST Generative AI</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">UNESCO Gender & Privacy</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">UN Global Digital Compact</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">Indigenous Data Sovereignty</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">Algorithmic Transparency</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">Digital Rights</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">AI Ethics</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">Data Governance</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">Pan-Africa Center for AI Ethics</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">Nigeria National AI Policy</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">NIST Generative AI</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">UNESCO Gender & Privacy</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">UN Global Digital Compact</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">Indigenous Data Sovereignty</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">Algorithmic Transparency</span><span class="marquee-dot"> · </span>
    <span class="marquee-item">Digital Rights</span><span class="marquee-dot"> · </span>
  </div>
</div>

<!-- ABOUT -->
<section id="about" style="padding: 6rem 4rem; background: var(--paper);">
  <div class="reveal">
    <p class="section-label">About</p>
    <h2 class="section-title">Bridging Technology,<br>Ethics & Policy</h2>
  </div>
  <div class="about-grid">
    <div class="about-text reveal">
      <p>
        I am a <strong>lawyer, AI ethicist, and policy advocate</strong> with over five years of 
        experience shaping how artificial intelligence is governed — particularly across 
        Africa and the Global South. My work sits at the crossroads of law, technology, 
        and social justice.
      </p>
      <p>
        As the founder of the Pan-Africa Center for AI Ethics, I built one of the continent's 
        most active AI ethics communities from the ground up — reaching researchers, 
        policymakers, and practitioners across 34 countries through training, research, 
        and advocacy.
      </p>
      <p>
        I led the AI Ethics cluster of the Volunteer Expert Group in drafting <strong>Nigeria's first National AI Policy</strong>, contributed to the
        NIST Generative AI Public Work Group, and have engaged with the UN, UNESCO,
        and the African Union on AI governance frameworks. My research focuses on
        data justice, algorithmic transparency, and what inclusive AI development
        truly looks like in practice.
      </p>
      <div class="about-tags">
        <span class="tag">AI Ethics</span>
        <span class="tag">Data Protection Law</span>
        <span class="tag">Policy Advocacy</span>
        <span class="tag">Digital Rights</span>
        <span class="tag">Algorithm Fairness</span>
        <span class="tag">Capacity Building</span>
        <span class="tag">Global South AI</span>
        <span class="tag">Internet Governance</span>
      </div>
    </div>
    <div class="about-credentials reveal">
      <div class="credential">
        <div class="credential-org">Pan-Africa Center for AI Ethics</div>
        <div class="credential-role">Founder & AI Ethicist</div>
        <div class="credential-date">January 2024 – Present</div>
      </div>
    </div>
  </div>
</section>

<!-- WORK -->
<section class="work-section" id="work">
  <div class="reveal">
    <p class="section-label">What I Do</p>
    <h2 class="section-title">Areas of Focus</h2>
  </div>
  <div class="work-grid">
    <div class="work-card reveal">
      <div class="work-num">01</div>
      <div class="work-title">AI Policy & Governance</div>
      <div class="work-desc">Designing and advocating for regulatory frameworks that govern AI development and deployment responsibly. From national AI strategies to international standards bodies.</div>
    </div>
    <div class="work-card reveal">
      <div class="work-num">02</div>
      <div class="work-title">Data Protection & Privacy</div>
      <div class="work-desc">Operationalising data protection law in real organisational contexts. Conducting DPIAs, advising on compliance, and advocating for data rights as human rights.</div>
    </div>
    <div class="work-card reveal">
      <div class="work-num">03</div>
      <div class="work-title">African AI Ethics</div>
      <div class="work-desc">Centring African perspectives in global AI conversations. Building frameworks that reflect the continent's cultural, legal, and socioeconomic realities — not imported assumptions.</div>
    </div>
    <div class="work-card reveal">
      <div class="work-num">04</div>
      <div class="work-title">Algorithmic Fairness</div>
      <div class="work-desc">Evaluating AI systems for bias, discrimination, and opacity. Translating technical AI safety concepts into actionable governance and audit frameworks.</div>
    </div>
    <div class="work-card reveal">
      <div class="work-num">05</div>
      <div class="work-title">Capacity Development</div>
      <div class="work-desc">Training the next generation of African AI ethics practitioners through the Annual AI Ethics Summer School and mentoring programmes across the continent and beyond.</div>
    </div>
    <div class="work-card reveal">
      <div class="work-num">06</div>
      <div class="work-title">Research & Publishing</div>
      <div class="work-desc">Producing peer-reviewed and policy research on recommender systems, data sovereignty, digital commons, and responsible AI — from ACM proceedings to UN submissions.</div>
    </div>
  </div>
</section>

<!-- IMPACT -->
<section class="impact-section" id="impact" style="padding: 6rem 4rem;">
  <div class="reveal">
    <p class="section-label">Impact</p>
    <h2 class="section-title">By the Numbers</h2>
  </div>
  <div class="impact-grid reveal">
    <div class="impact-cell">
      <div class="impact-num">1,500+</div>
      <div class="impact-label">Summer School<br>Participants</div>
    </div>
    <div class="impact-cell">
      <div class="impact-num">34</div>
      <div class="impact-label">Countries<br>Represented</div>
    </div>
    <div class="impact-cell">
      <div class="impact-num">5+</div>
      <div class="impact-label">International<br>Frameworks</div>
    </div>
    <div class="impact-cell">
      <div class="impact-num">20+</div>
      <div class="impact-label">Conference<br>Presentations</div>
    </div>
  </div>

  <div style="display:grid; grid-template-columns: 1fr 1fr; gap: 3rem;" class="reveal">
    <div>
      <p class="section-label" style="margin-bottom:1rem;">International Contributions</p>
      <ul style="list-style:none; display:flex; flex-direction:column; gap:0.8rem;">
        <li style="padding:1rem 1.2rem; border-left:3px solid var(--accent2); background:rgba(26,58,92,0.04); font-size:0.9rem;">🇺🇸 NIST Generative AI Public Work Group — US Dept. of Commerce</li>
        <li style="padding:1rem 1.2rem; border-left:3px solid var(--accent2); background:rgba(26,58,92,0.04); font-size:0.9rem;">🇺🇳 UN Global Digital Compact — Input Submission</li>
        <li style="padding:1rem 1.2rem; border-left:3px solid var(--accent2); background:rgba(26,58,92,0.04); font-size:0.9rem;">🌐 UNESCO · AI4D — Gender & Privacy Framework</li>
        <li style="padding:1rem 1.2rem; border-left:3px solid var(--accent2); background:rgba(26,58,92,0.04); font-size:0.9rem;">🌐 Google-funded AI & Pedagogy Framework</li>
        <li style="padding:1rem 1.2rem; border-left:3px solid var(--accent2); background:rgba(26,58,92,0.04); font-size:0.9rem;">🌍 Global AI Index Contributor</li>
      </ul>
    </div>
    <div>
      <p class="section-label" style="margin-bottom:1rem;">Fellowships</p>
      <ul style="list-style:none; display:flex; flex-direction:column; gap:0.8rem;">
        <li style="padding:1rem 1.2rem; border-left:3px solid var(--gold); background:rgba(184,152,42,0.05); font-size:0.9rem;">🛡️ AI Safety Instructor — European Network for AI Safety (ENAIS)</li>
        <li style="padding:1rem 1.2rem; border-left:3px solid var(--gold); background:rgba(184,152,42,0.05); font-size:0.9rem;">🤖 TechGov AI Fellowship — Nigeria AI Strategy Review</li>
        <li style="padding:1rem 1.2rem; border-left:3px solid var(--gold); background:rgba(184,152,42,0.05); font-size:0.9rem;">🌐 Fellow — Emerging Technology for Emerging Markets (E4E)</li>
        <li style="padding:1rem 1.2rem; border-left:3px solid var(--gold); background:rgba(184,152,42,0.05); font-size:0.9rem;">⚖️ Tech Policy Fellow — Lawyers Hub, Kenya</li>
        <li style="padding:1rem 1.2rem; border-left:3px solid var(--gold); background:rgba(184,152,42,0.05); font-size:0.9rem;">🌍 Fellow — West Africa Internet Governance Forum</li>
      </ul>
    </div>
  </div>
</section>

<!-- PUBLICATIONS -->
<section id="publications" style="padding: 6rem 4rem; background: #EDE8DF;">
  <div class="reveal">
    <p class="section-label">Writing & Research</p>
    <h2 class="section-title">Selected Publications</h2>
  </div>
  <div class="pub-list reveal">
    <div class="pub-item" onclick="window.open('https://github.com/Delekings/recsys-geographic-bias','_blank')" style="cursor:pointer;">
      <div class="pub-year">2026</div>
      <div>
        <div class="pub-title">Beyond Availability: Auditing Global South Cultural Visibility in Recommender Systems</div>
        <div class="pub-venue">NeurIPS 2026 "AI and the Self" Workshop · Paris, France — Introduces the Cultural Erasure Index (CEI)</div>
      </div>
      <div class="pub-arrow">→</div>
    </div>
    <div class="pub-item">
      <div class="pub-year">2026</div>
      <div>
        <div class="pub-title">Auditing from the Outside: Measuring the Language Blind Spots in Frontier AI Safety Evaluation</div>
        <div class="pub-venue">Poster · ERA Technical AI Governance Forum · London, November 2026</div>
      </div>
      <div class="pub-arrow">→</div>
    </div>
    <div class="pub-item">
      <div class="pub-year">2027</div>
      <div>
        <div class="pub-title">Coercive Transparency: How WhatsApp's Design Affordances Produce Asymmetric Accountability in Infrastructure-Dependent Markets</div>
        <div class="pub-venue">Targeting ACM FAccT 2027 · Porto, Portugal</div>
      </div>
      <div class="pub-arrow">→</div>
    </div>
    <div class="pub-item" onclick="window.open('https://arxiv.org/abs/2509.20099','_blank')" style="cursor:pointer;">
      <div class="pub-year">2025</div>
      <div>
        <div class="pub-title">Cascade! Human in the Loop Shortcomings Can Increase the Risk of Failures in Recommender Systems</div>
        <div class="pub-venue">arXiv:2509.20099 · Workshop on Socially Responsible Recommender Systems (FAccTRec@RecSys) · ACM</div>
      </div>
      <div class="pub-arrow">→</div>
    </div>
    <div class="pub-item" onclick="window.open('https://pacfaie.org/wp-content/uploads/2025/06/AI-Ethics-Report-2024-3-3.pdf','_blank')" style="cursor:pointer;">
      <div class="pub-year">2024</div>
      <div>
        <div class="pub-title">PACFAIE AI Ethics Report 2024</div>
        <div class="pub-venue">Editor-in-Chief · Pan-Africa Center for AI Ethics Annual Report</div>
      </div>
      <div class="pub-arrow">→</div>
    </div>
    <div class="pub-item">
      <div class="pub-year">2023</div>
      <div>
        <div class="pub-title">Chapter on Digital Commons for Public Good</div>
        <div class="pub-venue">United Nations Global Digital Compact Input Submission (with Marco G. & Odetta B.)</div>
      </div>
      <div class="pub-arrow">→</div>
    </div>
    <div class="pub-item">
      <div class="pub-year">2023</div>
      <div>
        <div class="pub-title">The Dance of Wheels: Ride-Hailing Services and the Quest for Regulatory Balance in Nigeria</div>
        <div class="pub-venue">Co-authored with A. Adegoroye, D. Tsebee et al.</div>
      </div>
      <div class="pub-arrow">→</div>
    </div>
    <div class="pub-item">
      <div class="pub-year">2023</div>
      <div>
        <div class="pub-title">Chapter on Data Privacy</div>
        <div class="pub-venue">Report on Coded Rights · Mankind and Artificial Intelligence Research Group, p. 26</div>
      </div>
      <div class="pub-arrow">→</div>
    </div>
    <div class="pub-item">
      <div class="pub-year">2023</div>
      <div>
        <div class="pub-title">Understanding the Metaverse</div>
        <div class="pub-venue">ResearchGate · Independent Publication</div>
      </div>
      <div class="pub-arrow">→</div>
    </div>
  </div>
</section>

<!-- SPEAKING -->
<section class="speaking-section" id="speaking">
  <div class="reveal">
    <p class="section-label">Speaking</p>
    <h2 class="section-title">Selected Talks & Keynotes</h2>
  </div>
  <div class="speaking-grid">
    <!-- 2026 -->
    <a href="https://github.com/Delekings/recsys-geographic-bias" target="_blank" class="speaking-card reveal" style="text-decoration:none;">
      <div class="speaking-year">2026 · Paris, France</div>
      <div class="speaking-event">Beyond Availability: Auditing Global South Cultural Visibility in Recommender Systems</div>
      <div class="speaking-venue">NeurIPS 2026 "AI and the Self" Workshop</div>
    </a>
    <div class="speaking-card reveal">
      <div class="speaking-year">2026 · London, UK</div>
      <div class="speaking-event">Auditing from the Outside: Language Blind Spots in Frontier AI Safety Evaluation</div>
      <div class="speaking-venue">ERA Technical AI Governance Forum · Poster Presentation</div>
    </div>
    <!-- 2025 -->
    <a href="https://arua.org/conferences/conference2025/" target="_blank" class="speaking-card reveal" style="text-decoration:none;">
      <div class="speaking-year">2025 · Kampala, Uganda</div>
      <div class="speaking-event">Research, Innovation & AI for Africa's Transformation</div>
      <div class="speaking-venue">ARUA 5th Biennial International Conference · Makerere University</div>
    </a>
    <a href="https://privconnigeria.org" target="_blank" class="speaking-card reveal" style="text-decoration:none;">
      <div class="speaking-year">2025 · Lagos, Nigeria</div>
      <div class="speaking-event">AI Ethics and Data Protection in Africa</div>
      <div class="speaking-venue">PrivCon Nigeria 2025 · The Civic Centre, Victoria Island</div>
    </a>
    <a href="https://waigf.ecowas.int" target="_blank" class="speaking-card reveal" style="text-decoration:none;">
      <div class="speaking-year">2025 · Accra, Ghana</div>
      <div class="speaking-event">AI Governance and Internet Policy in West Africa</div>
      <div class="speaking-venue">West Africa Internet Governance Forum (WAIGF) 2025</div>
    </a>
    <a href="https://criticalai.org/2025/11/28/program/" target="_blank" class="speaking-card reveal" style="text-decoration:none;">
      <div class="speaking-year">2025 · International</div>
      <div class="speaking-event">Critical AI: Perspectives from the Global South</div>
      <div class="speaking-venue">Critical AI Programme 2025</div>
    </a>
    <a href="https://sessionize.com/kingsley-owadara" target="_blank" class="speaking-card reveal" style="text-decoration:none;">
      <div class="speaking-year">2025 · Kenya</div>
      <div class="speaking-event">AI for Smart City: Ethical Consideration</div>
      <div class="speaking-venue">AI Summit, Kenya</div>
    </a>
    <!-- 2024 -->
    <a href="https://www.youtube.com/watch?v=B5EuYXXP8F8" target="_blank" class="speaking-card reveal" style="text-decoration:none;">
      <div class="speaking-year">2024 · Pretoria, South Africa</div>
      <div class="speaking-event">Indigenous Data Sovereignty in Algorithm Modeling</div>
      <div class="speaking-venue">Design Justice AI Global Humanities Institute · University of Pretoria · DSFSI Emerging Scholar Panel</div>
    </a>
    <a href="https://www.technomoralfutures.uk/events-database/technomoral-conversation-what-the-majority-world-can-teach-us-about-ai" target="_blank" class="speaking-card reveal" style="text-decoration:none;">
      <div class="speaking-year">2024 · Edinburgh, UK</div>
      <div class="speaking-event">Technomoral Conversations: What the Majority World Can Teach Us about AI</div>
      <div class="speaking-venue">Centre for Technomoral Futures · Edinburgh Futures Institute · with Prof. Shannon Vallor</div>
    </a>
    <a href="https://www.uj.ac.za/?p=553868" target="_blank" class="speaking-card reveal" style="text-decoration:none;">
      <div class="speaking-year">2024 · Johannesburg, South Africa</div>
      <div class="speaking-event">AI Ethics and Responsible Innovation in Africa</div>
      <div class="speaking-venue">UJ Library International Conference 2024 · University of Johannesburg</div>
    </a>
    <a href="https://privconnigeria.org/?p=199" target="_blank" class="speaking-card reveal" style="text-decoration:none;">
      <div class="speaking-year">2024 · Lagos, Nigeria</div>
      <div class="speaking-event">Privacy and Data Protection in Nigeria</div>
      <div class="speaking-venue">PrivCon Nigeria 2024 · The Civic Centre, Victoria Island</div>
    </a>
    <div class="speaking-card reveal">
      <div class="speaking-year">2024 · Bonn, Germany</div>
      <div class="speaking-event">AI for Sustainable Development in Africa</div>
      <div class="speaking-venue">Sustainability AI Lab · University of Bonn</div>
    </div>
    <!-- 2023 -->
    <div class="speaking-card reveal">
      <div class="speaking-year">2023 · Pretoria, South Africa</div>
      <div class="speaking-event">Keynote: Responsible AI and AI Ethics in Africa</div>
      <div class="speaking-venue">Future Africa, University of Pretoria</div>
    </div>
    <div class="speaking-card reveal">
      <div class="speaking-year">2023 · Sydney, Australia</div>
      <div class="speaking-event">Unleashing the Power of the Cutting-Edge: Technology in the Workplace</div>
      <div class="speaking-venue">23rd World Congress on Safety and Health at Work</div>
    </div>
    <div class="speaking-card reveal">
      <div class="speaking-year">2023 · Washington D.C., USA</div>
      <div class="speaking-event">Interdisciplinary AI Research: A Pathway to Data-driven Africa</div>
      <div class="speaking-venue">2nd International Workshop on Social Impact of AI for Africa (SIAIA-23)</div>
    </div>
    <div class="speaking-card reveal">
      <div class="speaking-year">2023 · Addis Ababa, Ethiopia</div>
      <div class="speaking-event">Ethical Considerations in Deploying LLMs in Africa</div>
      <div class="speaking-venue">1st PanAfricon AI Conference · Ethiopian AI Institute</div>
    </div>
    <a href="https://deeplearningindaba.com/2023/indabax/zim/" target="_blank" class="speaking-card reveal" style="text-decoration:none;">
      <div class="speaking-year">2023 · Zimbabwe</div>
      <div class="speaking-event">Data Ethics in Algorithm Modelling</div>
      <div class="speaking-venue">Deep Learning IndabaX Zimbabwe</div>
    </a>
    <div class="speaking-card reveal">
      <div class="speaking-year">2023 · Kigali, Rwanda</div>
      <div class="speaking-event">Responsible AI and the Sustainable Development Goals</div>
      <div class="speaking-venue">Data Science Africa 2023</div>
    </div>
    <a href="https://igf.ng/wp-content/uploads/2023/09/NIGF-2023-AGENDA.pdf" target="_blank" class="speaking-card reveal" style="text-decoration:none;">
      <div class="speaking-year">2023 · Lagos, Nigeria</div>
      <div class="speaking-event">Panel: AI and Emerging Technologies</div>
      <div class="speaking-venue">Nigeria Youth Internet Governance Forum (NYIGF) 2023</div>
    </a>
    <a href="https://deeplearningindaba.com/2023/indabax/nigeria/" target="_blank" class="speaking-card reveal" style="text-decoration:none;">
      <div class="speaking-year">2023 · Kwara, Nigeria</div>
      <div class="speaking-event">Organiser & Programme Lead</div>
      <div class="speaking-venue">Deep Learning IndabaX Nigeria 2023 · Thomas Adewumi University</div>
    </a>
  </div>
</section>

<!-- MEDIA & FEATURES -->
<section id="media" style="padding: 6rem 4rem; background: #EDE8DF;">
  <div class="reveal">
    <p class="section-label">Media & Features</p>
    <h2 class="section-title">In the Press & On Air</h2>
  </div>
  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem;">
    <a href="https://techcabal.com/2020/11/18/legavel_law_school_kingsley_owadara/" target="_blank" class="speaking-card reveal" style="text-decoration:none; background: var(--paper); border: 1px solid var(--light-rule);">
      <div class="speaking-year" style="color: var(--accent);">TECHCABAL · 2020</div>
      <div class="speaking-event" style="color: var(--ink);">Kingsley Owadara's LeGavel Wants to Help Law School Students Through a Difficult Academic Year</div>
      <div class="speaking-venue" style="color: var(--muted);">My Life In Tech Series · Feature Article</div>
    </a>
    <a href="https://pacfaie.org/wp-content/uploads/2025/06/AI-Ethics-Report-2024-3-3.pdf" target="_blank" class="speaking-card reveal" style="text-decoration:none; background: var(--paper); border: 1px solid var(--light-rule);">
      <div class="speaking-year" style="color: var(--accent);">PACFAIE · 2024</div>
      <div class="speaking-event" style="color: var(--ink);">AI Ethics Report 2024 — Editor-in-Chief</div>
      <div class="speaking-venue" style="color: var(--muted);">Pan-Africa Center for AI Ethics Annual Publication</div>
    </a>
    <a href="https://podcasts.apple.com/us/podcast/the-cybergist-podcast/id1760063230" target="_blank" class="speaking-card reveal" style="text-decoration:none; background: var(--paper); border: 1px solid var(--light-rule);">
      <div class="speaking-year" style="color: var(--accent);">PODCAST · OCT 2025</div>
      <div class="speaking-event" style="color: var(--ink);">The Cybergist Podcast S2E3: Responsible Use of AI, Especially Generative AI</div>
      <div class="speaking-venue" style="color: var(--muted);">Guest Speaker · AI Ethics, Cybersecurity & Technology Policy</div>
    </a>
    <a href="https://africatechradio.com/tts-ai-jesus-your-ai-personal-lord-and-saviour/" target="_blank" class="speaking-card reveal" style="text-decoration:none; background: var(--paper); border: 1px solid var(--light-rule);">
      <div class="speaking-year" style="color: var(--accent);">AFRICA TECH RADIO · AUG 2024</div>
      <div class="speaking-event" style="color: var(--ink);">TTS: AI Jesus - Your AI Personal Lord, and Saviour?</div>
      <div class="speaking-venue" style="color: var(--muted);">Guest Panelist · Faith, AI & Ethics Discussion</div>
    </a>
    <a href="https://bdan.ng" target="_blank" class="speaking-card reveal" style="text-decoration:none; background: var(--paper); border: 1px solid var(--light-rule);">
      <div class="speaking-year" style="color: var(--accent);">BDAN · PUBLICATION</div>
      <div class="speaking-event" style="color: var(--ink);">The Nigerian Bank Director Magazine, 7th Edition</div>
      <div class="speaking-venue" style="color: var(--muted);">Bank Directors Association of Nigeria · Featured Contributor</div>
    </a>
    <a href="https://privconnigeria.org/?p=2239" target="_blank" class="speaking-card reveal" style="text-decoration:none; background: var(--paper); border: 1px solid var(--light-rule);">
      <div class="speaking-year" style="color: var(--accent);">PRIVCON NIGERIA · 2025</div>
      <div class="speaking-event" style="color: var(--ink);">Featured Speaker Profile</div>
      <div class="speaking-venue" style="color: var(--muted);">PrivCon Nigeria — The Premier Privacy Conference</div>
    </a>
    <a href="https://deeplearningindaba.com/2024/recognising-our-reviewers/" target="_blank" class="speaking-card reveal" style="text-decoration:none; background: var(--paper); border: 1px solid var(--light-rule);">
      <div class="speaking-year" style="color: var(--accent);">DEEP LEARNING INDABA · 2024</div>
      <div class="speaking-event" style="color: var(--ink);">Recognised Application Reviewer</div>
      <div class="speaking-venue" style="color: var(--muted);">Reviewed 20+ applications for Africa's largest ML conference</div>
    </a>
    <a href="https://babl.ai/babl-ai-chief-operating-officer-leads-session-on-ai-bias-and-risk-mitigation-at-the-pan-africa-center-for-ai-ethics-summer-school" target="_blank" class="speaking-card reveal" style="text-decoration:none; background: var(--paper); border: 1px solid var(--light-rule);">
      <div class="speaking-year" style="color: var(--accent);">BABL AI · 2024</div>
      <div class="speaking-event" style="color: var(--ink);">PACFAIE AI Ethics Summer School Featured by BABL AI</div>
      <div class="speaking-venue" style="color: var(--muted);">International coverage of PACFAIE's flagship training programme</div>
    </a>
    <a href="https://www.youtube.com/watch?v=B5EuYXXP8F8" target="_blank" class="speaking-card reveal" style="text-decoration:none; background: var(--paper); border: 1px solid var(--light-rule);">
      <div class="speaking-year" style="color: var(--accent);">YOUTUBE · JULY 2024</div>
      <div class="speaking-event" style="color: var(--ink);">DJAI Emerging Scholar Panel: Indigenous Data Sovereignty in Algorithm Modeling</div>
      <div class="speaking-venue" style="color: var(--muted);">Data Science for Social Impact (DSFSI) · University of Pretoria · Design Justice AI Institute</div>
    </a>
    <div class="speaking-card reveal" style="background: var(--paper); border: 1px solid var(--light-rule);">
      <div class="speaking-year" style="color: var(--accent);">TEENS IN AI · MENTOR</div>
      <div class="speaking-event" style="color: var(--ink);">Teens in AI Global Hackathon Mentor</div>
      <div class="speaking-venue" style="color: var(--muted);">Mentored youth participants in AI ethics and responsible innovation</div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="contact-section" id="contact">
  <div class="reveal">
    <p class="section-label">Get in Touch</p>
    <h2 class="section-title">Let's Work Together</h2>
    <p class="contact-desc">
      Whether you're building AI governance frameworks, organising policy events, 
      or looking for a speaker, researcher, or collaborator — I'd love to hear from you.
    </p>
    <a href="mailto:k.owadara@pacfaie.org" class="btn-primary">k.owadara@pacfaie.org</a>
    <div class="contact-links">
      <a href="https://www.linkedin.com/in/kingsley-owadara" class="contact-link" target="_blank">LinkedIn</a>
      <a href="https://arxiv.org/pdf/2509.20099" class="contact-link" target="_blank">Latest Paper</a>
      <a href="https://africatechradio.com" class="contact-link" target="_blank">Africa Tech Radio</a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p>© 2026 Kingsley Bamidele Owadara · Lagos, Nigeria</p>
  <p>AI Ethicist · Data Governance Expert · Policy Advocate</p>
</footer>

<script>
  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => entry.target.classList.add('visible'), i * 80);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.08 });
  reveals.forEach(el => observer.observe(el));
</script>
</body>
</html>