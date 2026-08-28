
<!DOCTYPE html>
<html lang="ro">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DJ Arabul MC45</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
      background: #08000f;
      color: white;
      min-height: 100vh;
    }

    header {
      text-align: center;
      padding: 70px 20px 40px;
      background: radial-gradient(circle at center, #5d00a8, #08000f 65%);
    }

    header h1 {
      font-size: clamp(42px, 9vw, 85px);
      color: #fff;
      text-shadow:
        0 0 10px #a000ff,
        0 0 30px #a000ff,
        0 0 60px #6f00ff;
    }

    header p {
      margin-top: 15px;
      color: #d9a8ff;
      font-size: 20px;
    }

    .live {
      display: inline-block;
      margin-top: 25px;
      padding: 12px 28px;
      border-radius: 30px;
      background: #9d00ff;
      color: white;
      font-weight: bold;
      box-shadow: 0 0 25px #9d00ff;
    }

    main {
      max-width: 900px;
      margin: auto;
      padding: 30px 20px 70px;
    }

    .card {
      background: rgba(255,255,255,0.06);
      border: 1px solid rgba(180,0,255,0.35);
      border-radius: 20px;
      padding: 30px;
      margin-top: 25px;
      box-shadow: 0 0 30px rgba(140,0,255,0.15);
    }

    h2 {
      color: #d36aff;
      margin-bottom: 15px;
    }

    .player {
      text-align: center;
    }

    .play {
      border: none;
      border-radius: 50%;
      width: 80px;
      height: 80px;
      background: #a000ff;
      color: white;
      font-size: 30px;
      cursor: pointer;
      box-shadow: 0 0 30px #a000ff;
    }

    .play:hover {
      background: #c13cff;
    }

    .status {
      margin-top: 18px;
      color: #cfa1ff;
    }

    footer {
      text-align: center;
      padding: 25px;
      color: #9575a8;
      border-top: 1px solid #24102f;
    }
  </style>
</head>

<body>

  <header>
    <h1>DJ ARABUL MC45</h1>
    <p>DJ • MC • MUSIC • LIVE</p>
    <div class="live">🔴 LIVE SOON</div>
  </header>

  <main>

    <section class="card player">
      <h2>🎧 Player</h2>

      <button class="play" onclick="playMusic()">▶</button>

      <p class="status" id="status">
        Apasă Play pentru muzică
      </p>

      <audio id="music">
        <!-- Vom adăuga aici muzica ta mai târziu -->
      </audio>
    </section>

    <section class="card">
      <h2>🎤 Despre mine</h2>
      <p>
        Bine ai venit pe site-ul oficial DJ Arabul MC45!
        DJ, MC și iubitor de muzică. Aici vei găsi muzică,
        live-uri, evenimente și noutăți.
      </p>
    </section>

    <section class="card">
      <h2>📅 Evenimente</h2>
      <p>
        În curând vom adăuga aici evenimentele și petrecerile
        la care participă DJ Arabul MC45.
      </p>
    </section>

    <section class="card">
      <h2>📞 Contact</h2>
      <p>
        Pentru rezervări și colaborări, revino aici.
        Vom adăuga ulterior numărul de telefon și rețelele sociale.
      </p>
    </section>

  </main>

  <footer>
    © 2026 DJ Arabul MC45 — Toate drepturile rezervate.
  </footer>

  <script>
    function playMusic() {
      const music = document.getElementById("music");
      const status = document.getElementById("status");

      if (!music.src) {
        status.textContent = "🎵 Vom adăuga muzica aici în pasul următor.";
        return;
      }

      if (music.paused) {
        music.play();
        status.textContent = "🔊 Redare...";
      } else {
        music.pause();
        status.textContent = "⏸ Pauză";
      }
    }
  </script>

</body>
</html>
