# website

11.24 07:46
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Discover the Philippines</title>
    <style>
        /* Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* Header Styles */
        header {
            background-color: #0038a8;
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: #ffcc02;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1596422846543-75e6d59bf25e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 100vh;
            color: white;
            display: flex;
            align-items: center;
            text-align: center;
        }
        
        .hero-content h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.5);
        }
        
        .hero-content p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: #ffcc02;
            color: #0038a8;
            padding: 0.8rem 1.5rem;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #ffd84d;
        }
        
        /* Section Styles */
        section {
            padding: 5rem 0;
        }
        
        section h2 {
            text-align: center;
            margin-bottom: 3rem;
            color: #0038a8;
            font-size: 2.5rem;
        }
        
        /* About Section */
        .about-content {
            display: flex;
            align-items: center;
            gap: 3rem;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* Destinations Section */
        .destinations {
            background-color: #e9f0fa;
        }
        
        .destination-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .card:hover {
            transform: translateY(-10px);
        }
        
        .card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .card-content {
            padding: 1.5rem;
        }
        
        .card h3 {
            color: #0038a8;
            margin-bottom: 0.5rem;
        }
        
        /* Culture Section */
        .culture-items {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .culture-item {
            text-align: center;
            padding: 2rem;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .culture-item i {
            font-size: 3rem;
            color: #0038a8;
            margin-bottom: 1rem;
        }
        
        .culture-item h3 {
            color: #0038a8;
            margin-bottom: 1rem;
        }
        
        /* Footer */
        footer {
            background-color: #0038a8;
            color: white;
            padding: 3rem 0;
            text-align: center;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .footer-logo {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 1rem;
        }
        
        .footer-links {
            display: flex;
            gap: 2rem;
            margin-bottom: 1.5rem;
        }
        
        .footer-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: #ffcc02;
        }
        
        .copyright {
            margin-top: 1rem;
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 1rem;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 0.75rem;
            }
            
            .hero-content h1 {
                font-size: 2rem;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .footer-links {
                flex-direction: column;
                gap: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">Discover Philippines</div>
                <nav>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#destinations">Destinations</a></li>
                        <li><a href="#culture">Culture</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Welcome to the Philippines</h1>
                <p>Discover the beauty of 7,641 islands with pristine beaches, vibrant culture, and warm hospitality.</p>
                <a href="#destinations" class="btn">Explore Destinations</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <h2>About the Philippines</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>The Philippines is an archipelago in Southeast Asia, consisting of over 7,600 islands. It's known for its rich biodiversity, stunning landscapes, and warm, friendly people.</p>
                    <p>The country has a unique blend of Eastern and Western cultures, with influences from Malay, Chinese, Spanish, and American heritage. This diversity is reflected in its food, festivals, and traditions.</p>
                    <p>From the bustling capital of Manila to the tranquil beaches of Palawan, the Philippines offers a wide range of experiences for every type of traveler.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1558642084-fd07fae5282e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Philippine landscape">
                </div>
            </div>
        </div>
    </section>

    <!-- Destinations Section -->
    <section id="destinations" class="destinations">
        <div class="container">
            <h2>Popular Destinations</h2>
            <div class="destination-cards">
                <div class="card">
                    <img src="https://images.unsplash.com/photo-1526951521990-620dc14c214b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Palawan">
                    <div class="card-content">
                        <h3>Palawan</h3>
                        <p>Home to the Puerto Princesa Underground River and stunning lagoons, Palawan is often called the last ecological frontier of the Philippines.</p>
                    </div>
                </div>
                <div class="card">
                    <img src="https://images.unsplash.com/photo-1565962595476-06d6bb4c0e5c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Boracay">
                    <div class="card-content">
                        <h3>Boracay</h3>
                        <p>Famous for its powdery white sand beaches and vibrant nightlife, Boracay is one of the top beach destinations in the world.</p>
                    </div>
                </div>
                <div class="card">
                    <img src="https://images.unsplash.com/photo-1565962590998-32f1c6ef151d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Cebu">
                    <div class="card-content">
                        <h3>Cebu</h3>
                        <p>Known for its historical landmarks, beautiful waterfalls, and vibrant city life, Cebu offers a perfect mix of urban and natural attractions.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Culture Section -->
    <section id="culture" class="culture">
        <div class="container">
            <h2>Filipino Culture</h2>
            <div class="culture-items">
                <div class="culture-item">
                    <h3>Festivals</h3>
                    <p>The Philippines is known for its vibrant festivals like Sinulog, Ati-Atihan, and Pahiyas that showcase the country's rich cultural heritage.</p>
                </div>
                <div class="culture-item">
                    <h3>Cuisine</h3>
                    <p>Filipino food is a unique fusion of flavors, with popular dishes like adobo, sinigang, and lechon enjoyed across the country.</p>
                </div>
                <div class="culture-item">
                    <h3>Hospitality</h3>
                    <p>Filipinos are known for their warm hospitality and strong family values, making visitors feel welcome and at home.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">Discover Philippines</div>
                <div class="footer-links">
                    <a href="#home">Home</a>
                    <a href="#about">About</a>
                    <a href="#destinations">Destinations</a>
                    <a href="#culture">Culture</a>
                </div>
                <p class="copyright">&copy; 2023 Discover Philippines. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
