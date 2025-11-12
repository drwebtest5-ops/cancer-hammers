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
            font-family: 'Segoe UI', system-ui, sans-serif;
        }

        :root {
            --primary: #1a1a1a;
            --secondary: #2a2a2a;
            --accent: #ff2a2a;
            --text: #ffffff;
            --text-secondary: #b0b0b0;
        }

        body {
            background: var(--primary);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Современный хедер */
        header {
            background: rgba(26, 26, 26, 0.95);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            padding: 1.5rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: all 0.3s ease;
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
            font-size: 1.8rem;
            font-weight: 800;
            background: linear-gradient(135deg, var(--accent), #ff6b6b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: -1px;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 3rem;
        }

        .nav-links a {
            color: var(--text);
            text-decoration: none;
            font-weight: 500;
            font-size: 1rem;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Герой секция */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, rgba(26, 26, 26, 0.9), rgba(42, 42, 42, 0.8)),
                        url('https://images.unsplash.com/photo-1514525253161-7a46d19cd819?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 0 2rem;
            margin-top: 0;
        }

        .hero-content h1 {
            font-size: 4rem;
            font-weight: 800;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #fff, var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: -2px;
        }

        .hero-content .subtitle {
            font-size: 1.3rem;
            color: var(--text-secondary);
            margin-bottom: 3rem;
            font-weight: 300;
        }

        .stream-links {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .stream-button {
            padding: 12px 30px;
            background: rgba(255, 255, 255, 0.1);
            color: var(--text);
            text-decoration: none;
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 8px;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
            font-weight: 500;
        }

        .stream-button:hover {
            background: var(--accent);
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(255, 42, 42, 0.3);
        }

        /* Альбомы */
        .albums {
            padding: 8rem 2rem;
            background: var(--secondary);
        }

        .section-title {
            text-align: center;
            margin-bottom: 4rem;
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--text);
        }

        .albums-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 3rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .album-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 16px;
            padding: 2rem;
            text-align: center;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .album-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.1);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }

        .album-cover {
            width: 250px;
            height: 250px;
            border-radius: 12px;
            object-fit: cover;
            margin-bottom: 1.5rem;
            border: 2px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }

        .album-title {
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            color: var(--text);
        }

        .album-year {
            color: var(--text-secondary);
            font-size: 1rem;
            margin-bottom: 1.5rem;
        }

        .listen-button {
            display: inline-block;
            padding: 10px 25px;
            background: var(--accent);
            color: white;
            text-decoration: none;
            border-radius: 6px;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .listen-button:hover {
            background: #ff1a1a;
            transform: scale(1.05);
        }

        /* О группе */
        .about {
            padding: 8rem 2rem;
            background: var(--primary);
        }

        .about-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
            font-size: 1.2rem;
            line-height: 1.8;
            color: var(--text-secondary);
        }

        /* Футер */
        footer {
            background: var(--secondary);
            padding: 4rem 2rem;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .social-links a {
            color: var(--text);
            font-size: 1.5rem;
            text-decoration: none;
            padding: 12px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 8px;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: var(--accent);
            transform: translateY(-3px);
        }

        /* Адаптивность */
        @media (max-width: 768px) {
            .nav-links {
                gap: 1.5rem;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .albums-grid {
                grid-template-columns: 1fr;
            }

            .album-cover {
                width: 200px;
                height: 200px;
            }
        }

        /* Анимации */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .fade-in {
            animation: fadeInUp 0.8s ease-out;
        }
    </style>
</head>
<body>
    <!-- Хедер -->
    <header>
        <nav class="nav-container">
            <div class="logo">CANCER HAMMERS</div>
            <ul class="nav-links">
                <li><a href="#home">Главная</a></li>
                <li><a href="#albums">Альбомы</a></li>
                <li><a href="#about">О группе</a></li>
                <li><a href="#contact">Контакты</a></li>
            </ul>
        </nav>
    </header>

    <!-- Герой секция -->
    <section id="home" class="hero">
        <div class="hero-content fade-in">
            <h1>CANCER HAMMERS</h1>
            <div class="subtitle">Современный русский рок с характером</div>
            <div class="stream-links">
                <a href="https://music.yandex.ru/artist/16792546" class="stream-button">Слушать в Яндекс.Музыке</a>
                <a href="#" class="stream-button">Другие платформы</a>
            </div>
        </div>
    </section>

    <!-- Альбомы -->
    <section id="albums" class="albums">
        <h2 class="section-title">Наши альбомы</h2>
        <div class="albums-grid">
            <div class="album-card fade-in">
                <img src="https://i.imgur.com/ob8W8rA.png" alt="Self-Portrait" class="album-cover">
                <h3 class="album-title">SELF-PORTRAIT</h3>
                <p class="album-year">2024 • 8 треков</p>
                <a href="https://music.yandex.ru/album/38708892" class="listen-button">Слушать</a>
            </div>
            <div class="album-card fade-in">
                <img src="https://i.imgur.com/V1cY3bG.png" alt="Гаустный Молот" class="album-cover">
                <h3 class="album-title">ГАУСТНЫЙ МОЛОТ</h3>
                <p class="album-year">2024 • 7 треков</p>
                <a href="https://music.yandex.ru/album/38461870" class="listen-button">Слушать</a>
            </div>
        </div>
    </section>

    <!-- О группе -->
    <section id="about" class="about">
        <h2 class="section-title">О Cancer Hammers</h2>
        <div class="about-content">
            <p>CANCER HAMMERS — это современная рок-группа, создающая музыку на стыке альтернативного рока и пост-хардкора. Наши треки — это искренние эмоции, мощные гитарные рифы и тексты, которые заставляют задуматься.</p>
            <p>В наших альбомах "Self-Portrait" и "Гаустный Молот" мы исследуем темы самоидентификации, человеческих отношений и вызовов современного мира.</p>
        </div>
    </section>

    <!-- Футер -->
    <footer id="contact">
        <div class="social-links">
            <a href="#">VK</a>
            <a href="#">TG</a>
            <a href="#">YT</a>
            <a href="#">IG</a>
        </div>
        <p>© 2024 CANCER HAMMERS. Все права защищены.</p>
        <p style="color: var(--text-secondary); margin-top: 1rem;">booking@cancerhammers.com</p>
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

        // Эффект при скролле для хедера
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(26, 26, 26, 0.98)';
            } else {
                header.style.background = 'rgba(26, 26, 26, 0.95)';
            }
        });

        // Анимация появления элементов
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Наблюдаем за элементами с анимацией
        document.querySelectorAll('.fade-in').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(el);
        });
    </script>
</body>
</html>
