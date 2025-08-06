<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Official Website of Advocate Swarup Das">
    <title>Advocate Swarup Das</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <style>
        /* Base Colors & Variables */
        :root {
            --primary-dark: #003366;
            --primary-light: #f0f4f8;
            --accent-color-gold: #ffc107;
            --accent-color-blue: #007bff;
            --text-color: #343a40;
            --section-bg-light: #f8f9fa;
            --section-bg-mid: #e6f0ff;
            --section-bg-white: #ffffff;
        }

        /* General Styles for Mobile-First Approach */
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            line-height: 1.6;
            background-color: var(--primary-light);
            color: var(--text-color);
        }

        header {
            background-color: var(--primary-dark);
            color: #fff;
            padding: 20px 10px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        header img {
            max-width: 80px;
            display: block;
            margin: 0 auto 10px;
            border-radius: 50%;
            border: 3px solid var(--accent-color-gold);
        }

        header h1 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8em;
            margin: 0;
            color: var(--accent-color-gold);
        }
        
        header p {
            margin: 3px 0;
            font-size: 0.9em;
        }

        nav {
            text-align: center;
            background-color: var(--accent-color-blue);
            padding: 10px 0;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        nav a {
            margin: 0 10px;
            text-decoration: none;
            color: #fff;
            font-weight: bold;
            font-size: 1em;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: var(--accent-color-gold);
        }

        section {
            padding: 20px 15px;
            max-width: 900px;
            margin: 20px auto;
            background-color: var(--section-bg-white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            border-radius: 10px;
        }

        #about { background-color: var(--section-bg-mid); }
        #practice { background-color: var(--section-bg-light); }
        #contact { background-color: var(--section-bg-mid); }

        h2 {
            font-family: 'Playfair Display', serif;
            color: var(--primary-dark);
            font-size: 1.8em;
            border-bottom: 2px solid var(--accent-color-gold);
            padding-bottom: 8px;
            margin-bottom: 15px;
            text-align: center;
        }

        ul {
            list-style: none;
            padding-left: 0;
            display: grid;
            grid-template-columns: 1fr; /* Single column on mobile */
            gap: 10px;
        }

        ul li {
            background-color: var(--section-bg-white);
            padding: 12px;
            border-radius: 8px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.08);
            position: relative;
            padding-left: 30px;
            border-left: 4px solid var(--accent-color-blue);
        }
        
        ul li:before {
            content: '✓';
            color: var(--primary-dark);
            font-weight: bold;
            position: absolute;
            left: 10px;
            top: 50%;
            transform: translateY(-50%);
        }

        .contact p {
            margin: 8px 0;
            font-size: 1em;
        }

        .contact a {
            color: var(--primary-dark);
            text-decoration: none;
            font-weight: bold;
        }
        
        .contact a:hover {
            text-decoration: underline;
        }

        .disclaimer {
            font-size: 0.8em;
            background-color: #fff3cd;
            color: #664d03;
            padding: 15px;
            margin: 20px auto;
            max-width: 900px;
            border-left: 5px solid var(--accent-color-gold);
            text-align: justify;
            border-radius: 8px;
        }

        #about p {
            text-align: justify;
        }

        footer {
            background-color: var(--primary-dark);
            color: #fff;
            padding: 15px;
            text-align: center;
            font-size: 0.8em;
            margin-top: 20px;
        }

        .bio-card {
            text-align: center;
            padding: 20px;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
        }

        .bio-card img {
            border-radius: 50%;
            width: 150px;
            height: 150px;
            object-fit: cover;
            margin-bottom: 15px;
            border: 4px solid var(--primary-dark);
        }

        .whatsapp-chat {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #25d366;
            color: white;
            border-radius: 50%;
            width: 55px;
            height: 55px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            font-size: 30px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
            transition: transform 0.3s ease;
        }

        .whatsapp-chat:hover {
            transform: scale(1.1);
        }

        /* Desktop-specific styles */
        @media (min-width: 768px) {
            header {
                padding: 40px 10px;
            }
            header h1 {
                font-size: 2.5em;
            }
            header p {
                font-size: 1.1em;
            }
            
            h2 {
                font-size: 2em;
                padding-bottom: 10px;
                margin-bottom: 20px;
            }
            
            section {
                padding: 40px 20px;
                margin: 30px auto;
            }

            ul {
                grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
                gap: 15px;
            }

            .whatsapp-chat {
                width: 65px;
                height: 65px;
                font-size: 35px;
            }
        }
    </style>
