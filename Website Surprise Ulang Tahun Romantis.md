```html
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>For You ❤️</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;
    overflow: hidden;
    font-family: "Segoe UI", sans-serif;
    background:
        radial-gradient(circle at top, #72145f, #25051f 55%, #080008);
    color: white;
}

/* HALAMAN AWAL */

.start {
    position: fixed;
    inset: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    z-index: 10;
    background:
        radial-gradient(circle, #641653, #170315);
    transition: 1s;
}

.start-box {
    animation: muncul 1.5s ease;
}

.start-box h1 {
    font-size: 25px;
    margin-bottom: 25px;
}

.envelope {
    font-size: 110px;
    cursor: pointer;
    animation: goyang 1.5s infinite;
    filter: drop-shadow(0 0 25px #ff55ad);
}

.start-box p {
    margin-top: 20px;
    opacity: .8;
}

/* HALAMAN UTAMA */

.main {
    min-height: 100vh;
    display: none;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 25px;
}

.card {
    width: 100%;
    max-width: 430px;
    padding: 35px 25px;
    border-radius: 30px;

    background: rgba(255,255,255,.08);
    backdrop-filter: blur(12px);

    border: 1px solid rgba(255,255,255,.15);

    box-shadow:
        0 0 40px rgba(255,50,160,.25);
    
    animation: muncul 1.5s ease;
}

.big-heart {
    font-size: 70px;
    animation: beat 1.2s infinite;
}

h1 {
    margin: 15px 0;
    font-size: 32px;

    background: linear-gradient(
        90deg,
        #ff72bd,
        white,
        #ff72bd
    );

    -webkit-background-clip: text;
    color: transparent;
}

h2 {
    color: #ff9bd4;
    margin-bottom: 20px;
}

.message {
    line-height: 1.8;
    font-size: 16px;
}

.message b {
    color: #ff8dcc;
}

.photo {
    width: 180px;
    height: 180px;

    object-fit: cover;

    border-radius: 50%;

    border: 5px solid rgba(255,255,255,.8);

    margin: 15px auto;

    display: block;

    box-shadow:
        0 0 30px rgba(255,80,180,.7);
}

/* BUTTON */

.music-btn {
    margin-top: 20px;

    padding: 12px 22px;

    border: none;
    border-radius: 30px;

    color: white;

    background: linear-gradient(
        45deg,
        #ff3d9b,
        #ff75bd
    );

    cursor: pointer;

    box-shadow:
        0 0 20px rgba(255,50,160,.5);
}

/* HATI TERBANG */

.heart {
    position: fixed;
    bottom: -40px;

    pointer-events: none;

    animation: naik linear forwards;

    z-index: 1;
}

/* CONFETTI */

.confetti {
    position: fixed;

    width: 8px;
    height: 15px;

    top: -20px;

    animation: jatuh linear forwards;

    z-index: 20;
}

/* ANIMASI */

@keyframes beat {

    0%,100% {
        transform: scale(1);
    }

    50% {
        transform: scale(1.25);
    }
}

@keyframes goyang {

    0%,100% {
        transform: rotate(-5deg);
    }

    50% {
        transform: rotate(5deg);
    }
}

@keyframes muncul {

    from {
        opacity: 0;
        transform: translateY(40px) scale(.9);
    }

    to {
        opacity: 1;
        transform: translateY(0) scale(1);
    }
}

@keyframes naik {

    to {
        transform:
            translateY(-110vh)
            rotate(360deg);

        opacity: 0;
    }
}

@keyframes jatuh {

    to {
        transform:
            translateY(110vh)
            rotate(720deg);
    }
}

</style>
</head>

<body>


<!-- ===================== -->
<!-- HALAMAN PEMBUKA -->
<!-- ===================== -->

<div class="start" id="start">

    <div class="start-box">

        <h1>
            💌 Ada surat untuk kamu...
        </h1>

        <div
            class="envelope"
            onclick="buka()">

            💌

        </div>

        <p>
            Klik suratnya ❤️
        </p>

    </div>

</div>


<!-- ===================== -->
<!-- HALAMAN UTAMA -->
<!-- ===================== -->

<div class="main" id="main">

    <div class="card">

        <div class="big-heart">
            ❤️
        </div>


        <h1>
            I LOVE YOU
        </h1>


        <h2>
            SAYANG 💕
        </h2>


        <!-- GANTI FOTO DI SINI -->

        <img
            src="foto.jpg"
            class="photo"
            alt="Foto kita">


        <div class="message">

            <p>
                🎂 <b>SELAMAT ULANG TAHUN</b> 🎂
            </p>

            <br>

            <p>
                Hari ini adalah hari spesial,
                karena seseorang yang sangat berarti
                buat aku bertambah satu tahun lagi. ❤️
            </p>

            <br>

            <p>
                Semoga di umur yang baru,
                kamu selalu diberikan kesehatan,
                kebahagiaan, dan kesuksesan.
            </p>

            <br>

            <p>
                Semoga semua impian kamu
                satu per satu menjadi kenyataan.
                ✨
            </p>

            <br>

            <p>
                Terima kasih sudah hadir
                dan menjadi bagian indah
                dalam hidupku.
            </p>

            <br>

            <p>
                Aku mungkin tidak bisa memberikan
                semuanya di dunia ini,
                tapi aku akan selalu berusaha
                memberikan yang terbaik untukmu. ❤️
            </p>

            <br>

            <p>
                <b>
                I LOVE YOU MORE THAN WORDS CAN SAY ❤️
                </b>
            </p>

            <br>

            <p>
                🎂 HAPPY BIRTHDAY, SAYANG 🎂
            </p>

        </div>


        <button
            class="music-btn"
            onclick="musik()">

            🎵 Putar Musik

        </button>

    </div>

</div>


<!-- MUSIK -->

<audio
    id="music"
    loop>

    <!--
    GANTI "lagu.mp3"
    DENGAN FILE MUSIK KAMU
    -->

    <source
        src="lagu.mp3"
        type="audio/mpeg">

</audio>


<script>

/* =====================
   BUKA SURPRISE
===================== */

function buka() {

    document.getElementById("start").style.opacity = "0";

    setTimeout(() => {

        document.getElementById("start").style.display = "none";

        document.getElementById("main").style.display = "flex";

        confetti();

    }, 1000);

}


/* =====================
   MUSIK
===================== */

function musik() {

    const audio =
        document.getElementById("music");

    audio.play();

}


/* =====================
   HATI TERBANG
===================== */

setInterval(() => {

    const heart =
        document.createElement("div");

    heart.className = "heart";

    heart.innerHTML =
        ["❤️","💕","💗","💖","💘","💝"]
        [Math.floor(Math.random() * 6)];

    heart.style.left =
        Math.random() * 100 + "vw";

    heart.style.fontSize =
        (Math.random() * 25 + 15) + "px";

    heart.style.animationDuration =
        (Math.random() * 5 + 5) + "s";

    document.body.appendChild(heart);


    setTimeout(() => {

        heart.remove();

    }, 10000);

}, 500);


/* =====================
   CONFETTI
===================== */

function confetti() {

    for(let i = 0; i < 120; i++) {

        const c =
            document.createElement("div");

        c.className = "confetti";

        c.style.left =
            Math.random() * 100 + "vw";

        c.style.background =
            [
                "#ff4fa3",
                "#ffd166",
                "#ffffff",
                "#c77dff",
                "#ff6b9d"
            ][Math.floor(Math.random() * 5)];

        c.style.animationDuration =
            (Math.random() * 3 + 2) + "s";

        document.body.appendChild(c);

        setTimeout(() => {

            c.remove();

        }, 5000);

    }

}

</script>

</body>
</html>
```