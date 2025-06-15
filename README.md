<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BGMI BattleHub Malegaon | Official Esports Community</title>
    <style>
        :root {
            --bg-dark: #0a0e17;
            --accent-blue: #2563eb;
            --accent-cyan: #06b6d4;
            --accent-purple: #7c3aed;
            --text-light: #f8fafc;
            --text-gray: #94a3b8;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-light);
            margin: 0;
            padding: 0;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background-color: rgba(10, 14, 23, 0.95);
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.3);
            border-bottom: 1px solid rgba(37, 99, 235, 0.3);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-family: 'Orbitron', sans-serif;
            font-size: 2rem;
            font-weight: 700;
            background: linear-gradient(90deg, var(--accent-blue), var(--accent-cyan));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: 1px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
            margin: 0;
            padding: 0;
        }
        
        nav a {
            color: var(--text-gray);
            text-decoration: none;
            font-weight: 500;
            font-size: 1rem;
            transition: all 0.3s ease;
            position: relative;
        }
        
        nav a:hover {
            color: var(--text-light);
        }
        
        nav a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: var(--accent-cyan);
            transition: width 0.3s ease;
        }
        
        nav a:hover::after {
            width: 100%;
        }
        
        /* Hero Section */
        .hero {
            height: 90vh;
            background: linear-gradient(rgba(10, 14, 23, 0.8), rgba(10, 14, 23, 0.9)), 
                        url('https://images.unsplash.com/photo-1607853202273-797f1c22a38e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
        }
        
        .hero-content {
            max-width: 800px;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            font-weight: 700;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.2rem;
            color: var(--text-gray);
            margin-bottom: 40px;
            max-width: 700px;
        }
        
        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        .btn {
            padding: 14px 32px;
            border-radius: 6px;
            font-weight: 600;
            text-transform: uppercase;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 1rem;
            letter-spacing: 0.5px;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }
        
        .btn-primary {
            background-color: var(--accent-blue);
            color: white;
            box-shadow: 0 4px 15px rgba(37, 99, 235, 0.3);
        }
        
        .btn-primary:hover {
            background-color: #1d4ed8;
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(37, 99, 235, 0.4);
        }
        
        .btn-secondary {
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            border: 1px solid rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(5px);
        }
        
        .btn-secondary:hover {
            background-color: rgba(255, 255, 255, 0.2);
            transform: translateY(-2px);
        }
        
        /* About Us Section */
        .about {
            padding: 100px 0;
            background-color: #0f172a;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            width: 60px;
            height: 3px;
            background: linear-gradient(90deg, var(--accent-blue), var(--accent-cyan));
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }
        
        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--accent-cyan);
        }
        
        .about-text p {
            margin-bottom: 20px;
            color: var(--text-gray);
        }
        
        .about-image {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.3);
        }
        
        /* Winners Section */
        .winners {
            padding: 100px 0;
            background-color: var(--bg-dark);
        }
        
        .winner-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .winner-card {
            background: linear-gradient(145deg, #0f172a, #1e293b);
            border-radius: 10px;
            padding: 30px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: all 0.3s ease;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.2);
        }
        
        .winner-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.3);
            border-color: rgba(37, 99, 235, 0.3);
        }
        
        .winner-card img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--accent-blue);
            margin: 0 auto 20px;
            box-shadow: 0 5px 15px rgba(37, 99, 235, 0.3);
        }
        
        .winner-card h3 {
            font-size: 1.5rem;
            margin: 10px 0 5px;
        }
        
        .winner-card .position {
            font-size: 1rem;
            color: var(--accent-cyan);
            margin-bottom: 10px;
            font-weight: 600;
        }
        
        .winner-card .prize {
            font-size: 1.2rem;
            color: var(--text-light);
            font-weight: 600;
            background: rgba(37, 99, 235, 0.1);
            padding: 8px 15px;
            border-radius: 20px;
            display: inline-block;
        }
        
        /* Footer */
        footer {
            background-color: #020617;
            padding: 80px 0 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 60px;
        }
        
        .footer-logo {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.8rem;
            font-weight: 700;
            background: linear-gradient(90deg, var(--accent-blue), var(--accent-cyan));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 20px;
            display: inline-block;
        }
        
        .footer-about p {
            color: var(--text-gray);
            margin-bottom: 20px;
        }
        
        .footer-links h3, .footer-contact h3 {
            color: var(--text-light);
            font-size: 1.2rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-links h3::after, .footer-contact h3::after {
            content: '';
            position: absolute;
            width: 40px;
            height: 2px;
            background: var(--accent-cyan);
            bottom: 0;
            left: 0;
        }
        
        .footer-links ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        
        .footer-links li {
            margin-bottom: 12px;
        }
        
        .footer-links a {
            color: var(--text-gray);
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-links a:hover {
            color: var(--accent-cyan);
        }
        
        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 10px;
            margin-bottom: 15px;
            color: var(--text-gray);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 50%;
            color: var(--text-light);
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--accent-blue);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            color: var(--text-gray);
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .about-content {
                grid-template-columns: 1fr;
            }
            
            nav ul {
                gap: 15px;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Orbitron:wght@500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">BGMI BattleHub Malegaon</div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Malegaon's Premier BGMI Esports Community</h1>
            <p>Join the most competitive BGMI gaming hub in Maharashtra. Train with pros and showcase your skills.</p>
            <div class="cta-buttons">
                <a href="https://wa.me/917276149954?text=I%20want%20to%20join%20BGMI%20BattleHub%20Malegaon" class="btn btn-primary">
                    <i class="fab fa-whatsapp"></i> Register Now
                </a>
                <a href="https://youtube.com/@bgmimalegaon?si=JQnLPXDNuqds9SjZ" class="btn btn-secondary">
                    <i class="fab fa-youtube"></i> Watch Live
                </a>
            </div>
        </div>
    </section>

    <!-- About Us Section -->
    <section class="about" id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Our Community</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Elevating BGMI Esports in Malegaon</h3>
                    <p>BGMI BattleHub Malegaon is the definitive platform for competitive mobile gaming enthusiasts. Founded by passionate gamers, we've created a structured ecosystem that nurtures talent through:</p>
                    <p>• Weekly training sessions with experienced coaches<br>
                       • Regular scrimmages against top-tier teams<br>
                       • Fair and transparent tournament systems<br>
                       • Networking opportunities with esports organizations</p>
                    <p>Our mission is to put Malegaon on India's esports map by developing world-class BGMI players through professional training and competitive exposure.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="BGMI Esports Team">
                </div>
            </div>
        </div>
    </section>

    <!-- Winners Section -->
    <section class="winners">
        <div class="container">
            <div class="section-title">
                <h2>Recent Tournament Winners</h2>
                <p>Celebrating excellence in our latest championship</p>
            </div>
            <div class="winner-cards">
                <div class="winner-card">
                    <img src="https://images.unsplash.com/photo-1579547621309-5e57ab324182?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="IKKINZO Team">
                    <h3>IKKINZO</h3>
                    <div class="position">1st Place Champions</div>
                    <div class="prize">₹5,000 Prize</div>
                </div>
                
                <div class="winner-card">
                    <img src="https://images.unsplash.com/photo-1535223289827-42f1e9919769?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="PANDAOP Team">
                    <h3>PANDAOP</h3>
                    <div class="position">2nd Place Runners-up</div>
                    <div class="prize">₹2,000 Prize</div>
                </div>
                
                <div class="winner-card">
                    <img src="https://images.unsplash.com/photo-1519085360753-af0119f7cbe7?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="IKKINZO2 Player">
                    <h3>IKKINZO2</h3>
                    <div class="position">Most Valuable Player</div>
                    <div class="prize">₹1,000 Prize</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-about">
                    <div class="footer-logo">BGMI BattleHub Malegaon</div>
                    <p>The official competitive gaming community for Battlegrounds Mobile India in Malegaon.</p>
                    <div class="social-links">
                        <a href="https://wa.me/917276149954" target="_blank"><i class="fab fa-whatsapp"></i></a>
                        <a href="https://www.facebook.com/share/1C2h2PMXAH/" target="_blank"><i class="fab fa-facebook-f"></i></a>
                        <a href="https://www.instagram.com/bgmihubmalegaon?igsh=NDU4cHkwYTY3cTlv" target="_blank"><i class="fab fa-instagram"></i></a>
                        <a href="https://youtube.com/@bgmimalegaon?si=JQnLPXDNuqds9SjZ" target="_blank"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                
                <div class="footer-contact">
                    <h3>Connect With Us</h3>
                    <div class="contact-item">
                        <i class="fas fa-phone-alt"></i>
                        <span>+91 7276149954</span>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <span>contact@bgmimalegaon.com</span>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <span>Malegaon, Maharashtra</span>
                    </div>
                </div>
            </div>
            
            <div class="copyright">
                © 2025 BGMI BattleHub Malegaon. All Rights Reserved.
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
