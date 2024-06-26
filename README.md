## Duality of Mousekind
This project is a simple game that utilizes the client/server techniques illustrated above. The client sends information about the two mouse cursors' positions  to the server, and it draws elements of the game based on information received from the server. Mechanics like target generation, black box positioning/spawning, and scoring are all handled by the server, and the client renders the game based on that info. In terms of derived fields, the game's score is essentially a derived field, since it will only increase if the cursor's position, a non-derived field, is close enough to a target, which is also a non-derived field. Finally, for the clientside rendering, the two "play area" squares are in a flexbox rendering in column mode, along with a few spacer elements and the score. The black boxes and cursor are rendered with absolute positioning so they do not interfere with anything else.

https://a2-patrickhunter.glitch.me
**NOTE**: Since this project communicates with the server at a high frequency, the glitch website will recieve too many requests rather quickly, so localhosting it is a better option.

## Technical Achievements
- **Tech Achievement 1**: By having the entire state of the game managed on the server, this webpage can be ran on a single page. If you were to have two instances of the game running at the same time, both would not only be playable, but would hold the same exact game state.
- **Tech Achievement 2**: Since the current mouse positions and score are stored in the server, they are constantly being modified.