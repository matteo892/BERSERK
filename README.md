<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Berserk — Bienvenue</title>
  <meta name="description" content="Page d'accueil de Berserk — Communauté" />
  <meta name="theme-color" content="#000000" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet" />
  <style>
    :root{
      --bg:#000000;
      --text:#ff3b3b;         /* texte rouge vif */
      --muted:rgba(255,59,59,0.75);
      --card: rgba(255,59,59,0.04);
      --glass: rgba(255,59,59,0.03);
      --accent:#8b0000;      /* sang foncé */
      --accent-2:#4a0000;    /* sang très foncé */
      font-family: 'Inter', system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      background:var(--bg);
      color:var(--text);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }

    a{color:var(--text)}
    .container{max-width:1100px;margin:0 auto;padding:28px}

    header{display:flex;align-items:center;justify-content:space-between;padding:14px 0}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{
      width:48px;height:48px;border-radius:10px;
      display:flex;align-items:center;justify-content:center;font-weight:800;
      background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(255,255,255,0.01));
      color:var(--text);
      box-shadow:0 2px 10px rgba(0,0,0,0.6) inset;
    }
    .brand h1{margin:0;font-size:18px;color:var(--text)}
    nav a{color:var(--muted);text-decoration:none;margin-left:18px;font-weight:600}

    .hero{display:grid;grid-template-columns:1fr 420px;gap:32px;align-items:center;margin-top:18px;z-index:2;position:relative}
    .hero-card{
      background:linear-gradient(180deg,rgba(255,59,59,0.02),transparent);
      padding:28px;border-radius:14px;backdrop-filter:blur(6px);
      box-shadow:0 6px 30px rgba(0,0,0,0.6);
      border:1px solid rgba(255,59,59,0.03);
    }
    .hero h2{margin:0 0 12px;font-size:28px;color:var(--text)}
    .hero p{color:var(--muted);line-height:1.5}
    .invite-row{display:flex;gap:12px;margin-top:18px;flex-wrap:wrap}
    .btn{padding:12px 16px;border-radius:10px;border:0;font-weight:700;cursor:pointer;color:var(--text)}
    .btn-invite{
      background:linear-gradient(90deg,var(--accent),var(--accent-2));
      color:#fff;
      box-shadow:0 6px 18px rgba(139,0,0,0.35);
      border:1px solid rgba(255,255,255,0.02);
    }
    .btn-join{
      background:transparent;border:1px solid rgba(255,59,59,0.12);color:var(--text);
      text-decoration:none;display:inline-flex;align-items:center;justify-content:center;
    }

    .panel{background:var(--card);padding:18px;border-radius:12px;border:1px solid rgba(255,59,59,0.02)}
    .stat{display:flex;justify-content:space-between;margin-bottom:12px}
    .stat strong{font-size:20px;color:var(--text)}
    .muted{color:var(--muted);font-size:13px}

    .features{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-top:26px}
    .feature{background:var(--glass);padding:18px;border-radius:12px}
    .feature h3{margin:0 0 6px;color:var(--text)}
    .feature p{margin:0;color:var(--muted);font-size:14px}

    footer{margin-top:34px;padding:18px 0;color:var(--muted);text-align:center}

    @media (max-width:980px){.hero{grid-template-columns:1fr}.features{grid-template-columns:repeat(2,1fr)}}
    @media (max-width:640px){.features{grid-template-columns:1fr}.logo{width:42px;height:42px}.brand h1{font-size:16px}}

    .pill{display:inline-block;padding:6px 10px;border-radius:999px;background:rgba(255,59,59,0.04);font-weight:700;color:var(--text)}
    .copy-ok{background:rgba(139,0,0,0.9);padding:8px;border-radius:8px;position:fixed;right:18px;bottom:18px;color:#fff;display:none;z-index:9999}

    .bg-shape{
      position:fixed;right:-120px;top:-120px;width:420px;height:420px;border-radius:40%;
      filter:blur(60px);opacity:0.22;background:linear-gradient(45deg,var(--accent),var(--accent-2));
      transform:rotate(20deg);pointer-events:none;z-index:0;
    }

    /* gouttes de sang à la place des pétales */
    .drops{position:fixed;left:0;top:0;right:0;bottom:0;pointer-events:none;overflow:visible;z-index:1}
    .drops span{
      position:absolute;
      top:-10%;
      width:12px;
      height:18px;
      background:linear-gradient(180deg,var(--accent),var(--accent-2));
      border-radius:50% 50% 50% 50%/60% 60% 40% 40%;
      transform:rotate(45deg);
      opacity:0.95;
      box-shadow:0 6px 12px rgba(0,0,0,0.6);
      animation:drip 7s linear infinite;
      transform-origin:center;
    }
    .drops span:after{
      /* petite pointe pour rappeler la goutte */
      content:"";
      position:absolute;
      left:50%;
      top:84%;
      width:6px;
      height:6px;
      background:var(--accent-2);
      border-radius:50%;
      transform:translateX(-50%);
      box-shadow:0 2px 4px rgba(0,0,0,0.6);
    }
    @keyframes drip{
      0%{transform:translateY(-10vh) rotate(10deg) scaleY(0.9)}
      70%{transform:translateY(85vh) rotate(25deg) scaleY(1.05)}
      100%{transform:translateY(110vh) rotate(35deg) scaleY(1.1)}
    }
    .drops span:nth-child(odd){animation-duration:9s}
    .drops span:nth-child(2){animation-delay:1s}
    .drops span:nth-child(3){animation-delay:2.5s}
    .drops span:nth-child(4){animation-delay:.6s}
    .drops span:nth-child(5){animation-delay:3.1s}
    .drops span:nth-child(6){animation-delay:4.2s}

    button:focus, a.btn-join:focus {outline:3px solid rgba(255,59,59,0.18);outline-offset:2px}
  </style>
</head>
<body>
  <div class="bg-shape" aria-hidden="true"></div>

  <div class="container" role="main">
    <header>
      <div class="brand">
        <div class="logo" aria-hidden="true">🩸</div>
        <div>
          <h1>Berserk</h1>
          <div class="muted">Communauté • Événements • Jeux</div>
        </div>
      </div>
      <nav aria-label="Navigation principale">
        <a href="#about">À propos</a>
        <a href="#features">Fonctionnalités</a>
        <a href="#join">Rejoindre</a>
      </nav>
    </header>

    <section class="hero" aria-labelledby="hero-title">
      <div class="hero-card">
        <h2 id="hero-title">Bienvenue sur Berserk</h2>
        <p>Un lieu sombre et puissant pour se retrouver, jouer, organiser des événements et partager.</p>

        <div class="invite-row">
          <button class="btn btn-invite" id="copyInvite" aria-label="Copier et ouvrir l'invitation">Rejoindre le serveur</button>
          <a class="btn btn-join" href="https://discord.gg/YxyFDPCKWp" id="openInvite" target="_blank" rel="noopener noreferrer">Ouvrir l'invitation</a>
        </div>

        <div style="margin-top:14px;display:flex;gap:8px;align-items:center;flex-wrap:wrap">
          <span class="pill">>500 membres</span>
          <span class="pill">24/7</span>
          <span class="muted" style="margin-left:auto">Prochain event: Samedi 20h</span>
        </div>
      </div>

      <aside>
        <div class="panel" aria-labelledby="server-name">
          <div style="display:flex;align-items:center;gap:12px;margin-bottom:14px">
            <div style="width:56px;height:56px;border-radius:12px;display:flex;align-items:center;justify-content:center;font-weight:800;background:rgba(255,255,255,0.02)" aria-hidden="true">🩸</div>
            <div>
              <strong id="server-name">Berserk</strong>
              <div class="muted">Serveur communautaire</div>
            </div>
          </div>

          <div class="stat"><span class="muted">En ligne</span> <strong id="onlineCount">...</strong></div>
        </div>
      </aside>
    </section>

    <footer>
      <div class="muted">© <span id="year"></span> Berserk — Tous droits réservés</div>
    </footer>
  </div>

  <!-- input caché pour la copie (fallback) -->
  <input id="inviteInput" type="text" value="https://discord.gg/YxyFDPCKWp" style="position:absolute;left:-9999px;top:auto;width:1px;height:1px;overflow:hidden" aria-hidden="true" />

  <!-- notification copie -->
  <div id="copyOk" class="copy-ok" role="status" aria-live="polite">Lien copié !</div>

  <script>
    // Inscrire l'année
    const yearEl = document.getElementById('year');
    if (yearEl) yearEl.textContent = new Date().getFullYear();

    function showCopy(){
      const el = document.getElementById('copyOk');
      if (!el) return;
      el.style.display = 'block';
      el.setAttribute('aria-hidden','false');
      setTimeout(()=>{ el.style.display='none'; el.setAttribute('aria-hidden','true'); },1800);
    }

    // Compatibilité copy
    document.getElementById('copyBtn')?.addEventListener('click', async ()=>{
      const input = document.getElementById('inviteInput');
      if (!input) { alert('Aucun lien à copier'); return; }
      try { await navigator.clipboard.writeText(input.value); showCopy(); } catch(e){
        input.select();
        try { document.execCommand('copy'); showCopy(); } catch(err){ alert('Copie impossible'); }
      }
    });

    // Bouton principal : copie + ouvre (fallback)
    document.getElementById('copyInvite')?.addEventListener('click', async ()=>{
      const inviteInput = document.getElementById('inviteInput');
      const openInvite = document.getElementById('openInvite');
      const link = (inviteInput && inviteInput.value) || (openInvite && openInvite.href);
      if (!link) { alert('Aucun lien d\'invitation disponible'); return; }
      try {
        if (navigator.clipboard && navigator.clipboard.writeText) {
          await navigator.clipboard.writeText(link);
          showCopy();
        } else if (inviteInput) {
          inviteInput.style.position='absolute';
          inviteInput.style.left='0';
          inviteInput.style.top='0';
          inviteInput.focus();
          inviteInput.select();
          document.execCommand('copy');
          inviteInput.style.left='-9999px';
          showCopy();
        }
      } catch (e) {
        console.warn('Échec copie dans le presse-papiers', e);
      } finally {
        try { window.open(link, '_blank', 'noopener'); } catch(e){ /* noop */ }
      }
    });

    async function loadDiscordStats() {
      try {
        const res = await fetch("https://discord.com/api/guilds/1190398760946241536/widget.json", {cache:'no-store'});
        if (!res.ok) throw new Error('Widget non disponible');
        const data = await res.json();
        const el = document.getElementById("onlineCount");
        if (el) el.textContent = typeof data.presence_count !== 'undefined' ? data.presence_count : '—';
      } catch (e) {
        const el = document.getElementById("onlineCount");
        if (el) el.textContent = '—';
        console.warn('Impossible de charger les stats Discord:', e);
      }
    }
    loadDiscordStats();
  </script>

  <div class="drops" aria-hidden="true">
    <span style="left:10%"></span>
    <span style="left:25%"></span>
    <span style="left:40%"></span>
    <span style="left:55%"></span>
    <span style="left:70%"></span>
    <span style="left:85%"></span>
  </div>
</body>
</html>
