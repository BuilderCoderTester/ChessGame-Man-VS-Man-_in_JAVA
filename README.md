# ♟️ Java Chess Game

A fully functional chess game built in Java using Swing GUI, featuring complete chess rules implementation, pawn promotion, and win condition detection.


## 🎮 Features

- **Complete Chess Implementation**: All piece movements following official chess rules
- **Interactive GUI**: Clean and intuitive graphical interface using Java Swing
- **Pawn Promotion**: Automatic pawn promotion with player choice dialog
- **Game State Management**: 
  - Turn-based gameplay (White vs Black)
  - Check and Checkmate detection
  - Stalemate detection
  - King capture win condition
- **Visual Feedback**: 
  - Piece selection highlighting
  - Custom chess board colors
  - Smooth piece movement

## 🚀 Getting Started

### Prerequisites

- Java Development Kit (JDK) 8 or higher
- Java IDE (IntelliJ IDEA, Eclipse, VS Code, etc.) or command line

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/java-chess-game.git
   cd java-chess-game
   ```

2. **Set up piece images**
   - Create an `images` folder in your project directory
   - Add chess piece PNG files with the naming convention:
     - `w_pawn.png`, `w_rook.png`, `w_knight.png`, `w_bishop.png`, `w_queen.png`, `w_king.png`
     - `b_pawn.png`, `b_rook.png`, `b_knight.png`, `b_bishop.png`, `b_queen.png`, `b_king.png`

3. **Update image path**
   - Modify the file path in `loadImages()` method to point to your images folder:
   ```java
   BufferedImage img = ImageIO.read(new File("images/" + name + ".png"));
   ```

### Running the Game

**Option 1: Using IDE**
1. Open the project in your preferred Java IDE
2. Run the `ChessGame.java` file

**Option 2: Command Line**
```bash
javac *.java
java ChessGame
```

## 🎯 How to Play

1. **Start Game**: The game opens with the standard chess starting position
2. **Make Moves**: 
   - Click on a piece to select it (yellow highlight appears)
   - Click on a valid destination square to move
   - Only valid moves according to chess rules are allowed
3. **Pawn Promotion**: When a pawn reaches the opposite end, choose your promotion piece
4. **Win Conditions**: 
   - Checkmate: King is in check with no legal moves
   - King Capture: King is captured
   - Stalemate: No legal moves available but not in check

## 🏗️ Project Structure

```
java-chess-game/
├── ChessGame.java          # Main game class with GUI and game logic
├── ChessLogic.java         # Chess piece movement validation
├── PawnPromotion.java      # Pawn promotion functionality
├── images/                 # Chess piece images (PNG format)
└── README.md              # This file
```

## 🧩 Core Components

### ChessGame.java
- Main game panel extending JPanel
- Handles mouse input and user interactions
- Manages game state and turn logic
- Renders the chess board and pieces

### ChessLogic.java
- Validates piece movements according to chess rules
- Implements movement logic for all piece types:
  - Pawns (including initial two-square move and diagonal capture)
  - Knights (L-shaped movement)
  - Bishops (diagonal movement)
  - Rooks (horizontal and vertical movement)
  - Queens (combination of bishop and rook)
  - Kings (one square in any direction)

### PawnPromotion.java
- Handles pawn promotion when reaching the opposite end
- Provides player choice dialog for promotion piece selection
- Supports both standard and restricted promotion rules

## 🎨 Customization

### Board Colors
Modify the color constants in `ChessGame.java`:
```java
private static final Color WHITE_COLOR = new Color(198, 255, 171);
private static final Color BROWN_COLOR = new Color(0, 128, 0);
private static final Color SELECT_COLOR = new Color(255, 255, 0, 128);
```

### Board Size
Adjust the dimensions:
```java
private static final int WIDTH = 480, HEIGHT = 518;
```

### Promotion Rules
Choose between standard chess rules or custom restrictions in the pawn promotion system.

## 🐛 Known Issues

- ⚠️ No castling implementation yet
- ⚠️ No en passant capture
- ⚠️ Hardcoded image paths need to be updated for your system
- ⚠️ No move history or undo functionality

## 🔮 Future Enhancements

- [ ] Implement castling
- [ ] Add en passant capture
- [ ] Move history and notation
- [ ] Game save/load functionality
- [ ] AI opponent
- [ ] Online multiplayer
- [ ] Move timer
- [ ] Sound effects

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with Java Swing for cross-platform compatibility
- Chess piece images (source your image credits here)
- Inspired by the timeless game of chess

## 📞 Contact

**Your Name** - sarkaranurag556@gmail.com

Project Link: [https://github.com/yourusername/java-chess-game](https://github.com/yourusername/java-chess-game)

---

⭐ **Star this repository if you found it helpful!**
