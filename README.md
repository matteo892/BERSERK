<html lang="fr">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>BERSERK — Bienvenue</title>
  <meta name="description" content="Page d'accueil officielle de BERSERK — Rejoins-nous !">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg1:#000000;
      --bg2:#111111;
      --accent:#6ee7b7;
      --accent-2:#7c3aed;
      --muted:rgba(150,0,0,0.65);
      --glass: rgba(255,255,255,0.06);
      --card: rgba(255,255,255,0.08);
      font-family: 'Inter', system-ui;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{margin:0;background:#000;color:#3a0000;-webkit-font-smoothing:antialiased}

    .emoji-box{background:#111 !important;color:#3a0000 !important;}

    .container{max-width:1100px;margin:0 auto;padding:28px}

    header{display:flex;align-items:center;justify-content:space-between;padding:14px 0}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:48px;height:48px;border-radius:10px;display:flex;align-items:center;justify-content:center;font-weight:800}
    .brand h1{margin:0;font-size:18px}
    nav a{color:#3a0000;text-decoration:none;margin-left:18px;font-weight:600}

    .hero{display:grid;grid-template-columns:1fr 420px;gap:32px;align-items:center;margin-top:18px}
    .hero-card{background:linear-gradient(180deg,rgba(255,255,255,0.05),transparent);padding:28px;border-radius:14px;backdrop-filter:blur(6px);box-shadow:0 6px 30px rgba(0,0,0,0.5)}
    .hero h2{margin:0 0 12px;font-size:28px}
    .hero p{color:var(--muted);line-height:1.5}
    .invite-row{display:flex;gap:12px;margin-top:18px}
    .btn{padding:12px 16px;border-radius:10px;border:0;font-weight:700;cursor:pointer;color:#3a0000}
    .btn-invite{background:linear-gradient(90deg,#d7b3ff,#f7d9e3);color:#3a0000}
    .btn-join{background:transparent;border:1px solid rgba(255,255,255,0.3);color:#3a0000}

    .panel{background:var(--card);padding:18px;border-radius:12px}
    .stat{display:flex;justify-content:space-between;margin-bottom:12px}
    .stat strong{font-size:20px;color:#3a0000}
    .muted{color:var(--muted);font-size:13px}

    .features{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-top:26px}
    .feature{background:var(--glass);padding:18px;border-radius:12px}
    .feature h3{margin:0 0 6px;color:#3a0000}
    .feature p{margin:0;color:var(--muted);font-size:14px}

    footer{margin-top:34px;padding:18px 0;color:var(--muted);text-align:center}

    @media (max-width:980px){.hero{grid-template-columns:1fr}.features{grid-template-columns:repeat(2,1fr)}}
    @media (max-width:640px){.features{grid-template-columns:1fr}.logo{width:42px;height:42px}.brand h1{font-size:16px}}

    .pill{display:inline-block;padding:6px 10px;border-radius:999px;background:rgba(255,255,255,0.08);font-weight:700;color:#3a0000}
    .copy-ok{background:rgba(255,255,255,0.45);padding:8px;border-radius:8px;position:fixed;right:18px;bottom:18px;color:#3a0000;display:none}

    .bg-shape{position:fixed;right:-120px;top:-120px;width:420px;height:420px;border-radius:40%;filter:blur(60px);opacity:0.25;background:linear-gradient(45deg,var(--accent),var(--accent-2));}

    .petals span{position:absolute;top:-10%;width:10px;height:26px;background:#300000;border-radius:50% 50% 70% 70%;opacity:0.95;animation:drip 3s linear infinite;filter:drop-shadow(0 0 6px #220000);}
@keyframes drip{0%{transform:translateY(-10%) scale(1);}100%{transform:translateY(110vh) scale(0.8);}}{0%{transform:translateY(-10%) scale(1)}100%{transform:translateY(110vh) scale(0.8)}}
.petals span:nth-child(odd){animation-duration:10s}

    button{background:linear-gradient(90deg,#d7b3ff,#f7d9e3);color:#3a0000;padding:12px 16px;border-radius:10px;border:0;font-weight:700;cursor:pointer}
    .center-drop{position:fixed;top:-40px;left:50%;transform:translateX(-50%);width:14px;height:32px;background:#3a0000;border-radius:50% 50% 70% 70%;opacity:1;animation:centerDrip 2.8s linear infinite;filter:drop-shadow(0 0 8px #220000);z-index:9999;}
@keyframes centerDrip{0%{transform:translate(-50%,-40px) scale(1);}100%{transform:translate(-50%,110vh) scale(0.9);}}
.petals span:nth-child(1){left:5%;animation-delay:0s;} .petals span:nth-child(2){left:15%;animation-delay:1s;} .petals span:nth-child(3){left:25%;animation-delay:0.5s;} .petals span:nth-child(4){left:35%;animation-delay:1.3s;} .petals span:nth-child(5){left:45%;animation-delay:0.2s;} .petals span:nth-child(6){left:55%;animation-delay:1.1s;} .petals span:nth-child(7){left:65%;animation-delay:0.4s;} .petals span:nth-child(8){left:75%;animation-delay:1.4s;} .petals span:nth-child(9){left:85%;animation-delay:0.7s;} .petals span:nth-child(10){left:95%;animation-delay:1.6s;} .center-drop{position:fixed;top:-80px;left:50%;transform:translateX(-50%);width:26px;height:60px;background:#300000;border-radius:50% 50% 70% 70%;opacity:1;animation:centerDrip 4s ease-in-out infinite;filter:drop-shadow(0 0 10px #220000);z-index:9999;} @keyframes centerDrip{0%{transform:translate(-50%,-80px) scale(0);}20%{transform:translate(-50%,-40px) scale(1.4);}30%{transform:translate(-50%,-40px) scale(1);}100%{transform:translate(-50%,120vh) scale(0.9);} }
</style>
</head>
<body>
  <div class="center-drop"></div>
  <div class="petals" aria-hidden="true">
    <span></span><span></span><span></span><span></span><span></span>
    <span></span><span></span><span></span><span></span><span></span>
    <span></span><span></span><span></span><span></span><span></span>
  </div>
  <div class="bg-shape" aria-hidden="true"></div>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo emoji-box" aria-hidden="true">🩸</div>
        <div>
          <h1>BERSERK</h1>
          <div class="muted">Communauté • Événements • Jeux</div>
        </div>
      </div>
      <nav>
        <a href="#about">À propos</a>
        <a href="#features">Fonctionnalités</a>
        <a href="#join">Rejoindre</a>
      </nav>
    </header>

    <section class="hero">
      <div class="hero-card">
        <h2>Bienvenue sur BERSERK</h2>
        <p>Un lieu chaleureux pour se retrouver, jouer, organiser des événements et discuter de tout.</p>

        <div class="invite-row">
          <button class="btn btn-invite" id="copyInvite" aria-label="Copier et ouvrir l'invitation">Rejoindre le serveur</button>
          <a class="btn btn-join" href="https://discord.gg/YxyFDPCKWp" id="openInvite" target="_blank" rel="noopener noreferrer">Ouvrir l'invitation</a>
        </div>

        <div style="margin-top:14px;display:flex;gap:8px;align-items:center">
          <span class="pill">>500 membres</span>
          <span class="pill">24/7</span>
          <span class="muted" style="margin-left:auto">Prochain event: Samedi 20h</span>
        </div>
      </div>

      <aside>
        <div class="panel">
          <div style="display:flex;align-items:center;gap:12px;margin-bottom:14px">
            <div class="emoji-box" style="width:56px;height:56px;border-radius:12px;display:flex;align-items:center;justify-content:center;font-weight:800;" aria-hidden="true">🩸</div>
            <div>
              <strong>🩸 BERSERK 🩸 <strong>
