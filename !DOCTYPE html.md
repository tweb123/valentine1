<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<title>Be My Valentine 💕</title>  
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&family=Poppins:wght@300;400&display=swap" rel="stylesheet">  
  
<style>  
* { box-sizing: border-box; }  
  
body {  
  margin: 0;  
  height: 100vh;  
  background: radial-gradient(circle at top, #ffe6ec, #ff9eb5);  
  display: flex;  
  justify-content: center;  
  align-items: center;  
  font-family: 'Poppins', sans-serif;  
  overflow: hidden;  
}  
  
.card {  
  background: rgba(255,255,255,0.95);  
  padding: 50px;  
  border-radius: 30px;  
  text-align: center;  
  width: 360px;  
  box-shadow: 0 25px 60px rgba(0,0,0,0.25);  
  animation: fadeIn 2s ease;  
}  
  
h1 {  
  font-family: 'Playfair Display', serif;  
  color: #ff4d6d;  
  font-size: 2.6em;  
  margin-bottom: 10px;  
}  
  
h2 {  
  color: #444;  
  font-weight: 400;  
  margin-top: 0;  
}  
  
p {  
  color: #666;  
  font-size: 1.05em;  
  margin: 15px 0;  
}  
  
button {  
  margin: 12px;  
  padding: 14px 32px;  
  font-size: 1.05em;  
  border: none;  
  border-radius: 40px;  
  cursor: pointer;  
  background: linear-gradient(135deg, #ff4d6d, #ff7a9c);  
  color: white;  
  transition: transform 0.2s, box-shadow 0.2s;  
}  
  
button:hover {  
  transform: scale(1.08);  
  box-shadow: 0 10px 25px rgba(255,77,109,0.5);  
}  
  
.signature {  
  margin-top: 20px;  
  font-style: italic;  
  color: #888;  
}  
  
/* Floating hearts */  
.heart {  
  position: absolute;  
  color: #ff4d6d;  
  font-size: 22px;  
  animation: floatUp linear infinite;  
}  
  
@keyframes floatUp {  
  from { transform: translateY(110vh); opacity: 0; }  
  30% { opacity: 1; }  
  to { transform: translateY(-10vh); opacity: 0; }  
}  
  
@keyframes fadeIn {  
  from { opacity: 0; transform: scale(0.9); }  
  to { opacity: 1; transform: scale(1); }  
}  
  
/* Confetti */  
.confetti {  
  position: absolute;  
  width: 10px;  
  height: 10px;  
  background: pink;  
  animation: confettiFall 3s linear forwards;  
}  
  
@keyframes confettiFall {  
  from { transform: translateY(-10vh) rotate(0deg); }  
  to { transform: translateY(110vh) rotate(720deg); }  
}  
</style>  
</head>  
  
<body>  
  
<audio autoplay loop>  
  <source src="https://cdn.pixabay.com/audio/2022/10/16/audio_1d3b9e8e43.mp3" type="audio/mpeg">  
</audio>  
  
<div class="card">  
  <h1>💖 Saylor Henry 💖</h1>  
  <h2>Will you be my Valentine?</h2>  
  
  <p>  
    Every day with you feels a little brighter,<br>  
    a little sweeter, and a lot more special.  
  </p>  
  
  <button onclick="yesClicked()">Yes 💕</button>  
  <button onclick="yesClicked()">Obviously 💘</button>  
  
  <div class="signature">  
    — Love, Turner Weber  
  </div>  
</div>  
  
<script>  
// Floating hearts  
for (let i = 0; i < 40; i++) {  
  let heart = document.createElement("div");  
  heart.className = "heart";  
  heart.innerHTML = "❤️";  
  heart.style.left = Math.random() * 100 + "vw";  
  heart.style.animationDuration = (Math.random() * 4 + 4) + "s";  
  heart.style.fontSize = (Math.random() * 15 + 15) + "px";  
  document.body.appendChild(heart);  
}  
  
// Confetti + message  
function yesClicked() {  
  alert("You just made my Valentine perfect ❤️");  
  
  for (let i = 0; i < 80; i++) {  
    let confetti = document.createElement("div");  
    confetti.className = "confetti";  
    confetti.style.left = Math.random() * 100 + "vw";  
    confetti.style.background = ["#ff4d6d","#ffd1dc","#ff9eb5","#ffe6ec"][Math.floor(Math.random()*4)];  
    confetti.style.animationDuration = (Math.random() * 2 + 2) + "s";  
    document.body.appendChild(confetti);  
  
    setTimeout(() => confetti.remove(), 3000);  
  }  
}  
</script>  
  
</body>  
</html>  
