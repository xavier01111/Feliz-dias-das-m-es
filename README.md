<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Feliz Dia das Mães</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom, #ffe6f0, #ffffff);
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      flex-direction: column;
    }
    .envelope {
      width: 200px;
      height: 150px;
      background: #e91e63;
      position: relative;
      cursor: pointer;
      border-radius: 10px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 18px;
      text-align: center;
    }
    .card {
      background: white;
      border-radius: 20px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
      padding: 20px;
      text-align: center;
      max-width: 400px;
      display: none;
      animation: fadeIn 1s ease forwards;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    h1 {
      color: #e91e63;
    }
    p {
      font-size: 18px;
      color: #444;
    }
    .heart {
      font-size: 40px;
      color: #e91e63;
      margin: 20px 0;
    }
    .carousel {
      display: flex;
      overflow-x: auto;
      scroll-snap-type: x mandatory;
      gap: 10px;
      margin-top: 20px;
    }
    .carousel img {
      height: 200px;
      border-radius: 10px;
      scroll-snap-align: center;
      flex-shrink: 0;
    }
  </style>
</head>
<body>
  <div class="envelope" onclick="openCard()">
    Clique aqui para abrir sua carta 💌
  </div>

  <div class="card" id="messageCard">
    <h1>Feliz Dia das Mães! ❤️</h1>
    <div class="heart">&#10084;</div>
    <p>Mãe, hoje estou te desejando feliz Dia das Mães, mas todo mundo sabe que esse dia é todos os dias.<br>
    Sei que isso não vai retribuir tudo o que você já me fez, mas espero que goste.<br>
    Te amo muito, mãe.</p>
    <div class="carousel">
      <img src="IMG-20250510-WA0017.jpg" alt="Foto 1">
      <img src="IMG-20250510-WA0018.jpg" alt="Foto 2">
      <img src="IMG-20250510-WA0019.jpg" alt="Foto 3">
      <img src="IMG-20250510-WA0020.jpg" alt="Foto 4">
    </div>
  </div>

  <script>
    function openCard() {
      document.querySelector('.envelope').style.display = 'none';
      document.getElementById('messageCard').style.display = 'block';
    }
  </script>
</body>
</html>
