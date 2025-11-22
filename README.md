<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Berserk — Page d'invitation</title>
  <link href="styles.css" rel="stylesheet">
</head>
<body>
  <header class="site-header">
    <div class="container">
      <a class="brand" href="/">Berserk</a>
      <nav class="site-nav">
        <a href="#about">À propos</a>
        <a href="#features">Features</a>
        <a href="#community">Communauté</a>
        <a href="#widget">Widget</a>
        <a href="#rules">Règles</a>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="container hero-grid">
        <div class="hero-content">
          <h1>Sous le signe du Berserk</h1>
          <p class="lead">Une communauté pour discuter du manga, partager du fan‑art, organiser des events et jouer ensemble.</p>

          <div class="cta-row" role="group" aria-label="Actions">
            <a id="joinBtn" class="btn btn-primary" href="https://discord.gg/YOUR_INVITE" target="_blank" rel="noopener" aria-disabled="false">Rejoindre le serveur</a>
            <button id="copyInvite" class="btn btn-outline" data-invite="https://discord.gg/YOUR_INVITE" aria-label="Copier le lien d'invitation">Copier l'invitation</button>
          </div>

          <p class="muted">Préférez-vous un aperçu du widget ? Activez le widget côté Discord et entrez l'ID du serveur dans la section Widget.</p>

          <div class="quick-info">
            <div>
              <strong>Public</strong>
              <span>Discussions, jeux, fan‑art</span>
            </div>
            <div>
              <strong>Modération</strong>
              <span>Actifs et bienveillants</span>
            </div>
            <div>
              <strong>Langue</strong>
              <span>Français</span>
            </div>
          </div>
        </div>

        <div class="hero-visual" aria-hidden="true">
          <svg viewBox="0 0 400 240" xmlns="http://www.w3.org/2000/svg" class="hero-svg">
            <defs>
              <linearGradient id="g" x1="0" x2="1">
                <stop offset="0" stop-color="#2b2b2b"/>
                <stop offset="1" stop-color="#0b0b0b"/>
              </linearGradient>
            </defs>
            <rect width="100%" height="100%" fill="url(#g)"/>
            <text x="50%" y="55%" text-anchor="middle" fill="#8b0000" font-family="Cinzel, serif" font-size="42">BERSERK</text>
          </svg>
        </div>
      </div>
    </section>

    <section id="about" class="container card">
      <h2>À propos</h2>
      <p>Bienvenue sur le serveur inspiré par Berserk — un espace pour discuter du manga, des théories, organiser des parties, participer aux events et partager des créations. Respect, bienveillance et protection du droit d'auteur sont essentiels.</p>
    </section>

    <section id="features" class="container card">
      <h2>Features</h2>
      <div class="features">
        <article class="feature">
          <h3>Discussions</h3>
          <p>Théories, chapitres et analyses.</p>
        </article>
        <article class="feature">
          <h3>Jeux & Events</h3>
          <p>Tournois, soirées jeu et activités communautaires.</p>
        </article>
        <article class="feature">
          <h3>Ressources</h3>
          <p>Guides, fan‑art et créations.</p>
        </article>
      </div>
    </section>

    <section id="community" class="container card">
      <h2>Communauté — Activité récente</h2>
      <ul class="posts">
        <li>
          <strong>Heureux accueil</strong>
          <p>Bienvenue aux nouveaux membres ! Présentez‑vous dans #présentation.</p>
        </li>
        <li>
          <strong>Sondage</strong>
          <p>Votez pour le prochain event : quiz ou soirée RP ?</p>
        </li>
      </ul>
    </section>

    <section id="widget" class="container card dark">
      <h2>Widget Discord (aperçu)</h2>
      <p>Activez le widget côté Discord (Paramètres du serveur → Widget) et entrez l'ID du serveur ci‑dessous pour voir l'aperçu.</p>

      <div class="widget-config">
        <label for="serverId">ID du serveur (SERVER_ID)</label>
        <input id="serverId" name="serverId" placeholder="Entrez l'ID du serveur" aria-label="ID du serveur pour le widget">
        <div class="widget-actions">
          <button id="previewWidget" class="btn btn-outline">Aperçu</button>
          <button id="clearWidget" class="btn" id="clearWidget">Effacer</button>
        </div>
      </div>

      <div id="widgetPreview" class="widget-preview" aria-live="polite">Aucun aperçu — entrez un ID et cliquez sur « Aperçu ».</div>

      <pre class="example" aria-hidden="true">&lt;iframe src="https://discord.com/widget?id=SERVER_ID&amp;theme=dark" width="350" height="500" allowtransparency="true" frameborder="0"&gt;&lt;/iframe&gt;</pre>
    </section>

    <section id="rules" class="container card">
      <h2>Règles rapides</h2>
      <ul>
        <li>Respectez tous les membres.</li>
        <li>Pas de spoilers sans balise, pas de harcèlement.</li>
        <li>Respectez le droit d'auteur pour les images.</li>
      </ul>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container footer-inner">
      <p>Design thème sombre — accents rouges. &copy; <span id="year"></span> Thème Berserk</p>
      <p class="small">N'utilisez pas d'images protégées sans autorisation.</p>
    </div>
  </footer>

  <div id="toast" class="toast" role="status" aria-live="polite" aria-atomic="true"></div>
  <script src="script.js"></script>
</body>
</html>
