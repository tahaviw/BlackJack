# BlackJack

BlackJack is a browser-based card game built with vanilla JavaScript that recreates the core mechanics of the classic casino experience. The project focuses on interactive gameplay, real-time DOM rendering, and dynamic game state management while maintaining a clean and responsive user interface.

This application was developed as a front-end practice project to strengthen JavaScript fundamentals including arrays, objects, conditional logic, loops, functions, and DOM manipulation.

---

## Features

- Dynamic card generation using randomized game logic
- Real-time rendering of player cards and score
- Automated BlackJack win detection
- Conditional game state handling for win/loss scenarios
- Interactive UI with responsive button actions
- Player profile display with chip balance tracking
- Array-based hand management system
- Live game status messaging and updates

---

## Built With

- HTML5
- CSS3
- JavaScript ES6

---

## Project Structure

```bash
BlackJack/
│
├── index.html
├── index.css
├── index1.js
└── feuille-de-feutrine-epaisse-2mm-vert-format-a4.jpg
```

---

## Installation & Setup

### Clone the Repository

```bash
git clone https://github.com/your-username/blackjack.git
```

### Navigate to the Project Directory

```bash
cd blackjack
```

### Launch the Project

Option 1 — Open the HTML file directly in your browser:

```bash
open index.html
```

Option 2 — Run using VS Code Live Server:

```bash
Right Click on index.html -> Open with Live Server
```

---

## Usage

1. Click the **START GAME** button to begin a new round.
2. The application automatically generates two random cards.
3. The current cards and total score are displayed on the screen.
4. Click **NEW CARD** to draw an additional card.
5. Reach a total score of **21** to win the game.
6. Exceeding **21** results in an automatic loss state.

---

## Game Logic

### Randomized Card Generation

The game simulates a simplified deck system using JavaScript's `Math.random()` method.

Card value rules:

- Cards greater than `10` are converted to `10`
- Ace (`1`) is converted to `11`
- All remaining cards retain their numeric value

```javascript
function getRandomCard () {
    let randomNumber = Math.floor(Math.random() * 13) + 1    

    if (randomNumber > 10) {
        return 10    
    } else if (randomNumber === 1) {
        return 11
    } else {
        return randomNumber
    }
}
```

---

### Player Hand Management

The player's hand is managed using a JavaScript array:

```javascript
let cards = []
```

Each newly generated card is pushed into the array dynamically:

```javascript
cards.push(card)
```

The total score is continuously recalculated and rendered after every draw.

---

### Dynamic DOM Rendering

The application updates the interface in real time using:

- `document.querySelector()`
- `document.getElementById()`
- `textContent`

Core UI elements updated dynamically:

- Current player cards
- Total score
- Player information
- Win/loss messages

---

### Game State Validation

The game uses Boolean flags to control gameplay flow:

```javascript
let hasBlackJack = false
let isAlive = false
```

Validation logic ensures:

- Players cannot continue after losing
- Additional cards cannot be drawn after achieving BlackJack
- UI state updates instantly after every action

---

## Future Improvements

- Add a full 52-card deck system
- Implement betting mechanics and score persistence
- Add restart and reset functionality
- Improve mobile responsiveness
- Add animations and sound effects
- Store player statistics using Local Storage

---

## Author

Taha Belghiti — Junior Front-End Developer  
Built with HTML, CSS, and JavaScript · © 2026
