# Websy<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pampered Paws Pet Spa</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            line-height: 1.6;
        }

        header {
            background: #4CAF50;
            color: white;
            padding: 1rem;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: bold;
        }

        .hero {
            height: 80vh;
            background: url('https://images.unsplash.com/photo-1587300003388-59208cc962cb') center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 60px;
        }

        .hero-content h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .services {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .service-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .service-card {
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        footer {
            background: #333;
            color: white;
            padding: 2rem;
            text-align: center;
        }

        .contact {
            padding: 4rem 2rem;
            background: #f4f4f4;
        }

        form {
            max-width: 600px;
            margin: 0 auto;
        }

        input, textarea {
            width: 100%;
            padding: 0.5rem;
            margin-bottom: 1rem;
        }

        button {
            background: #4CAF50;
            color: white;
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero-content h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <h1>Pampered Paws</h1>
            <div class="nav-links">
                <a href="#home">Home</a>
                <a href="#services">Services</a>
                <a href="#contact">Contact</a>
            </div>
        </nav>
    </header>

    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Premium Pet Care Services</h1>
            <p>Your pets deserve the best care and relaxation</p>
        </div>
    </section>

    <section class="services" id="services">
        <h2>Our Services</h2>
        <div class="service-grid">
            <div class="service-card">
                <h3>Full Spa Treatment</h3>
                <p>Bath, massage, nail trimming, and styling</p>
            </div>
            <div class="service-card">
                <h3>Wellness Checkups</h3>
                <p>Professional veterinary examinations</p>
            </div>
            <div class="service-card">
                <h3>Pet Hotel</h3>
                <p>Luxury overnight stays with 24/7 care</p>
            </div>
        </div>
    </section>

    <section class="contact" id="contact">
        <h2>Book an Appointment</h2>
        <form>
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <input type="tel" placeholder="Phone Number" required>
            <textarea placeholder="Message" rows="5" required></textarea>
            <button type="submit">Send Request</button>
        </form>
    </section>

    <footer>
        <p>© 2023 Pampered Paws Pet Spa. All rights reserved.</p>
        <p>123 Pet Care Lane, Anytown, ST 12345</p>
        <p>Phone: (555) 123-4567</p>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Mobile menu toggle
        const mobileMenu = () => {
            const nav = document.querySelector('.nav-links');
            nav.style.display = nav.style.display === 'flex' ? 'none' : 'flex';
        }
    </script>
</body>
</html>
