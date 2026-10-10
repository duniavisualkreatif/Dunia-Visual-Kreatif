<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Dunia Visual Kreatif — Creative & Marketing Agency</title>

<meta name="description" content="Dunia Visual Kreatif adalah creative & marketing agency yang membantu brand, music label, dan talent membangun campaign yang relevan, kreatif, dan menghasilkan dampak nyata.">

<style>

/* =========================
   GLOBAL
========================= */

:root {
    --midnight: #000A18;
    --deep-navy: #00152B;
    --blue: #009DFF;
    --cyan: #00C8FF;
    --white: #FFFFFF;
    --text: #D7E7F4;
    --muted: #8195A8;
    --border: rgba(255,255,255,0.10);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background:
        radial-gradient(circle at 50% 15%, rgba(0,157,255,0.15), transparent 30%),
        linear-gradient(
            135deg,
            var(--midnight),
            var(--deep-navy),
            #000914,
            var(--midnight)
        );
    background-size: 180% 180%;
    animation: backgroundMove 18s ease infinite;
    color: var(--white);
    overflow-x: hidden;
}

@keyframes backgroundMove {
    0% {
        background-position: 0% 50%;
    }

    50% {
        background-position: 100% 50%;
    }

    100% {
        background-position: 0% 50%;
    }
}

a {
    color: inherit;
    text-decoration: none;
}

.container {
    width: min(1180px, 90%);
    margin: auto;
}

section {
    position: relative;
    padding: 120px 0;
}

/* =========================
   BACKGROUND EFFECT
========================= */

.energy {
    position: fixed;
    inset: 0;
    pointer-events: none;
    overflow: hidden;
    z-index: -1;
}

.energy-line {
    position: absolute;
    width: 800px;
    height: 2px;
    background: linear-gradient(
        90deg,
        transparent,
        rgba(0,157,255,0.35),
        rgba(0,200,255,0.8),
        transparent
    );
    filter: blur(1px);
    opacity: 0.35;
}

.energy-line:nth-child(1) {
    top: 18%;
    left: -200px;
    transform: rotate(25deg);
    animation: energyOne 13s linear infinite;
}

.energy-line:nth-child(2) {
    top: 55%;
    right: -250px;
    transform: rotate(-22deg);
    animation: energyTwo 17s linear infinite;
}

.energy-line:nth-child(3) {
    bottom: 10%;
    left: 10%;
    transform: rotate(-12deg);
    animation: energyThree 15s linear infinite;
}

@keyframes energyOne {
    from {
        transform: translateX(-300px) rotate(25deg);
    }

    to {
        transform: translateX(1600px) rotate(25deg);
    }
}

@keyframes energyTwo {
    from {
        transform: translateX(300px) rotate(-22deg);
    }

    to {
        transform: translateX(-1600px) rotate(-22deg);
    }
}

@keyframes energyThree {
    from {
        transform: translateX(-400px) rotate(-12deg);
    }

    to {
        transform: translateX(1300px) rotate(-12deg);
    }
}

.glow {
    position: fixed;
    width: 450px;
    height: 450px;
    border-radius: 50%;
    background: radial-gradient(
        circle,
        rgba(0,157,255,0.13),
        transparent 70%
    );
    pointer-events: none;
    z-index: -1;
}

.glow-one {
    top: 5%;
    left: -150px;
}

.glow-two {
    bottom: 0;
    right: -150px;
}

/* =========================
   NAVBAR
========================= */

.navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
    padding: 22px 0;
    background: rgba(0,10,24,0.55);
    backdrop-filter: blur(18px);
    border-bottom: 1px solid rgba(255,255,255,0.06);
}

.nav-container {
    width: min(1200px, 90%);
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-size: 16px;
    font-weight: 700;
    letter-spacing: 2px;
}

.logo span {
    color: var(--cyan);
}

.nav-menu {
    display: flex;
    gap: 28px;
    align-items: center;
}

.nav-menu a {
    font-size: 13px;
    color: #AFC1D0;
    transition: 0.3s;
}

.nav-menu a:hover {
    color: var(--cyan);
}

.nav-button {
    padding: 11px 20px;
    border: 1px solid rgba(0,200,255,0.5);
    border-radius: 30px;
    color: white !important;
    background: rgba(0,157,255,0.08);
    transition: 0.3s;
}

