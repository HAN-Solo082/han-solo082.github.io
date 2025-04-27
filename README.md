
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>A Mystic Falls Surprise</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background: linear-gradient(180deg, #1c2526, #4b2e39);
      font-family: 'Times New Roman', serif;
      color: #e6d7c3;
      text-align: center;
      overflow: hidden;
    }
    .container {
      background: rgba(0, 0, 0, 0.7);
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5);
      max-width: 400px;
      animation: fadeIn 1s ease-in-out;
    }
    h1 {
      font-size: 2em;
      color: #b22222;
      margin-bottom: 15px;
      text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
    }
    p {
      font-size: 1.1em;
      line-height: 1.5;
      margin: 10px 0;
    }
    button {
      padding: 10px 20px;
      font-size: 1em;
      color: #fff;
      background: #800000;
      border: none;
      border-radius: 20px;
      cursor: pointer;
      transition: background 0.3s, transform 0.2s;
      margin-top: 15px;
    }
    button:hover {
      background: #a52a2a;
      transform: scale(1.1);
    }
    #surpriseImage {
      display: none;
      margin-top: 20px;
      animation: slideIn 0.8s ease-in;
    }
    img {
      max-width: 200px;
      height: auto;
      border: 2px solid #b22222;
      border-radius: 5px;
    }
    .blood-drip {
      position: absolute;
      width: 100%;
      height: 100%;
      pointer-events: none;
    }
    .blood-drip span {
      position: absolute;
      font-size: 1em;
      color: #ff4040;
      animation: drip 3s infinite;
      opacity: 0.8;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes slideIn {
      from { opacity: 0; transform: translateX(-20px); }
      to { opacity: 1; transform: translateX(0); }
    }
    @keyframes drip {
      0% { transform: translateY(-100vh); opacity: 0.8; }
      100% { transform: translateY(100vh); opacity: 0; }
    }
  </style>
</head>
<body>
  <div class="blood-drip" id="drips"></div>
  <div class="container">
    <h1>Hey, Jenny</h1>
    <p>There's a wish I made for the both of us</p>
    <p>Ready for your surprise?</p>
    <button onclick="revealSurprise()">Unveil the Magic</button>
    <div id="surpriseImage">
      <img src="https://i.pinimg.com/736x/ed/b1/cd/edb1cdb56d0c9e9bb85428871d3176e7.jpg">
    </div>
  </div>

  <script>
    function revealSurprise() {
      document.getElementById('surpriseImage').style.display = 'block';
    }

    // Create dripping blood effect
    const dripsContainer = document.getElementById('drips');
    function createDrip() {
      const drip = document.createElement('span');
      drip.innerHTML = '💧';
      drip.style.left = Math.random() * 100 + 'vw';
      drip.style.animationDuration = Math.random() * 2 + 2 + 's';
      dripsContainer.appendChild(drip);
      setTimeout(() => drip.remove(), 3000);
    }
    setInterval(createDrip, 700);
  </script>
</body>
</html>
