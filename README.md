<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Portafolio Tecnológico</title>

<style>
body{
margin:0;
font-family:Arial;
color:#fff;
background:#0a0f1c;
overflow-x:hidden;
}

/* Fondo tecnológico */
.bg-tech{
position:fixed;
width:100%;
height:100%;
overflow:hidden;
z-index:-1;
}

.bg-tech span{
position:absolute;
color:rgba(0,255,255,0.08);
font-size:20px;
animation:move 20s linear infinite;
}

@keyframes move{
from{transform:translateY(100vh);}
to{transform:translateY(-100vh);}
}

/* Header */
header{
text-align:center;
padding:40px;
}

h1{margin:0;font-size:38px;}

.frase{
font-style:italic;
opacity:0.8;
}

/* Contenedor */
.container{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
gap:20px;
padding:30px;
max-width:1100px;
margin:auto;
}

/* Carpetas */
.folder{
padding:40px;
text-align:center;
font-weight:bold;
cursor:pointer;
transition:0.3s;
clip-path:polygon(0 0,100% 0,90% 100%,10% 100%);
}

.folder:hover{
transform:scale(1.08);
}

/* Diferentes formas */
.f2{clip-path:polygon(10% 0,100% 20%,90% 100%,0 80%);}
.f3{clip-path:polygon(0 20%,100% 0,80% 100%,20% 80%);}
.f4{clip-path:polygon(20% 0,80% 0,100% 100%,0 100%);}
.f5{clip-path:polygon(0 0,100% 10%,90% 90%,10% 100%);}
.f6{clip-path:polygon(10% 10%,90% 0,100% 90%,0 100%);}
.f7{clip-path:polygon(0 0,90% 0,100% 100%,10% 100%);}
.f8{clip-path:polygon(0 10%,100% 0,100% 90%,0 100%);}
.f9{clip-path:polygon(10% 0,100% 0,90% 100%,0 90%);}
.f10{clip-path:polygon(0 0,100% 0,80% 100%,20% 100%);}

/* Colores */
.s1{background:linear-gradient(45deg,#ff6a00,#ee0979);}
.s2{background:linear-gradient(45deg,#00c6ff,#0072ff);}
.s3{background:linear-gradient(45deg,#f7971e,#ffd200);}
.s4{background:linear-gradient(45deg,#43e97b,#38f9d7);}
.s5{background:linear-gradient(45deg,#fa709a,#fee140);}
.s6{background:linear-gradient(45deg,#a18cd1,#fbc2eb);}
.s7{background:linear-gradient(45deg,#30cfd0,#330867);}
.s8{background:linear-gradient(45deg,#667eea,#764ba2);}
.s9{background:linear-gradient(45deg,#ff9966,#ff5e62);}
.s10{background:linear-gradient(45deg,#00f260,#0575e6);}

/* Modal */
.modal{
display:none;
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,0.85);
justify-content:center;
align-items:center;
}

.modal-content{
background:#111;
padding:30px;
border-radius:10px;
text-align:center;
}

button{
padding:10px 20px;
border:none;
margin-top:15px;
background:linear-gradient(45deg,#ff7e5f,#feb47b);
color:#fff;
cursor:pointer;
border-radius:5px;
}
</style>
</head>

<body>

<div class="bg-tech" id="bg"></div>

<header>
<h1>Portafolio Tecnológico</h1>
<p class="frase">"Scientia potentia est — El conocimiento es poder en la era digital"</p>
</header>

<div class="container">

<div class="folder s1" onclick="openF(1)">Semestre 1</div>
<div class="folder s2 f2" onclick="openF(2)">Semestre 2</div>
<div class="folder s3 f3" onclick="openF(3)">Semestre 3</div>
<div class="folder s4 f4" onclick="openF(4)">Semestre 4</div>
<div class="folder s5 f5" onclick="openF(5)">Semestre 5</div>
<div class="folder s6 f6" onclick="openF(6)">Semestre 6</div>
<div class="folder s7 f7" onclick="openF(7)">Semestre 7</div>
<div class="folder s8 f8" onclick="openF(8)">Semestre 8</div>
<div class="folder s9 f9" onclick="openF(9)">Semestre 9</div>
<div class="folder s10 f10" onclick="openF(10)">Semestre 10</div>

</div>

<div class="modal" id="modal">
<div class="modal-content">
<h2 id="title"></h2>
<p>Contenido del semestre seleccionado.</p>
<button onclick="closeF()">Cerrar</button>
</div>
</div>

<script>
// Fondo tecnológico con palabras
const words=["HTML","CSS","JS","AI","DATA","CODE","TECH","WEB"];
const bg=document.getElementById("bg");

for(let i=0;i<40;i++){
let span=document.createElement("span");
span.innerText=words[Math.floor(Math.random()*words.length)];
span.style.left=Math.random()*100+"%";
span.style.fontSize=(15+Math.random()*25)+"px";
span.style.animationDuration=(10+Math.random()*20)+"s";
bg.appendChild(span);
}

// Abrir carpeta
function openF(n){
document.getElementById("modal").style.display="flex";
document.getElementById("title").innerText="Semestre "+n;
}

// Cerrar
function closeF(){
document.getElementById("modal").style.display="none";
}
</script>

</body>
</html>
