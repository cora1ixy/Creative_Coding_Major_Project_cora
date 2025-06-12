# Creative_Coding_Major_Project
Group component for major project

# 🌀 Animated Circle Patterns – Interactive Canvas

## 🖱 How to Interact
- **Click** anywhere on the canvas to generate a new animated circle with unique styling.
- **Hover your mouse** near any existing circle to attract it gently toward the cursor.
- Press **spacebar** to **pause/resume** the animation.
- Use the **↑ / ↓ arrow keys** to **increase or decrease** animation speed.
- Press **C** to **clear** all circles from the screen.

> There are no circles on load – you create your own visual composition by interacting with the canvas.

---

## 🎨 My Individual Approach to Animation
I focused on creating an **interaction-driven animation experience** where the user directly determines the shape and evolution of the visual through real-time input. Instead of passive or timed animations, I emphasized user agency: no two visual compositions will look the same.

---

## 🚀 Animation Driver: Interaction
The animation is entirely **interaction-based**:
- Circles only appear on **mouse clicks**.
- They are attracted to the **mouse pointer** when close.
- Their **movement speed** is controlled by **keyboard input**.

This direct, physical-style interaction makes the animation feel more like a living system that reacts to the user’s actions.

---

## 🧬 Animated Properties & Uniqueness
Compared to other group members:
- 🔁 My circles **move independently** using random velocity, but also respond to mouse proximity with smooth attraction.
- 🌀 I do **not** use audio or Perlin noise — I focus purely on **user input** to shape the experience.
- 🖌 Each circle has a **unique visual style**, randomly chosen from four custom-designed pattern classes (Cora, Yin, Kristien1, Kristien2).
- 🔄 The user can continuously modify the canvas through interaction, rather than watching a pre-set animation.

---

## 🌈 Visual Inspiration
Inspired by:
- **João Pombeiro’s collage animations** – their randomness and layering.
- **Generative art** on [openprocessing.org](https://www.openprocessing.org/) – especially those involving mouse-trail and bounce effects.

These references inspired my decision to let the mouse guide the scene composition and movement.

---

## 🛠 Technical Overview
- Each circle is an instance of one of four custom classes.
- When the mouse is pressed, a new circle object is created at `mouseX`, `mouseY` and pushed to an array.
- Each frame (`draw()` loop):
  - If not paused, every circle calls `.move()`:
    - If near the mouse, it slowly moves toward it.
    - Otherwise, it bounces around the screen.
  - `.display()` draws the animated pattern using custom visuals.
- Speed is modified via a `speedMultiplier` controlled by key presses.

### External Code / Techniques:
- I implemented a **mouse attraction logic** adapted from [Daniel Shiffman’s Nature of Code](https://natureofcode.com/) vector-based examples.
- `drawSpiral()`, `drawCirclePoints()` and custom ring patterns were inspired by class demos and modified for aesthetic consistency.

---

## ✏️ Modifications to Group Code
- Removed the default creation of 64 circles on page load.
- Added `mousePressed()` for user-created circles.
- Integrated `keyPressed()` to handle speed control, pause/resume, and clear actions.
- Applied attraction logic to all four circle pattern classes.

---

## 🧩 Tools & Techniques Beyond the Course
- Used randomness in shape/style generation to simulate diversity.
- Avoided using audio libraries or time-based triggers to keep the focus on interaction.
- No external libraries used – code is based on core `p5.js` and object-oriented techniques covered in class.

---

## 📚 Acknowledgements & Sources
- The Nature of Code – Attraction/Bouncing examples
- p5.js documentation for interactivity and animation
- Group feedback during workshops

---

Made by **[Your Name]** ✨ – one circle at a time.
