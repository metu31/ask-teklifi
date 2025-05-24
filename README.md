<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Esma'ya Aşk Mektubu</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

    body {
      font-family: 'Montserrat', sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #f8c8dc, #f3e0e0);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      color: #333;
      position: relative;
    }

    .container {
      background: rgba(255, 255, 255, 0.92);
      border-radius: 20px;
      box-shadow: 0 8px 20px rgba(233, 30, 99, 0.3);
      max-width: 600px;
      width: 90%;
      padding: 30px 40px;
      text-align: center;
      opacity: 0;
      transform: translateY(30px);
      animation: fadeInUp 1s forwards;
    }

    h1 {
      color: #e91e63;
      font-size: 2.8rem;
      margin-bottom: 20px;
      animation: slideInLeft 1s forwards;
    }

    p {
      font-size: 1.2rem;
      line-height: 1.6;
      margin-bottom: 30px;
      color: #555;
      animation: slideInRight 1s forwards;
    }

    .button-group {
      display: flex;
      justify-content: center;
      gap: 20px;
      animation: fadeIn 1.5s forwards;
    }

    button {
      background-color: #e91e63;
      border: none;
      padding: 12px 30px;
      border-radius: 30px;
      color: white;
      font-weight: 700;
      font-size: 1.1rem;
      cursor: pointer;
      box-shadow: 0 4px 10px rgba(233, 30, 99, 0.4);
      transition: background-color 0.3s ease;
      user-select: none;
    }
    button:hover {
      background-color: #c2185b;
    }

    /* Heart floating animation */
    .heart {
      position: absolute;
      top: 20px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 3.5rem;
      color: #e91e63;
      animation: heartBeat 1.5s infinite;
      pointer-events: none;
      user-select: none;
      text-shadow: 0 0 10px #e91e63;
    }

    /* Fireworks */
    .firework {
      position: fixed;
      width: 10px;
      height: 10px;
      background: gold;
      border-radius: 50%;
      animation: explode 1s ease-out forwards;
      z-index: 9999;
      pointer-events: none;
    }

    /* Animations */
    @keyframes fadeInUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    @keyframes slideInLeft {
      from {
        opacity: 0;
        transform: translateX(-100%);
      }
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }
    @keyframes slideInRight {
      from {
        opacity: 0;
        transform: translateX(100%);
      }
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }
    @keyframes fadeIn {
      to {
        opacity: 1;
      }
    }
    @keyframes heartBeat {
      0%, 100% {
        transform: translateX(-50%) scale(1);
      }
      50% {
        transform: translateX(-50%) scale(1.2);
      }
    }
    @keyframes explode {
      0% { transform: scale(1); opacity: 1; }
      100% { transform: scale(5); opacity: 0; }
    }

    /* Hidden sections */
    #secondPage, #finalPage {
      display: none;
    }

    #finalText {
      font-size: 2.8rem;
      color: #e91e63;
      font-weight: 700;
      margin-top: 40px;
      text-shadow: 0 0 10px #e91e63;
    }

    /* Music toggle button */
    #musicToggle {
      position: fixed;
      top: 20px;
      right: 20px;
      background: #e91e63;
      border: none;
      color: white;
      padding: 10px 18px;
      border-radius: 30px;
      cursor: pointer;
      box-shadow: 0 4px 10px rgba(233, 30, 99, 0.5);
      z-index: 10000;
      user-select: none;
      font-weight: 700;
      font-size: 1rem;
      transition: background-color 0.3s ease;
    }
    #musicToggle:hover {
      background-color: #c2185b;
    }
  </style>
