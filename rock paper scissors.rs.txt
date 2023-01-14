
// Create a basic game of rock, paper, scissors

// Create a function to generate a random number between 0 and 2
function randomNumber() {
  return Math.floor(Math.random() * 3);
}

// Create a function to determine the winner of the game
function determineWinner(playerChoice, computerChoice) {
  if (playerChoice === computerChoice) {
    return "It's a tie!";
  } else if (playerChoice === "rock" && computerChoice === "scissors") {
    return "You win!";
  } else if (playerChoice === "paper" && computerChoice === "rock") {
    return "You win!";
  } else if (playerChoice === "scissors" && computerChoice === "paper") {
    return "You win!";
  } else {
    return "Computer wins!";
  }
}

// Create a function to start the game
function playGame() {
  // Ask the player for their choice
  let playerChoice = prompt("Rock, paper, or scissors?");

  // Generate a random number to determine the computer's choice
  let computerChoiceNumber = randomNumber();
  let computerChoice;

  // Convert the random number to rock, paper, or scissors
  if (computerChoiceNumber === 0) {
    computerChoice = "rock";
  } else if (computerChoiceNumber === 1) {
    computerChoice = "paper";
  } else {
    computerChoice = "scissors";
  }

  // Log the choices to the console
  console.log("Player choice: " + playerChoice);
  console.log("Computer choice: " + computerChoice);

  // Determine the winner
  let winner = determineWinner(playerChoice, computerChoice);

  // Log the winner to the console

  console.log(winner);
}

