<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Mission OU</title>
    <style>
        body { background: #0077ff; font-family: sans-serif; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; color: white; }
        .card { background: white; color: #333; padding: 30px; border-radius: 20px; text-align: center; width: 300px; box-shadow: 0 10px 20px rgba(0,0,0,0.3); }
        .btn { padding: 10px 20px; margin: 10px; border: none; border-radius: 10px; cursor: pointer; font-weight: bold; font-size: 1.2rem; }
        .oui { background: #27ae60; color: white; }
        .non { background: #e74c3c; color: white; }
    </style>
</head>
<body>
    <div class="card">
        <h1>🤖 Son "OU"</h1>
        <p>Entends-tu "OU" dans :</p>
        <h2 id="mot" style="font-size: 2.5rem; color: #0077ff;">MOUTON</h2>
        <button class="btn oui" onclick="jouer(true)">OUI</button>
        <button class="btn non" onclick="jouer(false)">NON</button>
        <p id="bravo" style="display:none; color:green; font-weight:bold;">SUPER ! 🎉</p>
    </div>

    <script>
        function jouer(choix) {
            if(choix === true) {
                document.getElementById('bravo').style.display = 'block';
                setTimeout(() => { alert("Bravo Détective ! Mission réussie !"); location.reload(); }, 500);
            } else {
                alert("Réessaie encore !");
            }
        }
    </script>
</body>
</html>
