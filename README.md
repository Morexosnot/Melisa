<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Melisa İçin ❤️</title>
<style>
body{
  margin:0;
  font-family: 'Segoe UI', sans-serif;
  background: linear-gradient(135deg,#1e1e2f,#ff4e8a);
  color:white;
  text-align:center;
  overflow:hidden;
}
.screen{
  position:absolute;
  width:100%;
  height:100%;
  display:flex;
  justify-content:center;
  align-items:center;
  flex-direction:column;
}
input{
  padding:12px;
  border-radius:25px;
  border:none;
  text-align:center;
  font-size:1rem;
  margin-top:10px;
}
button{
  margin-top:15px;
  padding:12px 25px;
  border:none;
  border-radius:25px;
  background:white;
  color:#ff4e8a;
  font-weight:bold;
  cursor:pointer;
  transition:0.3s;
}
button:hover{
  transform:scale(1.1);
}
.hidden{
  display:none;
}
.content{
  padding:40px 20px;
  animation: fadeIn 2s ease-in-out;
}
@keyframes fadeIn{
  from{opacity:0; transform:translateY(20px);}
  to{opacity:1; transform:translateY(0);}
}
.heart{
  position:fixed;
  color:white;
  animation: float 6s linear infinite;
}
@keyframes float{
  from{transform:translateY(100vh);}
  to{transform:translateY(-10vh);}
}
</style>
</head>
<body>

<!-- Şifre Ekranı -->
<div class="screen" id="login">
  <h2>Bu site sadece Melisa için ❤️</h2>
  <p>Şifreyi gir</p>
  <input type="password" id="password" placeholder="Şifre">
  <button onclick="checkPassword()">Giriş Yap</button>
</div>

<!-- İçerik -->
<div class="screen hidden" id="main">
  <div class="content">
    <h1>Melisa ❤️</h1>
    <p>
      Hayatıma girdiğin günden beri dünya daha anlamlı.
      Sesin huzur, gülüşün mutluluk, varlığın ise en büyük şansım.
    </p>
    <p>
      Bazen kelimeler yetmez ama şunu bil:
      Sen benim en güzel duam,
      en değerli gerçeğim,
      en çok sevdiğim hikâyemsin.
    </p>
    <p style="font-size:1.5rem;">
      Seni her şeyden çok seviyorum.
    </p>
  </div>
</div>

<!-- Müzik (Gizli YouTube Embed) -->
<iframe width="0" height="0" 
src="https://youtu.be/7F8ew3WyUeA?si=CWgbetI8eSJC1kB_" 
frameborder="0" allow="autoplay">
</iframe>

<script>
function checkPassword(){
  const pass = document.getElementById("password").value;
  if(pass === "melisa123"){
    document.getElementById("login").classList.add("hidden");
    document.getElementById("main").classList.remove("hidden");
  } else {
    alert("Yanlış şifre ❤️");
  }
}

function createHeart(){
  const heart = document.createElement("div");
  heart.className="heart";
  heart.style.left=Math.random()*100+"vw";
  heart.style.fontSize=(Math.random()*20+10)+"px";
  heart.innerHTML="❤️";
  document.body.appendChild(heart);
  setTimeout(()=>{heart.remove();},6000);
}
setInterval(createHeart,300);
</script>

</body>
</html>
