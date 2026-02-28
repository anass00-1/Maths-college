# Maths-college
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Maths Collège 001 - Cours de Maths</title>
    <!-- Importation d'une police moderne -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <!-- Icônes Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* ========== CSS - LE STYLE DU SITE ========== */
        
        /* Variables de couleurs */
        :root {
            --primary-color: #FF0000; /* Rouge YouTube */
            --primary-dark: #cc0000;
            --dark-bg: #0f0f0f;
            --light-bg: #f9f9f9;
            --white: #ffffff;
            --text-dark: #1f1f1f;
            --text-gray: #666666;
            --card-shadow: 0 4px 20px rgba(0,0,0,0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--light-bg);
            color: var(--text-dark);
            line-height: 1.7;
        }

        a {
            text-decoration: none;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* ========== HEADER / HERO ========== */
        header {
            background: linear-gradient(135deg, #0f0f0f 0%, #1a1a1a 100%);
            color: var(--white);
            padding: 80px 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,0,0,0.1) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .header-content {
            position: relative;
            z-index: 2;
        }

        .channel-icon {
            width: 140px;
            height: 140px;
            border-radius: 50%;
            border: 4px solid var(--primary-color);
            object-fit: cover;
            margin-bottom: 20px;
            box-shadow: 0 0 30px rgba(255,0,0,0.3);
        }

        header h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            font-weight: 700;
        }

        header .tagline {
            font-size: 1.2rem;
            color: #aaa;
            margin-bottom: 30px;
        }

        .btn-subscribe {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background-color: var(--primary-color);
            color: var(--white);
            padding: 15px 35px;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(255,0,0,0.4);
        }

        .btn-subscribe:hover {
            background-color: var(--primary-dark);
            transform: translateY(-3px);
            box-shadow: 0 6px 25px rgba(255,0,0,0.5);
        }

        .btn-subscribe i {
            font-size: 1.4rem;
        }

        /* ========== STATS BAR ========== */
        .stats-bar {
            background: var(--white);
            padding: 30px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }

        .stats-grid {
            display: flex;
            justify-content: center;
            gap: 60px;
            flex-wrap: wrap;
        }

        .stat-item {
            text-align: center;
        }

        .stat-number {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary-color);
        }

        .stat-label {
            color: var(--text-gray);
            font-size: 0.9rem;
        }

        /* ========== ABOUT SECTION ========== */
        .about {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            margin-bottom: 50px;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: var(--primary-color);
            margin: 15px auto 0;
            border-radius: 2px;
        }

        .about-content {
            background: var(--white);
            padding: 40px;
            border-radius: 20px;
            box-shadow: var(--card-shadow);
            max-width: 900px;
            margin: 0 auto;
            text-align: center;
        }

        .about-content p {
            font-size: 1.1rem;
            color: var(--text-gray);
            margin-bottom: 20px;
        }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .feature {
            text-align: center;
            padding: 20px;
        }

        .feature i {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 15px;
        }

        .feature h3 {
            margin-bottom: 10px;
        }

        /* ========== VIDEOS SECTION ========== */
        .videos {
            padding: 80px 0;
            background: var(--white);
        }

        .video-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
            margin-bottom: 50px;
        }

        .video-card {
            background: var(--light-bg);
            border-radius: 15px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .video-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--card-shadow);
        }

        .video-thumbnail {
            position: relative;
            padding-bottom: 56.25%; /* 16:9 ratio */
            height: 0;
            overflow: hidden;
        }

        .video-thumbnail iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }

        .video-info {
            padding: 20px;
        }

        .video-info h3 {
            font-size: 1rem;
            margin-bottom: 10px;
            line-height: 1.4;
        }

        .video-meta {
            display: flex;
            justify-content: space-between;
            color: var(--text-gray);
            font-size: 0.85rem;
        }

        .center-btn {
            text-align: center;
        }

        .btn-all-videos {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: var(--dark-bg);
            color: var(--white);
            padding: 15px 30px;
            border-radius: 50px;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .btn-all-videos:hover {
            background: var(--primary-color);
        }

        /* ========== RESOURCES SECTION ========== */
        .resources {
            padding: 80px 0;
        }

        .resources-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .resource-card {
            background: var(--white);
            padding: 30px;
            border-radius: 15px;
            box-shadow: var(--card-shadow);
            text-align: center;
            transition: transform 0.3s ease;
        }

        .resource-card:hover {
            transform: translateY(-5px);
        }

        .resource-card i {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }

        .resource-card h3 {
            margin-bottom: 15px;
        }

        .resource-card p {
            color: var(--text-gray);
            margin-bottom: 20px;
        }

        .resource-btn {
            display: inline-block;
            padding: 10px 25px;
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
            border-radius: 25px;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .resource-btn:hover {
            background: var(--primary-color);
            color: var(--white);
        }

        /* ========== CONTACT SECTION ========== */
        .contact {
            padding: 80px 0;
            background: linear-gradient(135deg, #1a1a1a 0%, #0f0f0f 100%);
            color: var(--white);
        }

        .contact-content {
            text-align: center;
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-content h2 {
            margin-bottom: 20px;
        }

        .contact-content p {
            color: #aaa;
            margin-bottom: 30px;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .social-link {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 15px 25px;
            background: rgba(255,255,255,0.1);
            border-radius: 50px;
            color: var(--white);
            transition: all 0.3s ease;
        }

        .social-link:hover {
            background: var(--primary-color);
            transform: translateY(-3px);
        }

        /* ========== FOOTER ========== */
        footer {
            background: #0a0a0a;
            color: #666;
            text-align: center;
            padding: 30px 0;
        }

        footer p {
            margin-bottom: 10px;
        }

        /* ========== RESPONSIVE ========== */
        @media (max-width: 768px) {
            header h1 {
                font-size: 2rem;
            }
            
            .stats-grid {
                gap: 30px;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
            
            .video-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <!-- HEADER -->
    <header>
        <div class="container header-content">
            <!-- Remplacez le src par l'URL de votre photo de profil YouTube -->
            <img src="https://yt3.googleusercontent.com/ytc/APkrFKZ5G6p_YQKuJ0pHr0jM5JzKc3eJ9xjVJ1U0qGJJEng=s176-c-k-c0x00ffffff-no-rj" 
                 alt="Maths Collège 001" class="channel-icon">
            
            <h1>Maths Collège 001</h1>
            <p class="tagline">Cours de mathématiques clairs et gratuits pour tous les niveaux du collège</p>
            
            <a href="https://www.youtube.com/@Mathscoll%C3%A8ge001?sub_confirmation=1" target="_blank" class="btn-subscribe">
                <i class="fab fa-youtube"></i> S'abonner à la chaîne
            </a>
        </div>
    </header>

    <!-- STATS -->
    <div class="stats-bar">
        <div class="container">
            <div class="stats-grid">
                <div class="stat-item">
                    <div class="stat-number">+200</div>
                    <div class="stat-label">Abonnés</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">20+</div>
                    <div class="stat-label">Vidéos</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">5K+</div>
                    <div class="stat-label">Vues totales</div>
                </div>
            </div>
        </div>
    </div>

    <!-- À PROPOS -->
    <section class="about">
        <div class="container">
            <h2 class="section-title">À propos de la chaîne</h2>
            <div class="about-content">
                <p>
                    Bienvenue sur <strong>Maths Collège 001</strong> ! Je suis professeur de mathématiques et je propose 
                    des cours vidéo gratuits et clairs pour les élèves de la 6ème à la 3ème.
                </p>
                <p>
                    Mon objectif : rendre les maths accessibles à tous avec des explications simples et adaptées au programme scolaire français.
                </p>
                
                <div class="features">
                    <div class="feature">
                        <i class="fas fa-graduation-cap"></i>
                        <h3>Programme officiel</h3>
                        <p>Conforme aux programmes de l'Éducation Nationale</p>
                    </div>
                    <div class="feature">
                        <i class="fas fa-video"></i>
                        <h3>Cours en vidéo</h3>
                        <p>Explications visuelles claires et détaillées</p>
                    </div>
                    <div class="feature">
                        <i class="fas fa-infinity"></i>
                        <h3>Accès gratuit</h3>
                        <p>Toutes les ressources sont gratuites</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- VIDÉOS -->
    <section class="videos">
        <div class="container">
            <h2 class="section-title">Dernières Vidéos</h2>
            
            <div class="video-grid">
                <!-- Vidéo 1 -->
                <div class="video-card">
                    <div class="video-thumbnail">
                        <iframe src="https://www.youtube.com/embed/videoseries?list=UUVjE-3C5O6NqzFvhENdX8aQ" allowfullscreen></iframe>
                    </div>
                    <div class="video-info">
                        <h3>Cours de mathématiques - Collège</h3>
                        <div class="video-meta">
                            <span><i class="far fa-clock"></i> 15 min</span>
                            <span><i class="far fa-eye"></i> 500 vues</span>
                        </div>
                    </div>
                </div>

                <!-- Vidéo 2 -->
                <div class="video-card">
                    <div class="video-thumbnail">
                        <iframe src="https://www.youtube.com/embed/videoseries?list=UUVjE-3C5O6NqzFvhENdX8aQ" allowfullscreen></iframe>
                    </div>
                    <div class="video-info">
                        <h3>Exercices corrigés</h3>
                        <div class="video-meta">
                            <span><i class="far fa-clock"></i> 20 min</span>
                            <span><i class="far fa-eye"></i> 300 vues</span>
                        </div>
                    </div>
                </div>

                <!-- Vidéo 3 -->
                <div class="video-card">
                    <div class="video-thumbnail">
                        <iframe src="https://www.youtube.com/embed/videoseries?list=UUVjE-3C5O6NqzFvhENdX8aQ" allowfullscreen></iframe>
                    </div>
                    <div class="video-info">
                        <h3>Méthodes et Astuces</h3>
                        <div class="video-meta">
                            <span><i class="far fa-clock"></i> 10 min</span>
                            <span><i class="far fa-eye"></i> 200 vues</span>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="center-btn">
                <a href="https://www.youtube.com/@Mathscoll%C3%A8ge001" target="_blank" class="btn-all-videos">
                    <i class="fab fa-youtube"></i> Voir toutes les vidéos
                </a>
            </div>
        </div>
    </section>

    <!-- RESSOURCES -->
    <section class="resources">
        <div class="container">
            <h2 class="section-title">Ressources</h2>
            
            <div class="resources-grid">
                <div class="resource-card">
                    <i class="fas fa-file-pdf"></i>
                    <h3>Téléchargements</h3>
                    <p>Accédez aux fiches de cours et exercices en PDF</p>
                    <a href="#" class="resource-btn">