.nav-button:hover {
    background: rgba(0,157,255,0.2);
    box-shadow: 0 0 25px rgba(0,157,255,0.25);
}

/* =========================
   HERO
========================= */

.hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    text-align: center;
    overflow: hidden;
}

.hero-content {
    width: 100%;
    position: relative;
    z-index: 2;
}

.hero-small {
    font-size: 12px;
    letter-spacing: 4px;
    color: var(--cyan);
    margin-bottom: 25px;
    text-transform: uppercase;
}

.hero h1 {
    font-size: clamp(50px, 8vw, 105px);
    line-height: 0.95;
    letter-spacing: -4px;
    max-width: 1000px;
    margin: auto;
}

.hero h1 span {
    background: linear-gradient(
        90deg,
        #FFFFFF,
        #6EDBFF,
        #009DFF
    );
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.hero-description {
    max-width: 700px;
    margin: 35px auto;
    color: var(--text);
    line-height: 1.8;
    font-size: 16px;
}

.hero-buttons {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
}

.btn {
    padding: 15px 28px;
    border-radius: 30px;
    font-size: 13px;
    transition: 0.3s;
}

.btn-primary {
    background: linear-gradient(
        90deg,
        var(--blue),
        var(--cyan)
    );
    color: #00101c;
    font-weight: 700;
}

.btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 35px rgba(0,157,255,0.35);
}

.btn-secondary {
    border: 1px solid rgba(255,255,255,0.18);
    color: white;
}

.btn-secondary:hover {
    border-color: var(--cyan);
    color: var(--cyan);
}

.hero-tags {
    margin-top: 35px;
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 2px;
}

/* =========================
   CENTRAL LIGHT
========================= */

.hero-light {
    position: absolute;
    width: 500px;
    height: 500px;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    background: radial-gradient(
        circle,
        rgba(0,157,255,0.18),
        transparent 68%
    );
    animation: pulse 5s ease-in-out infinite;
    pointer-events: none;
}

@keyframes pulse {
    0%,100% {
        transform: translate(-50%, -50%) scale(0.85);
        opacity: 0.6;
    }

    50% {
        transform: translate(-50%, -50%) scale(1.1);
        opacity: 1;
    }
}

/* =========================
   SECTION TITLE
========================= */

.section-label {
    color: var(--cyan);
    font-size: 11px;
    letter-spacing: 3px;
    margin-bottom: 20px;
}

.section-title {
    font-size: clamp(35px, 5vw, 65px);
    letter-spacing: -2px;
    line-height: 1;
    max-width: 850px;
}

.section-description {
    margin-top: 25px;
    color: var(--text);
    line-height: 1.8;
    max-width: 700px;
}

/* =========================
   BELIEF
========================= */

.belief {
    text-align: center;
}

.belief .section-title {
    margin: auto;
}

.quote {
    font-size: clamp(22px, 3vw, 34px);
    line-height: 1.4;
    max-width: 900px;
    margin: 50px auto 30px;
    color: white;
}

.belief-text {
    max-width: 720px;
    margin: auto;
    color: var(--muted);
    line-height: 1.9;
}

/* =========================
   ABOUT
========================= */

.about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: center;
}

.about-text {
    color: var(--text);
    line-height: 1.9;
}

.strategy-line {
    margin-top: 35px;
    font-size: 13px;
    letter-spacing: 2px;
    color: var(--cyan);
}

/* =========================
   SERVICES
========================= */

.services-grid {
    margin-top: 60px;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
}

.service-card {
    padding: 35px;
    min-height: 300px;
    border: 1px solid var(--border);
    background: rgba(255,255,255,0.025);
    backdrop-filter: blur(15px);
    transition: 0.4s;
}

.service-card:hover {
    transform: translateY(-8px);
    border-color: rgba(0,200,255,0.35);
    box-shadow: 0 20px 60px rgba(0,0,0,0.25);
}

.service-number {
    color: var(--cyan);
    font-size: 12px;
    letter-spacing: 2px;
}

.service-card h3 {
    margin: 20px 0;
    font-size: 27px;
}

.service-card p {
    color: var(--muted);
    line-height: 1.7;
}

