# 3-Card-Poker-JavaFX

A JavaFX + Maven implementation of the casino game **Three Card Poker** with support for **single-player** and **two-player** modes. The project uses **FXML** for layout, **CSS** for styling, and event-driven logic for gameplay flow. [file:2]

## Overview

This project recreates a custom version of **3 Card Poker** where each player competes only against the dealer, not against each other. The application includes a welcome screen, player-selection screen, gameplay screens, betting flow, outcome messages, total winnings tracking, and a menu with **Exit**, **Fresh Start**, and **New Look** options. [file:2]

## Features

- Single-player and two-player modes. [file:2]
- Ante and optional Pair Plus wagers, each limited to $5–$25. [file:2]
- Dealer qualification rule: dealer must have at least **Queen high**. [file:2]
- Pair Plus payout logic based only on the player’s hand. [file:2]
- JavaFX GUI built with FXML and styled with CSS. [file:2]
- JUnit 5 tests for game logic, deck behavior, and dealer behavior. [file:2]

## Game Rules

Each player starts by placing an **Ante** bet, and may also place an optional **Pair Plus** bet. After the cards are dealt, players choose whether to **Play** or **Fold**. If a player folds, they lose their Ante and Pair Plus wagers. [file:2]

If a player chooses to play, the **Play wager** must equal the Ante. If the dealer does not qualify with at least **Queen high**, the Play wager is returned and the Ante is pushed. If the dealer qualifies, the player hand is compared to the dealer hand. [file:2]

### Pair Plus Payouts

- Straight Flush: 40 to 1 [file:2]
- Three of a Kind: 30 to 1 [file:2]
- Straight: 6 to 1 [file:2]
- Flush: 3 to 1 [file:2]
- Pair: 1 to 1 [file:2]

### Hand Rankings

The project uses this hand order:

- Straight Flush [file:2]
- Three of a Kind [file:2]
- Straight [file:2]
- Flush [file:2]
- Pair [file:2]
- High Card [file:2]

## Project Structure

Typical project components include:

- `JavaFXTemplate.java` – application entry point.
- `MyController.java` – main event-driven game controller.
- `SelectPlayer.java` – controller for player selection screen.
- `Card.java` – card model.
- `Deck.java` – shuffled 52-card deck.
- `Dealer.java` – dealer logic and dealing behavior.
- `Player.java` – player state, bets, and winnings.
- `ThreeCardLogic.java` – hand evaluation and comparison logic.
- FXML files for welcome, selection, and game screens.
- CSS files for theme switching. [file:2]

## How to Run

Run the project from the root of the Maven project.

### Compile and run
```bash
mvn clean compile exec:java -Dexec.mainClass="JavaFXTemplate"
```

### Run tests
```bash
mvn test
```

The project is expected to run from the command line using Maven. That is part of the assignment requirements. [file:2]

## How to Play

1. Launch the program.
2. On the welcome screen, choose **Start Game**.
3. Select **1 Player** or **2 Players**.
4. On the game screen, press **Deal**.
5. Enter the Ante wager and optional Pair Plus wager.
6. Press **Place Bets**.
7. Choose **Play** or **Fold**.
8. Read the game result shown in the info area and continue to the next round.

## Menu Options

Under the **Options** menu:

- **Exit** – leaves the current game flow and returns to the exit/welcome path. [file:2]
- **Fresh Start** – resets winnings and starts over. [file:2]
- **New Look** – switches the CSS theme for the interface. [file:2]

## Testing

This project includes **JUnit 5** tests in `src/test/java`. The assignment requires at least:

- 20 tests for `ThreeCardLogic` [file:2]
- 10 tests for `Deck` and `Dealer` [file:2]

Only logic is tested with JUnit; JavaFX graphical elements are not part of unit testing. [file:2]

## Notes

This project follows a custom class design and method signatures specified by the assignment, including the required classes `Card`, `Deck`, `Dealer`, `Player`, `ThreeCardLogic`, and `JavaFXTemplate`. [file:2]

The GUI must be implemented with **FXML** and **CSS**, but runtime updates to image views and UI state are allowed through controller code. [file:2]

## Author

**Denys Zabiyaka**  
NetID: **dzabi2**  
Email: **dzabi2@uic.edu**
