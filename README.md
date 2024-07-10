# Brick Breaker Game

This repository contains a Brick Breaker game implemented using OpenCV and Python. The game utilizes computer vision techniques to detect and interact with a colored object, such as a blue circle, which serves as the paddle for controlling the game.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Acknowledgements](#acknowledgements)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/utsavtyagi01/Augmented-Reality-Game-Using-Open-CV.git
    ```

2. Install the required dependencies:
    ```bash
    pip install opencv-python numpy
    ```

## Usage

1. Run the game:
    ```bash
    python brick_breaker.py
    ```

2. Use a blue-colored object (e.g., a blue circle) to control the paddle. Ensure your webcam is functioning properly.

3. Press the `q` key to quit the game.

## How It Works

### Game Mechanics

The game is a typical brick breaker game where a ball bounces around the screen, breaking bricks and being controlled by a paddle. The player uses a blue-colored(you can change color according to your need) object to control the paddle via a webcam. The game ends when the ball passes the paddle without being intercepted.

### Code Explanation

1. **detect_inrange Function:**
    - Converts the image to HSV color space.
    - Creates a mask to detect a specific color range (blue in this case).
    - Finds contours in the masked image and filters them based on size.
    - Returns the processed image, mask, and detected points.

2. **game Function:**
    - Initializes game parameters including ball speed, paddle position, brick layout, and score.
    - Captures video from the webcam and processes each frame.
    - Detects the blue-colored object and uses it to control the paddle.
    - Updates the ball's position and checks for collisions with bricks and the paddle.
    - Displays the game frame with the current score and game state.

3. **Main Loop:**
    - Continuously runs the `game` function until the user quits by pressing the `q` key.

