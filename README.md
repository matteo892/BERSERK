<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Rejoindre le serveur — Thème Berserk</title>

  <!-- Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:400,600&display=swap" rel="stylesheet">

  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="site-header">
    <div class="container header-inner">
      <a class="brand" href="/" aria-label="Accueil - Thème Berserk">
        <span class="brand-mark" aria-hidden="true">B</span>
        <span class="brand-text">Berserk</span>
      </a>

      <nav class="site-nav" aria-label="Navigation principale">
        <a href="#about">À propos</a>
        <a href="#features">Features</a>
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
          <p class="lead">Rejoignez une communauté dédiée au manga, aux stratégies, aux events et au fan‑art.</p>

          <div class="cta-row" role="group" aria-label="Actions">
            <!-- Remplacez l'attribut data-invite par votre lien complet (ex: https://discord.gg/abcd) -->
            <a id="joinBtn" class="btn btn-primary" href="YOUR_DISCORD_INVITE_HERE" target="_blank" rel="noopener" aria-disabled="false">Rejoindre le serveur</a>

            <button id="copyInvite" class="btn btn-outline" data-invite="YOUR_DISCORD_INVITE_HERE" aria-label="Copier le lien d'invitation">Copier l'invitation</button>
          </div>

          <p class="muted">Préférez-vous un widget ? Activez le "Widget du serveur" et insérez l'ID dans la section Widget ci‑dessous.</p>
        </div>

        <div class="hero-visual" aria-hidden="true">
          <!-- Décor visuel simple -->
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
      <p>Bienvenue sur le serveur inspiré par Berserk — un espace pour discuter du manga, du lore, organiser des parties et participer à des événements communautaires. Respect, bienveillance et consentement obligatoires.</p>

      <div id="features" class="features">
        <article class="feature">
          <h3>Discussions</h3>
          <p>Théories, chapitres, analyses et recommandations.</p>
        </article>
        <article class="feature">
          <h3>Jeux & Events</h3>
          <p>Tournois, soirées jeu et activités communautaires.</p>
        </article>
        <article class="feature">
          <h3>Ressources</h3>
          <p>Guides, fan-art, créations et salons NSFW modérés.</p>
        </article>
      </div>
    </section>

    <section id="widget" class="container card dark">
      <h2>Widget Discord (optionnel)</h2>
      <p>Pour intégrer un aperçu du serveur : activez "Widget du serveur" dans <em>Paramètres du serveur → Widgets</em>, puis saisissez l'ID du serveur ci‑dessous.</p>

      <div class="widget-config">
        <label for="serverId">ID du serveur (SERVER_ID)</label>
        <input id="serverId" name="serverId" placeholder="Entrez l'ID du serveur" aria-label="ID du serveur pour le widget">
        <div class="widget-actions">
          <button id="previewWidget" class="btn btn-outline">Aperçu</button>
          <button id="clearWidget" class="btn">Effacer</button>
        </div>
      </div>

      <div id="widgetPreview" class="widget-preview" aria-live="polite"></div>

      <pre class="example" aria-hidden="true">
&lt;iframe src="https://discord.com/widget?id=SERVER_ID&amp;theme=dark" width="350" height="500" allowtransparency="true" frameborder="0"&gt;&lt;/iframe&gt;
      </pre>
    </section>

    <section id="rules" class="container card">
      <h2>Règles rapides</h2>
      <ul>
        <li>Respectez tous les membres.</li>
        <li>Pas de spoilers sans balise, pas de harcèlement.</li>
        <li>Respectez les règles du droit d'auteur pour les images.</li>
      </ul>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container footer-inner">
      <p>Design thème sombre — accents rouges. &copy; <span id="year"></span> Thème Berserk</p>
      <p class="small">N'utilisez pas d'images protégées sans autorisation.</p>
    </div>
  </footer>

  <!-- Toast notifications -->
  <div id="toast" class="toast" role="status" aria-live="polite" aria-atomic="true"></div>

  <script src="script.js"></script>
</body>
</html>
