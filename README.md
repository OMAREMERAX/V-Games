
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>V-Games - Ultimate Gaming Experience</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
            color: white;
            overflow-x: hidden;
        }
        
        /* Animated background particles */
        .bg-particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.1;
        }
        
        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: #00ffff;
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }
        
        /* Header */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(15, 15, 35, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
        }
        
        nav {
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
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: glow 2s ease-in-out infinite alternate;
        }
        
        @keyframes glow {
            from { filter: drop-shadow(0 0 10px rgba(255, 107, 107, 0.5)); }
            to { filter: drop-shadow(0 0 20px rgba(78, 205, 196, 0.5)); }
        }
        
        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            padding: 0.5rem 1rem;
            border-radius: 25px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .nav-links a:hover {
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            transform: translateY(-2px);
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero-content {
            max-width: 800px;
            z-index: 2;
            animation: fadeInUp 1s ease-out;
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1, #f9ca24);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: titleGlow 3s ease-in-out infinite;
        }
        
        @keyframes titleGlow {
            0%, 100% { filter: drop-shadow(0 0 20px rgba(255, 107, 107, 0.3)); }
            50% { filter: drop-shadow(0 0 30px rgba(78, 205, 196, 0.5)); }
        }
        
        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        .cta-button {
            display: inline-block;
            padding: 1rem 2rem;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(255, 107, 107, 0.3);
        }
        
        .cta-button::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s;
        }
        
        .cta-button:hover::before {
            left: 100%;
        }
        
        /* Games Grid */
        .games-section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .section-title {
            text-align: center;
            font-size: 3rem;
            margin-bottom: 3rem;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .games-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }
        
        .game-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 2rem;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .game-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, #ff6b6b, #4ecdc4, #45b7d1);
        }
        
        .game-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(255, 107, 107, 0.2);
        }
        
        .game-image {
            width: 80px;
            height: 80px;
            border-radius: 15px;
            margin-bottom: 1rem;
            object-fit: cover;
            border: 2px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }
        
        .game-card:hover .game-image {
            transform: scale(1.05);
            border-color: rgba(255, 107, 107, 0.5);
        }
        
        .game-title {
            font-size: 1.3rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
        }
        
        .game-rating {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }
        
        .stars {
            color: #f9ca24;
        }
        
        .rating-text {
            opacity: 0.7;
        }
        
        .install-btn {
            display: block;
            width: 100%;
            padding: 0.8rem;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            border: none;
            border-radius: 25px;
            color: white;
            font-weight: bold;
            text-decoration: none;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .install-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(255, 107, 107, 0.3);
        }
        
        /* Stats Section */
        .stats-section {
            background: rgba(255, 255, 255, 0.03);
            padding: 4rem 2rem;
            text-align: center;
        }
        
        .stats-container {
            max-width: 800px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
        }
        
        .stat-item {
            padding: 2rem;
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: countUp 2s ease-out;
        }
        
        .stat-label {
            font-size: 1.1rem;
            opacity: 0.8;
            margin-top: 0.5rem;
        }
        
        /* Footer */
        footer {
            background: rgba(15, 15, 35, 0.8);
            padding: 3rem 2rem 1rem;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-bottom: 2rem;
            flex-wrap: wrap;
        }
        
        .footer-links a {
            color: white;
            text-decoration: none;
            opacity: 0.8;
            transition: opacity 0.3s ease;
        }
        
        .footer-links a:hover {
            opacity: 1;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .nav-links {
                display: none;
            }
            
            .games-grid {
                grid-template-columns: 1fr;
            }
            
            .stats-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
    </style>

    <!-- Animated Background -->
    <div class="bg-particles" id="particles"></div>
    
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">🎮 V-Games</div>
            
        </nav>
    </header>
    

    
    <!-- Games Section -->
    <section class="games-section" id="games">
        <h2 class="section-title">Featured Games</h2>
        <div class="games-grid">
             <div class="game-card">
                <img src="https://image.winudf.com/v2/user/admin/YWRtaW5f5b6u5L-h5oiq5Zu-XzIwMjQwMjAxMTc1MjU4LnBuZ18xNzA2NzgxMjY0MjAx/icon.webp?w=320&fakeurl=1&type=.webp" alt="Hollow Knight: Silksong" class="game-image"/>
                <div class="game-title">Hollow Knight: Silksong</div>
                <div class="game-rating">
                    <span class="stars">★★★★★</span>
                    <span class="rating-text">5 (100K)</span>
                </div>
                <a href="https://lockedapp.net/cl/i/r72lkl" class="install-btn">Install Now</a>
            </div>
             <div class="game-card">
                <img src="https://image.winudf.com/v2/user/admin/YWRtaW5fMC5qZmlmXzE3MzA4ODUyNjM0NzQ/icon.webp?w=320&fakeurl=1&type=.webp" alt="Slay the Spire 2" class="game-image"/>
                <div class="game-title">Slay the Spire 2</div>
                <div class="game-rating">
                    <span class="stars">★★★★★</span>
                    <span class="rating-text">4.9 (15K)</span>
                </div>
                <a href="https://lockedapp.net/cl/i/kl1wg8" class="install-btn">Install Now</a>
            </div>
            <div class="game-card">
                <img src="https://imgs.search.brave.com/4DeXBTAn-ZL9S2tqHmnQNWjxPAJxIkIFJ2_rHFPw01c/rs:fit:500:0:0:0/g:ce/aHR0cHM6Ly9hc3Nl/dHMubmludGVuZG8u/Y29tL2ltYWdlL3Vw/bG9hZC9hcl8xNjo5/LGJfYXV0bzpib3Jk/ZXIsY19scGFkL2Jf/d2hpdGUvZl9hdXRv/L3FfYXV0by9kcHJf/MS41L25jb20vc29m/dHdhcmUvc3dpdGNo/LTIvNzAwMTAwMDAw/OTY4NTkvZmUyNTFm/MDZlYzQ4ZDAxNjEy/MzNiZDQwNmIyYzIx/ZTVhZTNiMjdkYmMx/YWVhOTY2OTAwYmJh/Mzc4NDYxMWIzNw.jpeg" alt="Madden NFL" class="game-image"/>
                <div class="game-title">Madden NFL 26</div>
                <div class="game-rating">
                    <span class="stars">★★★★★</span>
                    <span class="rating-text">4.9 (15K)</span>
                </div>
                <a href="https://lockverify.net/sl/06wn5" class="install-btn">Install Now</a>
            </div>
            
            <div class="game-card">
                <img src="https://play-lh.googleusercontent.com/sITxnGaUxYVzTDkVAjRSKM8JKehWTuseE4hF8937sWVattKHEAirl7uZw93gqad_fQg6=w240-h480-rw" alt="Stick War: Legacy" class="game-image"/>
                <div class="game-title">Stick War: Legacy</div>
                <div class="game-rating">
                    <span class="stars">★★★★★</span>
                    <span class="rating-text">4.6 (10K)</span>
                </div>
                <a href="https://lockverify.net/cl/i/5k1pr3" class="install-btn">Install Now</a>
            </div>
            
            <div class="game-card">
                <img src="https://i.pinimg.com/736x/72/21/7e/72217e2aa3c129705e8ee60eaa1f9539.jpg" alt="merge games" class="game-image"/>
                <div class="game-title">merge games-online games</div>
                <div class="game-rating">
                    <span class="stars">★★★★★</span>
                    <span class="rating-text">4.7 (11K)</span>
                </div>
                <a href="https://lockedapp.net/cl/i/dv6dmw" class="install-btn">Install Now</a>
            </div>
            
            <div class="game-card">
                <img src="https://is1-ssl.mzstatic.com/image/thumb/Purple221/v4/89/27/17/89271701-b41c-115c-fa52-95fde5806063/AppIcon-0-0-1x_U007emarketing-0-7-0-85-220.png/230x0w.webp" alt="Rise of Kingdoms" class="game-image"/>
                <div class="game-title">Rise of Kingdoms</div>
                <div class="game-rating">
                    <span class="stars">★★★★★</span>
                    <span class="rating-text">4.8 (12K)</span>
                </div>
                <a href="https://lockedapp.org/cl/i/1oewr1" class="install-btn">Install Now</a>
            </div>
            
            <div class="game-card">
                <img src="https://image.winudf.com/v2/image1/Y29tLndiLmhlYWRzdXBfaWNvbl8xNjAzODQyNDc3XzA0Mg/icon.webp?w=140&fakeurl=1&type=.webp" alt="Heads Up!" class="game-image"/>
                <div class="game-title">Heads Up!</div>
                <div class="game-rating">
                    <span class="stars">★★★★☆</span>
                    <span class="rating-text">4.5 (8K)</span>
                </div>
                <a href="https://lockverify.net/cl/i/podeml" class="install-btn">Install Now</a>
            </div>
            
            <div class="game-card">
                <img src="https://image.winudf.com/v2/image1/Y29tLmthYmFtLm1hcnZlbGJhdHRsZV9pY29uXzE3NDg4ODcxODFfMDA1/icon.webp?w=140&fakeurl=1&type=.webp" alt="Marvel Contest of Champions" class="game-image"/>
                <div class="game-title">Marvel Contest of Champions</div>
                <div class="game-rating">
                    <span class="stars">★★★★☆</span>
                    <span class="rating-text">4.3 (7K)</span>
                </div>
                <a href="https://lockedapp.org/cl/i/w6q7kv" class="install-btn">Install Now</a>
            </div>
            
            <div class="game-card">
                <img src="https://image.winudf.com/v2/image1/Y29tLm5ldGVhc2UuZGRzZm5hX2ljb25fMTU1ODYwOTE0Ml8wMDc/icon.webp?w=140&fakeurl=1&type=.webp" alt="Stick Fight: The Game" class="game-image"/>
                <div class="game-title">Stick Fight: The Game</div>
                <div class="game-rating">
                    <span class="stars">★★★★☆</span>
                    <span class="rating-text">4.4 (5K)</span>
                </div>
                <a href="https://lockedapp.net/cl/i/ex8pqk" class="install-btn">Install Now</a>
            </div>
        </div>
    </section>
    
    <!-- Stats Section -->
    <section class="stats-section">
        <div class="stats-container">
            <div class="stat-item">
                <div class="stat-number">100k+</div>
                <div class="stat-label">Downloads</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">5+</div>
                <div class="stat-label">Games</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">4.8</div>
                <div class="stat-label">Average Rating</div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-links">
                <a href="#privacy">Privacy Policy</a>
                <a href="#terms">Terms of Service</a>
                <a href="#support">Support</a>
                <a href="#about">About Us</a>
            </div>
            <p>&copy; 2025 V-Games. All rights reserved.</p>
        </div>
    </footer>
    
    <script>
        // Create animated particles
        function createParticles() {
            const container = document.getElementById('particles');
            for (let i = 0; i < 50; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 6 + 's';
                particle.style.animationDuration = (3 + Math.random() * 6) + 's';
                container.appendChild(particle);
            }
        }
        
        // Smooth scrolling for navigation links
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
        
        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(15, 15, 35, 0.98)';
            } else {
                header.style.background = 'rgba(15, 15, 35, 0.95)';
            }
        });
        
        // Install button animations
        document.querySelectorAll('.install-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                this.style.transform = 'scale(0.95)';
                setTimeout(() => {
                    this.style.transform = 'scale(1)';
                }, 150);
            });
        });
        
        // Initialize particles
        createParticles();
        
        // Add entrance animations for game cards
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
        
        // Observe game cards for animation
        document.querySelectorAll('.game-card').forEach((card, index) => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(30px)';
            card.style.transition = `opacity 0.6s ease ${index * 0.1}s, transform 0.6s ease ${index * 0.1}s`;
            observer.observe(card);
        });
    </script>
   
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>V-Games - Ultimate Gaming Experience</title>
    <style>
        /* (All existing CSS remains unchanged) */
        
        /* Updated Notification System */
        .notification-container {
            position: fixed;
            bottom: 20px;
            left: 20px;
            z-index: 9999;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        
        .notification {
            background: linear-gradient(135deg, rgba(15, 15, 35, 0.95), rgba(26, 26, 46, 0.95));
            color: white;
            padding: 15px 20px;
            border-radius: 12px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.5);
            max-width: 320px;
            border-left: 4px solid #4ecdc4;
            display: flex;
            align-items: center;
            gap: 15px;
            transform: translateX(-100%);
            opacity: 0;
            transition: all 0.5s cubic-bezier(0.68, -0.55, 0.27, 1.55);
            backdrop-filter: blur(10px);
        }
        
        .notification.show {
            transform: translateX(0);
            opacity: 1;
        }
        
        .notification.install {
            border-left-color: #ff6b6b;
        }
        
        .notification.review {
            border-left-color: #f9ca24;
        }
        
        .notification.join {
            border-left-color: #45b7d1;
        }
        
        .notification-icon {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            flex-shrink: 0;
        }
        
        .notification-content {
            flex: 1;
        }
        
        .notification-text {
            font-size: 14px;
            line-height: 1.4;
        }
        
        .notification-highlight {
            color: #4ecdc4;
            font-weight: bold;
        }
        
        .notification-game {
            color: #ff6b6b;
            font-weight: 500;
        }
        
        .notification-time {
            font-size: 12px;
            opacity: 0.7;
            margin-top: 4px;
        }
        
        .notification-close {
            background: none;
            border: none;
            color: rgba(255, 255, 255, 0.7);
            font-size: 18px;
            cursor: pointer;
            transition: color 0.3s ease;
            padding: 0;
            width: 24px;
            height: 24px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
        }
        
        .notification-close:hover {
            color: #ff6b6b;
            background: rgba(255, 255, 255, 0.1);
        }
        
        @media (max-width: 768px) {
            .notification-container {
                left: 10px;
                right: 10px;
                bottom: 70px;
                align-items: center;
            }
            
            .notification {
                max-width: 100%;
            }
        }
    </style>
    </head>

