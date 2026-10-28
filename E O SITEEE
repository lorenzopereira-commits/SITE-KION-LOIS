<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Kiōn Jiu-Jitsu | Arte Suave em Campinas</title>

  <!-- Google Fonts: Caesar Dressing, Cinzel, Plus Jakarta Sans -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Caesar+Dressing&family=Cinzel:wght@600;700;800&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">

  <style>
    /* ==========================================================================
       TOKENS DE DESIGN & VARIÁVEIS DE COR (Passo 2)
       ========================================================================== */
    :root {
      --bg-obsidian: #08080A;
      --bg-card: #111116;
      --bg-card-hover: #17171e;
      --gold-kion: #C5A059;
      --gold-light: #DFCA9B;
      --gold-bronze: #8A6E2F;
      --graphite: #23232D;
      --text-main: #E2E8F0;
      --text-muted: #94A3B8;

      /* Fontes */
      --font-hero: 'Caesar Dressing', cursive;
      --font-heading: 'Cinzel', serif;
      --font-body: 'Plus Jakarta Sans', sans-serif;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: var(--font-body);
      background-color: var(--bg-obsidian);
      color: var(--text-main);
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* ==========================================================================
       CABEÇALHO & NAVEGAÇÃO
       ========================================================================== */
    header {
      position: sticky;
      top: 0;
      z-index: 1000;
      background-color: rgba(8, 8, 10, 0.95);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--graphite);
      padding: 15px 5%;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
      text-decoration: none;
      color: var(--gold-kion);
    }

    .brand-logo {
      width: 32px;
      height: 42px;
      fill: var(--gold-kion);
    }

    .brand-text {
      font-family: var(--font-heading);
      font-size: 1.4rem;
      font-weight: 700;
      letter-spacing: 2px;
      color: var(--gold-light);
    }

    nav {
      display: flex;
      gap: 24px;
    }

    nav a {
      color: var(--text-main);
      text-decoration: none;
      font-size: 0.95rem;
      font-weight: 500;
      transition: color 0.3s ease;
    }

    nav a:hover {
      color: var(--gold-kion);
    }

    /* ==========================================================================
       HERO SECTION + CARROSSEL HORIZONTAL (Passo 1 & 2)
       ========================================================================== */
    .hero {
      padding: 60px 20px 40px;
      text-align: center;
      max-width: 1100px;
      margin: 0 auto;
    }

    .hero-title {
      font-family: var(--font-hero);
      font-size: 3.5rem;
      color: var(--gold-kion);
      text-shadow: 0 4px 15px rgba(197, 160, 89, 0.2);
      margin-bottom: 10px;
      letter-spacing: 1px;
    }

    .hero-subtitle {
      font-family: var(--font-heading);
      font-size: 1.2rem;
      color: var(--gold-light);
      margin-bottom: 30px;
      letter-spacing: 1px;
    }

    /* Moldura em formato paisagem fixo */
    .slider-wrapper {
      position: relative;
      width: 100%;
      max-width: 850px;
      height: 450px;
      margin: 0 auto;
      overflow: hidden;
      border-radius: 16px;
      border: 1px solid var(--graphite);
      box-shadow: 0 15px 35px rgba(0, 0, 0, 0.7);
    }

    /* Trilha dos slides (4 slides = 400% de largura) */
    .slider-track {
      display: flex;
      width: 400%;
      height: 100%;
      animation: autoSlide 16s cubic-bezier(0.77, 0, 0.175, 1) infinite;
    }

    .slider-wrapper:hover .slider-track {
      animation-play-state: paused;
    }

    .slide-img {
      width: 25%;
      height: 100%;
      object-fit: cover;
      object-position: center;
      display: block;
    }

    @keyframes autoSlide {
      0%, 20% { transform: translateX(0%); }
      25%, 45% { transform: translateX(-25%); }
      50%, 70% { transform: translateX(-50%); }
      75%, 95% { transform: translateX(-75%); }
      100% { transform: translateX(0%); }
    }

    /* ==========================================================================
       SEÇÕES GERAIS
       ========================================================================== */
    section {
      padding: 80px 20px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .section-title {
      font-family: var(--font-heading);
      font-size: 2.2rem;
      color: var(--gold-kion);
      text-align: center;
      margin-bottom: 12px;
    }

    .section-subtitle {
      text-align: center;
      color: var(--text-muted);
      max-width: 600px;
      margin: 0 auto 50px;
      font-size: 1rem;
    }

    /* ==========================================================================
       CARD 3D FLIP - QUADRO DE MODALIDADES & LOJA (Passo 1 & 2)
       ========================================================================== */
    .cards-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 30px;
      justify-items: center;
    }

    /* Container com perspectiva 3D */
    .card-container {
      width: 100%;
      max-width: 320px;
      height: 440px;
      perspective: 1000px;
    }

    /* Elemento interno que gira */
    .card-inner {
      position: relative;
      width: 100%;
      height: 100%;
      text-align: center;
      transition: transform 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      transform-style: preserve-3d;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.5);
      cursor: pointer;
    }

    .card-container:hover .card-inner {
      transform: rotateY(180deg);
    }

    .card-front, .card-back {
      position: absolute;
      width: 100%;
      height: 100%;
      border-radius: 20px;
      overflow: hidden;
      -webkit-backface-visibility: hidden;
      backface-visibility: hidden;
      border: 1px solid var(--graphite);
    }

    /* FRENTE */
    .card-front {
      background-color: var(--bg-card);
    }

    .card-front img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .card-front-title {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      padding: 20px;
      background: linear-gradient(transparent, rgba(8, 8, 10, 0.95));
      font-family: var(--font-heading);
      font-size: 1.3rem;
      font-weight: 700;
      color: var(--gold-light);
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
    }

    .card-icon {
      width: 22px;
      height: 22px;
      fill: var(--gold-kion);
    }

    /* TRÁS */
    .card-back {
      background: linear-gradient(135deg, var(--bg-card), var(--bg-obsidian));
      border: 1px solid var(--gold-kion);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 24px;
      transform: rotateY(180deg);
    }

    .card-back h3 {
      font-family: var(--font-heading);
      font-size: 1.4rem;
      color: var(--gold-kion);
      margin-bottom: 12px;
    }

    .card-back p {
      font-size: 0.95rem;
      line-height: 1.6;
      color: var(--text-muted);
      margin-bottom: 20px;
    }

    .btn-gold {
      display: inline-block;
      padding: 10px 22px;
      background: linear-gradient(135deg, var(--gold-kion), var(--gold-bronze));
      color: #000;
      text-decoration: none;
      font-weight: 700;
      border-radius: 8px;
      transition: all 0.3s ease;
      font-size: 0.9rem;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    .btn-gold:hover {
      background: linear-gradient(135deg, var(--gold-light), var(--gold-kion));
      box-shadow: 0 0 15px rgba(197, 160, 89, 0.4);
    }

    /* ==========================================================================
       HORÁRIOS & GRADE OFICIAL (Melhoria da Hierarquia Visual)
       ========================================================================== */
    .schedule-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 20px;
      margin-top: 30px;
    }

    .schedule-card {
      background-color: var(--bg-card);
      border-left: 4px solid var(--gold-kion);
      padding: 24px;
      border-radius: 8px;
      display: flex;
      align-items: center;
      gap: 16px;
      transition: transform 0.3s ease;
    }

    .schedule-card:hover {
      transform: translateX(5px);
    }

    .schedule-time {
      font-family: var(--font-heading);
      font-size: 1.5rem;
      font-weight: 700;
      color: var(--gold-light);
    }

    .schedule-info h4 {
      font-family: var(--font-heading);
      color: var(--text-main);
      margin-bottom: 4px;
    }

    .schedule-info p {
      font-size: 0.85rem;
      color: var(--text-muted);
    }

    /* ==========================================================================
       GALERIA LIGHTBOX 100% CSS (Passo 1 & 2)
       ========================================================================== */
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
    }

    .gallery-item {
      position: relative;
      border-radius: 12px;
      overflow: hidden;
      cursor: pointer;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.4);
      border: 1px solid var(--graphite);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .gallery-item:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 25px rgba(197, 160, 89, 0.2);
    }

    .gallery-item img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      display: block;
    }

    /* LIGHTBOX MODAL */
    .lightbox {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background-color: rgba(8, 8, 10, 0.85);
      backdrop-filter: blur(8px);
      -webkit-backdrop-filter: blur(8px);
      display: flex;
      justify-content: center;
      align-items: center;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.4s ease;
      z-index: 9999;
    }

    .lightbox:target {
      opacity: 1;
      pointer-events: auto;
    }

    .lightbox-content {
      position: relative;
      max-width: 90%;
      max-height: 85vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      transform: scale(0.8);
      transition: transform 0.4s ease;
    }

    .lightbox:target .lightbox-content {
      transform: scale(1);
    }

    .lightbox-content img {
      max-width: 100%;
      max-height: 80vh;
      border-radius: 12px;
      border: 1px solid var(--gold-kion);
      box-shadow: 0 20px 50px rgba(0, 0, 0, 0.9);
      object-fit: contain;
    }

    .close-btn {
      position: absolute;
      top: -40px;
      right: 0;
      color: var(--gold-light);
      font-size: 2rem;
      text-decoration: none;
      font-weight: bold;
      line-height: 1;
      transition: color 0.2s ease;
    }

    .close-btn:hover {
      color: var(--gold-kion);
    }

    .lightbox-overlay {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      z-index: -1;
    }

    /* ==========================================================================
       RODAPÉ E INFORMAÇÕES DE LOCALIZAÇÃO
       ========================================================================== */
    footer {
      background-color: #040405;
      border-top: 1px solid var(--graphite);
      padding: 50px 20px 30px;
      text-align: center;
    }

    .footer-content {
      max-width: 800px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 16px;
    }

    .address-box {
      display: flex;
      align-items: center;
      gap: 10px;
      color: var(--text-muted);
      font-size: 0.95rem;
    }

    .address-icon {
      width: 20px;
      height: 20px;
      fill: var(--gold-kion);
    }

    .copyright {
      margin-top: 20px;
      font-size: 0.85rem;
      color: #52525b;
    }

    @media (max-width: 768px) {
      .hero-title { font-size: 2.5rem; }
      .slider-wrapper { height: 280px; }
      nav { display: none; }
    }
  </style>
