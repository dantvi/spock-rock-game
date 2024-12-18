# Spock Rock Game

The Spock Rock Game is an interactive and responsive implementation of the expanded "Rock, Paper, Scissors, Lizard, Spock" game. Built using HTML, CSS, and JavaScript, this project offers an engaging way to play against a computer opponent with real-time updates and dynamic visual feedback.

This project was developed as part of the course "JavaScript Web Projects: 20 Projects to Build Your Portfolio" by Zero To Mastery.

## Table of contents

- [Spock Rock Game](#spock-rock-game)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [Screenshot](#screenshot)
    - [Links](#links)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Useful resources](#useful-resources)
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)

## Overview

This game is an extension of the classic "Rock, Paper, Scissors," adding two additional options: Lizard and Spock. It includes:
- Real-time interaction with a user-friendly interface.
- Dynamic score tracking for both the player and the computer.
- Visual feedback for player and computer choices.
- Confetti animation when the player wins.
- Responsive design for optimal experience across devices.

### Screenshot

![](./screenshot.png)

### Links

- Live Site URL: [DT Code](https://spock-rock-game.dtcode.se/)

### Built with

- HTML5: Semantic structure for accessibility.
- CSS3:
  - Flexbox for layout.
  - Media queries for responsive design.
  - Font Awesome icons for intuitive gameplay visuals.
- JavaScript (ES6+):
  - Modular design for importing confetti effects.
  - Logic for gameplay, random computer choices, and dynamic score updates.
  - DOM manipulation for real-time interactivity.

### What I learned

Through this project, I enhanced my skills in:
- Creating an engaging and interactive game interface using DOM manipulation.
- Implementing complex game logic with multiple winning conditions.
- Using JavaScript modules for organizing code and importing effects like confetti.
- Designing a responsive layout to ensure usability across devices.

The following code snippet demonstrates how the game processes player and computer choices:

```js
function updateScore(playerChoice) {
  if (playerChoice === computerChoice) {
    resultText.textContent = "It's a tie.";
  } else {
    const choice = choices[playerChoice];
    if (choice.defeats.indexOf(computerChoice) > -1) {
      startConfetti();
      resultText.textContent = "You Won!";
      playerScoreNumber++;
      playerScoreEl.textContent = playerScoreNumber;
    } else {
      resultText.textContent = "You Lost!";
      computerScoreNumber++;
      computerScoreEl.textContent = computerScoreNumber;
    }
  }
}
```

### Useful resources

- [MDN: Math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random) - Used for generating random computer choices.
- [MDN: JavaScript Modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules) - Helped organize the code and import confetti effects.
- [Font Awesome](https://fontawesome.com/) - Icons used for gameplay visuals.

## Author

- GitHub - [@dantvi](https://github.com/dantvi)
- LinkedIn - [@danieltving](https://www.linkedin.com/in/danieltving/)

## Acknowledgments

Special thanks to Zero To Mastery for their comprehensive course material and to MDN Web Docs for their excellent resources on JavaScript and web development.
