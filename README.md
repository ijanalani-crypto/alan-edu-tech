<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ALAN Edu Tech - Site Vitrine</title>
  <link rel="stylesheet" href="style.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Poppins", sans-serif;
    }
    body {
      background-color: #f5f5f5;
      color: #333;
    }
    header {
      background: linear-gradient(90deg, #004aad, #0072ff);
      color: white;
      padding: 20px 10%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 3px 10px rgba(0,0,0,0.2);
    }
    header h1 {
      font-size: 1.6rem;
      letter-spacing: 1px;
    }
    nav ul {
      display: flex;
      list-style: none;
      gap: 20px;
    }
    nav ul li a {
      text-decoration: none;
      color: white;
      font-weight: 500;
      transition: color 0.3s;
    }
    nav ul li a:hover {
      color: #ffd700;
    }

    section {
      padding: 60px 10%;
    }

    .hero {
      background: url('images/hero-bg.jpg') center/cover no-repeat;
      color: white;
      text-align: center;
      padding: 120px 10%;
    }
    .hero h2 {
      font-size: 2.5rem;
      margin-bottom: 15px;
    }
    .hero p {
      font-size: 1.2rem;
      margin-bottom: 25px;
    }
    .btn {
      background: #ffd700;
      color: #004aad;
      padding: 10px 20px;
      border-radius: 25px;
      text-decoration: none;
      font-weight: 600;
      transition: 0.3s;
    }
    .btn:hover {
      background: white;
    }

    .about, .products, .videos, .contact {
      background: white;
      margin: 40px 0;
      border-radius: 10px;
      box-shadow: 0 3px 10px rgba(0,0,0,0.1);
      padding: 40px;
    }

    h2.section-title {
      text-align: center;
      margin-bottom: 25px;
      color: #004aad;
    }

    .products-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
      text-align: center;
    }
    .product-card {
      background: #f8f8f8;
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }
    .product-card img {
      width: 100%;
      border-radius: 10px;
      margin-bottom: 10px;
    }
    iframe {
      width: 100%;
      height: 300px;
      border-radius: 10px;
      border: none;
    }
    footer {
      text-align: center;
      padding: 20px;
      background: #004aad;
      color: white;
      margin-top: 40px;
    }
  </style>
</head>
<body>

  <header>
    <h1>ALAN Edu Tech</h1>
    <nav>
      <ul>
        <li><a href="#accueil">Accueil</a></li>
        <li><a href="#about">À propos</a></li>
        <li><a href="#products">Produits</a></li>
        <li><a href="#videos">Vidéos</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section id="accueil" class="hero">
    <h2>Apprendre. Innover. Partager.</h2>
    <p>ALAN Edu Tech — La technologie au service de l’éducation moderne.</p>
    <a href="#about" class="btn">Découvrir plus</a>
  </section>

  <section id="about" class="about">
    <h2 class="section-title">À propos</h2>
    <p>ALAN Edu Tech est une plateforme éducative et technologique dédiée à la formation, à l’innovation et au partage de ressources pour les enseignants, étudiants et passionnés du numérique.</p>
  </section>

  <section id="products" class="products">
    <h2 class="section-title">Nos Produits</h2>
    <div class="products-grid">
      <div class="product-card">
        <img src="images/course.jpg" alt="Cours en ligne">
        <h3>Cours en ligne</h3>
        <p>Des modules interactifs pour apprendre à votre rythme.</p>
      </div>
      <div class="product-card">
        <img src="images/app.jpg" alt="Application mobile">
        <h3>Application mobile</h3>
        <p>Apprenez et testez vos connaissances depuis votre smartphone.</p>
      </div>
      <div class="product-card">
        <img src="images/tools.jpg" alt="Outils éducatifs">
        <h3>Outils éducatifs</h3>
        <p>Des solutions numériques pour les enseignants et les écoles.</p>
      </div>
    </div>
  </section>

  <section id="videos" class="videos">
    <h2 class="section-title">Vidéos</h2>
    <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" allowfullscreen></iframe>
  </section>

  <section id="contact" class="contact">
    <h2 class="section-title">Contact</h2>
    <p>Email : contact@alanedutech.com</p>
    <p>Téléphone : +228 98 93 67 26 | 92 10 38 99</p>
    <p>Adresse : Lomé, Togo</p>
  </section>

  <footer>
    <p>© 2025 ALAN Edu Tech | Tous droits réservés.</p>
  </footer>

</body>
</html>