.service-list {
    margin-top: 25px;
    list-style: none;
    color: #AFC1D0;
    font-size: 13px;
    line-height: 2;
}

.service-list li::before {
    content: "→ ";
    color: var(--cyan);
}

/* =========================
   WORK
========================= */

.work-grid {
    margin-top: 60px;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.work-card {
    min-height: 280px;
    padding: 30px;
    border: 1px solid var(--border);
    background:
        linear-gradient(
            145deg,
            rgba(0,157,255,0.10),
            rgba(255,255,255,0.02)
        );
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    transition: 0.4s;
}

.work-card:hover {
    transform: translateY(-8px);
    border-color: var(--cyan);
}

.work-number {
    color: var(--cyan);
    font-size: 12px;
    margin-bottom: auto;
}

.work-card h3 {
    font-size: 28px;
}

.work-card p {
    color: var(--muted);
    margin-top: 8px;
}

/* =========================
   NUMBERS
========================= */

.stats {
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
}

.stats-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: var(--border);
}

.stat {
    padding: 45px 25px;
    text-align: center;
    background: var(--midnight);
}

.stat-number {
    font-size: 48px;
    font-weight: 700;
    background: linear-gradient(
        90deg,
        white,
        var(--cyan)
    );
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.stat-label {
    margin-top: 10px;
    color: var(--muted);
    font-size: 12px;
    letter-spacing: 1px;
}

/* =========================
   PARTNERS
========================= */

.partners-header {
    display: flex;
    justify-content: space-between;
    align-items: end;
    gap: 30px;
}

.partner-category {
    margin-top: 70px;
}

.partner-category h3 {
    font-size: 12px;
    color: var(--cyan);
    letter-spacing: 3px;
    margin-bottom: 25px;
}

/* LOGO WALL */

.logo-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 15px;
}

.logo-box {
    height: 120px;
    border: 1px solid rgba(255,255,255,0.08);
    background: rgba(255,255,255,0.025);
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 25px;
    transition: 0.4s;
    position: relative;
    overflow: hidden;
}

.logo-box::before {
    content: "";
    position: absolute;
    width: 100px;
    height: 100px;
    background: radial-gradient(
        circle,
        rgba(0,200,255,0.12),
        transparent 70%
    );
    opacity: 0;
    transition: 0.4s;
}

.logo-box:hover {
    transform: translateY(-5px);
    border-color: rgba(0,200,255,0.35);
    box-shadow: 0 15px 40px rgba(0,157,255,0.12);
}

.logo-box:hover::before {
    opacity: 1;
}

/* ACTUAL LOGOS */

.logo-box img {
    position: relative;
    z-index: 2;
    max-width: 150px;
    max-height: 55px;
    width: auto;
    height: auto;
    object-fit: contain;

    /* membuat logo terlihat clean & premium */
    filter:
        grayscale(100%)
        brightness(0)
        invert(1);

    opacity: 0.65;

    transition:
        transform 0.4s ease,
        opacity 0.4s ease,
        filter 0.4s ease;
}

.logo-box:hover img {
    filter: none;
    opacity: 1;
    transform: scale(1.07);
}

/* =========================
   CONTACT
========================= */

.contact {
    text-align: center;
}

.contact .section-title {
    margin: auto;
}

.contact-description {
    max-width: 650px;
    margin: 30px auto;
    color: var(--muted);
    line-height: 1.8;
}

.contact-info {
    margin-top: 40px;
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
}

.contact-item {
    padding: 15px 22px;
    border: 1px solid var(--border);
    background: rgba(255,255,255,0.025);
    transition: 0.3s;
}

.contact-item:hover {
    border-color: var(--cyan);
    color: var(--cyan);
}

/* =========================
   FOOTER
========================= */

footer {
    border-top: 1px solid var(--border);
    padding: 50px 0;
}

.footer-content {
    display: flex;
    justify-content: space-between;
    gap: 30px;
}

.footer-logo {
    font-weight: 700;
    letter-spacing: 2px;
}

.footer-description {
    margin-top: 10px;
    color: var(--muted);
    font-size: 12px;
}

.footer-right {
    color: var(--muted);
    font-size: 11px;
    text-align: right;
}

/* =========================
   SCROLL REVEAL
========================= */

