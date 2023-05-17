def display_board(board):
    for row in board:
        print("|".join(row))
        print("-----")

def get_move():
    row = int(input("Enter the row (0-2): "))
    col = int(input("Enter the column (0-2): "))
    return row, col

def validate_move(board, row, col):
    if row < 0 or row > 2 or col < 0 or col > 2:
        return False
    if board[row][col] != " ":
        return False
    return True

def check_winner(board):
    # Check rows
    for row in board:
        if row[0] == row[1] == row[2] != " ":
            return row[0]

    # Check columns
    for col in range(3):
        if board[0][col] == board[1][col] == board[2][col] != " ":
            return board[0][col]

    # Check diagonals
    if board[0][0] == board[1][1] == board[2][2] != " ":
        return board[0][0]
    if board[0][2] == board[1][1] == board[2][0] != " ":
        return board[0][2]

    return None

def play_game():
    board = [[" "]*3 for _ in range(3)]
    current_player = "X"

    while True:
        display_board(board)
        print(f"Player {current_player}'s turn.")
        row, col = get_move()

        if validate_move(board, row, col):
            board[row][col] = current_player
            winner = check_winner(board)
            if winner:
                display_board(board)
                print(f"Player {winner} wins!")
                break
            elif all(row.count(" ") == 0 for row in board):
                display_board(board)
                print("It's a tie!")
                break
            else:
                current_player = "O" if current_player == "X" else "X"
        else:
            print("Invalid move. Try again.")

play_game()
