# recreation-of-youareanidiot.org
warning if you run this you might lag up your pc because this was reused in youareanidiot.org
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>You Are An Idiot</title>
<style>
    body {
        margin: 0;
        background: black;
        color: white;
        font-family: Arial, sans-serif;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100vh;
        flex-direction: column;
        text-align: center;
    }
    h1 {
        font-size: 4rem;
        margin: 0.5rem;
    }
    button {
        padding: 1rem 2rem;
        font-size: 1.2rem;
        cursor: pointer;
        border: none;
        background: red;
        color: white;
        border-radius: 8px;
    }
</style>
</head>
<body>

<h1>YOU ARE AN IDIOT</h1>
<p>Click the button… if you dare 😈</p>
<button id="start">Start Chaos</button>

<audio id="audio" loop>
    <!-- Replace with your own audio file path -->
    <source src="youare.mp3" type="audio/mpeg">
</audio>

<script>
const startBtn = document.getElementById('start');
const audio = document.getElementById('audio');

startBtn.addEventListener('click', () => {
    // Try to play audio (HTML5, user gesture)
    audio.play().catch(() => {});

    // Spawn a bunch of popups
    for (let i = 0; i < 5; i++) {
        spawnPopup();
    }

    // Keep spawning more over time
    setInterval(() => {
        spawnPopup();
    }, 1500);
});

function spawnPopup() {
    const w = 300;
    const h = 200;
    const left = Math.floor(Math.random() * (screen.width - w));
    const top = Math.floor(Math.random() * (screen.height - h));

    const popup = window.open(
        '',
        '_blank',
        `width=${w},height=${h},left=${left},top=${top}`
    );

    if (!popup) return; // blocked by browser

    popup.document.write(`
        <!DOCTYPE html>
        <html lang="en">
        <head>
        <meta charset="UTF-8">
        <title>LOL</title>
        <style>
            body {
                margin: 0;
                background: yellow;
                font-family: Arial, sans-serif;
                display: flex;
                align-items: center;
                justify-content: center;
                height: 100vh;
                font-size: 2rem;
                text-align: center;
            }
        </style>
        </head>
        <body>
        😂 YOU ARE AN IDIOT 😂
        <script>
            let x = ${left}, y = ${top};
            let dx = (Math.random() > 0.5 ? 6 : -6);
            let dy = (Math.random() > 0.5 ? 6 : -6);

            setInterval(() => {
                x += dx;
                y += dy;

                if (x <= 0 || x >= screen.width - ${w}) dx = -dx;
                if (y <= 0 || y >= screen.height - ${h}) dy = -dy;

                window.moveTo(x, y);
            }, 30);

            document.body.onclick = () => {
                window.open(location.href, '_blank', 'width=${w},height=${h}');
            };
        <\/script>
        </body>
        </html>
    `);
}
</script>

</body>
</html>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>You Are An Idiot</title>
<style>
    body {
        margin: 0;
        background: black;
        color: white;
        font-family: Arial, sans-serif;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100vh;
        flex-direction: column;
        text-align: center;
    }
    h1 {
        font-size: 4rem;
        margin: 0.5rem;
    }
    button {
        padding: 1rem 2rem;
        font-size: 1.2rem;
        cursor: pointer;
        border: none;
        background: red;
        color: white;
        border-radius: 8px;
    }
</style>
</head>
<body>

<h1>YOU ARE AN IDIOT 😂</h1>
<p>Click to unleash chaos</p>
<button id="start">Start</button>

<script>
document.getElementById("start").onclick = () => {
    // Spawn initial popups
    for (let i = 0; i < 5; i++) spawnPopup();

    // Keep spawning more
    setInterval(spawnPopup, 2000);
};

function spawnPopup() {
    const w = 300, h = 200;
    const left = Math.random() * (screen.width - w);
    const top = Math.random() * (screen.height - h);

    const popup = window.open("", "_blank",
        `width=${w},height=${h},left=${left},top=${top}`);

    if (!popup) return; // popup blocked

    popup.document.write(`
        <!DOCTYPE html>
        <html>
        <head>
        <meta charset="UTF-8">
        <title>LOL</title>
        <style>
            body {
                margin: 0;
                background: yellow;
                font-family: Arial, sans-serif;
                display: flex;
                align-items: center;
                justify
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>You Are An Idiot!</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            background: black;
            font-family: Arial, sans-serif;
        }

        #idiot {
            position: absolute;
            font-size: 3rem;
            font-weight: bold;
            color: white;
            text-shadow: 0 0 10px white;
        }
    </style>
</head>
<body>

<div id="idiot">YOU ARE AN IDIOT!</div>

<script>
    const text = document.getElementById("idiot");

    let x = 100;
    let y = 100;

    // SUPER FAST SPEED
    let dx = 18;  
    let dy = 18;

    function bounce() {
        const w = window.innerWidth;
        const h = window.innerHeight;
        const rect = text.getBoundingClientRect();

        x += dx;
        y += dy;

        if (x <= 0 || x + rect.width >= w) dx = -dx;
        if (y <= 0 || y + rect.height >= h) dy = -dy;

        text.style.left = x + "px";
        text.style.top = y + "px";

        requestAnimationFrame(bounce);
    }

    bounce();
</script>

</body>
</html>
