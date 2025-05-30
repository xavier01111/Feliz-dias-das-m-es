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
      width: 350px; /* Tamanho ajustado */
      height: 200px;
      background: #fff8e1; /* Cor mais suave que lembra um envelope */
      position: relative;
      cursor: pointer;
      border-radius: 15px; /* Bordas arredondadas */
      border: 5px solid #e91e63; /* Borda espessa e colorida */
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2); /* Sombra para profundidade */
      display: flex;
      align-items: center;
      justify-content: center;
      color: #e91e63; /* Cor do texto */
      font-size: 22px;
      text-align: center;
      transition: transform 0.6s ease;
      position: relative;
    }

    /* Triângulo que simula a aba do envelope */
    .envelope:before {
      content: '';
      position: absolute;
      top: -20px;
      left: 50%;
      transform: translateX(-50%);
      border-left: 25px solid transparent;
      border-right: 25px solid transparent;
      border-bottom: 20px solid #e91e63; /* Cor da aba */
    }

    .card {
      background: white;
      border-radius: 20px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
      padding: 20px;
      text-align: center;
      max-width: 90%;
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

    .carousel-container {
      overflow-x: auto;
      scroll-snap-type: x mandatory;
      -webkit-overflow-scrolling: touch;
      display: flex;
      gap: 10px;
      margin-top: 20px;
      padding-bottom: 10px;
    }

    .carousel-container img {
      height: 200px;
      border-radius: 10px;
      scroll-snap-align: center;
      flex-shrink: 0;
    }
  </style>
</head>
<body>
  <div class="envelope" onclick="openCard()">
    💌 Clique na carta para abrir 💌
  </div>

  <div class="card" id="messageCard">
    <h1>Feliz Dia das Mães! ❤️</h1>
    <div class="heart">&#10084;</div>
    <p>Mãe, hoje estou te desejando feliz Dia das Mães, mas todo mundo sabe que esse dia é todos os dias.<br>
    Sei que isso não vai retribuir tudo o que você já me fez, mas espero que goste.<br>
    Te amo muito, mãe.</p>
    <div class="carousel-container">
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
