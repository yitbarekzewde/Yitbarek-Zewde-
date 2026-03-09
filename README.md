<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ethiopian Beauty | የኢትዮጵያ ውበት</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            overflow-x: hidden;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
        }

        /* Ethiopian Flag Colors */
        :root {
            --ethiopian-green: #078930;
            --ethiopian-yellow: #FCDD09;
            --ethiopian-red: #DA121A;
        }

        /* Animated Background */
        .animated-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.1;
        }

        .flag-stripe {
            position: absolute;
            width: 100%;
            height: 33.33vh;
            animation: wave 8s ease-in-out infinite;
        }

        .stripe-green {
            background: var(--ethiopian-green);
            top: 0;
            animation-delay: 0s;
        }

        .stripe-yellow {
            background: var(--ethiopian-yellow);
            top: 33.33vh;
            animation-delay: 0.3s;
        }

        .stripe-red {
            background: var(--ethiopian-red);
            top: 66.66vh;
            animation-delay: 0.6s;
        }

        @keyframes wave {
            0%, 100% { transform: scaleX(1); }
            50% { transform: scaleX(1.05); }
        }

        /* Main Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 1;
        }

        /* Header with Animation */
        .header {
            text-align: center;
            padding: 50px 20px;
            animation: fadeInDown 1.5s ease;
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .logo {
            width: 120px;
            height: 120px;
            margin: 0 auto 20px;
            background: linear-gradient(135deg, var(--ethiopian-green), var(--ethiopian-yellow), var(--ethiopian-red));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            animation: rotate 10s linear infinite, pulse 2s ease-in-out infinite;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1) rotate(0deg); }
            50% { transform: scale(1.05) rotate(180deg); }
        }

        .logo-inner {
            width: 100px;
            height: 100px;
            background: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 40px;
            animation: reverse-rotate 10s linear infinite;
        }

        @keyframes reverse-rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(-360deg); }
        }

        h1 {
            font-size: 3.5rem;
            margin: 20px 0;
            background: linear-gradient(45deg, var(--ethiopian-green), var(--ethiopian-yellow), var(--ethiopian-red));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: shimmer 3s infinite;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }

        @keyframes shimmer {
            0%, 100% { filter: brightness(1); }
            50% { filter: brightness(1.2); }
        }

        .subtitle {
            font-size: 1.3rem;
            color: #333;
            animation: slideIn 1.5s ease;
            opacity: 0.8;
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(-100px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        /* Flag Cards Section */
        .flag-cards {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 60px 0;
            flex-wrap: wrap;
        }

        .card {
            width: 200px;
            height: 300px;
            perspective: 1000px;
            cursor: pointer;
        }

        .card-inner {
            position: relative;
            width: 100%;
            height: 100%;
            text-align: center;
            transition: transform 0.8s;
            transform-style: preserve-3d;
            animation: float 3s ease-in-out infinite;
        }

        .card:hover .card-inner {
            transform: rotateY(180deg);
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .card-front, .card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            border-radius: 15px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.2);
        }

        .card-front {
            background: linear-gradient(135deg, var(--ethiopian-green), var(--ethiopian-yellow), var(--ethiopian-red));
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            font-weight: bold;
            font-size: 1.5rem;
        }

        .card-back {
            background: white;
            color: #333;
            transform: rotateY(180deg);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .card-back h3 {
            color: var(--ethiopian-red);
            margin-bottom: 10px;
        }

        .card-back p {
            font-size: 0.9rem;
            line-height: 1.6;
        }

        /* Animated Stripes Section */
        .stripes-showcase {
            margin: 80px 0;
            text-align: center;
        }

        .stripes-container {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin: 30px 0;
        }

        .animated-stripe {
            width: 100px;
            height: 200px;
            background: var(--ethiopian-green);
            animation: stripeAnimation 2s ease-in-out infinite;
            border-radius: 10px;
        }

        .animated-stripe:nth-child(2) {
            background: var(--ethiopian-yellow);
            animation-delay: 0.3s;
        }

        .animated-stripe:nth-child(3) {
            background: var(--ethiopian-red);
            animation-delay: 0.6s;
        }

        @keyframes stripeAnimation {
            0%, 100% { 
                transform: scaleY(1);
                border-radius: 10px;
            }
            50% { 
                transform: scaleY(1.5);
                border-radius: 30px;
                box-shadow: 0 0 30px currentColor;
            }
        }

        /* Ethiopian Pattern */
        .pattern-section {
            margin: 80px 0;
            padding: 40px;
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
        }

        .ethiopian-pattern {
            display: flex;
            justify-content: center;
            gap: 5px;
            margin: 30px 0;
        }

        .pattern-dot {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            animation: bounce 1s ease-in-out infinite;
        }

        .pattern-dot.green { background: var(--ethiopian-green); animation-delay: 0s; }
        .pattern-dot.yellow { background: var(--ethiopian-yellow); animation-delay: 0.2s; }
        .pattern-dot.red { background: var(--ethiopian-red); animation-delay: 0.4s; }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-30px); }
        }

        /* Timeline Section */
        .timeline {
            margin: 80px 0;
            position: relative;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 4px;
            height: 100%;
            background: linear-gradient(to bottom, var(--ethiopian-green), var(--ethiopian-yellow), var(--ethiopian-red));
            animation: glow 2s ease-in-out infinite;
        }

        @keyframes glow {
            0%, 100% { opacity: 0.5; }
            50% { opacity: 1; }
        }

        .timeline-item {
            display: flex;
            justify-content: space-between;
            margin: 40px 0;
            position: relative;
        }

        .timeline-content {
            width: 45%;
            padding: 20px;
            background: rgba(255,255,255,0.9);
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            animation: slideInLeft 1s ease;
            border-left: 5px solid var(--ethiopian-green);
        }

        .timeline-item:nth-child(even) .timeline-content {
            border-left: 5px solid var(--ethiopian-red);
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 40px;
            margin-top: 60px;
            background: linear-gradient(135deg, var(--ethiopian-green), var(--ethiopian-yellow), var(--ethiopian-red));
            border-radius: 20px 20px 0 0;
            color: white;
            animation: gradientShift 5s ease infinite;
        }

        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .footer h3 {
            font-size: 2rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }

        .social-icon {
            width: 50px;
            height: 50px;
            background: rgba(255,255,255,0.2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            cursor: pointer;
            transition: all 0.3s;
            animation: socialPulse 2s ease-in-out infinite;
        }

        .social-icon:hover {
            transform: scale(1.2);
            background: white;
            color: var(--ethiopian-red);
        }

        @keyframes socialPulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            .timeline::before {
                left: 30px;
            }
            
            .timeline-item {
                flex-direction: column;
            }
            
            .timeline-content {
                width: 100%;
                margin-left: 50px;
            }
        }
    </style>
