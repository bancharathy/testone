<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>About My Girlfriend</title>
  <meta name="description" content="A simple, sweet webpage celebrating my girlfriend." />
  <style>
    :root{
      --bg: #fff;
      --card: #f7f7fb;
      --muted: #000000;
      --accent: #fafafa;
      --radius: 14px;
      font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      background: linear-gradient(180deg,#fff 0%, #fbfbff 100%);
      color:#080808;
      line-height:1.45;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      padding:28px;
      display:flex;
      justify-content:center;
      font-size:16px;
    }
    .wrap{
      width:100%;
      max-width:980px;
      background:var(--card);
      border-radius:18px;
      padding:28px;
      box-shadow: 0 10px 30px rgba(20,20,40,0.06);
      overflow:hidden;
    }
    header{
      display:flex;
      gap:18px;
      align-items:center;
      margin-bottom:18px;
    }
    .avatar{
      width:110px;
      height:110px;
      border-radius:18px;
      overflow:hidden;
      flex: 0 0 110px;
      box-shadow: 0 6px 18px rgba(0,0,0,0.06);
    }
    .avatar img{ width:100%; height:100%; object-fit:cover; display:block; }
    h1{ margin:0; font-size:28px; }
    p.lead{ margin:6px 0 0; color:var(--muted); }
    .grid{
      display:grid;
      grid-template-columns: 1fr 360px;
      gap:20px;
      margin-top:18px;
    }
    .card{
      background:#f50478;
      border-radius:12px;
      padding:16px;
      box-shadow: 0 6px 18px rgba(16,16,30,0.04);
    }
    .bio h2{ margin:0 0 8px; font-size:18px; }
    .bio p{ margin:0 0 12px; color:var(--muted); }
    .info-list{ display:flex; gap:12px; flex-wrap:wrap; margin-top:8px; }
    .chip{
      background:#f2f6ff;
      padding:8px 10px;
      border-radius:999px;
      font-size:14px;
      color:#1f3d7a;
    }

    .favorites ul{ padding:0; margin:0; list-style:none; display:grid; gap:8px; }
    .favorites li{ display:flex; gap:10px; align-items:center; padding:8px; border-radius:10px; background:linear-gradient(180deg,#fff,#fbfdff); }
    .favorites .dot{ width:10px; height:10px; border-radius:50%; background:var(--accent); flex:0 0 10px; }

    .gallery{
      display:grid;
      grid-template-columns: repeat(3,1fr);
      gap:8px;
      margin-top:10px;
    }
    .gallery img{ width:100%; height:100px; object-fit:cover; border-radius:8px; display:block; }

    .timeline{ margin-top:10px; }
    .timeline-item{ display:flex; gap:12px; align-items:flex-start; margin-bottom:12px; }
    .timeline-item .dot{ width:12px; height:12px; border-radius:50%; background:#e9eefb; margin-top:6px; border:3px solid #cddbf9; }

    .cta{ display:flex; gap:8px; margin-top:18px; }
    .btn{
      display:inline-flex;
      align-items:center;
      gap:8px;
      padding:10px 14px;
      border-radius:10px;
      border:0;
      cursor:pointer;
      font-weight:600;
    }
    .btn-primary{ background:var(--accent); color:#fff; box-shadow:0 6px 18px rgba(255,107,107,0.18);}
    .btn-ghost{ background:transparent; color:var(--muted); border:1px solid rgba(16,16,30,0.06); }

    footer{ margin-top:18px; text-align:center; color:var(--muted); font-size:14px; }

    /* Responsive */
    @media (max-width:900px){
      .grid{ grid-template-columns: 1fr; }
      .avatar{ width:86px; height:86px; flex:0 0 86px; }
    }
  </style>
</head>
<body>
  <main class="wrap" role="main">
    <header>
      <div class="avatar" aria-hidden="true">
        <!-- Replace "photo_6129476574517513374_y.jpg" with your girlfriend's photo file name -->
        <img src="photo_6129476574517513374_y.jpg" alt="photo_6129476574517513374_y.jpg">
      </div>
      <div>
        <!-- Replace name and subtitle below -->
        <h1>Leng Inan</h1>
        <p class="lead">My girlfriend — kind, brave, and full of smiles.</p>
        <div style="margin-top:10px;" class="info-list" aria-hidden="true">
          <span class="chip">Age: 15</span>
          <span class="chip">From: Bekchan</span>
          <span class="chip">Loves: Matcha</span>
        </div>
      </div>
    </header>

    <div class="grid">
      <section class="card bio" aria-labelledby="about-title">
        <h2 id="about-title">About Her</h2>
        <p>
          <!-- Replace this paragraph with a short personal bio -->
          She is a warm, creative person who brings joy into small moments. She loves music, drawing, and exploring new places. She always supports me and makes every day better.
        </p>

        <div class="timeline">
          <div class="timeline-item">
            <div class="dot" aria-hidden="true"></div>
            <div>
              <strong>How we met</strong>
              <div style="color:var(--muted); font-size:14px;">We met at school and quickly became friends, then more.</div>
            </div>
          </div>

          <div class="timeline-item">
            <div class="dot" aria-hidden="true"></div>
            <div>
              <strong>Favorite memory</strong>
              <div style="color:var(--muted); font-size:14px;">We need to play games and beat each other</div>
            </div>
          </div>
        </div>

        <div class="cta" role="group" aria-label="Actions">
        </div>
      </section>

      <aside>
        <div class="card favorites" aria-labelledby="fav-title">
          <h3 id="fav-title" style="margin-top:0;">Favorites</h3>
          <ul>
            <li><span class="dot" aria-hidden="true"></span><strong style="margin-right:8px;">Food:</strong> Noodle soup</li>
            <li><span class="dot" aria-hidden="true"></span><strong style="margin-right:8px;">Song:</strong> (song khmer)</li>
            <li><span class="dot" aria-hidden="true"></span><strong style="margin-right:8px;">Hobby:</strong> Kimi</li>
          </ul>
        </div>

        
        </div>
      </aside>
    </div>

    <section class="card" id="gallery" style="margin-top:18px;">
      <h2 style="margin-top:0;">Photo Gallery</h2>
      <p style="color:var(--muted); margin:0 0 10px;">Replace these placeholder images with your favorite photos.</p>
      <div class="gallery" aria-label="Photo gallery">
        <!-- Replace the image sources with real image file names or URLs -->
        <img src="photo_6129476574517513374_y.jpg" alt="Photo 1">
        <img src="photo_6129476574517513374_y.jpg" alt="Photo 2">
        <img src="photo_6129476574517513374_y.jpg" alt="Photo 3">
        <img src="photo_6129476574517513374_y.jpg" alt="Photo 4">
        <img src="photo_6129476574517513374_y.jpg" alt="Photo 5">
        <img src="photo_6129476574517513374_y.jpg" alt="Photo 6">
      </div>
    </section>

    <footer>
      Made with ❤️ — a small page about someone special.
    </footer>
  </main>

  <script>
    // Small helper: if photo.jpg doesn't load, show a placeholder color block
    document.querySelectorAll('.avatar img').forEach(img=>{
      img.onerror = ()=> {
        img.style.display = 'none';
        const fallback = document.createElement('div');
        fallback.style.width = '100%';
        fallback.style.height = '100%';
        fallback.style.display = 'flex';
        fallback.style.alignItems = 'center';
        fallback.style.justifyContent = 'center';
        fallback.style.background = '#ffecec';
        fallback.style.color = '#9b3b3b';
        fallback.style.fontWeight = '700';
        fallback.textContent = 'Add photo.jpg';
        img.parentNode.appendChild(fallback);
      };
    });
  </script>
</body>
</html>

