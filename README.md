
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CyberJ's Tech Journey</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, Helvetica, sans-serif;
            background-color: #0d0d0d;
            color: #fff;
        }

        header {
            background: url('your-header-background-image.jpg') no-repeat center center fixed;
            background-size: cover;
            text-align: center;
            padding: 100px 20px;
            position: relative;
        }

        header h1 {
            font-size: 48px;
            margin: 0;
            text-shadow: 0 0 10px #0ff;
        }

        header p {
            font-size: 24px;
            margin: 20px 0 0;
        }

        nav {
            display: flex;
            justify-content: center;
            background: #000;
            padding: 10px 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.8);
        }

        nav a {
            color: #0ff;
            text-decoration: none;
            margin: 0 15px;
            font-size: 18px;
        }

        section {
            max-width: 1200px;
            margin: 50px auto;
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.8);
            border-radius: 10px;
        }

        section h2 {
            font-size: 36px;
            text-align: center;
            margin-bottom: 20px;
        }

        section p {
            font-size: 18px;
            line-height: 1.6;
        }

        .services, .projects, .contact {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
        }

        .services div, .projects div, .contact div {
            background: rgba(0, 0, 0, 0.6);
            border-radius: 10px;
            margin: 10px;
            padding: 20px;
            flex: 1 1 30%;
            text-align: center;
        }

        footer {
            background: #000;
            padding: 20px 0;
            text-align: center;
        }

        footer p {
            margin: 0;
            font-size: 14px;
        }

        .futuristic {
            text-shadow: 0 0 10px #0ff;
        }

        .button {
            display: inline-block;
            padding: 10px 20px;
            margin-top: 10px;
            background: #0ff;
            color: #000;
            text-decoration: none;
            border-radius: 5px;
            box-shadow: 0 0 10px #0ff;
        }

        .button:hover {
            background: #00f;
            color: #fff;
        }
    </style>
</head>
<body>

<header>
    <h1 class="futuristic">CyberJ's Tech Journey</h1>
    <p>Driving Digital Transformation</p>
</header>

<nav>
    <a href="#about">About</a>
    <a href="#services">Services</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a>
</nav>

<section id="about">
    <h2>About Me</h2>
    <p>I'm CyberJ, a passionate Cybersecurity Enthusiast, learning to code my own website from scratch! I'm dedicated to enhancing my skills and exploring new technologies to stay at the forefront of the tech industry.</p>
</section>

<section id="services">
    <h2>Services</h2>
    <div class="services">
        <div>
            <h3>Consulting</h3>
            <p>Providing best practices for beginner computer users.</p>
        </div>
        <div>
            <h3>Development</h3>
            <p>Building and improving personal websites from scratch.</p>
        </div>
        <div>
            <h3>Certification Prep</h3>
            <p>Guidance on preparing for certifications like AWS Cloud Practitioner.</p>
        </div>
    </div>
</section>

<section id="projects">
    <h2>Current Projects</h2>
    <div class="projects">
        <div>
            <h3>Website Development</h3>
            <p>Creating and improving my personal website.</p>
        </div>
        <div>
            <h3>AWS Certification</h3>
            <p>Preparing for the AWS Cloud Practitioner certification.</p>
        </div>
        <div>
            <h3>Cybersecurity Training</h3>
            <p>Following the SOC Level 1 Roadmap on TryHackMe.</p>
        </div>
    </div>
</section>

<section id="contact">
    <h2>Contact Me</h2>
    <div class="contact">
        <div>
            <h3>Email</h3>
            <p><a href="mailto:your-email@example.com" class="button">Send Email</a></p>
        </div>
        <div>
            <h3>LinkedIn</h3>
            <p><a href="https://www.linkedin.com/in/your-linkedin-profile" class="button" target="_blank">Connect on LinkedIn</a></p>
        </div>
        <div>
            <h3>GitHub</h3>
            <p><a href="https://github.com/CyberJ" class="button" target="_blank">View GitHub</a></p>
        </div>
    </div>
</section>

<footer>
    <p>© 2024 CyberJ. All rights reserved.</p>
</footer>

</body>
</html>
