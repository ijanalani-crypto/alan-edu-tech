# alan-edu-tech
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alan Edu Tech - Accueil</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <img src="images/logo.png" alt="Logo Alan Edu" class="logo">
        <nav>
            <ul>
                <li><a href="index.html" class="active">Accueil</a></li>
                <li><a href="about.html">À propos</a></li>
                <li><a href="products.html">Cours</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section class="hero">
        <h1>Bienvenue sur Alan Edu Tech</h1>
        <p>Apprenez, explorez et développez vos compétences en ligne.</p>
        <a href="products.html" class="btn">Découvrir les cours</a>
        <img src="images/hero.jpg" alt="Apprentissage en ligne" class="hero-img">
    </section>

    <section class="video-section">
        <h2>Présentation de notre plateforme</h2>
        <video controls>
            <source src="videos/presentation.mp4" type="video/mp4">
            Votre navigateur ne supporte pas la vidéo.
        </video>
    </section>

    <footer>
        <p>&copy; 2025 Alan Edu Tech. Tous droits réservés.</p>
    </footer>

    <script src="js/script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>À propos - Alan Edu Tech</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <img src="images/logo.png" alt="Logo Alan Edu" class="logo">
        <nav>
            <ul>
                <li><a href="index.html">Accueil</a></li>
                <li><a href="about.html" class="active">À propos</a></li>
                <li><a href="products.html">Cours</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section class="about">
        <h1>À propos de nous</h1>
        <p>Alan Edu Tech est une plateforme éducative moderne qui permet d'apprendre à son rythme. Nous proposons des cours interactifs avec vidéos, exercices et ressources téléchargeables.</p>
        <p>Notre mission : rendre l'éducation accessible à tous et développer les compétences du futur.</p>
    </section>

    <footer>
        <p>&copy; 2025 Alan Edu Tech. Tous droits réservés.</p>
    </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cours - Alan Edu Tech</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <img src="images/logo.png" alt="Logo Alan Edu" class="logo">
        <nav>
            <ul>
                <li><a href="index.html">Accueil</a></li>
                <li><a href="about.html">À propos</a></li>
                <li><a href="products.html" class="active">Cours</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section class="products">
        <h1>Nos Cours</h1>
        <div class="course-list">
            <div class="course">
                <img src="images/course1.jpg" alt="Cours 1">
                <h3>Anglais Niveau Débutant</h3>
                <p>Apprenez les bases de l'anglais avec nos leçons interactives et vidéos.</p>
            </div>
            <div class="course">
                <img src="images/course1.jpg" alt="Cours 2">
                <h3>Mathématiques pour tous</h3>
                <p>Renforcez vos compétences en mathématiques avec nos exercices guidés.</p>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2025 Alan Edu Tech. Tous droits réservés.</p>
    </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact - Alan Edu Tech</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <img src="images/logo.png" alt="Logo Alan Edu" class="logo">
        <nav>
            <ul>
                <li><a href="index.html">Accueil</a></li>
                <li><a href="about.html">À propos</a></li>
                <li><a href="products.html">Cours</a></li>
                <li><a href="contact.html" class="active">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section class="contact">
        <h1>Contactez-nous</h1>
        <form action="#" method="post">
            <label>Nom :</label>
            <input type="text" name="name" required>
            <label>Email :</label>
            <input type="email" name="email" required>
            <label>Message :</label>
            <textarea name="message" rows="5" required></textarea>
            <button type="submit">Envoyer</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2025 Alan Edu Tech. Tous droits réservés.</p>
    </footer>
</body>
</html>
