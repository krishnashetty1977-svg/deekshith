# deekshith <!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A Small Message</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
background:#0f172a;
color:white;
display:flex;
justify-content:center;
align-items:center;
height:100vh;
padding:20px;
}

.card{
max-width:500px;
width:100%;
background:#1e293b;
padding:35px;
border-radius:20px;
box-shadow:0 0 30px rgba(0,0,0,.5);
text-align:center;
}

h1{
margin-bottom:25px;
color:#60a5fa;
}

#text{
font-size:20px;
line-height:1.8;
min-height:180px;
}

button{
margin-top:25px;
padding:12px 28px;
font-size:18px;
border:none;
border-radius:30px;
cursor:pointer;
background:#3b82f6;
color:white;
}

button:hover{
background:#2563eb;
}

.fade{
animation:fade .8s;
}

@keyframes fade{
from{opacity:0;transform:translateY(20px);}
to{opacity:1;transform:translateY(0);}
}
</style>
</head>

<body>

<div class="card">

<h1>📩 One Small Message</h1>

<div id="text" class="fade">
Hi...<br><br>
I wanted to tell you something today.<br>
Please don't close this page yet. 🙂
</div>

<button onclick="next()">Continue ➜</button>

</div>

<script>

let page=0;

const messages=[

`Sometimes we remember dates without even trying.<br><br>
Not because they're written on a calendar...<br>
but because they're connected to someone.`,

`Out of millions of moments this year...<br><br>
Today quietly stood out.<br>
Maybe you know why... maybe you don't.`,

`I wasn't planning to make a big announcement.<br><br>
I just wanted you to know that someone remembered today. 😊`,

`🎂 <h2>Happy Birthday Deepthi C U</h2>

I hope this year surprises you in the best possible ways.

May your smile stay genuine,
your dreams become reality,
and your heart always find reasons to be happy.

Keep shining,
keep believing in yourself,
and never stop being the wonderful person you are.

✨ Have a beautiful birthday. ❤️`

];

function next(){

if(page<messages.length){

document.getElementById("text").classList.remove("fade");

setTimeout(()=>{

document.getElementById("text").innerHTML=messages[page];

document.getElementById("text").classList.add("fade");

page++;

if(page==messages.length){

document.querySelector("button").innerHTML="😊 Thank You";

}

},200);

}else{

document.body.innerHTML=`<div style="display:flex;justify-content:center;align-items:center;height:100vh;background:#000;color:white;font-size:28px;text-align:center;padding:20px;">
✨ Hope this little surprise made you smile.<br><br>
Once Again...<br>
🎂 Happy Birthday Deepthi C U ❤️
</div>`;

}

}

</script>

</body>
</html>
