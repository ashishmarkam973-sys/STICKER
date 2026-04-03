# STICKER
IT IS WHEN I HAVE NEWLY LEARNED ABOUT IT
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>StickerHub - Premium Stickers Collection</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 2rem;
            font-weight: bold;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #ff6b6b;
        }

        .hero {
            text-align: center;
            padding: 4rem 0;
            color: white;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .cta-button {
            display: inline-block;
            background: #ff6b6b;
            color: white;
            padding: 1rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s;
            box-shadow: 0 10px 30px rgba(255, 107, 107, 0.4);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(255, 107, 107, 0.6);
        }

        .categories {
            padding: 4rem 0;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }

        .category-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .category-card {
            background: white;
            border-radius: 20px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 10px 40px rgba(0,0,0,0.1);
            transition: all 0.3s;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .category-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 60px rgba(0,0,0,0.2);
        }

        .category-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #ff6b6b, #4ecdc4, #45b7d1);
        }

        .category-icon {
            font-size: 4rem;
            margin-bottom: 1rem;
        }

        .sticker-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
            padding: 2rem 0;
        }

        .sticker-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s;
            position: relative;
        }

        .sticker-card:hover {
            transform: translateY(-5px) scale(1.02);
            box-shadow: 0 20px 50px rgba(0,0,0,0.2);
        }

        .sticker-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
            background: linear-gradient(45deg, #f0f0f0, #e0e0e0);
        }

        .sticker-info {
            padding: 1.5rem;
        }

        .sticker-name {
            font-size: 1.2rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
            color: #333;
        }

        .sticker-price {
            font-size: 1.5rem;
            font-weight: bold;
            color: #ff6b6b;
            margin-bottom: 1rem;
        }

        .add-to-cart {
            width: 100%;
            background: linear-gradient(45deg, #ff6b6b, #ff8e8e);
            color: white;
            border: none;
            padding: 0.8rem;
            border-radius: 10px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
        }

        .add-to-cart:hover {
            transform: scale(1.05);
        }

        .features {
            padding: 4rem 0;
            text-align: center;
            color: white;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature {
            background: rgba(255, 255, 255, 0.1);
            padding: 2rem;
            border-radius: 20px;
            backdrop-filter: blur(10px);
        }

        .footer {
            background: rgba(0, 0, 0, 0.8);
            color: white;
            text-align: center;
            padding: 3rem 0;
            margin-top: 4rem;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .nav-links {
                display: none;
            }
            
            .sticker-grid {
                grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            }
        }

        .active-category {
            border: 3px solid #ff6b6b;
            background: linear-gradient(135deg, #ff6b6b, #ff8e8e);
            color: white;
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <div class="logo">StickerHub 🎨</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#categories">Categories</a></li>
                <li><a href="#popular">Popular</a></li>
                <li><a href="#contact">Contact</a></li>
                <a href="#" class="cta-button" style="padding: 0.5rem 1.5rem; font-size: 1rem;">🛒 Cart (0)</a>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="container">
            <h1>StickerHub</h1>
            <p>Discover thousands of premium stickers for every vibe ✨</p>
            <a href="#categories" class="cta-button">Browse Stickers</a>
        </div>
    </section>

    <section id="categories" class="categories">
        <div class="container">
            <h2 class="section-title">Choose Your Style</h2>
            <div class="category-grid">
                <div class="category-card" data-category="anime">
                    <div class="category-icon">🎌</div>
                    <h3>Anime Stickers</h3>
                    <p>200+ designs</p>
                </div>
                <div class="category-card" data-category="gaming">
                    <div class="category-icon">🎮</div>
                    <h3>Gaming Stickers</h3>
                    <p>150+ designs</p>
                </div>
                <div class="category-card" data-category="nature">
                    <div class="category-icon">🌿</div>
                    <h3>Nature Stickers</h3>
                    <p>180+ designs</p>
                </div>
                <div class="category-card" data-category="funny">
                    <div class="category-icon">😂</div>
                    <h3>Funny Stickers</h3>
                    <p>300+ designs</p>
                </div>
                <div class="category-card" data-category="quotes">
                    <div class="category-icon">💭</div>
                    <h3>Quote Stickers</h3>
                    <p>120+ designs</p>
                </div>
                <div class="category-card" data-category="custom">
                    <div class="category-icon">✨</div>
                    <h3>Custom Design</h3>
                    <p>Make your own!</p>
                </div>
            </div>

            <h3 id="sticker-title" class="section-title" style="display: none;">All Popular Stickers</h3>
            <div id="sticker-grid" class="sticker-grid" style="display: none;">
                <!-- Stickers will be generated here -->
            </div>
        </div>
    </section>

    <section class="features">
        <div class="container">
            <h2 class="section-title">Why Choose StickerHub?</h2>
            <div class="features-grid">
                <div class="feature">
                    <div style="font-size: 3rem; margin-bottom: 1rem;">⚡</div>
                    <h3>Fast Shipping</h3>
                    <p>Delivered in 3-5 days worldwide</p>
                </div>
                <div class="feature">
                    <div style="font-size: 3rem; margin-bottom: 1rem;">💎</div>
                    <h3>Premium Quality</h3>
                    <p>Vinyl stickers that last 5+ years</p>
                </div>
                <div class="feature">
                    <div style="font-size: 3rem; margin-bottom: 1rem;">🛡️</div>
                    <h3>100% Satisfaction</h3>
                    <p>Free returns & exchanges</p>
                </div>
                <div class="feature">
                    <div style="font-size: 3rem; margin-bottom: 1rem;">💰</div>
                    <h3>Best Prices</h3>
                    <p>Starting at just $1.99</p>
                </div>
            </div>
        </div>
    </section>

    <footer class="footer">
        <div class="container">
            <h3>StickerHub © 2024</h3>
            <p>Stick with the best! 🎉</p>
        </div>
    </footer>

    <script>
        // Sample stickers data
        const stickers = [
            { id: 1, name: "Cute Cat", price: 2.99, category: "all", image: "🐱" },
            { id: 2, name: "Space Rocket", price: 3.49, category: "all", image: "🚀" },
            { id: 3, name: "Pizza Slice", price: 1.99, category: "funny", image: "🍕" },
            { id: 4, name: "Mountain View", price: 2.79, category: "nature", image: "⛰️" },
            { id: 5, name: "Game Controller", price: 3.29, category: "gaming", image: "🎮" },
            { id: 6, name: "Anime Girl", price: 4.99, category: "anime", image: "🎌" },
            { id: 7, name: "Coffee Cup", price: 2.49, category: "all", image: "☕" },
            { id: 8, name: "Sunset Beach", price: 3.19, category: "nature", image: "🌅" },
            { id: 9, name: "Funny Doge", price: 2.29, category: "funny", image: "🐕" },
            { id: 10, name: "Cyberpunk City", price: 3.99, category: "gaming", image: "🌃" },
            { id: 11, name: "Motivational Quote", price: 2.89, category: "quotes", image: "💪" },
            { id: 12, name: "Sakura Flower", price: 2.69, category: "anime", image: "🌸" }
        ];

        let cartCount = 0;

        // Category filter functionality
        document.querySelectorAll('.category-card').forEach(card => {
            card.addEventListener('click', () => {
                document.querySelectorAll('.category-card').forEach(c => c.classList.remove('active-category'));
                card.classList.add('active-category');
                
                document.getElementById('sticker-title').style.display = 'block';
                document.getElementById('sticker-grid').style.display = 'grid';
                
                displayStickers('all');
            });
        });

        function displayStickers(category = 'all') {
            const grid = document.getElementById('sticker-grid');
            grid.innerHTML = '';

            const filteredStickers = category === 'all' 
                ? stickers 
                : stickers.filter(sticker => sticker.category === category);

            filteredStickers.forEach(sticker => {
                const stickerCard = document.createElement('div');
                stickerCard.className = 'sticker-card';
                stickerCard.innerHTML = `
                    <div class="sticker-image" style="background: linear-gradient(45deg, ${getRandomColor()}, ${getRandomColor()}); display: flex; align-items: center; justify-content: center; font-size: 4rem;">
                        ${sticker.image}
                    </div>
                    <div class="sticker-info">
                        <div class="sticker-name">${sticker.name}</div>
                        <div class="sticker-price">$${sticker.price}</div>
                        <button class="add-to-cart" onclick="addToCart(${sticker.id})">Add to Cart</button>
                    </div>
                `;
                grid.appendChild(stickerCard);
            });
        }

        function getRandomColor() {
            const colors = ['#ff6b6b', '#4ecdc4', '#45b7d1', '#f9ca24', '#ff9f43', '#6c5ce7'];
            return colors[Math.floor(Math.random() * colors.length)];
        }

        function addToCart(id) {
            cartCount++;
            updateCartCount();
            // Simple notification
            showNotification('Added to cart! 🎉');
        }

        function updateCartCount() {
            const cartButtons = document.querySelectorAll('.cta-button');
            cartButtons.forEach(btn => {
                btn.textContent = `🛒 Cart (${cartCount})`;
            });
        }

        function showNotification(message) {
            const notification = document.createElement('div');
            notification.style.cssText = `
                position: fixed;
                top: 20px;
                right: 20px;
                background: #ff6b6b;
                color: white;
                padding: 1rem 2rem;
                border-radius: 10px;
                box-shadow: 0 10px 30px rgba(0,0,0,0.3);
                z-index: 1000;
                animation: slideIn 0.3s ease;
            `;
            notification.textContent = message;
            document.body.appendChild(notification);

            setTimeout(() => {
                notification.remove();
            }, 3000);
        }

        // Smooth scrolling for nav links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Initialize
        displayStickers();
    </script>
</body>
</html>
