<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Elegan Ceria — Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    /* ======================
       Theme variables
       ====================== */
    :root{
      --bg: #fff8fb;
      --card: #ffffff;
      --muted: #6b6b6b;
      --accent-1: #ff8ab6; /* cerah pink */
      --accent-2: #ffd36b; /* soft yellow */
      --accent-3: #76e4a7; /* mint */
      --accent-4: #7cc7ff; /* sky */
      --glass: rgba(255,255,255,0.7);
      --radius: 14px;
      --shadow: 0 8px 24px rgba(20,20,30,0.08);
      --container: 1100px;
    }

    /* ======================
       Reset + base
       ====================== */
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
      background: linear-gradient(180deg, #fff8fb 0%, #f8fbff 100%);
      color:#111;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.5;
      padding-bottom:80px;
    }
    .container{
      max-width:var(--container);
      margin:0 auto;
      padding:0 20px;
    }

    /* ======================
       Header / Navigation
       ====================== */
    header{
      position:sticky;top:12px;z-index:40;
      backdrop-filter: blur(6px);
      display:flex;align-items:center;justify-content:center;
      padding:12px 20px;
    }
    .nav-wrap{
      width:100%;max-width:var(--container);
      display:flex;align-items:center;gap:20px;justify-content:space-between;
    }
    .brand{display:flex;align-items:center;gap:12px}
    .logo{
      width:48px;height:48px;border-radius:12px;display:grid;place-items:center;
      background:linear-gradient(135deg,var(--accent-1),var(--accent-4));box-shadow:var(--shadow);
      color:white;font-weight:700;font-family:'Poppins',sans-serif;
    }
    nav{display:flex;gap:18px;align-items:center}
    nav a{color:#1a1a1a;text-decoration:none;font-weight:600;padding:8px 12px;border-radius:10px}
    nav a:hover{background:rgba(255,255,255,0.6);box-shadow:var(--shadow)}
    .cta{background:linear-gradient(90deg,var(--accent-1),var(--accent-2));padding:9px 14px;border-radius:12px;color:#111;font-weight:700}

    /* Mobile nav */
    .hamburger{display:none;border:0;background:transparent}
    .mobile-menu{display:none}

    /* ======================
       Hero
       ====================== */
    .hero{padding:48px 0 28px}
    .hero-grid{display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center}
    .hero-inner{background:linear-gradient(180deg,var(--glass),rgba(255,255,255,0.5));border-radius:var(--radius);padding:30px;box-shadow:var(--shadow)}
    h1{font-family:'Poppins',sans-serif;font-size:34px;margin:0 0 12px}
    p.lead{margin:0 0 18px;color:var(--muted)}
    .hero-actions{display:flex;gap:12px}

    /* Feature cards */
    .features{display:grid;grid-template-columns:repeat(3,1fr);gap:18px;margin-top:22px}
    .card{background:var(--card);padding:16px;border-radius:12px;box-shadow:var(--shadow);display:flex;gap:12px;align-items:center}
    .icon{width:54px;height:54px;border-radius:10px;display:grid;place-items:center;font-weight:700;color:white}

    /* Gallery */
    .gallery{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-top:26px}
    .hero-img{border-radius:12px;overflow:hidden;box-shadow:var(--shadow)}
    .hero-img img{width:100%;height:100%;display:block;object-fit:cover}

    /* Sections */
    section{padding:36px 0}
    h2{font-family:'Poppins',sans-serif;margin:0 0 8px}

    /* Testimonials */
    .testi{display:grid;grid-template-columns:repeat(2,1fr);gap:18px}

    /* Footer */
    footer{padding:28px 0;background:linear-gradient(180deg,rgba(255,255,255,0.5),transparent)}
    .foot-inner{display:flex;justify-content:space-between;align-items:center;gap:20px}

    /* Responsiveness */
    @media (max-width:1000px){
      .hero-grid{grid-template-columns:1fr 1fr}
      .features{grid-template-columns:repeat(2,1fr)}
      .gallery{grid-template-columns:repeat(2,1fr)}
    }
    @media (max-width:720px){
      nav{display:none}
      .hamburger{display:inline-flex}
      .mobile-menu{display:none}
      .hero-grid{grid-template-columns:1fr}
      .features{grid-template-columns:1fr}
      .testi{grid-template-columns:1fr}
      .gallery{grid-template-columns:1fr}
      .brand{gap:8px}
      h1{font-size:26px}
    }
   


    /* small interactions */
    .float-blob{position:absolute;right:-40px;top:-40px;width:180px;height:180px;border-radius:50%;filter:blur(28px);opacity:0.65}
    .btn-ghost{background:transparent;padding:9px 12px;border-radius:10px;border:1px solid rgba(0,0,0,0.06)}

    /* subtle entrance animations */
    .reveal{opacity:0;transform:translateY(16px);transition:all 700ms cubic-bezier(.2,.9,.2,1)}
    .reveal.show{opacity:1;transform:none}
  </style>
</head>
<body>
  <!-- Header -->
  <header>
    <div class="nav-wrap container">
      <div class="brand">
        <div class="logo">AZ</div>
        <div style="line-height:1">
          <div style="font-weight:700">Elegan Ceria</div>
          <div style="font-size:12px;color:var(--muted)">Website yang cantik & berwarna</div>
        </div>
      </div>

      <nav aria-label="Main Navigation">
        <a href="#home">Home</a>
        <a href="#features">Fitur</a>
        <a href="#gallery">Galeri</a>
        <a href="#contact" class="cta">Kontak</a>
      </nav>

      <!-- Hamburger for mobile -->
      <button class="hamburger" aria-label="menu" id="hamb">
        <svg width="28" height="28" viewBox="0 0 24 24" fill="none"><path d="M4 7h16M4 12h16M4 17h16" stroke="#111" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </button>
    </div>
  </header>

  <main class="container">
    <!-- HERO -->
    <section id="home" class="hero">
      <div class="hero-grid">
        <div class="hero-inner reveal" id="heroLeft">
          <h1>Elegan. Cantik. Ceria.</h1>
          <p class="lead">Sebuah desain yang memadukan keseimbangan estetika elegan dengan palet warna ceria — cocok untuk portfolio, brand, atau toko kecil.
          </p>
          <div class="hero-actions">
            <a class="cta" href="#contact">Mulai Sekarang</a>
            <a class="btn-ghost" href="#features">Lihat Fitur</a>
          </div>

          <div class="features" style="margin-top:20px">
            <div class="card">
              <div class="icon" style="background:linear-gradient(135deg,var(--accent-1),var(--accent-4))">A</div>
              <div>
                <div style="font-weight:700">Desain Elegan</div>
                <div style="font-size:13px;color:var(--muted)">Tipografi bersih & tata letak rapi.</div>
              </div>
            </div>

            <div class="card">
              <div class="icon" style="background:linear-gradient(135deg,var(--accent-3),var(--accent-2))">C</div>
              <div>
                <div style="font-weight:700">Warna Ceria</div>
                <div style="font-size:13px;color:var(--muted)">Palet pastel yang lembut namun hidup.</div>
              </div>
            </div>

            <div class="card">
              <div class="icon" style="background:linear-gradient(135deg,var(--accent-4),var(--accent-3))">R</div>
              <div>
                <div style="font-weight:700">Responsif</div>
                <div style="font-size:13px;color:var(--muted)">Tampil cantik pada semua perangkat.</div>
              </div>
            </div>
          </div>
        </div>

        <div class="hero-img reveal" id="heroRight" style="position:relative">
          <div class="float-blob" style="background:linear-gradient(90deg,var(--accent-1),var(--accent-4))"></div>
          <img src="https://images.unsplash.com/photo-1522771739844-6a9f6d5f14af?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder" alt="Decorative" style="border-radius:12px;max-height:380px;object-fit:cover;width:100%">
        </div>
      </div>
    </section>

    <!-- GALLERY -->
    <section id="gallery">
      <h2>Galeri</h2>
      <p style="color:var(--muted);margin-top:6px">Contoh tampilan kartu & layout grid yang ceria.</p>
      <div class="gallery">
        <div class="card hero-img"><img src="https://images.unsplash.com/photo-1502673530728-f79b4cab31b1?q=80&w=800&auto=format&fit=crop&s=placeholder" alt="image1"></div>
        <div class="card hero-img"><img src="https://images.unsplash.com/photo-1499951360447-b19be8fe80f5?q=80&w=800&auto=format&fit=crop&s=placeholder" alt="image2"></div>
        <div class="card hero-img"><img src="https://images.unsplash.com/photo-1487412947147-5cebf100ffc2?q=80&w=800&auto=format&fit=crop&s=placeholder" alt="image3"></div>
      </div>
    </section>

    <!-- ABOUT / FEATURES -->
    <section id="features">
      <h2>Fitur Utama</h2>
      <p style="color:var(--muted);margin-top:6px">Dibangun untuk tampilan profesional namun penuh warna.</p>
      <div style="display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-top:16px">
        <div class="card">
          <div style="flex:1">
            <div style="font-weight:700">Customizable</div>
            <div style="font-size:13px;color:var(--muted)">Mudah diganti warna, font, dan gambar sesuai brandingmu.</div>
          </div>
        </div>

        <div class="card">
          <div style="flex:1">
            <div style="font-weight:700">Animasi Halus</div>
            <div style="font-size:13px;color:var(--muted)">Animasi ringan untuk kesan elegan tanpa mengganggu.</div>
          </div>
        </div>
      </div>
    </section>

    <!-- TESTIMONIALS -->
    <section>
      <h2>Testimoni</h2>
      <p style="color:var(--muted);margin-top:6px">Apa kata mereka yang sudah coba.</p>
      <div class="testi" style="margin-top:14px">
        <div class="card">
          <div style="font-weight:700">"Desainnya bersih dan sangat menggambarkan brand kami."</div>
          <div style="font-size:13px;color:var(--muted);margin-top:8px">— Ria, Founder</div>
        </div>
        <div class="card">
          <div style="font-weight:700">"Warna-warnanya hidup tapi tetap profesional."</div>
          <div style="font-size:13px;color:var(--muted);margin-top:8px">— Dito, Kreatif</div>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <h2>Kontak</h2>
      <p style="color:var(--muted);margin-top:6px">Tertarik pakai desain ini? Hubungi saya.</p>
      <!-- contact form sederhana (non-functional, contoh markup) -->
      <form style="margin-top:14px;display:grid;gap:12px;max-width:640px">
        <input type="text" placeholder="Nama" style="padding:12px;border-radius:10px;border:1px solid rgba(0,0,0,0.06)">
        <input type="email" placeholder="Email" style="padding:12px;border-radius:10px;border:1px solid rgba(0,0,0,0.06)">
        <textarea placeholder="Pesan" rows="5" style="padding:12px;border-radius:10px;border:1px solid rgba(0,0,0,0.06)"></textarea>
        <div style="display:flex;gap:12px;align-items:center">
          <button type="button" class="cta" onclick="location.href='mailto:azkashofa6@gmail.com?subject=Saya%20tertarik%20dengan%20Elegan%20Ceria'">Kirim via Email</button>
          <span style="color:var(--muted);font-size:13px">Atau langsung email: <strong>azkashofa6@gmail.com</strong></span>
        </div>
      </form>
    </section>
  </main>

  <footer>
    <div class="container foot-inner">
      <div style="display:flex;gap:12px;align-items:center">
        <div class="logo" style="width:40px;height:40px;font-size:14px">EC</div>
        <div>
          <div style="font-weight:700">Elegan Ceria</div>
          <div style="font-size:12px;color:var(--muted)">Didesain untuk tampil elegan & ceria.</div>
        </div>
      </div>
      <div style="color:var(--muted);font-size:13px">© <span id="year"></span> Elegan Ceria</div>
    </div>
  </footer>

  <script>
    // small interactive JS: mobile menu + reveal on load
    const hamb = document.getElementById('hamb');
    hamb && hamb.addEventListener('click', ()=>{
      const nav = document.querySelector('nav');
      if(nav.style.display === 'flex') nav.style.display = '';
      else nav.style.display = 'flex';
    });

    // simple reveal animation when content loads
    window.addEventListener('load', ()=>{
      document.getElementById('heroLeft').classList.add('show');
      document.getElementById('heroRight').classList.add('show');
      document.querySelectorAll('.reveal').forEach((el,i)=> setTimeout(()=>el.classList.add('show'), 140*i));
      document.getElementById('year').textContent = new Date().getFullYear();
    });

    // smooth scrolling for anchor links
    document.querySelectorAll('a[href^="#"]').forEach(link=>{
      link.addEventListener('click', (e)=>{
        e.preventDefault();
        const id = link.getAttribute('href');
        if(id === '#') return;
        const el = document.querySelector(id);
        el && el.scrollIntoView({behavior:'smooth',block:'start'});
      });
    });
  </script>
</body>
</html>
