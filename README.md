# hari_seldi

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hari Joki Mobile Legends</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&family=Poppins:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            background-color: #f4f4f4;
            color: #333;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        .navbar {
            background-image: url('G.jpg');
            background-size: cover;
            padding: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo img {
            max-height: 100px;
            vertical-align: middle;
        }

        .nav-links {
            display: flex;
            gap: 20px;
        }

        .navbar a {
            color: #f4f4f4;
            text-decoration: none;
            padding: 0.5rem 1rem;
            font-family: 'Poppins', sans-serif;
            font-weight: 700;
            cursor: pointer;
            position: relative;
        }

        .navbar a:hover {
            color: #001f3f;
        }

        .navbar a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            display: block;
            margin-top: 5px;
            right: 0;
            background: #FFDC00;
            transition: width 0.3s ease, background-color 0.3s ease;
        }

        .navbar a:hover::after {
            width: 100%;
            left: 0;
            background: #FFDC00;
        }

        .content {
            display: none;
            padding: 3rem;
            margin: 1rem 0;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            font-family: 'Poppins', sans-serif;
            flex: 1;
            opacity: 0;
            transition: opacity 0.5s ease, transform 0.5s ease;
            transform: translateY(10px);
        }

        .content.active {
            display: block;
            opacity: 1;
            transform: translateY(0);
        }

        .content h1, .content h2 {
            color: #001f3f;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 1rem;
        }

        .content h1 {
            font-size: 2.5rem;
        }

        .content h2 {
            font-size: 2rem;
        }

        .content p {
            font-size: 1rem;
            line-height: 1.6;
            margin-bottom: 1.5rem;
        }

        .content img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            margin-bottom: 1.5rem;
        }

       

        .services .service h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .services .service p {
            font-size: 1rem;
            line-height: 1.5;
        }

        .footer {
            background-color: #001f3f;
            color: #FFDC00;
            text-align: center;
            padding: 1rem 0;
            margin-top: auto;
        }

        .highlight {
            color: #000;
            padding: 1rem 0rem;
            border-radius: 5px;
        }

        .button {
            display: inline-block;
            background-color: #FFDC00;
            color: #001f3f;
            padding: 0.7rem 1.2rem;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            margin-top: 1rem;
        }

        .button:hover {
            background-color: #001f3f;
            color: #FFDC00;
            border: 2px solid #FFDC00;
        }

        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                align-items: flex-start;
            }

            .logo {
                margin-bottom: 1rem;
            }

            .nav-links {
                flex-direction: column;
                gap: 10px;
                align-items: flex-start;
                width: 100%;
            }

            .navbar a {
                padding: 0.5rem;
            }

            .content {
                padding: 1rem;
            }

            .content h1 {
                font-size: 2rem;
            }

            .content p {
                font-size: 0.9rem;
            }

            .services .service h3 {
                font-size: 1.2rem;
            }

            .services .service p {
                font-size: 0.9rem;
            }

            .button {
                padding: 0.5rem 1rem;
            }
        }

        @media (max-width: 480px) {
            .navbar {
                padding: 0.5rem;
            }

            .content h1 {
                font-size: 1.8rem;
            }

            .content p {
                font-size: 0.8rem;
            }

            .services .service h3 {
                font-size: 1rem;
            }

            .services .service p {
                font-size: 0.8rem;
            }

            .button {
                padding: 0.4rem 0.8rem;
            }
        }
    </style>
</head>
<body>
    <nav class="navbar">
        <div class="logo">
            <img src="logo.png" alt="Hari Joki Logo">
        </div>
        <div class="nav-links">
            <a onclick="showContent('home')">Beranda</a>
            <a onclick="showContent('services')">Paket Joki</a>
            <a onclick="showContent('contact')">Kontak</a>
        </div>
    </nav>

    <section class="content" id="home">
        <h1>Hari Joki Mobile Legends</h1>
        <img src="1.jpg" alt="Beranda Image">
        <p>Selamat datang di jasa joki Mobile Legends. Dapatkan layanan joki terbaik dengan harga terjangkau!</p>
        <a href="#" class="button" onclick="showContent('services')">Lihat Paket Joki</a>
    </section>

    <section class="content" id="services">
        <h2>Paket Joki</h2>
        <img src="2.jpg" alt="Paket Joki Image">
        <div class="service">
            <h3>Paket Legend</h3>
            <p>Naikkan rank Anda ke Legend dengan cepat dan aman.</p>
        </div>
        <div class="service">
            <h3>Paket Mythic</h3>
            <p>Jadilah yang terbaik dengan layanan joki ke rank Mythic.</p>
        </div>
        <div class="service">
            <h3>Paket Star</h3>
            <p>Nikmati layanan joki sepanjang season dengan harga spesial.</p>
        </div>
    </section>

    <section class="content" id="contact">
        <h2>Kontak</h2>
        <img src="3.jpg" alt="Kontak Image">
        <p>Hubungi kami melalui email di <a href="mailto:hariseldi666@gmail.com"><i class="fas fa-envelope"></i> hariseldi@gmail.com</a> atau melalui telepon/WhatsApp di <a href="tel:+6281211117017"><i class="fas fa-phone-alt"></i> +62 812 111 17017</a>. Kami siap membantu Anda kapan saja.</p>
    </section>

    <footer class="footer">
        <p>&copy; 2024 Hari Joki Mobile Legends. All Rights Reserved.</p>
    </footer>

    <script>
        function showContent(id) {
            var contents = document.querySelectorAll('.content');
            contents.forEach(function(content) {
                content.classList.remove('active');
            });

            var activeContent = document.getElementById(id);
            activeContent.classList.add('active');
        }

        showContent('home');
    </script>
</body>
</html>
