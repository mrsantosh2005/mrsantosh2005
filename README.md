<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Santosh Chintawar - GitHub Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Poppins:wght@300;400;600;700&display=swap');

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #0a0a2a 0%, #1a1a3e 100%);
            color: #ffffff;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Animated Background */
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }

        .star {
            position: absolute;
            background: white;
            border-radius: 50%;
            animation: twinkle 3s infinite;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.3; transform: scale(1); }
            50% { opacity: 1; transform: scale(1.2); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 1;
        }

        /* Glassmorphism Effect */
        .glass-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            padding: 30px;
            margin: 30px 0;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .glass-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 40px rgba(0, 247, 255, 0.2);
            border-color: rgba(0, 247, 255, 0.5);
        }

        /* Animated Gradient Text */
        .gradient-text {
            background: linear-gradient(45deg, #00F7FF, #8A2BE2, #FF6B6B);
            background-size: 200% 200%;
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: gradientShift 3s ease infinite;
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Tech Stack Icons */
        .tech-icons {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }

        .tech-icon {
            animation: float 3s ease-in-out infinite;
            transition: transform 0.3s ease;
        }

        .tech-icon:hover {
            transform: scale(1.2) rotate(5deg);
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        /* Project Cards */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }

        .project-card {
            background: linear-gradient(135deg, rgba(0, 247, 255, 0.1), rgba(138, 43, 226, 0.1));
            border-radius: 15px;
            padding: 25px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(0,247,255,0.1), transparent);
            transform: rotate(45deg);
            animation: shimmer 3s infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%) rotate(45deg); }
            100% { transform: translateX(100%) rotate(45deg); }
        }

        .project-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 40px rgba(0, 247, 255, 0.3);
        }

        /* Stats Container */
        .stats-container {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin: 40px 0;
        }

        .stat-card {
            background: rgba(0, 0, 0, 0.3);
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            transform: scale(1.05);
            background: rgba(0, 247, 255, 0.1);
        }

        /* Social Links */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 30px 0;
        }

        .social-icon {
            width: 60px;
            height: 60px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
            animation: pulse 2s infinite;
        }

        .social-icon:hover {
            transform: scale(1.1);
            background: rgba(0, 247, 255, 0.3);
            box-shadow: 0 0 20px rgba(0, 247, 255, 0.5);
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        /* Typing Animation */
        .typing-container {
            text-align: center;
            margin: 50px 0;
        }

        .typing-text {
            font-size: 2rem;
            font-weight: bold;
            font-family: 'Orbitron', monospace;
        }

        /* Progress Bars */
        .progress-bar {
            width: 100%;
            height: 10px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 5px;
            overflow: hidden;
            margin: 10px 0;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #00F7FF, #8A2BE2);
            border-radius: 5px;
            animation: fillProgress 2s ease-out;
        }

        @keyframes fillProgress {
            from { width: 0; }
            to { width: var(--width); }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .typing-text {
                font-size: 1.2rem;
            }
            
            .glass-card {
                padding: 20px;
            }
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }

        ::-webkit-scrollbar-track {
            background: #0a0a2a;
        }

        ::-webkit-scrollbar-thumb {
            background: linear-gradient(45deg, #00F7FF, #8A2BE2);
            border-radius: 5px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(45deg, #8A2BE2, #00F7FF);
        }
    </style>
</head>
<body>
    <div class="stars" id="stars"></div>
    
    <div class="container">
        <!-- Header Section -->
        <div class="glass-card" style="text-align: center;">
            <div class="typing-container">
                <div class="typing-text" id="typing-text"></div>
            </div>
            <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00F7FF,100:8A2BE2&height=200&section=header&text=Santosh%20Chintawar&fontSize=45&fontColor=ffffff&animation=fadeIn&fontAlignY=35" style="width: 100%; margin: 20px 0;">
            <p align="center">
                <img src="https://komarev.com/ghpvc/?username=SantoshChintawar&label=PROFILE+VIEWS&color=blueviolet&style=for-the-badge"/>
            </p>
        </div>

        <!-- About Me Section -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2.5rem; margin-bottom: 20px;">🌟 About Me</h1>
            <div style="display: flex; flex-wrap: wrap; gap: 30px; align-items: center;">
                <div style="flex: 1;">
                    <img src="https://media.giphy.com/media/f3iwJFOVOwuy7K6FFw/giphy.gif" style="width: 100%; max-width: 300px; border-radius: 20px;">
                </div>
                <div style="flex: 2;">
                    <p style="font-size: 1.2rem; margin-bottom: 15px;">✨ Passionate Full Stack MERN Developer</p>
                    <p style="font-size: 1.2rem; margin-bottom: 15px;">🚀 Building Real World Applications</p>
                    <p style="font-size: 1.2rem; margin-bottom: 15px;">☁️ Learning AWS & Cloud Technologies</p>
                    <p style="font-size: 1.2rem; margin-bottom: 15px;">🤖 Interested in AI & Automation</p>
                    <p style="font-size: 1.2rem; margin-bottom: 15px;">💻 Love solving real-world problems with code</p>
                    <p style="font-size: 1.2rem;">🔥 Always learning new technologies</p>
                </div>
            </div>
        </div>

        <!-- Social Links -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2rem; text-align: center; margin-bottom: 30px;">🌐 Connect With Me</h1>
            <div class="social-links">
                <a href="https://linkedin.com/in/santosh-chintawar" class="social-icon">
                    <img src="https://skillicons.dev/icons?i=linkedin" width="40">
                </a>
                <a href="https://github.com/SantoshChintawar" class="social-icon">
                    <img src="https://skillicons.dev/icons?i=github" width="40">
                </a>
                <a href="mailto:santoshchintawar@gmail.com" class="social-icon">
                    <img src="https://skillicons.dev/icons?i=gmail" width="40">
                </a>
            </div>
        </div>

        <!-- Tech Stack -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2rem; text-align: center; margin-bottom: 30px;">⚡ Tech Stack</h1>
            <div class="tech-icons">
                <img src="https://skillicons.dev/icons?i=mongodb,express,react,nodejs,java,js,html,css,spring,mysql,git,github,aws,vscode,postman" class="tech-icon" style="width: 60px;">
            </div>
        </div>

        <!-- Featured Projects -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2rem; text-align: center; margin-bottom: 30px;">🚀 Featured Projects</h1>
            <div class="projects-grid">
                <div class="project-card">
                    <h2 style="color: #00F7FF; margin-bottom: 15px;">🅿️ Smart Parking Platform</h2>
                    <p>🚗 Smart parking management system</p>
                    <p>📍 Find nearby parking slots</p>
                    <p>💳 Online parking booking</p>
                    <p>📊 Parking dashboard</p>
                    <p>⚡ Real-time slot availability</p>
                    <div style="margin-top: 20px;">
                        <span style="background: rgba(0,247,255,0.2); padding: 5px 10px; border-radius: 5px; margin-right: 10px;">React.js</span>
                        <span style="background: rgba(0,247,255,0.2); padding: 5px 10px; border-radius: 5px; margin-right: 10px;">Spring Boot</span>
                        <span style="background: rgba(0,247,255,0.2); padding: 5px 10px; border-radius: 5px;">MySQL</span>
                    </div>
                </div>

                <div class="project-card">
                    <h2 style="color: #00F7FF; margin-bottom: 15px;">📄 AI Resume Screening System</h2>
                    <p>🤖 AI-powered Resume Screening Web App</p>
                    <p>📑 Upload & analyze resumes</p>
                    <p>🎯 Smart candidate filtering</p>
                    <p>⚡ Automated skill matching</p>
                    <p>📊 Recruiter dashboard</p>
                    <div style="margin-top: 20px;">
                        <span style="background: rgba(0,247,255,0.2); padding: 5px 10px; border-radius: 5px; margin-right: 10px;">MongoDB</span>
                        <span style="background: rgba(0,247,255,0.2); padding: 5px 10px; border-radius: 5px; margin-right: 10px;">Express.js</span>
                        <span style="background: rgba(0,247,255,0.2); padding: 5px 10px; border-radius: 5px; margin-right: 10px;">React.js</span>
                        <span style="background: rgba(0,247,255,0.2); padding: 5px 10px; border-radius: 5px;">Node.js</span>
                    </div>
                </div>

                <div class="project-card">
                    <h2 style="color: #00F7FF; margin-bottom: 15px;">🏍️ MotoRent India</h2>
                    <p>🏍️ Motorcycle rental platform</p>
                    <p>📍 Browse bikes easily</p>
                    <p>💳 Online booking system</p>
                    <p>📅 Check pricing & availability</p>
                    <p>🔥 User-friendly UI</p>
                    <div style="margin-top: 20px;">
                        <span style="background: rgba(0,247,255,0.2); padding: 5px 10px; border-radius: 5px; margin-right: 10px;">HTML</span>
                        <span style="background: rgba(0,247,255,0.2); padding: 5px 10px; border-radius: 5px; margin-right: 10px;">CSS</span>
                        <span style="background: rgba(0,247,255,0.2); padding: 5px 10px; border-radius: 5px;">JavaScript</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Currently Learning -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2rem; text-align: center; margin-bottom: 30px;">🌱 Currently Learning</h1>
            <div class="tech-icons">
                <img src="https://img.shields.io/badge/AWS-Cloud-orange?style=for-the-badge&logo=amazonaws" class="tech-icon">
                <img src="https://img.shields.io/badge/MERN-Stack-green?style=for-the-badge&logo=mongodb" class="tech-icon">
                <img src="https://img.shields.io/badge/AI-Learning-blue?style=for-the-badge" class="tech-icon">
                <img src="https://img.shields.io/badge/Open%20Source-Contributor-purple?style=for-the-badge" class="tech-icon">
            </div>
        </div>

        <!-- GitHub Analytics -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2rem; text-align: center; margin-bottom: 30px;">📊 GitHub Analytics</h1>
            <div class="stats-container">
                <div class="stat-card">
                    <img height="180em" src="https://github-readme-stats.vercel.app/api?username=SantoshChintawar&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117"/>
                </div>
                <div class="stat-card">
                    <img height="180em" src="https://github-readme-streak-stats.herokuapp.com/?user=SantoshChintawar&theme=tokyonight&hide_border=true&background=0D1117"/>
                </div>
            </div>
        </div>

        <!-- Contribution Graph -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2rem; text-align: center; margin-bottom: 30px;">📈 Contribution Graph</h1>
            <img src="https://github-readme-activity-graph.vercel.app/graph?username=SantoshChintawar&theme=tokyo-night&hide_border=true&area=true" style="width: 100%; border-radius: 10px;">
        </div>

        <!-- GitHub Achievements -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2rem; text-align: center; margin-bottom: 30px;">🏆 GitHub Achievements</h1>
            <img src="https://github-profile-trophy.vercel.app/?username=SantoshChintawar&theme=radical&no-frame=true&margin-w=15&margin-h=15" style="width: 100%;">
        </div>

        <!-- Most Used Languages -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2rem; text-align: center; margin-bottom: 30px;">💻 Most Used Languages</h1>
            <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=SantoshChintawar&layout=compact&theme=tokyonight&hide_border=true" style="display: block; margin: 0 auto;">
        </div>

        <!-- Snake Animation -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2rem; text-align: center; margin-bottom: 30px;">🐍 Snake Eating Contributions</h1>
            <img src="https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake-dark.svg" style="width: 100%;">
        </div>

        <!-- Random Dev Quote -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2rem; text-align: center; margin-bottom: 30px;">✨ Random Dev Quote</h1>
            <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight" style="display: block; margin: 0 auto;">
        </div>

        <!-- Coding Profiles -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2rem; text-align: center; margin-bottom: 30px;">🔥 Coding Profiles</h1>
            <div class="tech-icons">
                <img src="https://img.shields.io/badge/LeetCode-Active-orange?style=for-the-badge&logo=leetcode" class="tech-icon">
                <img src="https://img.shields.io/badge/GeeksforGeeks-Coding-green?style=for-the-badge&logo=geeksforgeeks" class="tech-icon">
                <img src="https://img.shields.io/badge/HackerRank-Problem%20Solver-brightgreen?style=for-the-badge&logo=hackerrank" class="tech-icon">
            </div>
        </div>

        <!-- AWS Journey -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2rem; text-align: center; margin-bottom: 30px;">☁️ AWS Journey</h1>
            <div style="text-align: center;">
                <img src="https://img.shields.io/badge/AWS-Cloud%20Learner-orange?style=for-the-badge&logo=amazonaws" class="tech-icon">
            </div>
            <div class="progress-bar" style="margin: 20px auto; width: 80%;">
                <div class="progress-fill" style="--width: 65%; width: 65%;"></div>
            </div>
            <p style="text-align: center;">Progress: 65%</p>
        </div>

        <!-- 2026 Goals -->
        <div class="glass-card">
            <h1 class="gradient-text" style="font-size: 2rem; text-align: center; margin-bottom: 30px;">🎯 2026 Goals</h1>
            <div style="max-width: 600px; margin: 0 auto;">
                <p>✅ Become AWS Certified</p>
                <div class="progress-bar"><div class="progress-fill" style="--width: 70%; width: 70%;"></div></div>
                <p>✅ Contribute to Open Source</p>
                <div class="progress-bar"><div class="progress-fill" style="--width: 50%; width: 50%;"></div></div>
                <p>✅ Build AI Projects</p>
                <div class="progress-bar"><div class="progress-fill" style="--width: 60%; width: 60%;"></div></div>
                <p>✅ Crack Big Tech Opportunities</p>
                <div class="progress-bar"><div class="progress-fill" style="--width: 40%; width: 40%;"></div></div>
                <p>✅ Improve DSA & Development Skills</p>
                <div class="progress-bar"><div class="progress-fill" style="--width: 55%; width: 55%;"></div></div>
            </div>
        </div>

        <!-- Footer -->
        <div class="glass-card" style="text-align: center;">
            <img src="https://capsule-render.vercel.app/api?type=waving&color=0:8A2BE2,100:00F7FF&height=100&section=footer" style="width: 100%;">
            <h2 style="margin-top: 20px;">
                ⭐ Keep Learning • Keep Building • Keep Growing 🚀
            </h2>
        </div>
    </div>

    <script>
        // Create animated stars
        function createStars() {
            const starsContainer = document.getElementById('stars');
            for (let i = 0; i < 200; i++) {
                const star = document.createElement('div');
                star.className = 'star';
                star.style.width = Math.random() * 3 + 'px';
                star.style.height = star.style.width;
                star.style.left = Math.random() * 100 + '%';
                star.style.top = Math.random() * 100 + '%';
                star.style.animationDelay = Math.random() * 3 + 's';
                starsContainer.appendChild(star);
            }
        }

        // Typing animation
        const texts = [
            "Hey There 👋",
            "I'm Santosh Chintawar",
            "Full Stack Developer 🚀",
            "AWS Cloud Learner ☁️",
            "AI & Web Projects Builder 🔥"
        ];
        
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingTextElement = document.getElementById('typing-text');

        function typeEffect() {
            const currentText = texts[textIndex];
            
            if (isDeleting) {
                typingTextElement.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingTextElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }
            
            if (!isDeleting && charIndex === currentText.length) {
                isDeleting = true;
                setTimeout(typeEffect, 2000);
                return;
            }
            
            if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
            }
            
            const speed = isDeleting ? 50 : 100;
            setTimeout(typeEffect, speed);
        }

        // Intersection Observer for fade-in animations
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

        // Apply fade-in animation to all glass cards
        document.querySelectorAll('.glass-card').forEach((card, index) => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(30px)';
            card.style.transition = `opacity 0.6s ease ${index * 0.1}s, transform 0.6s ease ${index * 0.1}s`;
            observer.observe(card);
        });

        // Initialize animations
        createStars();
        typeEffect();

        // Add hover effect to tech icons
        document.querySelectorAll('.tech-icon').forEach(icon => {
            icon.addEventListener('mouseenter', function() {
                this.style.transform = 'scale(1.2) rotate(5deg)';
            });
            icon.addEventListener('mouseleave', function() {
                this.style.transform = 'scale(1) rotate(0deg)';
            });
        });
    </script>
</body>
</html>
