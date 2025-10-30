<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>portofolio saya ke 2</title>
  <style>
    /* ========== GLOBAL STYLE ========== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
      scroll-behavior: smooth;
    }

    body {
      background: linear-gradient(135deg, #1e3c72, #2a5298);
      color: white;
      overflow-x: hidden;
    }

    header {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(0, 0, 0, 0.4);
      padding: 15px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      transition: 0.3s;
      z-index: 1000;
    }

    header.scrolled {
      background: rgba(0, 0, 0, 0.8);
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    }

    .logo {
      font-size: 1.5rem;
      font-weight: 700;
      color: #00e0ff;
      letter-spacing: 2px;
    }

    nav a {
      text-decoration: none;
      color: white;
      margin-left: 25px;
      font-weight: 500;
      transition: 0.3s;
    }

    nav a:hover {
      color: #00e0ff;
    }

    section {
      min-height: 100vh;
      padding: 100px 40px;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      text-align: center;
    }

    /* ========== HERO SECTION ========== */
    #hero {
      background: url('https://images.unsplash.com/photo-1506765515384-028b60a970df?auto=format&fit=crop&w=1500&q=80') center/cover no-repeat;
      position: relative;
      color: white;
    }

    #hero::after {
      content: "";
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.5);
      z-index: 0;
    }

    #hero h1, #hero p, #hero button {
      z-index: 1;
      position: relative;
    }

    #hero h1 {
      font-size: 3rem;
      margin-bottom: 20px;
      animation: fadeDown 1.5s ease;
    }

    #hero p {
      font-size: 1.2rem;
      animation: fadeUp 1.5s ease;
    }

    #hero button {
      margin-top: 25px;
      padding: 12px 30px;
      border: none;
      border-radius: 30px;
      background: #00e0ff;
      color: #fff;
      font-size: 1rem;
      cursor: pointer;
      transition: 0.3s;
    }

    #hero button:hover {
      background: #0072ff;
      transform: scale(1.05);
    }

    /* ========== ABOUT SECTION ========== */
    #about {
      background: #142850;
      color: #e0e0e0;
    }

    #about h2 {
      color: #00e0ff;
      margin-bottom: 15px;
      font-size: 2rem;
    }

    #about p {
      max-width: 600px;
      line-height: 1.6;
    }

    /* ========== INTERACTIVE SKILLS ========== */
    #skills {
      background: #0c2461;
    }

    #skills h2 {
      color: #00e0ff;
      margin-bottom: 30px;
      font-size: 2rem;
    }

    .skill {
      width: 80%;
      max-width: 500px;
      text-align: left;
      margin: 10px 0;
    }

    .bar {
      height: 18px;
      background: #ddd;
      border-radius: 20px;
      overflow: hidden;
    }

    .bar span {
      display: block;
      height: 100%;
      width: 0;
      background: #00e0ff;
      transition: width 1.2s ease;
    }

    /* ========== CONTACT SECTION ========== */
    #contact {
      background: #1a1a2e;
    }

    #contact h2 {
      color: #00e0ff;
      margin-bottom: 20px;
    }

    form {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 15px;
      width: 100%;
      max-width: 400px;
    }

    input, textarea {
      width: 100%;
      padding: 10px;
      border-radius: 10px;
      border: none;
      outline: none;
      font-size: 1rem;
    }

    button[type="submit"] {
      background: #00e0ff;
      color: white;
      border: none;
      padding: 10px 25px;
      border-radius: 25px;
      cursor: pointer;
      transition: 0.3s;
    }

    button[type="submit"]:hover {
      background: #0072ff;
    }

    footer {
      background: #000;
      text-align: center;
      padding: 15px;
      font-size: 0.9rem;
    }

    /* ========== ANIMATIONS ========== */
    @keyframes fadeDown {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <header id="header">
    <div class="logo">Bagus Arief Ishakyudin</div>
    <nav>
      <a href="#hero">Home</a>
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section id="hero">
    <h1>Selamat Datang Di Prtofolio Saya</h1>
    <p>Beautiful, Responsive, and Animated</p>
    <button onclick="scrollToAbout()">Explore More</button>
  </section>

  <section id="about">
    <h2>About Me</h2>
    <p>Hai... Saya Bagus, seorang penggemar web kreatif yang gemar membangun situs web yang indah, interaktif, dan modern menggunakan HTML, CSS, dan JavaScript. Halaman ini adalah contoh bagaimana struktur sederhana bisa menjadi hidup dengan sedikit animasi dan gaya</p>
  </section>

  <section id="skills">
    <h2>My Skills</h2>
    <div class="skill">
      <p>HTML</p>
      <div class="bar"><span data-skill="100%"></span></div>
    </div>
    <div class="skill">
      <p>CSS</p>
      <div class="bar"><span data-skill="85%"></span></div>
    </div>
    <div class="skill">
      <p>PYTON</p>
      <div class="bar"><span data-skill="50%"></span></div>
    </div>
  </section>

  <section id="contact">
    <h2>Contact Me</h2>
    <form onsubmit="return sendMessage(event)">
      <input type="text" placeholder="Your Name" required>
      <input type="email" placeholder="Your Email" required>
      <textarea rows="4" placeholder="Your Message..." required></textarea>
      <button type="submit">Send</button>
    </form>
  </section>

  <footer>
    &copy; 2025 My Interactive Page | Made Bagus Arief 
  </footer>

  <script>
    // ===== Header scroll effect =====
    const header = document.getElementById('header');
    window.addEventListener('scroll', () => {
      header.classList.toggle('scrolled', window.scrollY > 50);
    });

    // ===== Smooth scroll button =====
    function scrollToAbout() {
      document.getElementById('about').scrollIntoView({ behavior: 'smooth' });
    }

    // ===== Animate skill bars on scroll =====
    const skillBars = document.querySelectorAll('.bar span');
    window.addEventListener('scroll', () => {
      const trigger = window.innerHeight * 0.8;
      skillBars.forEach(bar => {
        const rect = bar.getBoundingClientRect();
        if (rect.top < trigger) {
          bar.style.width = bar.dataset.skill;
        }
      });
    });

    // ===== Contact form popup =====
    function sendMessage(e) {
      e.preventDefault();
      alert("✅ Message sent successfully!");
      e.target.reset();
      return false;
    }
  </script>
</body>
</html>