</head>
<body>
  <div class="heart">💖</div>

  <!-- Arka plan müziği -->
  <audio id="bgMusic" autoplay loop>
    <source src="https://www.bensound.com/bensound-music/bensound-romantic.mp3" type="audio/mpeg" />
    Tarayıcınız audio elementini desteklemiyor.
  </audio>
  <button id="musicToggle">Müziği Kapat</button>

  <!-- İlk Sayfa -->
  <div id="firstPage" class="container">
    <p><strong>Not:</strong><br>
      Bu mesaj baya denemeler üzerine, birkaç gün düşünülmüştür. Yazım yanlışlarım olabilir, noktalama işaretleri gibi. Piknik filan yalandır, sadece işe heyecan katmak için düzenlenmiştir.<br><br>
      Mehmet Turgut Emir bir söz verdiyse ve bir plana “evet” dediyse, o işi yapar.<br><br>
      Ve sadece <strong>seni mutlu etmek istiyorum Esma’m</strong>. :)</p>

    <p id="continueText" style="font-size: 1.2rem; margin-top: 25px; color: #666;">
      <strong>Devam etmek istiyor musun?</strong>
    </p>

    <div class="button-group" id="continueButtons">
      <button id="yes1">Evet</button>
      <button id="no1">Hayır</button>
    </div>
  </div>

  <!-- İkinci Sayfa -->
  <div id="secondPage" class="container">
    <h1>Esmamm, HÜRREMİM, gönlümün sultanııı,</h1>
    <p>
      Hanım efendi...<br>
      Tarihler bile senin gibi güzel, ben de senin gibi özel olmak istiyorum.<br>
      Takvim bile bizi çift yazdı: <strong>25.5.2025</strong><br><br>
      Eksik olan bir "Evet".<br>
      Aşkımızın tarihi <strong>25.5.2025</strong>'te başlasın mı?<br><br>
      Sıcak kalpli biriyle tatlı bir başlangıç istermisin?<br>
      <strong>Benimle sevgili olur musun?</strong> 💖
    </p>

    <div class="button-group">
      <button id="yes2">Evet</button>
      <button id="no2">Hayır</button>
    </div>
  </div>

  <!-- Final Sayfası -->
  <div id="finalPage" class="container" style="flex-direction: column;">
    <h1 id="finalText">Kek bahane bu AŞK şahane olacak! 🎉</h1>
  </div>

  <script>
    // Buton referansları
    const yes1 = document.getElementById('yes1');
    const no1 = document.getElementById('no1');
    const yes2 = document.getElementById('yes2');
    const no2 = document.getElementById('no2');

    const firstPage = document.getElementById('firstPage');
    const secondPage = document.getElementById('secondPage');
    const finalPage = document.getElementById('finalPage');

    const continueText = document.getElementById('continueText');
    const continueButtons = document.getElementById('continueButtons');

    // Müzik kontrolleri
    const bgMusic = document.getElementById('bgMusic');
    const musicToggle = document.getElementById('musicToggle');

    musicToggle.onclick = () => {
      if (bgMusic.paused) {
        bgMusic.play();
        musicToggle.textContent = "Müziği Kapat";
      } else {
        bgMusic.pause();
        musicToggle.textContent = "Müziği Aç";
      }
    };

    // İlk sayfa butonları
    yes1.onclick = () => {
      firstPage.style.display = 'none';
      secondPage.style.display = 'block';
    };

    no1.onclick = () => {
      // Hayır butonlarını gizle, mesajı değiştir ve evet butonunu göster
      continueButtons.style.display = 'none';
      continueText.innerHTML = 'Naz yapmaaaa hadiii evet tuşuna bas! <br><button id="noYesBtn" style="margin-top:20px; background:#e91e63; color:#fff; border:none; border-radius:30px; padding:12px 30px; font-weight:700; cursor:pointer; box-shadow: 0 4px 10px rgba(233, 30, 99, 0.4);">Evet</button>';
      
      // Yeni evet butonu referansı
      const noYesBtn = document.getElementById('noYesBtn');
      noYesBtn.onclick = () => {
        firstPage.style.display = 'none';
        secondPage.style.display = 'block';
      };
    };

    // İkinci sayfa butonları
    yes2.onclick = () => {
      secondPage.style.display = 'none';
      finalPage.style.display = 'flex';
      launchFireworks();
    };

    no2.onclick = () => {
      no2.style.display = 'none';
    };

    // Havai fişek animasyonu
    function launchFireworks() {
      for (let i = 0; i < 50; i++) {
        const fw = document.createElement('div');
        fw.classList.add('firework');
        fw.style.left = Math.random() * window.innerWidth + 'px';
        fw.style.top = Math.random() * window.innerHeight + 'px';
        fw.style.background = `hsl(${Math.random() * 360}, 100%, 70%)`;
        document.body.appendChild(fw);
        setTimeout(() => fw.remove(), 1000);
      }
    }
  </script>
</body>
</html>
