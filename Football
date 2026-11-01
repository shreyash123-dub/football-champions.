<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#101820">

<title>Football Champions 2026</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: #101820;
    color: white;
    text-align: center;
}

header {
    background: linear-gradient(135deg, #064e32, #087c46);
    padding: 25px 10px;
    border-bottom: 3px solid #40ff85;
}

header h1 {
    margin: 0;
    font-size: 27px;
}

header p {
    margin-bottom: 0;
    color: #c9ffdc;
}

.container {
    max-width: 600px;
    margin: auto;
    padding: 15px;
}

.card {
    background: #202e39;
    padding: 20px;
    margin: 15px 0;
    border-radius: 15px;
    box-shadow: 0 4px 15px #0005;
}

h2, h3 {
    margin-top: 5px;
}

select, button {
    width: 100%;
    padding: 13px;
    margin: 7px 0;
    border: none;
    border-radius: 8px;
    font-size: 16px;
}

select {
    background: white;
    color: black;
}

button {
    background: #19d76b;
    color: #071b10;
    font-weight: bold;
    cursor: pointer;
}

button:active {
    transform: scale(0.98);
}

button.secondary {
    background: #34495e;
    color: white;
}

.pitch {
    background: repeating-linear-gradient(
        0deg,
        #168447,
        #168447 45px,
        #11763d 45px,
        #11763d 90px
    );

    border: 3px solid white;
    border-radius: 12px;
    padding: 18px 10px;
    position: relative;
}

.pitch::before {
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    left: 50%;
    border-left: 2px solid #ffffff90;
}

.pitch-label {
    position: relative;
    z-index: 1;
}

.ball {
    font-size: 48px;
    margin: 15px;
    animation: bounce 1s infinite alternate;
}

@keyframes bounce {
    from {
        transform: translateY(0);
    }
    to {
        transform: translateY(-6px);
    }
}

.score {
    font-size: 29px;
    font-weight: bold;
    margin: 15px 0;
    overflow-wrap: anywhere;
}

.team-name {
    font-size: 13px;
    color: #d7e5ee;
}

.small {
    color: #c8d4dc;
    font-size: 13px;
}

.stats {
    display: flex;
    justify-content: space-around;
    gap: 10px;
    flex-wrap: wrap;
}

.stat {
    background: #101820;
    border-radius: 10px;
    padding: 12px;
    flex: 1;
    min-width: 80px;
}

.stat strong {
    display: block;
    font-size: 23px;
    color: #40ff85;
    margin-bottom: 5px;
}

#message {
    min-height: 55px;
    line-height: 1.5;
    color: #69ff9f;
    font-weight: bold;
    padding: 8px;
}

.hidden {
    display: none !important;
}

footer {
    padding: 20px;
    color: #aab8c2;
    font-size: 12px;
}

button:disabled {
    opacity: 0.5;
    cursor: not-allowed;
}
</style>
</head>

<body>

<header>
    <h1>⚽ FOOTBALL CHAMPIONS</h1>
    <p>2026 • Build Your Legacy</p>
</header>

<div class="container">

    <!-- MAIN MENU -->

    <div class="card" id="setup">

        <h2>🏆 Choose Your Club</h2>

        <select id="club">
            <option>Real Madrid</option>
            <option>FC Barcelona</option>
            <option>Manchester United</option>
            <option>Paris Saint-Germain</option>
            <option>Bengaluru FC</option>
        </select>

        <h3>⭐ Choose Your Star Player</h3>

        <select id="player">
            <option value="85">Lionel Messi — 85</option>
            <option value="90">Cristiano Ronaldo — 90</option>
            <option value="82">Neymar Jr. — 82</option>
            <option value="88">Kylian Mbappe — 88</option>
            <option value="92">Erling Haaland — 92</option>
            <option value="80">Sunil Chhetri — 80</option>
        </select>

        <h3>🆚 Choose Your Opponent</h3>

        <select id="opponent">
            <option>Arsenal</option>
            <option>Bayern Munich</option>
            <option>Liverpool</option>
            <option>Inter Milan</option>
            <option>Atletico Madrid</option>
        </select>

        <button onclick="startGame()">⚽ START MATCH</button>

        <p class="small">
            Play matches, score goals, and earn rewards!
        </p>

    </div>

    <!-- MATCH SCREEN -->

    <div class="card hidden" id="match">

        <h2>🏟️ MATCH DAY</h2>

        <p id="matchTitle"></p>

        <div class="pitch">

            <div class="pitch-label">FOOTBALL ARENA</div>

            <div class="ball">⚽</div>

            <div class="pitch-label" id="minute">
                Minute 1
            </div>

        </div>

        <div class="score">

            <div class="team-name" id="yourTeam"></div>

            <span id="yourScore">0</span>
            -
            <span id="enemyScore">0</span>

            <div class="team-name" id="enemyTeam"></div>

        </div>

        <div class="stats">

            <div class="stat">
                <strong id="roundStat">0/6</strong>
                <span>Rounds</span>
            </div>

            <div class="stat">
                <strong id="goalStat">0</strong>
                <span>Your Goals</span>
            </div>

        </div>

        <p id="message">
            The referee blows the whistle!
        </p>

        <h3>Choose Your Move</h3>

        <button onclick="play('shoot')">
            🥅 SHOOT
        </button>

        <button onclick="play('dribble')">
            🔥 DRIBBLE
        </button>

        <button onclick="play('pass')">
            🤝 PASS
        </button>

        <p class="small">
            Six attacking rounds per match.
        </p>

    </div>

    <!-- RESULT SCREEN -->

    <div class="card hidden" id="result">

        <h2 id="resultTitle">FULL TIME</h2>

        <div class="score" id="finalScore"></div>

        <p id="reward"></p>

        <div class="stats">

            <div class="stat">
                <strong id="totalWins">0</strong>
                <span>Wins</span>
            </div>

            <div class="stat">
                <strong id="totalLosses">0</strong>
                <span>Losses</span>
            </div>

            <div class="stat">
                <strong id="totalCoins">0</strong>
                <span>Coins</span>
            </div>

        </div>

        <button onclick="startGame()">
            🔄 PLAY AGAIN
        </button>

        <button class="secondary" onclick="showMenu()">
            🏠 MAIN MENU
        </button>

    </div>