.reveal {
    opacity: 0;
    transform: translateY(30px);
    transition: 0.8s ease;
}

.reveal.active {
    opacity: 1;
    transform: translateY(0);
}

/* =========================
   MOBILE
========================= */

.mobile-menu {
    display: none;
    font-size: 25px;
    cursor: pointer;
}

@media(max-width: 900px) {

    .nav-menu {
        display: none;
        position: absolute;
        top: 75px;
        left: 5%;
        width: 90%;
        padding: 25px;
        flex-direction: column;
        background: rgba(0,10,24,0.96);
        border: 1px solid var(--border);
    }

    .nav-menu.active {
        display: flex;
    }

    .mobile-menu {
        display: block;
    }

    .about-grid {
        grid-template-columns: 1fr;
        gap: 40px;
    }

    .services-grid {
        grid-template-columns: 1fr;
    }

    .work-grid {
        grid-template-columns: 1fr;
    }

    .stats-grid {
        grid-template-columns: 1fr 1fr;
    }

    .logo-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    .partners-header {
        flex-direction: column;
        align-items: flex-start;
    }

    .footer-content {
        flex-direction: column;
    }

    .footer-right {
        text-align: left;
    }
}

@media(max-width: 500px) {

    section {
        padding: 90px 0;
    }

    .hero h1 {
        letter-spacing: -2px;
    }

    .logo-grid {
        grid-template-columns: 1fr 1fr;
        gap: 10px;
    }

    .logo-box {
        height: 95px;
        padding: 15px;
    }

    .logo-box img {
        max-width: 110px;
        max-height: 40px;
    }

    .stats-grid {
        grid-template-columns: 1fr;
    }
}

</style>
</head>


<body>

<!-- =========================
     BACKGROUND
========================= -->

<div class="energy">
    <div class="energy-line"></div>
    <div class="energy-line"></div>
    <div class="energy-line"></div>
</div>

<div class="glow glow-one"></div>
<div class="glow glow-two"></div>


<!-- =========================
     NAVBAR
========================= -->

<nav class="navbar">

    <div class="nav-container">

        <a href="#home" class="logo">
            DUNIA <span>VISUAL</span> KREATIF
        </a>

        <div class="mobile-menu" onclick="toggleMenu()">
            ☰
        </div>

        <div class="nav-menu" id="navMenu">

            <a href="#home">Beranda</a>

            <a href="#about">Tentang Kami</a>

            <a href="#services">Apa yang Kami Lakukan</a>

            <a href="#work">Pekerjaan Kami</a>

            <a href="#partners">Partner</a>

            <a href="#contact">Contact</a>

            <a href="#contact" class="nav-button">
                Mulai Kolaborasi
            </a>

        </div>

    </div>

</nav>


<!-- =========================
     HERO
========================= -->

<section class="hero" id="home">

    <div class="hero-light"></div>

    <div class="container hero-content reveal">

        <div class="hero-small">
            Creative & Marketing Agency
        </div>

        <h1>
            MENGUBAH IDE
            <br>
            <span>MENJADI GERAKAN.</span>
        </h1>

        <p class="hero-description">

            Dunia Visual Kreatif adalah creative & marketing agency
            yang membantu brand, music label, dan talent membangun
            kampanye yang relevan, kreatif, dan menghasilkan dampak nyata.

        </p>

        <div class="hero-buttons">

            <a href="#work" class="btn btn-primary">
                Lihat Pekerjaan Kami
            </a>

            <a href="#contact" class="btn btn-secondary">
                Mulai Kolaborasi
            </a>

        </div>

        <div class="hero-tags">

            Strategy • Creator • Affiliate • Music Marketing

        </div>

    </div>

</section>


<!-- =========================
     BELIEF
========================= -->

<section class="belief">

    <div class="container reveal">

        <div class="section-label">
            KAMI PERCAYA
        </div>

        <p class="quote">

            “Ide yang baik bukan hanya tentang terlihat menarik.
            Ide yang baik harus mampu bergerak, terhubung,
            dan memberikan hasil.”

        </p>

        <p class="belief-text">

            Di Dunia Visual Kreatif, kami percaya bahwa sebuah campaign
            bukan sekadar tentang membuat konten.

            <br><br>

            Kami menggabungkan strategi, kreativitas, creator,
            komunitas, dan eksekusi untuk menciptakan campaign
            yang memiliki tujuan yang jelas.

            <br><br>

            Karena bagi kami, kreativitas bukan hanya tentang apa yang terlihat.
            Tetapi tentang apa yang terjadi setelahnya.

        </p>

    </div>

