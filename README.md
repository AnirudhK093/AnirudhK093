<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Anirudh K | Cybersecurity Analyst</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Courier New", monospace;
}

body {
    background: black;
    color: #00ff88;
    overflow: hidden;
}

/* Matrix Canvas */
canvas {
    position: fixed;
    top: 0;
    left: 0;
    z-index: -1;
}

/* Main Container */
.container {
    position: relative;
    z-index: 2;
    text-align: center;
    padding-top: 15vh;
}

/* Neon Title */
h1 {
    font-size: 3rem;
    color: #00ff88;
    text-shadow: 0 0 10px #00ff88, 0 0 30px #00ff88;
    letter-spacing: 4px;
}

.subtitle {
    margin-top: 10px;
    font-size: 1.2rem;
    color: #00ffaa;
    opacity: 0.8;
}

/* Terminal Box */
.terminal {
    width: 70%;
    margin: 40px auto;
    padding: 25px;
    background: rgba(0, 0, 0, 0.8);
    border: 1px solid #00ff88;
    box-shadow: 0 0 20px #00ff88;
    text-align: left;
    line-height: 1.6;
    backdrop-filter: blur(5px);
}

.command {
    color: #00ffaa;
}

.footer {
    position: absolute;
    bottom: 20px;
    width: 100%;
    text-align: center;
    font-size: 0.9rem;
    color: #00ff88;
    opacity: 0.6;
}
</style>
</head>
<body>

<canvas id="matrix"></canvas>

<div class="container">
    <h1>ANIRUDH K</h1>
    <div class="subtitle">Cybersecurity Analyst | Offensive & Defensive Security</div>

    <div class="terminal">
        <div><span class="command">anirudh@matrix:~$</span> whoami</div>
        <div>Anirudh K</div><br>

        <div><span class="command">anirudh@matrix:~$</span> cat role.txt</div>
        <div>Cybersecurity Analyst</div><br>

        <div><span class="command">anirudh@matrix:~$</span> ls expertise/</div>
        <div>
            ethical_hacking<br>
            red_team_operations<br>
            blue_team_defense<br>
            active_directory_security<br>
            siem_engineering<br>
            incident_response
        </div><br>

        <div><span class="command">anirudh@matrix:~$</span> echo $MISSION</div>
        <div>Break. Understand. Secure. Repeat.</div><br>

        <div><span class="command">anirudh@matrix:~$</span> contact --secure</div>
        <div>
            email: anirudhnair799@gmail.com<br>
            location: India
        </div>
    </div>
</div>

<div class="footer">
    © 2026 Anirudh K — Matrix Mode Active
</div>

<script>
const canvas = document.getElementById("matrix");
const ctx = canvas.getContext("2d");

canvas.height = window.innerHeight;
canvas.width = window.innerWidth;

const letters = "アァカサタナハマヤャラワ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ";
const fontSize = 16;
const columns = canvas.width / fontSize;
const drops = [];

for (let x = 0; x < columns; x++) {
    drops[x] = 1;
}

function draw() {
    ctx.fillStyle = "rgba(0, 0, 0, 0.05)";
    ctx.fillRect(0, 0, canvas.width, canvas.height);

    ctx.fillStyle = "#00ff88";
    ctx.font = fontSize + "px monospace";

    for (let i = 0; i < drops.length; i++) {
        const text = letters.charAt(Math.floor(Math.random() * letters.length));
        ctx.fillText(text, i * fontSize, drops[i] * fontSize);

        if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
            drops[i] = 0;
        }
        drops[i]++;
    }
}

setInterval(draw, 35);

window.addEventListener("resize", () => {
    canvas.height = window.innerHeight;
    canvas.width = window.innerWidth;
});
</script>

</body>
</html>
