# Ligma
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ligma | Creative Agency</title>
    <style>
        :root {
            --deep-space-black: #0c0c0c;
            --dark-nebula-blue: #0a1128;
            --event-horizon-blue: #081229;
            --quantum-accent-blue: #0d47a1;
            --plasma-blue: #1565c0;
            --cosmic-light: #64b5f6;
            --starlight-white: #f4f4f4;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        body {
            font-family: "SF Pro Text", "SF Pro Icons", "Helvetica Neue", "Helvetica", "Arial", sans-serif;
            background-color: var(--deep-space-black);
            color: var(--starlight-white);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .cosmic-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(
                ellipse at center, 
                rgba(13, 71, 161, 0.2) 0%, 
                var(--deep-space-black) 100%
            );
            z-index: -1;
            pointer-events: none;
        }

        .container {
            max-width: 1420px;
            margin: 0 auto;
            padding: 0 20px;
            position: relative;
            z-index: 1;
        }

        /* Header Navigation */
        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 30px 0;
            background: linear-gradient(
                to right, 
                rgba(13, 71, 161, 0.1), 
                rgba(8, 18, 41, 0.3)
            );
            backdrop-filter: blur(15px);
        }

        .logo {
            font-size: 28px;
            font-weight: 700;
            letter-spacing: -0.03em;
            background: linear-gradient(45deg, var(--cosmic-light), var(--quantum-accent-blue));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            -webkit-text-fill-color: transparent;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        .nav-menu a {
            text-decoration: none;
            color: var(--cosmic-light);
            transition: all 0.3s ease;
            position: relative;
            font-weight: 500;
        }

        .nav-menu a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: linear-gradient(to right, var(--cosmic-light), transparent);
            transition: width 0.3s ease;
        }

        .nav-menu a:hover {
            color: var(--starlight-white);
        }

        .nav-menu a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            min-height: 90vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
        }

        .hero h1 {
            font-size: 58px;
            font-weight: 800;
            letter-spacing: -0.05em;
            background: linear-gradient(
                45deg, 
                var(--cosmic-light), 
                var(--quantum-accent-blue), 
                var(--starlight-white)
            );
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            -webkit-text-fill-color: transparent;
            animation: cosmic-pulse 4s infinite alternate;
        }

        @keyframes cosmic-pulse {
            0% { opacity: 0.7; }
            100% { opacity: 1; }
        }

        .hero p {
            font-size: 24px;
            color: var(--cosmic-light);
            margin: 20px 0 40px;
            line-height: 1.4;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(
                45deg, 
                var(--quantum-accent-blue), 
                var(--plasma-blue)
            );
            color: var(--starlight-white);
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            box-shadow: 0 10px 30px rgba(13, 71, 161, 0.4);
        }

        .cta-button:hover {
            transform: scale(1.05);
            box-shadow: 0 15px 40px rgba(13, 71, 161, 0.6);
        }

        /* Services Section */
        .services {
            background: linear-gradient(
                to bottom, 
                var(--event-horizon-blue), 
                var(--deep-space-black)
            );
            padding: 100px 0;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .service-card {
            background: rgba(13, 71, 161, 0.1);
            border: 1px solid rgba(101, 181, 246, 0.1);
            padding: 40px 30px;
            border-radius: 15px;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(13, 71, 161, 0.3);
        }

        .service-card h3 {
            font-size: 28px;
            margin-bottom: 20px;
            background: linear-gradient(
                45deg, 
                var(--cosmic-light), 
                var(--starlight-white)
            );
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            -webkit-text-fill-color: transparent;
        }

        /* Footer */
        .footer {
            background: linear-gradient(
                to top, 
                var(--event-horizon-blue), 
                var(--deep-space-black)
            );
            padding: 50px 0;
            text-align: center;
        }

        .contact-details {
            margin-top: 30px;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 40px;
        }

        .social-icon {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-decoration: none;
            transition: transform 0.3s ease;
        }

        .social-icon:hover {
            transform: translateY(-5px);
        }

        .social-icon img {
            width: 36px;
            height: 36px;
            margin-bottom: 8px;
            filter: brightness(0) invert(1);
            transition: filter 0.3s ease;
        }

        .social-icon:hover img {
            filter: brightness(0) invert(0.8) sepia(1) saturate(5) hue-rotate(180deg);
        }

        .social-icon span {
            color: var(--cosmic-light);
            font-size: 14px;
            transition: color 0.3s ease;
        }

        .social-icon:hover span {
            color: var(--starlight-white);
        }
    </style>
</head>
<body>
    <div class="cosmic-background"></div>

    <header class="container header">
        <div class="logo">Ligma</div>
        <nav>
            <ul class="nav-menu">
                <li><a href="#home">Home</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="home" class="container hero">
            <div class="hero-content">
                <h1>Build And Grow With Ligma </h1>
                <p>Dive into a realm where creativity defines boundaries, and innovation knows no limits. We transform abstract concepts into extraordinary realities.</p>
                <a href="#contact" class="cta-button">Explore Our Small Universe</a>
            </div>
        </section>

        <section id="services" class="services container">
            <div class="services-grid">
                <div class="service-card">
                    <h3>Branding</h3>
                    <p>Crafting unique brand identities that resonate and captivate across valuable consumers worldwide.</p>
                </div>
                <div class="service-card">
                    <h3>Marketing</h3>
                    <p>Strategic campaigns that break through the noise and connect with your audience by Heart.</p>
                </div>
                <div class="service-card">
                    <h3>Market Research</h3>
                    <p>Deep dive into market trends, uncovering insights that drive strategic decisions.</p>
                </div>
                <div class="service-card">
                    <h3>Creative Design</h3>
                    <p>Transforming abstract ideas into visual masterpieces that tell compelling stories.</p>
                </div>
                <div class="service-card">
                    <h3>Digital Strategy</h3>
                    <p>Navigating the digital landscape with innovative approaches and cutting-edge solutions.</p>
                </div>
                <div class="service-card">
                    <h3>Consulting</h3>
                    <p>Expert guidance to help your brand navigate complex market dynamics and I'll also provide a valuable tip towards your Goals.</p>
                </div>
            </div>
        </section>
    </main>

    <footer id="contact" class="footer">
        <div class="container">
            <h2>Dive Deeper With Ligma And Bounce Back Again </h2>
            <div class="contact-details">
                <a href="mailto:hariomdangi766593@gmail.com" class="social-icon">
                    <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZD0iTTIwIDRINEMyLjkgNCAyIDQuOSAyIDZ2MTJjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY2YzAtMS4xLS45LTItMi0yem0wIDRsLTggNS04LTVWNmw4IDUgOC01djJ6Ii8+PC9zdmc+" alt="Email Icon">
                    <span>Email</span>
                </a>
                <a href="https://www.linkedin.com/in/ohm-jaggy" target="_blank" class="social-icon">
                    <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZD0iTTQgNCBoMTYgdiAxNiBoLTE2IHoiIGZpbGw9Im5vbmUiIHN0cm9rZT0iI2ZmZiIgc3Ryb2tlLXdpZHRoPSIyIi8+PHBhdGggZD0iTTYgMTIgdiA2IE0xMCAxMCB2IDggbSA0IC00IGwgLTQgNCBtIDQgMCBsIDQtNCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjZmZmIiBzdHJva2Utd2lkdGg9IjIiLz48L3N2Zz4=" alt="LinkedIn Icon">
                    <span>LinkedIn</span>
                </a>
                <a href="https://twitter.com/OJagay" target="_blank" class="social-icon">
                    <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZD0iTTMgMyAxOCAxOCBNMTggMyAzIDE4IiBzdHJva2U9IiNmZmYiIHN0cm9rZS13aWR0aD0iMiIvPjwvc3ZnPg==" alt="X Icon">
                    <span>X (Twitter)</span>
                </a>
            </div>
            <p>&copy; 2025 Ligma Agency. All Cosmic Rights Reserved.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