</section>


<!-- =========================
     ABOUT
========================= -->

<section id="about">

    <div class="container">

        <div class="about-grid">

            <div class="reveal">

                <div class="section-label">
                    TENTANG KAMI
                </div>

                <h2 class="section-title">
                    Creative thinking.
                    Real execution.
                </h2>

            </div>

            <div class="about-text reveal">

                Dunia Visual Kreatif adalah creative marketing agency
                yang menghubungkan brand, creator, dan audience
                melalui strategi yang relevan dengan budaya digital.

                <br><br>

                Kami bekerja di persimpangan antara marketing,
                creator economy, social commerce, dan music culture.

                <br><br>

                Dengan pengalaman menangani campaign untuk berbagai
                brand, music label, dan talent, kami memahami bagaimana
                sebuah ide dapat diterjemahkan menjadi campaign
                yang dapat dijalankan secara nyata.

                <br><br>

                Mulai dari menyusun strategi, memilih creator yang tepat,
                melakukan negosiasi, mengelola campaign, hingga monitoring
                dan reporting — kami membantu memastikan setiap campaign
                berjalan dari ide hingga eksekusi.

                <div class="strategy-line">

                    STRATEGY → CREATIVE → CREATOR → EXECUTION → RESULT

                </div>

            </div>

        </div>

    </div>

</section>


<!-- =========================
     SERVICES
========================= -->

<section id="services">

    <div class="container">

        <div class="reveal">

            <div class="section-label">
                APA YANG KAMI LAKUKAN
            </div>

            <h2 class="section-title">
                Campaigns built
                to move.
            </h2>

            <p class="section-description">

                Kami membantu bisnis dan talent membangun campaign
                yang relevan, terukur, dan mampu bergerak
                di ekosistem digital.

            </p>

        </div>


        <div class="services-grid">


            <div class="service-card reveal">

                <div class="service-number">01</div>

                <h3>Affiliate Marketing</h3>

                <p>
                    Membangun dan mengelola campaign affiliate
                    untuk membantu brand meningkatkan awareness,
                    content volume, traffic, dan sales.
                </p>

                <ul class="service-list">

                    <li>Affiliate Campaign Strategy</li>
                    <li>Creator Recruitment</li>
                    <li>Creator Activation</li>
                    <li>Product Seeding</li>
                    <li>Campaign Management</li>
                    <li>Performance Monitoring</li>
                    <li>Reporting</li>

                </ul>

            </div>


            <div class="service-card reveal">

                <div class="service-number">02</div>

                <h3>KOL & Creator Marketing</h3>

                <p>
                    Menghubungkan brand dengan creator yang relevan
                    berdasarkan audience, content category,
                    positioning, dan campaign objective.
                </p>

                <ul class="service-list">

                    <li>Creator Research</li>
                    <li>Creator Selection</li>
                    <li>KOL Campaign</li>
                    <li>Negotiation</li>
                    <li>Briefing</li>
                    <li>Content Monitoring</li>
                    <li>Campaign Reporting</li>

                </ul>

            </div>


            <div class="service-card reveal">

                <div class="service-number">03</div>

                <h3>Music Marketing</h3>

                <p>
                    Membantu music label dan artist memperkenalkan
                    musik kepada audience melalui creator
                    dan social media.
                </p>

                <ul class="service-list">

                    <li>Music Campaign Strategy</li>
                    <li>TikTok Creator Campaign</li>
                    <li>Music Discovery Campaign</li>
                    <li>Artist / Release Promotion</li>
                    <li>Fanpage Management</li>
                    <li>Creator Activation</li>
                    <li>Campaign Monitoring</li>

                </ul>

            </div>


            <div class="service-card reveal">

                <div class="service-number">04</div>

                <h3>Marketing Strategy</h3>

                <p>
                    Mengubah business objective menjadi strategi
                    marketing yang dapat dijalankan.
                </p>

                <ul class="service-list">

                    <li>Campaign Strategy</li>
                    <li>Audience & Market Analysis</li>
                    <li>Creator Strategy</li>
                    <li>Content Strategy</li>
                    <li>Campaign Planning</li>
                    <li>Budget Planning</li>
                    <li>Performance Analysis</li>

                </ul>

            </div>


            <div class="service-card reveal">

                <div class="service-number">05</div>

                <h3>Campaign Management</h3>

                <p>
                    Dari awal hingga akhir, kami membantu mengelola
                    campaign agar tetap berjalan sesuai timeline,
                    brief, budget, dan objective.
                </p>

                <ul class="service-list">

                    <li>Strategy</li>
                    <li>Creator</li>
                    <li>Execution</li>
                    <li>Monitoring</li>
                    <li>Reporting</li>

                </ul>

            </div>

        </div>

    </div>