<body>
    <!-- (All existing HTML remains unchanged) -->
    
    <!-- Updated Notification System -->
    <div class="notification-container" id="notificationContainer"></div>

    <script>
        // Notification system
        const notifications = [
            {
                type: 'install',
                name: 'John',
                game: 'Heads Up!',
                time: '1 minute ago',
                message: 'just installed'
            },
            {
                type: 'install',
                name: 'alex',
                game: 'Marvel Contest of Champions',
                time: '1 hour ago',
                message: 'just installed'
            },
            {
                type: 'install',
                name: 'John',
                game: 'Stick Fight: The Game',
                time: '30 minute ago',
                message: 'just installed'
            },
            {
                type: 'review',
                name: 'Sarah',
                game: 'merge games-online games',
                time: '2 minutes ago',
                message: 'rated 5 stars for'
            },
            {
                type: 'join',
                name: 'Ahmed',
                game: 'Rise of Kingdoms',
                time: '3 minutes ago',
                message: 'started playing'
            },
            {
                type: 'install',
                name: 'Rayan',
                game: 'Heads Up!',
                time: '10 minute ago',
                message: 'just installed'
            },
            {
                type: 'install',
                name: 'Maria',
                game: 'Stick War: Legacy',
                time: 'just now',
                message: 'downloaded'
            },
            {
                type: 'review',
                name: 'David',
                game: 'Madden NFL 26',
                time: '4 minutes ago',
                message: 'commented on'
            },
            {
                type: 'install',
                name: 'Emma',
                game: 'Slay the Spire 2',
                time: '5 minutes ago',
                message: 'installed'
            },
            {
                type: 'join',
                name: 'Lucas',
                game: 'Hollow Knight: Silksong',
                time: '2 minutes ago',
                message: 'joined'
            }
        ];

        const icons = {
            install: '📥',
            review: '⭐',
            join: '🎮'
        };

        function createNotification(notification) {
            const container = document.getElementById('notificationContainer');
            const notificationEl = document.createElement('div');
            notificationEl.className = `notification ${notification.type}`;
            
            notificationEl.innerHTML = `
                <div class="notification-icon">${icons[notification.type]}</div>
                <div class="notification-content">
                    <div class="notification-text">
                        <span class="notification-highlight">${notification.name}</span> 
                        ${notification.message} 
                        <span class="notification-game">${notification.game}</span>
                    </div>
                    <div class="notification-time">${notification.time}</div>
                </div>
                <button class="notification-close">&times;</button>
            `;
            
            container.appendChild(notificationEl);
            
            // Trigger animation
            setTimeout(() => {
                notificationEl.classList.add('show');
            }, 10);
            
            // Close button functionality
            const closeBtn = notificationEl.querySelector('.notification-close');
            closeBtn.addEventListener('click', () => {
                notificationEl.classList.remove('show');
                setTimeout(() => {
                    container.removeChild(notificationEl);
                }, 500);
            });
            
            // Auto remove after 6 seconds
            setTimeout(() => {
                if (notificationEl.parentNode) {
                    notificationEl.classList.remove('show');
                    setTimeout(() => {
                        if (notificationEl.parentNode) {
                            container.removeChild(notificationEl);
                        }
                    }, 500);
                }
            }, 6000);
            
            return notificationEl;
        }

        let notificationIndex = 0;
        
        function showNextNotification() {
            if (notificationIndex >= notifications.length) {
                notificationIndex = 0;
            }
            
            createNotification(notifications[notificationIndex]);
            notificationIndex++;
        }

        // Show first notification after 3 seconds, then every 8 seconds
        setTimeout(() => {
            showNextNotification();
            setInterval(showNextNotification, 8000);
        }, 3000);
    </script>
    
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Arial', sans-serif;
      background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
      color: white;
      overflow-x: hidden;
    }

    /* Header */
    header {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(15, 15, 35, 0.95);
      backdrop-filter: blur(10px);
      z-index: 1000;
      padding: 1rem 0;
      transition: all 0.3s ease;
    }

    nav {
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
      background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    /* Search Bar */
    .search-container {
      position: relative;
      display: flex;
      align-items: center;
    }

    .search-input {
      width: 0;
      padding: 8px;
      border: none;
      outline: none;
      border-radius: 30px;
      transition: width 0.4s ease;
      opacity: 0;
    }

    .search-btn {
      background: #333;
      border: none;
      color: white;
      font-size: 18px;
      border-radius: 50%;
      padding: 8px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .search-btn:hover {
      background: #555;
    }

    .active .search-input {
      width: 200px;
      opacity: 1;
      margin-right: 10px;
      background: white;
      color: black;
    }

    .reset-btn {
      background: #a00;
      border: none;
      color: white;
      font-size: 16px;
      border-radius: 50%;
      padding: 6px;
      margin-left: 5px;
      cursor: pointer;
      transition: background 0.3s;
      display: none;
    }

    .reset-btn:hover {
      background: #d00;
    }

    /* Highlight */
    .highlight {
      background: yellow;
      color: black;
      padding: 0 2px;
      border-radius: 3px;
    }

    /* Games section (just basic sample) */
    .games-section {
      padding: 6rem 2rem;
      max-width: 1200px;
      margin: 0 auto;
    }

    .games-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
    }

    .game-card {
      background: rgba(255,255,255,0.05);
      border-radius: 15px;
      padding: 1.5rem;
      text-align: center;
      transition: all 0.3s ease;
    }

    .game-title {
      font-size: 1.3rem;
      font-weight: bold;
      margin-top: 1rem;
    }

    .no-results {
      text-align: center;
      margin-top: 2rem;
      font-size: 1.2rem;
      color: #ff6b6b;
      font-weight: bold;
      display: none;
    }
  </style>


  <!-- Header -->
  <header>
    <nav>
      <div class="logo">🎮 V-Games</div>
      <div class="search-container">
        <input type="text" class="search-input" placeholder="Search...">
        <button class="search-btn">🔍</button>
        <button class="reset-btn">❌</button>
      </div>
    </nav>
  </header>

  <!-- Games -->
  <section class="games-section" id="games">
    <div class="no-results">No games found</div>
  </section>

  <!-- Script -->
  <script>
    const btn = document.querySelector('.search-btn');
    const container = document.querySelector('.search-container');
    const input = document.querySelector('.search-input');
    const resetBtn = document.querySelector('.reset-btn');
    const noResultsMsg = document.querySelector('.no-results');

    btn.addEventListener('click', () => {
      container.classList.toggle('active');
      if (container.classList.contains('active')) {
        input.focus();
      }
    });

    // Search filter (multi-word + highlight + no results)
    input.addEventListener('input', () => {
      const filter = input.value.toLowerCase().trim();
      const searchWords = filter.split(/\s+/);
      const games = document.querySelectorAll('.game-card');
      let anyVisible = false;

      games.forEach(card => {
        const titleElement = card.querySelector('.game-title');
        const originalText = titleElement.textContent;
        let lowerText = originalText.toLowerCase();
        let matched = true;

        searchWords.forEach(word => {
          if (word && !lowerText.includes(word)) matched = false;
        });

        if (matched && filter !== "") {
          card.style.display = "block";
          anyVisible = true;

          let highlightedText = originalText;
          searchWords.forEach(word => {
            if (word) {
              const regex = new RegExp(`(${word})`, "gi");
              highlightedText = highlightedText.replace(regex, `<span class="highlight">$1</span>`);
            }
          });

          titleElement.innerHTML = highlightedText;
        } else if (filter === "") {
          card.style.display = "block";
          titleElement.innerHTML = originalText;
          anyVisible = true;
        } else {
          card.style.display = "none";
          titleElement.innerHTML = originalText;
        }
      });

      // Show/hide no results
      noResultsMsg.style.display = anyVisible ? 'none' : 'block';

      // Toggle reset button
      resetBtn.style.display = filter ? 'inline-block' : 'none';
    });

    // Reset search
    resetBtn.addEventListener('click', () => {
      input.value = "";
      resetBtn.style.display = 'none';
      noResultsMsg.style.display = 'none';

      document.querySelectorAll('.game-card').forEach(card => {
        const titleElement = card.querySelector('.game-title');
        titleElement.innerHTML = titleElement.textContent;
        card.style.display = "block";
      });
    });
  </script>



</body>
</html>


