# Jee---Tracker---Frontend
I ve built a homepage (frontend) for Jee Tracker as my grade 12 and I am working on it. I have used HTML , CSS, React  to build my homepage and also vibe coding.
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>JEE Tracker</title>
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
    />
    <style>
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }

      body {
        font-family: "Inter", sans-serif;
        background-color: #0a0a0a;
        color: #f5f5f5;
        line-height: 1.6;
        overflow-x: hidden;
      }

      /* NAVBAR */
      nav {
        width: 100%;
        padding: 20px 60px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        background: rgba(10, 10, 10, 0.95);
        position: fixed;
        top: 0;
        left: 0;
        z-index: 100;
      }

      nav .logo {
        font-size: 22px;
        font-weight: bold;
        color: #9ef01a;
        letter-spacing: 1px;
      }

      nav .nav-links button {
        margin-left: 20px;
        padding: 10px 18px;
        background: transparent;
        border: 1px solid #9ef01a;
        color: #9ef01a;
        border-radius: 6px;
        cursor: pointer;
        transition: all 0.3s ease;
      }

      nav .nav-links button:hover {
        background: #9ef01a;
        color: #0a0a0a;
      }

      /* HERO SECTION */
      .hero {
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: left;
        padding: 140px 60px 100px;
        gap: 50px;
      }

      .hero img {
        width: 100%;
        max-width: 450px;
        border-radius: 12px;
        animation: fadeInLeft 1.5s ease forwards;
        filter: brightness(0.9);
        transition: transform 0.5s ease, filter 0.5s ease, box-shadow 0.5s ease;
      }

      .hero img:hover {
        transform: scale(1.05) rotateY(8deg);
        filter: brightness(1.1) saturate(1.2);
        box-shadow: 0 0 30px rgba(158, 240, 26, 0.4);
      }

      .hero .content {
        max-width: 600px;
        animation: fadeInRight 1.5s ease forwards;
      }

      .hero h1 {
        font-size: 2.8rem;
        font-weight: 700;
        background: linear-gradient(90deg, #9ef01a, #38b000);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        margin-bottom: 20px;
      }

      .hero p {
        font-size: 1.1rem;
        color: #ccc;
        margin-bottom: 30px;
      }

      .quote {
        font-size: 1.4rem;
        font-weight: bold;
        color: #9ef01a;
        margin-top: 20px;
        animation: pulse 3s infinite;
      }

      /* IITan Floating Tag */
      .iit-tag {
        display: block;
        width: fit-content;
        background: #0a0a0a;
        color: #9ef01a;
        border: 2px solid #9ef01a;
        border-radius: 8px;
        padding: 10px 20px;
        font-size: 1.2rem;
        font-weight: bold;
        margin: 20px auto;
        text-align: center;
        animation: floatTag 3s ease-in-out infinite;
      }

      @keyframes floatTag {
        0% {
          transform: translateY(0px);
        }
        50% {
          transform: translateY(-12px);
        }
        100% {
          transform: translateY(0px);
        }
      }

      /* JEE Description Box */
      .jee-desc {
        max-width: 850px;
        margin: 60px auto;
        text-align: center;
        padding: 30px;
        background: rgba(20, 20, 20, 0.85);
        border: 1px solid #9ef01a;
        border-radius: 12px;
        box-shadow: 0 0 25px rgba(158, 240, 26, 0.2);
        transition: transform 0.3s ease, box-shadow 0.3s ease;
      }

      .jee-desc:hover {
        transform: scale(1.02);
        box-shadow: 0 0 40px rgba(158, 240, 26, 0.35);
      }

      .jee-desc h2 {
        font-size: 1.9rem;
        margin-bottom: 15px;
        color: #9ef01a;
      }

      .jee-desc p {
        color: #ccc;
        font-size: 1rem;
        line-height: 1.7;
      }

      /* ABOUT */
      .about {
        max-width: 800px;
        margin: 80px auto;
        text-align: center;
        padding: 20px;
      }

      .about h2 {
        font-size: 2rem;
        margin-bottom: 20px;
        color: #9ef01a;
      }

      .about p {
        color: #bbb;
        font-size: 1rem;
      }

      /* FOOTER */
      footer {
        background: #111;
        padding: 40px 20px;
        text-align: center;
        border-top: 1px solid #222;
      }

      footer .links {
        margin-bottom: 20px;
      }

      footer .links a {
        color: #777;
        margin: 0 15px;
        text-decoration: none;
        font-size: 0.95rem;
        transition: color 0.3s ease;
      }

      footer .links a:hover {
        color: #9ef01a;
      }

      footer .social a {
        margin: 0 10px;
        color: #777;
        font-size: 1.2rem;
        transition: color 0.3s ease;
      }

      footer .social a:hover {
        color: #9ef01a;
      }

      footer p {
        margin-top: 20px;
        font-size: 0.8rem;
        color: #555;
      }

      /* ANIMATIONS */
      @keyframes fadeInLeft {
        from {
          opacity: 0;
          transform: translateX(-40px);
        }
        to {
          opacity: 1;
          transform: translateX(0);
        }
      }

      @keyframes fadeInRight {
        from {
          opacity: 0;
          transform: translateX(40px);
        }
        to {
          opacity: 1;
          transform: translateX(0);
        }
      }

      @keyframes pulse {
        0%,
        100% {
          opacity: 1;
        }
        50% {
          opacity: 0.6;
        }
      }

      /* RESPONSIVE */
      @media (max-width: 900px) {
        .hero {
          flex-direction: column;
          text-align: center;
        }
        .hero img {
          max-width: 300px;
        }
        .hero h1 {
          font-size: 2rem;
        }
        .quote {
          font-size: 1.2rem;
        }
      }
    </style>
  </head>
  <body>
    <!-- Navbar -->
    <nav>
      <div class="logo">JEE TRACKER</div>
      <div class="nav-links">
        <button>Sign in</button>
        <button>Get Roadmap</button>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
      <img
        src="https://images.unsplash.com/photo-1523580846011-d3a5bc25702b?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80"
        alt="Student Studying"
      />
      <div class="content">
        <h1>Every AIR 1 starts with a plan. What’s yours?</h1>
        <p>
          The endless chapters, the backlogs, the fear of forgetting before the
          exam — it’s overwhelming. That ends here. Track your syllabus, build
          discipline, and crack JEE with clarity.
        </p>
        <div class="quote">
          “Work until you no longer have to introduce yourself — IIT awaits.”
        </div>
      </div>
    </section>

    <!-- IITan Floating Tag -->
    <div class="iit-tag"># IITan</div>

    <!-- JEE Description -->
    <section class="jee-desc">
      <h2>Why Do We Even Study for JEE?</h2>
      <p>
        JEE is more than just an exam — it’s a journey that pushes you to grow.
        The late-night doubts, the formulas you repeat a hundred times, the
        small wins when a tough question finally clicks — all of this shapes
        you. It’s not only about getting into IITs or NITs, it’s about building
        discipline, patience, and confidence in yourself. JEE makes you realize
        that with focus and persistence, you can conquer challenges far bigger
        than textbooks. That’s why we study — not just for a college, but for
        the version of ourselves we become along the way.
      </p>
    </section>

    <!-- About Section -->
    <section class="about">
      <h2>About</h2>
      <p>
        JEE preparation is not just about hard work — it’s about clarity,
        consistency, and confidence. All misery has come to an end now.This
        platform helps students track their syllabus, manage backlogs, and study
        smarter. With the right plan and mindset, <b>You got this.</b>
      </p>
    </section>

    <!-- Footer -->
    <footer>
      <div class="links">
        <a href="#">About</a>
        <a href="#">Contact</a>
        <a href="#">FAQ</a>
        <a href="#">Privacy Policy</a>
      </div>
      <div class="social">
        <a href="#"><i class="fab fa-linkedin"></i></a>
        <a href="#"><i class="fab fa-github"></i></a>
        <a href="#"><i class="fab fa-instagram"></i></a>
      </div>
      <p>© 2025 JEE Tracker. All rights reserved.</p>
    </footer>
  </body>
</html>

