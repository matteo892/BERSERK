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
    body{
      margin:0;
      background: linear-gradient(to bottom, #000000, #330000);
      color:#3a0000;
      -webkit-font-smoothing:antialiased;
      overflow-x:hidden;
      overflow-y:hidden;
    }

    .emoji-box{background:#111;color:#3a0000;}

    .container{max-width:1100px;margin:0 auto;padding:28px}

    header{display:flex;align-items:center;justify-content:space-between;padding:14px 0}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:48px;height:48px;border-radius:10px;display:flex;align-items:center;justify-content:center;font-weight:800}
    .brand h1{margin:0;font-size:18px}
    nav a{
      color:#3a0000;
      text-decoration:none;
      margin-left:18px;
      font-weight:600;
    }
    nav a:focus, nav a:hover{
      text-decoration:underline;
      outline:2px solid var(--accent);
    }

    .hero{display:grid;grid-template-columns:1fr 420px;gap:32px;align-items:center;margin-top:18px}
    .hero-card{background:linear-gradient(180deg,rgba(255,255,255,0.05),transparent);padding:28px;border-radius:14px;backdrop-filter:blur(6px);box-shadow:0 6px 30px rgba(0,0,0,0.5)}
    .hero h2{margin:0 0 12px;font-size:28px}
    .hero p{color:var(--muted);line-height:1.5}
    .invite-row{display:flex;gap:12px;margin-top:18px}
    .btn{padding:12px 16px;border-radius:10px;border:0;font-weight:700;cursor:pointer;color:#3a0000}
    .btn-invite{background:linear-gradient(90deg,#d7b3ff,#f7d9e3);color:#3a0000}
    .btn-invite:focus, .btn-invite:hover{outline:2px solid var(--accent-2)}
    .btn-join{background:transparent;border:1px solid rgba(255,255,255,0.3);color:#3a0000}
    .btn-join:focus, .btn-join:hover{outline:2px solid var(--accent-2)}

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
    .copy-ok{background:rgba(255,255,255,0.45);padding:8px;border-radius:8px;position:fixed;right:18px;bottom:18px;color:#3a0000;display:none;z-index:10000}

    .bg-shape{position:fixed;right:-120px;top:-120px;width:420px;height:420px;border-radius:40%;filter:blur(60px);opacity:0.25;background:linear-gradient(45deg,var(--accent),var(--accent-2));}

    /* Pétales rouges sang avec dérive */
    .petals span{
      position:absolute;
      top:-30px;
      width:12px;
      height:24px;
      background: #8B0000; /* rouge sang */
      border-radius:50% 50% 70% 70%;
      opacity:0.9;
      filter: drop-shadow(0 0 6px #550000);
      animation-name: fall;
      animation-timing-function: linear;
      animation-iteration-count: infinite;
    }

    @keyframes fall {
      0% {
        transform: translateX(0px) translateY(0px) rotate(0deg);
        opacity: 0.9;
      }
      50% {
        transform: translateX(var(--drift)) translateY(55vh) rotate(180deg);
      }
      100% {
        transform: translateX(calc(-1 * var(--drift))) translateY(110vh) rotate(360deg);
        opacity: 0.6;
      }
    }

    /* Style du compteur de membres en ligne */
    .online-count {
      display: inline-block;
      background: rgba(255,255,255,0.1);
      padding: 6px 12px;
      border-radius: 12px;
      font-weight: 700;
      color: #3a0000;
      font-size: 14px;
    }
  </style>
</head>
<body>
  <div class="petals" aria-hidden="true"></div>

  <div class="bg-shape" aria-hidden="true"></div>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo emoji-box" aria-hidden="true">🔥</div>
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
          <a class="btn btn-join" href="https://discord.gg/1198629149506551878" id="openInvite" target="_blank" rel="noopener noreferrer">Ouvrir l'invitation</a>
        </div>

        <div style="margin-top:14px;display:flex;gap:8px;align-items:center">
          <span class="pill">>500 membres</span>
          <span class="pill">24/7</span>
          <span class="online-count" id="onlineCount">Membres en ligne : …</span>
        </div>

        <!-- Widget Discord invisible pour récupérer le nombre de membres -->
        <iframe src="https://discord.com/widget?id=1198629149506551878&theme=dark" width="0" height="0" style="display:none;" id="discordWidget"></iframe>

      </div>

      <aside>
        <div class="panel">
          <div style="display:flex;align-items:center;gap:12px;margin-bottom:14px">
            <div class="emoji-box" style="width:56px;height:56px;border-radius:12px;display:flex;align-items:center;justify-content:center;font-weight:800;" aria-hidden="true">🔥</div>
            <div>
              <strong>BERSERK</strong>
            </div>
          </div>
        </div>
      </aside>
    </section>
  </div>

  <div class="copy-ok" id="copyOK">Lien copié !</div>

  <script>
    const copyBtn = document.getElementById('copyInvite');
    const openBtn = document.getElementById('openInvite');
    const copyOK = document.getElementById('copyOK');

    copyBtn.addEventListener('click', () => {
      const inviteLink = openBtn.href;
      navigator.clipboard.writeText(inviteLink).then(() => {
        copyOK.style.display = 'block';
        setTimeout(() => copyOK.style.display = 'none', 2000);
        window.open(inviteLink, "_blank");
      }).catch(err => console.error("Erreur lors de la copie:", err));
    });

    // Génération des pétales avec dérive
    const petalsContainer = document.querySelector('.petals');
    const numberOfPetals = 40;

    for(let i=0; i<numberOfPetals; i++){
      const petal = document.createElement('span');
      petalsContainer.appendChild(petal);
      petal.style.left = Math.random() * window.innerWidth + 'px';
      petal.style.transform = `scale(${Math.random() * 0.8 + 0.6}) rotate(${Math.random()*360}deg)`;
      petal.style.animationDuration = (Math.random() * 5 + 5) + 's';
      petal.style.animationDelay = Math.random() * 5 + 's';
      petal.style.setProperty('--drift', `${Math.random() * 60 - 30}px`);
    }

    // Affichage du nombre de membres en ligne via le widget Discord
    // ATTENTION : Discord ne permet pas de récupérer directement le nombre exact côté client
    // avec le widget invisible. Pour un compteur exact, il faut passer par un bot / API côté serveur.
    // Ici on laisse un texte statique ou dynamique si tu utilises un backend.

    document.getElementById('onlineCount').innerText = "Membres en ligne : (widget Discord actif)";
  </script>
</body>
</html>
