<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Shormi | Digital Artist & Illustrator</title>
  
  <!-- Google Fonts & Lucide Icons -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400;1,600&family=Plus+Jakarta+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
  <script src="https://unpkg.com/lucide@latest"></script>

  <style>
    :root {
      --bg-color: #f7f0e7;
      --paper-bg: #fffaf5;
      --card-bg: rgba(255, 255, 255, 0.85);
      --card-border: #e6cbcc;
      --text-dark: #33272d;
      --text-muted: #8c7379;
      --accent-pink: #e7a6c7;
      --accent-pink-hover: #d88fb3;
      --dark-banner: #2b1f2d;
      --font-heading: 'Cormorant Garamond', serif;
      --font-body: 'Plus Jakarta Sans', sans-serif;
    }

    [data-theme="dark"] {
      --bg-color: #1a1418;
      --paper-bg: #231b21;
      --card-bg: rgba(45, 33, 41, 0.85);
      --card-border: #4d333f;
      --text-dark: #fcedf3;
      --text-muted: #b89da6;
      --accent-pink: #e08bb6;
      --accent-pink-hover: #cb74a0;
      --dark-banner: #120d11;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      scroll-behavior: smooth;
      transition: background-color 0.3s ease, color 0.3s ease, border-color 0.3s ease;
    }

    body {
      background-color: var(--bg-color);
      color: var(--text-dark);
      font-family: var(--font-body);
      line-height: 1.6;
      overflow-x: hidden;
    }

    .container {
      max-width: 1100px;
      margin: 0 auto;
      padding: 0 1.5rem;
    }

    /* Navbar */
    header {
      position: sticky;
      top: 0;
      background: rgba(247, 240, 231, 0.9);
      backdrop-filter: blur(8px);
      z-index: 100;
      border-bottom: 1px solid var(--card-border);
      padding: 1rem 0;
    }

    [data-theme="dark"] header {
      background: rgba(26, 20, 24, 0.9);
    }

    .nav-wrapper {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .brand-logo {
      font-family: var(--font-heading);
      font-size: 1.8rem;
      font-weight: 600;
      text-decoration: none;
      color: var(--text-dark);
      display: flex;
      align-items: center;
      gap: 0.4rem;
    }

    .nav-links {
      display: flex;
      gap: 1.5rem;
      align-items: center;
      list-style: none;
    }

    .nav-links a {
      text-decoration: none;
      color: var(--text-dark);
      font-size: 0.9rem;
      font-weight: 500;
      transition: color 0.2s ease;
    }

    .nav-links a:hover {
      color: var(--accent-pink);
    }

    .theme-btn {
      background: none;
      border: none;
      cursor: pointer;
      color: var(--text-dark);
      display: flex;
      align-items: center;
    }

    /* Hero Section */
    .hero {
      padding: 4rem 0;
      background: var(--paper-bg);
      border-bottom: 1px solid var(--card-border);
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 3rem;
      align-items: center;
    }

    @media (max-width: 768px) {
      .hero-grid { grid-template-columns: 1fr; text-align: center; }
      .hero-socials { justify-content: center; }
    }

    .hero-greeting {
      font-size: 0.85rem;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--text-muted);
      margin-bottom: 0.5rem;
    }

    .hero-title {
      font-family: var(--font-heading);
      font-size: 3.8rem;
      font-weight: 600;
      line-height: 1.1;
      margin-bottom: 0.8rem;
    }

    .hero-subtitle {
      font-size: 1rem;
      color: var(--text-muted);
      margin-bottom: 1.2rem;
      font-weight: 500;
    }

    .hero-text {
      color: var(--text-dark);
      font-size: 1rem;
      margin-bottom: 2rem;
      max-width: 450px;
    }

    .btn-main {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.8rem 1.6rem;
      background: var(--dark-banner);
      color: #ffffff;
      text-decoration: none;
      border-radius: 99px;
      font-size: 0.9rem;
      font-weight: 500;
      border: none;
      cursor: pointer;
      transition: transform 0.2s ease, opacity 0.2s ease;
    }

    .btn-main:hover {
      opacity: 0.9;
      transform: translateY(-2px);
    }

    .hero-image-box {
      position: relative;
      border-radius: 20px;
      overflow: hidden;
      box-shadow: 0 15px 35px rgba(0,0,0,0.08);
      max-height: 480px;
    }

    .hero-image-box img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .hero-caption {
      position: absolute;
      bottom: 1rem;
      right: 1rem;
      background: rgba(255, 255, 255, 0.75);
      backdrop-filter: blur(6px);
      padding: 0.4rem 0.8rem;
      border-radius: 12px;
      font-family: var(--font-heading);
      font-style: italic;
      font-size: 0.85rem;
      color: #333;
    }

    .hero-socials {
      display: flex;
      gap: 1rem;
      margin-top: 1.8rem;
    }

    .social-icon {
      color: var(--text-dark);
      transition: color 0.2s ease;
    }

    .social-icon:hover { color: var(--accent-pink); }

    /* About Section */
    .about-section {
      padding: 5rem 0;
    }

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 3.5rem;
      align-items: center;
    }

    @media (max-width: 768px) {
      .about-grid { grid-template-columns: 1fr; }
    }

    .section-title {
      font-family: var(--font-heading);
      font-size: 2.5rem;
      font-weight: 600;
      margin-bottom: 1.2rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .about-desc {
      color: var(--text-dark);
      font-size: 0.98rem;
      margin-bottom: 1.2rem;
    }

    .about-gallery-collage {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1rem;
    }

    .collage-img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 16px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.06);
    }

    /* Portfolio Section */
    .portfolio-section {
      padding: 5rem 0;
      background: var(--paper-bg);
      border-top: 1px solid var(--card-border);
      border-bottom: 1px solid var(--card-border);
    }

    .portfolio-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 2rem;
      flex-wrap: wrap;
      gap: 1rem;
    }

    .controls-bar {
      display: flex;
      gap: 1rem;
      align-items: center;
      flex-wrap: wrap;
    }

    .search-box {
      position: relative;
    }

    .search-box input {
      padding: 0.5rem 1rem 0.5rem 2.2rem;
      border-radius: 99px;
      border: 1px solid var(--card-border);
      background: var(--bg-color);
      color: var(--text-dark);
      font-family: var(--font-body);
      font-size: 0.85rem;
      outline: none;
    }

    .search-box i {
      position: absolute;
      left: 0.75rem;
      top: 50%;
      transform: translateY(-50%);
      color: var(--text-muted);
      width: 16px;
      height: 16px;
    }

    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
      gap: 1.5rem;
    }

    .art-card {
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 6px 18px rgba(0,0,0,0.04);
      position: relative;
      cursor: pointer;
      transition: transform 0.3s ease;
    }

    .art-card:hover {
      transform: translateY(-5px);
    }

    .art-img-box {
      width: 100%;
      height: 250px;
      overflow: hidden;
      background: #f0f0f0;
    }

    .art-img-box img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.5s ease;
    }

    .art-card:hover .art-img-box img {
      transform: scale(1.05);
    }

    .art-info {
      padding: 1rem;
    }

    .art-title {
      font-family: var(--font-heading);
      font-size: 1.25rem;
      font-weight: 600;
    }

    .art-category {
      font-size: 0.75rem;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.08em;
    }

    .card-actions {
      position: absolute;
      top: 0.6rem;
      right: 0.6rem;
      display: flex;
      gap: 0.4rem;
      opacity: 0;
      transition: opacity 0.2s ease;
    }

    .art-card:hover .card-actions { opacity: 1; }

    .btn-icon-sm {
      width: 30px;
      height: 30px;
      border-radius: 50%;
      border: none;
      background: rgba(255, 255, 255, 0.9);
      color: #e53935;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 2px 8px rgba(0,0,0,0.15);
    }

    /* Shop & Banner Section */
    .shop-section {
      padding: 5rem 0;
    }

    .shop-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2rem;
    }

    @media (max-width: 768px) {
      .shop-grid { grid-template-columns: 1fr; }
    }

    .shop-card {
      background: var(--paper-bg);
      border: 1px solid var(--card-border);
      border-radius: 20px;
      padding: 2.5rem;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: flex-start;
      gap: 1rem;
    }

    .banner-card {
      background: linear-gradient(135deg, #f0d7e2 0%, #e7a6c7 100%);
      border-radius: 20px;
      padding: 2.5rem;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: #33272d;
    }

    /* Footer */
    footer {
      background: var(--dark-banner);
      color: #ffffff;
      padding: 4rem 0 2rem;
    }

    .footer-grid {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr;
      gap: 3rem;
      margin-bottom: 3rem;
    }

    @media (max-width: 768px) {
      .footer-grid { grid-template-columns: 1fr; }
    }

    .footer-brand h2 {
      font-family: var(--font-heading);
      font-size: 2.2rem;
      margin-bottom: 0.5rem;
    }

    .footer-sub {
      color: #b8a3ad;
      font-size: 0.85rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      margin-bottom: 1.5rem;
    }

    .footer-links h4 {
      font-size: 0.95rem;
      margin-bottom: 1rem;
      color: #e7a6c7;
    }

    .footer-links ul {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
    }

    .footer-links a {
      color: #d1c0c7;
      text-decoration: none;
      font-size: 0.88rem;
    }

    .footer-links a:hover { color: #ffffff; }

    .footer-bottom {
      border-top: 1px solid rgba(255,255,255,0.1);
      padding-top: 1.5rem;
      text-align: center;
      font-size: 0.8rem;
      color: #8c7379;
    }

    /* Modals */
    .modal {
      position: fixed;
      top: 0; left: 0; width: 100%; height: 100%;
      background: rgba(0,0,0,0.5);
      backdrop-filter: blur(8px);
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 1.5rem;
      z-index: 1000;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.3s ease;
    }

    .modal.active { opacity: 1; pointer-events: auto; }

    .modal-box {
      background: var(--paper-bg);
      border: 1px solid var(--card-border);
      border-radius: 20px;
      padding: 2rem;
      max-width: 500px;
      width: 100%;
      position: relative;
    }

    .close-btn {
      position: absolute;
      top: 1rem; right: 1rem;
      background: none; border: none;
      cursor: pointer;
      color: var(--text-dark);
    }

    .form-group {
      display: flex;
      flex-direction: column;
      gap: 0.4rem;
      margin-bottom: 1rem;
    }

    .form-group label { font-size: 0.85rem; font-weight: 600; }

    .form-group input, .form-group textarea, .form-group select {
      padding: 0.65rem 0.9rem;
      border-radius: 10px;
      border: 1px solid var(--card-border);
      background: var(--bg-color);
      color: var(--text-dark);
      font-family: var(--font-body);
      outline: none;
    }
  </style>
</head>
<body>

  <!-- Navigation -->
  <header>
    <div class="container nav-wrapper">
      <a href="#" class="brand-logo">🌷 Shormi</a>
      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#portfolio">Portfolio</a></li>
        <li><a href="#shop">Shop</a></li>
        <li><a href="#contact">Contact</a></li>
        <li>
          <button class="theme-btn" id="themeToggle" title="Toggle Theme">
            <i data-lucide="moon" id="themeIcon"></i>
          </button>
        </li>
      </ul>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero" id="home">
    <div class="container hero-grid">
      <div>
        <p class="hero-greeting">HELLO, I'M</p>
        <h1 class="hero-title">Shormi 🌷</h1>
        <p class="hero-subtitle">Digital Artist • Illustrator • Dreamer</p>
        <p class="hero-text">
          I create art that tells quiet stories — about emotions, nature, and the little moments in between.
        </p>
        <a href="#portfolio" class="btn-main">
          <span>View My Art</span>
          <i data-lucide="arrow-right" style="width: 16px;"></i>
        </a>
        <div class="hero-socials">
          <a href="https://www.instagram.com/0__skyblue__0?exln=eWQyeGI3ZmN4ZWJh" target="_blank" class="social-icon"><i data-lucide="instagram"></i></a>
          <a href="https://pin.it/4tmz3bq91" target="_blank" class="social-icon"><i data-lucide="pin"></i></a>
        </div>
      </div>
      <div class="hero-image-box">
        <img src="https://images.unsplash.com/photo-1518709268805-4e9042af9f23?auto=format&fit=crop&w=800&q=80" alt="Shormi Art" />
        <span class="hero-caption">Same sky, different dreams. ♡</span>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section class="about-section" id="about">
    <div class="container about-grid">
      <div>
        <h2 class="section-title">🌷 About Me</h2>
        <p class="about-desc">
          Hi! I'm Shormi (Sadia Ferdosi Shormi). I'm a Bangladeshi artist, currently studying BBA, and I create digital art, illustrations, and designs.
        </p>
        <p class="about-desc">
          I'm inspired by the sky, nature, cats, dark romance, and the beauty in small, quiet moments. Through my art, I try to express emotions, tell stories, and create worlds where people can feel seen.
        </p>
        <a href="#contact" class="btn-main" style="margin-top: 1rem;">
          <span>Get in Touch</span>
        </a>
      </div>
      <div class="about-gallery-collage">
        <img src="1000078651.jpg" alt="Sky Kid Fanart" class="collage-img" />
        <img src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=600&q=80" alt="Tulip Art" class="collage-img" />
      </div>
    </div>
  </section>

  <!-- Portfolio Section -->
  <section class="portfolio-section" id="portfolio">
    <div class="container">
      <div class="portfolio-header">
        <div>
          <h2 class="section-title">🌷 My Work</h2>
          <p style="color: var(--text-muted); font-size: 0.9rem;">Illustrations • Digital Art • Character Art • Designs</p>
        </div>
        
        <div class="controls-bar">
          <div class="search-box">
            <i data-lucide="search"></i>
            <input type="text" id="searchInput" placeholder="Search artwork..." />
          </div>
          <button class="btn-main" id="openUploadBtn">
            <i data-lucide="plus" style="width: 16px;"></i>
            <span>Add Artwork</span>
          </button>
        </div>
      </div>

      <div class="gallery-grid" id="galleryGrid">
        <!-- Gallery cards loaded dynamically via JS -->
      </div>
    </div>
  </section>

  <!-- Shop & Banner Section -->
  <section class="shop-section" id="shop">
    <div class="container shop-grid">
      <div class="shop-card">
        <h3 style="font-family: var(--font-heading); font-size: 2rem;">Shop My Art 🌷</h3>
        <p style="color: var(--text-muted); font-size: 0.9rem;">
          Support my work by visiting my Ko-fi shop for prints, digital downloads, and more.
        </p>
        <a href="https://ko-fi.com" target="_blank" class="btn-main" style="background: var(--accent-pink); color: #fff;">
          <span>Visit Ko-fi</span>
          <i data-lucide="coffee" style="width: 16px;"></i>
        </a>
      </div>

      <div class="banner-card">
        <h3 style="font-family: var(--font-heading); font-size: 2.2rem; font-style: italic;">Thank you for being here ♡</h3>
      </div>
    </div>
  </section>

  <!-- Footer / Contact Section -->
  <footer id="contact">
    <div class="container">
      <div class="footer-grid">
        <div class="footer-brand">
          <h2>🌷 Shormi</h2>
          <p class="footer-sub">Art • Creativity • Freedom</p>
        </div>
        <div class="footer-links">
          <h4>Quick Links</h4>
          <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#portfolio">Portfolio</a></li>
            <li><a href="#shop">Shop</a></li>
          </ul>
        </div>
        <div class="footer-links">
          <h4>Let's Connect</h4>
          <div style="display: flex; gap: 0.8rem; margin-top: 0.5rem;">
            <a href="https://www.instagram.com/0__skyblue__0?exln=eWQyeGI3ZmN4ZWJh" target="_blank"><i data-lucide="instagram"></i></a>
            <a href="https://pin.it/4tmz3bq91" target="_blank"><i data-lucide="pin"></i></a>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <p>© 2026 Shormi. All rights reserved. | Made with ♡</p>
      </div>
    </div>
  </footer>

  <!-- Add Artwork Modal -->
  <div class="modal" id="uploadModal">
    <div class="modal-box">
      <button class="close-btn" id="closeUploadBtn"><i data-lucide="x"></i></button>
      <h3 style="font-family: var(--font-heading); font-size: 1.8rem; margin-bottom: 1rem;">Add Artwork 🌷</h3>
      <form id="uploadForm">
        <div class="form-group">
          <label>Artwork Image File</label>
          <input type="file" id="artFile" accept="image/*" required />
        </div>
        <div class="form-group">
          <label>Title</label>
          <input type="text" id="artTitle" placeholder="e.g. My Sky Kid" required />
        </div>
        <div class="form-group">
          <label>Category</label>
          <select id="artCategory">
            <option value="Character">Character Art</option>
            <option value="Digital Art">Digital Art</option>
            <option value="Illustration">Illustration</option>
          </select>
        </div>
        <button type="submit" class="btn-main" style="width: 100%; justify-content: center; margin-top: 1rem;">
          Upload Artwork
        </button>
      </form>
    </div>
  </div>

  <script>
    // Initial Default Artworks (including your Sky Kid fanart!)
    const initialArtworks = [
      {
        id: '1',
        title: 'Spooky Sky Kid',
        category: 'Character',
        image: '1000078651.jpg'
      },
      {
        id: '2',
        title: 'Starlight Witch & Pumpkin',
        category: 'Illustration',
        image: 'https://images.unsplash.com/photo-1518709268805-4e9042af9f23?auto=format&fit=crop&w=600&q=80'
      },
      {
        id: '3',
        title: 'Floral Moon Night',
        category: 'Digital Art',
        image: 'https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=600&q=80'
      }
    ];

    let artworks = JSON.parse(localStorage.getItem('shormi_portfolio')) || initialArtworks;
    let searchQuery = '';

    const galleryGrid = document.getElementById('galleryGrid');
    const searchInput = document.getElementById('searchInput');

    function renderGallery() {
      galleryGrid.innerHTML = '';
      const filtered = artworks.filter(art => 
        art.title.toLowerCase().includes(searchQuery.toLowerCase()) ||
        art.category.toLowerCase().includes(searchQuery.toLowerCase())
      );

      filtered.forEach(art => {
        const card = document.createElement('div');
        card.className = 'art-card';
        card.innerHTML = `
          <div class="card-actions">
            <button class="btn-icon-sm" onclick="deleteArtwork(event, '${art.id}')" title="Delete Artwork">
              <i data-lucide="trash-2" style="width:14px;"></i>
            </button>
          </div>
          <div class="art-img-box">
            <img src="${art.image}" alt="${art.title}" loading="lazy" />
          </div>
          <div class="art-info">
            <span class="art-category">${art.category}</span>
            <h3 class="art-title">${art.title}</h3>
          </div>
        `;
        galleryGrid.appendChild(card);
      });
      lucide.createIcons();
    }

    window.deleteArtwork = function(e, id) {
      e.stopPropagation();
      if (confirm('Delete this artwork from gallery?')) {
        artworks = artworks.filter(item => item.id !== id);
        localStorage.setItem('shormi_portfolio', JSON.stringify(artworks));
        renderGallery();
      }
    };

    // Upload Handler
    const uploadModal = document.getElementById('uploadModal');
    document.getElementById('openUploadBtn').addEventListener('click', () => uploadModal.classList.add('active'));
    document.getElementById('closeUploadBtn').addEventListener('click', () => uploadModal.classList.remove('active'));

    document.getElementById('uploadForm').addEventListener('submit', (e) => {
      e.preventDefault();
      const fileInput = document.getElementById('artFile');
      const title = document.getElementById('artTitle').value;
      const category = document.getElementById('artCategory').value;

      if (fileInput.files && fileInput.files[0]) {
        const reader = new FileReader();
        reader.onload = function(evt) {
          const newArt = {
            id: Date.now().toString(),
            title: title,
            category: category,
            image: evt.target.result
          };
          artworks.unshift(newArt);
          localStorage.setItem('shormi_portfolio', JSON.stringify(artworks));
          renderGallery();
          uploadModal.classList.remove('active');
          document.getElementById('uploadForm').reset();
        };
        reader.readAsDataURL(fileInput.files[0]);
      }
    });

    searchInput.addEventListener('input', (e) => {
      searchQuery = e.target.value;
      renderGallery();
    });

    // Theme Switcher
    document.getElementById('themeToggle').addEventListener('click', () => {
      const isDark = document.body.getAttribute('data-theme') === 'dark';
      document.body.toggleAttribute('data-theme', !isDark);
      document.getElementById('themeIcon').setAttribute('data-lucide', isDark ? 'moon' : 'sun');
      lucide.createIcons();
    });

    renderGallery();
  </script>
</body>
</html>
