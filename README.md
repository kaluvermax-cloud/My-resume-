# My-resume-
My information 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kalu Verma - Commerce Student | Aspiring Finance Professional</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: #0a0a0a;
            color: #f0f0f0;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Smooth scrolling */
        html {
            scroll-behavior: smooth;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 10, 10, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
        }

        nav.scrolled {
            padding: 0.5rem 0;
            box-shadow: 0 2px 20px rgba(212, 175, 55, 0.1);
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
            font-size: 1.5rem;
            font-weight: 700;
            color: #d4af37;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: #f0f0f0;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: #d4af37;
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-links a:hover {
            color: #d4af37;
        }

        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
        }

        .hamburger span {
            width: 25px;
            height: 3px;
            background: #d4af37;
            margin: 3px 0;
            transition: 0.3s;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 100%);
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
            background: radial-gradient(circle at 20% 80%, rgba(212, 175, 55, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 80% 20%, rgba(212, 175, 55, 0.05) 0%, transparent 50%);
        }

        .hero-content {
            max-width: 800px;
            padding: 0 2rem;
            z-index: 2;
            animation: fadeInUp 1s ease-out;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 700;
            color: #f0f0f0;
            margin-bottom: 1rem;
            letter-spacing: -1px;
        }

        .hero .title {
            font-size: clamp(1.1rem, 2.5vw, 1.5rem);
            color: #d4af37;
            font-weight: 500;
            margin-bottom: 1.5rem;
        }

        .hero .tagline {
            font-size: 1.2rem;
            color: #b8b8b8;
            font-weight: 300;
            max-width: 600px;
            margin: 0 auto;
        }

        /* Sections */
        .section {
            padding: 100px 0;
            max-width: 1200px;
            margin: 0 auto;
            padding-left: 2rem;
            padding-right: 2rem;
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 600;
            color: #d4af37;
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: #d4af37;
            border-radius: 2px;
        }

        /* Section Content */
        .content-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .card {
            background: rgba(255, 255, 255, 0.02);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(212, 175, 55, 0.1);
            padding: 2rem;
            border-radius: 16px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 2px;
            background: linear-gradient(90deg, transparent, #d4af37, transparent);
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(212, 175, 55, 0.1);
            border-color: rgba(212, 175, 55, 0.3);
        }

        .card-icon {
            font-size: 2.5rem;
            color: #d4af37;
            margin-bottom: 1rem;
            display: block;
        }

        .card h3 {
            color: #f0f0f0;
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .card p {
            color: #b8b8b8;
            font-weight: 300;
        }

        .highlight {
            color: #d4af37;
            font-weight: 500;
        }

        /* List styles */
        .achievements-list, .skills-list {
            list-style: none;
            padding: 0;
        }

        .achievements-list li, .skills-list li {
            padding: 0.8rem 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            transition: all 0.3s ease;
        }

        .achievements-list li:hover, .skills-list li:hover {
            padding-left: 1rem;
            border-color: rgba(212, 175, 55, 0.2);
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1.5rem;
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(212, 175, 55, 0.1);
            border-radius: 12px;
            transition: all 0.3s ease;
        }

        .contact-item:hover {
            background: rgba(212, 175, 55, 0.05);
            border-color: #d4af37;
            transform: translateX(10px);
        }

        .contact-item i {
            font-size: 1.5rem;
            color: #d4af37;
            width: 40px;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 3rem 2rem;
            border-top: 1px solid rgba(212, 175, 55, 0.1);
            color: #b8b8b8;
        }

        /* Animations */
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
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* Mobile Responsiveness */
        @media (max-width: 768px) {
            .hamburger {
                display: flex;
            }

            .nav-links {
                position: fixed;
                top: 100%;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background: rgba(10, 10, 10, 0.98);
                flex-direction: column;
                justify-content: flex-start;
                align-items: center;
                padding-top: 2rem;
                transition: left 0.3s ease;
            }

            .nav-links.active {
                left: 0;
            }

            .section {
                padding: 80px 1rem;
                padding-left: 1rem;
                padding-right: 1rem;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .content-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll indicator */
        .scroll-indicator {
            position: absolute;
            bottom: 3rem;
            left: 50%;
            transform: translateX(-50%);
            color: #d4af37;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateX(-50%) translateY(0);
            }
            40% {
                transform: translateX(-50%) translateY(-10px);
            }
            60% {
                transform: translateX(-50%) translateY(-5px);
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <div class="logo">KV</div>
            <ul class="nav-links">
                <li><a href="#hero">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#education">Education</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="hero" class="hero">
        <div class="hero-content">
            <h1>Kalu Verma</h1>
            <div class="title">Commerce Student | Aspiring Finance Professional</div>
            <p class="tagline">Focused on building discipline, financial knowledge, and long-term stability.</p>
            <div class="scroll-indicator">
                <i class="fas fa-chevron-down"></i>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section fade-in">
        <h2 class="section-title"><i class="fas fa-user"></i> About Me</h2>
        <div class="content-grid">
            <div class="card">
                <i class="fas fa-graduation-cap card-icon"></i>
                <h3>Commerce Student</h3>
                <p>From Rajasthan, India. Passionate about finance, trading, and self-improvement. Continuously working on communication skills and real-world knowledge.</p>
            </div>
            <div class="card">
                <i class="fas fa-seedling card-icon"></i>
                <h3>Core Beliefs</h3>
                <p>I believe in <span class="highlight">discipline</span>, <span class="highlight">consistency</span>, and <span class="highlight">long-term growth</span>. Every day is an opportunity to build better habits and knowledge.</p>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section id="education" class="section fade-in">
        <h2 class="section-title"><i class="fas fa-book"></i> Education</h2>
        <div class="content-grid">
            <div class="card">
                <h3>Academic Institutions</h3>
                <ul>
                    <li>Tilak Public English Medium School (Early Education)</li>
                    <li>Moderna School, Aklera</li>
                </ul>
            </div>
            <div class="card">
                <h3>Academic Highlights</h3>
                <ul class="achievements-list">
                    <li><span class="highlight">Class 6:</span> 85.64% (5th & 3rd Position)</li>
                    <li><span class="highlight">Class 7:</span> 94.79%</li>
                    <li><span class="highlight">Class 8:</span> 2nd Position</li>
                    <li><span class="highlight">Class 9:</span> 90.33% (3rd Position)</li>
                </ul>
                <p class="highlight" style="margin-top: 1rem;">Consistent performance with continuous improvement</p>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section fade-in">
        <h2 class="section-title"><i class="fas fa-chart-line"></i> Skills</h2>
        <div class="content-grid">
            <div class="card">
                <i class="fas fa-comments card-icon"></i>
                <h3>Communication Skills</h3>
                <p>Actively improving through practice and real-world application</p>
            </div>
            <div class="card">
                <i class="fas fa-coins card-icon"></i>
                <h3>Financial Knowledge</h3>
                <p>Basic understanding of trading, markets, and personal finance</p>
            </div>
            <div class="card">
                <i class="fas fa-dumbbell card-icon"></i>
                <h3>Self-Discipline</h3>
                <p>Strong focus on consistency and habit building</p>
            </div>
            <div class="card">
                <i class="fas fa-search card-icon"></i>
                <h3>Learning Ability</h3>
                <p>Excellent research skills and continuous self-education</p>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="section fade-in">
        <h2 class="section-title"><i class="fas fa-briefcase"></i> Experience & Projects</h2>
        <div class="content-grid">
            <div class="card">
                <h3>Self-Learning Projects</h3>
                <ul>
                    <li>Explored <span class="highlight">Dropshipping Business Model</span></li>
                    <li>Created & managed motivational content page</li>
                    <li>Currently building personal content platform</li>
                </ul>
            </div>
            <div class="card">
                <h3>Personal Development</h3>
                <p>Focused on <span class="highlight">self-development</span> and <span class="highlight">fitness transformation</span>. Committed to building sustainable habits for long-term success.</p>
            </div>
        </div>
    </section>

    <!-- Achievements Section -->
    <section id="achievements" class="section fade-in">
        <h2 class="section-title"><i class="fas fa-trophy"></i> Achievements</h2>
        <div style="max-width: 600px; margin: 0 auto;">
            <ul class="achievements-list">
                <li><i class="fas fa-medal" style="color: #d4af37; margin-right: 0.5rem;"></i>Class 8: <span class="highlight">2nd Position</span></li>
                <li><i class="fas fa-medal" style="color: #d4af37; margin-right: 0.5rem;"></i>Class 6 & 9: <span class="highlight">3rd Position</span></li>
                <li><i class="fas fa-medal" style="color: #d4af37; margin-right: 0.5rem;"></i>Class 6: <span class="highlight">5th Position</span></li>
            </ul>
        </div>
    </section>

    <!-- Languages & Interests -->
    <section id="languages" class="section fade-in">
        <h2 class="section-title"><i class="fas fa-globe"></i> Languages & Interests</h2>
        <div class="content-grid">
            <div class="card">
                <h3>Languages</h3>
                <ul class="skills-list">
                    <li><i class="fas fa-check-circle" style="color: #d4af37;"></i> Hindi (Fluent)</li>
                   
