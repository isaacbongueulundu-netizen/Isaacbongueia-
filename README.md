# Isaacbongueia
<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Isabongue IA Pro</title>

<style>
body{
background:#0b1220;
font-family:Arial;
color:white;
display:flex;
justify-content:center;
align-items:center;
height:100vh;
margin:0;
}

.chat{
width:420px;
height:650px;
background:#18253d;
border-radius:20px;
display:flex;
flex-direction:column;
overflow:hidden;
}

.top{
background:#2563eb;
padding:15px;
font-size:24px;
text-align:center;
font-weight:bold;
}

#msgs{
flex:1;
overflow:auto;
padding:10px;
}

.user{
background:#2563eb;
padding:10px;
margin:8px;
border-radius:15px;
text-align:right;
}

.bot{
background:#374151;
padding:10px;
margin:8px;
border-radius:15px;
}

.bottom{
display:flex;
}

input{
flex:1;
padding:15px;
border:none;
font-size:16px;
}

button{
width:90px;
background:#2563eb;
color:white;
border:none;
font-size:18px;
}
</style>

</head>

<body>

<div class="chat">

<div class="top">
🤖 Isabongue IA Pro
</div>

<div id="msgs">
<div class="bot">
Olá Isaac! Sou a Isabongue IA Pro. Pergunte qualquer coisa.
</div>
</div>

<div class="bottom">
<input id="txt" placeholder="Escreva aqui...">
<button onclick="enviar()">Enviar</button>
</div>

</div>

<script>

function responder(t){

t=t.toLowerCase();

if(t.includes("olá")||t.includes("oi"))
return "Olá Isaac! Como posso ajudar?";

if(t.includes("nome"))
return "Sou a Isabongue IA Pro.";

if(t.includes("criador"))
return "Fui criada por Isaac Bongue.";

if(t.includes("jesus"))
return "Jesus Cristo é o Salvador do mundo.";

if(t.includes("bíblia"))
return "Versículo: João 3:16.";

if(t.includes("html"))
return "Posso ajudar a criar sites em HTML.";

if(t.includes("python"))
return "Também posso ajudar com Python.";

if(t.includes("minecraft"))
return "Minecraft é um excelente jogo para criatividade.";

if(t.includes("tchau"))
return "Até logo! Deus te abençoe.";

return "Ainda estou aprendendo. Em breve terei respostas muito mais inteligentes.";
}

function enviar(){

let txt=document.getElementById("txt");

if(txt.value=="") return;

let msgs=document.getElementById("msgs");

msgs.innerHTML+="<div class='user'>"+txt.value+"</div>";

setTimeout(function(){

msgs.innerHTML+="<div class='bot'>"+responder(txt.value)+"</div>";

msgs.scrollTop=msgs.scrollHeight;

},400);

txt.value="";

}

</script>

</body>
</html>
