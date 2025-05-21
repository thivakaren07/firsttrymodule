# firsttrymodule
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Name | Professional Portfolio</title>
    <style>
        /* Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }
        
        a {
            text-decoration: none;
            color: #2c3e50;
        }
        
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background: #2c3e50;
            color: #fff;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        header h1 {
            font-size: 24px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: #fff;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: #3498db;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: center;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://via.placeholder.com/1920x1080') no-repeat center center/cover;
            color: #fff;
            padding-top: 80px;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h2 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
        }
        
        .btn {
            display: inline-block;
            background: #3498db;
            color: #fff;
            padding: 10px 30px;
            border-radius: 5px;
            font-weight: 500;
            transition: background 0.3s;
        }
        
        .btn:hover {
            background: #2980b9;
        }
        
        /* About Section */
        .section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 36px;
            color: #2c3e50;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 40px;
        }
        
        .about-img {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
        }
        
        .about-img img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            font-size: 24px;
            margin-bottom: 20px;
            color: #2c3e50;
        }
        
        .about-text p {
            margin-bottom: 15px;
        }
        
        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .skill {
            background: #fff;
            padding: 30px;
            border-radius: 5px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            text-align: center;
            transition: transform 0.3s;
        }
        
        .skill:hover {
            transform: translateY(-10px);
        }
        
        .skill i {
            font-size: 50px;
            color: #3498db;
            margin-bottom: 20px;
        }
        
        .skill h3 {
            margin-bottom: 15px;
            color: #2c3e50;
        }
        
        /* Projects Section */
        .projects-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project {
            background: #fff;
            border-radius: 5px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .project-img {
            height: 200px;
            overflow: hidden;
        }
        
        .project-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .project:hover .project-img img {
            transform: scale(1.1);
        }
        
        .project-info {
            padding: 20px;
        }
        
        .project-info h3 {
            margin-bottom: 10px;
            color: #2c3e50;
        }
        
        .project-info p {
            margin-bottom: 15px;
        }
        
        /* Contact Section */
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background: #fff;
            padding: 30px;
            border-radius: 5px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
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
        
        /* Footer */
        footer {
            background: #2c3e50;
            color: #fff;
            text-align: center;
            padding: 20px 0;
        }
        
        .social-links {
            margin-bottom: 20px;
        }
        
        .social-links a {
            color: #fff;
            margin: 0 10px;
            font-size: 20px;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: #3498db;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .about-content {
                flex-direction: column;
            }
            
            .hero h2 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <h1>Your Name</h1>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h2>Hello, I'm Your Name</h2>
                <p>A passionate [Your Profession] specializing in [Your Specialization]. I create beautiful, functional websites and applications.</p>
                <a href="#projects" class="btn">View My Work</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-img">
                    <img src="https://via.placeholder.com/400x500" alt="Your Name">
                </div>
                <div class="about-text">
                    <h3>Who Am I?</h3>
                    <p>I'm a [Your Profession] with [X] years of experience in the industry. I specialize in [Your Specializations] and have worked with clients from various sectors.</p>
                    <p>My journey in [Your Field] began when [Your Story]. Since then, I've been passionate about creating solutions that are not only functional but also provide great user experiences.</p>
                    <p>When I'm not coding or designing, you can find me [Your Hobbies]. I believe in continuous learning and staying updated with the latest technologies and trends in the industry.</p>
                    <a href="#" class="btn">Download Resume</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section">
        <div class="container">
            <h2 class="section-title">My Skills</h2>
            <div class="skills-container">
                <div class="skill">
                    <i class="fas fa-code"></i>
                    <h3>Web Development</h3>
                    <p>Building responsive and interactive websites using modern technologies like HTML5, CSS3, JavaScript, and frameworks.</p>
                </div>
                <div class="skill">
                    <i class="fas fa-paint-brush"></i>
                    <h3>UI/UX Design</h3>
                    <p>Creating intuitive and visually appealing user interfaces with a focus on user experience principles.</p>
                </div>
                <div class="skill">
                    <i class="fas fa-mobile-alt"></i>
                    <h3>Mobile Development</h3>
                    <p>Developing cross-platform mobile applications using frameworks like React Native or Flutter.</p>
                </div>
                <div class="skill">
                    <i class="fas fa-database"></i>
                    <h3>Database Management</h3>
                    <p>Designing and implementing efficient database structures with SQL and NoSQL solutions.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section">
        <div class="container">
            <h2 class="section-title">My Projects</h2>
            <div class="projects-container">
                <div class="project">
                    <div class="project-img">
                        <img src="https://via.placeholder.com/600x400" alt="Project 1">
                    </div>
                    <div class="project-info">
                        <h3>E-commerce Website</h3>
                        <p>A fully responsive e-commerce platform with product listings, cart functionality, and secure checkout.</p>
                        <a href="#" class="btn">View Project</a>
                    </div>
                </div>
                <div class="project">
                    <div class="project-img">
                        <img src="https://via.placeholder.com/600x400" alt="Project 2">
                    </div>
                    <div class="project-info">
                        <h3>Task Management App</h3>
                        <p>A productivity application for managing tasks with drag-and-drop functionality and team collaboration.</p>
                        <a href="#" class="btn">View Project</a>
                    </div>
                </div>
                <div class="project">
                    <div class="project-img">
                        <img src="https://via.placeholder.com/600x400" alt="Project 3">
                    </div>
                    <div class="project-info">
                        <h3>Portfolio Website</h3>
                        <p>A custom portfolio website for a photographer with gallery, blog, and contact features.</p>
                        <a href="#" class="btn">View Project</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
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
                    <button type="submit" class="btn">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
            <p>&copy; 2023 Your Name. All Rights Reserved.</p>
        </div>
    </footer>
</body>
</html>
