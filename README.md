<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Bem Universitas Lumajang</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet" />
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet" />
  <style>
    /* Reset & base */
    *, *::before, *::after {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: 'Inter', sans-serif;
      background: #f9fafb;
      color: #1f2937;
      line-height: 1.6;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }
    a {
      text-decoration: none;
      color: inherit;
      cursor: pointer;
    }
    img {
      max-width: 100%;
      display: block;
    }

    /* Container */
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 24px;
      width: 100%;
    }

    /* Header */
    header {
      background-color: #2563eb;
      color: white;
      padding: 24px 0;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 6px rgb(0 0 0 / 0.1);
    }
    .header-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 16px;
    }
    .logo {
      font-weight: 800;
      font-size: 1.5rem;
      letter-spacing: 2px;
      user-select: none;
    }
    nav {
      display: none;
    }
    .menu-toggle {
      background: none;
      border: none;
      color: white;
      font-size: 32px;
      cursor: pointer;
      display: flex;
      align-items: center;
    }

    /* Mobile menu */
    nav.mobile-menu {
      display: none;
      flex-direction: column;
      background-color: #1e40af;
      padding: 16px 0;
    }
    nav.mobile-menu a {
      color: white;
      padding: 12px 24px;
      border-top: 1px solid rgba(255 255 255 / 0.1);
      font-weight: 600;
      transition: background-color 0.3s ease;
    }
    nav.mobile-menu a:hover,
    nav.mobile-menu a:focus {
      background-color: #3b82f6;
      outline: none;
    }
    nav.mobile-menu.show {
      display: flex;
    }

    /* Desktop Navigation */
    @media(min-width: 768px) {
      nav.mobile-menu {
        display: none !important;
      }
      nav.desktop-menu {
        display: flex;
        gap: 28px;
      }
      nav.desktop-menu a {
        color: white;
        font-weight: 600;
        padding: 8px 12px;
        border-radius: 6px;
        transition: background-color 0.3s ease;
      }
      nav.desktop-menu a:hover,
      nav.desktop-menu a:focus {
        background-color: #3b82f6;
        outline: none;
      }
      .menu-toggle {
        display: none;
      }
    }

    /* Hero Section */
    .hero {
      background: linear-gradient(135deg, #3b82f6, #2563eb);
      color: white;
      padding: 100px 24px 120px;
      text-align: center;
      user-select: none;
    }
    .hero h1 {
      font-size: 3rem;
      font-weight: 800;
      margin-bottom: 16px;
      line-height: 1.1;
      max-width: 700px;
      margin-left: auto;
      margin-right: auto;
    }
    .hero p {
      font-size: 1.25rem;
      max-width: 600px;
      margin-left: auto;
      margin-right: auto;
      margin-bottom: 40px;
      opacity: 0.9;
    }
    .btn-primary {
      background-color: #2563eb;
      border: none;
      padding: 16px 40px;
      border-radius: 12px;
      font-weight: 700;
      font-size: 1.1rem;
      color: white;
      user-select: none;
      cursor: pointer;
      box-shadow: 0 8px 16px rgb(37 99 235 / 0.4);
      transition: background-color 0.3s ease, box-shadow 0.3s ease;
    }
    .btn-primary:hover,
    .btn-primary:focus {
      background-color: #1e40af;
      box-shadow: 0 12px 32px rgb(37 99 235 / 0.6);
      outline: none;
    }

    /* Section */
    section {
      padding: 80px 0;
    }
    section h2 {
      font-size: 2rem;
      font-weight: 700;
      margin-bottom: 32px;
      text-align: center;
      user-select: none;
    }

    /* Cards Grid */
    .cards-grid {
      display: grid;
      gap: 32px;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      max-width: 1100px;
      margin-left: auto;
      margin-right: auto;
    }
    .card {
      background: white;
      padding: 32px 24px;
      border-radius: 16px;
      box-shadow: 0 5px 12px rgb(0 0 0 / 0.1);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      user-select: none;
      display: flex;
      flex-direction: column;
      gap: 12px;
    }
    .card:hover,
    .card:focus-within {
      transform: translateY(-6px);
      box-shadow: 0 12px 30px rgb(0 0 0 / 0.15);
      outline: none;
    }
    .card-icon {
      font-family: 'Material Icons';
      font-size: 48px;
      color: #2563eb;
      margin-bottom: 12px;
      user-select: none;
    }
    .card-title {
      font-weight: 700;
      font-size: 1.2rem;
      color: #1f2937;
      user-select: text;
    }
    .card-description {
      color: #4b5563;
      font-size: 1rem;
      flex-grow: 1;
      user-select: text;
    }

    /* Footer */
    footer {
      background: #1f2937;
      color: #9ca3af;
      padding: 40px 24px;
      text-align: center;
      user-select: none;
    }
    footer p {
      margin: 0;
      font-size: 0.9rem;
    }

    /* Accessibility focus */
    a:focus-visible,
    button:focus-visible,
    .card:focus-visible {
      outline: 3px solid #2563eb;
      outline-offset: 2px;
    }
  </style>
</head>
<body>

<header role="banner">
  <div class="container header-inner">
    <div class="logo" aria-label="Logo BEM Kampus" tabindex="0">BEM Universitas Lumajang</div>
    <nav class="desktop-menu" aria-label="Navigasi Utama">
      <a href="#home" tabindex="0">Beranda</a>
      <a href="#program" tabindex="0">Program Kerja</a>
      <a href="#about" tabindex="0">Tentang Kami</a>
      <a href="#contact" tabindex="0">Kontak</a>
    </nav>
    <button class="menu-toggle" aria-label="Buka menu navigasi" aria-expanded="false" aria-controls="mobile-menu" id="menuToggle">&#9776;</button>
  </div>
  <nav id="mobile-menu" class="mobile-menu" aria-label="Navigasi Mobile" role="menu" tabindex="-1">
    <a href="#home" role="menuitem" tabindex="-1">Beranda</a>
    <a href="#program" role="menuitem" tabindex="-1">Program Kerja</a>
    <a href="#about" role="menuitem" tabindex="-1">Tentang Kami</a>
    <a href="#contact" role="menuitem" tabindex="-1">Kontak</a>
  </nav>
</header>

<main>
  <section class="hero" id="home" role="region" aria-label="Sambutan BEM Kampus">
    <h1>Selamat Datang di Website Resmi BEM Kampus</h1>
    <p>Mewadahi aspirasi mahasiswa, membangun semangat perubahan, dan menginspirasi kampus kita.</p>
    <button class="btn-primary" onclick="document.getElementById('program').scrollIntoView({behavior:'smooth'})">Lihat Program Kerja</button>
  </section>

  <section id="program" role="region" aria-label="Program Kerja BEM Kampus">
    <h2>Program Kerja Unggulan</h2>
    <div class="cards-grid">
      <article class="card" tabindex="0" aria-labelledby="prog1-title">
        <span class="card-icon" aria-hidden="true">campaign</span>
        <h3 class="card-title" id="prog1-title">Pengelolaan Media Sosial</h3>
        <p class="card-description">Meningkatkan komunikasi melalui media sosial dengan konten berkualitas dan interaktif bagi mahasiswa.</p>
      </article>
      <article class="card" tabindex="0" aria-labelledby="prog2-title">
        <span class="card-icon" aria-hidden="true">language</span>
        <h3 class="card-title" id="prog2-title">Menjalin Kerja Sama</h3>
        <p class="card-description">Membangun kerja sama dengan organisasi eksternal, seperti lembaga pemerintah, NGO, dan perusahaan, untuk mendukung program-program BEM.</p>
      </article>
      <article class="card" tabindex="0" aria-labelledby="prog3-title">
        <span class="card-icon" aria-hidden="true">school</span>
        <h3 class="card-title" id="prog3-title">Pelatihan Jurnalistik</h3>
        <p class="card-description">Memberikan pelatihan jurnalistik agar mahasiswa lebih terampil dalam menyampaikan berita dan informasi.</p>
      </article>
      <article class="card" tabindex="0" aria-labelledby="prog4-title">
        <span class="card-icon" aria-hidden="true">record_voice_over</span>
        <h3 class="card-title" id="prog4-title">Webinar dan Diskusi Publik</h3>
        <p class="card-description">Menyelenggarakan edukasi terbuka mengenai berbagai isu penting di lingkungan kampus dan masyarakat.</p>
      </article>
      <article class="card" tabindex="0" aria-labelledby="prog5-title">
        <span class="card-icon" aria-hidden="true">feedback</span>
        <h3 class="card-title" id="prog5-title">Survey Aspirasi Mahasiswa</h3>
        <p class="card-description">Mengumpulkan dan menindaklanjuti aspirasi mahasiswa untuk mewujudkan kampus yang lebih baik.</p>
      </article>
      <article class="card" tabindex="0" aria-labelledby="prog6-title">
        <span class="card-icon" aria-hidden="true">human</span>
        <h3 class="card-title" id="prog6-title">Meningkatkan Kualitas Mahasiswa</h3>
        <p class="card-description">Mengadakan program-program yang bertujuan untuk meningkatkan kualitas akademik dan soft skills mahasiswa, seperti pelatihan kepemimpinan, manajemen waktu, dan keterampilan komunikasi.</p>
    </div>
  </section>

  <section id="about" role="region" aria-label="Tentang BEM Kampus">
    <div class="container">
      <h2>Tentang BEM Kampus</h2>
      <p style="max-width: 700px; margin: 0 auto; font-size: 1.1rem; color: #374151; user-select:text;">
        BEM Kampus adalah organisasi mahasiswa yang berperan sebagai wahana aspirasi, pengembangan potensi mahasiswa,
        serta fasilitator berbagai kegiatan yang membangun kualitas akademik dan sosial kampus. Kami berkomitmen untuk
        menghubungkan mahasiswa dengan kampus dan masyarakat melalui program-program inovatif dan komunikasi efektif.
      </p>
    </div>
  </section>

  <section id="contact" role="region" aria-label="Kontak BEM Kampus">
    <div class="container">
      <h2>Kontak Kami</h2>
      <p style="text-align:center; margin-bottom: 32px; color:#374151; user-select:text;">
        Untuk pertanyaan, saran, atau bergabung bersama kami, silakan hubungi:
      </p>
      <div style="max-width: 480px; margin: 0 auto; display:grid; gap:16px; font-size:1rem; color:#1e293b; user-select:text;">
        <div><span class="material-icons" aria-hidden="true" style="vertical-align:middle; color:#2563eb;">email</span> Email: <a href="mailto:dhikakuntull@gmail.com">dhikakuntull@gmail.com</a></div>
        <div><span class="material-icons" aria-hidden="true" style="vertical-align:middle; color:#2563eb;">local_phone</span> Telepon: <a href="tel:+6281240091012">+62 812 4009 1012</a></div>
        <div><span class="material-icons" aria-hidden="true" style="vertical-align:middle; color:#2563eb;">location_on</span> Alamat: Gedung A, Universitas Contoh, Jl. Pendidikan No.1</div>
      </div>
    </div>
  </section>
</main>

<footer role="contentinfo">
  <p>© 2024 BEM Kampus. All rights reserved.</p>
</footer>

<script>
  (() => {
    const menuToggle = document.getElementById('menuToggle');
    const mobileMenu = document.getElementById('mobile-menu');
    let menuOpen = false;

    menuToggle.addEventListener('click', () => {
      menuOpen = !menuOpen;
      mobileMenu.classList.toggle('show', menuOpen);
      menuToggle.setAttribute('aria-expanded', menuOpen);
      if (menuOpen) {
        mobileMenu.querySelector('a').focus();
      }
    });

    // Close mobile menu on click outside or pressing Escape
    document.addEventListener('click', (e) => {
      if (menuOpen && !mobileMenu.contains(e.target) && e.target !== menuToggle) {
        menuOpen = false;
        mobileMenu.classList.remove('show');
        menuToggle.setAttribute('aria-expanded', 'false');
      }
    });

    document.addEventListener('keydown', (e) => {
      if (e.key === 'Escape' && menuOpen) {
        menuOpen = false;
        mobileMenu.classList.remove('show');
        menuToggle.setAttribute('aria-expanded', 'false');
        menuToggle.focus();
      }
    });
  })();
</script>
</body>
</html>

