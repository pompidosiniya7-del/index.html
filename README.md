# index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Muliisa Francis | Music & Production</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, sans-serif;
      background: #090914;
      color: white;
      line-height: 1.6;
    }

    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 7%;
      background: #11111f;
      border-bottom: 1px solid #292943;
      position: sticky;
      top: 0;
      z-index: 10;
    }

    .logo {
      font-size: 23px;
      font-weight: bold;
      color: #c084fc;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 20px;
      font-size: 14px;
    }

    nav a:hover {
      color: #c084fc;
    }

    .hero {
      min-height: 85vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 30px 20px;
      background:
        radial-gradient(circle at top, #39205d, transparent 55%),
        #090914;
    }

    .hero .tag {
      color: #c084fc;
      letter-spacing: 4px;
      font-size: 13px;
      margin-bottom: 15px;
    }

    .hero h1 {
      font-size: clamp(38px, 8vw, 75px);
      line-height: 1.1;
      margin-bottom: 20px;
    }

    .hero h1 span {
      color: #c084fc;
    }

    .hero p {
      color: #c7c7d9;
      max-width: 550px;
      margin-bottom: 30px;
    }

    .btn {
      display: inline-block;
      padding: 13px 27px;
      background: #9333ea;
      color: white;
      text-decoration: none;
      border-radius: 30px;
      font-weight: bold;
      transition: 0.3s;
      border: none;
      cursor: pointer;
    }

    .btn:hover {
      background: #a855f7;
      transform: translateY(-3px);
    }

    section {
      padding: 75px 7%;
    }

    .section-title {
      text-align: center;
      font-size: 32px;
      margin-bottom: 15px;
    }

    .section-subtitle {
      text-align: center;
      color: #aaaac0;
      margin-bottom: 40px;
    }

    .music-box {
      max-width: 650px;
      margin: auto;
      background: #151526;
      padding: 30px;
      border-radius: 20px;
      border: 1px solid #30304b;
      text-align: center;
    }

    .music-icon {
      font-size: 60px;
      margin-bottom: 15px;
    }

    .music-box h3 {
      margin-bottom: 10px;
    }

    .music-box p {
      color: #aaaac0;
      margin-bottom: 20px;
    }

    input[type="file"] {
      display: block;
      width: 100%;
      margin: 20px 0;
      color: #ddd;
    }

    audio {
      width: 100%;
      margin-top: 15px;
    }

    .services {
      background: #10101d;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 25px;
    }

    .card {
      background: #19192b;
      padding: 30px;
      border-radius: 18px;
      border: 1px solid #30304b;
      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-7px);
      border-color: #a855f7;
    }

    .card .icon {
      font-size: 40px;
      margin-bottom: 15px;
    }

    .card h3 {
      color: #c084fc;
      margin-bottom: 12px;
    }

    .card p {
      color: #b7b7ca;
      font-size: 15px;
    }

    .about {
      text-align: center;
    }

    .about p {
      max-width: 700px;
      margin: auto;
      color: #b7b7ca;
    }

    .contact {
      background:
        radial-gradient(circle at center, #32194d, transparent 70%),
        #10101d;
      text-align: center;
    }

    .contact p {
      color: #c7c7d9;
      margin-bottom: 25px;
    }

    footer {
      text-align: center;
      padding: 25px 15px;
      background: #07070e;
      border-top: 1px solid #292943;
      color: #aaaac0;
      font-size: 14px;
    }

    footer strong {
      color: #c084fc;
      display: block;
      margin-top: 5px;
    }

    @media (max-width: 600px) {
      header {
        flex-direction: column;
        gap: 12px;
      }

      nav a {
        margin: 0 8px;
        font-size: 13px;
      }

      section {
        padding: 55px 6%;
      }

      .music-box {
        padding: 20px;
      }
    }
  </style>
</head>

<body>

  <!-- HEADER -->
  <header>
    <div class="logo">Muliisa Francis 🎶</div>

    <nav>
      <a href="#home">Home</a>
      <a href="#music">Music</a>
      <a href="#services">Services</a>
      <a href="#about">About</a>
    </nav>
  </header>

  <!-- HOME -->
  <section class="hero" id="home">
    <div class="tag">WELCOME TO MY WORLD</div>

    <h1>
      MUSIC 🎶 AND<br>
      <span>PRODUCTION</span>
    </h1>

    <p>
      Feel the rhythm. Create the sound.
      Discover music, creativity and production
      with Muliisa Francis.
    </p>

    <a href="#music" class="btn">Explore My Music</a>
  </section>

  <!-- MUSIC -->
  <section id="music">
    <h2 class="section-title">My Music 🎧</h2>

    <p class="section-subtitle">
      Listen to my sounds and musical creations.
    </p>

    <div class="music-box">
      <div class="music-icon">🎵</div>

      <h3>Music Player</h3>

      <p>
        Choose an audio file from your phone
        to play your music here.
      </p>

      <input
        type="file"
        id="audioFile"
        accept="audio/*"
      >

      <audio id="player" controls>
        Your browser does not support audio.
      </audio>
    </div>
  </section>

  <!-- SERVICES -->
  <section class="services" id="services">
    <h2 class="section-title">Production Services</h2>

    <p class="section-subtitle">
      Creativity meets sound.
    </p>

    <div class="cards">

      <div class="card">
        <div class="icon">🎙️</div>
        <h3>Music Recording</h3>
        <p>
          Recording vocals and musical ideas
          for original songs.
        </p>
      </div>

      <div class="card">
        <div class="icon">🎚️</div>
        <h3>Music Production</h3>
        <p>
          Creating beats, rhythms and
          exciting musical arrangements.
        </p>
      </div>

      <div class="card">
        <div class="icon">🎧</div>
        <h3>Mixing & Sound</h3>
        <p>
          Improving sound balance and
          creating a better listening experience.
        </p>
      </div>

    </div>
  </section>

  <!-- ABOUT -->
  <section class="about" id="about">
    <h2 class="section-title">About Me</h2>

    <p>
      I am Muliisa Francis, passionate about
      music, creativity and sound production.
      This website is my personal music space
      where I share my musical journey and
      creative ideas.
    </p>
  </section>

  <!-- CONTACT -->
  <section class="contact" id="contact">
    <h2 class="section-title">Let's Make Music 🎶</h2>

    <p>
      Music brings people together.
      Let's create something amazing.
    </p>

    <a href="#home" class="btn">Back to Top</a>
  </section>

  <!-- FOOTER -->
  <footer>
    <p>© 2026 Muliisa Francis</p>

    <strong>BAIT/26D/U/A1554</strong>

    <p>Music 🎶 And Production</p>
  </footer>

  <!-- AUDIO PLAYER FUNCTION -->
  <script>
    const audioFile = document.getElementById("audioFile");
    const player = document.getElementById("player");

    audioFile.addEventListener("change", function () {
      const file = this.files[0];

      if (file) {
        player.src = URL.createObjectURL(file);
        player.play();
      }
    });
  </script>

</body>
</html>

index.html
