<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>mo.salem</title>
  <style>
    body {
      background-color: #000;
      margin: 0;
      padding: 0;
      font-family: 'Arial', sans-serif;
      color: white;
      text-align: center;
    }

    .gold-frame {
      border: 15px solid gold;
      box-shadow: 0 0 25px gold, inset 0 0 25px gold;
      border-radius: 30px;
      margin: 30px;
      padding: 30px;
    }

    h1 {
      font-size: 70px;
      color: gold;
      text-shadow: 2px 2px 10px #ffcc00, 4px 4px 20px #b8860b;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    .sub-text {
      font-size: 22px;
      color: #ffd700;
      margin-top: -10px;
      margin-bottom: 40px;
    }

    .arrow {
      font-size: 50px;
      color: gold;
      animation: bounce 1.5s infinite;
      margin-bottom: 20px;
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(15px); }
    }

    .gift-box {
      width: 200px;
      margin: auto;
      cursor: pointer;
      transition: transform 0.3s ease;
    }

    .gift-box:hover {
      transform: scale(1.1);
    }

    .hearts {
      display: none;
      margin-top: 20px;
      font-size: 30px;
      color: red;
      animation: pop 1s forwards;
    }

    @keyframes pop {
      from { opacity: 0; transform: scale(0.5); }
      to { opacity: 1; transform: scale(1); }
    }
  </style>
</head>
<body>

  <div class="gold-frame">
    <h1>Mo.<span style="color:#fff; text-shadow: 2px 2px 5px gold;">Salem</span></h1>

    <div class="sub-text">mo.salem بيمسي على الشلة كلها<br>
      لو انت جيت هنا دلوقتي يبقى انت من الشلة 👑
    </div>

    <div class="arrow">⬇️</div>

    <!-- صندوق الهدايا -->
    <img class="gift-box" id="giftBox" src="https://i.imgur.com/xU7Y2GU.gif" alt="صندوق هدايا">

    <!-- قلوب -->
    <div class="hearts" id="hearts">❤️❤️❤️ الشلة ❤️❤️❤️</div>
  </div>

  <script>
    // لما المستخدم يضغط على صندوق الهدايا
    let giftBox = document.getElementById("giftBox");
    let hearts = document.getElementById("hearts");
    let clicks = 0;

    giftBox.addEventListener("click", function() {
      clicks++;
      if (clicks >= 3) {
        hearts.style.display = "block";
      }
    });
  </script>

</body>
</html>
