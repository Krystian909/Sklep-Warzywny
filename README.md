
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Stragan Owocowo-Warzywny — świeże owoce i warzywa każdego dnia.">
    <title>Stragan Owocowo-Warzywny</title>

    <style>
        :root {
            --green: #315b36;
            --dark-green: #203f27;
            --cream: #fff9ed;
            --orange: #e99b42;
            --text: #302d25;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: var(--cream);
            color: var(--text);
            line-height: 1.6;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        .top-bar {
            background: var(--dark-green);
            color: white;
            text-align: center;
            padding: 9px 15px;
            font-size: 14px;
        }

        header {
            background: #fffdf7;
            padding: 18px 7%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 20px;
            border-bottom: 1px solid #e9e0cf;
        }

        .logo {
            color: var(--green);
            font-size: 22px;
            font-weight: 800;
            line-height: 1.2;
        }

        .logo span {
            display: block;
            color: #a86a30;
            font-size: 12px;
            letter-spacing: 3px;
            text-transform: uppercase;
            margin-top: 5px;
        }

        nav {
            display: flex;
            gap: 24px;
            flex-wrap: wrap;
        }

        nav a {
            font-size: 14px;
            font-weight: bold;
        }

        nav a:hover {
            color: #a86a30;
        }

        .hero {
            min-height: 480px;
            padding: 75px 7%;
            display: flex;
            align-items: center;
            background:
                linear-gradient(90deg,
                    rgba(25, 43, 25, 0.86),
                    rgba(25, 43, 25, 0.25)),
                url("https://images.unsplash.com/photo-1542838132-92c53300491e?auto=format&fit=crop&w=1800&q=85")
                center/cover;
            color: white;
        }

        .hero-content {
            max-width: 620px;
        }

        .eyebrow {
            color: #f4c779;
            text-transform: uppercase;
            font-weight: bold;
            letter-spacing: 3px;
            font-size: 13px;
            margin-bottom: 14px;
        }

        h1 {
            font-size: clamp(38px, 6vw, 66px);
            line-height: 1.08;
            margin-bottom: 22px;
        }

        .hero p {
            font-size: 18px;
            max-width: 520px;
            margin-bottom: 30px;
        }

        .button {
            display: inline-block;
            padding: 13px 23px;
            border-radius: 5px;
            font-weight: bold;
            transition: 0.2s;
        }

        .button-primary {
            background: var(--orange);
            color: #2d261a;
        }

        .button-primary:hover {
            background: #f6b95f;
            transform: translateY(-2px);
        }

        .button-outline {
            border: 1px solid white;
            margin-left: 10px;
        }

        .button-outline:hover {
            background: white;
            color: var(--dark-green);
        }

        section {
            padding: 75px 7%;
            scroll-margin-top: 20px;
        }

        .section-heading {
            text-align: center;
            max-width: 650px;
            margin: 0 auto 38px;
        }

        .section-heading .eyebrow {
            color: #9c6a31;
            margin-bottom: 8px;
        }

        h2 {
            color: var(--dark-green);
            font-size: clamp(28px, 4vw, 40px);
            line-height: 1.2;
            margin-bottom: 12px;
        }

        .section-heading p {
            color: #6e685d;
        }

        .products {
            display: grid;
            grid-template-columns: repeat(4, minmax(0, 1fr));
            gap: 22px;
        }

        .product {
            background: white;
            border: 1px solid #ece4d6;
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .product:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 24px #43351a12;
        }

        .product img {
            display: block;
            width: 100%;
            height: 190px;
            object-fit: cover;
        }

        .product-info {
            padding: 18px;
        }

        .product-info h3 {
            color: var(--dark-green);
            font-size: 19px;
            margin-bottom: 6px;
        }

        .product-info p {
            color: #777064;
            font-size: 14px;
            min-height: 44px;
        }

        .price {
            display: block;
            color: #9b6128;
            font-size: 20px;
            font-weight: bold;
            margin-top: 13px;
        }

        .about {
            background: #edf0df;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            align-items: center;
            gap: 50px;
            max-width: 1100px;
            margin: auto;
        }

        .about img {
            width: 100%;
            min-height: 300px;
            max-height: 420px;
            object-fit: cover;
            border-radius: 12px;
        }

        .about-text p {
            margin: 15px 0;
            color: #5c5b4c;
        }

        .about-text ul {
            list-style: none;
            margin: 22px 0;
        }

        .about-text li {
            margin: 10px 0;
        }

        .about-text li::before {
            content: "✓ ";
            color: var(--green);
            font-weight: bold;
            margin-right: 7px;
        }

        .banner {
            background: var(--green);
            color: white;
            text-align: center;
            padding: 48px 7%;
        }

        .banner h2 {
            color: white;
        }

        .banner p {
            margin-bottom: 22px;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(0, 1fr));
            gap: 22px;
        }

        .contact-card {
            background: white;
            border: 1px solid #ece4d6;
            border-radius: 9px;
            padding: 26px 20px;
            text-align: center;
        }

        .contact-card .emoji {
            font-size: 30px;
            margin-bottom: 10px;
        }

        .contact-card h3 {
            color: var(--dark-green);
            margin-bottom: 8px;
        }

        .contact-card p {
            color: #6e685d;
            overflow-wrap: anywhere;
        }

        footer {
            background: #1d3322;
            color: #f9f3e6;
            padding: 27px 7%;
            text-align: center;
            font-size: 14px;
        }

        footer p + p {
            margin-top: 6px;
            color: #d5ddce;
        }

        @media (max-width: 900px) {
            .products {
                grid-template-columns: repeat(2, minmax(0, 1fr));
            }

            header {
                flex-direction: column;
            }

            nav {
                justify-content: center;
                gap: 15px;
            }

            .about-grid {
                gap: 28px;
            }
        }

        @media (max-width: 600px) {
            .hero {
                min-height: 430px;
                padding: 55px 6%;
            }

            .hero p {
                font-size: 16px;
            }

            .button {
                margin: 5px 5px 5px 0;
            }

            section {
                padding: 55px 6%;
            }

            .products,
            .about-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .product img {
                height: 230px;
            }

            .about-grid {
                gap: 25px;
            }

            .about img {
                min-height: 230px;
            }
        }
    </style>
