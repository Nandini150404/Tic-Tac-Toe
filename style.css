let currentPlayer = 'X';
let board = ['', '', '', '', '', '', '', '', ''];
let gameover = false;

function makeMove(index) {
    if (!gameover && board[index] === '') {
        board[index] = currentPlayer;
        const cellElement = document.getElementsByClassName('cell')[index];
        cellElement.textContent = currentPlayer;
        
        // Add background color based on the current player
        cellElement.style.backgroundColor = currentPlayer === 'X' ? '#EF6262' : '#00DFA2';
        
        document.getElementById('message').textContent = `Player ${currentPlayer}'s turn`;

        if (checkWin(currentPlayer)) {
            document.getElementById('message').textContent = `Player ${currentPlayer} wins!`;
            gameover = true;
        } else if (checkDraw()) {
            document.getElementById('message').textContent = "It's a draw!";
            gameover = true;
        }

        currentPlayer = currentPlayer === 'X' ? 'O' : 'X';
    }
}



function checkWin(player) {
    const winCombinations = [[0, 1, 2], [3, 4, 5], [6, 7, 8],[0, 3, 6], [1, 4, 7], [2, 5, 8],[0, 4, 8], [2, 4, 6]];
    for (const [a, b, c] of winCombinations) {
        if (board[a] === player && board[b] === player && board[c] === player) {
            return true;
        }
    }

    return false;
}

function checkDraw() {
    return !board.includes('');
}

function resetBoard() {
    currentPlayer = 'X';
    board = ['', '', '', '', '', '', '', '', ''];
    gameover = false;

    const cells = document.getElementsByClassName('cell');
    for (let i = 0; i < cells.length; i++) {
        cells[i].textContent = '';
        cells[i].style.backgroundColor = ''; // Remove background color
    }

    document.getElementById('message').textContent = `Player ${currentPlayer}'s turn`;
}


document.getElementById('message').textContent = `Player ${currentPlayer}'s turn`;
