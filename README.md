# My-portfolio-
It contains html,css and JavaScript 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alex Rivera · interactive portfolio</title>
    <!-- Font Awesome 6 (free) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>


        .hero-content h1 {
            font-size: 3.5rem;
            font-weight: 700;
            line-height: 1.2;
           * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
        }

        body {
            background: #f5f7fb;
            color: #1e1e2f;
            line-height: 1.5;
            scroll-behavior: smooth;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem 2rem;
        }

        /* header / nav */


        .nav-links a {
           .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.2rem 2rem;
            background: rgba(255,255,255,0.75);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.02);
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid rgba(230,232,240,0.6);
        }

        .logo {
            font-weight: 700;
            font-size: 1.7rem;
            letter-spacing: -0.5px;
            background: linear-gradient(145deg, #1f1f3a, #3a3a6e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .nav-links {
            display: flex;
            gap: 2.2rem;
            font-weight: 500;
        } text-decoration: none;
            color: #2b2b4f;
            transition: 0.2s;
            font-size: 1.05rem;
            border-bottom: 2px solid transparent;
            padding-bottom: 4px;
        }

        .nav-links a:hover {
            border-bottom-color: #5c5cbc;
            color: #1e1e3f;
        }

        /* buttons / tags */
        .btn-outline {
            display: inline-block;
            padding: 0.5rem 1.2rem;
            border-radius: 40px;
            border: 1.5px solid #cfd1e2;
            background: transparent;
            font-weight: 500;
            transition: 0.2s;
            text-decoration: none;
            color: #2e2e4a;
        }

        .btn-outline:hover {
            border-color: #6b6bc9;
            background: #ffffff;
            box-shadow: 0 4px 10px rgba(0,0,0,0.02);
        }

        .btn-primary {
            background: #2d2d5a;
            color: white;
            border: none;
            padding: 0.8rem 2rem;
            border-radius: 40px;
            font-weight: 600;
            font-size: 1rem;
            cursor: pointer;
            transition: 0.2s;
            text-decoration: none;
            display: inline-block;
            box-shadow: 0 8px 18px rgba(45,45,90,0.15);
        }

        .btn-primary:hover {
            background: #3f3f7a;
            transform: translateY(-3px);
            box-shadow: 0 14px 24px rgba(45,45,90,0.2);
        }

        /* hero */
        .hero {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 2rem;
            margin: 1.5rem 0 3rem 0;
        }

        .hero-content {
            flex: 1 1 350px;
        }

        .hero-badge {
            background: #e7e7ff;
            color: #3d3d75;
            padding: 0.25rem 1rem;
            border-radius: 40px;
            display: inline-block;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
            border: 1px solid #cdcdf0;
        }     letter-spacing: -1px;
            background: linear-gradient(145deg, #1b1b3a, #41417e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-highlight {
            color: #2d2d68;
            background: linear-gradient(145deg, #3e3e7a, #6363b0);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-desc {
            font-size: 1.2rem;
            color: #45455f;
            max-width: 500px;
            margin: 1.5rem 0 2rem;
        }

        .hero-avatar {
            flex: 0 0 280px;
            height: 280px;
            background: linear-gradient(135deg, #cdd1f0, #b1b6e0);
            border-radius: 42% 58% 70% 30% / 44% 36% 64% 56%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 20px 25px 40px rgba(55, 55, 100, 0.2);
            transition: 1s ease-in-out;
            animation: float 6s infinite alternate;
        }

        .hero-avatar i {
            font-size: 8rem;
            color: white;
            text-shadow: 0 10px 15px rgba(0,0,0,0.1);
        }

        @keyframes float {
            0% { border-radius: 42% 58% 70% 30% / 44% 36% 64% 56%; transform: translateY(0); }
            100% { border-radius: 58% 42% 40% 60% / 50% 58% 42% 50%; transform: translateY(-15px); }
        }

        /* section headings */
        .section-head {
            font-size: 2.2rem;
            font-weight: 650;
            letter-spacing: -0.5px;
            margin: 3rem 0 1.5rem 0;
            color: #20203a;
            display: flex;
            align-items: center;
            gap: 0.8rem;
        }

        .section-head i {
            color: #4b4b9a;
            font-size: 2rem;
        }

        /* project cards */
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 1rem;
        }

        .project-card {
            background: white;
            border-radius: 2rem;
            padding: 1.8rem 1.5rem;
            box-shadow: 0 20px 35px -8px rgba(30,30,60,0.1);
            transition: all 0.25s;
            border: 1px solid rgba(230,232,250,0.6);
            backdrop-filter: blur(4px);
            display: flex;
            flex-direction: column;
        }

        .project-card:hover {
            transform: scale(1.02) translateY(-8px);
            border-color: #b7b7e5;
            box-shadow: 0 32px 45px -8px rgba(45,45,90,0.2);
        }

        .project-icon {
            font-size: 2.2rem;
            background: #efefff;
            width: 60px;
            height: 60px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #3f3f87;
            margin-bottom: 1.2rem;
        }

        .project-card h3 {
            font-size: 1.6rem;
            font-weight: 650;
            margin-bottom: 0.5rem;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem;
            margin: 1rem 0 1.2rem;
        }

        .tag {
            background: #eaeefc;
            color: #2c2c68;
            padding: 0.2rem 1rem;
            border-radius: 30px;
            font-size: 0.8rem;
            font-weight: 600;
            border: 1px solid #c7c7f0;
        }

        .project-link {
            margin-top: auto;
            font-weight: 600;
            text-decoration: none;
            color: #2b2b78;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .project-link i {
            transition: transform 0.2s;
        }

        .project-link:hover i {
            transform: translateX(6px);
        }

        /* skills / tools */
        .skills-cloud {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem 1.2rem;
            background: rgba(255,255,255,0.6);
            backdrop-filter: blur(6px);
            border-radius: 60px;
            padding: 2rem 2.2rem;
            border: 1px solid white;
            box-shadow: 0 20px 30px rgba(0,0,0,0.02);
            margin: 1.5rem 0 1rem;
        }

        .skill-item {
            background: white;
            padding: 0.8rem 1.8rem;
            border-radius: 40px;
            font-weight: 600;
            color: #25254b;
            box-shadow: 0 6px 16px rgba(0,0,0,0.02);
            border: 1px solid #e2e2f0;
            transition: 0.15s;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill-item i {
            color: #4f4faa;
            font-size: 1.2rem;
        }

        .skill-item:hover {
            background: #272751;
            color: white;
            border-color: #272751;
        }
        .skill-item:hover i {
            color: white;
        }

        /* contact & footer */
        .contact-section {
            background: white;
            border-radius: 4rem 4rem 2rem 2rem;
            padding: 3rem 2.5rem;
            margin-top: 3.5rem;
            box-shadow: 0 -10px 30px rgba(0,0,0,0.02);
            border: 1px solid #edf0fa;
        }

        .contact-flex {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 2rem;
        }

        .contact-text h2 {
            font-size: 2.2rem;
            font-weight: 700;
            color: #1e1e3a;
        }

        .social-links {
            display: flex;
            gap: 1.8rem;
        }

        .social-links a {
            color: #34346e;
            font-size: 2rem;
            transition: 0.15s;
        }

        .social-links a:hover {
            color: #5b5bb3;
            transform: scale(1.15);
        }

        .footer-bottom {
            text-align: center;
            margin-top: 3rem;
            color: #5f5f82;
            font-size: 0.95rem;
            border-top: 1px dashed #cfd1e8;
            padding-top: 2rem;
        }

        hr {
            border: none;
            border-top: 1px solid #d9dcf0;
            margin: 1rem 0;
        }

        /* responsive */
        @media (max-width: 700px) {
            .navbar {
                flex-direction: column;
                gap: 0.7rem;
            }
            .hero-content h1 {
                font-size: 2.5rem;
            }
            .hero-avatar {
                flex-basis: 200px;
                height: 200px;
            }
            .section-head {
                font-size: 1.9rem;
            }
        }
    </style>
</head>
<body>
    <nav class="navbar">
        <span class="logo">✨ alex.dev</span>
        <div class="nav-links">
            <a href="#work">work</a>
            <a href="#skills">stack</a>
            <a href="#contact">contact</a>
            <a href="#" class="btn-outline"><i class="far fa-file-pdf" style="margin-right: 6px;"></i>resume</a>
        </div>
    </nav>

    <main class="container">
        <!-- hero section -->
        <div class="hero" id="home">
            <div class="hero-content">
                <span class="hero-badge"><i class="fas fa-cube" style="margin-right: 6px;"></i> product engineer</span>
                <h1>crafting digital <span class="hero-highlight">experiences</span> with soul</h1>
                <p class="hero-desc">I'm Alex Rivera — designer & front-end architect. I build products that are fast, fluid, and human.</p>
                <a href="#work" class="btn-primary"><i class="fas fa-arrow-down" style="margin-right: 8px;"></i>see projects</a>
                <span style="margin-left: 1.2rem;"><i class="fas fa-map-pin" style="color: #5a5aaf;"></i> NYC · remote</span>
            </div>
            <div class="hero-avatar">
                <i class="fas fa-paint-brush"></i>
            </div>
        </div>

        <!-- work / projects section -->
        <div id="work"></div>
        <div class="section-head">
            <i class="fas fa-code-branch"></i> 
            <span>selected projects</span>
        </div>

        <div class="project-grid">
            <!-- card 1 -->
            <div class="project-card">
                <div class="project-icon"><i class="fas fa-chart-line"></i></div>
                <h3>finwise</h3>
                <p>AI‑powered dashboard for personal finance. Visualized complex data with smooth canvas animations.</p>
                <div class="project-tags">
                    <span class="tag">react</span>
                    <span class="tag">d3</span>
                    <span class="tag">express</span>
                </div>
                <a href="#" class="project-link">live preview <i class="fas fa-arrow-right"></i></a>
            </div>
            <!-- card 2 -->
            <div class="project-card">
                <div class="project-icon"><i class="fas fa-seedling"></i></div>
              <h3>eden</h3>
                <p>Sustainable marketplace for local growers. Includes real‑time chat and geolocation.It provides quality products</p>
                <div class="project-tags">
                    <span class="tag">vue</span>
                    <span class="tag">tailwind</span>
                    <span class="tag">firebase</span>
                </div>
                <a href="#" class="project-link">live preview <i class="fas fa-arrow-right"></i></a>
            </div>
            <!-- card 3 -->
            <div class="project-card">
                <div class="project-icon"><i class="fas fa-mask"></i></div>
                <h3>morph</h3>
                <p>Generative avatars and identity layers. Experiment with WebGL and GLSL shaders.</p>
                <div class="project-tags">
                    <span class="tag">three.js</span>
                    <span class="tag">webgl</span>
                    <span class="tag">figma</span>
                </div>
                <a href="#" class="project-link">live preview <i class="fas fa-arrow-right"></i></a>
            </div>
            <!-- card 4 extra (more dynamic) -->
            <div class="project-card">
                <div class="project-icon"><i class="fas fa-brain"></i></div>
                <h3>context</h3>
                <p>Collaborative whiteboard with spatial reasoning. Real‑time sync & infinite canvas.</p>
                <div class="project-tags">
                    <span class="tag">react</span>
                    <span class="tag">socket.io</span>
                    <span class="tag">p5js</span>
                </div>
                <a href="#" class="project-link">case study <i class="fas fa-arrow-right"></i></a>
            </div>
        </div>

        <!-- skills / tech stack -->
        <div id="skills"></div>
        <div class="section-head" style="margin-top: 4rem;">
            <i class="fas fa-cog"></i>
            <span>toolbox & technologies</span>
        </div>

        <div class="skills-cloud">
            <span class="skill-item"><i class="fab fa-react"></i> react</span>
            <span class="skill-item"><i class="fab fa-vuejs"></i> vue</span>
            <span class="skill-item"><i class="fab fa-js"></i> typescript</span>
            <span class="skill-item"><i class="fab fa-node"></i> node.js</span>
            <span class="skill-item"><i class="fas fa-database"></i> mongoDB</span>
            <span class="skill-item"><i class="fab fa-figma"></i> figma</span>
            <span class="skill-item"><i class="fas fa-code"></i> python</span>
            <span class="skill-item"><i class="fas fa-cloud"></i> firebase</span>
            <span class="skill-item"><i class="fas fa-mobile-alt"></i> responsive</span>
            <span class="skill-item"><i class="fas fa-cubes"></i> three.js</span>
            <span class="skill-item"><i class="fas fa-paint-brush"></i> illustration</span>
        </div>

        <!-- contact & footer area -->
        <div id="contact" class="contact-section">
            <div class="contact-flex">
                <div class="contact-text">
                    <h2>let's connect <i class="fas fa-hand-peace" style="color: #4d4daa;"></i></h2>
                    <p style="color: #4f4f73; max-width: 400px; margin-top: 0.5rem;">Open for collaborations, creative builds, or just a nice chat.</p>
                    <div style="margin-top: 1.4rem;">
                        <a href="mailto:alex.r@example.com" class="btn-primary" style="background: transparent; color: #2f2f62; border: 2px solid #b3b3e0; box-shadow: none;">alex.r@example.com</a>
                    </div>
                </div>
                <div class="social-links">
                    <a href="#" aria-label="GitHub"><i class="fab fa-github"></i></a>
                    <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#" aria-label="Dribbble"><i class="fab fa-dribbble"></i></a>
                    <a href="#" aria-label="X / Twitter"><i class="fab fa-x-twitter"></i></a>
                </div>
            </div>
            <hr>
            <div class="footer-bottom">
                <span>© 2026 Alex Rivera – built with <i class="fas fa-heart" style="color: #b25b8c;"></i> for the web</span>
                <span style="display: block; margin-top: 0.3rem; font-size: 0.85rem;">
                    <i class="far fa-clock"></i> NYC time · available for work
                </span>
            </div>
        </div>
    </main>
</body>
<script>
    const links=linksdocument.queryselectorAll(
        'click' ,()=>{
            console.log('social link clinked');   
        });
</script>
</html>