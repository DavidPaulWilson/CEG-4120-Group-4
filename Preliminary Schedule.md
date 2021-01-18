# Preliminary Schedule for CEG-4120 Course Project: Combined Scrabble/Monopoly Game Suite
Since the project is due the week of 4/19, it would wise to set our "due date" to be a week (or more) before that to allow last minute revisions.


## Milestone 1 - Initial Requirements
| Start Date     | End Date     |
| :----------: | -----------: |
| 1/18/21   | 1/24/21    |

1. Select tools and languages to be used for development.
2. Create individual accounts for each developer to use each selected tool.
    1. E.g., Git, Gantt, Kanban, etc.
3. Host game suite on a server.
4. Set up workspace for all group members.

## Milestone 2 - Scrabble Foundation
| Start Date     | End Date     |
| :----------: | -----------: |
| 1/25/21  | 2/15/21    |
1. Build or establish a dictionary to use for validating words.
1. Create a blank 15x15 game board.
1. Create a 'bag' with 100 letter tiles & their individual score values.
1. Ask each user their name at first login, to a max of four players.
1. Build a score card with each player's name and current score.
1. Start each game with the first player named on the score card, with play to proceed in a logical order vertically (top to bottom) or horizontally (left to right).
1. Allow users to drag and drop tiles to a free spaces that are aligned horizontally or vertically on the board.
1. Create a "Submit" button to begin the tile-validation process.
1. Validate all tiles are in a playable spot, i.e., connected to existing tiles.
1. Read the tiles placed and all connected tiles to generate a list of added words.
1. Validate each word played on the tiles against the list of existing words to ensure no duplicates.
1. Validate each word played on the tiles against the dictionary. **(TODO: Do we want to check each word every turn, or do we want to implement a user-based "challenge" feature?)**
1. Display a warning message if any of the words given are invalid and explain which rule was broken.
1. "Lock" placed tiles at the end of the current turn if they are validated, disallowing users to move tiles that were already placed.
1. Calculate the player's score from the values of each tile used to build the current turn's word list.
1. Add the new points to the active player's total score on the score card.
1. Begin a new turn after scoring is complete, with the next player on the score card becoming the active player.
1. Ensure the game can be played over the Internet.

## Milestone 3 - Monopoly Foundation
| Start Date     | End Date     |
| :----------: | -----------: |
| 2/16/21  | 3/9/21    |
1. Create a game board with names for each space reflecting the traditional Monopoly board.
1. Ask each player their name at first login, to a max of four players.
1. Build a score card with each player's name and current money total.
1. Set each player's initial status to "Clear," representing that they are ready to play as normal without any special rules in place.
1. Define a readout area that explains to the player what happens at each step of the game, stating such actions as "Player has spent $X."
1. Establish deed cards for each purchasable property on the board, with each containing the property's name, color-coded set identity, purchase price, and rental fee, with the exception of utilities and railroads.
1. Give each user a way to check their purchased properties and all free properties, the latter of which may be identified as property of "The Bank."
1. Allow each player to pick a piece to represent them, with each piece belonging to a maximum of one player per game.
1. Give each player the traditional starting money. **(TODO: How much money is this?)**
1. Start each game with the first player named on the score card, with play to proceed in a logical order vertically (top to bottom) or horizontally (left to right).
1. Allow active player to begin their turn by rolling the dice.
1. Move the active player's piece as many spaces as the total face value on the dice.
1. Allow the active player to choose whether or not to purchase property they land on if it is owned by The Bank.
1. Move the deed to the property from The Bank to the active player if it is purchased.
1. Deduct money from the active player's total, up to the maximum of the associated property's rental fee, if the property they on is owned by another player.
1. Assign a value of "Bankrupt" to the active player if they cannot pay their total rental fee.
1. Reassign ownership of any Bankrupt player's properties to the bank.
1. Display a "End Turn" button that players can press to rotate to the next round, providing an automatic pause to allow them to read the results of the current turn.
1. Ensure the "End Turn" button is only clickable or only visible after the player has rolled the dice, moved, and resolved the effects of any space on which they land.
1. Begin the next turn when the "End Turn" button is pressed, rotating to the next player on the score card without a status of "Bankrupt."
1. Add $200 to the active player's money total if they pass the space designated "Go."
1. Ensure the game ends when only one player does not have a status of "Bankrupt," checking each time the "End Turn" button is pressed.
1. Ensure the game can be played over the Internet.

