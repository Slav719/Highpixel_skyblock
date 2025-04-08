# Highpixel_skyblock
<!DOCTYPE html>
<html>
<head>
  <title>SkyBlock Progress</title>
  <link href="https://fonts.cdnfonts.com/css/minecraftia" rel="stylesheet">
  <style>
    body {
      font-family: 'Minecraftia', sans-serif;
      background-color: black;
      color: white;
      text-align: center;
    }

    .player {
      width: 45%;
      display: inline-block;
      background-color: #222;
      margin: 10px;
      padding: 10px;
      border: 2px solid lime;
    }

    h1 {
      color: lime;
    }

    h2 {
      color: yellow;
      cursor: pointer;
    }

    p {
      margin: 5px;
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
    }

    #backArrow {
      color: lime;
      font-size: 24px;
      margin-top: 20px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Hypixel SkyBlock Progress</h1>

  <div class="player">
    <h2 onclick="showImage1()
    <h2>Dani</h2>
    <p>Combat: XIII</p>
    <p>Farming: XX</p>
    <p>Slayer: Revenant T3</p>
    <p>Pets: Griffin</p>
    <p>SkyBlock level: 26</p>
    <p>Minions: 7</p>
  </div>

  <div class="player">
    <h2 onclick="showImage2()">Slav</h2>
    <p>Combat: VIII</p>
    <p>Farming: VII</p>
    <p>Slayer: Revenant T2</p>
    <p>Pets: no</p>
    <p>SkyBlock level: 4</p>
    <p>Minions: 6</p>
  </div>

  <div id="imageView">
    <img src="" alt="Slav Image">
    <div id="backArrow" onclick="hideImage1()">← Back</div>
  </div>

  <script>
    function showImage1("C:\Users\Acer\Documents\ViberDownloads\clipboard_image_25e107b4ca6b5ffc.jpg") {
      document.getElementById('imageView').style.display = 'flex';
    }

    function hideImage() {
      document.getElementById('imageView').style.display = 'none';
    }
  </script>
</body>
</html>
