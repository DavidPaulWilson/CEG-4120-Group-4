# Preliminary Schedule for developing Scrabble/Monopoly web app
Since the project is due the week of 4/19, it would wise to set our "due date" to be a week (or more) before that to allow last minute revisions.


## Milestone 1 - Initial Requirements
| Start Date     | End Date     |
| :----------: | -----------: |
| 1/18/21   | 1/24/21    |

1. Research technology/languages to be used for development and set up accounts
    1. Git, Gantt, Kanban, etc
2. Game suite needs to be hosted on a server
3. Set up workspace for all group members.

## Milestone 2 - Scrabble Startup
| Start Date     | End Date     |
| :----------: | -----------: |
| 1/25/21  | 2/15/21    |
1. Create blank 15x15 game board
1. Create 'bag' with 100 letter tiles & their score value
1. On first login, ask a user their name, max of 4 players
1. User can drag and drop tiles to a free space on the board
1. Tiles already played in previous turns cannot be moved
1. "Submit" button to play tiles
1. Check if word played is valid
1. Rotate active player once word is played
1. Validate all tiles are in a playable spot (connected to existing tiles)
1. Game can be played over the web

## Milestone 3 - Monopoly Startup
| Start Date     | End Date     |
| :----------: | -----------: |
| 2/16/21  | 3/9/21    |
1. Create game board, with names for each space
1. User can pick a game icon/piece (depends if we do 2D or 3D)
1. Player can roll dice and move their piece that many spaces
1. Give player starting money
1. Set up Bank with deed cards
1. Display users current money
1. Allow user to buy properties if not owned
1. User has to pay property owner if space landed on is owned
1. Passing go gives player $200
1. Game can be played over the web

## Milestone 4 - Scrabble finalizing
| Start Date     | End Date     |
| :----------: | -----------: |
| 3/10/21  | 3/24/21    |
1. Add special tiles (double word, triple letter, etc)
1. Add special tile scoring
1. Make the first word played has one letter in the middle tile
1. Add "pass" button
1. Game over sequence when there are no more tiles or 'pass' has been played by all players
1. display scoreboard


## Milestone 5 - Monopoly finalizing
| Start Date     | End Date     |
| :----------: | -----------: |
| 3/25/21  | 4/19/21    |
1. Add chance cards
1. Add communinty chest cards
1. User can hold onto change or community chest cards if permitted.
1. user can go to jail from landing on 'Go to jail' or rolling doubles 3 times in a row
1. Player can go backrupt and be 'out' of the game, while the rest of the players keep playing
    1. amtPlayers -1 going backrupt -> game over
1. Add 'Free parking' spot
1. Add Luxery Tax spot rule
1. Add utility spot rules
1. Add railroad spot rules
1. Landing on 'Go' gives player $400
1. Add houses/Hotels
