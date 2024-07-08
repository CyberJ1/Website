
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CyberJ's Tech Journey</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, Helvetica, sans-serif;
            background-color: black;
            color: #fff;
            overflow: hidden;
        }

        h1, h2 {
            text-align: center;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.8);
        }

        section {
            max-width: 800px;
            margin: 50px auto;
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.6);
            border-radius: 10px;
        }

        a {
            color: #0ff;
        }

        .flicker {
            animation: flicker 1.5s infinite alternate;
        }

        @keyframes flicker {
            0%, 19%, 21%, 23%, 25%, 54%, 56%, 100% {
                opacity: 1;
            }
            20%, 24%, 55% {
                opacity: 0;
            }
        }

        .matrix {
            position: fixed;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: black;
            overflow: hidden;
        }

        .matrix canvas {
            display: block;
        }

        .monitor {
            width: 100px;
            height: 70px;
            background: #0ff;
            position: absolute;
            animation: monitorEffect 1s infinite;
        }

        @keyframes monitorEffect {
            0% { background: #0ff; }
            50% { background: #00f; }
            100% { background: #0ff; }
        }

        .wire {
            width: 5px;
            height: 100px;
            background: #333;
            position: absolute;
            box-shadow: 0 0 5px #0ff;
        }
    </style>
</head>
<body>
    <div class="matrix">
        <canvas id="matrixCanvas"></canvas>
    </div>
    <header>
        <h1>Welcome to CyberJ's Tech Journey</h1>
    </header>
    <section>
        <h2>About Me</h2>
        <p>I'm CyberJ, a passionate Cybersecurity Enthusiast, learning to code my own website from scratch! I'm dedicated to enhancing my skills and exploring new technologies to stay at the forefront of the tech industry.</p>
        <p>Connect with me on <a href="https://www.linkedin.com/in/jose-maldonado-cyberlink/" target="_blank">LinkedIn</a>.</p>
    </section>
    <section>
        <h2>Current Projects</h2>
        <h3>SOC Level 1 Pathway (In progress)</h3>
        <p>Comprehensive training in Security Operations Center (SOC) fundamentals.</p>
        <ul>
            <li>Hands-on experience in incident response and threat detection.</li>
            <li>Mastery of Security Information and Event Management (SIEM) tools and techniques.</li>
            <li>Development of skills in monitoring and analyzing security alerts.</li>
        </ul>
        <h3>Skills (Security Engineer Pathway)</h3>
        <ul>
            <li>Network Security</li>
            <li>Security Engineering</li>
            <li>System Hardening</li>
            <li>Vulnerability Assessment</li>
            <li>Secure System Design</li>
        </ul>
        <h3>Preparing for AWS Cloud Practitioner Certification</h3>
    </section>
    <div class="monitor" style="top: 20%; left: 30%;"></div>
    <div class="monitor" style="top: 25%; left: 50%;"></div>
    <div class="monitor" style="top: 40%; left: 70%;"></div>

    <div class="wire" style="top: 10%; left: 20%; height: 50%;"></div>
    <div class="wire" style="top: 15%; left: 45%; height: 60%;"></div>
    <div class="wire" style="top: 35%; left: 60%; height: 70%;"></div>

    <script>
        const canvas = document.getElementById('matrixCanvas');
        const ctx = canvas.getContext('2d');

        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        const matrixChars = "ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789@#$%^&*()*&^%";
        const fontSize = 16;
        const columns = canvas.width / fontSize;
        const drops = Array.from({ length: columns }, () => 1);

        function draw() {
            ctx.fillStyle = 'rgba(0, 0, 0, 0.05)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            ctx.fillStyle = '#0F0';
            ctx.font = `${fontSize}px monospace`;

            for (let i = 0; i < drops.length; i++) {
                const text = matrixChars[Math.floor(Math.random() * matrixChars.length)];
                ctx.fillText(text, i * fontSize, drops[i] * fontSize);

                if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
                    drops[i] = 0;
                }

                drops[i]++;
            }
        }

        setInterval(draw, 33);

        window.addEventListener('resize', () => {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
            drops.length = Math.floor(canvas.width / fontSize);
            for (let i = 0; i < drops.length; i++) {
                drops[i] = 1;
            }
        });

        function createFlickeringLightEffect(element, intensity) {
            setInterval(() => {
                element.style.opacity = (Math.random() * (1 - intensity) + intensity).toString();
            }, 50);
        }

        function createMonitorEffect() {
            const monitors = document.querySelectorAll('.monitor');
            monitors.forEach(monitor => {
                setInterval(() => {
                    monitor.style.backgroundColor = `rgb(${Math.random()*255}, ${Math.random()*255}, ${Math.random()*255})`;
                }, 100);
            });
        }

        function createSignalEffect() {
            const wires = document.querySelectorAll('.wire');
            wires.forEach(wire => {
                setInterval(() => {
                    wire.style.boxShadow = `0 0 ${Math.random()*10}px 5px #0ff`;
                }, 200);
            });
        }

        createMonitorEffect();
        createSignalEffect();
    </script>
</body>
</html>
