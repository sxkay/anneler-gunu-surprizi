<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Anneler Günü Sürprizi</title>
<style>
  body {
    background-color: #ffe4e1;
    font-family: Arial, sans-serif;
    margin: 0;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  h1 {
    font-size: 2em;
    margin-bottom: 20px;
  }
  button {
    padding: 15px 30px;
    font-size: 1.2em;
    background-color: #f08080;
    border: none;
    border-radius: 10px;
    cursor: pointer;
  }
  #confetti-canvas {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 9999;
  }
</style>
</head>
<body>

<h1>Anneler Günün Kutlu Olsun, Annecim!</h1>
<button id="surpriseBtn">Tıkla Bakalım 💖</button>
<canvas id="confetti-canvas"></canvas>
<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.4.0/dist/confetti.browser.min.js"></script>
<script>
  const btn = document.getElementById('surpriseBtn');
  btn.onclick = () => {
    confetti({
      particleCount: 300,
      spread: 100,
      origin: { y: 0.6 }
    });
  }
</script>

</body>
</html>
