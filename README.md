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
        <li><a /* ========== STYLE GLOBAL ========== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}

html {
  scroll-behavior: smooth;
}

body {
  background-color: #f8f9fa;
  color: #333;
}

/* ========== EN-TÊTE ========== */
header {
  background: linear-gradient(90deg, #004aad, #0072ff);
  color: white;
  padding: 20px 10%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: sticky;
  top: 0;
  z-index: 100;
  box-shadow: 0 3px 10px rgba(0,0,0,0.2);
}

header h1 {
  font-size: 1.8rem;
  font-weight: 700;
}

nav ul {
  display: flex;
  list-style: none;
  gap: 25px;
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

/* ========== SECTION HERO ========== */
.hero {
  background: linear-gradient(rgba(0,74,173,0.7), rgba(0,74,173,0.7)), 
              url('images/hero-bg.jpg') center/cover no-repeat;
  color: white;
  text-align: center;
  padding: 120px 10%;
}

.hero h2 {
  font-size: 2.8rem;
  margin-bottom: 15px;
  animation: fadeInDown 1s ease-out;
}

.hero p {
  font-size: 1.2rem;
  margin-bottom: 25px;
  animation: fadeInUp 1.2s ease-out;
}

.btn {
  background: #ffd700;
  color: #004aad;
  padding: 12px 25px;
  border-radius: 25px;
  text-decoration: none;
  font-weight: 600;
  transition: 0.3s;
}

.btn:hover {
  background: white;
  transform: scale(1.05);
}

/* ========== SECTIONS GÉNÉRALES ========== */
section {
  padding: 70px 10%;
}

.about, .products, .videos, .contact {
  background: white;
  margin: 40px 0;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  padding: 50px;
  animation: fadeIn 1s ease-in-out;
}

h2.section-title {
  text-align: center;
  margin-bottom: 30px;
  color: #004aad;
  position: relative;
}

h2.section-title::after {
  content: '';
  display: block;
  width: 60px;
  height: 4px;
  background: #ffd700;
  margin: 10px auto 0;
  border-radius: 2px;
}

/* ========== PRODUITS ========== */
.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 25px;
  text-align: center;
}

.product-card {
  background: #f8f8f8;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.product-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.2);
}

.product-card img {
  width: 100%;
  border-radius: 10px;
  margin-bottom: 15px;
}

/* ========== VIDÉOS ========== */
iframe {
  width: 100%;
  height: 350px;
  border-radius: 10px;
  border: none;
}

/* ========== CONTACT ========== */
.contact p {
  font-size: 1.1rem;
  text-align: center;
  margin-bottom: 10px;
}

/* ========== PIED DE PAGE ========== */
footer {
  text-align: center;
  padding: 25px;
  background: #004aad;
  color: white;
  margin-top: 40px;
}

/* ========== ANIMATIONS ========== */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes fadeInDown {
  from { opacity: 0; transform: translateY(-30px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

/* ========== RESPONSIVE DESIGN ========== */
@media (max-width: 768px) {
  header {
    flex-direction: column;
    text-align: center;
  }

  nav ul {
    flex-direction: column;
    gap: 10px;
  }

  .hero h2 {
    font-size: 2rem;
  }

  .hero p {
    font-size: 1rem;
  }
}
