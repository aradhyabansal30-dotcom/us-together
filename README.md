<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Anniversary Website</title>
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #fff0f5;
      margin: 0;
      padding: 0;
      text-align: center;
    }
    #lockscreen {
      padding-top: 100px;
    }
    #mainContent {
      display: none;
      padding: 30px;
    }
    input, button {
      padding: 10px;
      font-size: 16px;
      margin: 10px;
    }
    button {
      background-color: #ff4081;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    h2 {
      color: #d81b60;
    }
    .section {
      margin: 40px 0;
    }
    ol {
      text-align: left;
      max-width: 600px;
      margin: 0 auto;
    }
    p {
      max-width: 700px;
      margin: 0 auto;
      line-height: 1.6;
    }
    img {
      max-width: 80%;
      border-radius: 10px;
      margin-bottom: 20px;
    }
  </style>
</head>
<body>

<!-- Lock Screen -->
<div id="lockscreen">
  <h2>🔐 Enter the Magic Date</h2>
  <input type="text" id="password" placeholder="DD MMM YYYY">
  <br>
  <button onclick="checkPassword()">Unlock</button>
  <p><em>Wahi din jab hum ek hue the…</em></p>
</div>

<!-- Main Content -->
<div id="mainContent">
  <!-- Background Music -->
  <audio autoplay loop>
    <source src="https://www.dropbox.com/scl/fi/a99yuqcvszfqvghl13c3x/Dil-Diyan-Gallan-Song-_-Tiger-Zinda-Hai-_-Salman-Khan-Katrina-Kaif-_-Atif-Aslam-_-Vishal-Shekhar.mp3?rlkey=qrdyymie64e50u3bh4vixzime&st=mkscfvz7&dl=0" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

  <!-- Page 1 -->
  <div class="section" id="page1">
    <h2>🌸 Tu Krishna ke bansuri sa madhur priye…</h2>
    <img src="https://www.dropbox.com/scl/fi/xoedcld91pn207yhjkyir/566588892_1350779783405212_1066810312211966486_n.jpg?rlkey=zyk4jmarr7o1v1o238hmw0i4j&st=0yegurjh&dl=0" alt="Us together">
    <p>
      Mai Radha ke mann ki rooth-priye 💫<br>
      Tu Krishna ke muskaan sa shaitaan, priye…<br>
      Mai Radha ke abhimaan si shaan, priye…<br><br>

      Tu Vrindavan ke mor pankh jaisa pyara,<br>
      Mai Radha ke naino ki ishaare, priye…<br>
      Tum Krishna ke naino ka jaadu, priye…<br>
      Mai Radha, jo har pal ho jaati tum mai madhosh, priye…<br><br>

      Tu vrindavan ki lehrata dhun,<br>
      Mai wo Radha hoon, jise bas tumhara junoon sunai de chun-chun…<br><br>

      Tum bansuri bajao, mai dil haar jaun,<br>
      Tum muskaan dikhao, mai sans rok jaun…<br><br>

      Tum kanhaiya ke natkhat andaaz,<br>
      Mai Radha, jiska har gussa bhi tere liye khaas<br>
      Tum prem ho, mai bhakti hoon,<br>
      Tum bajate ho bansuri, mai har sur mein basti hoon..<br><br>

      Tum bansuri ka sur ho madhur,<br>
      Mai wo Radha hoon jo tumpe magan surur…<br>
      Tum makhan chor ke natkhat adaa,<br>
      Mai Radha, jiska chura liya dil tumne zara-zara…<br>
      Tum Krishna ke prem ka geet,<br>
      Mai Radha, jisme basa tumhara preet…<br><br>

      YHI thi mere dil ki baat priyee..<br>
      Ho gya hai ek saal saath priyee 🫠🫠
    </p>
    <button onclick="showPage('page2')">Next: 7 Waade</button>
  </div>

  <!-- Page 2 -->
  <div class="section" id="page2" style="display:none;">
    <h2>💍 7 Waade, Saath Nibhane</h2>
    <ol>
      <li>Khushi mein hoon ya na hoon, dukh mein hamesha rahungi 🤍</li>
      <li>Tere har sapne ko apna banaungi, chahe raaste mushkil hoon 🌠</li>
      <li>Tere har khamoshi ko samajhne ki koshish karungi, bina shabd ke 💫</li>
      <li>Jab tu thak jaaye, main teri himmat ban jaungi 💪</li>
      <li>Tere har gusse ko pyaar se gale lagaungi ❤️</li>
      <li>Har saal, har pal tujhe yaad dilaaungi ki tu mera hai, meri dua bhi 🙏</li>
      <li>Jab tak saansein chalti hain, main tujhmein basti rahungi 💞</li>
    </ol>
    <button onclick="showPage('page3')">Next: Final Message</button>
  </div>

  <!-- Page 3 -->
  <div class="section" id="page3" style="display:none;">
    <h2>🥹 Thank You Beta…</h2>
    <p>
      Bas ek hi dua hai… ki humara CS ho jaye 🫶🏻<br>
      Aur vo reel ek din sach ho jaye —<br>
      <em>“Ye naayi naayi suhagan, ho gayi hai teri jogan”</em> 🥹💋<br><br>

      Love you so much… itna zyada ki shabdon mein bayaan bhi nahi ho sakta 🫠<br>
      Pata hi nahi chala kab ek saal ho gaya…<br>
      Itne ups & downs… pata nahi kya kya jhela… par tu tha, main thi… aur hum the 🤌🏻<br><br>

      Tu mera sukoon hai, mera junoon bhi…<br>
      Tu mera har din hai, mera har kal bhi…<br>
      Thank you for being mine. 💖
    </p>
    <button onclick="showPage('page1')">Back to Start</button>
  </div>
</div>

<!-- JavaScript -->
<script>
  function checkPassword() {
    const password = document.getElementById("password").value;
    if (password === "18 oct 2024") {
      document.getElementById("lockscreen").style.display = "none";
      document.getElementById("mainContent").style.display = "block";
      confetti({
        particleCount: 150,
        spread: 70,
        origin: { y: 0.6 }
      });
    } else {
      alert("Galat password beta 😅");
    }
  }

  function showPage(pageId) {
    document.querySelectorAll('.section').forEach(sec => sec.style.display = 'none');
    document.getElementById(pageId).style.display = 'block';
  }
</script>

</body>
</html>
