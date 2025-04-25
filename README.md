# invitacion
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>XV Años de Alexa</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Open+Sans&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Open Sans', sans-serif;
      background: linear-gradient(to bottom, #e0f7fa, #fff);
      margin: 0;
      color: #333;
    }
    header {
      text-align: center;
      background: #b3e5fc;
      padding: 40px 20px;
      color: #004d61;
    }
    header h1 {
      font-family: 'Great Vibes', cursive;
      font-size: 3rem;
      margin: 0;
    }
    section {
      padding: 30px;
      text-align: center;
    }
    .countdown {
      font-size: 2rem;
      font-weight: bold;
      color: #01579b;
    }
    .gallery img {
      width: 150px;
      height: 150px;
      margin: 10px;
      object-fit: cover;
      border-radius: 10px;
      box-shadow: 0 0 10px #ccc;
    }
    iframe {
      border: 0;
      border-radius: 10px;
      margin-top: 20px;
    }
    form {
      margin-top: 20px;
    }
    input, textarea, button {
      display: block;
      margin: 10px auto;
      padding: 10px;
      width: 80%;
      max-width: 400px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    footer {
      background: #b3e5fc;
      text-align: center;
      padding: 20px;
      font-size: 0.9rem;
    }
  </style>
</head>
<body>

  <!-- 🎶 Música de fondo -->
  <audio autoplay loop>
    <source src="https://dl.sndup.net/3gns/Jennie%20-%20FTS.mp3" type="audio/mp3">
  </audio>

  <header>
    <h1>XV Años de Alexa</h1>
    <p>¡Estás cordialmente invitado a celebrar este día mágico!</p>
  </header>

  <section>
    <h2>✨ Fecha y lugar ✨</h2>
    <p><strong>7 de septiembre de 2025</strong></p>
    <p>Monterrey, Nuevo León</p>
    <iframe src="https://www.google.com/maps?q=Monterrey,+NL,+Mexico&output=embed" width="90%" height="300"></iframe>
  </section>

  <section>
    <h2>⏳ Falta para el gran día:</h2>
    <div class="countdown" id="countdown"></div>
  </section>

  <section class="gallery">
    <h2>📸 Recuerdos</h2>
    <img src="https://via.placeholder.com/150?text=Foto+1" alt="Foto 1">
    <img src="https://via.placeholder.com/150?text=Foto+2" alt="Foto 2">
    <img src="https://via.placeholder.com/150?text=Foto+3" alt="Foto 3">
  </section>

  <section>
    <h2>✅ Confirma tu asistencia</h2>
    <form action="https://formsubmit.co/tu_correo@gmail.com" method="POST">
      <input type="text" name="nombre" placeholder="Tu nombre" required />
      <input type="number" name="acompañantes" placeholder="Número de acompañantes" required />
      <textarea name="mensaje" placeholder="Mensaje o duda (opcional)"></textarea>
      <input type="hidden" name="_captcha" value="false">
      <button type="submit">Enviar confirmación</button>
    </form>
  </section>

  <footer>
    Gracias por acompañarnos en este día tan especial 💙
  </footer>

  <!-- 🕒 Cuenta regresiva -->
  <script>
    const countdown = document.getElementById("countdown");
    const targetDate = new Date("2025-09-07T00:00:00").getTime();

    setInterval(() => {
      const now = new Date().getTime();
      const distance = targetDate - now;

      const days = Math.floor(distance / (1000 * 60 * 60 * 24));
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((distance % (1000 * 60)) / 1000);

      countdown.innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s`;
    }, 1000);
  </script>
</body>
</html>
