<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2인용 할리갈리</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #3d5a49;
            color: #fff;
            margin: 0;
            user-select: none;
        }

        .game-container {
            text-align: center;
            background-color: #4a6d5a;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
            width: 800px;
        }

        .game-board {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 20px;
            margin: 20px 0;
        }

        .player-area {
            width: 250px;
            padding: 15px;
            border-radius: 10px;
        }
        
        .red-team {
             background-color: rgba(217, 83, 79, 0.2);
        }
        
        .blue-team {
            background-color: rgba(66, 139, 202, 0.2);
        }

        .deck-container {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 15px;
            height: 150px;
        }

        .deck {
            width: 80px;
            height: 120px;
            border: 3px solid #fff;
            border-radius: 10px;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 40px;
            font-weight: bold;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        .deck.red-deck { background-color: #d9534f; }
        .deck.blue-deck { background-color: #428bca; }


        .deck:hover {
            transform: translateY(-5px);
            transition: transform 0.2s;
        }

        .card-pile {
            width: 80px;
            height: 120px;
            background-color: #f0e6d2;
            border: 3px solid #ccc;
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            font-size: 14px;
            padding: 5px;
            box-sizing: border-box;
        }

        .card {
            width: 100%;
            height: 100%;
            border-radius: 7px;
            background-size: contain;
            background-repeat: no-repeat;
            background-position: center;
            color: black;
            font-weight: bold;
        }

        /* 과일 이미지 URL */
        .card.fruit-strawberry { background-image: url('https://i.imgur.com/dJ2xSPk.png'); }
        .card.fruit-banana { background-image: url('https://i.imgur.com/yDM44nI.png'); }
        .card.fruit-lime { background-image: url('https://i.imgur.com/CXJbVp6.png'); }
        .card.fruit-plum { background-image: url('https://i.imgur.com/WJafE9n.png'); }


        .center-area {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
        }

        .bell {
            background: none;
            border: none;
            cursor: pointer;
            padding: 0;
            transition: transform 0.1s;
        }

        .bell img {
            width: 100px;
            height: 100px;
        }

        .bell:active {
            transform: scale(0.9);
        }

        .message-box {
            min-height: 40px;
            font-size: 1.1em;
            color: #ffdd57;
            font-weight: bold;
        }

        .controls-info {
            display: flex;
            justify-content: space-around;
            width: 100%;
            margin-top: 20px;
            font-size: 0.9em;
        }
        .controls-info div {
             padding: 10px;
             border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="game-container">
        <h1>2인용 할리갈리</h1>
        <div class="game-board">
            <!-- Red 팀 영역 -->
            <div id="red-area" class="player-area red-team">
                <h2>Red 팀</h2>
                <div class="deck-container">
                    <div id="red-deck" class="deck red-deck"></div>
                    <div id="red-discard" class="card-pile"></div>
                </div>
                <p>남은 카드: <span id="red-count">0</span></p>
            </div>

            <!-- 중앙 영역 -->
            <div class="center-area">
                <button id="bell" class="bell">
                    <img src="https://i.imgur.com/y1v6Y3h.png" alt="bell">
                </button>
                <p id="message-box" class="message-box">게임을 시작하려면 종을 누르세요</p>
            </div>

            <!-- Blue 팀 영역 -->
            <div id="blue-area" class="player-area blue-team">
                <h2>Blue 팀</h2>
                <div class="deck-container">
                    <div id="blue-deck" class="deck blue-deck"></div>
                    <div id="blue-discard" class="card-pile"></div>
                </div>
                <p>남은 카드: <span id="blue-count">0</span></p>
            </div>
        </div>
        <div class="controls-info">
             <div class="red-team"><strong>Red 팀:</strong> 카드(A), 종(D)</div>
             <div class="blue-team"><strong>Blue 팀:</strong> 카드(L), 종(M)</div>
        </div>
    </div>

    <script>
    document.addEventListener('DOMContentLoaded', () => {
        const fruits = ['strawberry', 'banana', 'lime', 'plum'];
        const cards = [];

        const deckElements = { red: document.getElementById('red-deck'), blue: document.getElementById('blue-deck') };
        const discardElements = { red: document.getElementById('red-discard'), blue: document.getElementById('blue-discard') };
        const countElements = { red: document.getElementById('red-count'), blue: document.getElementById('blue-count') };
        const areaElements = { red: document.getElementById('red-area'), blue: document.getElementById('blue-area') };
        const bellEl = document.getElementById('bell');
        const messageBoxEl = document.getElementById('message-box');

        let decks = { red: [], blue: [] };
        let discards = { red: [], blue: [] };

        let currentTurn = 'red';
        let gameInProgress = false;
        let canRing = true;

        function createDeck() {
            cards.length = 0;
            // 총 50장 생성 (25장씩 분배)
            const cardCounts = { 1: 5, 2: 3, 3: 3, 4: 2, 5: 2 }; // 과일 개수별 카드 수
            fruits.forEach(fruit => {
                for (let i = 1; i <= 5; i++) {
                    for (let j = 0; j < cardCounts[i]; j++) {
                        cards.push({ fruit, count: i });
                    }
                }
            });
             // 50장으로 맞추기 위해 2장 추가
            cards.push({ fruit: 'strawberry', count: 1 });
            cards.push({ fruit: 'banana', count: 1 });
        }

        function shuffleAndDeal() {
            for (let i = cards.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [cards[i], cards[j]] = [cards[j], cards[i]];
            }
            decks.red = cards.slice(0, 25);
            decks.blue = cards.slice(25, 50);
        }

        function updateUI() {
            for (const team of ['red', 'blue']) {
                countElements[team].textContent = decks[team].length;
                deckElements[team].style.display = decks[team].length > 0 ? 'flex' : 'none';
                
                const discardCard = discards[team].length > 0 ? discards[team][discards[team].length - 1] : null;
                displayCard(discardElements[team], discardCard);
            }
            
            areaElements.red.style.boxShadow = currentTurn === 'red' ? '0 0 15px 5px #ffdd57' : 'none';
            areaElements.blue.style.boxShadow = currentTurn === 'blue' ? '0 0 15px 5px #ffdd57' : 'none';
        }

        function displayCard(pileElement, card) {
            pileElement.innerHTML = '';
            if (card) {
                const cardDiv = document.createElement('div');
                cardDiv.className = `card fruit-${card.fruit}`;
                cardDiv.innerHTML = `<span>${card.count}</span>`;
                pileElement.appendChild(cardDiv);
            }
        }

        function checkWinCondition() {
            const openCards = [
                discards.red.length > 0 ? discards.red[discards.red.length - 1] : null,
                discards.blue.length > 0 ? discards.blue[discards.blue.length - 1] : null
            ].filter(Boolean);

            const fruitCounts = {};
            openCards.forEach(card => {
                fruitCounts[card.fruit] = (fruitCounts[card.fruit] || 0) + card.count;
            });

            for (const fruit in fruitCounts) {
                if (fruitCounts[fruit] === 5) {
                    return true;
                }
            }
            return false;
        }

        function ringBell(ringingTeam) {
            if (!canRing || !gameInProgress) return;
            canRing = false;

            const isCorrect = checkWinCondition();

            if (isCorrect) {
                messageBoxEl.textContent = `${ringingTeam.toUpperCase()} 정답!`;
                collectCards(ringingTeam);
            } else {
                messageBoxEl.textContent = `${ringingTeam.toUpperCase()} 실수!`;
                penalty(ringingTeam);
            }
            
            setTimeout(() => {
                canRing = true;
                if (gameInProgress) {
                    messageBoxEl.textContent = `${currentTurn.toUpperCase()} 팀 차례`;
                    updateUI();
                }
            }, 1500);
        }

        function collectCards(winnerTeam) {
            const pile = [...discards.red, ...discards.blue];
            decks[winnerTeam] = [...pile.reverse(), ...decks[winnerTeam]];
            clearPiles();
        }

        function penalty(penaltyTeam) {
            if (decks[penaltyTeam].length > 0) {
                const opponent = penaltyTeam === 'red' ? 'blue' : 'red';
                decks[opponent].push(decks[penaltyTeam].shift());
            }
            updateUI();
            checkGameOver();
        }

        function clearPiles() {
            discards.red = [];
            discards.blue = [];
            updateUI();
            checkGameOver();
        }
        
        function flipCard(team) {
            if (!gameInProgress || team !== currentTurn || decks[team].length === 0) return;

            const card = decks[team].shift();
            discards[team].push(card);
            
            currentTurn = (team === 'red') ? 'blue' : 'red';
            messageBoxEl.textContent = `${currentTurn.toUpperCase()} 팀 차례`;
            
            updateUI();
            checkGameOver();
        }

        function checkGameOver() {
            if (decks.red.length === 0 && discards.red.length === 0) {
                endGame('Blue');
            } else if (decks.blue.length === 0 && discards.blue.length === 0) {
                endGame('Red');
            }
        }

        function endGame(winner) {
            gameInProgress = false;
            messageBoxEl.textContent = `${winner.toUpperCase()} 팀 승리! 다시 하려면 종을 누르세요.`;
        }

        function startGame() {
            gameInProgress = true;
            currentTurn = 'red';
            createDeck();
            shuffleAndDeal();
            discards = { red: [], blue: [] };
            messageBoxEl.textContent = 'Red 팀 차례';
            updateUI();
        }
        
        document.addEventListener('keydown', (e) => {
            if (!gameInProgress) return;

            switch (e.key.toLowerCase()) {
                case 'a':
                    flipCard('red');
                    break;
                case 'l':
                    flipCard('blue');
                    break;
                case 'd':
                    ringBell('red');
                    break;
                case 'm':
                    ringBell('blue');
                    break;
            }
        });

        bellEl.addEventListener('click', () => {
            if (!gameInProgress) {
                startGame();
            }
        });
    });
    </script>
</body>
</html>
