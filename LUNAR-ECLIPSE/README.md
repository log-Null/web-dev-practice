# Blood Moon Lunar Eclipse Simulation

This is a simple **HTML + CSS project** that simulates a **lunar eclipse (Blood Moon)** with a glowing moon, moving shadow, and date text.

## Demo

- The Moon glows with a soft halo.
- A black shadow slowly moves across the Moon to simulate the Earth’s shadow.
- The date and title appear in a spooky monospace font above the Moon.
- <img width="1920" height="1020" alt="Screenshot 2025-09-07 212536" src="https://github.com/user-attachments/assets/f7260f0e-249c-4eb8-a23d-6d5411492d46" />

## Features

- **Glowing Moon** using `box-shadow`.
- **Animated shadow** simulating the lunar eclipse.
- **Text overlay** for “BLOOD MOON” and the date.
- Uses only **built-in fonts** (`Courier New`) for a creepy effect.
- Beginner-friendly HTML and CSS.
  

## Usage

1. Copy the following HTML code into a `.html` file (e.g., `blood-moon.html`):

```html
<!DOCTYPE html>
<html>
<head>
  <title>Lunar Eclipse</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: black;
      position: relative;
    }

    .moon {
      width: 150px;
      height: 150px;
      background: lightgray;
      border-radius: 50%;
      position: relative;
      overflow: hidden;
      box-shadow: 0 0 30px 10px rgba(255, 255, 200, 0.5);
    }

    .shadow {
      width: 150px;
      height: 150px;
      background: black;
      border-radius: 50%;
      position: absolute;
      left: -150px;
      top: 0;
      animation: eclipse 10s infinite linear;
    }

    @keyframes eclipse {
      0% { left: -150px; }
      50% { left: 0; }
      100% { left: -150px; }
    }

    .text {
      position: absolute;
      top: 20px;
      left: 50%;
      transform: translateX(-50%);
      color: white;
      font-size: 24px;
      font-family: 'Courier New', Courier, monospace;
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="moon">
    <div class="shadow"></div>
  </div>

  <div class="text">
    BLOOD MOON<br>
    SEPTEMBER 7, 2025
  </div>
</body>
</html>