</div>

<footer>
    FOOTBALL CHAMPIONS 2026<br>
    An independent fan-made football game.
</footer>

<script>

// ============================
// GAME DATA
// ============================

let club = "";
let player = "";
let opponent = "";

let shooting = 0;

let yourGoals = 0;
let enemyGoals = 0;

let round = 0;
let coins = 0;

let wins = 0;
let losses = 0;
let draws = 0;

let finished = false;


// ============================
// START GAME
// ============================

function startGame() {

    club = document.getElementById("club").value;

    opponent = document.getElementById("opponent").value;

    let selector = document.getElementById("player");

    player = selector.options[selector.selectedIndex].text;

    shooting = Number(selector.value);

    yourGoals = 0;
    enemyGoals = 0;
    round = 0;
    finished = false;

    document.getElementById("setup").classList.add("hidden");

    document.getElementById("result").classList.add("hidden");

    document.getElementById("match").classList.remove("hidden");

    document.getElementById("matchTitle").textContent =
        club + " VS " + opponent;

    document.getElementById("yourTeam").textContent = club;

    document.getElementById("enemyTeam").textContent = opponent;

    document.getElementById("message").textContent =
        "Kick-off! " + player + " is ready to play!";

    updateScore();

}


// ============================
// UPDATE SCOREBOARD
// ============================

function updateScore() {

    document.getElementById("yourScore").textContent = yourGoals;

    document.getElementById("enemyScore").textContent = enemyGoals;

    document.getElementById("minute").textContent =
        "Minute " + (round * 15 + 1);

    document.getElementById("roundStat").textContent =
        round + "/6";

    document.getElementById("goalStat").textContent =
        yourGoals;

}


// ============================
// PLAY MATCH
// ============================

function play(move) {

    if (finished || round >= 6) {
        return;
    }

    let message = "";

    // SHOOTING

    if (move === "shoot") {

        let chance = Math.random() * 100;

        if (chance < shooting) {

            yourGoals++;

            message = "⚽ GOOOOAL! " + player + " SCORES!";

        } else {

            message = "🧤 The goalkeeper saves your shot!";

        }

    }

    // DRIBBLING

    else if (move === "dribble") {

        if (Math.random() < 0.70) {

            message = "🔥 You beat the defender! ";

            if (Math.random() * 100 < shooting) {

                yourGoals++;

                message += "GOOOOAL! WHAT A FINISH!";

            } else {

                message += "Your final shot misses!";

            }

        } else {

            message = "😱 The defender takes the ball!";

        }

    }

    // PASSING

    else if (move === "pass") {

        if (Math.random() < 0.80) {

            message = "🤝 Brilliant teamwork! ";

            if (Math.random() < 0.60) {

                yourGoals++;

                message += "YOUR TEAMMATE SCORES!";

            } else {

                message += "The goalkeeper saves the shot!";

            }

        } else {

            message = "The opponent intercepts your pass!";

        }

    }

    // COMPUTER ATTACK

    if (Math.random() < 0.30) {

        enemyGoals++;

        message += " | ⚽ " + opponent + " SCORES!";

    } else {

        message += " | 🧤 Your defence holds!";

    }

    round++;

    updateScore();

    document.getElementById("message").textContent = message;

    if (round === 6) {

        finishGame();

    }

}


// ============================
// FINISH MATCH
// ============================

function finishGame() {

    finished = true;

    document.getElementById("match").classList.add("hidden");

    document.getElementById("result").classList.remove("hidden");

    document.getElementById("finalScore").textContent =
        club + " " + yourGoals +
        " - " + enemyGoals + " " + opponent;

    if (yourGoals > enemyGoals) {

        coins += 500;

        wins++;

        document.getElementById("resultTitle").textContent =
            "🏆 VICTORY!";

        document.getElementById("reward").textContent =
            "Champions! You earned 500 coins!";

    }

    else if (yourGoals < enemyGoals) {

        coins += 100;

        losses++;

        document.getElementById("resultTitle").textContent =
            "😢 DEFEAT!";

        document.getElementById("reward").textContent =
            "Keep training! You earned 100 coins.";

    }

    else {

        coins += 250;

        draws++;

        document.getElementById("resultTitle").textContent =
            "🤝 DRAW!";

        document.getElementById("reward").textContent =
            "A hard-fought match! You earned 250 coins.";

    }

    updateCareer();

}


// ============================
// CAREER STATISTICS
// ============================

function updateCareer() {

    document.getElementById("totalWins").textContent = wins;

    document.getElementById("totalLosses").textContent = losses;

    document.getElementById("totalCoins").textContent = coins;

}


// ============================
// RETURN TO MENU
// ============================

function showMenu() {

    document.getElementById("result").classList.add("hidden");

    document.getElementById("match").classList.add("hidden");

    document.getElementById("setup").classList.remove("hidden");

}

</script>

</body>
</html>
