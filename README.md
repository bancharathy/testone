<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ST Shop Dimond</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f4f6f9;
      color: #000000;
    }
    header {
      background: #000000;
      color: rgb(209, 209, 209);
      text-align: center;
      padding: 20px;
      font-size: 24px;
      font-weight: bold;
    }
    .container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
      padding: 20px;
    }
    .card {
      background: rgb(249, 126, 126);
      border-radius: 12px;
      padding: 20px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      text-align: center;
    }
    .card h2 {
      margin-bottom: 15px;
      color: #007bff;
    }
    ul {
      list-style: none;
      padding: 0;
    }
    ul li {
      padding: 8px;
      margin: 6px 0;
      border: 1px solid #ddd;
      border-radius: 6px;
      background: #f9fafc;
    }
    
    }
    .order-box {
      max-width: 600px;
      margin: 40px auto;
      background: #fff;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }
    label {
      display: block;
      margin: 10px 0 6px;
    }
    select, input {
      width: 100%;
      padding: 10px;
      border-radius: 8px;
      border: 1px solid #ccc;
      margin-bottom: 15px;
    }
    .result {
      font-weight: bold;
      color: green;
      margin-top: 10px;
    }
    button {
      background: #007bff;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 8px;
      cursor: pointer;
    }
    button:hover {
      background: #000000;
    }
  </style>
</head>
<body>

  <header>
    ST Shop Dimond
  </header>

  <div class="container">
    <!-- Mobile Legends -->
    <div class="card">
      <h2>Mobile Legends</h2>
      <ul>
        <li>$1 = 60 Diamonds</li>
        <li>$2 = 120 Diamonds</li>
        <li>$5 = 300 Diamonds</li>
        <li>$10 = 560 Diamonds</li>
        <li>$20 = 1200 Diamonds</li>
        <li>$30 = 1800 Diamonds</li>
        <li>$100 = 6000 Diamonds</li>
      </ul>
    </div>

    <!-- Free Fire -->
    <div class="card">
      <h2>Free Fire</h2>
      <ul>
        <li>$1 = 100 Diamonds</li>
        <li>$2 = 200 Diamonds</li>
        <li>$5 = 600 Diamonds</li>
        <li>$10 = 1200 Diamonds</li>
        <li>$20 = 2400 Diamonds</li>
        <li>$30 = 3600 Diamonds</li>
        <li>$100 = 12000 Diamonds</li>
      </ul>
    </div>

   
  <!-- Order Calculator -->
  <div class="order-box">
    <h2>Quick Order</h2>
    <label for="game">Select Game:</label>
    <select id="game">
      <option value="ml">Mobile Legends</option>
      <option value="ff">Free Fire</option>
    </select>

    <label for="amount">Select Amount (USD):</label>
    <select id="amount"></select>

    <label for="player">Player ID:</label>
    <input type="text" id="player" placeholder="Enter your Player ID">

    <button onclick="calculate()">Calculate Diamonds</button>
    <div class="result" id="result">Please select options above.</div>
  </div>

  <footer>
    © 2025 ST Shop Dimond — Fast & Safe Top Up
  </footer>

  <script>
    const priceMap = {
      ml: {1:60, 2:120, 5:300, 10:560, 20:1200, 30:1800, 100:6000},
      ff: {1:100, 2:200, 5:600, 10:1200, 20:2400, 30:3600, 100:12000}
    };

    const gameSel = document.getElementById("game");
    const amountSel = document.getElementById("amount");
    const result = document.getElementById("result");

    function loadAmounts() {
      const game = gameSel.value;
      const plans = priceMap[game];
      amountSel.innerHTML = "";
      for (let usd in plans) {
        let opt = document.createElement("option");
        opt.value = usd;
        opt.textContent = `$${usd}`;
        amountSel.appendChild(opt);
      }
    }

    function calculate() {
      const game = gameSel.value;
      const usd = amountSel.value;
      const diamonds = priceMap[game][usd];
      const playerId = document.getElementById("player").value;
      const gameName = game === "ml" ? "Mobile Legends" : "Free Fire";
      result.textContent = `${gameName} → $${usd} = ${diamonds} Diamonds for Player ID: ${playerId}`;
    }

    gameSel.addEventListener("change", loadAmounts);
    window.onload = loadAmounts;
  </script>

</body>
</html>

