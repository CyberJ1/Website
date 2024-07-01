
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CyberJ's Tech Journey</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: black;
            color: white; /* Change text color to white */
            overflow-y: scroll; /* Enable vertical scrolling */
        }
        header, section {
            margin: 20px;
            padding: 20px;
            background: rgba(0, 0, 0, 0.7); /* Semi-transparent background */
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.5);
        }
        h1, h2 {
            color: white; /* Change headings to white */
        }
        header {
            text-align: center;
        }
        section {
            margin-bottom: 40px;
        }
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: url('https://www.transparenttextures.com/patterns/asfalt-dark.png'), 
                        url('https://i.pinimg.com/originals/2a/8e/9b/2a8e9b30172e4c3b26e1ea9c287b0d6e.gif'); 
            background-repeat: repeat, no-repeat;
            background-position: center;
            background-size: cover;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to CyberJ's Tech Journey</h1>
        <p>Explore my journey, skills, and projects in the field of technology and cybersecurity.</p>
    </header>
    <section>
        <h2>About Me</h2>
        <p>I'm CyberJ, a passionate Cybersecurity Enthusiast, learning to code my own website from scratch! I'm dedicated to enhancing my skills and exploring new technologies to stay at the forefront of the tech industry.</p>
    </section>
    <section>
        <h2>Current Projects</h2>
        <p>I'm actively working on several projects to build my skills and knowledge:</p>
        <ul>
            <li>Creating and improving my personal website from scratch.</li>
            <li>Preparing for the AWS Cloud Practitioner certification.</li>
            <li>Following the SOC Level 1 Roadmap on TryHackMe.</li>
        </ul>
    </section>
    <section>
        <h2>Accomplishments</h2>
        <ul>
            <li>Successfully created and continuously improving my personal website from scratch.</li>
            <li>Gained hands-on experience in various cybersecurity tools and techniques.</li>
            <li>Reduced security issues by 20% in 30 days through system updates and vulnerability assessments.</li>
        </ul>
    </section>
    <section>
        <h2>Experience</h2>
        <h3>Power Design, Inc. | Bilingual IT Support Technician (2024 - Present)</h3>
        <ul>
            <li>Managed user accounts and groups in Active Directory (AD), ensuring compliance with access policies.</li>
            <li>Administered Microsoft Intune, implementing Multi-Factor Authentication (MFA) and synchronizing company devices for security compliance.</li>
            <li>Configured iOS and Windows devices for employees, ensuring seamless integration and functionality within the network environment and MDM policies.</li>
            <li>Triage and managed an active ticket queue, ensuring prompt resolution within the SLA to avoid breaches.</li>
            <li>Managed problem recognition, research, isolation, resolution, and follow-up for routine and complex issues with precision and efficiency.</li>
            <li>Proficiently identified, diagnosed, and resolved technical issues onsite through hands-on support and extensive training.</li>
            <li>Oversaw software licensing for various platforms and third-party vendors, ensuring compliance and optimal resource utilization.</li>
            <li>Documented device configurations, troubleshooting steps, and user interactions for knowledge sharing and future reference.</li>
            <li>Consulted with customers to recommend solutions and configuration changes, ensuring optimal functionality and satisfaction with hardware and software solutions.</li>
            <li>Served as a dedicated point of contact for onsite support, ensuring prompt resolution for technical issues with exceptional service delivery to the user.</li>
            <li>Developed Jira automation and canned responses to increase proactivity and efficiency for the Jira project.</li>
        </ul>
        <h3>Marchman Technical College | Cybersecurity Apprentice (08/2022 - 04/2023)</h3>
        <ul>
            <li>Implemented security measures to safeguard devices, conducted vulnerability assessments, collaborated with others to identify and mitigate security risks, and monitored network activities to enhance system defense.</li>
            <li>Installed system updates to address vulnerabilities and reduce security issues by 20% in 30 days.</li>
            <li>Managed user accounts and groups in Active Directory (AD), ensuring compliance with access policies.</li>
            <li>Over 150 hours as an Information Security Admin creating and analyzing configurations with security policies using Group Policy Management.</li>
        </ul>
    </section>
    <section>
        <h2>Education</h2>
        <ul>
            <li>FAMU University | Cybersecurity Bootcamp Program (04/2023 - 10/2023)</li>
            <li>Fred K. Marchman Technical College | Applied Cyber Security Program (08/2022 - 04/2023)</li>
        </ul>
    </section>
    <section>
        <h2>Skills & Abilities</h2>
        <ul>
            <li>Communication, Leadership, Network Security, Bilingual, Splunk</li>
            <li>NIST Frameworks, Analytical Skills, Wireshark, VMware, Digital Forensics</li>
            <li>AWS, Public Speaking, Active Directory, Azure, Intune, M365</li>
            <li>Troubleshooting, Windows OS, Jira, ABM, GPM, Documentation, Configuration, MFA</li>
     </ul>
    </section>
    <script>
        const canvas = document.getElementById('matrixCanvas');
        const context = canvas.getContext('2d');

        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        const katakana = 'アァカサタナハマヤャラワガザダバパイィキシチニヒミリヰギジビピウゥクスツヌフムユュルグズブプエェケセテネヘメレヱゲゼベペオォコソトノホモヨョロヲゴゾドボポヴッン0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ';
        const latin = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
        const nums = '0123456789';

        const alphabet = katakana + latin + nums;

        const fontSize = 16;
        const columns = canvas.width / fontSize;

        const rainDrops = [];

        for (let x = 0; x < columns; x++) {
            rainDrops[x] = 1;
        }

        const draw = () => {
            context.fillStyle = 'rgba(0, 0, 0, 0.05)';
            context.fillRect(0, 0, canvas.width, canvas.height);

            context.fillStyle = '#0f0';
            context.font = fontSize + 'px monospace';

            for (let i = 0; i < rainDrops.length; i++) {
                const text = alphabet.charAt(Math.floor(Math.random() * alphabet.length));
                context.fillText(text, i * fontSize, rainDrops[i] * fontSize);

                if (rainDrops[i] * fontSize > canvas.height && Math.random() > 0.975) {
                    rainDrops[i] = 0;
                }
                rainDrops[i]++;
            }
        };

        setInterval(draw, 30);

        window.addEventListener('resize', () => {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        });
    </script>
</body>
</html>
