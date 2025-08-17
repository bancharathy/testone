<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Ban charathik top up dimond</title>

  <style>
    /* Basic reset */
    *,*::before,*::after{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial;
      background: linear-gradient(180deg,#01080a 0%, #f8f8f8 100%);
      color:#f9fbff;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }

    /* Layout */
    .container{
      max-width:980px;
      margin:28px auto;
      padding:20px;
      background:#0a0303;
      border-radius:12px;
      box-shadow:0 8px 30px rgba(242, 244, 246, 0.08);
      overflow:hidden;
      display:grid;
      grid-template-columns: 360px 1fr;
      gap:24px;
    }

    /* Left column (QR + seller) */
    .card{
      background:linear-gradient(180deg,#140303 0%, #fbfdff 100%);
      border-radius:10px;
      padding:18px;
      box-shadow:0 4px 18px rgba(9,30,63,0.04);
    }
    .qr-wrap{
      text-align:center;
    }
    .qr{
      width:220px;
      height:220px;
      display:inline-block;
      border-radius:8px;
      background:#fff;
      padding:10px;
      border:1px solid rgba(15,23,42,0.06);
      cursor:pointer;
      transition:transform .15s ease;
    }
    .qr:hover{transform:translateY(-4px)}
    .seller{
      margin-top:14px;
      font-weight:700;
      letter-spacing:0.6px;
      font-size:18px;
      color:#eaeff1;
    }
    .scan-note{color:#fbfeff;margin-top:6px;font-size:14px}

    /* Right column (details, games, form) */
    .main{
      padding:8px 2px;
    }
    h1{
      margin:0 0 8px 0;
      font-size:22px;
      color:#f0f3f4;
    }
    p.lead{margin:0 0 14px 0;color:#f8fcfd}

    .games{
      display:flex;
      gap:10px;
      flex-wrap:wrap;
      margin-bottom:14px;
    }
    .game{
      background:#f1fbfb;
      border:1px solid rgba(9,30,63,0.04);
      padding:8px 12px;
      border-radius:8px;
      font-weight:600;
      color:#064049;
      font-size:14px;
    }

    table.prices{
      width:100%;
      border-collapse:collapse;
      margin:14px 0 18px 0;
      font-size:14px;
    }
    table.prices th, table.prices td{
      padding:10px 8px;
      border-bottom:1px solid #eef3f5;
      text-align:left;
    }
    table.prices th{
      background:#fbffff;
      font-weight:700;
      color:#082b30;
    }

    /* Form */
    form{margin-top:6px}
    .field{
      margin-bottom:10px;
    }
    label{display:block;margin-bottom:6px;font-size:13px;color:#24474b}
    input[type="text"], input[type="tel"], select, textarea{
      width:100%;
      padding:10px 12px;
      border-radius:8px;
      border:1px solid #d6e6e8;
      font-size:14px;
      outline:none;
      transition:box-shadow .15s ease, border-color .15s ease;
      background:#fbffff;
    }
    input:focus, select:focus, textarea:focus{box-shadow:0 4px 18px rgba(6,22,45,0.06); border-color:#8fd6d6}
    textarea{min-height:90px;resize:vertical}

    .row{
      display:flex; gap:10px;
    }
    .row .col{flex:1}

    .btn{
      display:inline-block;
      padding:10px 14px;
      background:#0597a1;
      color:#fff;
      border:none;
      border-radius:8px;
      font-weight:700;
      cursor:pointer;
      box-shadow:0 6px 18px rgba(5,151,161,0.18);
      transition:transform .12s ease, box-shadow .12s ease;
    }
    .btn:active{transform:translateY(1px)}
    .muted{color:#f0f3f4;font-size:13px}

    .note{
      margin-top:12px;
      padding:10px;
      background:#fcfffb;
      border:1px solid #f1f7ee;
      border-radius:8px;
      color:#2f5f2f;
      font-size:13px;
    }

    /* modal for QR enlarge */
    .modal{
      position:fixed;
      inset:0;
      display:none;
      align-items:center;
      justify-content:center;
      background:rgba(4,10,12,0.45);
      z-index:60;
      padding:20px;
    }
    .modal.open{display:flex}
    .modal .modal-card{
      background:#fff;
      padding:16px;
      border-radius:10px;
      max-width:420px;
      width:100%;
      text-align:center;
      box-shadow:0 20px 50px rgba(3,12,18,0.5);
    }
    .modal .modal-card img{max-width:100%;height:auto;border-radius:8px}
    .modal .close{
      margin-top:12px;
      display:inline-block;
      background:#e6f7f5;
      color:#055c58;
      border-radius:8px;
      padding:8px 12px;
      cursor:pointer;
      border:1px solid rgba(5,92,88,0.08);
    }

    /* responsive */
    @media (max-width:880px){
      .container{grid-template-columns:1fr; padding:16px}
      .qr{width:200px;height:200px}
    }
  </style>
</head>
<body>

  <div class="container" role="main" aria-labelledby="site-title">
    <!-- left: QR & seller card -->
    <div class="card" aria-hidden="false">
      <div class="qr-wrap" title="Click to enlarge QR">
        <!-- Replace the src with the actual uploaded QR file path if needed.
             Current path uses the image you provided earlier in this conversation. -->
        <img class="qr" id="qrImage" src="/mnt/data/photo_6127253447905494481_y (1).jpg"
             alt="Payment QR code for Ban Charathik top up dimond" />
        <div class="seller">BAN CHARATHIK</div>
        <div class="scan-note">Scan this QR with your banking or e-wallet app to pay.</div>
      </div>

      <div style="margin-top:14px;font-size:13px;color:#f6fcfd">
        <strong>Payment instructions</strong>
        <p class="muted" style="margin:8px 0 0 0">
          1) Open your mobile banking or e-wallet app → Scan QR → Pay.<br>
          2) Keep the payment screenshot or transaction ID and submit it with the Top-Up form.<br>
          3) Delivery usually within 1–10 minutes after verification.
        </p>
      </div>
    </div>

    <!-- right: main content -->
    <div class="main">
      <h1 id="site-title">Ban charathik top up dimond</h1>
      <p class="lead">Fast, safe diamond top-ups for your favorite games. We support Mobile Legends, Free Fire, PUBG and Blood Strike — instant delivery after payment verification.</p>

      <div class="games" aria-hidden="false" role="list">
        <div class="game" role="listitem">Mobile Legend</div>
        <div class="game" role="listitem">Free Fire</div>
        <div class="game" role="listitem">PUBG</div>
        <div class="game" role="listitem">Blood Strik</div>
      </div>

      <h2 style="margin-top:8px;font-size:17px;color:#08323a">Price examples</h2>
      <table class="prices" aria-describedby="price-note">
        <thead>
          <tr>
            <th>Game</th>
            <th>Package</th>
            <th>Amount</th>
            <th>Price</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>Mobile Legend</td><td>Small</td><td>86 Diamonds</td><td>10.00</td></tr>
          <tr><td>Mobile Legend</td><td>Medium</td><td>257 Diamonds</td><td>25.00</td></tr>
          <tr><td>Free Fire</td><td>Starter</td><td>50 Diamonds</td><td>8.00</td></tr>
          <tr><td>PUBG</td><td>UC Pack</td><td>330 UC</td><td>20.00</td></tr>
          <tr><td>Blood Strik</td><td>Diamond Pack</td><td>100 Diamonds</td><td>12.00</td></tr>
        </tbody>
      </table>
      <div id="price-note" class="muted">Prices are examples. Final price depends on package and current rates. Contact the seller for exact pricing.</div>

      <h2 style="margin-top:18px;font-size:17px;color:#08323a">Top-Up Form</h2>
      <p class="muted">After you pay with the QR, complete the form below so we can deliver your top-up.</p>

      <form id="topupForm" autocomplete="off" novalidate>
        <div class="row">
          <div class="col field">
            <label for="payerName">Payer name</label>
            <input id="payerName" name="payerName" type="text" placeholder="Your name" required />
          </div>
          <div class="col field">
            <label for="phone">Phone (for contact)</label>
            <input id="phone" name="phone" type="tel" placeholder="+855 12 345 678" />
          </div>
        </div>

        <div class="field">
          <label for="gameSelect">Select game</label>
          <select id="gameSelect" name="gameSelect" required>
            <option value="">-- choose game --</option>
            <option value="mobile-legend">Mobile Legend</option>
            <option value="free-fire">Free Fire</option>
            <option value="pubg">PUBG</option>
            <option value="blood-strik">Blood Strik</option>
          </select>
        </div>

        <div class="field">
          <label for="account">Game account ID / nickname</label>
          <input id="account" name="account" type="text" placeholder="Example: player123" required />
        </div>

        <div class="field">
          <label for="packageInput">Package / Amount</label>
          <input id="packageInput" name="packageInput" type="text" placeholder="e.g. 86 Diamonds / 330 UC" required />
        </div>

        <div class="field">
          <label for="paymentRef">Payment reference or note (transaction id or screenshot link)</label>
          <input id="paymentRef" name="paymentRef" type="text" placeholder="Transaction ID or short note" required />
        </div>

        <div class="field">
          <label for="note">Additional note (optional)</label>
          <textarea id="note" name="note" placeholder="Any extra info"></textarea>
        </div>

        <div style="display:flex;gap:10px;align-items:center;margin-top:8px">
          <button class="btn" type="submit">Submit Top-Up Request</button>
          <div class="muted" style="font-size:13px">We will verify and deliver within minutes.</div>
        </div>

        <div id="formMessage" class="note" style="display:none"></div>
      </form>

      <div style="margin-top:16px;font-size:13px;">
        <strong>Contact / Support</strong>
        <p class="muted" style="margin:6px 0 0 0">
          Seller: Ban Charathik — Keep your payment screenshot until delivery is confirmed. If delivery takes longer than 30 minutes contact support.
        </p>
      </div>

      <footer style="margin-top:18px;color:#5b6f72;font-size:13px">
        © <span id="year"></span> Ban charathik top up dimond
      </footer>
    </div>
  </div>

  <!-- QR Modal (enlarge) -->
  <div id="qrModal" class="modal" role="dialog" aria-modal="true" aria-labelledby="modalTitle">
    <div class="modal-card" role="document">
      <h3 id="modalTitle" style="margin:0 0 10px 0;color:#06323a">Scan to Pay — Ban Charathik</h3>
      <img id="qrModalImage" src="/mnt/data/photo_6127253447905494481_y (1).jpg" alt="Enlarged QR code" />
      <div>
        <button class="close" id="closeModalBtn" type="button">Close</button>
      </div>
    </div>
  </div>

  <script>
    // Small JS to handle form validation, fake submit (demo) and QR modal
    (function(){
      const form = document.getElementById('topupForm');
      const formMsg = document.getElementById('formMessage');
      const yearEl = document.getElementById('year');
      yearEl.textContent = new Date().getFullYear();

      // Basic client-side validation and simulated submission
      form.addEventListener('submit', function(evt){
        evt.preventDefault();
        formMsg.style.display = 'none';
        formMsg.textContent = '';

        // gather fields
        const payer = document.getElementById('payerName').value.trim();
        const game = document.getElementById('gameSelect').value;
        const account = document.getElementById('account').value.trim();
        const pkg = document.getElementById('packageInput').value.trim();
        const paymentRef = document.getElementById('paymentRef').value.trim();

        // simple checks
        if(!payer || !game || !account || !pkg || !paymentRef){
          showMessage('Please fill in all required fields (payer, game, account, package, payment reference).', true);
          return;
        }

        // Simulate sending (in a real site you'd POST to a server API)
        const payload = {
          payer, game, account, package: pkg, paymentRef, note: document.getElementById('note').value || ''
        };

        // Show a friendly processing state
        showMessage('Processing your request... Please wait.', false);
        // Simulate small delay to mimic server processing
        setTimeout(function(){
          // After "success"
          showMessage('Top-up request submitted successfully! We will verify your payment and deliver within minutes. Keep your payment screenshot for verification.', false, true);
          form.reset();
        }, 900); // short simulated delay
      });

      function showMessage(msg, isError, persist){
        formMsg.style.display = 'block';
        formMsg.textContent = msg;
        formMsg.style.borderColor = isError ? '#f7d0d0' : '#e6f7ee';
        formMsg.style.background = isError ? '#fff7f7' : '#fbfffe';
        formMsg.style.color = isError ? '#7d2525' : '#114b3b';
        if(!persist && !isError){
          // hide after 6 seconds
          setTimeout(()=>{ formMsg.style.display='none'; }, 6000);
        }
      }

      // QR modal logic
      const qr = document.getElementById('qrImage');
      const modal = document.getElementById('qrModal');
      const closeBtn = document.getElementById('closeModalBtn');

      qr.addEventListener('click', ()=> modal.classList.add('open'));
      closeBtn.addEventListener('click', ()=> modal.classList.remove('open'));
      modal.addEventListener('click', function(e){
        if(e.target === modal) modal.classList.remove('open');
      });

      // Accessibility: close modal on Esc
      window.addEventListener('keydown', function(e){
        if(e.key === 'Escape' && modal.classList.contains('open')){
          modal.classList.remove('open');
        }
      });

    })();
  </script>
</body>
</html>

      
