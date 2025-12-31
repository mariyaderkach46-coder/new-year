<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<title>С Новым годом!</title>
<style>
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: radial-gradient(circle, #00111a, #000);
    color: white;
    overflow: hidden;
    text-align: center;
}

#gift {
    font-size: 120px;
    cursor: pointer;
    margin-top: 25vh;
    animation: pulse 1.5s infinite;
}

@keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
}

#content {
    display: none;
    padding-top: 40px;
}

h1 {
    font-size: 48px;
    margin-bottom: 20px;
}

img {
    max-width: 300px;
    border-radius: 20px;
    box-shadow: 0 0 20px gold;
}

.firework {
    position: absolute;
    width: 6px;
    height: 6px;
    background: gold;
    border-radius: 50%;
    animation: explode 1s linear infinite;
}

@keyframes explode {
    from { transform: scale(1); opacity: 1; }
    to { transform: scale(6); opacity: 0; }
}
</style>
</head>
<body>

<div id="gift">🎁</div>

<div id="content">
    <h1>🎄 С Новым годом! 🎄</h1>
    <p>Пусть этот год принесёт счастье, радость и исполнение желаний ✨</p>
    <img src="https://i.imgur.com/4AiXzf8.jpeg" alt="Фото">
</div>

<script>
document.getElementById("gift").onclick = () => {
    document.getElementById("gift").style.display = "none";
    document.getElementById("content").style.display = "block";
    setInterval(createFirework, 200);
};

function createFirework() {
    const fw = document.createElement("div");
    fw.className = "firework";
    fw.style.left = Math.random() * window.innerWidth + "px";
    fw.style.top = Math.random() * window.innerHeight + "px";
    fw.style.background = `hsl(${Math.random()*360},100%,60%)`;
    document.body.appendChild(fw);
    setTimeout(() => fw.remove(), 1000);
}
</script>

</body>
</html># new-year
