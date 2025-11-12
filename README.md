<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CANCER HAMMERS - Официальный сайт</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Bebas Neue', 'Impact', 'Arial Black', sans-serif;
        }

        :root {
            --primary: #0a0a0a;
            --secondary: #1a1a1a;
            --accent: #ff0000;
            --accent-glow: #ff4444;
            --text: #ffffff;
            --text-secondary: #cccccc;
        }

        body {
            background: var(--primary);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
            background-image: 
                radial-gradient(circle at 20% 30%, rgba(255, 0, 0, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 70%, rgba(255, 68, 68, 0.1) 0%, transparent 50%);
        }

        /* Гранж текстура */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                repeating-linear-gradient(
                    0deg,
                    transparent,
                    transparent 2px,
                    rgba(255, 0, 0, 0.03) 2px,
                    rgba(255, 0, 0, 0.03) 4px
                );
            pointer-events: none;
            z-index: 1000;
            mix-blend-mode: overlay;
        }

        /* Панк-хедер */
        header {
            background: rgba(10, 10, 10, 0.95);
            border-bottom: 3px solid var(--accent);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 2.5rem;
            font-weight: 900;
            color: var(--accent);
            text-shadow: 3px 3px 0 #000, 6px 6px 0 rgba(255, 0, 0, 0.3);
            letter-spacing: 2px;
            text-transform: uppercase;
            transform: skew(-5deg);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: var(--text);
            text-decoration: none;
            font-size: 1.2rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            padding: 0.5rem 1rem;
            border: 2px solid transparent;
            transition: all 0.3s ease;
            background: rgba(255, 0, 0, 0.1);
        }

        .nav-links a:hover {
            border: 2px solid var(--accent);
            background: rgba(255, 0, 0, 0.2);
            transform: skew(-5deg) scale(1.1);
        }

        /* Герой секция */
        .hero {
            height: 100vh;
            background: 
                linear-gradient(45deg, rgba(10, 10, 10, 0.9), rgba(26, 26, 26, 0.8)),
                url('https://images.unsplash.com/photo-1514525253161-7a46d19cd819?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 0 2rem;
            margin-top: 80px;
            position: relative;
        }

        .hero::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><rect fill="none" stroke="%23ff0000" stroke-width="0.5" x="0" y="0" width="100" height="100"/></svg>');
            opacity: 0.1;
            pointer-events: none;
        }

        .hero-content h1 {
            font-size: 5rem;
            font-weight: 900;
            margin-bottom: 1rem;
            color: var(--accent);
            text-shadow: 4px 4px 0 #000, 8px 8px 0 rgba(255, 0, 0, 0.3);
            text-transform: uppercase;
            letter-spacing: 3px;
            transform: skew(-3deg);
        }

        .hero-content .subtitle {
            font-size: 1.5rem;
            color: var(--text);
            margin-bottom: 3rem;
            text-transform: uppercase;
            letter-spacing: 4px;
            background: rgba(0, 0, 0, 0.7);
            padding: 1rem 2rem;
            display: inline-block;
            border: 2px solid var(--accent);
        }

        /* Альбомы */
        .albums {
            padding: 6rem 2rem;
            background: var(--secondary);
            border-top: 5px solid var(--accent);
            border-bottom: 5px solid var(--accent);
        }

        .section-title {
            text-align: center;
            margin-bottom: 4rem;
            font-size: 3rem;
            color: var(--accent);
            text-transform: uppercase;
            letter-spacing: 3px;
            text-shadow: 2px 2px 0 #000;
            transform: skew(-3deg);
        }

        .albums-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .album-card {
            background: rgba(0, 0, 0, 0.8);
            border: 3px solid var(--accent);
            padding: 2rem;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .album-card::before {
            content: "";
            position: absolute;
            top: -10px;
            left: -10px;
            right: -10px;
            bottom: -10px;
            border: 1px solid var(--accent-glow);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .album-card:hover {
            transform: translateY(-10px) skew(-2deg);
            box-shadow: 0 20px 40px rgba(255, 0, 0, 0.3);
        }

        .album-card:hover::before {
            opacity: 1;
        }

        .album-cover {
            width: 200px;
            height: 200px;
            object-fit: cover;
            margin-bottom: 1.5rem;
            border: 3px solid #000;
            box-shadow: 5px 5px 0 var(--accent);
        }

        .album-title {
            font-size: 1.8rem;
            font-weight: 900;
            margin-bottom: 0.5rem;
            color: var(--text);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .album-year {
            color: var(--text-secondary);
            font-size: 1rem;
            margin-bottom: 1.5rem;
            font-family: 'Courier New', monospace;
        }

        .listen-button {
            display: inline-block;
            padding: 12px 30px;
            background: var(--accent);
            color: #000;
            text-decoration: none;
            border: 2px solid #000;
            font-weight: 900;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            font-size: 1.1rem;
        }

        .listen-button:hover {
            background: #000;
            color: var(--accent);
            border: 2px solid var(--accent);
            transform: scale(1.1);
        }

        /* О группе */
        .about {
            padding: 6rem 2rem;
            background: var(--primary);
        }

        .about-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
            font-size: 1.3rem;
            line-height: 1.8;
            color: var(--text);
            background: rgba(0, 0, 0, 0.7);
            padding: 3rem;
            border: 2px solid var(--accent);
            position: relative;
        }

        .about-content::before {
            content: "⚡";
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--primary);
            padding: 0 1rem;
            font-size: 2rem;
        }

        /* Футер */
        footer {
            background: var(--secondary);
            border-top: 3px solid var(--accent);
            padding: 3rem 2rem;
            text-align: center;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 2rem;
        }

        .social-links a {
            color: var(--accent);
            font-size: 1.5rem;
            text-decoration: none;
            padding: 10px;
            border: 2px solid var(--accent);
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
            background: #000;
        }

        .social-links a:hover {
            background: var(--accent);
            color: #000;
            transform: rotate(10deg) scale(1.2);
        }

        /* Адаптивность */
        @media (max-width: 768px) {
            .nav-links {
                flex-direction: column;
                gap: 1rem;
            }

            .hero-content h1 {
                font-size: 3rem;
            }

            .album-cover {
                width: 150px;
                height: 150px;
            }

            .section-title {
                font-size: 2rem;
            }
        }

        /* Анимации */
        @keyframes glitch {
            0% { transform: translate(0); }
            20% { transform: translate(-2px, 2px); }
            40% { transform: translate(-2px, -2px); }
            60% { transform: translate(2px, 2px); }
            80% { transform: translate(2px, -2px); }
            100% { transform: translate(0); }
        }

        .glitch:hover {
            animation: glitch 0.3s infinite;
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Хедер -->
    <header>
        <nav class="nav-container">
            <div class="logo glitch">CANCER HAMMERS</div>
            <ul class="nav-links">
                <li><a href="#home">Главная</a></li>
                <li><a href="#albums">Альбомы</a></li>
                <li><a href="#about">О нас</a></li>
                <li><a href="#contact">Контакты</a></li>
            </ul>
        </nav>
    </header>

    <!-- Герой секция -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1 class="glitch">CANCER HAMMERS</h1>
            <div class="subtitle">ГРОМ, СТАЛЬ И ПАНК-РОК</div>
        </div>
    </section>

    <!-- Альбомы -->
    <section id="albums" class="albums">
        <h2 class="section-title glitch">НАШИ АЛЬБОМЫ</h2>
        <div class="albums-grid">
            <div class="album-card">
                <img src="https://i.imgur.com/ob8W8rA.png" alt="Self-Portrait" class="album-cover">
                <h3 class="album-title">SELF-PORTRAIT</h3>
                <p class="album-year">2024 • 8 ТРЕКОВ</p>
                <a href="https://music.yandex.ru/album/38708892" class="listen-button">СЛУШАТЬ</a>
            </div>
            <div class="album-card">
                <img src="https://i.imgur.com/V1cY3bG.png" alt="Гаустный Молот" class="album-cover">
                <h3 class="album-title">ГАУСТНЫЙ МОЛОТ</h3>
                <p class="album-year">2024 • 7 ТРЕКОВ</p>
                <a href="https://music.yandex.ru/album/38461870" class="listen-button">СЛУШАТЬ</a>
            </div>
        </div>
    </section>

    <!-- О группе -->
    <section id="about" class="about">
        <h2 class="section-title glitch">О CANCER HAMMERS</h2>
        <div class="about-content">
            <p>Мы - Cancer Hammers. Родились в гараже, выросли на сцене. Наша музыка - это крик души, закованный в сталь гитарных рифов и ударных.</p>
            <p>Более 100 концертов, 3 студийных альбома и море выпитого пива. Присоединяйся к нашему безумию!</p>
        </div>
    </section>

    <!-- Футер -->
    <footer id="contact">
        <div class="social-links">
            <a href="#" class="glitch">VT</a>
            <a href="#" class="glitch">IC</a>
            <a href="#" class="glitch">SP</a>
            <a href="#" class="glitch">TG</a>
        </div>
        <p>© 2024 CANCER HAMMERS. ВСЕ ПРАВА ЗАЩИЩЕНЫ. ИЛИ НЕТ.</p>
        <p style="color: var(--text-secondary); margin-top: 1rem;">hookings@cancerhammers.com | +7 (666) 666-13-13</p>
    </footer>

    <script>
        // Плавная прокрутка
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Глитч эффект при наведении
        document.querySelectorAll('.glitch').forEach(element => {
            element.addEventListener('mouseenter', function() {
                this.style.animation = 'glitch 0.3s infinite';
            });
            element.addEventListener('mouseleave', function() {
                this.style.animation = 'none';
            });
        });

        // Случайные смещения для панк-эффекта
        document.querySelectorAll('.album-card, .nav-links a').forEach(element => {
            const randomRotate = (Math.random() - 0.5) * 2;
            element.style.transform = `rotate(${randomRotate}deg)`;
        });
    </script>
</body>
</html>
