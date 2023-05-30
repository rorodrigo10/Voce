html>
<head>
  <title>Pedido de Namoro</title>
  <style>
    body {
      text-align: center;
      background-color: #f2f2f2;
      font-family: Arial, sans-serif;
    }
    
    h1 {
      margin-top: 50px;
    }

    .option-container {
      display: inline-block;
      margin-top: 30px;
    }

    .option-container button {
      font-size: 24px;
      padding: 10px 20px;
      margin: 0 10px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Me da o cuzinho?</h1>

  <div class="option-container">
    <button id="sim-button" onclick="simClicked()">Sim</button>
    <button id="nao-button" onclick="naoClicked()">Não</button>
  </div>

  <script>
    function getRandomPosition() {
      var windowHeight = window.innerHeight;
      var windowWidth = window.innerWidth;

      var buttonWidth = 100; // Largura do botão "Não"
      var buttonHeight = 40; // Altura do botão "Não"

      var maxTop = windowHeight - buttonHeight;
      var maxLeft = windowWidth - buttonWidth;

      var randomTop = Math.floor(Math.random() * maxTop);
      var randomLeft = Math.floor(Math.random() * maxLeft);

      return { top: randomTop, left: randomLeft };
    }

    function naoClicked() {
      var naoButton = document.getElementById("nao-button");
      var position = getRandomPosition();

      naoButton.style.position = "absolute";
      naoButton.style.top = position.top + "px";
      naoButton.style.left = position.left + "px";
    }

    function simClicked() {
      window.location.href = "https://www.youtube.com/shorts/sGAM8w6_zoc";
    }
  </script>
</body>
</html>

