[README-4.md](https://github.com/user-attachments/files/26541710/README-4.md)
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>UXORA — La Maison des Génies</title>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@600;700&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --green: #1d9e75;
      --green-light: #5dcaa5;
      --dark: #0b1f2a;
      --dark2: #0f3040;
      --white: #ffffff;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--dark);
      color: var(--white);
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* BACKGROUND */
    .bg-layer {
      position: fixed; inset: 0; z-index: 0; pointer-events: none;
      background: linear-gradient(135deg, #0b1f2a 0%, #0f3040 50%, #0a2535 100%);
    }
    .bg-blob1 {
      position: fixed; width: 500px; height: 500px; border-radius: 50%;
      background: radial-gradient(circle, rgba(29,158,117,0.18) 0%, transparent 65%);
      top: -150px; right: -100px; pointer-events: none; z-index: 0;
    }
    .bg-blob2 {
      position: fixed; width: 300px; height: 300px; border-radius: 50%;
      background: radial-gradient(circle, rgba(29,158,117,0.1) 0%, transparent 65%);
      bottom: 0; left: -80px; pointer-events: none; z-index: 0;
    }
    .bg-grid {
      position: fixed; inset: 0; z-index: 0; pointer-events: none;
      background-image: linear-gradient(rgba(255,255,255,0.02) 1px, transparent 1px),
                        linear-gradient(90deg, rgba(255,255,255,0.02) 1px, transparent 1px);
      background-size: 40px 40px;
    }

    /* LAYOUT */
    .page { position: relative; z-index: 1; max-width: 1100px; margin: 0 auto; padding: 0 24px; }

    /* NAV */
    nav {
      display: flex; align-items: center; justify-content: space-between;
      padding: 28px 0; border-bottom: 0.5px solid rgba(255,255,255,0.06);
    }
    .brand-name {
      font-family: 'Cormorant Garamond', serif; font-size: 36px; font-weight: 700;
      letter-spacing: 4px; line-height: 1; color: var(--white);
    }
    .brand-sub {
      font-size: 9px; letter-spacing: 5px; color: var(--green);
      text-transform: uppercase; margin-top: 4px; font-weight: 400;
    }
    .nav-links { display: flex; gap: 28px; align-items: center; }
    .nav-link {
      font-size: 11px; color: rgba(255,255,255,0.4); letter-spacing: 1.5px;
      text-transform: uppercase; cursor: pointer; text-decoration: none;
      transition: color 0.2s;
    }
    .nav-link:hover { color: var(--green-light); }
    .btn-whatsapp {
      display: inline-flex; align-items: center; gap: 8px;
      background: var(--green); color: var(--white);
      font-size: 11px; letter-spacing: 2px; text-transform: uppercase;
      padding: 10px 22px; border-radius: 4px; font-weight: 500;
      text-decoration: none; font-family: 'DM Sans', sans-serif;
      transition: background 0.2s, transform 0.15s;
    }
    .btn-whatsapp:hover { background: #17845f; transform: translateY(-1px); }
    .btn-whatsapp svg { width: 16px; height: 16px; fill: white; flex-shrink: 0; }

    /* HERO */
    .hero {
      display: grid; grid-template-columns: 1fr 1fr;
      gap: 40px; align-items: center; padding: 64px 0 48px;
    }
    .hero-label {
      font-size: 10px; letter-spacing: 4px; color: var(--green);
      text-transform: uppercase; margin-bottom: 16px; font-weight: 500;
    }
    .hero-title {
      font-family: 'Cormorant Garamond', serif; font-size: 52px;
      font-weight: 700; line-height: 1.15; margin-bottom: 20px;
    }
    .hero-title em { color: var(--green-light); font-style: normal; }
    .hero-desc {
      font-size: 15px; color: rgba(255,255,255,0.5); line-height: 1.8;
      font-weight: 300; margin-bottom: 36px; max-width: 420px;
    }
    .btn-hero {
      display: inline-flex; align-items: center; gap: 10px;
      background: var(--green); color: var(--white);
      font-size: 13px; letter-spacing: 2px; text-transform: uppercase;
      padding: 14px 32px; border-radius: 4px; font-weight: 500;
      text-decoration: none; font-family: 'DM Sans', sans-serif;
      transition: background 0.2s, transform 0.15s;
      box-shadow: 0 8px 32px rgba(29,158,117,0.3);
    }
    .btn-hero:hover { background: #17845f; transform: translateY(-2px); }
    .btn-hero svg { width: 18px; height: 18px; fill: white; }

    /* PHONE MOCKUP */
    .phone-wrap { display: flex; justify-content: center; align-items: center; }
    .phone {
      width: 220px; background: #111; border-radius: 32px;
      border: 7px solid #1c1c1c; box-shadow: 0 32px 80px rgba(0,0,0,0.6);
      overflow: hidden;
    }
    .phone-screen { background: linear-gradient(160deg, #0f3040, #0b1f2a); }
    .phone-header {
      background: rgba(29,158,117,0.9); padding: 18px 14px 12px; text-align: center;
    }
    .phone-brand {
      font-family: 'Cormorant Garamond', serif; font-size: 20px;
      color: #fff; font-weight: 700; letter-spacing: 3px;
    }
    .phone-sub {
      font-size: 7px; color: rgba(255,255,255,0.65); letter-spacing: 3px;
      text-transform: uppercase; margin-top: 2px;
    }
    .phone-stats {
      display: flex; justify-content: space-around;
      padding: 14px 10px; border-bottom: 0.5px solid rgba(255,255,255,0.07);
    }
    .ps { text-align: center; }
    .ps-n { font-size: 15px; font-weight: 500; color: #fff; }
    .ps-l { font-size: 7px; color: rgba(255,255,255,0.35); text-transform: uppercase; letter-spacing: 1px; margin-top: 2px; }
    .phone-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 5px; padding: 10px; }
    .thumb {
      background: rgba(29,158,117,0.12); border-radius: 7px; height: 64px;
      display: flex; align-items: center; justify-content: center;
      font-size: 7px; color: rgba(255,255,255,0.25); letter-spacing: 1px; text-transform: uppercase;
    }
    .thumb.a { background: rgba(29,158,117,0.28); color: rgba(255,255,255,0.55); }

    /* SERVICES */
    .section-label {
      font-size: 10px; letter-spacing: 4px; color: var(--green);
      text-transform: uppercase; font-weight: 500; margin-bottom: 24px;
    }
    .services-grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 14px; margin-bottom: 64px;
    }
    .service-card {
      background: rgba(255,255,255,0.03); border: 0.5px solid rgba(255,255,255,0.08);
      border-radius: 12px; padding: 22px 20px;
      transition: border-color 0.2s, background 0.2s;
    }
    .service-card:hover { border-color: rgba(29,158,117,0.4); background: rgba(29,158,117,0.06); }
    .service-icon {
      width: 36px; height: 36px; background: rgba(29,158,117,0.15);
      border-radius: 9px; display: flex; align-items: center; justify-content: center;
      margin-bottom: 14px;
    }
    .service-icon svg { width: 18px; height: 18px; stroke: var(--green-light); fill: none; stroke-width: 1.8; stroke-linecap: round; }
    .service-title { font-size: 14px; font-weight: 500; color: #fff; margin-bottom: 6px; }
    .service-desc { font-size: 12px; color: rgba(255,255,255,0.35); line-height: 1.6; font-weight: 300; }

    /* STATS */
    .stats-bar {
      display: grid; grid-template-columns: repeat(4, 1fr);
      border: 0.5px solid rgba(255,255,255,0.07); border-radius: 12px;
      overflow: hidden; margin-bottom: 64px;
    }
    .stat-block {
      padding: 24px; border-right: 0.5px solid rgba(255,255,255,0.07);
      text-align: center;
    }
    .stat-block:last-child { border-right: none; }
    .stat-num {
      font-family: 'Cormorant Garamond', serif; font-size: 32px;
      color: var(--green-light); font-weight: 700; margin-bottom: 4px;
    }
    .stat-desc { font-size: 10px; color: rgba(255,255,255,0.3); letter-spacing: 1.5px; text-transform: uppercase; }

    /* TOOLS */
    .tools-row { display: flex; gap: 10px; align-items: center; flex-wrap: wrap; margin-bottom: 64px; }
    .tool-badge {
      background: rgba(255,255,255,0.05); border: 0.5px solid rgba(255,255,255,0.1);
      border-radius: 6px; padding: 8px 16px; font-size: 11px;
      color: rgba(255,255,255,0.45); letter-spacing: 1.5px; text-transform: uppercase; font-weight: 500;
    }

    /* CTA SECTION */
    .cta-section {
      background: rgba(29,158,117,0.08); border: 0.5px solid rgba(29,158,117,0.2);
      border-radius: 16px; padding: 48px 40px; text-align: center; margin-bottom: 48px;
    }
    .cta-title {
      font-family: 'Cormorant Garamond', serif; font-size: 36px;
      font-weight: 700; margin-bottom: 12px;
    }
    .cta-desc { font-size: 14px; color: rgba(255,255,255,0.45); margin-bottom: 28px; font-weight: 300; }
    .btn-cta-big {
      display: inline-flex; align-items: center; gap: 12px;
      background: var(--green); color: var(--white);
      font-size: 14px; letter-spacing: 2px; text-transform: uppercase;
      padding: 16px 40px; border-radius: 4px; font-weight: 500;
      text-decoration: none; font-family: 'DM Sans', sans-serif;
      transition: background 0.2s, transform 0.15s;
      box-shadow: 0 12px 40px rgba(29,158,117,0.35);
    }
    .btn-cta-big:hover { background: #17845f; transform: translateY(-2px); }
    .btn-cta-big svg { width: 20px; height: 20px; fill: white; }

    /* FOOTER */
    footer {
      border-top: 0.5px solid rgba(255,255,255,0.06);
      padding: 28px 0; display: flex; align-items: center;
      justify-content: space-between; flex-wrap: gap;
    }
    .footer-contact { display: flex; flex-direction: column; gap: 3px; }
    .footer-label { font-size: 9px; letter-spacing: 3px; color: var(--green); text-transform: uppercase; }
    .footer-num { font-size: 18px; font-weight: 500; color: #fff; letter-spacing: 1px; }
    .social-row { display: flex; gap: 8px; flex-wrap: wrap; }
    .social-link {
      background: rgba(255,255,255,0.04); border: 0.5px solid rgba(255,255,255,0.09);
      border-radius: 6px; padding: 7px 14px; font-size: 10px;
      color: rgba(255,255,255,0.45); letter-spacing: 1px; text-decoration: none;
      transition: border-color 0.2s, color 0.2s;
    }
    .social-link:hover { border-color: rgba(29,158,117,0.5); color: var(--green-light); }
    .footer-brand {
      font-family: 'Cormorant Garamond', serif; font-size: 24px;
      color: rgba(255,255,255,0.07); letter-spacing: 5px; font-weight: 700;
    }

    /* ANIMATIONS */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(24px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    .hero-left > * { animation: fadeUp 0.6s ease both; }
    .hero-label { animation-delay: 0.1s; }
    .hero-title  { animation-delay: 0.2s; }
    .hero-desc   { animation-delay: 0.3s; }
    .btn-hero    { animation-delay: 0.4s; }

    /* CREATIONS */
    .creations-section { margin-bottom: 64px; }
    .creations-header { margin-bottom: 36px; }
    .creations-header .section-label { margin-bottom: 6px; }
    .creations-title {
      font-family: 'Cormorant Garamond', serif; font-size: 38px;
      font-weight: 700; color: #fff; margin-bottom: 12px; letter-spacing: 1px;
    }
    .creations-title em { color: var(--green-light); font-style: normal; }
    .creations-subtitle {
      font-size: 13px; color: rgba(255,255,255,0.35); font-weight: 300;
      letter-spacing: 1px;
    }
    .filter-bar {
      display: flex; gap: 10px; flex-wrap: wrap; margin-bottom: 32px;
    }
    .filter-btn {
      padding: 7px 20px;
      border: 0.5px solid rgba(255,255,255,0.12);
      background: transparent; color: rgba(255,255,255,0.35);
      font-size: 10px; letter-spacing: 2px; text-transform: uppercase;
      cursor: pointer; border-radius: 30px;
      font-family: 'DM Sans', sans-serif;
      transition: all 0.25s ease;
    }
    .filter-btn:hover { border-color: var(--green); color: var(--green-light); }
    .filter-btn.active {
      background: var(--green); color: #fff; border-color: var(--green);
    }
    .creation-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 16px;
    }
    .creation-card {
      position: relative; overflow: hidden; border-radius: 10px;
      cursor: pointer; background: rgba(255,255,255,0.03);
      border: 0.5px solid rgba(255,255,255,0.07);
      aspect-ratio: 3/4;
    }
    .creation-card.wide { grid-column: span 2; aspect-ratio: 16/10; }
    .creation-card img {
      width: 100%; height: 100%; object-fit: cover; display: block;
      transition: transform 0.5s ease;
    }
    .creation-card:hover img { transform: scale(1.06); }
    .card-overlay {
      position: absolute; inset: 0;
      background: linear-gradient(to top, rgba(0,0,0,0.85) 0%, rgba(0,0,0,0.2) 50%, transparent 100%);
      display: flex; flex-direction: column;
      justify-content: flex-end; padding: 20px;
      opacity: 0; transition: opacity 0.3s ease;
    }
    .creation-card:hover .card-overlay { opacity: 1; }
    .card-overlay h3 {
      color: #fff; font-size: 15px; font-weight: 500;
      letter-spacing: 2px; text-transform: uppercase; margin: 0 0 4px;
    }
    .card-overlay p {
      color: rgba(255,255,255,0.55); font-size: 11px;
      letter-spacing: 1px; margin: 0 0 12px; font-weight: 300;
    }
    .card-tag {
      display: inline-block; padding: 3px 12px;
      border: 0.5px solid var(--green-light); color: var(--green-light);
      font-size: 9px; letter-spacing: 2px; text-transform: uppercase;
      border-radius: 20px;
    }
    /* LIGHTBOX */
    .lightbox {
      display: none; position: fixed; inset: 0;
      background: rgba(0,0,0,0.95); z-index: 9999;
      align-items: center; justify-content: center; padding: 20px;
    }
    .lightbox.open { display: flex; }
    .lightbox img {
      max-width: 88vw; max-height: 88vh;
      object-fit: contain; border-radius: 6px;
    }
    .lb-close {
      position: fixed; top: 20px; right: 28px;
      color: #fff; font-size: 38px; cursor: pointer;
      background: none; border: none; line-height: 1; z-index: 10000;
      opacity: 0.6; transition: opacity 0.2s;
    }
    .lb-close:hover { opacity: 1; }
    .lb-nav {
      position: fixed; top: 50%; transform: translateY(-50%);
      background: rgba(255,255,255,0.08); border: none;
      color: #fff; font-size: 30px; padding: 14px 18px;
      cursor: pointer; z-index: 10000; border-radius: 6px;
      transition: background 0.2s;
    }
    .lb-nav:hover { background: rgba(29,158,117,0.4); }
    .lb-prev { left: 16px; }
    .lb-next { right: 16px; }
    .lb-info {
      position: fixed; bottom: 24px; left: 50%;
      transform: translateX(-50%); color: #fff; text-align: center;
      pointer-events: none;
    }
    .lb-info h3 {
      font-size: 14px; letter-spacing: 3px; text-transform: uppercase;
      margin: 0 0 4px; font-weight: 500;
    }
    .lb-info p { font-size: 11px; color: rgba(255,255,255,0.4); margin: 0; }

    /* RESPONSIVE */
    @media (max-width: 700px) {
      .creation-grid { grid-template-columns: 1fr 1fr; }
      .creation-card.wide { grid-column: span 2; }
      .hero { grid-template-columns: 1fr; }
      .phone-wrap { display: none; }
      .hero-title { font-size: 38px; }
      .stats-bar { grid-template-columns: 1fr 1fr; }
      .stat-block:nth-child(2) { border-right: none; }
      nav { flex-direction: column; gap: 16px; align-items: flex-start; }
      .nav-links { flex-wrap: wrap; gap: 12px; }
      footer { flex-direction: column; gap: 20px; align-items: flex-start; }
    }
  </style>
</head>
<body>

<div class="bg-layer"></div>
<div class="bg-blob1"></div>
<div class="bg-blob2"></div>
<div class="bg-grid"></div>

<div class="page">

  <!-- NAV -->
  <nav>
    <div>
      <div class="brand-name">UXORA</div>
      <div class="brand-sub">La Maison des Génies</div>
    </div>
    <div class="nav-links">
      <a class="nav-link" href="#services">Services</a>
      <a class="nav-link" href="#stats">À propos</a>
      <a class="nav-link" href="#creations">Créations</a>
      <a class="btn-whatsapp" href="https://wa.me/50931656011?text=Bonjour%20UXORA%2C%20je%20souhaite%20un%20devis%20pour%20un%20projet%20de%20design." target="_blank">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
        Contact
      </a>
    </div>
  </nav>

  <!-- HERO -->
  <div class="hero">
    <div class="hero-left">
      <p class="hero-label">Agence de Design Graphique</p>
      <h1 class="hero-title">Votre marque,<br><em>magnifiée.</em></h1>
      <p class="hero-desc">UXORA transforme vos idées en expériences visuelles inoubliables. Design sur mesure, stratégie créative, résultats qui marquent les esprits.</p>
      <a class="btn-hero" href="https://wa.me/50931656011?text=Bonjour%20UXORA%2C%20je%20souhaite%20un%20devis%20pour%20un%20projet%20de%20design." target="_blank">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
        Démarrer un projet
      </a>
    </div>
    <div class="phone-wrap">
      <div class="phone">
        <div class="phone-screen">
          <div class="phone-header">
            <div class="phone-brand">UXORA</div>
            <div class="phone-sub">La Maison des Génies</div>
          </div>
          <div class="phone-stats">
            <div class="ps"><div class="ps-n">58</div><div class="ps-l">Following</div></div>
            <div class="ps"><div class="ps-n">114</div><div class="ps-l">Followers</div></div>
            <div class="ps"><div class="ps-n">357</div><div class="ps-l">Likes</div></div>
          </div>
          <div class="phone-grid">
            <div class="thumb a">Portfolio</div>
            <div class="thumb">UXORA</div>
            <div class="thumb">UXORA</div>
            <div class="thumb a">Design</div>
            <div class="thumb">UXORA</div>
            <div class="thumb a">Projet</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- SERVICES -->
  <div id="services">
    <p class="section-label">Nos Services</p>
    <div class="services-grid">
      <div class="service-card">
        <div class="service-icon"><svg viewBox="0 0 24 24"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/></svg></div>
        <div class="service-title">Création de Logo</div>
        <div class="service-desc">Identités visuelles uniques et mémorables qui représentent votre marque.</div>
      </div>
      <div class="service-card">
        <div class="service-icon"><svg viewBox="0 0 24 24"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M3 9h18M9 21V9"/></svg></div>
        <div class="service-title">Affiches & Flyers</div>
        <div class="service-desc">Supports de communication percutants pour vos événements et promotions.</div>
      </div>
      <div class="service-card">
        <div class="service-icon"><svg viewBox="0 0 24 24"><rect x="2" y="3" width="20" height="14" rx="2"/><path d="M8 21h8M12 17v4"/></svg></div>
        <div class="service-title">Sites Web</div>
        <div class="service-desc">Sites modernes, rapides et adaptés à tous les appareils.</div>
      </div>
      <div class="service-card">
        <div class="service-icon"><svg viewBox="0 0 24 24"><rect x="5" y="2" width="14" height="20" rx="2"/><path d="M12 18h.01"/></svg></div>
        <div class="service-title">Applications PWA</div>
        <div class="service-desc">Applications web progressives installables sur tous vos appareils.</div>
      </div>
    </div>
  </div>

  <!-- STATS -->
  <div id="stats" class="stats-bar">
    <div class="stat-block"><div class="stat-num">100+</div><div class="stat-desc">Projets livrés</div></div>
    <div class="stat-block"><div class="stat-num">50+</div><div class="stat-desc">Clients satisfaits</div></div>
    <div class="stat-block"><div class="stat-num">4</div><div class="stat-desc">Services offerts</div></div>
    <div class="stat-block"><div class="stat-num">24h</div><div class="stat-desc">Réponse rapide</div></div>
  </div>

  <!-- TOOLS -->
  <p class="section-label">Outils utilisés</p>
  <div class="tools-row">
    <span class="tool-badge">Canva</span>
    <span class="tool-badge">Affinity Designer</span>
    <span class="tool-badge">Photoshop</span>
    <span class="tool-badge">Illustrator</span>
  </div>

  <!-- CRÉATIONS -->
  <div id="creations" class="creations-section">
    <div class="creations-header">
      <p class="section-label">Portfolio</p>
      <h2 class="creations-title">Nos <em>Créations</em></h2>
      <p class="creations-subtitle">Design · Branding · Visual Identity · Food · Fashion</p>
    </div>

    <div class="filter-bar">
      <button class="filter-btn active" data-filter="all">Tout</button>
      <button class="filter-btn" data-filter="fashion">Fashion</button>
      <button class="filter-btn" data-filter="food">Food & Drink</button>
      <button class="filter-btn" data-filter="branding">Branding</button>
      <button class="filter-btn" data-filter="parfum">Parfum</button>
    </div>

        

  <!-- LIGHTBOX -->
  <div class="lightbox" id="lightbox">
    <button class="lb-close" id="lb-close">&times;</button>
    <button class="lb-nav lb-prev" id="lb-prev">&#8249;</button>
    <img src="" id="lb-img" alt="">
    <button class="lb-nav lb-next" id="lb-next">&#8250;</button>
    <div class="lb-info">
      <h3 id="lb-title"></h3>
      <p id="lb-desc"></p>
    </div>
  </div>

  <!-- CTA -->
  <div class="cta-section">
    <h2 class="cta-title">Prêt à lancer votre projet ?</h2>
    <p class="cta-desc">Contactez-nous sur WhatsApp et recevez un devis rapide.</p>
    <a class="btn-cta-big" href="https://wa.me/50931656011?text=Bonjour%20UXORA%2C%20je%20souhaite%20un%20devis%20pour%20un%20projet%20de%20design." target="_blank">
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
      Nous contacter sur WhatsApp
    </a>
  </div>

  <!-- FOOTER -->
  <footer>
    <div class="footer-contact">
      <span class="footer-label">Contact us</span>
      <span class="footer-num">+509 3165 6011</span>
    </div>
    <div class="social-row">
      <a class="social-link" href="https://instagram.com/UXORA04" target="_blank">📸 UXORA04</a>
      <a class="social-link" href="https://facebook.com/trevor.phillips" target="_blank">👤 Trevor Phillips</a>
      <a class="social-link" href="https://tiktok.com/@UXORA7" target="_blank">🎵 UXORA7</a>
    </div>
    <div class="footer-brand">UXORA</div>
  </footer>

</div>
<script>
  const cards = document.querySelectorAll('.creation-card');
  const lightbox = document.getElementById('lightbox');
  const lbImg = document.getElementById('lb-img');
  const lbTitle = document.getElementById('lb-title');
  const lbDesc = document.getElementById('lb-desc');
  let currentIndex = 0;
  let visibleCards = [];

  const allData = Array.from(cards).map(card => ({
    src: card.querySelector('img').src,
    title: card.querySelector('h3').textContent,
    desc: card.querySelector('p').textContent,
    category: card.dataset.category
  }));

  function updateVisible() {
    visibleCards = Array.from(cards).filter(c => c.style.display !== 'none');
  }

  function openLightbox(card) {
    updateVisible();
    currentIndex = visibleCards.indexOf(card);
    const d = allData[parseInt(card.dataset.index)];
    lbImg.src = d.src; lbTitle.textContent = d.title; lbDesc.textContent = d.desc;
    lightbox.classList.add('open');
    document.body.style.overflow = 'hidden';
  }

  function closeLightbox() {
    lightbox.classList.remove('open');
    document.body.style.overflow = '';
  }

  function navigate(dir) {
    updateVisible();
    currentIndex = (currentIndex + dir + visibleCards.length) % visibleCards.length;
    const d = allData[parseInt(visibleCards[currentIndex].dataset.index)];
    lbImg.src = d.src; lbTitle.textContent = d.title; lbDesc.textContent = d.desc;
  }

  cards.forEach(card => card.addEventListener('click', () => openLightbox(card)));
  document.getElementById('lb-close').addEventListener('click', closeLightbox);
  document.getElementById('lb-prev').addEventListener('click', () => navigate(-1));
  document.getElementById('lb-next').addEventListener('click', () => navigate(1));
  lightbox.addEventListener('click', e => { if (e.target === lightbox) closeLightbox(); });
  document.addEventListener('keydown', e => {
    if (e.key === 'Escape') closeLightbox();
    if (e.key === 'ArrowLeft') navigate(-1);
    if (e.key === 'ArrowRight') navigate(1);
  });

  document.querySelectorAll('.filter-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;
      cards.forEach(card => {
        card.style.display = (filter === 'all' || card.dataset.category === filter) ? '' : 'none';
      });
    });
  });
</script>
</body>
</html>
![image URL](Limage URL](https://github.com/korramomo65-png/SampleRepo/blob/main/1JLY1SLSK8-AZ08gt9UdYqA.jpg?raw=true))
