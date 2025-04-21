# Digital Piano - README

## Overview

This C++ program simulates a digital piano with two different visual styles: Classic and Ovule. It utilizes the graphics library in Turbo C++ to create a graphical interface where users can play the piano using their keyboard.  The program also includes options for saving user input and accessing help and about sections.

## Features

-   **Two Piano Styles:** Choose between a Classic piano interface and an Ovule piano interface with animated visuals.
-   **Keyboard Input:** Play the piano by pressing keys '1' through '9' and '0' to produce different notes.
-   **Sound Generation:** Generates sound corresponding to the pressed keys using the `sound()` function.
-   **Adjustable Tone:** Change the tone of the piano using the 'A', 'B', and 'C' keys.
-   **Help Section:** Provides instructions on how to use the piano.
-   **About Section:** Displays information about the developers and the program.
-   **Saving Feature:** Allows users to save their "performance" (key presses) to a file.
-   **Loading Animation:** Includes a loading screen with a percentage indicator.
-   **Mouse Interface:** Implements mouse functionality for certain interactive elements like data entry and button clicks.

## Compilation and Execution

### Prerequisites

-   Turbo C++ compiler
-   DOSBox (if running on a modern operating system)

### Steps

1.  **Install Turbo C++:** If you don't have it already, install the Turbo C++ compiler.

2.  **Set up DOSBox (if necessary):** If you are using a modern operating system, you will likely need to use DOSBox to run the program.  Install DOSBox and mount the directory containing the Turbo C++ files.

3.  **Copy the code:** Save the provided code as a `.cpp` file (e.g., `piano.cpp`).

4.  **Compile the code:** Open the Turbo C++ IDE and compile the `piano.cpp` file. Make sure that the BGI (Borland Graphics Interface) files are properly linked. This usually involves ensuring that the `BGI` directory is in the compiler's include path.

5.  **Run the executable:**  After successful compilation, run the executable file (e.g., `piano.exe`).

## Controls

### Main Menu

-   **W/S:** Move up or down to select options.
-   **E:** Enter the selected option.

### Classic and Ovule Piano

-   **1-9, 0:** Play the corresponding notes on the piano.
-   **A, B, C:** Change the tone/octave of the piano.
-   **Z:** Return to the main menu.
-   **H:** Access the help screen.
-   **S:** Save the current performance.
-   **X:** Exit the program.

### Additional Controls

-   In data entry screens, mouse clicks are used on the virtual keyboard for entering names.

## File Structure

The program interacts with the following files:

-   `name.txt`:  Saves the user's name entered during registration.
-   `save.dat`:  Saves the piano performance data (key presses).

## Code Structure

The code is organized into several functions and a `Main` class:

-   **`Main` Class:**  Handles the piano playing logic and stores the state of the piano.

    -   `piano()`: Implements the classic piano interface and functionality.
    -   `opiano()`: Implements the ovule piano interface and functionality.
-   **Graphics Functions:**
    -   `frame()`: Draws the border frame.
    -   `registration()`: Creates the registration screen.
    -   `About()`: Displays the about section.
    -   `help()`: Displays the help section.
    -   `classic()`: Draws the classic piano keys.
-   **Sound Functions:**
    -   `soundo()`: Generates a sequence of sounds for the startup screen.
-   **Menu Functions:**
    -   `menup()`: Displays the main menu.
-   **Utility Functions:**
    -   `loading()`: Displays the loading animation.
    -   `enter()`: Manages user name input.
    -   `shift()`: Manages main menu options.
    -   `thank()`: displays the thank you screen
-   **Mouse Functions:**
    -   `showmouse()`: Displays the mouse cursor.
    -   `getmousepos()`: Gets the mouse position.

## Notes

-   This program is designed for the Turbo C++ environment and may require adjustments to run in other environments.
-   The graphics and sound functions are specific to the Borland Graphics Interface (BGI) and may not be directly compatible with modern graphics libraries.
-   The program uses DOS-specific functions like `int86()` for mouse interaction, which may need to be adapted for other platforms.
