<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>سکه جمع کن</title>
  <style>
    body {
      margin: 0;
      font-family: Tahoma, sans-serif;
      background: radial-gradient(#1e085d, #000);
      color: white;
      text-align: center;
      direction: rtl;
    }
    .coin-display {
      font-size: 2em;
      margin-top: 1.5em;
    }
    .coin-display img {
      width: 150px;
      margin-top: 1em;
    }
    .energy {
      color: yellow;
      margin: 1em;
    }
    .buttons {
      display: flex;
      justify-content: center;
      gap: 1em;
      margin-top: 2em;
    }
    button {
      padding: 1em 2em;
      font-size: 1em;
      border: none;
      border-radius: 15px;
      cursor: pointer;
      background: #4422a1;
      color: white;
      transition: background 0.3s;
    }
    button:hover {
      background: #5c35e0;
    }
    .status {
      margin-top: 1em;
      font-size: 1.2em;
      color: #ccc;
    }
  </style>
</head>
<body>
  <div class="coin-display">
    <div>سکه‌ها: <span id="coins">20000</span></div>
    <div style="color:silver;">نقره‌ای</div>
    <img src="https://i.imgur.com/o7Jb12h.png" alt="coin" />
  </div>

  <div class="energy">انرژی: <span id="energy">1500</span>/1500 ⚡</div>

  <div class="buttons">
    <button onclick="earnCoins()">جمع آوری سکه</button>
    <button onclick="alert('دوستانت را دعوت کن!')">فرندز</button>
    <button onclick="alert('بوست فعال شد!')">بوست</button>
  </div>

  <div class="status" id="status">30 سکه گرفتی!</div>

  <script>
    let coins = 20000;
    let energy = 1500;

    function earnCoins() {
      if (energy >= 100) {
        coins += 30;
        energy -= 100;
        document.getElementById('coins').textContent = coins;
        document.getElementById('energy').textContent = energy;
        document.getElementById('status').textContent = '30 سکه گرفتی!';
      } else {
        document.getElementById('status').textContent = 'انرژی کافی نیست!';
      }
    }
  </script>
</body>
</html>
