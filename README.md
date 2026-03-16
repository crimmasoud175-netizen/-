<!DOCTYPE html>
<html>

<head>

<meta charset="UTF-8">

<title>燕子高飞 Token</title>

<style>

body{
margin:0;
font-family:Arial;
background:#020617;
color:white;
text-align:center;
overflow-x:hidden;
}

canvas{
position:fixed;
top:0;
left:0;
z-index:-1;
}

header{
padding:120px 20px;
}

h1{
font-size:60px;
background:linear-gradient(90deg,#38bdf8,#a78bfa,#38bdf8);
-webkit-background-clip:text;
color:transparent;
}

.subtitle{
font-size:22px;
color:#cbd5f5;
}

.logo{
width:140px;
margin-bottom:20px;
}

.buy-btn{
margin-top:30px;
padding:18px 60px;
font-size:20px;
border:none;
border-radius:12px;
background:linear-gradient(90deg,#38bdf8,#a78bfa);
color:white;
cursor:pointer;
box-shadow:0 0 25px #38bdf8;
transition:0.3s;
}

.buy-btn:hover{
transform:scale(1.1);
box-shadow:0 0 50px #a78bfa;
}

section{
padding:90px 20px;
}

.card{
background:rgba(30,41,59,0.85);
padding:30px;
border-radius:16px;
max-width:500px;
margin:auto;
box-shadow:0 0 30px rgba(56,189,248,0.4);
}

h2{
font-size:34px;
margin-bottom:30px;
}

.links a{
display:block;
margin:12px;
font-size:18px;
color:#38bdf8;
text-decoration:none;
}

.links a:hover{
color:#a78bfa;
}

footer{
padding:40px;
margin-top:60px;
background:#020617;
}

.chart{
margin-top:40px;
}

</style>

</head>

<body>

<canvas id="stars"></canvas>

<header>

<img src="logo.png" class="logo">

<h1>燕子高飞</h1>

<p class="subtitle">Meme Token on BNB Smart Chain</p>

<button class="buy-btn" onclick="buy()">立即购买</button>

</header>

<section>

<h2>Token 信息</h2>

<div class="card">

<p><b>名称:</b> 燕子高飞</p>

<p><b>符号:</b> YZGF</p>

<p><b>总供应:</b> 1,000,000</p>

<p><b>税率:</b> 0%</p>

<p><b>流动性:</b> 已锁定</p>

<p><b>合约地址:</b></p>

<p style="word-break:break-all">

0x1f4e033b45e03fbceb52e869c43b422c8ef6e1e1

</p>

</div>

</section>

<section>

<h2>实时行情</h2>

<div class="chart">

<iframe 
src="https://dexscreener.com/bsc/0x1f4e033b45e03fbceb52e869c43b422c8ef6e1e1?embed=1"
width="90%" 
height="500">
</iframe>

</div>

</section>

<section>

<h2>社区</h2>

<div class="card links">

<a href="#">Telegram</a>

<a href="#">Twitter</a>

<a href="https://bscscan.com/token/0x1f4e033b45e03fbceb52e869c43b422c8ef6e1e1">BscScan</a>

</div>

</section>

<footer>

<p>© 2026 燕子高飞 Token</p>

</footer>

<script>

function buy(){

window.open(
"https://pancakeswap.finance/swap?outputCurrency=0x1f4e033b45e03fbceb52e869c43b422c8ef6e1e1"
)

}

var canvas=document.getElementById("stars");
var ctx=canvas.getContext("2d");

canvas.width=window.innerWidth;
canvas.height=window.innerHeight;

var stars=[];

for(let i=0;i<200;i++){
stars.push({
x:Math.random()*canvas.width,
y:Math.random()*canvas.height,
r:Math.random()*2
})
}

function draw(){

ctx.clearRect(0,0,canvas.width,canvas.height);

ctx.fillStyle="white";

stars.forEach(s=>{
ctx.beginPath();
ctx.arc(s.x,s.y,s.r,0,Math.PI*2);
ctx.fill();
})

requestAnimationFrame(draw)
}

draw();

</script>

</body>

</html>
