<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SkyBlock Progress</title>
  <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Press Start 2P', cursive;
      background-color: black;
      color: white;
      margin: 0;
      padding: 20px;
      text-align: center;
    }
    h1 {
      color: lime;
      font-size: 20px;
      margin-bottom: 40px;
    }
    .players {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
    }
    .player {
      background-color: #222;
      border: 2px solid lime;
      padding: 20px;
      width: 300px;
      box-sizing: border-box;
    }
    .player h2 {
      color: yellow;
      font-size: 16px;
      margin-top: 0;
    }
    .player p {
      margin: 10px 0;
      font-size: 10px;
    }
    #imageView {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background-color: black;
      z-index: 1000;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }
    #imageView img {
      max-width: 90%;
      max-height: 80vh;
      border: 2px solid white;
    }
    #backArrow {
      color: lime;
      font-size: 16px;
      margin-top: 20px;
      cursor: pointer;
    }
    .buy-button {
      margin-top: 40px;
      padding: 15px 25px;
      font-size: 12px;
      background-color: lime;
      color: black;
      border: none;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Hypixel SkyBlock Progress</h1>
  <div class="players">
    <div class="player">
      <h2>Dani</h2>
      <p>Combat: XIII</p>
      <p>Farming: XX</p>
      <p>Slayer: Revenant T3</p>
      <p>Pets: Griffin</p>
      <p>SkyBlock level: 26</p>
      <p>Minions: 7</p>
    </div>
    <div class="player">
      <h2 onclick="showImage()">Slav</h2>
      <p>Combat: VIII</p>
      <p>Farming: VII</p>
      <p>Slayer: Revenant T2</p>
      <p>Pets: no</p>
      <p>SkyBlock level: 4</p>
      <p>Minions: 6</p>
    </div>
  </div>

  <button class="buy-button" onclick="buyTutorial()">Unlock Tutorial – $1.99</button>

  <div id="imageView">
    <img src="https://i.ibb.co/pFDXwbg/image.png" alt="Slav Image">
    <div id="backArrow" onclick="hideImage()">← Back</div>
  </div>

  <script>
    function showImage() {
      document.getElementById('imageView').style.display = 'flex';
    }
    function hideImage() {
      document.getElementById('imageView').style.display = 'none';
    }
    async function buyTutorial() {
      const res = await fetch('https://your-backend.com/create-checkout-session');
      const data = await res.json();
      window.location.href = data.url;
    }
  </script>
</body>
</html>
