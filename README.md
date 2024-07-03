
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CyberJ's Tech Journey</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, Helvetica, sans-serif;
            background: url('https://www.thefinalhop.com/content/images/size/w1600/2024/03/thefinalhop_Foremost_The_Essential_Tool_for_Data_Recovery_and_D_f09ec14e-8a23-4e5b-b846-5a7cae36611c.png') no-repeat center center fixed;
            background-size: cover;
            color: #fff;
            overflow-x: hidden; /* Hide horizontal overflow */
            overflow-y: scroll; /* Enable vertical scrolling */
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

        /* Flicker animation for lights */
        @keyframes flicker {
            0%, 19%, 21%, 23%, 25%, 54%, 56%, 100% {
                opacity: 1;
            }
            20%, 24%, 55% {
                opacity: 0;
            }
        }

        .flicker {
            animation: flicker 1.5s infinite alternate;
        }

        /* Monitor effect */
        .monitor {
            position: absolute;
            width: 100px;
            height: 70px;
            background: #0ff;
            animation: monitorEffect 1s infinite;
        }

        @keyframes monitorEffect {
            0% { background: #0ff; }
            50% { background: #00f; }
            100% { background: #0ff; }
        }

        /* Signal animation */
        @keyframes signal {
            0% {
                box-shadow: 0 0 2px #0ff, 0 0 5px #0ff, 0 0 10px #0ff, 0 0 20px #0ff, 0 0 40px #0ff, 0 0 80px #0ff, 0 0 90px #0ff, 0 0 100px #0ff, 0 0 150px #0ff;
            }
            100% {
                box-shadow: 0 0 5px #0ff, 0 0 10px #0ff, 0 0 20px #0ff, 0 0 30px #0ff, 0 0 60px #0ff, 0 0 70px #0ff, 0 0 80px #0ff, 0 0 100px #0ff, 0 0 150px #0ff;
            }
        }

        .signal {
            animation: signal 2s infinite alternate;
        }
    </style>
</head>
<body>
    <header>
        <h1 class="flicker">Welcome to CyberJ's Tech Journey</h1>
    </header>
    <section>
        <h2>About Me</h2>
        <p>I'm CyberJ, a passionate Cybersecurity Enthusiast, learning to code my own website from scratch! I'm dedicated to enhancing my skills and exploring new technologies to stay at the forefront of the tech industry.</p>
        <p>Connect with me on <a href="https://www.linkedin.com/in/your-linkedin-profile" target="_blank">LinkedIn</a>.</p>
    </section>
    <section>
        <h2>Current Projects</h2>
        <ul>
            <li>Creating and improving my personal website from scratch.</li>
            <li>Preparing for the AWS Cloud Practitioner certification.</li>
            <li>Following the SOC Level 1 Roadmap on TryHackMe.</li>
        </ul>
    </section>
    <script>
        // Simulate monitor effect
        const monitors = [
            {top: '20%', left: '30%'},
            {top: '25%', left: '50%'},
            {top: '40%', left: '70%'}
        ];

        monitors.forEach((monitor, index) => {
            const monitorElement = document.createElement('div');
            monitorElement.className = 'monitor';
            monitorElement.style.top = monitor.top;
            monitorElement.style.left = monitor.left;
            document.body.appendChild(monitorElement);
        });

        // Simulate signal traveling through wires
        function createSignal() {
            const signal = document.createElement('div');
            signal.className = 'signal';
            signal.style.position = 'absolute';
            signal.style.width = '5px';
            signal.style.height = '5px';
            signal.style.backgroundColor = '#0ff';
            signal.style.borderRadius = '50%';
            signal.style.top = '50%';
            signal.style.left = '0';
            document.body.appendChild(signal);

            let position = 0;
            function animateSignal() {
                position += 2;
                signal.style.left = position + 'px';
                if (position < window.innerWidth) {
                    requestAnimationFrame(animateSignal);
                } else {
                    signal.remove();
                    createSignal();
                }
            }
            animateSignal();
        }
        createSignal();
    </script>
</body>
</html>
