<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Surakiad | My Profile</title>

    <!-- Google Font -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

    <link
        href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600&display=swap"
        rel="stylesheet"
    >

    <!-- Font Awesome -->
    <link
        rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"
    >

    <style>

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Kanit", sans-serif;
        }

        body {
            min-height: 100vh;

            display: flex;
            justify-content: center;
            align-items: center;

            color: white;
            overflow: hidden;

            background:
                linear-gradient(
                    135deg,
                    rgba(20, 20, 40, 0.75),
                    rgba(80, 20, 100, 0.65)
                ),
                url("{{ url_for('static', filename='images/background.jpg') }}");

            background-size: cover;
            background-position: center;
        }


        /* =========================
           Background Effect
        ========================= */

        .background {
            position: fixed;
            inset: 0;

            z-index: -1;

            background:
                radial-gradient(
                    circle at 20% 20%,
                    #ff4ecd55,
                    transparent 30%
                ),

                radial-gradient(
                    circle at 80% 80%,
                    #4e7bff55,
                    transparent 30%
                );

            animation: move 8s infinite alternate;
        }

        @keyframes move {

            from {
                transform: scale(1);
            }

            to {
                transform: scale(1.15);
            }

        }


        /* =========================
           Profile Card
        ========================= */

        .profile-card {

            width: 380px;
            max-width: 90%;

            padding: 35px 25px;

            text-align: center;

            background: rgba(255, 255, 255, 0.12);

            border: 1px solid rgba(255, 255, 255, 0.25);

            -webkit-backdrop-filter: blur(18px);
            backdrop-filter: blur(18px);

            border-radius: 25px;

            box-shadow:
                0 20px 60px rgba(0, 0, 0, 0.35);

            animation: appear 1s ease;
        }


        @keyframes appear {

            from {
                opacity: 0;
                transform: translateY(30px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }

        }


        /* =========================
           Profile Image
        ========================= */

        .profile-img {

            width: 120px;
            height: 120px;

            object-fit: cover;

            border-radius: 50%;

            border: 4px solid white;

            box-shadow:
                0 0 30px rgba(255, 255, 255, 0.4);

            margin-bottom: 15px;
        }


        /* =========================
           Name
        ========================= */

        h1 {

            font-size: 30px;

            margin-bottom: 5px;

        }


        .username {

            opacity: 0.75;

            font-size: 14px;

            margin-bottom: 15px;

        }


        /* =========================
           Bio
        ========================= */

        .bio {

            font-size: 15px;

            line-height: 1.7;

            margin-bottom: 25px;

            opacity: 0.9;

        }


        /* =========================
           Social
        ========================= */

        .social {

            display: flex;

            flex-direction: column;

            gap: 12px;

        }


        .social a {

            text-decoration: none;

            color: white;

            padding: 13px;

            border-radius: 14px;

            display: flex;

            align-items: center;

            justify-content: center;

            gap: 10px;

            background: rgba(255, 255, 255, 0.13);

            border: 1px solid rgba(255, 255, 255, 0.2);

            transition: 0.3s;

        }


        .social a:hover {

            transform: translateY(-3px);

            background: rgba(255, 255, 255, 0.25);

            box-shadow:
                0 8px 25px rgba(0, 0, 0, 0.2);

        }


        .facebook:hover {

            background: #1877f2 !important;

        }


        .instagram:hover {

            background:
                linear-gradient(
                    45deg,
                    #feda75,
                    #fa7e1e,
                    #d62976,
                    #962fbf,
                    #4f5bd5
                ) !important;

        }


        /* =========================
           Music Player
        ========================= */

        .music-player {

            margin-top: 25px;

            padding: 15px;

            border-radius: 15px;

            background: rgba(0, 0, 0, 0.2);

        }


        .music-title {

            font-size: 13px;

            opacity: 0.8;

            margin-bottom: 10px;

        }


        .music-btn {

            width: 48px;
            height: 48px;

            border: none;

            border-radius: 50%;

            color: white;

            background: rgba(255, 255, 255, 0.2);

            cursor: pointer;

            font-size: 18px;

            transition: 0.3s;

        }


        .music-btn:hover {

            transform: scale(1.1);

            background: rgba(255, 255, 255, 0.35);

        }


        .music-btn.playing {

            background: #9b4dff;

            box-shadow:
                0 0 20px rgba(155, 77, 255, 0.7);

        }


        /* =========================
           Footer
        ========================= */

        .footer {

            margin-top: 20px;

            font-size: 12px;

            opacity: 0.5;

        }


        /* =========================
           Mobile
        ========================= */

        @media (max-width: 500px) {

            .profile-card {

                padding: 30px 20px;

            }

            h1 {

                font-size: 26px;

            }

            .profile-img {

                width: 100px;
                height: 100px;

            }

        }

    </style>

</head>


<body>

    <!-- Background -->
    <div class="background"></div>


    <!-- Profile -->
    <div class="profile-card">


        <!-- Profile Image -->

        <img
            src="https://i.pinimg.com/736x/68/d8/61/68d861299a7948e5c6e0882658c4d413.jpg"
            class="profile-img"
            alt="รูปโปรไฟล์ของ ลมบรูพา"
        >


        <!-- Name -->

        <h1>ลมบรูพา</h1>


        <div class="username">
            @mntraarysuur
        </div>


        <!-- Bio -->

        <div class="bio">

            👋 สวัสดีครับ ผม ลมบรูพา
            <br>

            💻 พระจันทร์สีม่วงที่สองสว่างในยามที่ทุกคนเกลียด ถ้ามีเธอคอยเคียงข้างพระจันทร์ดวงนี้คงจะหน้ามองขึ้น
            <br>

            🎮 ชอบเล่นเกมและชอบด่าคน
            <br>

            ✨ ยินดีที่ได้รู้จักครับ

        </div>


        <!-- Social -->

        <div class="social">


            <!-- Facebook -->

            <a
                class="facebook"
                href="https://web.facebook.com/AzirTheEmperorOfTheSands3"
                target="_blank"
                rel="noopener noreferrer"
                aria-label="Facebook"
            >

                <i class="fa-brands fa-facebook"></i>

                Facebook

            </a>


            <!-- Instagram -->

            <a
                class="instagram"
                href="https://www.instagram.com/mntraarysuur/"
                target="_blank"
                rel="noopener noreferrer"
                aria-label="Instagram"
            >

                <i class="fa-brands fa-instagram"></i>

                Instagram

            </a>


        </div>


        <!-- Music -->

        <div class="music-player">


            <div class="music-title">
                🎵 My Favorite Song
            </div>


            <button
                class="music-btn"
                id="musicBtn"
                type="button"
                aria-label="เล่นเพลง"
                title="เล่นเพลง"
            >

                <i
                    id="musicIcon"
                    class="fa-solid fa-play"
                    aria-hidden="true"
                ></i>

            </button>


            <audio
                id="music"
                preload="metadata"
            >

                <source
                    src="https://w1.savevids.net/downloads/a17099da-eeb7-4e57-bec4-9e09a20666d7/Ultra%20Instinct%20Badass%20Remix%20Dragon%20Ball%20Super%20OST%20cover.mp3"
                    type="audio/mpeg"
                >

                เบราว์เซอร์ของคุณไม่รองรับการเล่นเพลง

            </audio>


        </div>


        <!-- Footer -->

        <div class="footer">

            © 2026 Surakiad

        </div>


    </div>


    <!-- JavaScript -->

    <script>

        const music = document.getElementById("music");

        const musicBtn = document.getElementById("musicBtn");

        const musicIcon = document.getElementById("musicIcon");


        musicBtn.addEventListener("click", function () {


            if (music.paused) {

                music.play();

                musicIcon.className =
                    "fa-solid fa-pause";

                musicBtn.classList.add("playing");

                musicBtn.setAttribute(
                    "aria-label",
                    "หยุดเพลง"
                );

                musicBtn.setAttribute(
                    "title",
                    "หยุดเพลง"
                );

            }

            else {

                music.pause();

                musicIcon.className =
                    "fa-solid fa-play";

                musicBtn.classList.remove("playing");

                musicBtn.setAttribute(
                    "aria-label",
                    "เล่นเพลง"
                );

                musicBtn.setAttribute(
                    "title",
                    "เล่นเพลง"
                );

            }

        });


        /* เมื่อเพลงเล่นจบ */

        music.addEventListener("ended", function () {

            musicIcon.className =
                "fa-solid fa-play";

            musicBtn.classList.remove("playing");

            musicBtn.setAttribute(
                "aria-label",
                "เล่นเพลง"
            );

            musicBtn.setAttribute(
                "title",
                "เล่นเพลง"
            );

        });

    </script>


</body>

</html>
