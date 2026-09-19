<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>For Pedrosa ❤️</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ffd1e1, #ffeef5);
      overflow: hidden;
    }

    .container {
      width: 90%;
      max-width: 520px;
      text-align: center;
      padding: 30px 20px;
    }

    /* =========================
       QUESTION PAGE
    ========================= */

    .heart {
      font-size: 75px;
      animation: heartbeat 1.2s infinite;
    }

    @keyframes heartbeat {
      0%, 100% {
        transform: scale(1);
      }

      50% {
        transform: scale(1.15);
      }
    }

    h1 {
      color: #ff3f78;
      font-size: 40px;
      margin: 15px 0 35px;
    }

    .buttons {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
      min-height: 60px;
    }

    button {
      border: none;
      padding: 14px 30px;
      border-radius: 30px;
      font-size: 18px;
      font-weight: bold;
      cursor: pointer;
      transition: transform 0.2s, background 0.2s;
    }

    #yesBtn {
      background: #ff3f78;
      color: white;
      box-shadow: 0 5px 15px rgba(255, 63, 120, 0.3);
    }

    #yesBtn:hover {
      background: #ff1f62;
      transform: scale(1.08);
    }

    #noBtn {
      background: white;
      color: #ff3f78;
      border: 2px solid #ff3f78;
    }

    .message {
      color: #ff3f78;
      font-size: 17px;
      margin-top: 25px;
      min-height: 30px;
    }

    /* =========================
       LOVE LETTER
    ========================= */

    #letterPage {
      display: none;
    }

    .letter {
      background: #fffdf5;
      padding: 35px;
      border-radius: 10px;
      box-shadow: 0 12px 35px rgba(0, 0, 0, 0.15);
      text-align: left;
      position: relative;
      animation: letterAppear 1s ease forwards;
    }

    .letter::before {
      content: "💌";
      position: absolute;
      top: -45px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 55px;
    }

    .letter h2 {
      text-align: center;
      color: #ff3f78;
      margin-top: 10px;
      margin-bottom: 25px;
    }

    .letter p {
      color: #555;
      line-height: 1.8;
      font-size: 16px;
    }

    .greeting {
      font-weight: bold;
      color: #444 !important;
    }

    .final-love {
      text-align: center;
      color: #ff2868;
      font-size: 30px;
      font-weight: bold;
      margin-top: 30px;
      animation: lovePulse 1.5s infinite;
    }

    .signature {
      text-align: right;
      margin-top: 30px;
      color: #555;
      line-height: 1.7;
    }

    .signature strong {
      color: #ff2868;
      font-size: 21px;
    }

    @keyframes letterAppear {
      from {
        opacity: 0;
        transform: translateY(40px) scale(0.9) rotate(-2deg);
      }

      to {
        opacity: 1;
        transform: translateY(0) scale(1) rotate(-1deg);
      }
    }

    @keyframes lovePulse {
      0%, 100% {
        transform: scale(1);
      }

      50% {
        transform: scale(1.08);
      }
    }

    /* =========================
       FLOATING HEARTS
    ========================= */

    .floating-heart {
      position: fixed;
      bottom: -40px;
      font-size: 25px;
      pointer-events: none;
      z-index: 100;
      animation: floatUp 4s linear forwards;
    }

    @keyframes floatUp {
      0% {
        transform: translateY(0) rotate(0deg);
        opacity: 1;
      }

      100% {
        transform: translateY(-110vh) rotate(360deg);
        opacity: 0;
      }
    }

    /* =========================
       MOBILE
    ========================= */

    @media (max-width: 500px) {

      h1 {
        font-size: 30px;
      }

      .heart {
        font-size: 60px;
      }

      .letter {
        padding: 25px 20px;
      }

      .letter p {
        font-size: 14px;
      }

      .final-love {
        font-size: 25px;
      }

      button {
        padding: 13px 25px;
        font-size: 16px;
      }
    }

  </style>
</head>


