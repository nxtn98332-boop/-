<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<title>Hacking System</title>
<style>
body {
  background: black;
  color: #00ff00;
  font-family: monospace;
  text-align: center;
  padding-top: 50px;
}

#box {
  border: 2px solid #00ff00;
  width: 90%;
  max-width: 400px;
  margin: auto;
  padding: 20px;
}

.progress {
  margin-top: 20px;
}
</style>
</head>
<body>

<div id="box">
  <h2>🔐 HACKING IN PROGRESS...</h2>
  <p id="log">Connecting to server...</p>
  <div class="progress">
    <span id="percent">0%</span>
  </div>
</div>

<script>
let percent = 0;
let logs = [
  "Connecting to server...",
  "Bypassing firewall...",
  "Accessing user data...",
  "Decrypting password...",
  "Downloading files..."
];

let interval = setInterval(() => {
  percent += 5;
  document.getElementById("percent").innerText = percent + "%";
  document.getElementById("log").innerText =
    logs[Math.floor(Math.random() * logs.length)];

  if (percent >= 100) {
    clearInterval(interval);
    setTimeout(() => {
      document.getElementById("box").innerHTML = `
        <h2 style="color:white;">😂 โดนแกล้งแล้ว!</h2>
        <p style="color:white;">
        ไม่มีการแฮ็กจริง ขำๆ เท่านั้น<br>
        อย่าตกใจนะเพื่อน 😆
        </p>
      `;
    }, 1000);
  }
}, 400);
</script>

</body>
</html>
