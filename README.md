<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Surprise Valentine ❤️</title>
<style>
*{box-sizing:border-box;-webkit-tap-highlight-color:transparent}
body{background-color:#fff1f2;margin:0;display:flex;justify-content:center;align-items:center;height:100vh;font-family:sans-serif;overflow:hidden}
.container{background:white;padding:30px;border-radius:25px;box-shadow:0 10px 30px rgba(251,113,133,0.2);width:85%;max-width:350px;text-align:center;border:2px solid #fecdd3;position:relative;z-index:10}
.page{display:none}
.active{display:block!important}
h1{color:#be185d;font-size:1.4rem;margin-bottom:20px}
.heart-btn{font-size:80px;cursor:pointer;display:inline-block;animation:beat 1.2s infinite}
@keyframes beat{0%,100%{transform:scale(1)}50%{transform:scale(1.1)}}
.btn{display:block;width:100%;padding:15px;margin:10px 0;border:none;border-radius:50px;background:#ec4899;color:white;font-weight:bold;cursor:pointer}
#noBtn{background:#f3f4f6;color:#9ca3af;width:80px;display:inline-block;position:relative}
img{width:100%;border-radius:15px;margin-top:15px}
</style>
</head>
<body>
<div id="p1" class="container page active">
<h1>I have a surprise for you...</h1>
<div class="heart-btn" onclick="nextPage(2)">💖</div>
<p style="color:#fb7185">Touch the heart to open</p>
</div>
<div id="p2" class="container page">
<h1>Will you be my Valentine? 🌹</h1>
<div style="display:flex;gap:10px;justify-content:center">
<button class="btn" style="width:100px" onclick="nextPage(3)">YES!</button>
<button id="noBtn" class="btn" onmouseover="dodge()">No</button>
</div>
</div>
<div id="p3" class="container page">
<h1>Pick your gift: ✨</h1>
<button class="btn" onclick="finish('Makeup 💄')">Makeup 💄</button>
<button class="btn" onclick="finish('Flowers 💐')">Flowers 💐</button>
<button class="btn" onclick="finish('Bubu ✨🐱')">Bubu (Glitter Cat) 🐱</button>
</div>
<div id="p4" class="container page">
<h1>Excellent Choice! 🥰</h1>
<p>You chose: <span id="res" style="color:#ec4899;font-weight:bold"></span></p>
<img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNHJpZzR6ZzR6ZzR6ZzR6ZzR6ZzR6ZzR6ZzR6ZzR6ZzR6ZzR6JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/KztT2c4u8mYYUiMKdJ/giphy.gif">
</div>
<script>
function nextPage(n){document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));document.getElementById('p'+n).classList.add('active')}
function dodge(){const b=document.getElementById('noBtn');b.style.position='fixed';b.style.left=Math.random()*70+'vw';b.style.top=Math.random()*70+'vh'}
function finish(item){document.getElementById('res').innerText=item;nextPage(4)}
</script>
</body>
</html>
