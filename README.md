<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Augusto Carlos · Full Stack & Odoo Developer</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(145deg, #f6f9fc 0%, #eef2f5 100%);
            font-family: 'Inter', sans-serif;
            color: #1e2a3e;
            line-height: 1.5;
            padding: 2rem 1.5rem;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            background: white;
            border-radius: 2rem;
            box-shadow: 0 25px 45px -12px rgba(0, 0, 0, 0.2);
            overflow: hidden;
            transition: all 0.2s ease;
        }

        /* header com gradiente */
        .hero {
            background: linear-gradient(135deg, #0b2b3b 0%, #1c4e6e 100%);
            padding: 2.5rem 2rem;
            color: white;
            text-align: center;
        }

        .hero h1 {
            font-size: 2.8rem;
            font-weight: 700;
            letter-spacing: -0.5px;
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            flex-wrap: wrap;
        }

        .hero h1 i {
            font-size: 2.4rem;
            color: #ffd966;
        }

        .hero .tagline {
            font-size: 1.2rem;
            font-weight: 400;
            opacity: 0.9;
            background: rgba(255,255,255,0.15);
            display: inline-block;
            padding: 0.4rem 1.2rem;
            border-radius: 40px;
            backdrop-filter: blur(2px);
            margin-top: 0.8rem;
        }

        .badge-group {
            margin-top: 1.5rem;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 12px;
        }

        .badge {
            background: rgba(255,255,255,0.2);
            backdrop-filter: blur(4px);
            padding: 0.4rem 1rem;
            border-radius: 40px;
            font-size: 0.85rem;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .badge i {
            font-size: 0.9rem;
        }

        /* conteúdo principal */
        .content {
            padding: 2rem 2rem 2.5rem;
        }

        .about-section {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            margin-bottom: 2.5rem;
            border-bottom: 1px solid #e2e8f0;
            padding-bottom: 2rem;
        }

        .about-text {
            flex: 2;
        }

        .about-text h2, .tech h2, .contact h2 {
            font-size: 1.6rem;
            font-weight: 600;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 10px;
            color: #0f3b4f;
            border-left: 5px solid #2c7da0;
            padding-left: 1rem;
        }

        .about-text p {
            margin-bottom: 0.9rem;
            font-size: 1rem;
            color: #2d3e50;
        }

        .about-text ul {
            list-style: none;
            margin-top: 1rem;
        }

        .about-text li {
            margin-bottom: 0.6rem;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .about-text li i {
            width: 24px;
            color: #2c7da0;
            font-size: 1.2rem;
        }

        .gif-side {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            background: #f8fafc;
            border-radius: 28px;
            padding: 1rem;
            box-shadow: 0 8px 20px rgba(0,0,0,0.03);
        }

        .gif-side img {
            max-width: 100%;
            height: auto;
            border-radius: 20px;
            transition: transform 0.2s;
        }

        .gif-side img:hover {
            transform: scale(1.02);
        }

        /* tech stack */
        .tech {
            margin-bottom: 2.5rem;
        }

        .tech-icons {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1.2rem;
            background: #f9fbfd;
            padding: 1.5rem;
            border-radius: 2rem;
            margin-top: 1rem;
        }

        .tech-icons .icon-card {
            background: white;
            border-radius: 1.5rem;
            padding: 0.7rem 1rem;
            box-shadow: 0 5px 12px rgba(0,0,0,0.05);
            transition: all 0.25s;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
            min-width: 80px;
        }

        .tech-icons .icon-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 15px 25px -10px rgba(0,0,0,0.1);
        }

        .tech-icons img {
            width: 42px;
            height: 42px;
            object-fit: contain;
        }

        .tech-icons span {
            font-size: 0.75rem;
            font-weight: 500;
            color: #1f4e6e;
        }

        /* contatos */
        .contact {
            background: #eef3f7;
            border-radius: 1.5rem;
            padding: 1.5rem 2rem;
        }

        .contact-info {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
            margin-top: 1rem;
        }

        .contact-card {
            background: white;
            border-radius: 1.2rem;
            padding: 1rem 1.8rem;
            display: flex;
            align-items: center;
            gap: 14px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.02);
            transition: all 0.2s;
            border: 1px solid #dce5ec;
        }

        .contact-card i {
            font-size: 1.8rem;
            color: #1e6f5c;
        }

        .contact-card a, .contact-card span {
            font-weight: 500;
            color: #1e2a3e;
            text-decoration: none;
        }

        .contact-card:hover {
            transform: scale(1.02);
            border-color: #90b8cf;
        }

        footer {
            text-align: center;
            font-size: 0.8rem;
            color: #6c7e8f;
            border-top: 1px solid #e2edf2;
            padding: 1.5rem 2rem;
            background: #ffffff;
        }

        @media (max-width: 720px) {
            .hero h1 { font-size: 2rem; }
            .content { padding: 1.5rem; }
            .tech-icons .icon-card { min-width: 65px; padding: 0.5rem; }
            .contact-card { width: 100%; justify-content: center; }
        }
    </style>
</head>
<body>
<div class="container">
    <div class="hero">
        <h1>
            <i class="fas fa-code"></i> 
            Augusto Carlos
            <i class="fas fa-laptop-code"></i>
        </h1>
        <div class="tagline">
            Full Stack Developer · Odoo Specialist · Scalable Solutions
        </div>
        <div class="badge-group">
            <span class="badge"><i class="fab fa-python"></i> Python</span>
            <span class="badge"><i class="fab fa-php"></i> PHP / Laravel</span>
            <span class="badge"><i class="fab fa-java"></i> Java / Spring</span>
            <span class="badge"><i class="fas fa-cubes"></i> Odoo ERP</span>
        </div>
    </div>

    <div class="content">
        <div class="about-section">
            <div class="about-text">
                <h2><i class="fas fa-user-astronaut"></i> Sobre mim</h2>
                <p>👨‍💻 <strong>Full Stack Developer</strong> com experiência em aplicações web modernas e responsivas usando <strong>HTML, CSS, JavaScript, PHP, Laravel, MySQL e Bootstrap</strong>.</p>
                <p>🏢 Especialista <strong>Odoo Software Developer</strong> (Python): personalização, integração e desenvolvimento de soluções ERP que impulsionam a eficiência de negócios.</p>
                <p>🚀 Foco em backends robustos com Laravel e frontends limpos e intuitivos. Apaixonado por arquitetura escalável e boas práticas.</p>
                <ul>
                    <li><i class="fas fa-graduation-cap"></i> Aprendiz constante — sempre evoluindo em web, ERP e novas tecnologias.</li>
                    <li><i class="fas fa-handshake"></i> Aberto a colaborar em projetos inovadores que gerem valor real.</li>
                    <li><i class="fas fa-globe"></i> Tecnologia que transforma vidas é a minha motivação.</li>
                </ul>
            </div>
            <div class="gif-side">
                <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExYzI5YzA5ZDU4YzI0ZDNlNzM0YzE4OTc5N2QzYzI0N2Q0NmNmYzA5OCZlcD12MV9pbnRlcm5hbF9naWZzX2dpZklkJmN0PWc/bGgsc5mWoryfgKBK1x/giphy.gif" 
                     alt="coding gif" 
                     onerror="this.src='https://media.giphy.com/media/26tn33aiTi1jkl6H6/giphy.gif'">
            </div>
        </div>

        <div class="tech">
            <h2><i class="fas fa-microchip"></i> Tech Stack & Ferramentas</h2>
            <div class="tech-icons">
                <div class="icon-card"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5"><span>HTML5</span></div>
                <div class="icon-card"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS3"><span>CSS3</span></div>
                <div class="icon-card"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JS"><span>JavaScript</span></div>
                <div class="icon-card"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" alt="Bootstrap"><span>Bootstrap</span></div>
                <div class="icon-card"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" alt="PHP"><span>PHP</span></div>
                <div class="icon-card"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" alt="MySQL"><span>MySQL</span></div>
                <div class="icon-card"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-original.svg" alt="Laravel"><span>Laravel</span></div>
                <div class="icon-card"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="Python"><span>Python</span></div>
                <div class="icon-card"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" alt="Java"><span>Java</span></div>
                <div class="icon-card"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg" alt="Spring"><span>Spring Boot</span></div>
                <div class="icon-card"><img src="https://cdn.worldvectorlogo.com/logos/odoo.svg" alt="Odoo" style="width:42px;"><span>Odoo</span></div>
            </div>
        </div>

        <div class="contact">
            <h2><i class="fas fa-address-card"></i> Vamos conectar?</h2>
            <div class="contact-info">
                <div class="contact-card">
                    <i class="fas fa-envelope"></i>
                    <a href="mailto:augustoaccarlos@gmail.com">augustoaccarlos@gmail.com</a>
                </div>
                <div class="contact-card">
                    <i class="fas fa-phone-alt"></i>
                    <span>+244 959 361 115</span>
                </div>
                <div class="contact-card">
                    <i class="fab fa-github"></i>
                    <a href="#">github/augustocarlos</a> <span style="font-size:0.7rem;">(em breve)</span>
                </div>
                <div class="contact-card">
                    <i class="fab fa-linkedin"></i>
                    <a href="#">LinkedIn</a>
                </div>
            </div>
        </div>
    </div>

    <footer>
        ✨ <em>“Technology is best when it brings people together.”</em> — Sempre construindo soluções que unem negócios e pessoas.
    </footer>
</div>
</body>
</html>
