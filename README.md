<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Partecipa al Concorso</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 30px;
      background: #f9f9f9;
    }
    #countdown {
      font-size: 28px;
      font-weight: bold;
      color: #d9534f;
      margin-bottom: 20px;
    }
    iframe {
      width: 100%;
      max-width: 700px;
      height: 900px;
      border: none;
    }
  </style>
</head>
<body>

  <h1>Partecipa al Concorso ElettroNando!</h1>
  <p>Compila il modulo qui sotto. Il concorso chiude tra:</p>
  <div id="countdown">Caricamento timer…</div>

  <!-- INCORPORA IL TUO MODULO QUI -->
  <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfIF4sIcWhsPk-fs3eCKFKfuVEsVksI1ekHbOMwrktKVEhKiw/viewform?usp=preview" allowfullscreen>Caricamento…</iframe>

  <script>
    const endTime = new Date("May 9, 2025 21:00:00").getTime();

    const countdown = setInterval(() => {
      const now = new Date().getTime();
      const distance = endTime - now;

      if (distance < 0) {
        clearInterval(countdown);
        document.getElementById("countdown").innerHTML = "⛔ Il modulo è stato chiuso.";
        return;
      }

      const days = Math.floor(distance / (1000 * 60 * 60 * 24));
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((distance % (1000 * 60)) / 1000);

      document.getElementById("countdown").innerHTML = 
        `⏳ ${days}g ${hours}h ${minutes}m ${seconds}s`;
    }, 1000);
  </script>

</body>
</html>

