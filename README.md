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
            font-family: 'Impact', 'Arial Black', sans-serif;
        }

        body {
            background: #000;
            color: #fff;
            background-image: 
                radial-gradient(circle at 10% 20%, rgba(255, 0, 0, 0.1) 0%, transparent 20%),
                radial-gradient(circle at 90% 80%, rgba(139, 0, 0, 0.1) 0%, transparent 20%);
            overflow-x: hidden;
        }

        /* Грязные текстуры */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                repeating-linear-gradient(
                    45deg,
                    transparent,
                    transparent 2px,
                    rgba(255, 0, 0, 0.03) 2px,
                    rgba(255, 0, 0, 0.03) 4px
                );
            pointer-events: none;
            z-index: 1000;
        }

        /* Header - Грязный и агрессивный */
        header {
            background: linear-gradient(135deg, #2a0000 0%, #000 50%, #2a0000 100%);
            border-bottom: 3px solid #8b0000;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 20px rgba(139, 0, 0, 0.5);
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
            font-size: 2rem;
            font-weight: bold;
            color: #ff0000;
            text-shadow: 2px 2px 0 #000, 4px 4px 0 #8b0000;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        .logo span {
            color: #fff;
            text-shadow: 2px 2px 0 #8b0000;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: #fff;
            text-decoration: none;
            font-size: 1.1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            padding: 0.5rem 1rem;
            border: 2px solid transparent;
            transition: all 0.3s ease;
            background: rgba(139, 0, 0, 0.3);
        }

        .nav-links a:hover {
            border: 2px solid #ff0000;
            background: rgba(255, 0, 0, 0.2);
            transform: skew(-5deg);
        }

        /* Hero Section - Мотоцикл и все дела */
        .hero {
            height: 100vh;
            background: 
                linear-gradient(rgba(0, 0, 0, 0.7), rgba(139, 0, 0, 0.3)),
                url('https://images.unsplash.com/photo-1558618666-fcd25856cd63?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            margin-top: 80px;
        }

        .hero-content h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            color: #ff0000;
            text-shadow: 3px 3px 0 #000, 6px 6px 0 #8b0000;
            text-transform: uppercase;
            letter-spacing: 4px;
        }

        .hero-content .subtitle {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            color: #fff;
            text-shadow: 2px 2px 0 #000;
        }

        .cta-button {
            display: inline-block;
            padding: 15px 40px;
            background: #ff0000;
            color: #000;
            text-decoration: none;
            border: 3px solid #000;
            border-radius: 0;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 2px;
            transition: all 0.3s ease;
            font-size: 1.2rem;
            box-shadow: 5px 5px 0 #000;
        }

        .cta-button:hover {
            background: #000;
            color: #ff0000;
            border: 3px solid #ff0000;
            transform: translate(3px, 3px);
            box-shadow: 2px 2px 0 #000;
        }

        /* Концерты */
        .concerts {
            padding: 5rem 2rem;
            background: #111;
            border-top: 5px solid #8b0000;
            border-bottom: 5px solid #8b0000;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2.5rem;
            color: #ff0000;
            text-transform: uppercase;
            letter-spacing: 3px;
            text-shadow: 2px 2px 0 #000;
        }

        .concerts-grid {
            max-width: 800px;
            margin: 0 auto;
        }

        .concert-item {
            background: #1a0000;
            border: 2px solid #8b0000;
            padding: 2rem;
            margin-bottom: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.3s ease;
        }

        .concert-item:hover {
            background: #2a0000;
            border: 2px solid #ff0000;
            transform: scale(1.02);
        }

        .concert-info h3 {
            color: #fff;
            margin-bottom: 0.5rem;
            font-size: 1.3rem;
        }

        .concert-info p {
            color: #ccc;
        }

        .buy-button {
            padding: 10px 25px;
            background: #ff0000;
            color: #000;
            text-decoration: none;
            border: 2px solid #000;
            font-weight: bold;
            text-transform: uppercase;
            transition: all 0.3s ease;
        }

        .buy-button:hover {
            background: #000;
            color: #ff0000;
            border: 2px solid #ff0000;
        }

        /* О группе */
        .about {
            padding: 5rem 2rem;
            background: #000;
        }

        .about-content {
            max-width: 1000px;
            margin: 0 auto;
            text-align: center;
            font-size: 1.2rem;
            line-height: 1.8;
            color: #ccc;
        }

        /* Музыка */
        .music {
            padding: 5rem 2rem;
            background: #111;
        }

        .music-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            max-width: 1000px;
            margin: 0 auto;
        }

        .album {
            background: #1a0000;
            border: 2px solid #8b0000;
            padding: 2rem;
            text-align: center;
        }

        .album img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border: 3px solid #000;
            margin-bottom: 1rem;
        }

        /* Футер */
        footer {
            background: #000;
            border-top: 3px solid #8b0000;
            padding: 3rem 2rem;
            text-align: center;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .social-links a {
            color: #ff0000;
            font-size: 1.5rem;
            text-decoration: none;
            padding: 10px;
            border: 2px solid #ff0000;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: #ff0000;
            color: #000;
            transform: rotate(10deg);
        }

        /* Адаптивность */
        @media (max-width: 768px) {
            .nav-links {
                flex-direction: column;
                gap: 1rem;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .concert-item {
                flex-direction: column;
                text-align: center;
                gap: 1rem;
            }

            .social-links {
                flex-wrap: wrap;
            }
        }

        /* Эффект "потертости" */
        .grunge-border {
            border: 1px solid #8b0000;
            position: relative;
        }

        .grunge-border::before {
            content: "";
            position: absolute;
            top: -5px;
            left: -5px;
            right: -5px;
            bottom: -5px;
            border: 1px solid #ff0000;
            opacity: 0.3;
            pointer-events: none;
        }
    </style>
</head>
<body>
    <!-- Хедер -->
    <header>
        <nav class="nav-container">
            <div class="logo">CANCER <span>HAMMERS</span></div>
            <ul class="nav-links">
                <li><a href="#home">Главная</a></li>
                <li><a href="#concerts">Концерты</a></li>
                <li><a href="#music">Музыка</a></li>
                <li><a href="#about">О нас</a></li>
                <li><a href="#contact">Контакты</a></li>
            </ul>
        </nav>
    </header>

    <!-- Герой с мотоциклом -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Cancer Hammers</h1>
            <div class="subtitle">ГРОМ, СТАЛЬ И ПАНК-РОК</div>
            <a href="#concerts" class="cta-button">Билеты на концерты</a>
        </div>
    </section>

    <!-- Концерты -->
    <section id="concerts" class="concerts">
        <h2 class="section-title">Ближайшие концерты</h2>
        <div class="concerts-grid">
            <div class="concert-item grunge-border">
                <div class="concert-info">
                    <h3>Москва | 15.12.2024</h3>
                    <p>Клуб "Гараж" | 20:00</p>
                </div>
                <a href="#" class="buy-button">Купить билет</a>
            </div>
            <div class="concert-item grunge-border">
                <div class="concert-info">
                    <h3>Санкт-Петербург | 20.12.2024</h3>
                    <p>Арена "Металл" | 19:30</p>
                </div>
                <a href="#" class="buy-button">Купить билет</a>
            </div>
            <div class="concert-item grunge-border">
                <div class="concert-info">
                    <h3>Екатеринбург | 25.12.2024</h3>
                    <p>Бар "Отвертка" | 21:00</p>
                </div>
                <a href="#" class="buy-button">Купить билет</a>
            </div>
        </div>
    </section>

    <!-- О группе -->
    <section id="about" class="about">
        <h2 class="section-title">О Cancer Hammers</h2>
        <div class="about-content">
            <p>Мы - Cancer Hammers. Родились в гараже, выросли на сцене. Наша музыка - это крик души, закованный в сталь гитарных рифов и ударных.</p>
            <p>Более 100 концертов, 3 студийных альбома и море выпитого пива. Присоединяйся к нашему безумию!</p>
        </div>
    </section>

    <!-- Музыка -->
    <section id="music" class="music">
        <h2 class="section-title">Наша музыка</h2>
        <div class="music-grid">
            <div class="album grunge-border">
                <img src="https://images.unsplash.com/photo-1493225457124-a3eb161ffa5f?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Альбом 1">
                <h3>Steel Revolution</h3>
                <p>2023 | 12 треков</p>
            </div>
            <div class="album grunge-border">
                <img src="https://images.unsplash.com/photo-1470225620780-dba8ba36b745?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Альбом 2">
                <h3>Garage Demons</h3>
                <p>2022 | 10 треков</p>
            </div>
            <div class="album grunge-border">
                <img src="https://images.unsplash.com/photo-1571330735066-03aaa9429d89?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Альбом 3">
                <h3>Rust & Blood</h3>
                <p>2021 | 8 треков</p>
            </div>
        </div>
    </section>

    <!-- Футер -->
    <footer id="contact">
        <div class="social-links">
            <a href="#">YT</a>
            <a href="#">IG</a>
            <a href="#">SP</a>
            <a href="#">TG</a>
        </div>
        <p>© 2024 CANCER HAMMERS. ВСЕ ПРАВА ЗАЩИЩЕНЫ. ИЛИ НЕТ.</p>
        <p>booking@cancerhammers.com | +7 (666) 666-13-13</p>
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
                header.style.background = 'rgba(42, 0, 0, 0.95)';
            } else {
                header.style.background = 'linear-gradient(135deg, #2a0000 0%, #000 50%, #2a0000 100%)';
            }
        });

        // Случайные эффекты для кнопок
        document.querySelectorAll('.buy-button, .cta-button').forEach(button => {
            button.addEventListener('mouseenter', function() {
                this.style.transform = 'skew(-5deg) scale(1.05)';
            });
            
            button.addEventListener('mouseleave', function() {
                this.style.transform = '';
            });
        });
    </script>
</body>
</html>