</head>
<body>

  <!-- CABEÇALHO COM A LOGOMARCA PILAR DÓRICO GREGO -->
  <header>
    <a href="#" class="brand">
      <!-- Símbolo Vetorial do Pilar Dórico Grego Kiōn -->
      <svg class="brand-logo" viewBox="0 0 100 130" xmlns="http://www.w3.org/2000/svg">
        <rect x="10" y="10" width="80" height="12" rx="2" />
        <rect x="20" y="22" width="60" height="8" rx="1" />
        <rect x="25" y="30" width="10" height="70" />
        <rect x="45" y="30" width="10" height="70" />
        <rect x="65" y="30" width="10" height="70" />
        <rect x="15" y="100" width="70" height="10" rx="1" />
        <rect x="10" y="110" width="80" height="12" rx="2" />
      </svg>
      <span class="brand-text">KIŌN</span>
    </a>
    <nav>
      <a href="#modalidades">Modalidades</a>
      <a href="#horarios">Horários</a>
      <a href="#loja">Loja VIP</a>
      <a href="#galeria">Galeria</a>
    </nav>
  </header>

  <!-- SEÇÃO HERO COM O CARROSSEL HORIZONTAL -->
  <section class="hero">
    <h1 class="hero-title">Kiōn Jiu-Jitsu</h1>
    <p class="hero-subtitle">Arte Suave • Tradição • Alta Performance em Campinas</p>

    <!-- Componente Carrossel Horizontal Integrado -->
    <div class="slider-wrapper">
      <div class="slider-track">
        <img class="slide-img" src="https://picsum.photos/800/450?random=101" alt="Kiōn Jiu-Jitsu Treino 1">
        <img class="slide-img" src="https://picsum.photos/800/450?random=102" alt="Kiōn Jiu-Jitsu Treino 2">
        <img class="slide-img" src="https://picsum.photos/800/450?random=103" alt="Kiōn Jiu-Jitsu Treino 3">
        <img class="slide-img" src="https://picsum.photos/800/450?random=104" alt="Kiōn Jiu-Jitsu Treino 4">
      </div>
    </div>
  </section>

  <!-- SEÇÃO DE MODALIDADES COM FLIP CARDS 3D -->
  <section id="modalidades">
    <h2 class="section-title">Nossos Programas</h2>
    <p class="section-subtitle">Passe o cursor sobre os cards para virar e explorar a essência do nosso tatame.</p>

    <div class="cards-grid">
      
      <!-- CARD 1: Jiu-Jitsu Adulto -->
      <div class="card-container">
        <div class="card-inner">
          <div class="card-front">
            <img src="https://picsum.photos/400/600?random=201" alt="Jiu-Jitsu Adulto">
            <div class="card-front-title">
              <svg class="card-icon" viewBox="0 0 24 24"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/></svg>
              Jiu-Jitsu Adulto
            </div>
          </div>
          <div class="card-back">
            <h3>Jiu-Jitsu Adulto</h3>
            <p>Do iniciante ao avançado. Metodologia focada na evolução técnica, condicionamento físico e domínio da Arte Suave.</p>
            <a href="#horarios" class="btn-gold">Ver Grade</a>
          </div>
        </div>
      </div>

      <!-- CARD 2: Defesa Pessoal -->
      <div class="card-container">
        <div class="card-inner">
          <div class="card-front">
            <img src="https://picsum.photos/400/600?random=202" alt="Defesa Pessoal">
            <div class="card-front-title">
              <svg class="card-icon" viewBox="0 0 24 24"><path d="M12 1L3 5v6c0 5.55 3.84 10.74 9 12 5.16-1.26 9-6.45 9-12V5l-9-4z"/></svg>
              Defesa Pessoal
            </div>
          </div>
          <div class="card-back">
            <h3>Defesa Pessoal</h3>
            <p>Técnicas reais de reação e controle contra imprevistos cotidianos, aplicáveis a qualquer biotipo.</p>
            <a href="#horarios" class="btn-gold">Conhecer</a>
          </div>
        </div>
      </div>

      <!-- CARD 3: Categoria VIP & Atletas -->
      <div class="card-container">
        <div class="card-inner">
          <div class="card-front">
            <img src="https://picsum.photos/400/600?random=203" alt="Performance VIP">
            <div class="card-front-title">
              <svg class="card-icon" viewBox="0 0 24 24"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
              Atletas VIP
            </div>
          </div>
          <div class="card-back">
            <h3>Programa VIP</h3>
            <p>Acompanhamento personalizado para praticantes exigentes e preparação de atletas de alto rendimento.</p>
            <a href="#loja" class="btn-gold">Saiba Mais</a>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- SEÇÃO DE HORÁRIOS -->
  <section id="horarios">
    <h2 class="section-title">Grade Oficial de Aulas</h2>
    <p class="section-subtitle">Horários fixos para melhor planejamento da sua rotina de treinos.</p>

    <div class="schedule-grid">
      <div class="schedule-card">
        <div class="schedule-time">07:00</div>
        <div class="schedule-info">
          <h4>Treino Matinal</h4>
          <p>Todos os Níveis • Módulo Técnico & Rola</p>
        </div>
      </div>

      <div class="schedule-card">
        <div class="schedule-time">18:30</div>
        <div class="schedule-info">
          <h4>Fundamentos & Defesa</h4>
          <p>Técnicas Básicas, Fugas e Posições Chave</p>
        </div>
      </div>

      <div class="schedule-card">
        <div class="schedule-time">19:45</div>
        <div class="schedule-info">
          <h4>Avançado & Competição</h4>
          <p>Estratégia, Tática de Luta e Sparring Intensivo</p>
        </div>
      </div>
    </div>
  </section>

  <!-- SEÇÃO LOJA KION (FLIP CARDS INTERATIVOS) -->
  <section id="loja">
    <h2 class="section-title">Loja & Armadura Kiōn</h2>
    <p class="section-subtitle">Kimonos e vestuário oficial desenvolvidos com durabilidade extrema.</p>

    <div class="cards-grid">
      
      <!-- PRODUTO 1 -->
      <div class="card-container">
        <div class="card-inner">
          <div class="card-front">
            <img src="https://picsum.photos/400/600?random=301" alt="Kimono Kiōn Gold Edition">
            <div class="card-front-title">
              <svg class="card-icon" viewBox="0 0 24 24"><path d="M12 2L4 5v14.5L12 22l8-2.5V5l-8-3z"/></svg>
              Kimono Gold Edition
            </div>
          </div>
          <div class="card-back">
            <h3>Kimono Gold</h3>
            <p>Trança trançada de 450 GSM com bordados em fio de ouro metálico Kiōn. Modelagem justa e resistente.</p>
            <a href="#" class="btn-gold">Garantir Meu Kimono</a>
          </div>
        </div>
      </div>

      <!-- PRODUTO 2 -->
      <div class="card-container">
        <div class="card-inner">
          <div class="card-front">
            <img src="https://picsum.photos/400/600?random=302" alt="Rashguard No-Gi Obsidiana">
            <div class="card-front-title">
              <svg class="card-icon" viewBox="0 0 24 24"><path d="M12 2L4 5v14.5L12 22l8-2.5V5l-8-3z"/></svg>
              Rashguard Obsidiana
            </div>
          </div>
          <div class="card-back">
            <h3>Rashguard No-Gi</h3>
            <p>Compressão graduada de alta performance, costuras reforçadas e proteção UV50+.</p>
            <a href="#" class="btn-gold">Comprar Agora</a>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- SEÇÃO GALERIA COM LIGHTBOX MODAL 100% CSS -->
  <section id="galeria">
    <h2 class="section-title">Nossa Galeria</h2>
    <p class="section-subtitle">Clique em qualquer imagem para abrir em alta resolução.</p>

    <!-- GRID DA GALERIA -->
    <div class="gallery">
      <a href="#img1" class="gallery-item">
        <img src="https://picsum.photos/800/600?random=401" alt="Foto Tatame Kiōn 1">
      </a>
      <a href="#img2" class="gallery-item">
        <img src="https://picsum.photos/800/600?random=402" alt="Foto Tatame Kiōn 2">
      </a>
      <a href="#img3" class="gallery-item">
        <img src="https://picsum.photos/800/600?random=403" alt="Foto Tatame Kiōn 3">
      </a>
      <a href="#img4" class="gallery-item">
        <img src="https://picsum.photos/800/600?random=404" alt="Foto Tatame Kiōn 4">
      </a>
    </div>

    <!-- ESTRUTURA DOS MODAIS (LIGHTBOX) -->
    <div class="lightbox" id="img1">
      <a href="#galeria" class="lightbox-overlay"></a>
      <div class="lightbox-content">
        <a href="#galeria" class="close-btn">&times;</a>
        <img src="https://picsum.photos/1200/800?random=401" alt="Foto Kiōn Ampliada 1">
      </div>
    </div>

    <div class="lightbox" id="img2">
      <a href="#galeria" class="lightbox-overlay"></a>
      <div class="lightbox-content">
        <a href="#galeria" class="close-btn">&times;</a>
        <img src="https://picsum.photos/1200/800?random=402" alt="Foto Kiōn Ampliada 2">
      </div>
    </div>

    <div class="lightbox" id="img3">
      <a href="#galeria" class="lightbox-overlay"></a>
      <div class="lightbox-content">
        <a href="#galeria" class="close-btn">&times;</a>
        <img src="https://picsum.photos/1200/800?random=403" alt="Foto Kiōn Ampliada 3">
      </div>
    </div>

    <div class="lightbox" id="img4">
      <a href="#galeria" class="lightbox-overlay"></a>
      <div class="lightbox-content">
        <a href="#galeria" class="close-btn">&times;</a>
        <img src="https://picsum.photos/1200/800?random=404" alt="Foto Kiōn Ampliada 4">
      </div>
    </div>
  </section>

  <!-- RODAPÉ E LOCALIZAÇÃO -->
  <footer>
    <div class="footer-content">
      <a href="#" class="brand">
        <svg class="brand-logo" viewBox="0 0 100 130" xmlns="http://www.w3.org/2000/svg">
          <rect x="10" y="10" width="80" height="12" rx="2" />
          <rect x="20" y="22" width="60" height="8" rx="1" />
          <rect x="25" y="30" width="10" height="70" />
          <rect x="45" y="30" width="10" height="70" />
          <rect x="65" y="30" width="10" height="70" />
          <rect x="15" y="100" width="70" height="10" rx="1" />
          <rect x="10" y="110" width="80" height="12" rx="2" />
        </svg>
        <span class="brand-text">KIŌN JIU-JITSU</span>
      </a>

      <div class="address-box">
        <svg class="address-icon" viewBox="0 0 24 24"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>
        <span>Av. Dr. Moraes Salles, 1205 — Nova Campinas, Campinas/SP</span>
      </div>

      <p class="copyright">&copy; Kiōn Jiu-Jitsu. Todos os direitos reservados.</p>
    </div>
  </footer>

</body>
</html>
