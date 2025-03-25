<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>John Doe | BDMS Community Services</title>
    <style>
        :root {
            --primary: #2A5C82;
            --secondary: #5DA9E9;
            --accent: #FF6B6B;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', sans-serif;
            line-height: 1.6;
            background: #f8f9fa;
            color: #333;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .hero {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            padding: 4rem 2rem;
            border-radius: 15px;
            margin-bottom: 2rem;
            text-align: center;
        }

        .profile-grid {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 2rem;
            margin-top: 2rem;
        }

        .digital-card {
            background: white;
            border-radius: 15px;
            padding: 1rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .digital-card img {
            width: 100%;
            border-radius: 10px;
        }

        .services {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            margin-top: 2rem;
        }

        .flyer-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .flyer-card {
            border: 1px solid #eee;
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s ease;
        }

        .flyer-card:hover {
            transform: translateY(-5px);
        }

        .flyer-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .contact-bar {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 2rem 0;
            flex-wrap: wrap;
        }

        .social-link {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            color: var(--primary);
            text-decoration: none;
            padding: 0.5rem 1rem;
            border-radius: 25px;
            background: rgba(255,255,255,0.9);
            transition: all 0.3s ease;
        }

        .social-link:hover {
            background: var(--primary);
            color: white;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="hero">
            <h1>John Doe</h1>
            <p>Founder & Director</p>
            <h2>BDMS Community Services</h2>
            <p>NDIS Registered Provider Since 2019</p>
        </div>

        <div class="profile-grid">
            <div class="digital-card">
                <!-- Replace with your digital card image -->
                <img src="digital-card.png" alt="Digital Visiting Card">
            </div>

            <div class="services">
                <h3>Our Services</h3>
                <ul>
                    <li>Disability Support Services</li>
                    <li>Behavioral Support (BOC)</li>
                    <li>Community Participation</li>
                    <li>Therapeutic Support</li>
                </ul>

                <div class="contact-bar">
                    <a href="tel:+61123456789" class="social-link">📞 +61 123 456 789</a>
                    <a href="mailto:contact@bdms.com" class="social-link">✉️ contact@bdms.com</a>
                </div>
            </div>
        </div>

        <div class="flyer-gallery">
            <!-- Add your flyer images -->
            <div class="flyer-card">
                <img src="service-flyer-1.jpg" alt="Services Flyer">
                <div style="padding: 1rem;">
                    <h4>Our Services</h4>
                    <a href="services.pdf" download class="social-link">Download PDF</a>
                </div>
            </div>

            <div class="flyer-card">
                <img src="ndis-flyer.jpg" alt="NDIS Information">
                <div style="padding: 1rem;">
                    <h4>NDIS Guide</h4>
                    <a href="ndis-guide.pdf" download class="social-link">Download PDF</a>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Simple animation on scroll
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        });

        document.querySelectorAll('.flyer-card, .digital-card').forEach((el) => {
            el.style.opacity = 0;
            el.style.transform = 'translateY(20px)';
            el.style.transition = 'all 0.6s ease-out';
            observer.observe(el);
        });
    </script>
</body>
</html>
