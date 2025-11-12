<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Политика Безопасности - CANCER HAMMERS</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Courier New', monospace;
        }

        body {
            background: #000;
            color: #0f0;
            background-image: 
                radial-gradient(circle at 20% 30%, rgba(0, 255, 0, 0.05) 0%, transparent 20%),
                radial-gradient(circle at 80% 70%, rgba(0, 255, 0, 0.05) 0%, transparent 20%);
            overflow-x: hidden;
        }

        /* Matrix эффект */
        .matrix-bg {
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
                    rgba(0, 255, 0, 0.03) 2px,
                    rgba(0, 255, 0, 0.03) 4px
                );
            pointer-events: none;
            z-index: -1;
        }

        /* Хедер в стиле хакера */
        header {
            background: #001100;
            border-bottom: 3px solid #0f0;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 100;
            box-shadow: 0 0 30px rgba(0, 255, 0, 0.3);
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
            font-weight: bold;
            color: #0f0;
            text-shadow: 0 0 10px #0f0;
            letter-spacing: 3px;
            text-transform: uppercase;
            font-family: 'Courier New', monospace;
        }

        /* Главный контейнер */
        .security-container {
            max-width: 1000px;
            margin: 120px auto 50px;
            padding: 2rem;
            background: rgba(0, 20, 0, 0.8);
            border: 2px solid #0f0;
            box-shadow: 0 0 50px rgba(0, 255, 0, 0.2);
            position: relative;
        }

        /* Мигающий бордер */
        .security-container::before {
            content: "";
            position: absolute;
            top: -4px;
            left: -4px;
            right: -4px;
            bottom: -4px;
            border: 1px solid #0f0;
            animation: pulse 2s infinite;
            pointer-events: none;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.3; }
        }

        .security-header {
            text-align: center;
            margin-bottom: 3rem;
            border-bottom: 1px solid #0f0;
            padding-bottom: 1rem;
        }

        .security-header h1 {
            font-size: 2.5rem;
            color: #0f0;
            text-shadow: 0 0 15px #0f0;
            margin-bottom: 1rem;
            text-transform: uppercase;
        }

        .security-level {
            background: #002200;
            padding: 0.5rem 1rem;
            border: 1px solid #0f0;
            display: inline-block;
            margin: 1rem 0;
            animation: blink 1s infinite;
        }

        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }

        /* Секции политики */
        .policy-section {
            margin-bottom: 3rem;
            padding: 1.5rem;
            background: rgba(0, 30, 0, 0.5);
            border-left: 3px solid #0f0;
        }

        .policy-section h2 {
            color: #0f0;
            margin-bottom: 1rem;
            font-size: 1.5rem;
            text-transform: uppercase;
        }

        .policy-section p {
            line-height: 1.6;
            margin-bottom: 1rem;
            color: #afa;
        }

        .feature-list {
            list-style: none;
            padding-left: 1rem;
        }

        .feature-list li {
            margin-bottom: 0.8rem;
            position: relative;
            padding-left: 2rem;
            color: #8f8;
        }

        .feature-list li::before {
            content: ">";
            position: absolute;
            left: 0;
            color: #0f0;
            font-weight: bold;
        }

        /* Шифрование индикатор */
        .encryption-status {
            background: #001100;
            padding: 2rem;
            text-align: center;
            border: 1px solid #0f0;
            margin: 2rem 0;
            position: relative;
        }

        .encryption-indicator {
            display: inline-block;
            padding: 0.5rem 1rem;
            background: #003300;
            border: 1px solid #0f0;
            animation: encrypt 3s infinite;
        }

        @keyframes encrypt {
            0% { color: #0f0; }
            50% { color: #0a0; }
            100% { color: #0f0; }
        }

        /* Предупреждения */
        .warning {
            background: #330000;
            border: 1px solid #f00;
            padding: 1rem;
            margin: 1rem 0;
            color: #f88;
        }

        .warning h3 {
            color: #f00;
            margin-bottom: 0.5rem;
        }

        /* Футер */
        footer {
            background: #001100;
            border-top: 3px solid #0f0;
            padding: 2rem;
            text-align: center;
            margin-top: 3rem;
        }

        .access-log {
            font-size: 0.9rem;
            color: #0a0;
            margin-top: 1rem;
        }

        /* Терминал эффект */
        .terminal {
            background: #000;
            border: 1px solid #0f0;
            padding: 1rem;
            margin: 1rem 0;
            font-family: 'Courier New', monospace;
            color: #0f0;
        }

        .command {
            color: #0ff;
        }

        .response {
            color: #0f0;
            margin-left: 1rem;
        }

        /* Адаптивность */
        @media (max-width: 768px) {
            .security-container {
                margin: 100px 1rem 2rem;
                padding: 1rem;
            }
            
            .security-header h1 {
                font-size: 1.8rem;
            }
        }

        /* Сканирующая линия */
        .scan-line {
            position: fixed;
            left: 0;
            right: 0;
            height: 2px;
            background: linear-gradient(90deg, transparent, #0f0, transparent);
            animation: scan 3s linear infinite;
            pointer-events: none;
            z-index: 999;
        }

        @keyframes scan {
            0% { top: 0; }
            100% { top: 100%; }
        }
    </style>
</head>
<body>
    <!-- Сканирующая линия -->
    <div class="scan-line"></div>
    
    <!-- Matrix фон -->
    <div class="matrix-bg"></div>

    <!-- Хедер -->
    <header>
        <nav class="nav-container">
            <div class="logo">CANCER HAMMERS SECURITY</div>
        </nav>
    </header>

    <!-- Основной контент -->
    <div class="security-container">
        <div class="security-header">
            <h1>ПОЛИТИКА БЕЗОПАСНОСТИ</h1>
            <div class="security-level">УРОВЕНЬ ДОСТУПА: ОМЕГА-ЧЕРНЫЙ</div>
            <div class="encryption-indicator">ШИФРОВАНИЕ AES-512 АКТИВНО</div>
        </div>

        <!-- Терминал -->
        <div class="terminal">
            <div><span class="command">$ whoami</span></div>
            <div class="response">> АНОНИМНЫЙ ПОЛЬЗОВАТЕЛЬ</div>
            <div><span class="command">$ security_status --check</span></div>
            <div class="response">> СИСТЕМА ЗАЩИЩЕНА | ТРАФИК ЗАШИФРОВАН | ЛОГИ УНИЧТОЖЕНЫ</div>
        </div>

        <!-- Секция 1 -->
        <div class="policy-section">
            <h2>🔒 АНОНИМНОСТЬ И ЗАЩИТА ДАННЫХ</h2>
            <p>Мы не существуем. Вы не существуете. Данные не существуют.</p>
            
            <ul class="feature-list">
                <li>Zero-knowledge архитектура - мы ничего не знаем о вас</li>
                <li>Сквозное шифрование военного уровня</li>
                <li>Автоматическое удаление логов каждые 24 часа</li>
                <li>Tor-маршрутизация всех подключений</li>
                <li>Фальшивые DNS-запросы для маскировки трафика</li>
                <li>Динамические IP-адреса с ротацией каждые 5 минут</li>
                <li>Шифрование метаданных пакетов</li>
            </ul>
        </div>

        <!-- Секция 2 -->
        <div class="policy-section">
            <h2>🛡️ ЗАЩИТА ОТ ВТОРЖЕНИЙ</h2>
            <p>Наша система безопасности отражает 99.99% атак автоматически.</p>
            
            <ul class="feature-list">
                <li>Многоуровневая система обнаружения вторжений</li>
                <li>Behavioral analysis всех подключений</li>
                <li>Автоматические honeypot-ловушки для хакеров</li>
                <li>Защита от DDoS через распределенную сеть узлов</li>
                <li>Ежеминутное обновление сигнатур угроз</li>
                <li>Квантово-устойчивые алгоритмы шифрования</li>
                <li>Физическая изоляция серверов в подземных бункерах</li>
            </ul>
        </div>

        <!-- Секция 3 -->
        <div class="policy-section">
            <h2>🌐 ПРИВАТНОСТЬ ВЕБ-СЕРФИНГА</h2>
            <p>Ваши цифровые следы стираются быстрее, чем появляются.</p>
            
            <ul class="feature-list">
                <li>Автоматическая очистка cookies после сессии</li>
                <li>Блокировка всех трекеров и fingerprint-скриптов</li>
                <li>VPN-over-Tor технология</li>
                <li>Динамическая подмена user-agent</li>
                <li>Шифрование DNS-запросов через DNSCrypt</li>
                <li>Защита от canvas fingerprinting</li>
                <li>Случайная задержка запросов для предотвращения анализа</li>
            </ul>
        </div>

        <!-- Секция 4 -->
        <div class="policy-section">
            <h2>🚨 АВАРИЙНЫЕ ПРОТОКОЛЫ</h2>
            <p>В случае компрометации - система самоуничтожается.</p>
            
            <ul class="feature-list">
                <li>Dead man's switch - активация при отсутствии сигнала</li>
                <li>Cryptographic erase всех данных при нарушении целостности</li>
                <li>Автоматическое перераспределение на backup-локации</li>
                <li>Физическое уничтожение носителей при попытке вскрытия</li>
                <li>Распределенное хранение с порогом Шамира</li>
                <li>Ежедневные пентесты автоматизированными системами</li>
            </ul>
        </div>

        <!-- Статус шифрования -->
        <div class="encryption-status">
            <div class="encryption-indicator">🚀 СИСТЕМА БЕЗОПАСНОСТИ АКТИВНА</div>
            <div style="margin-top: 1rem; font-size: 0.9rem;">
                ТРАФИК ЗАШИФРОВАН | АНОНИМИЗАЦИЯ РАБОТАЕТ | ЛОГИ ОЧИЩЕНЫ
            </div>
        </div>

        <!-- Предупреждение -->
        <div class="warning">
            <h3>⚠️ ВНИМАНИЕ: СИСТЕМА САМОЗАЩИТЫ АКТИВНА</h3>
            <p>Любая попытка взлома будет отслежена и заблокирована. Все действия логируются (но потом удаляются).</p>
        </div>

        <!-- Футер -->
        <footer>
            <div>CANCER HAMMERS SECURITY PROTOCOL v4.2</div>
            <div class="access-log">
                Последний доступ: [СКРЫТО] | IP: [СКРЫТО] | Локация: [СКРЫТО]
            </div>
        </footer>
    </div>

    <script>
        // Эффект печатающегося текста
        document.addEventListener('DOMContentLoaded', function() {
            const terminal = document.querySelector('.terminal');
            const commands = terminal.querySelectorAll('.command');
            
            commands.forEach((command, index) => {
                const text = command.textContent;
                command.textContent = '';
                
                setTimeout(() => {
                    let i = 0;
                    const typeWriter = setInterval(() => {
                        if (i < text.length) {
                            command.textContent += text.charAt(i);
                            i++;
                        } else {
                            clearInterval(typeWriter);
                        }
                    }, 50);
                }, index * 1000);
            });
        });

        // Случайные сообщения безопасности
        const securityMessages = [
            "Проверка целостности системы... ОК",
            "Сканирование на уязвимости... ЧИСТО", 
            "Мониторинг сетевой активности... НОРМА",
            "Проверка шифрования... AES-512 АКТИВЕН",
            "Анализ трафика... АНОНИМЕН",
            "Проверка брандмауэра... АКТИВЕН",
            "Сканирование на malware... ОТСУТСТВУЕТ"
        ];

        setInterval(() => {
            const status = document.querySelector('.encryption-status div:last-child');
            const randomMessage = securityMessages[Math.floor(Math.random() * securityMessages.length)];
            status.textContent = `🔍 ${randomMessage}`;
        }, 5000);

        // Эффект мигающего курсора
        const cursor = document.createElement('span');
        cursor.textContent = '_';
        cursor.style.animation = 'blink 1s infinite';
        document.querySelector('.terminal').appendChild(cursor);

        // Защита от копирования (шутка)
        document.addEventListener('copy', (e) => {
            e.clipboardData.setData('text/plain', '🚫 КОПИРОВАНИЕ ЗАПРЕЩЕНО СИСТЕМОЙ БЕЗОПАСНОСТИ 🚫');
            e.preventDefault();
        });
    </script>
</body>
</html>
