<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>0xanon - Cybersecurity Professional</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary: #2ecc71;
            --dark: #2c3e50;
            --light: #ecf0f1;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', sans-serif;
        }

        body {
            background: var(--dark);
            color: var(--light);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Header Styles */
        header {
            background: linear-gradient(rgba(44, 62, 80, 0.9), rgba(44, 62, 80, 0.9)),
                        url('https://images.unsplash.com/photo-1451187580459-43490279c0fa?auto=format&fit=crop&w=1950');
            background-size: cover;
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: center;
        }

        .profile-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            margin-bottom: 1rem;
            border: 5px solid var(--primary);
        }

        /* Section Styles */
        section {
            padding: 5rem 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 3px;
            background: var(--primary);
        }

        /* Experience Timeline */
        .timeline {
            position: relative;
            max-width: 900px;
            margin: 0 auto;
        }

        .timeline-item {
            padding: 2rem;
            background: rgba(255, 255, 255, 0.1);
            margin-bottom: 2rem;
            border-radius: 10px;
            position: relative;
            transition: transform 0.3s ease;
        }

        .timeline-item:hover {
            transform: translateX(10px);
        }

        /* Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .skill-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
        }

        /* Contact Form */
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }

        input, textarea {
            width: 100%;
            padding: 1rem;
            margin-bottom: 1rem;
            background: rgba(255, 255, 255, 0.1);
            border: none;
            color: var(--light);
        }

        .btn {
            display: inline-block;
            padding: 1rem 2rem;
            background: var(--primary);
            color: var(--dark);
            text-decoration: none;
            border-radius: 5px;
            transition: transform 0.3s ease;
        }

        .btn:hover {
            transform: translateY(-3px);
        }

        /* Social Links */
        .social-links {
            margin-top: 2rem;
        }

        .social-links a {
            color: var(--light);
            font-size: 1.5rem;
            margin: 0 1rem;
            transition: color 0.3s ease;
        }

        .social-links a:hover {
            color: var(--primary);
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <img src="your-profile-image.jpg" alt="0xanon" class="profile-img">
            <h1>0xanon</h1>
            <p>Cybersecurity Specialist | Ethical Hacker | Security Researcher</p>
            <div class="social-links">
                <a href="https://www.linkedin.com/in/0xanon/" target="_blank"><i class="fab fa-linkedin"></i></a>
                <a href="https://github.com/yourusername" target="_blank"><i class="fab fa-github"></i></a>
                <a href="mailto:your.email@example.com"><i class="fas fa-envelope"></i></a>
            </div>
        </div>
    </header>

    <section id="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <p>Seasoned cybersecurity professional with X+ years of experience in penetration testing, vulnerability assessment, and security infrastructure design. Passionate about ethical hacking and developing robust security solutions.</p>
        </div>
    </section>

    <section id="skills">
        <div class="container">
            <h2 class="section-title">Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <h3>Penetration Testing</h3>
                    <p>Burp Suite, Metasploit, Nmap</p>
                </div>
                <div class="skill-card">
                    <h3>Security Tools</h3>
                    <p>Wireshark, Kali Linux, Snort</p>
                </div>
                <div class="skill-card">
                    <h3>Programming</h3>
                    <p>Python, Bash, C/C++</p>
                </div>
            </div>
        </div>
    </section>

    <section id="experience">
        <div class="container">
            <h2 class="section-title">Professional Experience</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <h3>Senior Security Engineer</h3>
                    <p>XYZ Corporation • 2020-Present</p>
                    <ul>
                        <li>Conducted 50+ penetration tests for Fortune 500 companies</li>
                        <li>Developed automated vulnerability scanning system</li>
                    </ul>
                </div>
                <!-- Add more timeline items -->
            </div>
        </div>
    </section>

    <script>
        // Smooth scrolling for navigation
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Animation on scroll
        window.addEventListener('scroll', function() {
            const elements = document.querySelectorAll('.timeline-item, .skill-card');
            elements.forEach(element => {
                const elementTop = element.getBoundingClientRect().top;
                if(elementTop < window.innerHeight - 100) {
                    element.style.opacity = '1';
                    element.style.transform = 'translateY(0)';
                }
            });
        });
    </script>
</body>
</html>
