<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Top Up Diamonds - Game Portal</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <header>
    <div class="navbar">
      <h1>Game Portal</h1>
      <nav>
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">Top Up</a></li>
          <li><a href="#">Support</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <section class="top-up-section">
    <div class="content">
      <h2>Top Up Diamonds</h2>
      <p>Boost your in-game progress by topping up diamonds! Diamonds can be used to buy exclusive items, skins, and boosts.</p>
      
      <form id="topUpForm">
        <label for="diamondAmount">Select Amount:</label>
        <select id="diamondAmount" required>
          <option value="100">100 Diamonds - $1</option>
          <option value="250">250 Diamonds - $2.5</option>
          <option value="500">500 Diamonds - $5</option>
          <option value="1000">1000 Diamonds - $10</option>
        </select>

        <button type="submit">Top Up Now</button>
      </form>

      <div id="confirmationMessage" class="hidden">
        <p>Your top up of <span id="amountValue"></span> diamonds was successful!</p>
      </div>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 Game Portal. All rights reserved.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  color: #333;
}

header {
  background-color: #1d3557;
  color: white;
  padding: 10px 0;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
}

.navbar h1 {
  font-size: 1.8em;
}

nav ul {
  list-style-type: none;
}

nav ul li {
  display: inline;
  margin-left: 20px;
}

nav ul li a {
  text-decoration: none;
  color: white;
  font-weight: bold;
}

.top-up-section {
  padding: 50px 20px;
  text-align: center;
}

.top-up-section .content {
  max-width: 600px;
  margin: 0 auto;
  background-color: white;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

h2 {
  margin-bottom: 20px;
}

label {
  font-size: 1.2em;
  margin-bottom: 10px;
  display: block;
}

select {
  width: 100%;
  padding: 10px;
  margin-bottom: 20px;
  font-size: 1em;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  background-color: #1d3557;
  color: white;
  padding: 10px 20px;
  border: none;
  font-size: 1em;
  cursor: pointer;
  border-radius: 4px;
}

button:hover {
  background-color: #457b9d;
}

.hidden {
  display: none;
}

footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 20px;
}
document.getElementById("topUpForm").addEventListener("submit", function (event) {
  event.preventDefault(); // Prevent form from submitting

  const diamondAmount = document.getElementById("diamondAmount").value;
  const confirmationMessage = document.getElementById("confirmationMessage");
  const amountValue = document.getElementById("amountValue");

  // Set the amount in the confirmation message
  amountValue.textContent = diamondAmount;

  // Show the confirmation message
  confirmationMessage.classList.remove("hidden");
});
