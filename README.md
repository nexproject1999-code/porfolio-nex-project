<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#f5f5f2">
  <meta name="description" content="NEX AI membantu UMKM memakai teknologi yang sesuai kebutuhan usaha, dari website hingga proses kerja yang lebih praktis.">
  <title>NEX AI — Teknologi untuk usaha</title>
  <style>
    :root{
      --paper:#f5f5f2;--white:#fff;--ink:#111;--muted:#666762;--line:#d9d9d3;
      --dark:#111;--darkmuted:#b8b8b2;--radius:22px;--max:1160px;
      --ease:cubic-bezier(.2,.75,.25,1)
    }
    *{box-sizing:border-box}
    html{scroll-behavior:smooth;scroll-padding-top:90px}
    body{margin:0;background:var(--paper);color:var(--ink);font-family:Inter,ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif;line-height:1.6;-webkit-font-smoothing:antialiased}
    a{color:inherit;text-decoration:none}
    button{font:inherit}
    ::selection{background:#111;color:#fff}
    .wrap{width:min(var(--max),calc(100% - 48px));margin-inline:auto}
    .nav-shell{position:sticky;top:0;z-index:20;background:rgba(245,245,242,.88);backdrop-filter:blur(18px);border-bottom:1px solid rgba(17,17,17,.08)}
    .nav{height:76px;display:flex;align-items:center;justify-content:space-between;gap:24px}
    .brand{display:inline-flex;align-items:center;gap:11px;font-weight:800;letter-spacing:-.06em;font-size:21px}
    .brand-mark{width:34px;height:34px;background:var(--ink);color:white;border-radius:10px;display:grid;place-items:center;font-size:14px;letter-spacing:-.08em;position:relative;overflow:hidden}
    .brand-mark:after{content:"";position:absolute;width:38px;height:1px;background:#fff;transform:rotate(-48deg);opacity:.9}
    .brand small{display:block;font-weight:500;letter-spacing:.12em;font-size:9px;color:var(--muted);line-height:1.2;margin-top:2px}
    .nav-links{display:flex;align-items:center;gap:30px;font-size:13px;color:#444}
    .nav-links a:not(.nav-cta):hover{color:#000}
    .nav-cta,.button{display:inline-flex;align-items:center;justify-content:center;gap:10px;border:1px solid var(--ink);border-radius:999px;padding:12px 18px;font-size:13px;font-weight:650;transition:background .25s,color .25s,transform .25s var(--ease)}
    .nav-cta,.button.dark{background:var(--ink);color:white}
    .nav-cta:hover,.button.dark:hover{background:#333;transform:translateY(-2px)}
    .button.light{background:transparent;color:var(--ink)}
    .button.light:hover{background:var(--ink);color:white;transform:translateY(-2px)}
    .menu-btn{display:none;background:none;border:1px solid var(--line);border-radius:50%;height:42px;width:42px;cursor:pointer;font-size:19px}
    .hero{padding:92px 0 68px;overflow:hidden}
    .hero-grid{display:grid;grid-template-columns:1.06fr .94fr;align-items:center;gap:58px}
    .eyebrow{display:inline-flex;align-items:center;gap:9px;text-transform:uppercase;letter-spacing:.14em;font-size:10px;font-weight:750;color:#54554f}
    .eyebrow:before{content:"";width:22px;height:1px;background:currentColor;display:block}
    h1,h2,h3,p{margin-top:0}
    h1{font-size:clamp(48px,6.3vw,82px);line-height:.99;letter-spacing:-.075em;margin:22px 0 24px;font-weight:750;max-width:680px}
    h1 .outline{color:transparent;-webkit-text-stroke:1.4px var(--ink)}
    .hero-copy{font-size:17px;color:#53544f;max-width:510px;line-height:1.75;margin-bottom:28px}
    .hero-actions{display:flex;gap:11px;flex-wrap:wrap}
    .arrow{font-size:17px;line-height:0;transition:transform .25s var(--ease)}
    a:hover .arrow{transform:translate(3px,-2px)}
    .hero-note{font-size:11px;color:#73746e;margin-top:19px}
    .visual{min-height:440px;position:relative;display:grid;place-items:center}
    .orbit{position:absolute;width:min(38vw,410px);aspect-ratio:1;border:1px solid #d2d2cb;border-radius:50%;animation:slow-spin 35s linear infinite}
    .orbit:before,.orbit:after{content:"";position:absolute;border:1px solid #d2d2cb;border-radius:50%}
    .orbit:before{inset:30px}.orbit:after{inset:66px}
    .orbit-dot{position:absolute;top:19%;right:17%;width:11px;height:11px;background:#111;border-radius:50%;box-shadow:0 0 0 7px rgba(17,17,17,.08)}
    .hero-card{position:relative;z-index:1;width:min(100%,390px);background:#fff;border:1px solid #e1e1db;border-radius:20px;padding:24px;box-shadow:0 25px 65px rgba(20,20,18,.08);transform:rotate(2deg);animation:float 6s ease-in-out infinite}
    .card-top{display:flex;justify-content:space-between;align-items:center;border-bottom:1px solid #e9e9e4;padding-bottom:17px;margin-bottom:20px}
    .card-top strong{font-size:12px;letter-spacing:-.02em}.status{display:inline-flex;align-items:center;gap:6px;font-size:10px;color:#62635e}.status:before{content:"";width:6px;height:6px;background:#111;border-radius:50%}
    .card-kicker{font-size:10px;color:#787972;text-transform:uppercase;letter-spacing:.11em;margin-bottom:7px}
    .card-heading{font-size:27px;letter-spacing:-.055em;font-weight:730;line-height:1.15;margin-bottom:19px}
    .flow{display:grid;grid-template-columns:1fr 24px 1fr 24px 1fr;gap:5px;align-items:center}
    .flow-step{min-height:88px;padding:12px 9px;border:1px solid #e4e4de;border-radius:12px;display:flex;flex-direction:column;justify-content:space-between;font-size:10px;font-weight:650}
    .flow-step b{display:grid;place-items:center;width:25px;height:25px;border-radius:8px;background:#111;color:white;font-size:11px}
    .flow-arrow{text-align:center;color:#8c8d86;font-size:16px}
    .card-bottom{margin-top:20px;padding:12px 13px;border-radius:10px;background:#f4f4f0;font-size:11px;color:#55564f;display:flex;justify-content:space-between;gap:15px;align-items:center}
    .card-bottom span:last-child{color:#111;font-weight:750}
    .side-label{position:absolute;right:2%;bottom:10%;writing-mode:vertical-rl;font-size:10px;letter-spacing:.16em;color:#777870;text-transform:uppercase}
    .ticker{border-block:1px solid var(--line);overflow:hidden;white-space:nowrap;padding:16px 0;color:#454640;font-size:11px;text-transform:uppercase;letter-spacing:.12em}
    .ticker-track{display:flex;width:max-content;animation:marquee 27s linear infinite;gap:30px}
    .ticker span{display:inline-flex;align-items:center;gap:30px}.ticker i{width:5px;height:5px;background:#111;display:inline-block;border-radius:50%}
    section{padding:100px 0}
    .section-head{display:grid;grid-template-columns: .7fr 1.3fr;gap:44px;align-items:start;margin-bottom:48px}
    .section-label{font-size:11px;color:#6c6d66;letter-spacing:.13em;text-transform:uppercase;font-weight:700;padding-top:9px}
    h2{font-size:clamp(34px,4.7vw,57px);line-height:1.05;letter-spacing:-.065em;margin-bottom:18px;font-weight:720}
    .section-intro{max-width:630px;font-size:16px;color:#5b5c56;line-height:1.8;margin-bottom:0}
    .about{background:#111;color:#f7f7f2}
    .about .section-label{color:#b5b6af}.about .section-intro{color:#bebfb8}
    .about-grid{display:grid;grid-template-columns:1fr 1fr;gap:70px;align-items:end}
    .about h2{max-width:600px}.about .about-copy{font-size:17px;color:#c8c9c1;line-height:1.85;max-width:560px}
    .quote-line{padding:24px 0;border-top:1px solid #3b3b37;border-bottom:1px solid #3b3b37;display:flex;align-items:center;gap:18px;margin-top:28px;font-size:13px;color:#efefe9}
    .quote-icon{width:38px;height:38px;border:1px solid #5a5a54;border-radius:50%;display:grid;place-items:center;flex:none;font-size:16px}
    .manifesto{font-size:clamp(25px,3.2vw,39px);line-height:1.3;letter-spacing:-.045em;font-weight:560}
    .manifesto span{color:#777871}
    .services{background:var(--paper)}
    .service-grid{display:grid;grid-template-columns:repeat(3,1fr);border-top:1px solid var(--line);border-left:1px solid var(--line)}
    .service{padding:28px;min-height:280px;border-right:1px solid var(--line);border-bottom:1px solid var(--line);transition:background .25s,transform .3s var(--ease)}
    .service:hover{background:#fff}
    .service-no{font-size:11px;color:#777870;letter-spacing:.1em;display:flex;justify-content:space-between;margin-bottom:52px}
    .service-icon{width:36px;height:36px;border:1px solid #b9bab3;border-radius:11px;display:grid;place-items:center;font-size:15px;color:#111}
    .service h3{font-size:21px;letter-spacing:-.045em;margin-bottom:10px}
    .service p{font-size:13px;color:#666760;line-height:1.8;margin-bottom:0;max-width:280px}
    .service-tag{display:inline-block;margin-top:18px;padding:5px 9px;border:1px solid #d9d9d3;border-radius:999px;font-size:10px;color:#55564f}
    .principle{padding:0 0 100px;background:var(--paper)}
    .principle-box{background:#e9e9e3;border-radius:var(--radius);padding:35px 38px;display:grid;grid-template-columns: .55fr 1.45fr;gap:40px;align-items:center}
    .principle-label{font-size:11px;text-transform:uppercase;letter-spacing:.13em;color:#62635c;font-weight:700}
    .principle-box h2{font-size:clamp(27px,3.5vw,42px);margin:0;max-width:700px}
    .principle-box h2 span{color:#777870}
    .steps{background:#fff}
    .step-list{border-top:1px solid var(--line)}
    .step{display:grid;grid-template-columns:70px .8fr 1.2fr;gap:30px;padding:25px 0;border-bottom:1px solid var(--line);align-items:start}
    .step-no{font-size:12px;color:#777870;padding-top:7px}
    .step h3{font-size:21px;letter-spacing:-.04em;margin:0}
    .step p{font-size:13px;color:#676862;line-height:1.8;margin:0;max-width:480px}
    .contact{background:#111;color:#fff;padding:100px 0 60px;overflow:hidden;position:relative}
    .contact:after{content:"N";position:absolute;font-size:clamp(250px,40vw,520px);font-weight:850;letter-spacing:-.12em;line-height:1;right:-.05em;bottom:-.28em;color:rgba(255,255,255,.035);pointer-events:none}
    .contact-grid{display:grid;grid-template-columns:1fr auto;align-items:end;gap:40px;position:relative;z-index:1}
    .contact .eyebrow{color:#c6c7c0}.contact h2{font-size:clamp(43px,6.3vw,76px);max-width:680px;margin:20px 0}.contact p{font-size:15px;color:#c0c1ba;max-width:470px;line-height:1.8;margin-bottom:0}
    .contact-actions{display:flex;flex-direction:column;gap:12px;align-items:flex-start}.contact .button.dark{background:#f5f5f2;color:#111;border-color:#f5f5f2}.contact .button.dark:hover{background:#dcdcd5}.contact .button.light{color:#f5f5f2;border-color:#4f504a}.contact .button.light:hover{background:#fff;color:#111}
    .contact-bottom{position:relative;z-index:1;display:flex;justify-content:space-between;gap:20px;border-top:1px solid #383933;margin-top:90px;padding-top:22px;color:#989991;font-size:11px}
    .contact-bottom a:hover{color:#fff}
    .reveal{opacity:0;transform:translateY(22px);transition:opacity .7s var(--ease),transform .7s var(--ease)}
    .reveal.visible{opacity:1;transform:translateY(0)}
    .delay-1{transition-delay:.1s}.delay-2{transition-delay:.2s}.delay-3{transition-delay:.3s}
    @keyframes float{0%,100%{transform:translateY(0) rotate(2deg)}50%{transform:translateY(-10px) rotate(1deg)}}
    @keyframes slow-spin{to{transform:rotate(360deg)}}
    @keyframes marquee{to{transform:translateX(-50%)}}
    @media (prefers-reduced-motion:reduce){*,*::before,*::after{scroll-behavior:auto!important;animation-duration:.01ms!important;animation-iteration-count:1!important;transition-duration:.01ms!important}.reveal{opacity:1;transform:none}}
    @media(max-width:900px){.hero-grid{grid-template-columns:1fr;gap:20px}.hero{padding-top:70px}.visual{min-height:400px}.orbit{width:360px}.section-head{grid-template-columns:1fr;gap:17px}.about-grid{grid-template-columns:1fr;gap:25px}.service-grid{grid-template-columns:repeat(2,1fr)}.principle-box{grid-template-columns:1fr;gap:17px}.contact-grid{grid-template-columns:1fr}.contact-actions{flex-direction:row;flex-wrap:wrap}.step{grid-template-columns:45px .8fr 1.2fr;gap:18px}}
    @media(max-width:620px){.wrap{width:min(var(--max),calc(100% - 34px))}.nav{height:66px}.menu-btn{display:grid;place-items:center}.nav-links{display:none;position:absolute;top:65px;left:0;right:0;padding:20px 24px 24px;background:var(--paper);border-bottom:1px solid var(--line);flex-direction:column;align-items:stretch;gap:18px}.nav-links.open{display:flex}.nav-cta{text-align:center}.hero{padding:58px 0 45px}h1{font-size:clamp(46px,14vw,66px)}.hero-copy{font-size:15px}.visual{min-height:340px}.orbit{width:min(83vw,340px)}.hero-card{width:min(100%,340px);padding:19px}.card-heading{font-size:24px}.flow{grid-template-columns:1fr 14px 1fr 14px 1fr;gap:3px}.flow-step{min-height:77px;padding:9px 7px;font-size:9px}.side-label{right:0;bottom:2%}.ticker{padding:12px 0}section{padding:72px 0}.section-head{margin-bottom:32px}h2{font-size:39px}.section-intro{font-size:14px}.service-grid{grid-template-columns:1fr}.service{min-height:auto;padding:24px}.service-no{margin-bottom:30px}.principle{padding-bottom:72px}.principle-box{padding:26px 22px}.step{grid-template-columns:30px 1fr;gap:12px;padding:20px 0}.step p{grid-column:2}.step h3{font-size:19px}.contact{padding:76px 0 35px}.contact h2{font-size:47px}.contact p{font-size:14px}.contact-actions{flex-direction:column;align-items:stretch}.contact-actions .button{width:100%}.contact-bottom{margin-top:55px;flex-direction:column;gap:8px}.brand{font-size:19px}}
  </style>
</head>
<body>
  <div class="nav-shell">
    <nav class="nav wrap" aria-label="Navigasi utama">
      <a class="brand" href="#home" aria-label="NEX AI, beranda">
        <span class="brand-mark" aria-hidden="true">NEX</span>
        <span>NEX AI<small>TEKNOLOGI UNTUK USAHA</small></span>
      </a>
      <button class="menu-btn" id="menuBtn" aria-label="Buka menu" aria-expanded="false">☰</button>
      <div class="nav-links" id="navLinks">
        <a href="#tentang">Tentang</a>
        <a href="#solusi">Solusi</a>
        <a href="#cara-kerja">Cara kerja</a>
        <a class="nav-cta" href="#kontak">Hubungi Hatta <span class="arrow">↗</span></a>
      </div>
    </nav>
  </div>

  <main>
    <section class="hero" id="home">
      <div class="wrap hero-grid">
        <div class="reveal visible">
          <div class="eyebrow">Teknologi yang pas untuk usahamu</div>
          <h1>Bikin kerja usaha<br><span class="outline">lebih praktis.</span></h1>
          <p class="hero-copy">Saya Hatta, programmer di balik NEX AI. Saya membantu UMKM memakai teknologi agar pekerjaan sehari-hari lebih mudah—mulai dari website sampai pencatatan dan otomasi.</p>
          <div class="hero-actions">
            <a class="button dark" href="#kontak">Ngobrol via WhatsApp <span class="arrow">↗</span></a>
            <a class="button light" href="#solusi">Lihat layanan <span class="arrow">↓</span></a>
          </div>
          <p class="hero-note">Belum harus tahu butuh apa. Kita cari tahu bersama.</p>
        </div>
        <div class="visual reveal delay-2" aria-label="Ilustrasi alur kerja NEX AI">
          <div class="orbit"><span class="orbit-dot"></span></div>
          <div class="hero-card">
            <div class="card-top"><strong>NEX AI</strong><span class="status">Mulai dari cerita</span></div>
            <div class="card-kicker">Cari tahu dulu</div>
            <div class="card-heading">Dengar dulu.<br>Baru cari solusi.</div>
            <div class="flow" aria-label="Pahami, rancang, uji">
              <div class="flow-step"><b>01</b><span>Pahami</span></div><div class="flow-arrow">→</div>
              <div class="flow-step"><b>02</b><span>Rancang</span></div><div class="flow-arrow">→</div>
              <div class="flow-step"><b>03</b><span>Uji</span></div>
            </div>
            <div class="card-bottom"><span>Solusi mengikuti kebutuhan usaha.</span><span>↗</span></div>
          </div>
          <div class="side-label">Teknologi yang berguna</div>
        </div>
      </div>
    </section>

    <div class="ticker" aria-hidden="true">
      <div class="ticker-track">
        <span>Usaha lebih praktis <i></i> Teknologi sesuai kebutuhan <i></i> Mulai dari masalah <i></i> Kerja lebih rapi <i></i> Usaha lebih praktis <i></i> Teknologi sesuai kebutuhan <i></i> Mulai dari masalah <i></i> Kerja lebih rapi <i></i></span>
        <span>Usaha lebih praktis <i></i> Teknologi sesuai kebutuhan <i></i> Mulai dari masalah <i></i> Kerja lebih rapi <i></i> Usaha lebih praktis <i></i> Teknologi sesuai kebutuhan <i></i> Mulai dari masalah <i></i> Kerja lebih rapi <i></i></span>
      </div>
    </div>

    <section class="about" id="tentang">
      <div class="wrap">
        <div class="section-head reveal">
          <div class="section-label">01 / Tentang NEX AI</div>
          <div><h2>Apa itu NEX AI?</h2><p class="section-intro">NEX AI adalah proyek teknologi yang saya bangun untuk membantu UMKM memakai solusi digital yang benar-benar berguna.</p></div>
        </div>
        <div class="about-grid reveal delay-1">
          <div>
            <p class="about-copy">Saya percaya teknologi tidak harus rumit. Kadang website sederhana sudah cukup; kadang yang dibutuhkan justru pencatatan yang rapi atau cara mengurangi kerja berulang. Kita bahas dulu sebelum memilih solusi.</p>
            <div class="quote-line"><span class="quote-icon">↗</span><span>Bukan asal membuat aplikasi. Yang penting benar-benar berguna.</span></div>
          </div>
          <div class="manifesto">Mulai dari ceritamu. <span>Kita cari langkah yang masuk akal untuk usahamu.</span></div>
        </div>
      </div>
    </section>

    <section class="services" id="solusi">
      <div class="wrap">
        <div class="section-head reveal">
          <div class="section-label">02 / Layanan</div>
          <div><h2>Hal yang bisa kita kerjakan.</h2><p class="section-intro">Tidak perlu langsung membuat aplikasi besar. Kita mulai dari kebutuhan yang paling terasa.</p></div>
        </div>
        <div class="service-grid">
          <article class="service reveal"><div class="service-no"><span>01 / WEB</span><span class="service-icon">↗</span></div><h3>Website & katalog</h3><p>Tampilkan produk, harga, lokasi, dan kontak agar pelanggan mudah mendapat informasi.</p><span class="service-tag">Info usaha lebih jelas</span></article>
          <article class="service reveal delay-1"><div class="service-no"><span>02 / OPERASI</span><span class="service-icon">⌘</span></div><h3>Pencatatan usaha</h3><p>Buat catatan pesanan, stok, atau pekerjaan harian lebih rapi.</p><span class="service-tag">Kerja lebih rapi</span></article>
          <article class="service reveal delay-2"><div class="service-no"><span>03 / DATA</span><span class="service-icon">▥</span></div><h3>Ringkasan bisnis</h3><p>Lihat data penjualan dan biaya dengan lebih mudah untuk memahami kondisi usaha.</p><span class="service-tag">Lebih mudah dipantau</span></article>
          <article class="service reveal"><div class="service-no"><span>04 / OTOMASI</span><span class="service-icon">⟳</span></div><h3>Otomasi & integrasi</h3><p>Kurangi input berulang dengan menghubungkan proses atau aplikasi yang memang perlu tersambung.</p><span class="service-tag">Kurangi kerja berulang</span></article>
          <article class="service reveal delay-1"><div class="service-no"><span>05 / AI</span><span class="service-icon">✳</span></div><h3>AI jika cocok</h3><p>Gunakan AI untuk tugas tertentu jika memang bisa membantu pekerjaan sehari-hari.</p><span class="service-tag">Bukan sekadar ikut tren</span></article>
          <article class="service reveal delay-2"><div class="service-no"><span>06 / DISKUSI</span><span class="service-icon">↔</span></div><h3>Diskusi kebutuhan</h3><p>Belum tahu butuh apa? Ceritakan kendalanya, lalu kita bahas pilihan yang mungkin.</p><span class="service-tag">Mulai dari obrolan</span></article>
        </div>
      </div>
    </section>

    <div class="principle"><div class="wrap"><div class="principle-box reveal"><div class="principle-label">Cara kami berpikir</div><h2>Kalau ada cara yang lebih sederhana, <span>kita tidak perlu membuat sistem yang rumit.</span></h2></div></div></div>

    <section class="steps" id="cara-kerja">
      <div class="wrap">
        <div class="section-head reveal">
          <div class="section-label">03 / Cara kerja</div>
          <div><h2>Kita obrolkan dulu.</h2><p class="section-intro">Tidak harus langsung sepakat membuat sesuatu. Kita pahami kebutuhannya dulu.</p></div>
        </div>
        <div class="step-list">
          <div class="step reveal"><div class="step-no">01</div><h3>Ceritakan</h3><p>Kamu bisa mulai dari bagian usaha yang terasa merepotkan.</p></div>
          <div class="step reveal"><div class="step-no">02</div><h3>Cari inti masalah</h3><p>Kita lihat apa yang paling perlu dibantu dan apa yang sudah berjalan baik.</p></div>
          <div class="step reveal"><div class="step-no">03</div><h3>Bahas pilihan</h3><p>Kalau ada solusi yang cocok, kita bahas cara kerja, biaya, dan waktunya sebelum mulai.</p></div>
          <div class="step reveal"><div class="step-no">04</div><h3>Kerjakan & uji</h3><p>Solusi dibuat sesuai kesepakatan, lalu kita cek bersama apakah sudah membantu.</p></div>
        </div>
      </div>
    </section>

    <section class="contact" id="kontak">
      <div class="wrap">
        <div class="contact-grid reveal">
          <div><div class="eyebrow">04 / Ngobrol dulu</div><h2>Ada yang ingin kamu buat lebih mudah?</h2><p>Ceritakan saja lewat WhatsApp. Kita bahas dulu, tanpa harus langsung sepakat membuat proyek.</p></div>
          <div class="contact-actions"><a class="button dark" id="waButton" href="https://wa.me/6289679434870?text=Halo%20NEX%20AI%2C%20saya%20ingin%20ngobrol%20tentang%20kebutuhan%20digital%20usaha%20saya." target="_blank" rel="noopener noreferrer">Chat WhatsApp <span class="arrow">↗</span></a><a class="button light" href="#solusi">Lihat solusi <span class="arrow">↑</span></a></div><p class="hero-note" style="color:#b8b8b2;grid-column:1/-1;margin-top:6px">WhatsApp: 0896 7943 4870</p>
        </div>
        <div class="contact-bottom"><span>© <span id="year"></span> NEX AI. Dibangun dari kebutuhan nyata.</span><a href="#home">Kembali ke atas ↑</a></div>
      </div>
    </section>
  </main>

  <script>
    // Nomor WhatsApp NEX AI dalam format internasional, tanpa tanda + atau spasi.
    const WHATSAPP_NUMBER = "6289679434870";
    const waButton = document.getElementById("waButton");
    const message = "Halo NEX AI, saya ingin ngobrol tentang kebutuhan digital usaha saya.";
    waButton.addEventListener("click", function (event) {
      if (!/^\d{10,15}$/.test(WHATSAPP_NUMBER)) {
        event.preventDefault();
        alert("Maaf, tombol WhatsApp belum bisa dibuka. Coba hubungi 089679434870.");
        return;
      }
      event.preventDefault();
      window.open("https://wa.me/" + WHATSAPP_NUMBER + "?text=" + encodeURIComponent(message), "_blank", "noopener,noreferrer");
    });
    document.getElementById("year").textContent = new Date().getFullYear();
    const menuBtn = document.getElementById("menuBtn");
    const navLinks = document.getElementById("navLinks");
    menuBtn.addEventListener("click", () => {
      const open = navLinks.classList.toggle("open");
      menuBtn.setAttribute("aria-expanded", String(open));
      menuBtn.setAttribute("aria-label", open ? "Tutup menu" : "Buka menu");
      menuBtn.textContent = open ? "×" : "☰";
    });
    navLinks.querySelectorAll("a").forEach(link => link.addEventListener("click", () => {
      navLinks.classList.remove("open"); menuBtn.setAttribute("aria-expanded", "false"); menuBtn.setAttribute("aria-label", "Buka menu"); menuBtn.textContent = "☰";
    }));
    const revealObserver = new IntersectionObserver(entries => {
      entries.forEach(entry => { if (entry.isIntersecting) { entry.target.classList.add("visible"); revealObserver.unobserve(entry.target); } });
    }, { threshold: 0.12 });
    document.querySelectorAll(".reveal:not(.visible)").forEach(el => revealObserver.observe(el));
  </script>
</body>
</html>
