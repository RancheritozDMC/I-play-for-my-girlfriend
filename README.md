<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>I play for my girlfriend 💖</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background: #ffe6f0;
      text-align: center;
      padding: 30px;
    }
    h1 {
      color: #d63384;
    }
    .heart {
      font-size: 50px;
      cursor: pointer;
      transition: transform 0.2s ease;
    }
    .heart:hover {
      transform: scale(1.2);
    }
    .message {
      margin-top: 20px;
      font-size: 20px;
      color: #555;
      background: #fff;
      padding: 15px;
      border-radius: 10px;
      max-width: 400px;
      margin-left: auto;
      margin-right: auto;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    .btn-reset {
      margin-top: 20px;
      background: #ff4d6d;
      border: none;
      color: white;
      padding: 10px 20px;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
    }
    .btn-reset:hover {
      background: #c9184a;
    }
  </style>
</head>
<body>
  <h1>Click on the Heart to see how much I love you 💘</h1>
  <div class="heart" onclick="mostrarMensaje()">❤️</div>
  <div class="message" id="mensaje">Click the heart to start ✨</div>
  <button class="btn-reset" onclick="reiniciarJuego()">Reboot</button>

  <script>
    const mensajes = [
      "You are my favorite person in the world 💖",
      "With you everything is better 🌟",
      "Thank you for existing 💫",
      "Your smile is my happy place 😊",
      "I love you more than desserts 🍰",
      "You are my reason to smile every day 😘",
      "If I could give you a star for every time I think of you, the sky would be empty ✨",
      "Playing with you is the best thing that has ever happened to me 💕"
    ];

    let usado = [];

    function mostrarMensaje() {
      if (usado.length === mensajes.length) {
        document.getElementById("mensaje").textContent = "!You've already seen all my message! 💌";
        return;
      }

      let index;
      do {
        index = Math.floor(Math.random() * mensajes.length);
      } while (usado.includes(index));

      usado.push(index);
      document.getElementById("mensaje").textContent = mensajes[index];
    }

    function reiniciarJuego() {
      usado = [];
      document.getElementById("mensaje").textContent = "Click on the heart to start ✨";
    }
  </script>
</body>
</html>
