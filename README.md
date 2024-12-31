<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Élection du Meilleur Baddeur 2024</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #0f0f1f, #1c1a33);
            color: #fff;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
        }
        .header {
            text-align: center;
            padding: 50px 20px;
            background: linear-gradient(60deg, #FF6B6B, #6B66FF);
            border-radius: 20px;
            margin-bottom: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            transform: translateY(0);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .header:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.4);
        }
        .header h1 {
            font-size: 2.8em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
        }
        .vote-form {
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
            margin-bottom: 30px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }
        .input-group {
            margin-bottom: 20px;
        }
        .input-group label {
            display: block;
            margin-bottom: 10px;
            font-size: 1.2em;
            color: #fff;
        }
        .input-group input {
            width: 100%;
            padding: 15px;
            border: 2px solid rgba(255, 255, 255, 0.2);
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            font-size: 16px;
            color: #fff;
            transition: all 0.3s ease;
        }
        .input-group input:focus {
            outline: none;
            border-color: #6B66FF;
            background: rgba(255, 255, 255, 0.1);
        }
        .vote-btn {
            background: linear-gradient(45deg, #6B66FF, #4CAF50);
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 12px;
            cursor: pointer;
            font-size: 18px;
            width: 100%;
            transition: all 0.3s ease;
            text-transform: uppercase;
            font-weight: bold;
            letter-spacing: 1px;
        }
        .vote-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(107, 102, 255, 0.4);
        }
        .vote-btn:active {
            transform: translateY(0);
        }
        .ranking-section {
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }
        .ranking-section h2 {
            margin-bottom: 20px;
            text-align: center;
            color: #fff;
        }
        .baddeur-rank {
            display: flex;
            align-items: center;
            padding: 20px;
            margin-bottom: 10px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            transition: all 0.3s ease;
        }
        .baddeur-rank:hover {
            transform: translateX(10px);
            background: rgba(255, 255, 255, 0.1);
        }
        .rank-number {
            font-size: 28px;
            font-weight: bold;
            margin-right: 20px;
            min-width: 50px;
            text-align: center;
        }
        .rank-1 {
            color: #FFD700;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
        }
        .rank-2 {
            color: #C0C0C0;
            text-shadow: 0 0 10px rgba(192, 192, 192, 0.5);
        }
        .rank-3 {
            color: #CD7F32;
            text-shadow: 0 0 10px rgba(205, 127, 50, 0.5);
        }
        .baddeur-info {
            flex-grow: 1;
        }
        .baddeur-info strong {
            font-size: 1.2em;
            display: block;
            margin-bottom: 5px;
        }
        .location {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9em;
            display: flex;
            align-items: center;
            margin-top: 5px;
        }
        .vote-count {
            background: linear-gradient(45deg, #6B66FF, #4CAF50);
            padding: 5px 10px;
            border-radius: 8px;
            font-weight: bold;
            font-size: 0.9em;
            display: inline-block;
            margin-top: 5px;
        }
        .error-message, .success-message {
            padding: 15px;
            border-radius: 12px;
            margin-top: 15px;
            display: none;
            text-align: center;
            animation: slideUp 0.3s ease;
        }
        .error-message {
            background: rgba(255, 0, 0, 0.2);
            border: 1px solid rgba(255, 0, 0, 0.3);
        }
        .success-message {
            background: rgba(0, 255, 0, 0.2);
            border: 1px solid rgba(0, 255, 0, 0.3);
        }
        @keyframes slideUp {
            from {
                transform: translateY(10px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }
        .rank-1 .vote-count {
            animation: pulse 2s infinite;
        }
        @keyframes pulse {
            0% {
                box-shadow: 0 0 0 0 rgba(107, 102, 255, 0.4);
            }
            70% {
                box-shadow: 0 0 0 10px rgba(107, 102, 255, 0);
            }
            100% {
                box-shadow: 0 0 0 0 rgba(107, 102, 255, 0);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🏆 Élection du Meilleur Baddeur 2024 🏆</h1>
            <p>Votez pour votre baddeur préféré !</p>
        </div>
        <div class="vote-form">
            <div class="input-group">
                <label for="identifier">Pseudo ou Numéro du baddeur :</label>
                <input type="text" id="identifier" placeholder="Ex: @badding_babi ou 0709XXXXXX">
            </div>
            <button class="vote-btn" onclick="submitVote()">Voter</button>
            <div id="error-message" class="error-message"></div>
            <div id="success-message" class="success-message"></div>
        </div>
        <div class="ranking-section">
            <h2>🏆 Classement des Baddeurs</h2>
            <div id="rankings"></div>
        </div>
    </div>
    <script>
// Charger les données depuis le localStorage
function loadVotes() {
    const storedBaddeurs = localStorage.getItem('baddeurs');
    if (storedBaddeurs) {
        return JSON.parse(storedBaddeurs);
    }
    return [
        { id: 1, username: "natsuyanis777", phone: "0143257049", votes: 1865 , location: "Marcory 🇨🇮" },
        { id: 2, username: "@badding_babi", phone: "0570911151", votes: 1547, location: "Abidjan 🇨🇮" },
        { id: 3, username: "@bad_boy225", phone: "0789222222", votes: 1238, location: "Cocody 🇨🇮" },
        { id: 4, username: "@la_queen_bad", phone: "0709333333", votes: 982, location: "Yopougon 🇨🇮" },
        { id: 5, username: "@baddeur_supreme", phone: "0789444444", votes: 876, location: "Marcory 🇨🇮" },
        { id: 6, username: "@bad_girl_ivy", phone: "0709555555", votes: 754, location: "Treichville 🇨🇮" },
        { id: 7, username: "@king_bad225", phone: "0789666666", votes: 643, location: "Adjamé 🇨🇮" },
        { id: 8, username: "@badding_princess", phone: "0709777777", votes: 521, location: "Plateau 🇨🇮" },
        { id: 9, username: "@le_bad_original", phone: "0789888888", votes: 432, location: "Koumassi 🇨🇮" }
    ];
}

// Sauvegarder les données dans le localStorage
function saveVotes() {
    localStorage.setItem('baddeurs', JSON.stringify(baddeurs));
}

// Liste des baddeurs initialisée depuis le localStorage
const baddeurs = loadVotes();

function submitVote() {
    const identifier = document.getElementById('identifier').value.trim();
    if (!identifier) {
        showError("Entrez un pseudo ou un numéro valide");
        return;
    }

    // Expression régulière corrigée pour les numéros de téléphone
    const validPhonePattern = /^(?:\+225|0)\d{9}$/;

    const baddeur = baddeurs.find(b =>
        b.username.toLowerCase() === identifier.toLowerCase() ||
        (validPhonePattern.test(identifier) &&
         (b.phone === identifier || b.phone === identifier.replace('+225', '0')))
    );

    if (!baddeur) {
        showError("Baddeur non trouvé. Vérifiez le pseudo ou le numéro");
        return;
    }

    baddeur.votes++;
    saveVotes(); // Sauvegarder les données après chaque vote
    showSuccess(`Vote enregistré pour ${baddeur.username} ! 🎉`);
    updateRankings();
    document.getElementById('identifier').value = '';
}

function showError(message) {
    const errorDiv = document.getElementById('error-message');
    const successDiv = document.getElementById('success-message');
    errorDiv.textContent = message;
    errorDiv.style.display = 'block';
    successDiv.style.display = 'none';
}

function showSuccess(message) {
    const errorDiv = document.getElementById('error-message');
    const successDiv = document.getElementById('success-message');
    successDiv.textContent = message;
    successDiv.style.display = 'block';
    errorDiv.style.display = 'none';
}

function updateRankings() {
    const rankingsDiv = document.getElementById('rankings');
    const sortedBaddeurs = [...baddeurs].sort((a, b) => b.votes - a.votes);

    rankingsDiv.innerHTML = sortedBaddeurs.map((baddeur, index) => `
        <div class="baddeur-rank">
            <span class="rank-number rank-${index + 1}">#${index + 1}</span>
            <div class="baddeur-info">
                <strong>${baddeur.username}</strong>
                <div class="location">${baddeur.location}</div>
                <span class="vote-count">${baddeur.votes.toLocaleString()} votes</span>
            </div>
        </div>
    `).join('');

    const rankElements = document.querySelectorAll('.baddeur-rank');
    rankElements.forEach((element, index) => {
        if (index === 0) {
            element.classList.add('rank-1');
        } else if (index === 1) {
            element.classList.add('rank-2');
        } else if (index === 2) {
            element.classList.add('rank-3');
        } else {
            element.classList.remove('rank-1', 'rank-2', 'rank-3');
        }
    });
}

// Initialisation de l'affichage
updateRankings();

    </script>
</body>
</html>