</head>

<body>

    <div class="top-bar">
        🥕 Świeże owoce i warzywa — zapraszamy na zakupy!
    </div>

    <header>
        <a class="logo" href="#glowna">
            Stragan
            <span>Owocowo-Warzywny</span>
        </a>

        <nav aria-label="Menu główne">
            <a href="#glowna">Strona główna</a>
            <a href="#produkty">Nasze produkty</a>
            <a href="#onas">O nas</a>
            <a href="#kontakt">Kontakt</a>
        </nav>
    </header>

    <main>
        <section class="hero" id="glowna">
            <div class="hero-content">
                <div class="eyebrow">Smak natury każdego dnia</div>
                <h1>Prosto z pola na Twój stół!</h1>
                <p>
                    Witamy na naszym straganie! Znajdziesz u nas
                    kolorowe owoce, świeże warzywa i smaki,
                    które przypominają o domowej kuchni.
                </p>
                <a class="button button-primary" href="#produkty">
                    Zobacz nasze produkty
                </a>
                <a class="button button-outline" href="#kontakt">
                    Odwiedź nas
                </a>
            </div>
        </section>

        <section id="produkty">
            <div class="section-heading">
                <div class="eyebrow">Prosto z targu</div>
                <h2>Co dziś znajdziesz na straganie?</h2>
                <p>
                    Wybierz ulubione smaki i skomponuj koszyk
                    pełen świeżych produktów.
                </p>
            </div>

            <div class="products">
                <article class="product">
                    <img
                        src="https://images.unsplash.com/photo-1546094096-0df4bcaaa337?auto=format&fit=crop&w=700&q=80"
                        alt="Dojrzałe czerwone pomidory"
                        loading="lazy">
                    <div class="product-info">
                        <h3>Pomidory</h3>
                        <p>Idealne do kanapek, sałatek i sosów.</p>
                        <span class="price">6,99 zł / kg</span>
                    </div>
                </article>

                <article class="product">
                    <img
                        src="https://images.unsplash.com/photo-1445282768818-728615cc910a?auto=format&fit=crop&w=700&q=80"
                        alt="Świeże marchewki"
                        loading="lazy">
                    <div class="product-info">
                        <h3>Marchew</h3>
                        <p>Świetna do zup, surówek i chrupania.</p>
                        <span class="price">3,99 zł / kg</span>
                    </div>
                </article>

                <article class="product">
                    <img
                        src="https://images.unsplash.com/photo-1604977042946-1eecc30f269e?auto=format&fit=crop&w=700&q=80"
                        alt="Zielone świeże ogórki"
                        loading="lazy">
                    <div class="product-info">
                        <h3>Ogórki</h3>
                        <p>Doskonale pasują do letnich sałatek.</p>
                        <span class="price">5,49 zł / kg</span>
                    </div>
                </article>

                <article class="product">
                    <img
                        src="https://images.unsplash.com/photo-1568702846914-96b305d2aaeb?auto=format&fit=crop&w=700&q=80"
                        alt="Soczyste czerwone jabłka"
                        loading="lazy">
                    <div class="product-info">
                        <h3>Jabłka</h3>
                        <p>Słodka i chrupiąca przekąska na każdy dzień.</p>
                        <span class="price">4,49 zł / kg</span>
                    </div>
                </article>
            </div>
        </section>

        <section class="about" id="onas">
            <div class="about-grid">
                <img
                    src="https://images.unsplash.com/photo-1488459716781-31db52582fe9?auto=format&fit=crop&w=1000&q=85"
                    alt="Kolorowe owoce i warzywa na targowym stoisku"
                    loading="lazy">

                <div class="about-text">
                    <div class="eyebrow">Poznaj nas</div>
                    <h2>Mały stragan, wielki smak!</h2>
                    <p>
                        Wierzymy, że najlepsze posiłki zaczynają się
                        od dobrych składników. Dlatego nasz stragan
                        to miejsce dla wszystkich, którzy lubią
                        świeże produkty i domowe smaki.
                    </p>
                    <p>
                        Chcemy, aby codzienne zakupy były proste,
                        przyjemne i pełne kolorów.
                    </p>

                    <ul>
                        <li>Owoce i warzywa na co dzień</li>
                        <li>Produkty do domowych posiłków</li>
                        <li>Przyjazna atmosfera jak na lokalnym targu</li>
                    </ul>

                    <a class="button button-primary" href="#kontakt">
                        Znajdź nas
                    </a>
                </div>
            </div>
        </section>

        <section class="banner">
            <h2>Kolorowy koszyk zaczyna się tutaj!</h2>
            <p>Wpadnij po świeże składniki na dzisiejszy obiad.</p>
            <a class="button button-primary" href="#kontakt">
                Sprawdź kontakt
            </a>
        </section>

        <section id="kontakt">
            <div class="section-heading">
                <div class="eyebrow">Zapraszamy</div>
                <h2>Odwiedź nasz stragan</h2>
                <p>
                    Codziennie nowe owoce i warzywa.
                </p>
            </div>

            <div class="contact-grid">
                <div class="contact-card">
                    <div class="emoji">📍</div>
                    <h3>Adres</h3>
                    <p>ul. Kwiatowa 12, Gdańsk</p>
                </div>

                <div class="contact-card">
                    <div class="emoji">🕒</div>
                    <h3>Godziny otwarcia</h3>
                    <p>Pon.–Pt.: 8.00 - 18.00<br>
                       Sobota: 8.00 - 14.00</p>
                </div>

                <div class="contact-card">
                    <div class="emoji">📞</div>
                    <h3>Telefon</h3>
                    <p>T=+48 123-456-789</p>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <p><strong>Stragan Owocowo-Warzywny</strong></p>
        <p>Świeżość, smak i tradycja.</p>
        <p>&copy; 2026 Stragan Owocowo-Warzywny</p>
    </footer>

</body>
</html>
