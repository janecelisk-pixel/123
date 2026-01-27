<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>Para ti 🤍</title>

  <!-- Fuente -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #f0f0f0, #dcdcdc);
      font-family: 'Playfair Display', serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }

    .card {
      background: white;
      max-width: 500px;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 15px 30px rgba(0,0,0,0.2);
      text-align: center;
      animation: aparecer 1.5s ease;
    }

    h1 {
      color: #333;
      margin-bottom: 15px;
    }

    p {
      color: #555;
      line-height: 1.7;
      font-size: 17px;
    }

    input {
      padding: 10px;
      border-radius: 15px;
      border: 1px solid #ccc;
      margin-top: 15px;
      width: 70%;
      font-size: 14px;
      text-align: center;
    }

    button {
      margin-top: 15px;
      padding: 10px 25px;
      border: none;
      border-radius: 20px;
      background: #000;
      color: white;
      cursor: pointer;
      font-size: 15px;
      transition: transform 0.2s ease;
    }

    button:hover {
      transform: scale(1.05);
    }

    .hidden {
      display: none;
    }

    .mensaje {
      margin-top: 20px;
      font-weight: 600;
      animation: latido 1.5s infinite;
    }

    /* Animaciones */
    @keyframes aparecer {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes latido {
      0% { transform: scale(1); }
      50% { transform: scale(1.05); }
      100% { transform: scale(1); }
    }

    /* Corazones flotando */
    .heart {
      position: absolute;
      bottom: -20px;
      font-size: 20px;
      animation: flotar 6s linear infinite;
      opacity: 0.7;
    }

    @keyframes flotar {
      from {
        transform: translateY(0);
        opacity: 1;
      }
      to {
        transform: translateY(-110vh);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <div class="card" id="login">
    <h1>💌 Carta privada</h1>
    <p>Ingresa la contraseña para leer esto 🤍</p>
    <input type="password" id="password" placeholder="Contraseña">
    <br>
    <button onclick="verificar()">Entrar</button>
  </div>

  <div class="card hidden" id="carta">
    <h1>Para ti 🤍</h1>

    <p>
      HOLIIIS
    </p>

    <p>
      3 MESES DE NOVIOS JSJSJSJ YA ES BASTANTE TIEMPO LA VERDAD UWU PERO QUE BUENO
    </p>

    <p>
      Mi niño perdoname si estas ulItmas dos veces no puede contestarte no tengo celular y esoy usando mi lap pero.. Te amo mucho esta es mi forma de expresarte lo que siento por ti te adoro mucho me haces falta necesito verte reirme contigo y si hay veces que enojarse es necesario estar lejos de ti me enseño a valorar tu presencia siempre te voy a amar mucho mi niño nunca lo dudes y pase lo q pase siempre te voy a buscar nos vemos el martes 3 CON AMOR PENEBOLITAS  
    </p>

    <div class="mensaje">
      🤍WASAAAA BAY TE AMO 🤍
    </div>
  </div>

  <script>
    function verificar() {
      const pass = document.getElementById("password").value;
      if (pass === "PENIBOLAS") {
        document.getElementById("login").classList.add("hidden");
        document.getElementById("carta").classList.remove("hidden");
      } else {
        alert("Contraseña incorrecta 💔");
      }
    }

    // Crear corazones animados
    setInterval(() => {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.innerText = "🤍";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (4 + Math.random() * 3) + "s";
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 7000);
    }, 500);
  </script>

</body>
</html>
