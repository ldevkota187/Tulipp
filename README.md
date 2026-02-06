<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>For Tulippp 🌷</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
    }

    .card {
      background: white;
      padding: 30px;
      border-radius: 20px;
      text-align: center;
      max-width: 350px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
      animation: fadeIn 2s;
    }

    h1 {
      color: #ff4b5c;
    }

    p {
      font-size: 16px;
      color: #444;
    }

    .buttons {
      margin-top: 20px;
      position: relative;
      height: 60px;
    }

    button {
      padding: 12px 20px;
      font-size: 16px;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      position: absolute;
    }

    #yes {
      background: #ff4b5c;
      color: white;
      left: 50%;
      transform: translateX(-50%);
    }

    #no {
      background: #ddd;
      color: #333;
      left: 10%;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }

    .heart {
      position: fixed;
      bottom: -20px;
      font-size: 20px;
      animation: floatUp 4s linear infinite;
      color: #ff4b5c;
    }

    @keyframes floatUp {
      0% { transform: translateY(0); opacity: 1; }
      100% { transform: translateY(-100vh); opacity: 0; }
    }
  </style>
</head>
<body>

<div class="card" id="card">
  <h1>Tulippp 🌷</h1>
  <p>
    From the moment I started talking to you,<br>
    something felt special.<br><br>
    Timro presence le mero din ramro banaucha 💕
  </p>

  <p><strong>Will you be mine?</strong></p>

  <div class="buttons">
    <button id="yes" onclick="yesClick()">YES 💖</button>
    <button id="no" onmouseover="moveNo()">NO 🙈</button>
  </div>
</div>

<script>
  function moveNo() {
    const noBtn = document.getElementById("no");
    const x = Math.random() * 250;
    const y = Math.random() * 100;
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
  }

  function yesClick() {
    document.getElementById("card").innerHTML = `
      <h1>I knew it 💘</h1>
      <p>
        Tulippp 🌷<br><br>
        Timilai pauda jindagi ajhai sundar lagcha.<br>
        I promise to respect you, care for you,<br>
        and make you smile every day 😊<br><br>
        ❤️❤️❤️
      </p>
    `;
    createHearts();
  }

  function createHearts() {
    setInterval(() => {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.innerHTML = "❤️";
      heart.style.left = Math.random() * 100 + "vw";
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 4000);
    }, 300);
  }
</script>

</body>
</html>
