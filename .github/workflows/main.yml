<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ESG-IN Roulette Game</title>
  <style>
    body { font-family: Arial, sans-serif; text-align: center; padding: 40px; }
    .wheel {
      margin: 0 auto;
      width: 300px;
      height: 300px;
      border-radius: 50%;
      border: 10px solid #4CAF50;
      position: relative;
    }
    .wheel span {
      position: absolute;
      width: 50%;
      height: 50%;
      left: 50%;
      top: 50%;
      transform-origin: 0% 0%;
      background: #c8e6c9;
      border: 1px solid #2e7d32;
    }
    #spin {
      margin-top: 30px;
      padding: 10px 20px;
      font-size: 18px;
    }
    #result {
      margin-top: 20px;
      font-size: 20px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>🎯 ESG-IN Spin for Points!</h1>
  <div class="wheel" id="wheel"></div>
  <button id="spin">🎰 Spin Now</button>
  <div id="result"></div>

  <script>
    const options = ["1,000P", "500P", "300P", "200P", "100P", "50P", "30P"];
    const wheel = document.getElementById("wheel");
    const result = document.getElementById("result");

    function createWheel() {
      const angle = 360 / options.length;
      options.forEach((label, i) => {
        const span = document.createElement("span");
        span.style.transform = `rotate(${i * angle}deg) skewY(-${90 - angle}deg)`;
        span.innerText = label;
        wheel.appendChild(span);
      });
    }

    function spinWheel() {
      const angle = 3600 + Math.floor(Math.random() * 360); // random spin
      wheel.style.transition = "transform 4s ease-out";
      wheel.style.transform = `rotate(${angle}deg)`;

      const index = Math.floor(((angle % 360) / 360) * options.length);
      const prize = options[(options.length - index) % options.length];
      setTimeout(() => {
        result.textContent = `🎉 You won ${prize}!`;
      }, 4000);
    }

    createWheel();
    document.getElementById("spin").addEventListener("click", spinWheel);
  </script>
</body>
</html>