</head>
<body>

<header>
    <img src="30bf6f82c3d71b67c631b7e1ce3e6a14.jpg" alt="Advocate Logo">
    <h1>Advocate Swarup Das</h1>
    <p>Practicing Advocate, in Civil, Criminal & Contractual Matters</p>
    <p>Enrolled with Bar Council of West Bengal in the year 2020</p>
    <p>Fluent in Bengali, Hindi, and English | Based in All over West Bengal, India</p>
</header>

<div class="disclaimer">
    <p><strong>Disclaimer:</strong> This website is meant only for providing basic information to clients about the advocate and does not amount to advertisement or solicitation. The user voluntarily accesses this website for informational purposes.</p>
</div>

<nav>
    <a href="#about">About Me</a>
    <a href="#practice">Practice Areas</a>
    <a href="#contact">Contact</a>
</nav>

<section id="about">
    <h2>About Me</h2>
    <div class="bio-card">
        <img src="https://via.placeholder.com/180" alt="Swarup Das">
        <p>I am Swarup Das, an independent legal practitioner enrolled with the Bar Council of West Bengal. Since 2020, I have been actively providing legal services with a focus on civil, criminal, and contractual matters.</p>
        <p>Over the years, I have built a reputation for offering honest, ethical, and timely legal assistance to individuals and organizations. My approach is client-centric and solutions-oriented — ensuring that each case is handled with utmost dedication, professionalism, and integrity.</p>
        <p>I believe that access to justice is a fundamental right, and I strive to make quality legal services available to clients across India, regardless of their location or background.</p>
        <p>Whether you are facing a legal dispute, require strategic legal advice, or need assistance with documentation and compliance — I am here to guide you with clarity and confidence.</p>
    </div>
</section>

<section id="practice">
    <h2>Practice Areas</h2>
    <ul>
        <li>Civil Disputes</li>
        <li>Criminal Defense</li>
        <li>FIR, Bail Matters etc.</li>
        <li>Property & Land Litigation</li>
        <li>Contract Law</li>
        <li>Legal Drafting & Documentation</li>
        <li>Power of Attorney</li>
        <li>Succession Certificate</li>
        <li>Legal Heir Certificate</li>
        <li>Name Change / Correction</li>
        <li>Divorce</li>
        <li>Maintenance</li>
        <li>Probate of Will</li>
        <li>Cheque Bouncing Cases</li>
        <li>Sale Deed and Transfer Deed Registration in India</li>
        <li>All Types of Affidavit</li>
        <li>Legal Consultation (Online & Offline)</li>
    </ul>
</section>

<section id="contact" class="contact">
    <h2>Contact</h2>
    <p><strong>Email:</strong> <a href="mailto:swarupscience@gmail.com">swarupscience@gmail.com</a></p>
    <p><strong>Phone:</strong> +91-8918135367</p>
    <p><strong>WhatsApp:</strong> +91-8918135367</p>
    <p><strong>Address:</strong> Village & Post - Pritinagar, P.S - Ranaghat, District - Nadia, West Bengal, Pin - 741247, India</p>
    <p><strong>Consultation:</strong> Available via Google Meet / Zoom</p>
</section>

<a href="https://wa.me/918918135367" target="_blank" class="whatsapp-chat">💬</a>

<footer>
    <p>&copy; 2025 Advocate Swarup Das</p>
</footer>

</body>
</html>
