<!DOCTYPE html><html><head><title>🗿</title><link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet"><style>
body{font-family:'Press Start 2P',sans-serif;background:#000;color:#fff;margin:0;padding:20px;text-align:center}
h1{color:lime;font-size:20px;margin-bottom:40px}
.players{display:flex;flex-wrap:wrap;justify-content:center;gap:20px}
.player{background:#222;border:2px solid lime;padding:20px;width:300px;box-sizing:border-box}
.player h2{color:yellow;font-size:16px;margin-top:0;cursor:pointer}
.player p{margin:10px 0;font-size:10px}
#imageView{display:none;position:fixed;top:0;left:0;width:100vw;height:100vh;background:#000;z-index:1000;justify-content:center;align-items:center;flex-direction:column}
#imageView img{max-width:90%;max-height:80vh;border:2px solid #fff}
#backArrow{color:lime;font-size:16px;margin-top:20px;cursor:pointer}
</style></head><body>
<h1>🛡️ Hypixel SkyBlock Progress</h1>
<div class="players">
<div class="player"><h2>Dani</h2><p>Combat: XIII</p><p>Farming: XX</p><p>Slayer: Revenant T3</p><p>Pets: Griffin</p><p>SkyBlock level: 26</p><p>Minions: 7</p></div>
<div class="player"><h2 onclick="(()=>{document.getElementById('imageView').style.display='flex'})()">Slav</h2><p>Combat: VIII</p><p>Farming: VII</p><p>Slayer: Revenant T2</p><p>Pets: no</p><p>SkyBlock level: 4</p><p>Minions: 6</p></div>
</div>
<div id="imageView">
<img src="https://i.ibb.co/pFDXwbg/image.png" alt="Slav Image">
<div id="backArrow" onclick="(()=>{document.getElementById('imageView').style.display='none'})()">← Back</div>
</div>
</body></html>
// Node.js (Express.js server)
const express = require('express');
const stripe = require('stripe')('your-secret-key');
const app = express();
const cors = require('cors');
app.use(cors());

app.get('/create-checkout-session', async (req, res) => {
  const session = await stripe.checkout.sessions.create({
    payment_method_types: ['card'],
    line_items: [{
      price_data: {
        currency: 'usd',
        product_data: {
          name: 'SkyBlock PRO Tutorial'
        },
        unit_amount: 199, // $1.99
      },
      quantity: 1,
    }],
    mode: 'payment',
    success_url: 'https://yourdomain.com/success',
    cancel_url: 'https://yourdomain.com',
  });
  res.json({ url: session.url });
});

app.listen(3000, () => console.log('Server ready'));

