# Creative Coding Major Project 
cora's individual part 


## How to Interact
- **Click** anywhere on the canvas to generate a new animated circle with unique styling.
- **Hover your mouse** near any existing circle to attract it gently toward the cursor.
- Press **spacebar** to **pause/resume** the animation.
- Use the **↑ / ↓ arrow keys** to **increase or decrease** animation speed.
- Press **C** to **clear** all circles from the screen.

> There are no circles on load – you create your own visual composition by interacting with the canvas.


## My Individual Approach to Animation
### Animation Driver
I chose the **user input** to create animation where the user directly determines the shape and evolution of the visual through 
real-time input. Instead of passive or timed animations, I emphasized user agency: no two visual compositions will look the same.

The animation is entirely **interaction-based**:
- Circles only **appear on mouse clicks** and **move independently** using random velocity, but also respond to mouse proximity with smooth attraction.
- They are attracted to the **mouse pointer** when close.
- Their **movement speed** is controlled by **keyboard input**.

### Visual Inspiration
Inspired by:
- ** [Complexity Explorables] (complexity-explorables.org) ** – A collection of interactive visual essays that explore complex systems through code.
- **Generative art** on [openprocessing.org](https://www.openprocessing.org/) – especially those involving mouse-trail and bounce effects.

These references inspired my decision to let the mouse guide the scene composition and movement.

A short technical explanation of how your individual code works to animate the image and any appropriate references.
If you made a lot of changes to the group code, explain it here.
If you use tools and technique from outside the course, explain why you used them and how they work.
If you copy a technique from the Internet, explain how it works, why you used it, and where it came from.

### Technical Overview
- Each circle is an instance of one of four custom classes.
- When the mouse is pressed, a new circle object is created at `mouseX`, `mouseY` and pushed to an array.
- Each frame (`draw()` loop):
  - If not paused, every circle calls `.move()`:
    - If near the mouse, it slowly moves toward it.
    - Otherwise, it bounces around the screen.
  - `.display()` draws the animated pattern using custom visuals.
- Speed is modified via a `speedMultiplier` controlled by key presses.

#### External Code / Techniques:
- I implemented a **mouse attraction logic** adapted from [Daniel Shiffman’s Nature of Code](https://natureofcode.com/) vector-based examples.
- `drawSpiral()`, `drawCirclePoints()` and custom ring patterns were inspired by class demos and modified for aesthetic consistency.

#### Modifications to Group Code
- Removed the default creation of 64 circles on page load.
- Added `mousePressed()` for user-created circles.
- Integrated `keyPressed()` to handle speed control, pause/resume, and clear actions.
- Applied attraction logic to all four circle pattern classes.

#### Acknowledgements & Sources
- No external libraries used – code is based on core p5.js 
- The Nature of Code – Attraction/Bouncing examples
- Group feedback during workshops

