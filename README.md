# Advanced 2D Tetris - Feel, Sound & AI

> **Tip:** Record a GIF of your game in action (using a tool like [ScreenToGif](https://www.screentogif.com/) or [LiceCap](https://www.cockos.com/licecap/)) and replace the image link above.

This is a 2D Tetris clone built from scratch in vanilla JavaScript, with a modern approach focusing on "game feel," dynamic audio, and an optional AI player. The entire project is self-contained in a **single 1000+ line HTML file**, with no external dependencies other than Three.js (loaded via CDN). This makes it an excellent case study for code organization, 2D rendering with WebGL, and implementing complex systems from the ground up.

**[➡️ Play the Live Demo](https://YOUR-USERNAME.github.io/your-repo/)**
> **Note:** Replace the link above with your GitHub Pages link after setting it up.

---

## ✨ Key Features

This is not your average Tetris clone. It was developed as a laboratory to explore features that enhance the player experience:

*   **2D Graphics Engine with Three.js:** Uses an orthographic camera to render the grid, pieces, and effects, leveraging WebGL hardware acceleration for a smooth performance.
*   **Procedural Audio Engine (WebAudio API):**
    *   **Dynamic Music:** A chiptune-style melody generated in real-time, with no audio files needed.
    *   **Contextual SFX:** Programmatically generated sound effects for every action (move, rotate, drop, line clear, etc.).
*   **"Game Feel" System:**
    *   **Adjustable Visual Effects:** `Shake` (screen tremor), `Squash & Stretch` (on block placement), `Flash` (background flashes), and particle effects.
    *   **UI Controls:** Sliders that allow the player to adjust the intensity of these effects in real-time.
*   **Optional Artificial Intelligence (AI):**
    *   **Automated Player:** An AI that can be enabled at any time to play the game on its own.
    *   **Classic Heuristics:** The AI evaluates moves based on weighted values for aggregate height, holes, bumpiness, and completed lines.
    *   **Adjustable Speed:** The AI's "thinking" and action speed can be controlled via a slider.
*   **Rich & Modern UI:**
    *   A comprehensive HUD with score, lines, level, high score, combo, and performance metrics (APM, FPS, playtime).
    *   Previews for the next piece and the held piece.
    *   Control panels for audio, "feel," and AI with a backdrop-blur effect.
    *   Light/dark theme support.
*   **Modern Gameplay Mechanics:**
    *   "7-bag" system for fair, random piece distribution.
    *   "Ghost piece" to show where the current piece will land.
    *   "Hold" function to save a piece for later.
    *   "Wall kicks" to make maneuvering near the walls easier.

---

## 🛠️ Tech Stack

*   **HTML5**
*   **CSS3** (with CSS Variables for theming)
*   **JavaScript (ES6+)** - No frameworks, just pure vanilla JS.
*   **Three.js** - For 2D rendering via WebGL.
*   **Web Audio API** - For the procedural sound and music engine.

---

## 🎮 How to Play

### Controls

| Action       | Keyboard         | Gamepad           |
| ------------ | ---------------- | ----------------- |
| **Move**     | `←` / `→`        | D-Pad or Analog   |
| **Soft Drop**| `↓`              | D-Pad or Analog   |
| **Rotate**   | `↑` / `Z`        | A / B Buttons     |
| **Hard Drop**| `Space`          | X Button          |
| **Hold Piece**| `C`             | Y Button          |
| **Pause**    | `P`              | Start Button      |
| **Restart**  | `R`              | -                 |
| **Music**    | `M`              | -                 |
| **SFX**      | `N`              | -                 |
| **Gamepad**  | `G`              | -                 |

### Objective

The goal is simple: complete horizontal lines with the falling blocks (Tetriminos). When a line is completed, it disappears, and the blocks above it fall. The game ends if the stack of blocks reaches the top of the screen.

---

## 🚀 How to Run Locally

Since this project is a single `index.html` file with no build steps, running it is extremely simple.

1.  Clone the repository:
    ```bash
    git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
    ```
2.  Navigate to the project directory:
    ```bash
    cd YOUR-REPO
    ```
3.  Open the `index.html` file in your web browser.

For the best experience (and to avoid potential browser security issues with local files), it's recommended to serve the file using a local server. If you have VS Code, you can use the **Live Server** extension. If you have Python installed, you can run:

```bash
# Python 3
python -m http.server

# Python 2
python -m SimpleHTTPServer