<body>

  <div class="container">

    <!-- =========================
         QUESTION
    ========================== -->

    <div id="questionPage">

      <div class="heart">
        ❤️
      </div>

      <h1>
        Do you love me?
      </h1>

      <div class="buttons">

        <button id="yesBtn" type="button">
          Yes 💗
        </button>

        <button id="noBtn" type="button">
          No 😢
        </button>

      </div>

      <div class="message" id="message"></div>

    </div>


    <!-- =========================
         LOVE LETTER
    ========================== -->

    <div id="letterPage">

      <div class="letter">

        <h2>
          💌 A Little Letter For You
        </h2>

        <p class="greeting">
          Dear Pedrosa, my love,
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

        <p>
          Thank you for being someone so special in my life.
          I hope this little surprise makes you smile. ❤️
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


  <script>

    /* =========================
       GET ELEMENTS
    ========================== */

    const yesBtn = document.getElementById("yesBtn");
    const noBtn = document.getElementById("noBtn");

    const message = document.getElementById("message");

    const questionPage =
      document.getElementById("questionPage");

    const letterPage =
      document.getElementById("letterPage");


    let noCount = 0;


    /* =========================
       NO BUTTON MESSAGES
    ========================== */

    const messages = [

      "Are you sure? 🥺",

      "Really? Think again! 😭",

      "Nooo, don't do that! 💔",

      "Please reconsider 🥹",

      "Why are you clicking No? 😭❤️",

      "The button is running away! 😂",

      "You can't escape the question! 💕",

      "Just click YES already! 🥺❤️"

    ];


    /* =========================
       WHEN SHE CLICKS NO
    ========================== */

    noBtn.addEventListener("click", function () {

      noCount++;


      /* Change the message */

      message.textContent =
        messages[
          Math.min(
            noCount - 1,
            messages.length - 1
          )
        ];


      /* Move the NO button */

      const buttonWidth =
        noBtn.offsetWidth;

      const buttonHeight =
        noBtn.offsetHeight;


      const maxX =
        window.innerWidth -
        buttonWidth -
        20;


      const maxY =
        window.innerHeight -
        buttonHeight -
        20;


      const x =
        Math.random() *
        Math.max(maxX, 50);


      const y =
        Math.random() *
        Math.max(maxY, 50);


      noBtn.style.position = "fixed";

      noBtn.style.left = x + "px";

      noBtn.style.top = y + "px";


      /* Make YES bigger */

      const scale =
        Math.min(
          1 + noCount * 0.08,
          1.8
        );


      yesBtn.style.transform =
        "scale(" + scale + ")";


      /* Create a heart */

      createHeart();

    });


    /* =========================
       WHEN SHE CLICKS YES
    ========================== */

    yesBtn.addEventListener("click", function () {

      /* Hide the question */

      questionPage.style.display = "none";


      /* Show the letter */

      letterPage.style.display = "block";


      /* Heart celebration */

      for (let i = 0; i < 25; i++) {

        setTimeout(
          createHeart,
          i * 150
        );

      }

    });


    /* =========================
       CREATE FLOATING HEART
    ========================== */

    function createHeart() {

      const heart =
        document.createElement("div");


      heart.className =
        "floating-heart";


      const hearts = [
        "❤️",
        "💕",
        "💗",
        "💖",
        "💘",
        "💓",
        "💞"
      ];


      heart.textContent =
        hearts[
          Math.floor(
            Math.random() *
            hearts.length
          )
        ];


      /* Random horizontal position */

      heart.style.left =
        Math.random() * 100 + "vw";


      /* Random size */

      heart.style.fontSize =
        (20 + Math.random() * 20) + "px";


      /* Random speed */

      heart.style.animationDuration =
        (3 + Math.random() * 3) + "s";


      document.body.appendChild(heart);


      /* Delete after animation */

      setTimeout(function () {

        heart.remove();

      }, 6000);

    }

  </script>

</body>
</html>