</section>


<!-- =========================
     WORK
========================= -->

<section id="work">

    <div class="container">

        <div class="reveal">

            <div class="section-label">
                PEKERJAAN KAMI
            </div>

            <h2 class="section-title">
                Strategi yang kami buat.
                Campaign yang kami jalankan.
            </h2>

            <p class="section-description">

                Kami bekerja bersama brand, music label, dan talent
                untuk membangun campaign melalui creator,
                social commerce, dan digital marketing.

            </p>

        </div>


        <div class="work-grid">


            <div class="work-card reveal">

                <div class="work-number">
                    01
                </div>

                <h3>
                    BRAND CAMPAIGNS
                </h3>

                <p>
                    Creator & Affiliate Marketing
                </p>

            </div>


            <div class="work-card reveal">

                <div class="work-number">
                    02
                </div>

                <h3>
                    MUSIC CAMPAIGNS
                </h3>

                <p>
                    Music Discovery & Artist Promotion
                </p>

            </div>


            <div class="work-card reveal">

                <div class="work-number">
                    03
                </div>

                <h3>
                    CREATOR CAMPAIGNS
                </h3>

                <p>
                    KOL & Creator Activation
                </p>

            </div>


        </div>

    </div>

</section>


<!-- =========================
     STATS
========================= -->

<section class="stats">

    <div class="container">

        <div class="stats-grid">

            <div class="stat reveal">

                <div class="stat-number">
                    300K+
                </div>

                <div class="stat-label">
                    CREATOR NETWORK
                </div>

            </div>


            <div class="stat reveal">

                <div class="stat-number">
                    100+
                </div>

                <div class="stat-label">
                    BRANDS HANDLED
                </div>

            </div>


            <div class="stat reveal">

                <div class="stat-number">
                    4
                </div>

                <div class="stat-label">
                    INTERNATIONAL MUSIC LABELS
                </div>

            </div>


            <div class="stat reveal">

                <div class="stat-number">
                    25B+
                </div>

                <div class="stat-label">
                    GMV GENERATED
                </div>

            </div>


            <div class="stat reveal">

                <div class="stat-number">
                    1,500+
                </div>

                <div class="stat-label">
                    CREATORS ACTIVATED
                </div>

            </div>


            <div class="stat reveal">

                <div class="stat-number">
                    20+
                </div>

                <div class="stat-label">
                    MUSIC CAMPAIGNS
                </div>

            </div>

        </div>

    </div>

</section>


<!-- =========================
     PARTNERS
========================= -->

