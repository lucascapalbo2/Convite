<html>
<head>
  <title>Convite</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: Arial, sans-serif;
    }

    #container {
      text-align: center;
    }

    #nao-button {
      display: inline-block;
      padding: 10px 20px;
      background-color: red;
      color: white;
      border: none;
      outline: none;
      cursor: pointer;
      position: absolute;
      top: 50%;
      left: 58%;
      transform: translate(-50%, -50%);
    }

    #sim-button {
      display: inline-block;
      padding: 10px 20px;
      background-color: green;
      color: white;
      border: none;
      top: 55%;
      outline: none;
      cursor: pointer;
    }

    #heart {
      font-size: 60px;
      color: red;
      display: none;
    }

    #message {
      margin-top: 20px;
      font-size: 20px;
    }
  </style>
</head>
<body>
  <div id="container">
    <button id="nao-button">Não</button>
    <button id="sim-button">Sim</button>
    <p id="message">Posso ir para sua casa?</p>
    <span id="heart">&hearts;</span>
  </div>

  <script>
    var naoButton = document.getElementById("nao-button");
    var simButton = document.getElementById("sim-button");
    var heart = document.getElementById("heart");

    naoButton.addEventListener("mouseover", function() {
      var rect = this.getBoundingClientRect();
      var maxX = window.innerWidth - rect.width;
      var maxY = window.innerHeight - rect.height;
      var newX = Math.floor(Math.random() * maxX);
      var newY = Math.floor(Math.random() * maxY);
      this.style.left = newX + "px";
      this.style.top = newY + "px";
    });

    simButton.addEventListener("click", function() {
      heart.style.display = "inline";
    });
  </script>
</body>
</html>
