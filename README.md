
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>❤️ Mein Herz</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      height: 100vh;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      background: radial-gradient(circle at center, #35104d, #09000f 70%);
      font-family: Arial, sans-serif;
    }

    .container {
      text-align: center;
      position: relative;
      z-index: 2;
    }

    .heart {
      font-size: 150px;
      animation: heartbeat 1.2s infinite;
      filter: drop-shadow(0 0 25px #ff1744);
      cursor: pointer;
    }

    .text {
      margin-top: 20px;
      color: white;
      font-size: 28px;
      font-weight: bold;
      text-shadow: 0 0 15px #ff1744;
    }

    @keyframes heartbeat {
      0% {
        transform: scale(1);
      }

      15% {
        transform: scale(1.2);
      }

      30% {
        transform: scale(1);
      }

      45% {
        transform: scale(1.15);
      }

      60% {
        transform: scale(1);
      }

      100% {
        transform: scale(1);
      }
    }

    .floating-heart {
      position: absolute;
      bottom: -50px;
      color: #ff1744;
      font-size: 25px;
      animation: floatUp linear infinite;
      opacity: 0.8;
    }

    @keyframes floatUp {
      0% {
        transform: translateY(0) rotate(0deg);
        opacity: 0;
      }

      20% {
        opacity: 1;
      }

      100% {
        transform: translateY(-110vh) rotate(360deg);
        opacity: 0;
      }
    }
  </style>
</head>

<body>

  <div class="container">
    <div class="heart">❤️</div>
    <div class="text">Mein Herz ❤️</div>
  </div>

  <script>
    function createHeart() {
      const heart = document.createElement("div");

      heart.className = "floating-heart";
      heart.innerHTML = "❤️";

      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = (15 + Math.random() * 35) + "px";
      heart.style.animationDuration = (4 + Math.random() * 5) + "s";

      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 9000);
    }

    setInterval(createHeart, 350);
  </script>

</body>
</html>