## Milestone 4 - Scrabble Finalization
| Start Date     | End Date     |
| :----------: | -----------: |
| 3/10/21  | 3/24/21    |
1. Add special tiles to the game board, e.g., double score tiles and triple score tiles.
1. Tweak score calculation at the end of each turn to incorporate bonuses from special tiles.
1. Require the first word played to have one letter on the middle tile of the game board.
1. Add a "Pass" button to allow players to skip their own turn.
1. Play a "Game Over" sequence that is triggered when either the bag of tiles is empty or when each player consecutively passes.
1. **TODO: If we decide to include a "Challenge" function, we could place that and the "dictionary" elements of the Scrabble Foundation here.**


## Milestone 5 - Monopoly Finalization
| Start Date     | End Date     |
| :----------: | -----------: |
| 3/25/21  | 4/19/21    |
1. Add a mortage value to each property deed.
1. Add an unmortgage fee to each property deed, which will be equal to 110% of the same property's mortgage value.
1. Add a schedule of house and hotel purchase prices and rental fees to each property deed.
1. Allow the active player to mortgage individual properties they own to add that deed's mortgage value to their money total.
1. Allow the active player to unmortgage owned properties by paying the unmortgage fee of the deed.
1. Prevent the active player from having to pay rent on properties that are mortgaged.
1. Add all "Chance" cards.
1. Add all "Communinty Chest" cards.
1. Ensure the active player receives the appropriate type of card when landing on the matching space.
1. Allow the active player to hold "Get Out of Jail Free" cards for later use when they are drawn.
1. Allow players that roll doubles on the dice to take an additional turn after completing their current turn.
1. Set the active player's status from "Clear" to "Jailed" if they either land on the 'Go to Jail' space or roll doubles three times in a row. **(TODO: We will need to remember to us a special flag and count variable. We may not be able to simply refer to the current state of the dice if any of the cards require the players to reroll them for any reason.)**
1. Move the piece representing a "Jailed" player to the "Jail" space.
1. Disallow the active player to enter the normal turn routine if their status is "Jailed."
1. Allow the active player, if they are "Jailed," to attempt to leave jail by either paying a $50 fine, returning a held "Get Out of Jail Free Card" to the appropriate stack, or attempting to roll doubles.
1. Set the active player's status from "Jailed" to "Clear" if they roll doubles while jailed, and then return them to the normal turn routine with the value of the dice already established.
1. Record the number of failed dice rolls a player makes while jailed, disallowing them to roll again if they fail to get doubles after three dice rolls.
1. Require the player to choose to either spend a "Get Out of Jail Free" card or pay a $50 fine to leave jail if they reach three failed die rolls, resetting their status to "Clear" and returning to the normal turn routine with the value of the dice already established.
1. Add functionality for the "Free Parking" space, if any. **(TODO: What functionality should we use for this spot?)**
1. Add functionality for the "Income Tax" space, requiring the active player landing on it to pay their choice of either $200 or 10% of the combined purchase prices and improvement prices of their properties, up to their current improvement level on each. **(TODO: Should we display this latter value to the player so they can make an informed choice? Should we take a different value for mortgaged versus non-mortgaged proeperties? Also, some versions simplify this space by removing the percentage option. Should we do this as well?)**
1. Add functionality for the "Luxury Tax" space, requiring the active player to pay $100 if they land on it.
1. Establish deed cards for utility and railroad properties on the board, with each containing the property's name, set identity, purchase price, and dynamic rental fees based on the owner's percentage of the set.
1. Ensure that utility properties have a dynamic rental value based on the percentage of total utilities with the same owner: 4x the dice total for 50% or 10x the dice total for 100%.
1. Ensure that railroad properties have a dynamic rental value based on the percentage of total railroads with the same owner: $25 for 25%, $50 for 50%, $100 for 75%, or $200 for 100%.
1. Add a schedule of rental fees, improvement prices, and improvement sale values to each property, except for utilities and railroads, to create an "improvement" system, i.e., houses and hotels.
1. Allow the active player to improve a property with an additional house or hotel by paying the appropriate improvement price so long as they own each other property in the matching set.
1. Disallow the active player to improve a property more than one step higher than the other properties in the matching set.
1. Allow the active player to sell an improvement on an owned property, reducing the improvement level of that property by one and adding the matching improvement sale value to their money total.
1. Require the active player to pay an appropriately elevated amount of rent if they land on a non-mortgaged property owend by another player that has houses or a hotel on it.
1. Allow each player unable to pay a required fee with their money total to sell improvement levels they own or mortgage non-mortgaged individual properties they own until they have enough money to pay the fee, then deduct the required fee from their total.
1. Assign a status of "Bankrupt" to the active player if they do not have enough money to pay any fee required by a card or by Jail and have no improvements left to sell or non-mortgaged properties left to mortgage.
1. **(TODO: Should we add a function to auction properties when players go bankrupt? Should we add a function to auction unowned properties players decline to purchase at the end of their turn?)**