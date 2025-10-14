<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>午夜福利 - 炫酷网站横幅</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #0a0a16;
            color: #fff;
            overflow-x: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            padding: 20px;
        }
        
        .banner {
            position: relative;
            width: 100%;
            height: 500px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            background: linear-gradient(135deg, #0a0a16 0%, #1a1a2e 50%, #0a0a16 100%);
            border-radius: 15px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.5);
        }
        
        #particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
        }
        
        .content {
            position: relative;
            z-index: 2;
            text-align: center;
            padding: 0 20px;
        }
        
        .site-title {
            font-size: 5rem;
            font-weight: 900;
            letter-spacing: 5px;
            margin-bottom: 20px;
            text-transform: uppercase;
            color: #fff;
            text-shadow: 
                0 0 5px #8a2be2,
                0 0 10px #8a2be2,
                0 0 20px #8a2be2,
                0 0 40px #8a2be2,
                0 0 80px #8a2be2;
            animation: neonPulse 2s infinite alternate;
            transition: all 0.3s ease;
        }
        
        .site-title:hover {
            transform: scale(1.05);
            text-shadow: 
                0 0 10px #8a2be2,
                0 0 20px #8a2be2,
                0 0 30px #8a2be2,
                0 0 50px #8a2be2,
                0 0 100px #8a2be2;
        }
        
        .site-subtitle {
            font-size: 1.5rem;
            margin-bottom: 30px;
            opacity: 0.8;
            font-weight: 300;
            letter-spacing: 2px;
            color: #c0c0ff;
        }
        
        .cta-button {
            display: inline-block;
            padding: 15px 40px;
            background: rgba(138, 43, 226, 0.2);
            color: white;
            text-decoration: none;
            font-weight: 600;
            letter-spacing: 1px;
            border-radius: 50px;
            border: 2px solid #8a2be2;
            backdrop-filter: blur(10px);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            text-transform: uppercase;
            box-shadow: 0 0 15px rgba(138, 43, 226, 0.5);
        }
        
        .cta-button:before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: all 0.6s ease;
        }
        
        .cta-button:hover {
            background: rgba(138, 43, 226, 0.4);
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(138, 43, 226, 0.7);
        }
        
        .cta-button:hover:before {
            left: 100%;
        }
        
        .moon {
            position: absolute;
            top: 10%;
            right: 10%;
            width: 100px;
            height: 100px;
            border-radius: 50%;
            background: radial-gradient(circle at 30px 30px, #f9f3d5, #e6d8a5);
            box-shadow: 0 0 30px #f9f3d5;
            z-index: 2;
            animation: float 6s ease-in-out infinite;
        }
        
        .stars {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
        }
        
        .star {
            position: absolute;
            background-color: white;
            border-radius: 50%;
            animation: twinkle 5s infinite;
        }
        
        .features {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 40px;
            flex-wrap: wrap;
        }
        
        .feature {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 10px;
            width: 200px;
            text-align: center;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(138, 43, 226, 0.3);
            transition: all 0.3s ease;
        }
        
        .feature:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(138, 43, 226, 0.3);
        }
        
        .feature i {
            font-size: 2.5rem;
            color: #8a2be2;
            margin-bottom: 15px;
        }
        
        .feature h3 {
            margin-bottom: 10px;
            color: #fff;
        }
        
        .feature p {
            color: #c0c0ff;
            font-size: 0.9rem;
        }
        
        @keyframes neonPulse {
            from {
                text-shadow: 
                    0 0 5px #8a2be2,
                    0 0 10px #8a2be2,
                    0 0 20px #8a2be2,
                    0 0 40px #8a2be2,
                    0 0 80px #8a2be2;
            }
            to {
                text-shadow: 
                    0 0 10px #8a2be2,
                    0 0 15px #8a2be2,
                    0 0 25px #8a2be2,
                    0 0 45px #8a2be2,
                    0 0 85px #8a2be2;
            }
        }
        
        @keyframes twinkle {
            0%, 100% {
                opacity: 0.2;
            }
            50% {
                opacity: 1;
            }
        }
        
        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-20px);
            }
        }
        
        @media (max-width: 768px) {
            .site-title {
                font-size: 3rem;
                letter-spacing: 3px;
            }
            
            .site-subtitle {
                font-size: 1.2rem;
            }
            
            .moon {
                width: 60px;
                height: 60px;
                top: 5%;
                right: 5%;
            }
            
            .banner {
                height: 400px;
            }
            
            .features {
                gap: 15px;
            }
            
            .feature {
                width: 150px;
                padding: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="banner">
            <canvas id="particles"></canvas>
            <div class="stars" id="stars"></div>
            <div class="moon"></div>
            <div class="content">
                <h1 class="site-title">午夜福利</h1>
                <p class="site-subtitle">神秘世界，等你探索</p >
                <!-- 请将下面的链接替换为您网站的URL -->
                <a href=" " class="cta-button">立即进入</a >
            </div>
        </div>
        
        <div class="features">
            <div class="feature">
                <i class="fas fa-gem"></i>
                <h3>独家内容</h3>
                <p>精心挑选的独家福利内容</p >
            </div>
            <div class="feature">
                <i class="fas fa-lock"></i>
                <h3>安全私密</h3>
                <p>保护您的隐私安全</p >
            </div>
            <div class="feature">
                <i class="fas fa-bolt"></i>
                <h3>快速加载</h3>
                <p>高速服务器，流畅体验</p >
            </div>
            <div class="feature">
                <i class="fas fa-mobile-alt"></i>
                <h3>移动适配</h3>
                <p>完美适配各种设备</p >
            </div>
        </div>
    </div>

    <script>
        // 粒子背景效果
        const canvas = document.getElementById('particles');
        const ctx = canvas.getContext('2d');
        
        // 设置canvas尺寸
        function resizeCanvas() {
            canvas.width = canvas.parentElement.clientWidth;
            canvas.height = canvas.parentElement.clientHeight;
        }
        
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 粒子类
        class Particle {
            constructor() {
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * canvas.height;
                this.size = Math.random() * 3 + 1;
                this.speedX = Math.random() * 3 - 1.5;
                this.speedY = Math.random() * 3 - 1.5;
                this.color = `rgba(${Math.floor(Math.random() * 100 + 100)}, 
                                  ${Math.floor(Math.random() * 50 + 50)}, 
                                  ${Math.floor(Math.random() * 155 + 100)}, 
                                  ${Math.random() * 0.5 + 0.1})`;
            }
            
            update() {
                this.x += this.speedX;
                this.y += this.speedY;
                
                if (this.x > canvas.width || this.x < 0) this.speedX = -this.speedX;
                if (this.y > canvas.height || this.y < 0) this.speedY = -this.speedY;
            }
            
            draw() {
                ctx.fillStyle = this.color;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
            }
        }
        
        // 创建粒子
        const particles = [];
        const particleCount = 80;
        
        for (let i = 0; i < particleCount; i++) {
            particles.push(new Particle());
        }
        
        // 连接粒子
        function connectParticles() {
            const maxDistance = 150;
            for (let a = 0; a < particles.length; a++) {
                for (let b = a; b < particles.length; b++) {
                    const dx = particles[a].x - particles[b].x;
                    const dy = particles[a].y - particles[b].y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance < maxDistance) {
                        const opacity = 1 - distance / maxDistance;
                        ctx.strokeStyle = `rgba(138, 43, 226, ${opacity * 0.2})`;
                        ctx.lineWidth = 1;
                        ctx.beginPath();
                        ctx.moveTo(particles[a].x, particles[a].y);
                        ctx.lineTo(particles[b].x, particles[b].y);
                        ctx.stroke();
                    }
                }
            }
        }
        
        // 动画循环
        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            for (let i = 0; i < particles.length; i++) {
                particles[i].update();
                particles[i].draw();
            }
            
            connectParticles();
            requestAnimationFrame(animate);
        }
        
        animate();
        
        // 创建星星
        function createStars() {
            const starsContainer = document.getElementById('stars');
            const starCount = 100;
            
            for (let i = 0; i < starCount; i++) {
                const star = document.createElement('div');
                star.classList.add('star');
                
                // 随机位置和大小
                const size = Math.random() * 3;
                star.style.width = `${size}px`;
                star.style.height = `${size}px`;
                star.style.left = `${Math.random() * 100}%`;
                star.style.top = `${Math.random() * 100}%`;
                
                // 随机动画延迟
                star.style.animationDelay = `${Math.random() * 5}s`;
                
                starsContainer.appendChild(star);
            }
        }
        
        createStars();
        
        // 鼠标交互效果
        let mouseX = 0;
        let mouseY = 0;
        
        document.addEventListener('mousemove', (e) => {
            mouseX = e.clientX;
            mouseY = e.clientY;
            
            // 鼠标附近的粒子受到排斥
            for (let i = 0; i < particles.length; i++) {
                const dx = particles[i].x - mouseX;
                const dy = particles[i].y - mouseY;
                const distance = Math.sqrt(dx * dx + dy * dy);
                
                if (distance < 100) {
                    particles[i].speedX += dx / distance * 0.5;
                    particles[i].speedY += dy / distance * 0.5;
                }
            }
        });
    </script>
</body>
</html>
