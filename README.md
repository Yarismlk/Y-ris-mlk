# Y-ris-mlk
Chaque son raconte un combat,entre flow et émotion, écoute et ressent l'énergie 🔥 
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Stylée avec Fond</title>
    <style>
        /* Mise en page de base */
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            font-family: Arial, sans-serif;
            overflow-x: hidden;
        }

        /* Fond avec effet parallax léger */
        .background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('https://i.imgur.com/FJwNn6t.jpg');
            background-size: cover;
            background-position: center;
            z-index: -1;
            transform: scale(1);
            transition: transform 0.5s ease;
        }

        /* Conteneur pour le texte */
        .texte-container {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            text-align: center;
            color: white;
        }

        /* Fond semi-transparent pour lisibilité */
        .texte {
            background-color: rgba(0, 0, 0, 0.5);
            padding: 25px 50px;
            border-radius: 15px;
            opacity: 0;
            transform: translateY(20px);
            animation: fadeIn 1.5s forwards;
        }

        /* Animation du texte */
        @keyframes fadeIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Ajustement du texte selon la taille de l’écran */
        h1 {
            font-size: 3em;
            margin: 0 0 10px 0;
        }

        p {
            font-size: 1.5em;
            margin: 0;
        }

    </style>
</head>
<body>
    <!-- Fond -->
    <div class="background" id="background"></div>

    <!-- Texte -->
    <div class="texte-container">
        <div class="texte">
            <h1>Bienvenue sur ma page</h1>
            <p>Ton image en fond avec un effet stylé et texte animé</p>
        </div>
    </div>

    <!-- Script pour effet de zoom léger lors du scroll -->
    <script>
        const bg = document.getElementById('background');
        window.addEventListener('scroll', () => {
            let scrollValue = window.scrollY;
            bg.style.transform = `scale(${1 + scrollValue / 5000})`;
        });
    </script>
</body>
</html>
