<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SnakeBattleArena - Epic Multiplayer Snake Battle Game Online</title>
    <meta name="description" content="Play SnakeBattleArena, the ultimate multiplayer snake battle game online. Challenge friends in real-time snake combat with stunning graphics and smooth gameplay.">
    <meta name="keywords" content="SnakeBattleArena, snake game, multiplayer snake, online snake battle, snake combat, browser game, arcade game">
    <meta name="robots" content="index, follow">
    <meta name="author" content="SnakeBattleArena Team">
    
    <!-- Open Graph Meta Tags -->
    <meta property="og:title" content="SnakeBattleArena - Epic Multiplayer Snake Battle Game">
    <meta property="og:description" content="Experience the ultimate snake battle arena with multiplayer combat, stunning visuals, and competitive gameplay.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://snakebattlearena.com">
    <meta property="og:image" content="https://snakebattlearena.com/images/og-image.jpg">
    
    <!-- Twitter Card Meta Tags -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="SnakeBattleArena - Epic Multiplayer Snake Battle Game">
    <meta name="twitter:description" content="Challenge friends in the ultimate snake battle arena with real-time multiplayer combat.">
    <meta name="twitter:image" content="https://snakebattlearena.com/images/twitter-card.jpg">
    
    <!-- Canonical URL -->
    <link rel="canonical" href="https://snakebattlearena.com">
    
    <!-- Favicon -->
    <link rel="icon" type="image/x-icon" href="/favicon.ico">
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
    
    <!-- Preconnect for performance -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=SF+Pro+Display:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            /* Apple-inspired color palette */
            --primary-blue: #007AFF;
            --primary-blue-hover: #0051D5;
            --secondary-blue: #5AC8FA;
            --background-light: #F2F2F7;
            --background-dark: #1C1C1E;
            --surface-light: #FFFFFF;
            --surface-dark: #2C2C2E;
            --text-primary: #000000;
            --text-secondary: #8E8E93;
            --accent-green: #30D158;
            --accent-orange: #FF9500;
            --accent-red: #FF3B30;
            --accent-purple: #AF52DE;
            --border-light: #D1D1D6;
            --shadow: rgba(0, 0, 0, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: var(--text-primary);
            background-color: var(--background-light);
            font-size: 16px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid var(--border-light);
            position: sticky;
            top: 0;
            z-index: 100;
            padding: 1rem 0;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-blue);
            text-decoration: none;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            text-decoration: none;
            color: var(--text-primary);
            font-weight: 500;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: var(--primary-blue);
        }

        /* Hero Section */
        .hero {
            padding: 4rem 0;
            text-align: center;
            background: linear-gradient(135deg, var(--primary-blue) 0%, var(--secondary-blue) 100%);
            color: white;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="20" cy="20" r="1" fill="white" opacity="0.1"/><circle cx="80" cy="40" r="1" fill="white" opacity="0.05"/><circle cx="40" cy="80" r="1" fill="white" opacity="0.1"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
            opacity: 0.3;
        }

        .hero-content {
            position: relative;
            z-index: 1;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 700;
            margin-bottom: 1rem;
            letter-spacing: -0.02em;
        }

        .hero-subtitle {
            font-size: clamp(1.1rem, 2.5vw, 1.5rem);
            font-weight: 400;
            margin-bottom: 2rem;
            opacity: 0.9;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-button {
            display: inline-block;
            background: var(--surface-light);
            color: var(--primary-blue);
            text-decoration: none;
            padding: 1rem 2rem;
            border-radius: 12px;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.15);
        }

        /* Game Section */
        .game-section {
            padding: 4rem 0;
            background: var(--surface-light);
        }

        .game-container {
            background: var(--background-light);
            border-radius: 20px;
            padding: 2rem;
            box-shadow: 0 4px 30px var(--shadow);
            border: 1px solid var(--border-light);
        }

        .game-iframe {
            width: 100%;
            height: 600px;
            border: none;
            border-radius: 12px;
            background: #000;
        }

        /* Features Section */
        .features {
            padding: 4rem 0;
            background: var(--background-light);
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature-card {
            background: var(--surface-light);
            padding: 2rem;
            border-radius: 16px;
            box-shadow: 0 2px 20px var(--shadow);
            border: 1px solid var(--border-light);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 40px var(--shadow);
        }

        .feature-icon {
            width: 60px;
            height: 60px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        .feature-icon.multiplayer {
            background: linear-gradient(135deg, var(--accent-green), var(--secondary-blue));
        }

        .feature-icon.graphics {
            background: linear-gradient(135deg, var(--accent-purple), var(--accent-red));
        }

        .feature-icon.competitive {
            background: linear-gradient(135deg, var(--accent-orange), var(--accent-red));
        }

        .feature-icon.cross-platform {
            background: linear-gradient(135deg, var(--primary-blue), var(--accent-purple));
        }

        .feature-card h3 {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 1rem;
            color: var(--text-primary);
        }

        .feature-card p {
            color: var(--text-secondary);
            line-height: 1.6;
        }

        /* About Section */
        .about {
            padding: 4rem 0;
            background: var(--surface-light);
        }

        .about-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .about h2 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 2rem;
            color: var(--text-primary);
        }

        .about p {
            font-size: 1.1rem;
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
            line-height: 1.7;
        }

        /* How to Play Section */
        .how-to-play {
            padding: 4rem 0;
            background: var(--background-light);
        }

        .controls-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .control-card {
            background: var(--surface-light);
            padding: 1.5rem;
            border-radius: 12px;
            border: 1px solid var(--border-light);
            text-align: center;
        }

        .control-card h4 {
            color: var(--primary-blue);
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .control-keys {
            display: flex;
            justify-content: center;
            gap: 0.5rem;
            flex-wrap: wrap;
        }

        .key {
            background: var(--background-light);
            border: 2px solid var(--border-light);
            border-radius: 6px;
            padding: 0.5rem;
            font-weight: 600;
            min-width: 40px;
            text-align: center;
        }

        /* Footer */
        footer {
            background: var(--surface-dark);
            color: white;
            padding: 3rem 0 2rem;
            text-align: center;
        }

        .footer-content {
            max-width: 800px;
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
            color: rgba(255, 255, 255, 0.8);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: white;
        }

        .copyright {
            color: rgba(255, 255, 255, 0.6);
            font-size: 0.9rem;
        }

        /* Section Headers */
        .section-header {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-header h2 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: var(--text-primary);
        }

        .section-header p {
            font-size: 1.1rem;
            color: var(--text-secondary);
            max-width: 600px;
            margin: 0 auto;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                padding: 0 15px;
            }

            .header-content {
                flex-direction: column;
                gap: 1rem;
            }

            nav ul {
                gap: 1rem;
            }

            .hero {
                padding: 3rem 0;
            }

            .game-section,
            .features,
            .about,
            .how-to-play {
                padding: 3rem 0;
            }

            .game-iframe {
                height: 400px;
            }

            .section-header h2 {
                font-size: 2rem;
            }

            .about h2 {
                font-size: 2rem;
            }

            .footer-links {
                flex-direction: column;
                gap: 1rem;
            }
        }

        @media (max-width: 480px) {
            .game-container {
                padding: 1rem;
            }

            .game-iframe {
                height: 350px;
            }

            .feature-card,
            .control-card {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <a href="#" class="logo">SnakeBattleArena</a>
                <nav>
                    <ul>
                        <li><a href="#game">Play Now</a></li>
                        <li><a href="#features">Features</a></li>
                        <li><a href="#how-to-play">How to Play</a></li>
                        <li><a href="#about">About</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>SnakeBattleArena</h1>
                <p class="hero-subtitle">Experience the ultimate multiplayer snake battle with stunning graphics and competitive gameplay</p>
                <a href="#game" class="cta-button">Play Now - Free Online</a>
            </div>
        </div>
    </section>

    <!-- Game Section -->
    <section id="game" class="game-section">
        <div class="container">
            <div class="section-header">
                <h2>Play SnakeBattleArena Online</h2>
                <p>Challenge your friends in real-time multiplayer snake combat. No downloads required - play instantly in your browser!</p>
            </div>
            <div class="game-container">
                <iframe class="game-iframe" 
                        src="data:text/html;charset=utf-8,%3C!DOCTYPE%20html%3E%3Chtml%3E%3Chead%3E%3Ctitle%3ESnakeBattleArena%20Game%3C/title%3E%3C/head%3E%3Cbody%20style%3D%22margin%3A0%3Bpadding%3A0%3Bbackground%3A%23000%3Bcolor%3A%23fff%3Bfont-family%3AArial%3Bdisplay%3Aflex%3Balign-items%3Acenter%3Bjustify-content%3Acenter%3Bheight%3A100vh%3B%22%3E%3Cdiv%20style%3D%22text-align%3Acenter%3B%22%3E%3Ch2%20style%3D%22color%3A%23007AFF%3B%22%3ESnakeBattleArena%3C/h2%3E%3Cp%3EGame%20loading...%3C/p%3E%3Cp%20style%3D%22font-size%3A14px%3Bopacity%3A0.7%3B%22%3EPress%20WASD%20(Player%201)%20or%20Arrow%20Keys%20(Player%202)%20to%20start%3C/p%3E%3C/div%3E%3C/body%3E%3C/html%3E"
                        title="SnakeBattleArena Game"
                        loading="lazy">
                </iframe>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
        <div class="container">
            <div class="section-header">
                <h2>Game Features</h2>
                <p>Discover what makes SnakeBattleArena the most exciting snake game experience</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon multiplayer">🎮</div>
                    <h3>Real-Time Multiplayer</h3>
                    <p>Battle against friends or players worldwide in intense real-time snake combat. Experience smooth, lag-free multiplayer action with up to 4 players simultaneously.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon graphics">✨</div>
                    <h3>Stunning Graphics</h3>
                    <p>Enjoy beautiful visual effects, smooth animations, and modern design. Our game features glowing trails, particle effects, and responsive visual feedback.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon competitive">🏆</div>
                    <h3>Competitive Gameplay</h3>
                    <p>Master strategic movement, timing, and positioning to dominate the arena. Climb leaderboards and prove you're the ultimate snake battle champion.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon cross-platform">📱</div>
                    <h3>Cross-Platform Compatible</h3>
                    <p>Play seamlessly across desktop, tablet, and mobile devices. Our responsive design ensures optimal gameplay experience on any screen size.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- How to Play Section -->
    <section id="how-to-play" class="how-to-play">
        <div class="container">
            <div class="section-header">
                <h2>How to Play SnakeBattleArena</h2>
                <p>Master the controls and dominate the battlefield with these essential gameplay mechanics</p>
            </div>
            <div class="controls-grid">
                <div class="control-card">
                    <h4>Player 1 Controls</h4>
                    <div class="control-keys">
                        <span class="key">W</span>
                        <span class="key">A</span>
                        <span class="key">S</span>
                        <span class="key">D</span>
                    </div>
                    <p>Use WASD keys to move your snake around the arena</p>
                </div>
                <div class="control-card">
                    <h4>Player 2 Controls</h4>
                    <div class="control-keys">
                        <span class="key">↑</span>
                        <span class="key">←</span>
                        <span class="key">↓</span>
                        <span class="key">→</span>
                    </div>
                    <p>Use arrow keys to navigate and outmaneuver opponents</p>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="about-content">
                <h2>About SnakeBattleArena</h2>
                <p>SnakeBattleArena revolutionizes the classic snake game by introducing competitive multiplayer combat in a modern, visually stunning arena. Built with cutting-edge web technologies, our game delivers smooth 60fps gameplay with responsive controls and engaging visual effects.</p>
                
                <p>Whether you're a casual player looking for quick entertainment or a competitive gamer seeking intense battles, SnakeBattleArena offers the perfect balance of accessibility and depth. The game features intuitive controls that are easy to learn but difficult to master, ensuring endless hours of engaging gameplay.</p>
                
                <p>Our development team has carefully crafted every aspect of the game experience, from the fluid snake movement mechanics to the satisfying collision detection system. With regular updates and new features, SnakeBattleArena continues to evolve as the premier online snake battle experience.</p>
                
                <p>Join thousands of players worldwide who have discovered the thrill of multiplayer snake combat. Challenge your reflexes, outsmart your opponents, and climb the leaderboards in the ultimate test of snake mastery.</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-links">
                    <a href="#game">Play Game</a>
                    <a href="#features">Features</a>
                    <a href="#how-to-play">How to Play</a>
                    <a href="#about">About</a>
                    <a href="#privacy">Privacy Policy</a>
                    <a href="#terms">Terms of Service</a>
                </div>
                <div class="copyright">
                    <p>&copy; 2024 SnakeBattleArena. All rights reserved. Built with ❤️ for snake game enthusiasts worldwide.</p>
                </div>
            </div>
        </div>
    </footer>

    <!-- Schema.org structured data -->
    <script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "VideoGame",
        "name": "SnakeBattleArena",
        "description": "Ultimate multiplayer snake battle game with real-time combat, stunning graphics, and competitive gameplay",
        "url": "https://snakebattlearena.com",
        "genre": ["Action", "Arcade", "Multiplayer"],
        "gamePlatform": ["Web Browser", "Mobile", "Desktop"],
        "applicationCategory": "Game",
        "operatingSystem": ["Windows", "macOS", "iOS", "Android", "Linux"],
        "offers": {
            "@type": "Offer",
            "price": "0",
            "priceCurrency": "USD"
        },
        "aggregateRating": {
            "@type": "AggregateRating",
            "ratingValue": "4.8",
            "ratingCount": "1250"
        }
    }
    </script>
</body>
</html>
