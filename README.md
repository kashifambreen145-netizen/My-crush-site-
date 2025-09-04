# My-crush-site-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Special for You ❤️</title>
  <style>
    body {
      margin: 0;
      font-family: "Comic Sans MS", cursive, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #ffeef8;
      text-align: center;
      padding: 20px;
    }
    .page {
      display: none;
      font-size: 28px;
      color: #d63384;
      line-height: 1.6;
      max-width: 90%;
    }
    .active {
      display: block;
    }
    button {
      margin-top: 30px;
      padding: 12px 24px;
      font-size: 20px;
      background: #d63384;
      color: white;
      border: none;
      border-radius: 12px;
      cursor: pointer;
    }
    video, img {
      width: 80%;
      max-width: 400px;
      border-radius: 15px;
      margin-top: 20px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.3);
    }
  </style>
</head>
<body>

  <!-- Page 1 -->
  <div class="page active" id="page1">
    <h1>Hey Kaisi Ho 😊</h1>
    <button onclick="nextPage(2)">Next ➡️</button>
  </div>

  <!-- Page 2 -->
  <div class="page" id="page2">
    <h1>Dekho mujhe tumse ek important baat karni hai…</h1>
    <button onclick="nextPage(3)">Next ➡️</button>
  </div>

  <!-- Page 3 -->
  <div class="page" id="page3">
    <p>
      Kabhi kabhi sochta hoon ki tumhari muskaan kaisi itni powerful ho sakti hai…<br><br>
      Shayad tumhe andaza bhi nahi hoga ki tum kitni special ho mere liye.<br><br>
      Tumhari baaton me ek ajeeb si magic hai… jo mujhe baar baar tumse baat karne par majboor kar deti hai.<br><br>
      Waise ek secret bataun? Jab bhi tum online hoti ho na,<br>
      mera dil thoda fast beat karne lagta hai 😅❤️
    </p>
    <button onclick="nextPage(4)">Next ➡️</button>
  </div>

  <!-- Page 4 -->
<div class="page" id="page4">
  <h1>Ab tumhare liye ek chhoti si surprise 💖</h1>
  <video controls autoplay loop>
    <source src="lv_7528487066779405621_20250904134329.mp4" type="video/mp4">
  </video>
</div>

  <!-- Background Music -->
  <audio id="bgmusic" loop>
    <source src="if the World was Ending.mp3"type="audio/mpeg">
    Your browser does not support audio.
  </audio>

  <script>
    function nextPage(pageNumber) {
      document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
      document.getElementById('page' + pageNumber).classList.add('active');
    }

    // Autoplay music after first click
    document.addEventListener('click', function startMusic() {
      const audio = document.getElementById('bgmusic');
      audio.play().catch(() => {});
      document.removeEventListener('click', startMusic);
    });
  </script>

</body>
</html>
