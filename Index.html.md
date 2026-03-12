<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>For Aanya ❤️</title>  
<style>  
body{  
margin:0;  
font-family:Arial;  
text-align:center;  
background:linear-gradient(135deg,#ff4e8a,#ff7eb3,#ffb6c1);  
background-size:400% 400%;  
animation:bg 10s infinite alternate;  
color:white;  
overflow-x:hidden;  
}  
  
@keyframes bg{  
0%{background-position:0% 50%;}  
100%{background-position:100% 50%;}  
}  
  
.startScreen{  
position:fixed;  
top:0;  
left:0;  
width:100%;  
height:100%;  
background:#ff4e8a;  
display:flex;  
flex-direction:column;  
justify-content:center;  
align-items:center;  
z-index:10;  
}  
  
.startScreen h2{  
font-size:35px;  
}  
  
button{  
padding:14px 30px;  
border:none;  
border-radius:30px;  
margin:10px;  
font-size:18px;  
cursor:pointer;  
}  
  
.yes{  
background:white;  
color:#ff2e63;  
}  
  
.no{  
background:#ff2e63;  
color:white;  
position:relative;  
}  
  
.main{  
display:none;  
}  
  
h1{  
font-size:55px;  
margin-top:40px;  
}  
  
.slider{  
width:90%;  
max-width:500px;  
margin:40px auto;  
overflow:hidden;  
border-radius:20px;  
box-shadow:0 15px 40px rgba(0,0,0,0.3);  
}  
  
.slides{  
display:flex;  
width:500%;  
animation:slide 20s infinite;  
}  
  
.slides img{  
width:100%;  
}  
  
@keyframes slide{  
0%{margin-left:0}  
20%{margin-left:0}  
25%{margin-left:-100%}  
45%{margin-left:-100%}  
50%{margin-left:-200%}  
70%{margin-left:-200%}  
75%{margin-left:-300%}  
90%{margin-left:-300%}  
100%{margin-left:-400%}  
}  
  
.letter{  
width:85%;  
max-width:600px;  
margin:auto;  
font-size:20px;  
background:rgba(255,255,255,0.15);  
padding:25px;  
border-radius:15px;  
}  
  
.heart{  
position:fixed;  
color:#ff2e63;  
font-size:25px;  
animation:float 6s linear infinite;  
}  
  
@keyframes float{  
0%{transform:translateY(100vh);opacity:1}  
100%{transform:translateY(-10vh);opacity:0}  
}  
  
.timer{  
margin-bottom:20px;  
font-size:20px;  
}  
</style>  
</head>  
<body>  
<div class="startScreen" id="start">  
<h2>Aanya 💗</h2>  
<p>Do you want to see something special?</p>  
  
YES  
NO  
  
</div>  
<div class="main" id="main">  
<h1>I LOVE YOU FOREVER AANYA 💗</h1>  
<div class="timer" id="timeTogether"></div>  
<div class="slider">  
<div class="slides">  
<img src="IMG_0694.jpeg">  
<img src="IMG_0698.jpeg">  
<img src="IMG_0708.jpeg">  
<img src="IMG_0715.jpeg">  
<img src="IMG_0500.jpeg">  
</div>  
</div>  
<div class="letter" id="loveLetter"></div>  
<audio autoplay loop>  
<source src="music.mp3" type="audio/mp3">  
</audio>  
</div>  
<script>  
  
const message="Aanya, every moment with you feels like a memory I never want to forget. Your smile, your eyes, the way you look at me… everything about you makes my world brighter. I just want you to know one thing — I love you forever. ❤️";  
  
let i=0;  
  
function type(){  
if(i<message.length){  
document.getElementById("loveLetter").innerHTML+=message.charAt(i);  
i++;  
setTimeout(type,40);  
}  
}  
  
function openSite(){  
document.getElementById("start").style.display="none";  
document.getElementById("main").style.display="block";  
type();  
  
for(let i=0;i<30;i++){  
createHeart();  
}  
}  
  
function createHeart(){  
const heart=document.createElement("div");  
heart.classList.add("heart");  
heart.innerHTML="💗";  
heart.style.left=Math.random()*100+"vw";  
heart.style.fontSize=(20+Math.random()*30)+"px";  
document.body.appendChild(heart);  
  
setTimeout(()=>{  
heart.remove();  
},6000);  
}  
  
setInterval(createHeart,400);  
  
const noBtn=document.getElementById("noBtn");  
  
noBtn.addEventListener("mouseover",()=>{  
const x=Math.random()*300-150;  
const y=Math.random()*300-150;  
noBtn.style.transform=`translate(${x}px,${y}px)`;  
});  
  
const startDate=new Date("2024-02-14");  
  
function update(){  
const now=new Date();  
const diff=now-startDate;  
  
const days=Math.floor(diff/(1000*60*60*24));  
const hours=Math.floor(diff/(1000*60*60)%24);  
const minutes=Math.floor(diff/(1000*60)%60);  
  
document.getElementById("timeTogether").innerHTML=  
days+" days "+hours+" hours "+minutes+" minutes with you ❤️";  
}  
  
setInterval(update,1000);  
  
</script>  
</body>  
</html>  
