<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MineralEdge Advisory</title>
    <style>
        :root {
            --primary: #1e3a8a;
            --secondary: #ca8a04;
            --light: #f8fafc;
            --dark: #0f172a;
            --gray: #64748b;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background-color: var(--primary);
            color: white;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
        }
        
        .logo span {
            color: var(--secondary);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--secondary);
        }
        
        .hero {
            background-image: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('/api/placeholder/1200/600');
            background-size: cover;
            background-position: center;
            height: 600px;
            display: flex;
            align-items: center;
            color: white;
            margin-top: 76px;
        }
        
        .hero-content {
            max-width: 800px;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 12px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #b45309;
        }
        
        section {
            padding: 80px 0;
        }
        
        section h2 {
            font-size: 36px;
            margin-bottom: 40px;
            text-align: center;
            color: var(--primary);
        }
        
        .services {
            background-color: white;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background-color: var(--light);
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
        }
        
        .service-card h3 {
            font-size: 24px;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        .service-icon {
            font-size: 50px;
            color: var(--secondary);
            margin-bottom: 20px;
        }
        
        .approach {
            background-color: var(--primary);
            color: white;
        }
        
        .approach h2 {
            color: white;
        }
        
        .approach-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .approach-card {
            background-color: rgba(255,255,255,0.1);
            padding: 30px;
            border-radius: 10px;
        }
        
        .approach-card h3 {
            font-size: 24px;
            margin-bottom: 15px;
            color: var(--secondary);
        }
        
        .testimonials {
            background-color: white;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial-card {
            background-color: var(--light);
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
        }
        
        .testimonial-author {
            font-weight: 600;
            color: var(--primary);
        }
        
        .contact {
            background-color: var(--light);
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .contact-info h3 {
            font-size: 24px;
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .contact-item {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }
        
        .contact-icon {
            margin-right: 10px;
            color: var(--secondary);
        }
        
        .contact-form {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
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
        
        footer {
            background-color: var(--dark);
            color: white;
            padding: 40px 0;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
        }
        
        .footer-col h3 {
            font-size: 20px;
            margin-bottom: 20px;
            color: var(--secondary);
        }
        
        .footer-col ul {
            list-style: none;
        }
        
        .footer-col ul li {
            margin-bottom: 10px;
        }
        
        .footer-col ul li a {
            color: #cbd5e1;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-col ul li a:hover {
            color: var(--secondary);
        }
        
        .copyright {
            text-align: center;
            padding-top: 40px;
            color: #94a3b8;
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
            }
            
            nav ul {
                margin-top: 20px;
            }
            
            nav ul li {
                margin: 0 10px;
            }
            
            .hero {
                height: 500px;
                margin-top: 120px;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-content">
            <div class="logo">Mineral<span>Edge</span> Advisory</div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#approach">Our Approach</a></li>
                    <li><a href="#testimonials">Case Studies</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section id="home" class="hero">
        <div class="container hero-content">
            <h1>Transforming Political Complexity into Strategic Advantage</h1>
            <p>Specialized political risk and strategic advisory services for the mineral resources sector in South Africa, with particular expertise in facilitating Saudi Arabian investment into the region.</p>
            <a href="#contact" class="btn">Get in Touch</a>
        </div>
    </section>

    <section id="services" class="services">
        <div class="container">
            <h2>Our Core Services</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">📊</div>
                    <h3>Political Intelligence & Analysis</h3>
                    <p>Comprehensive mapping of regulatory trajectories, stakeholder landscapes, and political risk assessment to provide actionable intelligence for investment decisions.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🤝</div>
                    <h3>Strategic Advisory Services</h3>
                    <p>Expert guidance on government relations strategy, stakeholder engagement planning, and crisis management tailored to the South African mineral resources sector.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">💼</div>
                    <h3>Transaction Support</h3>
                    <p>Thorough political due diligence, deal structure optimization, and regulatory approval strategy to ensure successful investments in the mining sector.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="approach" class="approach">
        <div class="container">
            <h2>Our Approach</h2>
            <div class="approach-grid">
                <div class="approach-card">
                    <h3>Intelligence-Driven Analysis</h3>
                    <p>Systematic monitoring of legislative developments, ministerial statements, and policy positions through sophisticated intelligence networks across South Africa's political landscape.</p>
                </div>
                <div class="approach-card">
                    <h3>Stakeholder Ecosystem Management</h3>
                    <p>Comprehensive mapping and navigation of the complex web of stakeholders that influence mining success, developing strategies for constructive engagement.</p>
                </div>
                <div class="approach-card">
                    <h3>Government Relations Architecture</h3>
                    <p>Sophisticated strategies that align with political realities while advancing client objectives through relationship development and effective messaging.</p>
                </div>
                <div class="approach-card">
                    <h3>Political Risk Mitigation</h3>
                    <p>Transformation of political risk assessment into practical risk management strategies with clear contingency planning for adverse developments.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="testimonials" class="testimonials">
        <div class="container">
            <h2>Client Success Stories</h2>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <p class="testimonial-text">"MineralEdge Advisory provided us with intelligence about pending regulatory changes that allowed us to restructure our manganese investment before our competitors even recognized the risk. Their political insights translated directly to competitive advantage."</p>
                    <p class="testimonial-author">— Director of International Investments, Saudi Mining Conglomerate</p>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">"Their understanding of ministerial priorities and decision-making processes proved invaluable in securing our mining license renewal under challenging circumstances. The team's government relations strategy turned a potentially disastrous situation into a strengthened relationship with regulatory authorities."</p>
                    <p class="testimonial-author">— CEO, Joint Saudi-South African Mining Venture</p>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">"When community protests threatened to shut down our operation indefinitely, MineralEdge's stakeholder mapping and engagement strategy transformed what had been a contentious relationship into a productive partnership."</p>
                    <p class="testimonial-author">— Operations Director, Platinum Mining Investment</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="contact">
        <div class="container">
            <h2>Contact Us</h2>
            <div class="contact-grid">
                <div class="contact-info">
                    <h3>Our Offices</h3>
                    <div class="contact-item">
                        <span class="contact-icon">📍</span>
                        <div>
                            <strong>Johannesburg Headquarters</strong><br>
                            Mining District Tower<br>
                            123 Mineral Street<br>
                            Sandton, Johannesburg<br>
                            South Africa<br>
                            +27 11 000 0000
                        </div>
                    </div>
                    <div class="contact-item">
                        <span class="contact-icon">📍</span>
                        <div>
                            <strong>Riyadh Office</strong><br>
                            Kingdom Center, Level 30<br>
                            King Fahd Road<br>
                            Riyadh<br>
                            Saudi Arabia<br>
                            +966 11 000 0000
                        </div>
                    </div>
                    <div class="contact-item">
                        <span class="contact-icon">✉️</span>
                        <div>
                            <strong>Email</strong><br>
                            info@mineraledge.com
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <h3>Send us a Message</h3>
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
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-col">
                    <h3>About Us</h3>
                    <p>MineralEdge Advisory is a specialized political risk and strategic advisory firm focused exclusively on the mineral resources sector in South Africa, with particular expertise in facilitating Saudi Arabian investment into the region.</p>
                </div>
                <div class="footer-col">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#approach">Our Approach</a></li>
                        <li><a href="#testimonials">Case Studies</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>Sector Expertise</h3>
                    <ul>
                        <li><a href="#">Critical Battery Minerals</a></li>
                        <li><a href="#">Precious Metals</a></li>
                        <li><a href="#">Industrial Minerals</a></li>
                        <li><a href="#">Rare Earth Elements</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>Connect With Us</h3>
                    <p>Follow our latest insights and updates on social media.</p>
                    <div style="margin-top: 15px;">
                        <a href="#" style="color: white; margin-right: 15px; font-size: 20px;">📱</a>
                        <a href="#" style="color: white; margin-right: 15px; font-size: 20px;">📘</a>
                        <a href="#" style="color: white; margin-right: 15px; font-size: 20px;">📸</a>
                        <a href="#" style="color: white; font-size: 20px;">📊</a>
                    </div>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2025 MineralEdge Advisory. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
