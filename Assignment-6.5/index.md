Here is your complete Assignment 6.5 — Profile Card / Product Card Mini-Project using HTML and CSS. I’ve chosen a Profile Card because it covers all the required features: profile image, name and role, description, skills, contact button, box model properties, rounded borders, positioning, and responsive design.

Save the code as Assignment-6.5.html and open it in your browser. The HTML and CSS are included in one file, so you can run it directly.
Complete HTML and CSS code

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 6.5 - Profile Card</title>

    <style>
        /* Reset and box model */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background: #f0f5fc;
            color: #24344d;
            line-height: 1.6;
            padding: 20px;
        }

        header {
            text-align: center;
            background: #204878;
            color: white;
            padding: 25px 15px;
            border-radius: 12px;
            margin-bottom: 30px;
        }

        header h1 {
            font-size: 28px;
            margin-bottom: 8px;
        }

        /* Responsive card layout */
        .card-container {
            display: flex;
            justify-content: center;
            align-items: stretch;
            flex-wrap: wrap;
            gap: 30px;
            max-width: 1000px;
            margin: 0 auto;
        }

        /* Profile card */
        .profile-card {
            position: relative;
            background: white;
            border: 1px solid #d9e4f2;
            border-radius: 18px;
            padding: 25px;
            width: 100%;
            max-width: 420px;
            box-shadow: 0 5px 20px #1c3d6015;
            text-align: center;
        }

        /* Profile image */
        .profile-image {
            width: 140px;
            height: 140px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid #e0edff;
            margin: 10px auto 15px;
            display: block;
        }

        /* Positioned badge */
        .status-badge {
            position: absolute;
            top: 18px;
            right: 18px;
            z-index: 2;
            background: #159b62;
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: bold;
        }

        .profile-card h2 {
            color: #17365f;
            font-size: 27px;
            margin-bottom: 3px;
        }

        .role {
            color: #1769e0;
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 15px;
        }

        .description {
            color: #52627a;
            margin-bottom: 20px;
        }

        /* Skills */
        .skills-title {
            text-align: left;
            margin-bottom: 10px;
            color: #17365f;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 8px;
            margin-bottom: 25px;
        }

        .skill {
            background: #e6f0ff;
            color: #1558b0;
            padding: 7px 14px;
            border-radius: 20px;
            font-size: 14px;
        }

        /* Contact button */
        .contact-button {
            display: block;
            width: 100%;
            padding: 13px;
            background: #2468e8;
            color: white;
            text-decoration: none;
            border: none;
            border-radius: 9px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s;
        }

        .contact-button:hover {
            background: #174eb7;
        }

        /* Product card */
        .product-card {
            position: relative;
            width: 100%;
            max-width: 420px;
            padding: 25px;
            background: white;
            border: 1px solid #d9e4f2;
            border-radius: 18px;
            box-shadow: 0 5px 20px #1c3d6015;
        }

        .product-image {
            width: 100%;
            height: 220px;
            object-fit: cover;
            border-radius: 12px;
            margin-bottom: 15px;
        }

        .product-badge {
            position: absolute;
            top: 35px;
            right: 35px;
            z-index: 2;
            background: #e63946;
            color: white;
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: bold;
        }

        .product-card h2 {
            color: #17365f;
            margin-bottom: 10px;
        }

        .price {
            color: #159b62;
            font-size: 28px;
            font-weight: bold;
            margin-bottom: 12px;
        }

        .old-price {
            color: #788497;
            font-size: 16px;
            text-decoration: line-through;
            margin-left: 8px;
        }

        .product-description {
            color: #52627a;
            margin-bottom: 20px;
        }

        .buy-button {
            display: block;
            width: 100%;
            padding: 13px;
            border: none;
            border-radius: 9px;
            background: #159b62;
            color: white;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
        }

        .buy-button:hover {
            background: #107849;
        }

        footer {
            text-align: center;
            color: #607087;
            margin-top: 35px;
            padding: 15px;
        }

        /* Mobile responsive design */
        @media (max-width: 480px) {
            body {
                padding: 12px;
            }

            header h1 {
                font-size: 22px;
            }

            .profile-card,
            .product-card {
                padding: 20px;
            }

            .profile-card h2 {
                font-size: 24px;
            }

            .product-image {
                height: 180px;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>Assignment 6.5</h1>
        <p>Profile Card / Product Card Mini-Project</p>
        <p>HTML | CSS | Box Model | Positioning | Responsive Design</p>
    </header>

    <main class="card-container">

        <!-- Profile Card -->
        <article class="profile-card">

            <span class="status-badge">Available</span>

            <img
                class="profile-image"
                src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?auto=format&fit=crop&w=300&h=300&q=80"
                alt="Profile portrait"
            >

            <h2>Amit Kumar</h2>
            <p class="role">Web Developer</p>

            <p class="description">
                I am a passionate web developer who enjoys creating
                modern and responsive websites. I love learning new
                technologies and solving programming problems.
            </p>

            <h3 class="skills-title">My Skills</h3>

            <div class="skills">
                <span class="skill">HTML</span>
                <span class="skill">CSS</span>
                <span class="skill">JavaScript</span>
                <span class="skill">Responsive Design</span>
                <span class="skill">Git</span>
            </div>

            <a class="contact-button"
               href="mailto:student@example.com">
                Contact Me
            </a>

        </article>

        <!-- Product Card -->
        <article class="product-card">

            <span class="product-badge">Best Seller</span>

            <img
                class="product-image"
                src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?auto=format&fit=crop&w=700&h=400&q=80"
                alt="Wireless headphones product"
            >

            <h2>Wireless Headphones</h2>

            <p class="price">
                ₹2,499
                <span class="old-price">₹3,999</span>
            </p>

            <p class="product-description">
                Enjoy high-quality sound, comfortable ear cushions,
                and a stylish design. These headphones are suitable
                for music, online classes, and everyday use.
            </p>

            <button
                class="buy-button"
                type="button"
                onclick="alert('Thank you for your interest in this product!')">
                Buy Now
            </button>

        </article>

    </main>

    <footer>
        <p>Assignment 6.5 - Profile Card / Product Card</p>
        <p>Created using HTML and CSS</p>
        <p>Responsive layout for desktop, tablet, and mobile screens.</p>
    </footer>

</body>
</html>



How this assignment meets the requirements
Requirement	Implementation
Profile image	Circular image using border-radius: 50%
Name and role	Amit Kumar — Web Developer
Short description	Developer introduction
Skills	HTML, CSS, JavaScript, Responsive Design, Git
Contact button	Email link using mailto:
Box model	margin, padding, width, box-sizing
Background and border	Background colors, borders, rounded corners
Positioning	position: relative on cards and position: absolute on badges
Meaningful class names	.profile-card, .profile-image, .skills, .contact-button
Responsive design	Flexbox, flex-wrap, and a mobile media query

How to save and submit
1. Open Notepad or Visual Studio Code.
2. Copy the complete code and save it as Assignment-6.5.html.
3. Open the file in Chrome. Internet access is needed to load the external images.
4. Resize the browser to check the desktop and mobile layouts.
5. Take a screenshot using Win + Shift + S and save it as Assignment-6.5-Screenshot.png.
Submission: Include the HTML file and screenshot. The CSS is currently inside the HTML file, which is sufficient unless your instructor specifically requires a separate .css file.

Note: The Buy Now button is a demonstration only; it does not process an actual purchase.