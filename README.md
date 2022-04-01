# sql-gwent
## Contents
The contents of this repository contain all the data needed to populate a database with [Gwent](https://witcher.fandom.com/wiki/Gwent) cards and affiliated details.
![Structure](https://github.com/DudasDorian/sql-gwent/blob/main/db%20diagram.png)
There are 3 related attributes that each card may have: [Type, Strength, Rows, Abilities](https://witcher.fandom.com/wiki/Gwent#Card_Types) and [Faction](https://witcher.fandom.com/wiki/Gwent#Factions).
While Type and Strength are simple attributes, the rest are not. A card may be played in 1, 2, or no rows; a card may have 0 or more abilities, and its Faction will be used to check the rights to own in a deck of the same faction.
Therefore, the Rows, Abilities and Factions were split into their own tables, and were connected to the cards via another table.
There is a table for [Players that you would encounter in the game](https://witcher.fandom.com/wiki/Gwent_players) for possible developments of the gameplay.
And there are two more tables relating to the player's decks - one for storing the decks and one for storing each deck's cards. 
[Deck example, viewed as report](https://github.com/DudasDorian/sql-gwent/blob/main/Report%20examples/My%20Deck.pdf).

This structure has allowed for some quick Microsoft Access forms which could interact with the data in the database similarly to the [original game](https://witcher.fandom.com/wiki/Gwent)
_Some examples for the cards selection:_
![View all Cards](https://github.com/DudasDorian/sql-gwent/blob/main/MS%20Access%20form%20examples/cards_all.PNG)
![View all siege Cards](https://github.com/DudasDorian/sql-gwent/blob/main/MS%20Access%20form%20examples/cards_siege.PNG)
![View all special Cards](https://github.com/DudasDorian/sql-gwent/blob/main/MS%20Access%20form%20examples/cards_special.PNG)
_The ability to see one's decks and its cards_
![View deck](https://github.com/DudasDorian/sql-gwent/blob/main/MS%20Access%20form%20examples/my%20decks.PNG)
_And the forms bunched together into one, deck builder form:_
![Deck Builder](https://github.com/DudasDorian/sql-gwent/blob/main/MS%20Access%20form%20examples/deck%20builder%20stitched%20final.png)

## Additional details
In the [MS Access form examples](https://github.com/DudasDorian/sql-gwent/tree/main/MS%20Access%20form%20examples) one can find some screenshots of the Access forms.
In the [Report examples](https://github.com/DudasDorian/sql-gwent/tree/main/Report%20examples) there are some examples of reports both in pdf and rdl formats.
In the [Table contents](https://github.com/DudasDorian/sql-gwent/tree/main/Table%20contents) a copy of my data has been stored in csv files for the tables' contents and bmp for the images used.

## Context of the project
This was initially a mere school assignment, for getting to know the SQL syntax, but I went beyond that and imported all the data related to Gwent into my database.
It went through a few changes, and in the context of the game, I think it is the final version.