</head>
<body>
    <!-- Animated Flag Background -->
    <div class="animated-bg">
        <div class="flag-stripe stripe-green"></div>
        <div class="flag-stripe stripe-yellow"></div>
        <div class="flag-stripe stripe-red"></div>
    </div>

    <div class="container">
        <!-- Header -->
        <header class="header">
            <div class="logo">
                <div class="logo-inner"></div>
            </div>
            <h1>የኢትዮጵያ ውበት</h1>
            <h1>Beauty of Ethiopia</h1>
            <p class="subtitle">Land of Origins • የትውልድ ምድር • 13 Months of Sunshine</p>
        </header>

        <!-- Flag Cards -->
        <div class="flag-cards">
            <div class="card" style="animation-delay: 0s">
                <div class="card-inner">
                    <div class="card-front">
                        <span>💚</span>
                        <span>Green</span>
                    </div>
                    <div class="card-back">
                        <h3>Green</h3>
                        <p>ለምለም • Lush<br>Land & Fertility<br>የምድር ሀብት</p>
                    </div>
                </div>
            </div>
            
            <div class="card" style="animation-delay: 0.2s">
                <div class="card-inner">
                    <div class="card-front">
                        <span>💛</span>
                        <span>Yellow</span>
                    </div>
                    <div class="card-back">
                        <h3>Yellow</h3>
                        <p>ወርቅ • Gold<br>Peace & Hope<br>ሰላም እና ተስፋ</p>
                    </div>
                </div>
            </div>
            
            <div class="card" style="animation-delay: 0.4s">
                <div class="card-inner">
                    <div class="card-front">
                        <span>❤️</span>
                        <span>Red</span>
                    </div>
                    <div class="card-back">
                        <h3>Red</h3>
                        <p>ጀግንነት • Courage<br>Strength & Sacrifice<brጥንካሬ እና መስዋዕትነት</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Animated Stripes -->
        <div class="stripes-showcase">
            <h2 style="color: var(--ethiopian-red); margin-bottom: 30px;">The Colors of Ethiopia</h2>
            <div class="stripes-container">
                <div class="animated-stripe"></div>
                <div class="animated-stripe"></div>
                <div class="animated-stripe"></div>
            </div>
        </div>

        <!-- Ethiopian Pattern -->
        <div class="pattern-section">
            <h2 style="text-align: center; color: var(--ethiopian-green);">Traditional Pattern</h2>
            <div class="ethiopian-pattern">
                <div class="pattern-dot green"></div>
                <div class="pattern-dot yellow"></div>
                <div class="pattern-dot red"></div>
                <div class="pattern-dot green"></div>
                <div class="pattern-dot yellow"></div>
                <div class="pattern-dot red"></div>
                <div class="pattern-dot green"></div>
                <div class="pattern-dot yellow"></div>
                <div class="pattern-dot red"></div>
            </div>
        </div>

        <!-- Timeline -->
        <div class="timeline">
            <h2 style="text-align: center; margin-bottom: 40px; color: var(--ethiopian-yellow);">Ethiopian Heritage</h2>
            
            <div class="timeline-item">
                <div class="timeline-content">
                    <h3 style="color: var(--ethiopian-green);">🌍 Land of Origins</h3>
                    <p>Birthplace of mankind, home to Lucy (Dinkinesh) - 3.2 million years old</p>
                </div>
                <div class="timeline-content"></div>
            </div>
            
            <div class="timeline-item">
                <div class="timeline-content"></div>
                <div class="timeline-content">
                    <h3 style="color: var(--ethiopian-yellow);">👑 Ancient Kingdom</h3>
                    <p>One of the oldest civilizations in the world, with over 3000 years of history</p>
                </div>
            </div>
            
            <div class="timeline-item">
                <div class="timeline-content">
                    <h3 style="color: var(--ethiopian-red);">✝️ First Christian Nation</h3>
                    <p>One of the first countries to adopt Christianity as state religion in 330 AD</p>
                </div>
                <div class="timeline-content"></div>
            </div>
        </div>

        <!-- Footer -->
        <footer class="footer">
            <h3>🇪🇹 Ethiopia 🇪🇹</h3>
            <p>📅 13 Months of Sunshine • 13 ወር ፀሐይ</p>
            <p>🌅 Land of the Rising Sun • የፀሐይ መውጫ ምድር</p>
            
            <div class="social-links">
                <div class="social-icon">🇪🇹</div>
                <div class="social-icon">💚</div>
                <div class="social-icon">💛</div>
                <div class="social-icon">❤️</div>
                <div class="social-icon">☀️</div>
            </div>
            
            <p style="margin-top: 30px;">© 2024 Ethiopian Beauty | የኢትዮጵያ ውበት</p>
            <p style="font-size: 0.9rem; opacity: 0.8;">💚💛❤️ This site is developed by Yitbarek Zewde Ethiopia </p>
        </footer>
    </div>

    <!-- Floating Particles -->
    <script>
        // Add floating particles effect
        document.addEventListener('DOMContentLoaded', function() {
            const colors = ['#078930', '#FCDD09', '#DA121A'];
            
            for(let i = 0; i < 30; i++) {
                const particle = document.createElement('div');
                particle.style.position = 'fixed';
                particle.style.width = '10px';
                particle.style.height = '10px';
                particle.style.background = colors[Math.floor(Math.random() * colors.length)];
                particle.style.borderRadius = '50%';
                particle.style.pointerEvents = 'none';
                particle.style.zIndex = '0';
                particle.style.opacity = '0.3';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.animation = `floatParticle ${5 + Math.random() * 10}s linear infinite`;
                
                const style = document.createElement('style');
                style.innerHTML = `
                    @keyframes floatParticle {
                        0% {
                            transform: translate(0, 0) rotate(0deg);
                        }
                        100% {
                            transform: translate(${Math.random() * 200 - 100}px, ${Math.random() * 200 - 100}px) rotate(360deg);
                        }
                    }
                `;
                document.head.appendChild(style);
                
                document.body.appendChild(particle);
            }
        });
    </script>
</body>
</html>