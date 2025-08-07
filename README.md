<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TaxEase Legal (By Anurag) | GST & Tax Consultants</title>
  <!-- EmailJS Library -->
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
  <style>
    /* Global Styles */
    :root {
        --primary: #2c3e50;
        --secondary: #3498db;
        --accent: #e74c3c;
        --light: #ecf0f1;
        --dark: #2c3e50;
    }
    
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
    
    body {
        line-height: 1.6;
        color: #333;
        padding-top: 70px;
    }
    
    .container {
        width: 90%;
        max-width: 1200px;
        margin: 0 auto;
    }
    
    .btn {
        display: inline-block;
        background: var(--secondary);
        color: white;
        padding: 10px 20px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        text-decoration: none;
        font-size: 16px;
        transition: all 0.3s;
    }
    
    .btn:hover {
        background: #2980b9;
        transform: translateY(-2px);
    }
    
    .btn-accent {
        background: var(--accent);
    }
    
    .btn-accent:hover {
        background: #c0392b;
    }
    
    section {
        padding: 60px 0;
    }
    
    .section-title {
        text-align: center;
        margin-bottom: 40px;
        color: var(--primary);
        font-size: 2.2rem;
        position: relative;
    }
    
    .section-title::after {
        content: '';
        display: block;
        width: 80px;
        height: 4px;
        background: var(--secondary);
        margin: 15px auto 0;
    }
    
    /* Header Styles */
    header {
        background: white;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        position: fixed;
        width: 100%;
        top: 0;
        z-index: 1000;
    }
    
    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 15px 0;
    }
    
    .logo {
        font-size: 24px;
        font-weight: bold;
        color: var(--primary);
        text-decoration: none;
        display: flex;
        align-items: center;
    }
    
    .logo img {
        height: 40px;
        margin-right: 10px;
    }
    
    .nav-links {
        display: flex;
        list-style: none;
    }
    
    .nav-links li {
        margin-left: 30px;
    }
    
    .nav-links a {
        text-decoration: none;
        color: var(--dark);
        font-weight: 500;
        transition: color 0.3s;
        position: relative;
    }
    
    .nav-links a::after {
        content: '';
        position: absolute;
        width: 0;
        height: 2px;
        background: var(--secondary);
        bottom: -5px;
        left: 0;
        transition: width 0.3s;
    }
    
    .nav-links a:hover::after {
        width: 100%;
    }
    
    .mobile-menu-btn {
        display: none;
        background: none;
        border: none;
        font-size: 24px;
        cursor: pointer;
        color: var(--primary);
    }
    
    /* Hero Section */
    .hero {
        background: linear-gradient(rgba(44, 62, 80, 0.9), rgba(44, 62, 80, 0.9)), url('https://images.unsplash.com/photo-1450101499163-c8848c66ca85?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
        background-size: cover;
        background-position: center;
        height: 80vh;
        min-height: 500px;
        display: flex;
        align-items: center;
        text-align: center;
        color: white;
    }
    
    .hero-content {
        max-width: 800px;
        margin: 0 auto;
    }
    
    .hero h1 {
        font-size: 3rem;
        margin-bottom: 20px;
        line-height: 1.2;
    }
    
    .hero p {
        font-size: 1.2rem;
        margin-bottom: 30px;
    }
    
    /* Services Section */
    .services-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 30px;
    }
    
    .service-card {
        background: white;
        border-radius: 10px;
        overflow: hidden;
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        transition: all 0.3s;
    }
    
    .service-card:hover {
        transform: translateY(-10px);
        box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
    }
    
    .service-img {
        height: 200px;
        background-size: cover;
        background-position: center;
    }
    
    .service-content {
        padding: 25px;
    }
    
    .service-content h3 {
        margin-bottom: 15px;
        color: var(--primary);
        font-size: 1.5rem;
    }
    
    .service-content ul {
        list-style-position: inside;
        margin-bottom: 20px;
    }
    
    .service-content li {
        margin-bottom: 8px;
        color: #555;
    }
    
    /* About Section */
    .about {
        background: #f9f9f9;
    }
    
    .about-content {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 40px;
        align-items: center;
    }
    
    .about-text h3 {
        font-size: 1.8rem;
        color: var(--primary);
        margin-bottom: 20px;
    }
    
    .about-text p {
        margin-bottom: 15px;
        color: #555;
    }
    
    .about-img {
        border-radius: 10px;
        overflow: hidden;
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    }
    
    .about-img img {
        width: 100%;
        height: auto;
        display: block;
    }
    
    /* Appointment Section */
    .appointment {
        background: var(--light);
    }
    
    .appointment-container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 40px;
        align-items: center;
    }
    
    .appointment-info h3 {
        font-size: 1.8rem;
        color: var(--primary);
        margin-bottom: 20px;
    }
    
    .appointment-info ul {
        list-style: none;
        margin-bottom: 30px;
    }
    
    .appointment-info li {
        margin-bottom: 15px;
        display: flex;
        align-items: center;
    }
    
    .appointment-info i {
        margin-right: 10px;
        color: var(--secondary);
        font-size: 1.2rem;
    }
    
    .appointment-form {
        background: white;
        padding: 30px;
        border-radius: 10px;
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    }
    
    .form-group {
        margin-bottom: 20px;
    }
    
    .form-group label {
        display: block;
        margin-bottom: 8px;
        font-weight: 500;
        color: var(--primary);
    }
    
    .form-group input,
    .form-group select,
    .form-group textarea {
        width: 100%;
        padding: 12px;
        border: 1px solid #ddd;
        border-radius: 5px;
        font-size: 16px;
        transition: border 0.3s;
    }
    
    .form-group input:focus,
    .form-group select:focus,
    .form-group textarea:focus {
        border-color: var(--secondary);
        outline: none;
    }
    
    .form-group textarea {
        height: 120px;
        resize: vertical;
    }
    
    /* Testimonials */
    .testimonials {
        background: var(--primary);
        color: white;
    }
    
    .testimonials .section-title {
        color: white;
    }
    
    .testimonials .section-title::after {
        background: var(--accent);
    }
    
    .testimonial-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 30px;
    }
    
    .testimonial-card {
        background: rgba(255, 255, 255, 0.1);
        padding: 30px;
        border-radius: 10px;
        position: relative;
    }
    
    .testimonial-card::before {
        content: '"';
        position: absolute;
        top: 10px;
        left: 20px;
        font-size: 5rem;
        color: rgba(255, 255, 255, 0.1);
        font-family: serif;
        line-height: 1;
    }
    
    .testimonial-text {
        margin-bottom: 20px;
        font-style: italic;
        position: relative;
        z-index: 1;
    }
    
    .testimonial-author {
        display: flex;
        align-items: center;
    }
    
    .author-img {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        overflow: hidden;
        margin-right: 15px;
    }
    
    .author-img img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
    
    .author-info h4 {
        margin-bottom: 5px;
    }
    
    .author-info p {
        font-size: 0.9rem;
        opacity: 0.8;
    }
    
    /* Contact Section */
    .contact-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 30px;
    }
    
    .contact-card {
        text-align: center;
        padding: 30px;
        border-radius: 10px;
        background: white;
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        transition: all 0.3s;
    }
    
    .contact-card:hover {
        transform: translateY(-5px);
        box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
    }
    
    .contact-icon {
        font-size: 2.5rem;
        color: var(--secondary);
        margin-bottom: 20px;
    }
    
    .contact-card h3 {
        margin-bottom: 15px;
        color: var(--primary);
    }
    
    /* Footer */
    footer {
        background: var(--dark);
        color: white;
        padding: 60px 0 20px;
    }
    
    .footer-content {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 40px;
        margin-bottom: 40px;
    }
    
    .footer-column h3 {
        margin-bottom: 25px;
        font-size: 1.3rem;
        position: relative;
        padding-bottom: 10px;
    }
    
    .footer-column h3::after {
        content: '';
        position: absolute;
        bottom: 0;
        left: 0;
        width: 50px;
        height: 2px;
        background: var(--secondary);
    }
    
    .footer-column ul {
        list-style: none;
    }
    
    .footer-column ul li {
        margin-bottom: 12px;
    }
    
    .footer-column a {
        color: #bbb;
        text-decoration: none;
        transition: color 0.3s;
    }
    
    .footer-column a:hover {
        color: white;
    }
    
    .social-links {
        display: flex;
        gap: 15px;
        margin-top: 20px;
    }
    
    .social-links a {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        width: 40px;
        height: 40px;
        background: rgba(255, 255, 255, 0.1);
        border-radius: 50%;
        color: white;
        transition: all 0.3s;
    }
    
    .social-links a:hover {
        background: var(--secondary);
        transform: translateY(-3px);
    }
    
    .copyright {
        text-align: center;
        padding-top: 20px;
        border-top: 1px solid rgba(255, 255, 255, 0.1);
        color: #bbb;
        font-size: 0.9rem;
    }
    
    /* Responsive */
    @media (max-width: 992px) {
        .about-content,
        .appointment-container {
            grid-template-columns: 1fr;
        }
        
        .appointment-info {
            order: 2;
        }
        
        .appointment-form {
            order: 1;
        }
    }
    
    @media (max-width: 768px) {
        .mobile-menu-btn {
            display: block;
        }
        
        .nav-links {
            position: fixed;
            top: 70px;
            left: -100%;
            width: 100%;
            height: calc(100vh - 70px);
            background: white;
            flex-direction: column;
            align-items: center;
            padding: 40px 0;
            transition: left 0.3s;
        }
        
        .nav-links.active {
            left: 0;
        }
        
        .nav-links li {
            margin: 15px 0;
        }
        
        .hero h1 {
            font-size: 2.2rem;
        }
        
        .hero p {
            font-size: 1rem;
        }
    }
    /* WhatsApp and Call Now Buttons */
    .floating-contact-buttons {
        position: fixed;
        bottom: 30px;
        right: 30px;
        display: flex;
        flex-direction: column;
        gap: 15px;
        z-index: 999;
    }

    .floating-btn {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 60px;
        height: 60px;
        border-radius: 50%;
        color: white;
        font-size: 28px;
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        transition: all 0.3s;
        position: relative;
    }

    .floating-btn:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
    }

    .whatsapp-btn {
        background: #25D366;
    }

    .call-btn {
        background: var(--secondary);
    }

    .floating-btn .tooltip {
        position: absolute;
        right: 70px;
        background: var(--dark);
        color: white;
        padding: 5px 10px;
        border-radius: 5px;
        font-size: 14px;
        white-space: nowrap;
        opacity: 0;
        pointer-events: none;
        transition: opacity 0.3s;
    }

    .floating-btn:hover .tooltip {
        opacity: 1;
    }

    @media (max-width: 768px) {
        .floating-contact-buttons {
            bottom: 20px;
            right: 20px;
        }
        
        .floating-btn {
            width: 50px;
            height: 50px;
            font-size: 24px;
        }
    }

    /* Appointment Form Styles */
    .booking-container {
        background-color: white;
        border-radius: 8px;
        padding: 30px;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        max-width: 800px;
        margin: 0 auto;
    }

    .booking-title {
        color: #2c3e50;
        text-align: center;
        margin-bottom: 30px;
    }

    .required {
        color: red;
    }

    .time-slots {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 10px;
        margin-top: 10px;
    }

    .time-slot {
        padding: 10px;
        background: #f0f0f0;
        border: 1px solid #ddd;
        border-radius: 4px;
        text-align: center;
        cursor: pointer;
    }

    .time-slot.selected {
        background: #3498db;
        color: white;
        border-color: #2980b9;
    }

    .loading {
        display: none;
        text-align: center;
        margin-top: 20px;
    }

    .success-message {
        display: none;
        background-color: #d4edda;
        color: #155724;
        padding: 15px;
        border-radius: 4px;
        margin-top: 20px;
        text-align: center;
    }

    .error-message {
        display: none;
        background-color: #f8d7da;
        color: #721c24;
        padding: 15px;
        border-radius: 4px;
        margin-top: 20px;
        text-align: center;
    }

    .setup-instructions {
        background-color: #fff3cd;
        border-left: 4px solid #ffc107;
        padding: 15px;
        margin-bottom: 20px;
        border-radius: 4px;
    }

    code {
        background-color: #f0f0f0;
        padding: 2px 5px;
        border-radius: 3px;
        font-family: monospace;
    }
  </style>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo">
                    <img src="https://via.placeholder.com/40x40?text=NS" alt="Logo">
                    <span>TaxEase Legal (By Anurag)</span>
                </a>
                <button class="mobile-menu-btn">
                    <i class="fas fa-bars"></i>
                </button>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#appointment">Appointment</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Expert GST & Income Tax Services</h1>
                <p>Professional accounting solutions for businesses and individuals. Trusted by clients for GST filing, income tax preparation, and financial compliance.</p>
                <a href="#appointment" class="btn btn-accent">Book Free Consultation</a>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services">
        <div class="container">
            <h2 class="section-title">Our Services</h2>
            <div class="services-grid">
                <!-- GST Services -->
                <div class="service-card">
                    <div class="service-img" style="background-image: url('https://images.unsplash.com/photo-1554224155-6726b3ff858f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');"></div>
                    <div class="service-content">
                        <h3>GST Services</h3>
                        <ul>
                            <li>GST Registration & Migration</li>
                            <li>Monthly/Quarterly Return Filing</li>
                            <li>GST Compliance Advisory</li>
                            <li>GST Audit & Assessment</li>
                            <li>Refund Filing & Reconciliation</li>
                            <li>E-way Bill Compliance</li>
                        </ul>
                        <a href="#appointment" class="btn">Get Service</a>
                    </div>
                </div>
                
                <!-- Income Tax Services -->
                <div class="service-card">
                    <div class="service-img" style="background-image: url('https://images.unsplash.com/photo-1579621970563-ebec7560ff3e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');"></div>
                    <div class="service-content">
                        <h3>Income Tax Services</h3>
                        <ul>
                            <li>Income Tax Return Filing</li>
                            <li>Tax Planning & Advisory</li>
                            <li>TDS Compliance & Returns</li>
                            <li>Tax Audit Representation</li>
                            <li>Notice Handling & Appeals</li>
                            <li>Form 16/16A Generation</li>
                        </ul>
                        <a href="#appointment" class="btn">Get Service</a>
                    </div>
                </div>
                
                <!-- Balance Sheet Services -->
                <div class="service-card">
                    <div class="service-img" style="background-image: url('https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');"></div>
                    <div class="service-content">
                        <h3>Balance Sheet Services</h3>
                        <ul>
                            <li>Balance Sheet Preparation</li>
                            <li>Financial Statement Analysis</li>
                            <li>Annual Compliance Reporting</li>
                            <li>Bookkeeping & Accounting</li>
                            <li>Tax Audit Support</li>
                            <li>XBRL Filing Services</li>
                        </ul>
                        <a href="#appointment" class="btn">Get Service</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">About Our Firm</h2>
            <div class="about-content">
                <div class="about-text">
                    <h3>TaxEase Legal (By Anurag)</h3>
                    <p>Founded in 2010, TaxEase Legal has grown to become a trusted name in taxation and financial services. Our firm specializes in providing comprehensive GST, income tax, and accounting solutions to businesses of all sizes.</p>
                    <p>With a team of qualified professionals, we combine technical expertise with personalized service to ensure our clients remain compliant while optimizing their financial position. Our approach focuses on understanding each client's unique needs and delivering tailored solutions.</p>
                    <p>We stay updated with the latest changes in tax laws and accounting standards to provide accurate and timely advice. Whether you're a startup needing GST registration or an established business requiring complex tax planning, we have the knowledge and experience to guide you.</p>
                    <a href="#appointment" class="btn">Consult With Us</a>
                </div>
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1521791055366-0d553872125f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Our Office">
                </div>
            </div>
        </div>
    </section>

    <!-- Appointment Section -->
    <section class="appointment" id="appointment">
        <div class="container">
            <h2 class="section-title">Book an Appointment</h2>
            <div class="appointment-container">
                <div class="appointment-form">
                    <form id="bookingForm">
                        <div class="form-group">
                            <label for="appointmentName">Full Name <span class="required">*</span></label>
                            <input type="text" id="appointmentName" name="name" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="appointmentEmail">Email <span class="required">*</span></label>
                            <input type="email" id="appointmentEmail" name="email" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="appointmentPhone">Phone Number <span class="required">*</span></label>
                            <input type="tel" id="appointmentPhone" name="phone" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="appointmentService">Service Type <span class="required">*</span></label>
                            <select id="appointmentService" name="service" required>
                                <option value="">Select a service</option>
                                <option value="gst">GST Services</option>
                                <option value="income-tax">Income Tax Services</option>
                                <option value="balance-sheet">Balance Sheet Services</option>
                                <option value="consultation">General Consultation</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="appointmentDate">Preferred Date <span class="required">*</span></label>
                            <input type="date" id="appointmentDate" name="date" required>
                        </div>
                        
                        <div class="form-group">
                            <label>Preferred Time <span class="required">*</span></label>
                            <div class="time-slots">
                                <div class="time-slot" data-time="9:00 AM">9:00 AM</div>
                                <div class="time-slot" data-time="10:00 AM">10:00 AM</div>
                                <div class="time-slot" data-time="11:00 AM">11:00 AM</div>
                                <div class="time-slot" data-time="1:00 PM">1:00 PM</div>
                                <div class="time-slot" data-time="2:00 PM">2:00 PM</div>
                                <div class="time-slot" data-time="3:00 PM">3:00 PM</div>
                                <div class="time-slot" data-time="4:00 PM">4:00 PM</div>
                                <div class="time-slot" data-time="5:00 PM">5:00 PM</div>
                            </div>
                            <input type="hidden" id="selectedTime" name="selectedTime" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="appointmentNotes">Additional Notes</label>
                            <textarea id="appointmentNotes" name="notes" rows="3"></textarea>
                        </div>
                        
                        <button type="submit" class="btn">Book Appointment</button>
                    </form>
                    
                    <div id="loadingIndicator" class="loading">
                        <p>Submitting your appointment...</p>
                    </div>
                    
                    <div id="successMessage" class="success-message">
                        <h3>Appointment Booked Successfully!</h3>
                        <p>Your appointment details have been sent to: <strong>varshney8126@gmail.com</strong></p>
                        <p>You will also receive a confirmation at your provided email address.</p>
                    </div>
                    
                    <div id="errorMessage" class="error-message">
                        <h3>Error!</h3>
                        <p>There was a problem submitting your appointment. Please try again later or contact us directly.</p>
                    </div>
                </div>
                
                <div class="appointment-info">
                    <h3>Why Book With Us?</h3>
                    <ul>
                        <li><i class="fas fa-check-circle"></i> Expert tax consultants with 10+ years experience</li>
                        <li><i class="fas fa-check-circle"></i> Personalized service tailored to your needs</li>
                        <li><i class="fas fa-check-circle"></i> Transparent pricing with no hidden fees</li>
                        <li><i class="fas fa-check-circle"></i> Timely filing to avoid penalties</li>
                        <li><i class="fas fa-check-circle"></i> Dedicated support throughout the process</li>
                    </ul>
                    
                    <h3>Office Hours</h3>
                    <ul>
                        <li><i class="fas fa-clock"></i> Monday - Friday: 9:30 AM - 6:30 PM</li>
                        <li><i class="fas fa-clock"></i> Saturday: 10:00 AM - 2:00 PM</li>
                        <li><i class="fas fa-clock"></i> Sunday: Closed</li>
                    </ul>
                    
                    <h3>Need Immediate Help?</h3>
                    <p>For urgent matters outside office hours, please call us at <strong>+91 82796 85059</strong> or email <strong>support@TaxEaseLegal.com</strong></p>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials">
        <div class="container">
            <h2 class="section-title">Client Testimonials</h2>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <p class="testimonial-text">TaxEase Legal (By Anurag) has been handling our GST filings for the past 3 years. Their team is professional, knowledgeable, and always available to answer our queries. Highly recommended!</p>
                    <div class="testimonial-author">
                        <div class="author-img">
                            <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Rahul Sharma">
                        </div>
                        <div class="author-info">
                            <h4>Rahul Sharma</h4>
                            <p>Director, Sharma Traders</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">Excellent service for income tax filing. They saved me a significant amount in taxes through proper planning. The team is very responsive and explains everything in simple terms.</p>
                    <div class="testimonial-author">
                        <div class="author-img">
                            <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Priya Patel">
                        </div>
                        <div class="author-info">
                            <h4>Priya Patel</h4>
                            <p>Small Business Owner</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">We've been using their balance sheet services for our manufacturing unit. Their attention to detail and timely delivery has helped us maintain perfect financial records for audits.</p>
                    <div class="testimonial-author">
                        <div class="author-img">
                            <img src="https://randomuser.me/api/portraits/men/67.jpg" alt="Vikram Mehta">
                        </div>
                        <div class="author-info">
                            <h4>Vikram Mehta</h4>
                            <p>CEO, Mehta Industries</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Floating Contact Buttons -->
    <div class="floating-contact-buttons">
        <a href="https://wa.me/918279685059" class="floating-btn whatsapp-btn" target="_blank">
            <i class="fab fa-whatsapp"></i>
            <span class="tooltip">Chat on WhatsApp</span>
        </a>
        <a href="tel:+918279685059" class="floating-btn call-btn">
            <i class="fas fa-phone-alt"></i>
            <span class="tooltip">Call Now</span>
        </a>
    </div>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <h2 class="section-title">Contact Us</h2>
            <div class="contact-grid">
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fas fa-map-marker-alt"></i>
                    </div>
                    
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fas fa-phone-alt"></i>
                    </div>
                    <h3>Phone</h3>
                    <p>+91 82796 85059</p>
                    <p>Mon-Sat: 9:30 AM - 6:30 PM</p>
                </div>
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </div>
                    <h3>Email</h3>
                    <p>taxeaselegalbyanurag@gmail.com<br>support@TaxEaseLegal.com</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>TaxEase Legal</h3>
                    <p>Professional GST, Income Tax, and Accounting services for businesses and individuals. Your trusted financial partner.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#appointment">Appointment</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class
                                <div class="footer-column">
                    <h3>Services</h3>
                    <ul>
                        <li><a href="#services">GST Services</a></li>
                        <li><a href="#services">Income Tax</a></li>
                        <li><a href="#services">Balance Sheet</a></li>
                        <li><a href="#services">Tax Planning</a></li>
                        <li><a href="#services">Compliance</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Legal</h3>
                    <ul>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Terms of Service</a></li>
                        <li><a href="#">Disclaimer</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 TaxEase Legal (By Anurag). All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        document.querySelector('.mobile-menu-btn').addEventListener('click', function() {
            document.querySelector('.nav-links').classList.toggle('active');
        });
        
        // Close mobile menu when clicking a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                document.querySelector('.nav-links').classList.remove('active');
            });
        });
        
        // Initialize EmailJS with your public key
        emailjs.init("DL8AlM6Bk5spToHGa"); // Replace with your actual public key
        
        // Set minimum date to today for appointment booking
        const today = new Date().toISOString().split('T')[0];
        document.getElementById('appointmentDate').min = today;
        
        // Time slot selection functionality
        const timeSlots = document.querySelectorAll('.time-slot');
        timeSlots.forEach(slot => {
            slot.addEventListener('click', function() {
                // Remove selected class from all slots
                timeSlots.forEach(s => s.classList.remove('selected'));
                
                // Add selected class to clicked slot
                this.classList.add('selected');
                
                // Update hidden input
                document.getElementById('selectedTime').value = this.dataset.time;
            });
        });
        
        // Form submission handling
        const bookingForm = document.getElementById('bookingForm');
        bookingForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Validate form
            if (!validateBookingForm()) {
                return;
            }
            
            // Show loading indicator
            document.getElementById('loadingIndicator').style.display = 'block';
            document.querySelector('#bookingForm button[type="submit"]').disabled = true;
            
            // Get form data
            const formData = {
                name: document.getElementById('appointmentName').value,
                email: document.getElementById('appointmentEmail').value,
                phone: document.getElementById('appointmentPhone').value,
                service: document.getElementById('appointmentService').value,
                date: document.getElementById('appointmentDate').value,
                time: document.getElementById('selectedTime').value,
                notes: document.getElementById('appointmentNotes').value || "No additional notes",
                admin_email: "varshney8126@gmail.com" // Admin email for notifications
            };
            
            // Send email using EmailJS
            emailjs.send(
                "Appointment Service", // Replace with your EmailJS service ID
                "template_qwjr4rb", // Replace with your EmailJS template ID
                formData
            ).then(function(response) {
                console.log('SUCCESS!', response.status, response.text);
                
                // Hide loading indicator
                document.getElementById('loadingIndicator').style.display = 'none';
                document.querySelector('#bookingForm button[type="submit"]').disabled = false;
                
                // Show success message
                document.getElementById('successMessage').style.display = 'block';
                
                // Reset form
                bookingForm.reset();
                timeSlots.forEach(s => s.classList.remove('selected'));
                document.getElementById('selectedTime').value = '';
                
                // Scroll to success message
                document.getElementById('successMessage').scrollIntoView({ behavior: 'smooth' });
                
                // Hide success message after 5 seconds
                setTimeout(() => {
                    document.getElementById('successMessage').style.display = 'none';
                }, 5000);
                
            }, function(error) {
                console.log('FAILED...', error);
                
                // Hide loading indicator
                document.getElementById('loadingIndicator').style.display = 'none';
                document.querySelector('#bookingForm button[type="submit"]').disabled = false;
                
                // Show error message
                document.getElementById('errorMessage').style.display = 'block';
                document.getElementById('errorMessage').scrollIntoView({ behavior: 'smooth' });
                
                // Hide error message after 5 seconds
                setTimeout(() => {
                    document.getElementById('errorMessage').style.display = 'none';
                }, 5000);
            });
        });
        
        function validateBookingForm() {
            // Basic validation
            const requiredFields = [
                'appointmentName', 
                'appointmentEmail', 
                'appointmentPhone', 
                'appointmentService', 
                'appointmentDate', 
                'selectedTime'
            ];
            let isValid = true;
            
            requiredFields.forEach(field => {
                const element = document.getElementById(field);
                if (!element.value) {
                    isValid = false;
                    element.style.borderColor = 'red';
                    
                    // Scroll to first invalid field
                    if (isValid === false) {
                        element.scrollIntoView({ behavior: 'smooth', block: 'center' });
                        isValid = null; // Prevent scrolling to other fields
                    }
                } else {
                    element.style.borderColor = '#ddd';
                }
            });
            
            // Email validation
            const email = document.getElementById('appointmentEmail').value;
            if (email && !validateEmail(email)) {
                isValid = false;
                document.getElementById('appointmentEmail').style.borderColor = 'red';
                alert('Please enter a valid email address');
            }
            
            return isValid;
        }
        
        function validateEmail(email) {
            const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return re.test(email);
        }
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 70,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>
