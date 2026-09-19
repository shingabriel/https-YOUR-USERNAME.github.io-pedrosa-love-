<!DOCTYPE html>

<html lang="en"> <head> <meta charset="UTF-8"> <meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Do You Love Me?</title>

<style> * { box-sizing: border-box; } body { margin: 0; min-height: 100vh; display: flex; justify-content: center; align-items: center; font-family: "Poppins", Arial, sans-serif; background: linear-gradient(135deg, #ffd6e7, #ffeef5); overflow: hidden; } .container { text-align: center; width: 90%; max-width: 500px; padding: 35px 20px; } /* HEART */ .heart { font-size: 70px; animation: heartbeat 1.2s infinite; } @keyframes heartbeat { 0%, 100% { transform: scale(1); } 50% { transform: scale(1.15); } } /* QUESTION */ h1 { color: #ff4f81; font-size: 38px; margin: 15px 0 30px; } .buttons { position: relative; display: flex; justify-content: center; align-items: center; gap: 20px; min-height: 60px; } button { border: none; padding: 14px 30px; border-radius: 30px; font-size: 18px; font-weight: bold; cursor: pointer; transition: 0.2s; } #yesBtn { background: #ff4f81; color: white; box-shadow: 0 5px 15px rgba(255, 79, 129, 0.3); } #yesBtn:hover { transform: scale(1.08); background: #ff326b; } #noBtn { background: white; color: #ff4f81; border: 2px solid #ff4f81; position: relative; } .message { margin-top: 20px; color: #ff4f81; font-size: 16px; min-height: 25px; } /* LOVE LETTER */ .letter-container { display: none; animation: fadeIn 1s ease forwards; } .letter { background: #fffdf7; padding: 35px; border-radius: 8px; box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15); text-align: left; position: relative; transform: rotate(-1deg); } .letter::before { content: "💌"; position: absolute; top: -45px; left: 50%; transform: translateX(-50%); font-size: 55px; } .letter h2 { text-align: center; color: #e94f7c; margin-top: 15px; } .letter p { color: #555; line-height: 1.8; font-size: 16px; } .final-love { text-align: center; font-size: 30px; font-weight: bold; color: #ff326b; margin-top: 25px; animation: pulse 1.5s infinite; } .signature { text-align: right; margin-top: 30px; color: #555; font-size: 17px; line-height: 1.6; } .signature strong { color: #ff326b; font-size: 20px; } @keyframes pulse { 0%, 100% { transform: scale(1); } 50% { transform: scale(1.08); } } @keyframes fadeIn { from { opacity: 0; transform: translateY(30px) scale(0.9); } to { opacity: 1; transform: translateY(0) scale(1); } } /* FLOATING HEARTS */ .floating-heart { position: fixed; bottom: -30px; font-size: 25px; animation: floatUp 4s linear forwards; pointer-events: none; z-index: 10; } @keyframes floatUp { from { transform: translateY(0) rotate(0deg); opacity: 1; } to { transform: translateY(-110vh) rotate(360deg); opacity: 0; } } /* MOBILE */ @media (max-width: 500px) { h1 { font-size: 30px; } .heart { font-size: 60px; } .letter { padding: 25px 20px; } .letter p { font-size: 14px; } .final-love { font-size: 25px; } } </style>

</head>

<body>

<div class="container">

<!-- =========================
     QUESTION PAGE
========================== -->

<div id="questionPage">

  <div class="heart">
    ❤️
  </div>

  <h1>
    Do you love me?
  </h1>

  <div class="buttons">

    <button id="yesBtn">
      Yes 💗
    </button>

    <button id="noBtn">
      No 😢
    </button>

  </div>

  <div class="message" id="message"></div>

</div>


<!-- =========================
     LOVE LETTER PAGE
========================== -->

<div class="letter-container" id="letterPage">

  <div class="letter">

    <h2>
      💌 A Little Letter For You
    </h2>

    <p>
      <strong>Dear Pedrosa, my love,</strong>
    </p>

    <p>
      I just wanted to remind you how special you are to me.
      Every little moment with you means more than you know.
      Your smile, your laugh, and simply having you around
      can make my day so much better.
    </p>

    <p>
      No matter how many times I could say it,
      it would never feel like enough.
    </p>

    <p>
      You mean so much to me, and I hope you always remember
      that you are loved, appreciated, and treasured.
    </p>

    <div class="final-love">
      I LOVE YOU ❤️
    </div>

    <div class="signature">
      With all my love,<br>
      <strong>— Shin ❤️</strong>
    </div>

  </div>

</div>

</div>

<script> /* ========================= GET HTML ELEMENTS ========================== */ const yesBtn = document.getElementById("yesBtn"); const noBtn = document.getElementById("noBtn"); const message = document.getElementById("message"); const questionPage = document.getElementById("questionPage"); const letterPage = document.getElementById("letterPage"); let noCount = 0; /* ========================= NO BUTTON MESSAGES ========================== */ const messages = [ "Are you sure? 🥺", "Really? Think again! 😭", "Nooo, don't do that! 💔", "Please reconsider 🥹", "The button doesn't believe you 😂", "You can't escape love! ❤️", "Nice try! 😆", "The YES button is waiting... 💗" ]; /* ========================= NO BUTTON ========================== */ noBtn.addEventListener("click", function () { noCount++; /* * Change the message */ message.textContent = messages[Math.min(noCount - 1, messages.length - 1)]; /* * Move the NO button * to a random position */ const buttonWidth = noBtn.offsetWidth; const buttonHeight = noBtn.offsetHeight; const maxX = window.innerWidth - buttonWidth - 20; const maxY = window.innerHeight - buttonHeight - 20; const x = Math.random() * Math.max(maxX, 50); const y = Math.random() * Math.max(maxY, 50); noBtn.style.position = "fixed"; noBtn.style.left = x + "px"; noBtn.style.top = y + "px"; /* * Make YES button bigger * every time NO is clicked */ const scale = Math.min(1 + noCount * 0.08, 1.8); yesBtn.style.transform = `scale(${scale})`; /* * Create a floating heart */ createHeart(); }); /* ========================= YES BUTTON ========================== */ yesBtn.addEventListener("click", function () { /* * Hide question */ questionPage.style.display = "none"; /* * Show love letter */ letterPage.style.display = "block"; /* * Create lots of hearts */ for (let i = 0; i < 20; i++) { setTimeout(function () { createHeart(); }, i * 150); } }); /* ========================= FLOATING HEART FUNCTION ========================== */ function createHeart() { const heart = document.createElement("div"); heart.className = "floating-heart"; const heartTypes = [ "❤️", "💕", "💗", "💖", "💘", "💓" ]; heart.textContent = heartTypes[ Math.floor( Math.random() * heartTypes.length ) ]; /* * Random horizontal position */ heart.style.left = Math.random() * 100 + "vw"; /* * Random animation speed */ heart.style.animationDuration = (3 + Math.random() * 3) + "s"; document.body.appendChild(heart); /* * Remove heart after animation */ setTimeout(function () { heart.remove(); }, 6000); } </script>

</body> </html>