<section id="partners">

    <div class="container">

        <div class="partners-header reveal">

            <div>

                <div class="section-label">
                    PARTNERS
                </div>

                <h2 class="section-title">
                    BRANDS, LABELS
                    & TALENTS.
                </h2>

            </div>

            <p class="section-description">

                Kami pernah bekerja bersama berbagai brand,
                music label, dan artist dalam menjalankan
                campaign di Indonesia.

            </p>

        </div>


        <!-- =====================
             BRAND LOGOS
        ====================== -->

        <div class="partner-category reveal">

            <h3>
                BRANDS
            </h3>

            <div class="logo-grid">


                <div class="logo-box">

                    <img
                        src="images/maybelline.png"
                        alt="Maybelline"
                    >

                </div>


                <div class="logo-box">

                    <img
                        src="images/implora.png"
                        alt="Implora"
                    >

                </div>


                <div class="logo-box">

                    <img
                        src="images/dettol.png"
                        alt="Dettol"
                    >

                </div>


                <div class="logo-box">

                    <img
                        src="images/veet.png"
                        alt="Veet"
                    >

                </div>


                <div class="logo-box">

                    <img
                        src="images/somethinc.png"
                        alt="Somethinc"
                    >

                </div>


                <div class="logo-box">

                    <img
                        src="images/purbasari.png"
                        alt="Purbasari"
                    >

                </div>


                <div class="logo-box">

                    <img
                        src="images/madame-gie.png"
                        alt="Madame Gie"
                    >

                </div>


                <div class="logo-box more-brand">

                    <span>
                        +100 BRANDS
                    </span>

                </div>


            </div>

        </div>


        <!-- =====================
             MUSIC LABEL LOGOS
        ====================== -->

        <div class="partner-category reveal">

            <h3>
                MUSIC LABELS
            </h3>

            <div class="logo-grid">


                <div class="logo-box">

                    <img
                        src="images/universal-music-group.png"
                        alt="Universal Music Group"
                    >

                </div>


                <div class="logo-box">

                    <img
                        src="images/atlantic-records.png"
                        alt="Atlantic Records"
                    >

                </div>


                <div class="logo-box">

                    <img
                        src="images/darkroom-records.png"
                        alt="Darkroom Records"
                    >

                </div>


                <div class="logo-box">

                    <img
                        src="images/interscope-records.png"
                        alt="Interscope Records"
                    >

                </div>


            </div>

        </div>

    </div>

</section>


<!-- =========================
     CONTACT
========================= -->

<section class="contact" id="contact">

    <div class="container reveal">

        <div class="section-label">
            CONTACT
        </div>

        <h2 class="section-title">

            LET'S CREATE
            SOMETHING
            THAT MOVES.

        </h2>

        <p class="contact-description">

            Punya brand yang ingin dikembangkan?

            <br>

            Campaign yang ingin dijalankan?

            <br>

            Atau musik yang ingin didengar lebih banyak orang?

            <br><br>

            Mari bicarakan bagaimana kita bisa bekerja bersama.

        </p>


        <div class="contact-info">

            <a
                href="mailto:partnership@duniavisualkreatif.com"
                class="contact-item"
            >

                partnership@duniavisualkreatif.com

            </a>


            <a
                href="https://wa.me/6285285942855"
                target="_blank"
                class="contact-item"
            >

                WhatsApp +62 852-8594-2855

            </a>

        </div>

    </div>

</section>


<!-- =========================
     FOOTER
========================= -->

<footer>

    <div class="container footer-content">

        <div>

            <div class="footer-logo">
                DUNIA VISUAL KREATIF
            </div>

            <div class="footer-description">

                Creative & Marketing Agency

                <br><br>

                Affiliate Marketing • Creator Marketing
                • Music Marketing • Marketing Strategy

            </div>

        </div>


        <div class="footer-right">

            © 2026 Dunia Visual Kreatif.
            All Rights Reserved.

        </div>

    </div>

</footer>


<!-- =========================
     JAVASCRIPT
========================= -->

<script>

/* MOBILE MENU */

function toggleMenu() {

    const menu = document.getElementById("navMenu");

    menu.classList.toggle("active");

}


/* CLOSE MOBILE MENU */

document.querySelectorAll(".nav-menu a").forEach(link => {

    link.addEventListener("click", () => {

        document
            .getElementById("navMenu")
            .classList.remove("active");

    });

});


/* SCROLL REVEAL */

const observer = new IntersectionObserver(

    entries => {

        entries.forEach(entry => {

            if (entry.isIntersecting) {

                entry.target.classList.add("active");

            }

        });

    },

    {
        threshold: 0.12
    }

);


document.querySelectorAll(".reveal").forEach(element => {

    observer.observe(element);

});


/* MOUSE PARALLAX */

document.addEventListener("mousemove", e => {

    const x =
        (e.clientX / window.innerWidth - 0.5) * 20;

    const y =
        (e.clientY / window.innerHeight - 0.5) * 20;

    const light =
        document.querySelector(".hero-light");

    if (light) {

        light.style.marginLeft = `${x}px`;
        light.style.marginTop = `${y}px`;

    }

});

</script>

</body>
</html>
