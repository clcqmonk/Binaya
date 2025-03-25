<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>John Doe | BDMS Community Services</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
        }

        body {
            font-family: 'Segoe UI', system-ui, sans-serif;
            line-height: 1.6;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            color: var(--primary-color);
        }

        .header {
            display: flex;
            align-items: center;
            gap: 2rem;
            margin-bottom: 3rem;
            padding: 2rem;
            background: white;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .profile-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--secondary-color);
        }

        .contact-bar {
            background: var(--primary-color);
            color: white;
            padding: 1rem;
            border-radius: 10px;
            margin: 2rem 0;
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .social-links {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            margin: 2rem 0;
        }

        .social-card {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            transition: transform 0.3s ease;
            text-align: center;
        }

        .social-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .downloads-section {
            margin: 3rem 0;
        }

        .flyer-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 1.5rem;
        }

        .flyer-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .flyer-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .flyer-card p {
            padding: 1rem;
            text-align: center;
        }

        a {
            color: var(--secondary-color);
            font-weight: 500;
        }

        h1 { color: var(--primary-color); }
        h2 { color: var(--secondary-color); }
        h3 { color: var(--accent-color); margin-top: 2rem; }
    </style>
</head>
<body>
    <div class="header">
        <!-- 🔽 Upload your digital card to repository and update src -->
        <img src="your-digital-card.png" alt="BDMS Digital Card" class="profile-img">
        <div>
            <h1>Binay K Sharma</h1>
            <h2>Founder & Director</h2>
            <p>BDMS Community Services</p>
            <p>NDIS Registered Provider</p>
        </div>
    </div>

    <div class="contact-bar">
        <div>📞 1300 108 512</div> <div>📞08 8948 5753</div> <div>📞0412447312</div>
        <div>✉️ www.bdmscommunityservices.com.au</div>
        <div>✉️ info@bdmscommunityservices.com.au</div>
        <div>📍 Darwin | Sydney</div>
    </div>

    <div class="social-links">

    <a href="https://www.facebook.com/BDMSCSNSW" class="social-card">
            <h3>Facebook/X</h3>
            <p> Connect with us</p>
        </a>
        
        <a href="[https://linkedin.com/in/binay-kumar-sharma-1545539a/" class="social-card">
            <h3>LinkedIn</h3>
            <p>Connect Professionally</p>
        </a>
        <a href="https://youtube.com/@bdmscommunityservices8981" class="social-card">
            <h3>YouTube</h3>
            <p>Watch Our Videos</p>
        </a>
        
    </div>

    <div class="downloads-section">
        <h3>Company Resources</h3>
        <div class="flyer-gallery">
            <!-- 🔽 Add your flyer images and update src -->
            <div class="flyer-card">
                <img src="service-flyer-1.jpg" alt="Our Services">
                <p>Service Overview <a href="bdms-services.pdf" download>Download PDF</a></p>
            </div>
            <div class="flyer-card">
                <img src="ndis-flyer-2.jpg" alt="NDIS Information">
                <p>NDIS Guide <a href="ndis-guide.pdf" download>Download PDF</a></p>
            </div>
        </div>
    </div>

    <script>
        // Simple smooth scroll behavior
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add current year to footer
        document.addEventListener('DOMContentLoaded', function() {
            document.getElementById('current-year').textContent = new Date().getFullYear();
        });
    </script>

    <!-- Add this footer section before </body> -->
    <footer style="text-align: center; margin-top: 3rem; padding: 2rem; background: var(--primary-color); color: white; border-radius: 10px;">
        <p>© <span id="current-year">2023</span> BDMS Community Services. All rights reserved.</p>
    </footer>
</body>
</html>
