# TCP-Chess-Cpp

Chess game on a concurrent TCP server that allows multiple clients to play at the same time (made on linux operating system)

- client interface made using QT
- server uses multiplexing to manage client commands (concurrent due to the turn based nature of the game)

# Game Implementation
The server generates a game board for each session of players (Piece *board[8][8]). After each player's move, it checks if the king is in check by starting from the king's position and verifying all possible attack angles (diagonals, lines, columns, etc.).
