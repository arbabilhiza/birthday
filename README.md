<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Sayang ❤️</title>

<style>

body{
margin:0;
font-family: 'Segoe UI', sans-serif;
background: linear-gradient(135deg,#ff4d6d,#ff8fa3);
color:white;
text-align:center;
overflow-x:hidden;
}

.container{
padding:60px 20px;
}

h1{
font-size:55px;
margin-bottom:10px;
}

h2{
font-weight:300;
}

button{
padding:15px 35px;
font-size:18px;
border:none;
border-radius:40px;
background:white;
color:#ff4d6d;
cursor:pointer;
margin-top:30px;
transition:0.3s;
}

button:hover{
transform:scale(1.1);
}

#message{
display:none;
max-width:600px;
margin:auto;
margin-top:40px;
font-size:20px;
line-height:1.7;
animation:fade 2s;
}

img{
width:260px;
border-radius:20px;
margin-top:25px;
box-shadow:0 10px 30px rgba(0,0,0,0.3);
}

@keyframes fade{
from{opacity:0}
to{opacity:1}
}

/* animasi hati */

.heart{
position:fixed;
top:-10px;
color:pink;
font-size:20px;
animation:fall linear infinite;
}

@keyframes fall{
to{
transform:translateY(110vh);
}
}

footer{
margin-top:60px;
opacity:0.8;
}

</style>
</head>

<body>

<div class="container">

<h1>Happy Birthday 🎂</h1>
<h2 id="nama">Untuk Kamu, Sayang ❤️</h2>

<p id="countdown"></p>

<button onclick="showLove()">Klik Untuk Kejutan 💌</button>

<div id="message">

<img src="foto.jpg">

<p>
Selamat ulang tahun cintaku ❤️<br><br>

Terima kasih sudah hadir dalam hidupku,  
terima kasih sudah jadi alasan aku tersenyum setiap hari.<br><br>

Semoga semua impian kamu tercapai,  
semoga kebahagiaan selalu menyertai kamu.<br><br>

Dan aku berharap...  
aku masih jadi orang yang menemani kamu  
di ulang tahunmu yang berikutnya, dan berikutnya lagi. ❤️<br><br>

I love you forever 💕
</p>

</div>

<footer>
dibuat khusus untuk kamu ✨
</footer>

</div>

<audio autoplay loop>
<source src="musik.mp3" type="audio/mpeg">
</audio>

<script>

/* tombol pesan */

function showLove(){
document.getElementById("message").style.display="block";
}

/* countdown */

var birthday = new Date("2026-12-25").getTime();

setInterval(function(){

var now = new Date().getTime();
var distance = birthday - now;

var days = Math.floor(distance / (1000 * 60 * 60 * 24));

document.getElementById("countdown").innerHTML =
"Menuju ulang tahun kamu: " + days + " hari lagi 🎉";

},1000);

/* animasi hati */

function createHeart(){
const heart=document.createElement("div");
heart.classList.add("heart");
heart.innerHTML="❤";
heart.style.left=Math.random()*100+"vw";
heart.style.animationDuration=(Math.random()*3+3)+"s";
document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},6000);
}

setInterval(createHeart,300);

</script>

</body>
</html>
