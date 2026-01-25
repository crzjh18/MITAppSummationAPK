# Sigma Summation Calculator

**A Mathematical Utility Built with MIT App Inventor**

This project is a mathematical utility application designed to calculate the **Summation ($\sum$)** of a user-defined function over a specific range. It evaluates mathematical expressions dynamically, providing both the final calculated result and a step-by-step expansion of the series for verification purposes.

## Key Features

* **Dynamic Function Evaluation:** Users can input any mathematical function using the variable `n` (e.g., `n^2`, `2*n + 1`) and the app will interpret and solve it dynamically.
* **Custom Loop Limits:** Allows for the definition of specific **Lower** and **Upper** bounds for the summation loop.
* **Series Visualization:** Generates a text-based expansion of the series (e.g., `1 + 4 + 9...`), allowing users to verify the logic behind the calculation.
* **Real-time Computation:** Instantly computes the running sum and updates the display upon execution.

## Dependencies

This project relies on a specific extension to handle string-based mathematical evaluation. This extension must be loaded for the logic to function.

* **Extension:** TaifunMath
* **Package Name:** `com.puravidaapps.TaifunMath`
* **Function:** Parses and evaluates the string input from the text box as a mathematical expression.
* **Source:** [Pura Vida Apps](https://puravidaapps.com/math.php)

> **Important:** If importing the source `.aia` file, verify that the TaifunMath extension is correctly loaded in the "Extensions" palette at the bottom of the Designer view.

## Algorithm and Block Logic

The core functionality is built upon a standard accumulation loop algorithm implemented via MIT App Inventor blocks:

1.  **Initialization:**
    * Global variables for `Sum` (0) and `Steps` (Empty string) are reset.
    * User inputs are captured from the UI components.
2.  **Iterative Loop:**
    * A `For Each` loop initiates, running from the defined `Lower Limit` to the `Upper Limit`.
3.  **Substitution & Evaluation:**
    * **Substitute:** Within each iteration, the algorithm takes the user's function string and replaces the variable character `"n"` with the current loop index `i`.
    * **Evaluate:** The `TaifunMath.Expression` block takes this modified string and calculates its numerical value.
4.  **Accumulation:**
    * The calculated value is added to the `globalRunningSum`.
    * The value is appended to the `globalStepstext` variable to build the visualization string.
5.  **Output:**
    * The final expansion string and the total sum are rendered to the user interface.

## How to Use

1.  **Function Input:** Enter the mathematical formula in the first text box using the variable `n`.
2.  **Define Range:** Enter the starting number (Lower Limit) and ending number (Upper Limit) in their respective fields.
3.  **Execute:** Press the **Calculate** button.
4.  **Review:**
    * View the expansion series in the "Steps" display.
    * View the final total in the "Result" display.

## Installation

1.  Download the `.aia` source file from this repository.
2.  Navigate to [MIT App Inventor](http://ai2.appinventor.mit.edu/).
3.  Select **Projects** > **Import project (.aia) from my computer**.
4.  Upload the file to load the blocks and designer view.

## License and Credits

This project source code is licensed under the **MIT License**.

**Third-Party Credits:**
* **TaifunMath Extension:** Copyright © Pura Vida Apps. Used under fair use for educational and functional purposes.
