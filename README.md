Crystal Run

A small 3D arcade game built with Three.js, using 3D models generated in Vi3W.

Fly a ship down a space tunnel, collect crystals, and dodge asteroids. The game speeds up the longer you survive, and you have 3 lives.

Play

Live: (https://khuship003.github.io/crystal-run/)

Run locally (the browser needs a server to load the models):

python -m http.server 8000

Then open http://localhost:8000 and press Space.

Controls: WASD / arrow keys / mouse to move. Crystals give +10 points; asteroids cost a life.

How I used Vi3W

All three assets were made with the Vi3W sketch → image → 3D flow:

Asset	Sketch	Prompt (summary)
Ship	Triangle body with two wings	Sleek sci-fi fighter, dark grey hull, glowing blue engines, single object, plain background
Asteroid	Lumpy blob	Rocky grey-brown asteroid with craters, single object, plain background
Crystal	Diamond shape	Glowing pink faceted gem, single object, plain background

What I learned:

Each sketch needs one object only. My first attempt put all three in one image, which would have produced one merged model.
Adding "single object, plain background" to the prompt gave much cleaner results for the 3D step.
[What worked well in Vi3W]
[What was confusing or could be improved]
Tech notes
Three.js with GLTFLoader loads models/ship.glb, models/asteroid.glb and models/crystal.glb.
Each model is automatically scaled and centred on load, so any Vi3W export works without manual tuning.
If a model file is missing, the game falls back to a simple placeholder shape.
Model sizes and orientation are set in the MODELS config at the top of index.html.
Ideas for next steps
Power-ups (shield, crystal magnet)
Sound effects and a saved high score
A boss asteroid generated in Vi3W
