<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mudisch Elektronik - TV Satış & Tamir</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }

        header {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 28px;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav-wrapper {
            display: flex;
            align-items: center;
            gap: 30px;
        }

        nav {
            display: flex;
            gap: 30px;
            align-items: center;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: opacity 0.3s;
        }

        nav a:hover {
            opacity: 0.8;
        }

        .language-selector {
            display: flex;
            gap: 10px;
            align-items: center;
            border-left: 1px solid rgba(255,255,255,0.3);
            padding-left: 20px;
        }

        .lang-btn {
            background: none;
            border: none;
            cursor: pointer;
            font-size: 24px;
            transition: transform 0.3s;
            opacity: 0.7;
        }

        .lang-btn:hover {
            transform: scale(1.2);
            opacity: 1;
        }

        .lang-btn.active {
            opacity: 1;
            transform: scale(1.3);
        }

        .cta-button {
            background-color: #ff6b35;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
        }

        .cta-button:hover {
            background-color: #e55a2b;
        }

        .hero {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 80px 20px;
            text-align: center;
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
            opacity: 0.95;
        }

        .hero-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 15px 40px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary {
            background-color: #ff6b35;
            color: white;
        }

        .btn-primary:hover {
            background-color: #e55a2b;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(255,107,53,0.3);
        }

        .btn-secondary {
            background-color: white;
            color: #1e3c72;
        }

        .btn-secondary:hover {
            background-color: #f0f0f0;
            transform: translateY(-2px);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 60px 20px;
        }

        .section-title {
            text-align: center;
            font-size: 36px;
            margin-bottom: 50px;
            color: #1e3c72;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }

        .service-card {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }

        .service-icon {
            font-size: 50px;
            margin-bottom: 20px;
        }

        .service-card h3 {
            color: #1e3c72;
            margin-bottom: 15px;
            font-size: 22px;
        }

        .service-card p {
            color: #666;
            line-height: 1.8;
        }

        .platforms {
            background-color: #f0f4f8;
            padding: 60px 20px;
        }

        .platforms-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .platform-card {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-align: center;
            transition: all 0.3s;
        }

        .platform-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }

        .platform-logo {
            font-size: 40px;
            margin-bottom: 15px;
        }

        .platform-card h3 {
            color: #1e3c72;
            margin-bottom: 10px;
        }

        .platform-card p {
            color: #666;
            margin-bottom: 20px;
            font-size: 14px;
        }

        .platform-link {
            display: inline-block;
            background-color: #ff6b35;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
        }

        .platform-link:hover {
            background-color: #e55a2b;
        }

        .products-section {
            background: white;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
        }

        .product-card {
            background: white;
            border: 1px solid #e0e0e0;
            border-radius: 10px;
            overflow: hidden;
            transition: all 0.3s;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
        }

        .product-image {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            height: 200px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 80px;
            color: white;
        }

        .product-info {
            padding: 20px;
        }

        .product-info h3 {
            color: #1e3c72;
            margin-bottom: 10px;
            font-size: 18px;
        }

        .product-info p {
            color: #666;
            font-size: 14px;
            margin-bottom: 15px;
        }

        .price {
            font-size: 24px;
            color: #ff6b35;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .guarantee {
            background-color: #e8f5e9;
            color: #2e7d32;
            padding: 8px 12px;
            border-radius: 5px;
            font-size: 13px;
            margin-bottom: 15px;
            display: inline-block;
        }

        .contact-section {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 60px 20px;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: start;
        }

        .contact-info {
            display: grid;
            gap: 30px;
        }

        .contact-card {
            background: rgba(255,255,255,0.1);
            padding: 25px;
            border-radius: 10px;
            backdrop-filter: blur(10px);
        }

        .contact-card .icon {
            font-size: 40px;
            margin-bottom: 15px;
        }

        .contact-card h3 {
            margin-bottom: 10px;
            font-size: 18px;
        }

        .contact-card p {
            opacity: 0.95;
            line-height: 1.8;
        }

        .contact-card a {
            color: #ff6b35;
            text-decoration: none;
            font-weight: bold;
        }

        .contact-card a:hover {
            text-decoration: underline;
        }

        .contact-form {
            background: rgba(255,255,255,0.1);
            padding: 30px;
            border-radius: 10px;
            backdrop-filter: blur(10px);
        }

        .contact-form h3 {
            margin-bottom: 25px;
            font-size: 22px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 5px;
            font-family: inherit;
            font-size: 14px;
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .form-group button {
            background-color: #ff6b35;
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
            transition: background-color 0.3s;
            width: 100%;
        }

        .form-group button:hover {
            background-color: #e55a2b;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin: 60px 0;
        }

        .stat-card {
            text-align: center;
            padding: 30px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .stat-number {
            font-size: 40px;
            color: #ff6b35;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .stat-label {
            color: #666;
            font-size: 16px;
        }

        footer {
            background-color: #1e3c72;
            color: white;
            text-align: center;
            padding: 30px 20px;
            margin-top: 60px;
        }

        footer p {
            margin-bottom: 10px;
        }

        footer a {
            color: #ff6b35;
            text-decoration: none;
        }

        footer a:hover {
            text-decoration: underline;
        }

        .hidden {
            display: none;
        }

        @media (max-width: 768px) {
            .nav-wrapper {
                flex-direction: column;
                gap: 15px;
            }

            nav {
                gap: 15px;
                font-size: 14px;
            }

            .language-selector {
                border-left: none;
                padding-left: 0;
            }

            .hero h1 {
                font-size: 32px;
            }

            .hero p {
                font-size: 16px;
            }

            .contact-content {
                grid-template-columns: 1fr;
            }

            .hero-buttons {
                flex-direction: column;
            }

            .btn {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-container">
            <div class="logo">
                📺 Mudisch Elektronik
            </div>
            <div class="nav-wrapper">
                <nav>
                    <a href="#home" data-tr="home" data-en="home" data-de="home">Startseite</a>
                    <a href="#services" data-tr="services" data-en="services" data-de="services">Dienstleistungen</a>
                    <a href="#products" data-tr="products" data-en="products" data-de="products">Produkte</a>
                    <a href="#platforms" data-tr="platforms" data-en="platforms" data-de="platforms">Plattformen</a>
                    <a href="#contact" class="cta-button" data-tr="contact" data-en="contact" data-de="contact">Kontakt</a>
                </nav>
                <div class="language-selector">
                    <button class="lang-btn active" onclick="changeLang('tr')" title="Türkçe">🇹🇷</button>
                    <button class="lang-btn" onclick="changeLang('en')" title="English">🇬🇧</button>
                    <button class="lang-btn" onclick="changeLang('de')" title="Deutsch">🇩🇪</button>
                </div>
            </div>
        </div>
    </header>

    <!-- TURKISH VERSION -->
    <div id="content-tr">
        <section class="hero" id="home">
            <div class="container">
                <h1>Mudisch Elektronik'e Hoş Geldiniz</h1>
                <p>Mönchengladbach'ta Profesyonel TV Satışı ve Tamir Hizmeti</p>
                <div class="hero-buttons">
                    <a href="#products" class="btn btn-primary">Ürünleri Görüntüle</a>
                    <a href="#contact" class="btn btn-secondary">Bize Ulaşın</a>
                </div>
            </div>
        </section>

        <section id="services">
            <div class="container">
                <h2 class="section-title">Hizmetlerimiz</h2>
                <div class="services-grid">
                    <div class="service-card">
                        <div class="service-icon">📺</div>
                        <h3>TV Satışı</h3>
                        <p>Önde gelen markalardan yüksek kaliteli televizyonlar. Yeni ve kullanılmış modeller 1 yıl garantili ve faturalı.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">🔧</div>
                        <h3>Profesyonel Tamir</h3>
                        <p>Tüm TV markalarının hızlı ve güvenilir tamiri. Teşhis, yedek parçalar ve profesyonel bakım.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">✅</div>
                        <h3>Garanti & Hizmet</h3>
                        <p>Tüm ürünlerde 1 yıl garantisi. Hızlı yanıt süreleri ve profesyonel müşteri hizmeti.</p>
                    </div>
                </div>

                <div class="stats">
                    <div class="stat-card">
                        <div class="stat-number">17+</div>
                        <div class="stat-label">Satılan Cihaz</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">87,5%</div>
                        <div class="stat-label">Olumlu Değerlendirme</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">1s</div>
                        <div class="stat-label">Yanıt Süresi</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">5★</div>
                        <div class="stat-label">En İyi Memnuniyet</div>
                    </div>
                </div>
            </div>
        </section>

        <section id="products" class="products-section">
            <div class="container">
                <h2 class="section-title">Mevcut Ürünler</h2>
                <div class="products-grid">
                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>Hisense 65" QLED 4K</h3>
                            <p>65E7NQ PRO QLED 4K Smart TV 144Hz Dolby Vision</p>
                            <div class="price">549€</div>
                            <div class="guarantee">✓ 1 Yıl Garantisi + Fatura</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Sorgula</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>TCL 65" Gaming Pro</h3>
                            <p>65QM8B 144Hz Mini-LED 4K QLED Display</p>
                            <div class="price">849€</div>
                            <div class="guarantee">✓ 1 Yıl Garantisi + Fatura</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Sorgula</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>Metz 55" OLED Smart TV</h3>
                            <p>55TY91 OLED Smart TV - Çok İyi Durum</p>
                            <div class="price">799€</div>
                            <div class="guarantee">✓ 1 Yıl Garantisi + Fatura</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Sorgula</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>LG 55" Smart TV</h3>
                            <p>Tam Fonksiyonel, WiFi, Uygulamalar, Full HD, HDMI</p>
                            <div class="price">169€</div>
                            <div class="guarantee">✓ 1 Yıl Garantisi + Fatura</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Sorgula</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>Nokia 50" Android TV</h3>
                            <p>Android Smart Televizyon - Mükemmel Çalışıyor</p>
                            <div class="price">69€</div>
                            <div class="guarantee">✓ 1 Yıl Garantisi + Fatura</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Sorgula</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>Medion 40" LCD TV</h3>
                            <p>MD 31212, 2017 Yılı - Tam Fonksiyonel</p>
                            <div class="price">49€</div>
                            <div class="guarantee">✓ 1 Yıl Garantisi + Fatura</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Sorgula</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="platforms" id="platforms">
            <div class="container">
                <h2 class="section-title">Bizi Favori Platformlarında Bulun</h2>
                <div class="platforms-grid">
                    <div class="platform-card">
                        <div class="platform-logo">🛒</div>
                        <h3>Kleinanzeigen</h3>
                        <p>Almanya'nın en büyük pazarında mevcut tekliflerimizi keşfedin</p>
                        <a href="https://www.kleinanzeigen.de/s-bestandsliste.html?userId=151673361" target="_blank" class="platform-link">Ziyaret Et</a>
                    </div>

                    <div class="platform-card">
                        <div class="platform-logo">🏪</div>
                        <h3>eBay</h3>
                        <p>eBay'de yüksek kaliteli ürünler ve tamir hizmeti mevcuttur</p>
                        <a href="https://www.ebay.de/usr/mu-519626" target="_blank" class="platform-link">Ziyaret Et</a>
                    </div>

                    <div class="platform-card">
                        <div class="platform-logo">📞</div>
                        <h3>Doğrudan İletişim</h3>
                        <p>Kişisel danışmanlık ve hızlı çözümler için bize doğrudan ulaşın</p>
                        <a href="#contact" class="platform-link">İletişim</a>
                    </div>
                </div>
            </div>
        </section>

        <section class="contact-section" id="contact">
            <div class="container">
                <h2 class="section-title" style="color: white;">Bize Ulaşın</h2>
                <div class="contact-content">
                    <div class="contact-info">
                        <div class="contact-card">
                            <div class="icon">📍</div>
                            <h3>Adres</h3>
                            <p>Laurentiusplatz 3<br>41199 Mönchengladbach<br>Almanya</p>
                        </div>

                        <div class="contact-card">
                            <div class="icon">📞</div>
                            <h3>Telefon</h3>
                            <p><a href="tel:015783987978">0157 839 87 978</a></p>
                            <p style="margin-top: 10px; font-size: 14px;">Yanıt süresi: 1 saat içinde</p>
                        </div>

                        <div class="contact-card">
                            <div class="icon">✉️</div>
                            <h3>E-Posta</h3>
                            <p><a href="mailto:mudischmarketing@gmail.com">mudischmarketing@gmail.com</a></p>
                        </div>

                        <div class="contact-card">
                            <div class="icon">⏰</div>
                            <h3>Çalışma Saatleri</h3>
                            <p>Pazartesi - Cumartesi: 09:00 - 19:00<br>Pazar: Kapalı</p>
                        </div>
                    </div>

                    <div class="contact-form">
                        <h3>Bize Mesaj Gönderin</h3>
                        <form onsubmit="handleSubmit(event)">
                            <div class="form-group">
                                <label for="name">Ad</label>
                                <input type="text" id="name" name="name" required>
                            </div>

                            <div class="form-group">
                                <label for="phone">Telefon</label>
                                <input type="tel" id="phone" name="phone" required>
                            </div>

                            <div class="form-group">
                                <label for="email">E-Posta</label>
                                <input type="email" id="email" name="email" required>
                            </div>

                            <div class="form-group">
                                <label for="subject">Konu</label>
                                <select id="subject" name="subject" required>
                                    <option value="">Seçiniz...</option>
                                    <option value="repair">Tamir Talebi</option>
                                    <option value="purchase">Satın Alma Sorgusu</option>
                                    <option value="parts">Yedek Parçalar</option>
                                    <option value="other">Diğer</option>
                                </select>
                            </div>

                            <div class="form-group">
                                <label for="message">Mesaj</label>
                                <textarea id="message" name="message" required></textarea>
                            </div>

                            <div class="form-group">
                                <button type="submit">Mesaj Gönder</button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </section>

        <footer>
            <p>&copy; 2026 Mudisch Elektronik. Tüm hakları saklıdır.</p>
            <p>Adres: Laurentiusplatz 3, 41199 Mönchengladbach, Almanya</p>
            <p>Telefon: <a href="tel:015783987978">0157 839 87 978</a> | E-Posta: <a href="mailto:mudischmarketing@gmail.com">mudischmarketing@gmail.com</a></p>
            <p style="margin-top: 20px; font-size: 14px;">Bizi <a href="https://www.kleinanzeigen.de/s-bestandsliste.html?userId=151673361" target="_blank">Kleinanzeigen</a> ve <a href="https://www.ebay.de/usr/mu-519626" target="_blank">eBay</a>'de de bulun</p>
        </footer>
    </div>

    <!-- ENGLISH VERSION -->
    <div id="content-en" class="hidden">
        <section class="hero" id="home">
            <div class="container">
                <h1>Welcome to Mudisch Electronics</h1>
                <p>Professional TV Sales and Repair Service in Mönchengladbach</p>
                <div class="hero-buttons">
                    <a href="#products" class="btn btn-primary">View Products</a>
                    <a href="#contact" class="btn btn-secondary">Contact Us</a>
                </div>
            </div>
        </section>

        <section id="services">
            <div class="container">
                <h2 class="section-title">Our Services</h2>
                <div class="services-grid">
                    <div class="service-card">
                        <div class="service-icon">📺</div>
                        <h3>TV Sales</h3>
                        <p>High-quality televisions from leading brands. New and used models with 1-year warranty and invoice.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">🔧</div>
                        <h3>Professional Repair</h3>
                        <p>Fast and reliable repair of all TV brands. Diagnosis, spare parts, and professional maintenance.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">✅</div>
                        <h3>Warranty & Service</h3>
                        <p>1-year warranty on all products. Quick response times and professional customer service.</p>
                    </div>
                </div>

                <div class="stats">
                    <div class="stat-card">
                        <div class="stat-number">17+</div>
                        <div class="stat-label">Devices Sold</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">87.5%</div>
                        <div class="stat-label">Positive Ratings</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">1h</div>
                        <div class="stat-label">Response Time</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">5★</div>
                        <div class="stat-label">Top Satisfaction</div>
                    </div>
                </div>
            </div>
        </section>

        <section id="products" class="products-section">
            <div class="container">
                <h2 class="section-title">Current Products</h2>
                <div class="products-grid">
                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>Hisense 65" QLED 4K</h3>
                            <p>65E7NQ PRO QLED 4K Smart TV 144Hz Dolby Vision</p>
                            <div class="price">€549</div>
                            <div class="guarantee">✓ 1 Year Warranty + Invoice</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Inquire</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>TCL 65" Gaming Pro</h3>
                            <p>65QM8B 144Hz Mini-LED 4K QLED Display</p>
                            <div class="price">€849</div>
                            <div class="guarantee">✓ 1 Year Warranty + Invoice</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Inquire</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>Metz 55" OLED Smart TV</h3>
                            <p>55TY91 OLED Smart TV - Excellent Condition</p>
                            <div class="price">€799</div>
                            <div class="guarantee">✓ 1 Year Warranty + Invoice</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Inquire</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>LG 55" Smart TV</h3>
                            <p>Fully Functional, WiFi, Apps, Full HD, HDMI</p>
                            <div class="price">€169</div>
                            <div class="guarantee">✓ 1 Year Warranty + Invoice</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Inquire</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>Nokia 50" Android TV</h3>
                            <p>Android Smart Television - Works Perfectly</p>
                            <div class="price">€69</div>
                            <div class="guarantee">✓ 1 Year Warranty + Invoice</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Inquire</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>Medion 40" LCD TV</h3>
                            <p>MD 31212, Year 2017 - Fully Functional</p>
                            <div class="price">€49</div>
                            <div class="guarantee">✓ 1 Year Warranty + Invoice</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Inquire</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="platforms" id="platforms">
            <div class="container">
                <h2 class="section-title">Find Us on Your Favorite Platforms</h2>
                <div class="platforms-grid">
                    <div class="platform-card">
                        <div class="platform-logo">🛒</div>
                        <h3>Kleinanzeigen</h3>
                        <p>Discover our current offers on Germany's largest marketplace</p>
                        <a href="https://www.kleinanzeigen.de/s-bestandsliste.html?userId=151673361" target="_blank" class="platform-link">Visit</a>
                    </div>

                    <div class="platform-card">
                        <div class="platform-logo">🏪</div>
                        <h3>eBay</h3>
                        <p>High-quality products and repair service available on eBay</p>
                        <a href="https://www.ebay.de/usr/mu-519626" target="_blank" class="platform-link">Visit</a>
                    </div>

                    <div class="platform-card">
                        <div class="platform-logo">📞</div>
                        <h3>Direct Contact</h3>
                        <p>Contact us directly for personal advice and quick solutions</p>
                        <a href="#contact" class="platform-link">Contact</a>
                    </div>
                </div>
            </div>
        </section>

        <section class="contact-section" id="contact">
            <div class="container">
                <h2 class="section-title" style="color: white;">Contact Us</h2>
                <div class="contact-content">
                    <div class="contact-info">
                        <div class="contact-card">
                            <div class="icon">📍</div>
                            <h3>Address</h3>
                            <p>Laurentiusplatz 3<br>41199 Mönchengladbach<br>Germany</p>
                        </div>

                        <div class="contact-card">
                            <div class="icon">📞</div>
                            <h3>Phone</h3>
                            <p><a href="tel:015783987978">0157 839 87 978</a></p>
                            <p style="margin-top: 10px; font-size: 14px;">Response time: Within 1 hour</p>
                        </div>

                        <div class="contact-card">
                            <div class="icon">✉️</div>
                            <h3>Email</h3>
                            <p><a href="mailto:mudischmarketing@gmail.com">mudischmarketing@gmail.com</a></p>
                        </div>

                        <div class="contact-card">
                            <div class="icon">⏰</div>
                            <h3>Opening Hours</h3>
                            <p>Monday - Saturday: 09:00 - 19:00<br>Sunday: Closed</p>
                        </div>
                    </div>

                    <div class="contact-form">
                        <h3>Send us a Message</h3>
                        <form onsubmit="handleSubmit(event)">
                            <div class="form-group">
                                <label for="name">Name</label>
                                <input type="text" id="name" name="name" required>
                            </div>

                            <div class="form-group">
                                <label for="phone">Phone</label>
                                <input type="tel" id="phone" name="phone" required>
                            </div>

                            <div class="form-group">
                                <label for="email">Email</label>
                                <input type="email" id="email" name="email" required>
                            </div>

                            <div class="form-group">
                                <label for="subject">Subject</label>
                                <select id="subject" name="subject" required>
                                    <option value="">Select...</option>
                                    <option value="repair">Repair Request</option>
                                    <option value="purchase">Purchase Inquiry</option>
                                    <option value="parts">Spare Parts</option>
                                    <option value="other">Other</option>
                                </select>
                            </div>

                            <div class="form-group">
                                <label for="message">Message</label>
                                <textarea id="message" name="message" required></textarea>
                            </div>

                            <div class="form-group">
                                <button type="submit">Send Message</button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </section>

        <footer>
            <p>&copy; 2026 Mudisch Electronics. All rights reserved.</p>
            <p>Address: Laurentiusplatz 3, 41199 Mönchengladbach, Germany</p>
            <p>Phone: <a href="tel:015783987978">0157 839 87 978</a> | Email: <a href="mailto:mudischmarketing@gmail.com">mudischmarketing@gmail.com</a></p>
            <p style="margin-top: 20px; font-size: 14px;">Find us also on <a href="https://www.kleinanzeigen.de/s-bestandsliste.html?userId=151673361" target="_blank">Kleinanzeigen</a> and <a href="https://www.ebay.de/usr/mu-519626" target="_blank">eBay</a></p>
        </footer>
    </div>

    <!-- GERMAN VERSION -->
    <div id="content-de" class="hidden">
        <section class="hero" id="home">
            <div class="container">
                <h1>Willkommen bei Mudisch Elektronik</h1>
                <p>Professionelle TV-Verkäufe und Reparaturservice in Mönchengladbach</p>
                <div class="hero-buttons">
                    <a href="#products" class="btn btn-primary">Produkte Ansehen</a>
                    <a href="#contact" class="btn btn-secondary">Kontaktieren</a>
                </div>
            </div>
        </section>

        <section id="services">
            <div class="container">
                <h2 class="section-title">Unsere Dienstleistungen</h2>
                <div class="services-grid">
                    <div class="service-card">
                        <div class="service-icon">📺</div>
                        <h3>TV-Verkauf</h3>
                        <p>Hochwertige Fernseher von führenden Marken. Neue und gebrauchte Modelle mit 1 Jahr Garantie und Rechnung.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">🔧</div>
                        <h3>Professionelle Reparatur</h3>
                        <p>Schnelle und zuverlässige Reparatur aller TV-Marken. Diagnose, Ersatzteile und fachgerechte Wartung.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">✅</div>
                        <h3>Garantie & Service</h3>
                        <p>1 Jahr Garantie auf alle Produkte. Schnelle Antwortzeiten und professioneller Kundenservice.</p>
                    </div>
                </div>

                <div class="stats">
                    <div class="stat-card">
                        <div class="stat-number">17+</div>
                        <div class="stat-label">Verkaufte Geräte</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">87,5%</div>
                        <div class="stat-label">Positive Bewertungen</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">1h</div>
                        <div class="stat-label">Antwortzeit</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">5★</div>
                        <div class="stat-label">TOP Zufriedenheit</div>
                    </div>
                </div>
            </div>
        </section>

        <section id="products" class="products-section">
            <div class="container">
                <h2 class="section-title">Aktuelle Produkte</h2>
                <div class="products-grid">
                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>Hisense 65" QLED 4K</h3>
                            <p>65E7NQ PRO QLED 4K Smart TV 144Hz Dolby Vision</p>
                            <div class="price">549€</div>
                            <div class="guarantee">✓ 1 Jahr Garantie + Rechnung</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Anfrage</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>TCL 65" Gaming Pro</h3>
                            <p>65QM8B 144Hz Mini-LED 4K QLED Display</p>
                            <div class="price">849€</div>
                            <div class="guarantee">✓ 1 Jahr Garantie + Rechnung</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Anfrage</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>Metz 55" OLED Smart TV</h3>
                            <p>55TY91 OLED Smart TV - Sehr guter Zustand</p>
                            <div class="price">799€</div>
                            <div class="guarantee">✓ 1 Jahr Garantie + Rechnung</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Anfrage</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>LG 55" Smart TV</h3>
                            <p>Voll funktionsfähig, WLAN, Apps, Full HD, HDMI</p>
                            <div class="price">169€</div>
                            <div class="guarantee">✓ 1 Jahr Garantie + Rechnung</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Anfrage</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>Nokia 50" Android TV</h3>
                            <p>Android-Fernseher - Funktioniert einwandfrei</p>
                            <div class="price">69€</div>
                            <div class="guarantee">✓ 1 Jahr Garantie + Rechnung</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Anfrage</a>
                        </div>
                    </div>

                    <div class="product-card">
                        <div class="product-image">📺</div>
                        <div class="product-info">
                            <h3>Medion 40" LCD TV</h3>
                            <p>MD 31212, Baujahr 2017 - Voll funktionsfähig</p>
                            <div class="price">49€</div>
                            <div class="guarantee">✓ 1 Jahr Garantie + Rechnung</div>
                            <a href="#contact" class="btn btn-primary" style="width: 100%; text-align: center;">Anfrage</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="platforms" id="platforms">
            <div class="container">
                <h2 class="section-title">Finde uns auf deinen Lieblings-Plattformen</h2>
                <div class="platforms-grid">
                    <div class="platform-card">
                        <div class="platform-logo">🛒</div>
                        <h3>Kleinanzeigen</h3>
                        <p>Entdecke unsere aktuellen Angebote auf Deutschlands größtem Marktplatz</p>
                        <a href="https://www.kleinanzeigen.de/s-bestandsliste.html?userId=151673361" target="_blank" class="platform-link">Besuchen</a>
                    </div>

                    <div class="platform-card">
                        <div class="platform-logo">🏪</div>
                        <h3>eBay</h3>
                        <p>Hochwertige Produkte und Reparaturservice auf eBay verfügbar</p>
                        <a href="https://www.ebay.de/usr/mu-519626" target="_blank" class="platform-link">Besuchen</a>
                    </div>

                    <div class="platform-card">
                        <div class="platform-logo">📞</div>
                        <h3>Direkt Kontakt</h3>
                        <p>Kontaktiere uns direkt für persönliche Beratung und schnelle Lösungen</p>
                        <a href="#contact" class="platform-link">Kontaktieren</a>
                    </div>
                </div>
            </div>
        </section>

        <section class="contact-section" id="contact">
            <div class="container">
                <h2 class="section-title" style="color: white;">Kontaktiere uns</h2>
                <div class="contact-content">
                    <div class="contact-info">
                        <div class="contact-card">
                            <div class="icon">📍</div>
                            <h3>Adresse</h3>
                            <p>Laurentiusplatz 3<br>41199 Mönchengladbach<br>Deutschland</p>
                        </div>

                        <div class="contact-card">
                            <div class="icon">📞</div>
                            <h3>Telefon</h3>
                            <p><a href="tel:015783987978">0157 839 87 978</a></p>
                            <p style="margin-top: 10px; font-size: 14px;">Antwortzeit: Innerhalb 1 Stunde</p>
                        </div>

                        <div class="contact-card">
                            <div class="icon">✉️</div>
                            <h3>E-Mail</h3>
                            <p><a href="mailto:mudischmarketing@gmail.com">mudischmarketing@gmail.com</a></p>
                        </div>

                        <div class="contact-card">
                            <div class="icon">⏰</div>
                            <h3>Öffnungszeiten</h3>
                            <p>Montag - Samstag: 09:00 - 19:00<br>Sonntag: Geschlossen</p>
                        </div>
                    </div>

                    <div class="contact-form">
                        <h3>Sende uns eine Nachricht</h3>
                        <form onsubmit="handleSubmit(event)">
                            <div class="form-group">
                                <label for="name">Name</label>
                                <input type="text" id="name" name="name" required>
                            </div>

                            <div class="form-group">
                                <label for="phone">Telefon</label>
                                <input type="tel" id="phone" name="phone" required>
                            </div>

                            <div class="form-group">
                                <label for="email">E-Mail</label>
                                <input type="email" id="email" name="email" required>
                            </div>

                            <div class="form-group">
                                <label for="subject">Betreff</label>
                                <select id="subject" name="subject" required>
                                    <option value="">Wählen Sie...</option>
                                    <option value="repair">Reparaturanfrage</option>
                                    <option value="purchase">Kaufanfrage</option>
                                    <option value="parts">Ersatzteile</option>
                                    <option value="other">Sonstiges</option>
                                </select>
                            </div>

                            <div class="form-group">
                                <label for="message">Nachricht</label>
                                <textarea id="message" name="message" required></textarea>
                            </div>

                            <div class="form-group">
                                <button type="submit">Nachricht Senden</button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </section>

        <footer>
            <p>&copy; 2026 Mudisch Elektronik. Alle Rechte vorbehalten.</p>
            <p>Adresse: Laurentiusplatz 3, 41199 Mönchengladbach, Deutschland</p>
            <p>Telefon: <a href="tel:015783987978">0157 839 87 978</a> | E-Mail: <a href="mailto:mudischmarketing@gmail.com">mudischmarketing@gmail.com</a></p>
            <p style="margin-top: 20px; font-size: 14px;">Finde uns auch auf <a href="https://www.kleinanzeigen.de/s-bestandsliste.html?userId=151673361" target="_blank">Kleinanzeigen</a> und <a href="https://www.ebay.de/usr/mu-519626" target="_blank">eBay</a></p>
        </footer>
    </div>

    <script>
        function changeLang(lang) {
            // Hide all content
            document.getElementById('content-tr').classList.add('hidden');
            document.getElementById('content-en').classList.add('hidden');
            document.getElementById('content-de').classList.add('hidden');

            // Show selected language
            document.getElementById('content-' + lang).classList.remove('hidden');

            // Update active button
            document.querySelectorAll('.lang-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            event.target.classList.add('active');

            // Save preference
            localStorage.setItem('selectedLang', lang);
        }

        function handleSubmit(event) {
            event.preventDefault();
            alert('Thank you for your message! We will contact you soon.');
            document.querySelector('.contact-form form').reset();
        }

        // Load saved language preference
        window.addEventListener('load', function() {
            const savedLang = localStorage.getItem('selectedLang') || 'tr';
            changeLang(savedLang);
        });

        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>
