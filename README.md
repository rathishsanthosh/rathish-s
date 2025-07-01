<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rathish S - Portfolio</title>
    <style>
        /* CSS Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        /* Variables */
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
        }

        /* General Styles */
        body {
            background-color: #f5f5f5;
            color: var(--dark-color);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 60px 0;
        }

        h1, h2, h3 {
            margin-bottom: 20px;
            color: var(--primary-color);
        }

        p {
            margin-bottom: 15px;
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary-color);
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        .btn:hover {
            background-color: #2980b9;
        }

        /* Header Styles */
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: white;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--secondary-color);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('/api/placeholder/1200/800') center/cover;
            color: white;
            text-align: center;
            padding-top: 80px;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            color: white;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }

        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        /* About Section */
        .about {
            background-color: white;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }

        .about-img {
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .about-img img {
            width: 100%;
            display: block;
        }

        .about-content h2 {
            color: var(--primary-color);
        }

        .personal-info {
            margin-top: 20px;
        }

        .info-item {
            margin-bottom: 10px;
            display: flex;
        }

        .info-item strong {
            min-width: 120px;
            display: inline-block;
        }

        /* Skills Section */
        .skills {
            background-color: var(--light-color);
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
        }

        .skill-card {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            text-align: center;
            transition: transform 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-5px);
        }

        .skill-card i {
            font-size: 2.5rem;
            color: var(--secondary-color);
            margin-bottom: 15px;
        }

        /* Education Section */
        .education {
            background-color: white;
        }

        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline::after {
            content: '';
            position: absolute;
            width: 2px;
            background-color: var(--primary-color);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -1px;
        }

        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }

        .timeline-item:nth-child(odd) {
            left: 0;
        }

        .timeline-item:nth-child(even) {
            left: 50%;
        }

        .timeline-item::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: white;
            border: 2px solid var(--secondary-color);
            top: 15px;
            border-radius: 50%;
            z-index: 1;
        }

        .timeline-item:nth-child(odd)::after {
            right: -11px;
        }

        .timeline-item:nth-child(even)::after {
            left: -11px;
        }

        .timeline-content {
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .timeline-year {
            color: var(--accent-color);
            font-weight: bold;
        }

        /* Projects Section */
        .projects {
            background-color: var(--light-color);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .project-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }

        .project-card:hover {
            transform: translateY(-5px);
        }

        .project-img {
            height: 200px;
            background-color: var(--secondary-color);
            position: relative;
        }

        .project-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .project-content {
            padding: 20px;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }

        .tech-tag {
            background-color: var(--light-color);
            padding: 5px 10px;
            border-radius: 5px;
            font-size: 0.8rem;
        }

        /* Contact Section */
        .contact {
            background-color: white;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .contact-form {
            background-color: var(--light-color);
            padding: 30px;
            border-radius: 10px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .form-group textarea {
            height: 150px;
        }

        .submit-btn {
            background-color: var(--accent-color);
            color: white;
            border: none;
            padding: 12px 25px;
            cursor: pointer;
            border-radius: 5px;
            font-size: 1rem;
            transition: background-color 0.3s;
        }

        .submit-btn:hover {
            background-color: #c0392b;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }

        .contact-item i {
            font-size: 1.5rem;
            color: var(--secondary-color);
            margin-right: 15px;
        }

        /* Footer */
        footer {
            background-color: var(--dark-color);
            color: white;
            text-align: center;
            padding: 20px 0;
        }

        .social-links {
            display: flex;
            justify-content: center;
            margin-bottom: 20px;
            gap: 20px;
        }

        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: var(--secondary-color);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .about-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .timeline::after {
                left: 31px;
            }

            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 0;
            }

            .timeline-item:nth-child(even) {
                left: 0;
            }

            .timeline-item:nth-child(odd)::after,
            .timeline-item:nth-child(even)::after {
                left: 22px;
            }

            .nav-links {
                display: none;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo">Rathish S</a>
                <ul class="nav-links">
                    <li><a href="#about">About</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#education">Education</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Rathish S</h1>
                <p>Computer Science Engineering Student | Web Developer | Programmer</p>
                <div class="hero-btns">
                    <a href="#projects" class="btn">View My Work</a>
                    <a href="#contact" class="btn">Contact Me</a>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2>About Me</h2>
            <div class="about-grid">
                <div class="about-img">
                    <img src="C:\Users\Asus\OneDrive\Desktop\WhatsApp Image 2025-04-16 at 3.11.59 PM.jpeg" alt="Rathish S">
                </div>
                <div class="about-content">
                    <p>I am a passionate Computer Science Engineering student with a keen interest in web development and database management. I enjoy creating innovative solutions to real-world problems and am constantly learning new technologies to expand my skill set.</p>
                    <div class="personal-info">
                        <div class="info-item">
                            <strong>Name:</strong> <span>Rathish S</span>
                        </div>
                        <div class="info-item">
                            <strong>Age:</strong> <span>20</span>
                        </div>
                        <div class="info-item">
                            <strong>Degree:</strong> <span>BE - Computer Science Engineering</span>
                        </div>
                        <div class="info-item">
                            <strong>College:</strong> <span>SNS College of Engineering</span>
                        </div>
                        <div class="info-item">
                            <strong>Email:</strong> <span>rathishs171@gmail.com</span>
                        </div>
                        <div class="info-item">
                            <strong>Location:</strong> <span>2/358 CRPF, Coimbatore, Tamil Nadu</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section class="skills" id="skills">
        <div class="container">
            <h2>My Skills</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <h3>HTML</h3>
                    <p>Proficient in creating structured, semantic web pages with modern HTML5 features.</p>
                </div>
                <div class="skill-card">
                    <h3>CSS</h3>
                    <p>Skilled in designing responsive and attractive user interfaces with CSS3 including animations and transitions.</p>
                </div>
                <div class="skill-card">
                    <h3>JavaScript</h3>
                    <p>Experienced in implementing interactive features and dynamic content for web applications.</p>
                </div>
                <div class="skill-card">
                    <h3>Python</h3>
                    <p>Capable of developing automation scripts, data analysis tools, and integrating with hardware like Raspberry Pi.</p>
                </div>
                <div class="skill-card">
                    <h3>SQL</h3>
                    <p>Knowledge of database design, querying and management with SQL for structured data storage.</p>
                </div>
                <div class="skill-card">
                    <h3>MongoDB</h3>
                    <p>Familiar with NoSQL database concepts and implementing MongoDB for flexible data storage solutions.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section class="education" id="education">
        <div class="container">
            <h2>Education</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-year">2022 - Present</div>
                        <h3>Bachelor of Engineering - Computer Science</h3>
                        <p>SNS College of Engineering, Coimbatore</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-year">2020 - 2022</div>
                        <h3>Higher Secondary Education (12th Grade)</h3>
                        <p>Sri Ramakrishna Matric HSC School</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-year">2018 - 2020</div>
                        <h3>Secondary Education (10th Grade)</h3>
                        <p>Sri Ramakrishna Matric HSC School</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="projects" id="projects">
        <div class="container">
            <h2>Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-img">
                        <img src="/api/placeholder/400/300" alt="Automated Streetlight Project">
                    </div>
                    <div class="project-content">
                        <h3>Automated Streetlight</h3>
                        <p>A smart streetlight system that automatically adjusts brightness based on ambient light and detects vehicle movement to conserve energy.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Raspberry Pi</span>
                            <span class="tech-tag">Python</span>
                            <span class="tech-tag">IoT</span>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img">
                        <img src="/api/placeholder/400/300" alt="Student Dashboard">
                    </div>
                    <div class="project-content">
                        <h3>Student Dashboard</h3>
                        <p>A comprehensive web-based dashboard for students to track assignments, view grades, access course materials, and communicate with professors.</p>
                        <div class="project-tech">
                            <span class="tech-tag">HTML</span>
                            <span class="tech-tag">CSS</span>
                            <span class="tech-tag">JavaScript</span>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img">
                        <img src="/api/placeholder/400/300" alt="Blood Bank Donation System">
                    </div>
                    <div class="project-content">
                        <h3>Blood Bank Donation System</h3>
                        <p>A database-driven platform that connects blood donors with patients in need, allowing for easy registration, blood group matching, and donation tracking.</p>
                        <div class="project-tech">
                            <span class="tech-tag">PHP</span>
                            <span class="tech-tag">SQL</span>
                            <span class="tech-tag">Web Development</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <h2>Contact Me</h2>
            <div class="contact-grid">
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Name</label>
                            <input type="text" id="name" name="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" name="email" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" name="subject" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" name="message" required></textarea>
                        </div>
                        <button type="submit" class="submit-btn">Send Message</button>
                    </form>
                </div>
                <div class="contact-info">
                    <div class="contact-item">
                        <div>
                            <h3>Email</h3>
                            <p>rathishs171@gmail.com</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div>
                            <h3>Phone</h3>
                            <p>+91 98765 43210</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div>
                            <h3>Address</h3>
                            <p>2/358 CRPF, Coimbatore, Tamil Nadu, India</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="https://www.linkedin.com/in/rathish-s-?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app">LinkedIn</a>
                <a href="#">GitHub</a>
                <a href="#">Twitter</a>
            </div>
            <p>&copy; 2025 Rathish S. All Rights Reserved.</p>
        </div>
    </footer>
</body>
</html>
