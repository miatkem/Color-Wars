# Color-Wars
An experiment with cellular automata with original rules, proving to create emergent properties that are quite unexpected.

# The Setting
As most cellular automatas do, this one is acted out in a grid of cells.
Each space holds properties that change each time increment takes place.
A cell can be either be empty or hold a color. Cells that hold colors also contain its population value, strength, and age.

# The Rules
The system begins with 5 populations each assigned a random color. (The amount can be changed by changing the numPop varible on line 5)

Each increment of time the cell reproduces once in a random direction (U,D,L,R). <ul><li>If the color already exists there then nothing happens. <li>If nothing exists there that cell becomes that color, the age is set to 0 and its strength is randomly mutated to be any between 3 points worse than its parent cell or three points stronger. (The mutation range can be changed by changing the maxMutation and minMutation varibles.) <li>If another color exists at the new cell a fight takes place. <ul><li>If the new mutated strength is greater than the strength of the current resident of the cell the current resident is replaced by the color.<li> If the new mutated strength is less than the strength of the current resident of the cell the current resident's strength is subtracted by the mutated strength of the attacker. <li>Finally if the two strengths or equal the cell is set to empty</li></ul>
</li></ul>

Each increment of time the age of every existing cell is incremented by 1.
If a cell's strength is less than its age than it dies off and becomes an empty cell.

# Features
<b>Click</b> to add a new population. It will create a 3 by 3 block with the strength equal to the average stength of the entire system allowing it a fighting chance at anytime during the run process.(It may take a few clicks though)

# Emergent Properties
The strong few -- one thing that happens often is that one color will be forced to a very small size and then suddenly over take the other color in an impressive comeback. Because of this a fight between two colors can go back and forth for a very long time.

Constant give and take -- when different colors are fighting for cells, if one part of the grid is being taken by "red" there is a good chance at the same time another part of the grid is be taken by the same color thats loosing to "red".

Don't get cornered -- although edges aren't bad for dwindling populations a corner could be the end for a color. It seems to be hard to come back from being shoved into a corner by a larger population.

Too many cooks -- the more populations alive in the system the faster they die off. This property is true all the way to the end. The fight between the last two will be longer than the fight between the last three and so on to the starting five.
