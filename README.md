<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Ban Charathik — Portfolio</title>
  <meta name="description" content="Portfolio of Ban Charathik — student and beginner web developer." />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#f6f9fc; --card:#060606; --muted:#e8e8f7; --accent:#000000; --accent-2:#000000; --text:#eceef1; --glass: rgba(15,23,36,0.04);
      --radius:14px;
    }
    *{box-sizing:border-box}
    body{ margin:0; font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, 'Noto Sans', Arial; color:var(--text); background:var(--bg); -webkit-font-smoothing:antialiased }

    .wrap{ max-width:1100px; margin:32px auto; padding:20px }

    /* Header / Hero */
    header{ display:flex; gap:20px; align-items:center; background:linear-gradient(135deg,var(--accent),var(--accent-2)); padding:22px; border-radius:var(--radius); color:white }
   .avatar{ width:110px; height:110px; border-radius:18px; background:linear-gradient(135deg, rgba(255,255,255,0.12), rgba(255,255,255,0.06)); display:flex; align-items:center; justify-content:center; font-weight:800; font-size:34px; box-shadow:0 8px 20px rgba(14,165,233,0.12) }
    .head-info h1{ margin:0; font-size:28px; letter-spacing:0.2px }
    .head-info p{ margin:6px 0 0; opacity:.95 }
    .nav-links{ margin-top:12px; display:flex; gap:10px; flex-wrap:wrap }
    .chip{ background:rgba(255,255,255,0.12); padding:8px 12px; border-radius:999px; font-weight:600; font-size:14px }

    /* Layout */
    main{ display:grid; grid-template-columns: 1fr 320px; gap:22px; margin-top:22px }
    @media (max-width:980px){ main{ grid-template-columns: 1fr } }

    /* Cards */
    .card{ background:var(--card); border-radius:12px; padding:18px; box-shadow: 0 6px 18px rgba(15,23,36,0.06); border:1px solid rgba(15,23,36,0.03) }
    section + section{ margin-top:16px }

    /* About */
    .about p{ color:var(--muted); margin:8px 0 0 }

    /* Projects */
    .projects{ display:grid; gap:12px; color: #e2d8d8; }
    .project{ display:flex; gap:12px; align-items:center; padding:12px; border-radius:10px; transition:transform .12s ease, box-shadow .12s ease; cursor:default }
    .project:hover{ transform: translateY(-6px); box-shadow:0 18px 38px rgba(2,6,23,0.08) }
    .proj-thumb{ width:76px; height:64px; border-radius:8px; background:linear-gradient(135deg,var(--accent),var(--accent-2)); color:white; display:flex; align-items:center; justify-content:center; font-weight:800 }
    .project h4{ margin:0; font-size:15px }
    .project p{ margin:4px 0 0; color:var(--muted); font-size:13px }

    /* Skills */
    .skills{ display:flex; flex-wrap:wrap; gap:8px }
    .skill{ padding:8px 10px; background:var(--glass); border-radius:999px; font-weight:700; color:var(--text); font-size:13px }

    /* Sidebar */
    aside .contact-info{ display:grid; gap:10px }
    .info-row{ display:flex; justify-content:space-between; gap:8px; align-items:center }
    .info-row .label{ color:var(--muted) }

    .cta{ display:block; text-align:center; margin-top:12px; padding:10px 14px; border-radius:12px; font-weight:800; background:linear-gradient(90deg,var(--accent-2),var(--accent)); color:white; text-decoration:none }

    footer{ text-align:center; color:var(--muted); margin-top:28px }

    /* Small utilities */
    .muted{ color:var(--muted) }
    .small{ font-size:13px }
    .avatar img {
  width: 100px;       /* adjust width as needed */
  height: 100px;      /* adjust height as needed */
  border-radius: 50%; /* makes it circular */
  object-fit: cover;  /* keeps the image proportion and crops excess */
}

  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="avatar">
    <img src="photo_6127380742146213603_y.jpg" alt="BC's Avatar" />
      </div>
      <div class="head-info">
        <h1>Ban Charathik</h1>
        <p>My name is Ban Charathik. I'm 15 years old — a student learning web development and programming.</p>
        <div class="nav-links">
          <span class="chip">About</span>
          <span class="chip">Projects</span>
          <span class="chip">Skills</span>
          <span class="chip">Contact</span>
        </div>
      </div>
    </header>

    <main>
      <div>
        <section class="card about" id="about">
          <h2>About Me</h2>
          <p>My name is ban charathik I'm 15 years old. In my family there are 5 members: my brother <strong>Ban Sothea</strong>, my mother <strong>Chhoeun Sokin</strong>, my father <strong>Ban Buntheoun</strong>, my sister <strong>Ban Jenna</strong>, and me.</p>
          <p class="muted">I enjoy learning HTML, CSS, and JavaScript. I build small projects to practice and improve my skills. I like experimenting with layouts and making things that look nice and work well.</p>
        </section>

        <section class="card" id="projects">
          <h2>Selected Projects</h2>
          <div class="projects">
            <div class="project">
              <div class="proj-thumb">P1</div>
              <div>
                <h4>Personal Portfolio Website</h4>
                <p class="muted small">A responsive one-page portfolio built with HTML and CSS to showcase my work.</p>
              </div>
            </div>

            <div class="project">
              <div class="proj-thumb">P2</div>
              <div>
                <h4>Simple To‑Do App</h4>
                <p class="muted small">A JavaScript to-do list app for learning DOM manipulation and localStorage.</p>
              </div>
            </div>

            <div class="project">
              <div class="proj-thumb">P3</div>
              <div>
                <h4>Game Top‑Up Demo</h4>
                <p class="muted small">Buy car and sell car</p>
              </div>
            </div>
          </div>
        </section>

        <section class="card" id="skills">
          <h2>Skills</h2>
          <div class="skills" aria-label="skills list">
            <div class="skill">HTML</div>
            <div class="skill">CSS</div>
            <div class="skill">JavaScript (beginner)</div>
            <div class="skill">Responsive Design</div>
            <div class="skill">Git (basic)</div>
          </div>
        </section>
      </div>


        

        <section class="card">
          <h3>Goals</h3>
          <p class="muted">Keep learning web development, build useful projects, and eventually create games and apps people enjoy.</p>
        </section>
      </aside>
    </main>

    <footer>
      <p class="muted">© <span id="year"></span> Ban Charathik — Made with curiosity.</p>
    </footer>
  </div>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ban Charathik - Portfolio</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(to right, #232526, #414345);
      color: white;
      text-align: center;
    }
    header {
      background: #1f1f1f;
      padding: 20px;
      font-size: 24px;
      font-weight: bold;
      letter-spacing: 2px;
    }
    .profile {
      margin-top: 30px;
    }
    .profile img {
      width: 180px;
      height: 180px;
      object-fit: cover;
      border-radius: 50%;
      border: 4px solid #00adb5;
      box-shadow: 0 4px 12px rgba(0,0,0,0.5);
    }
    .about {
      margin: 30px auto;
      max-width: 600px;
      background: rgba(255, 255, 255, 0.05);
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    }
    h2 {
      color: #00adb5;
      margin-bottom: 10px;
    }
    footer {
      margin-top: 50px;
      padding: 15px;
      background: #111;
      font-size: 14px;
    }
  </style>
</head>
<body>
  <header>
    🌟 Ban Charathik - Portfolio 🌟
  </header>

  <section class="profile">
    <img src="photo_6127380742146213603_y.jpg" alt="Ban Charathik Profile">
    <h2>Hello, I'm Ban Charathik</h2>
    <p>I'm 15 years old</p>
  </section>

  <section class="about">
    <h2>About Me</h2>
    <p>In my family, there are 5 members:</p>
    <ul style="list-style:none; padding:0;">
      <li>👨 Dad: Ban Buntheoun</li>
      <li>👩 Mother: Chhoeun Sokin</li>
      <li>👦 Brother: Ban Sothea</li>
      <li>👧 Sister: Ban Jenna</li>
      <li>🙋 Me: Ban Charathik</li>
    </ul>
  </section>

  <footer>
    © 2025 Ban Charathik | Personal Portfolio
  </footer>
</body>
</html>

