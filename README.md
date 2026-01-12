# Sigma Summation Calculator (MIT App Inventor)

A mathematical utility app built with MIT App Inventor that calculates the **Summation ($\sum$)** of a specific function over a defined range. This app evaluates mathematical expressions dynamically and displays both the step-by-step expansion and the final result.

## 🚀 Features

* **Dynamic Function Evaluation:** Input any mathematical function (in terms of variable `n`) and calculate its value.
* **Custom Ranges:** Set specific **Lower** and **Upper** limits for the summation loop.
* **Step-by-Step Visualization:** Displays the expanded series (e.g., `1 + 4 + 9...`) so users can verify the calculation.
* **Real-time Calculation:** Instantly computes the running sum upon button click.

## 🛠️ Dependencies & Extensions

This project requires the **TaifunMath** extension to evaluate string-based mathematical expressions.

* **Extension Name:** `com.puravidaapps.TaifunMath`
* **Location:** You can find the `.aix` file in this repository (e.g., in the `extensions/` folder or root directory).
* **Credit:** [Pura Vida Apps - TaifunMath](https://puravidaapps.com/math.php)

> **Note:** If you are importing this project (.aia) into MIT App Inventor, ensure the extension is loaded correctly in the Designer view.

## 📖 How to Use

1.  **Function Input (`TextBox1`):** Enter your mathematical formula using the variable `n`.
    * *Example:* `n^2` or `2*n + 1`
2.  **Upper Limit (`TextBox2`):** Enter the ending number for the loop.
3.  **Lower Limit (`TextBox3`):** Enter the starting number for the loop.
4.  **Calculate:** Press **Button1**.
5.  **Results:**
    * **TextBox4:** Shows the expansion series text.
    * **TextBox5:** Shows the final calculated sum.

## 🧩 How It Works (Blocks Logic)

The core logic handles the summation loop as follows:

1.  **Initialization:**
    * Global variables are reset (Sum = 0, Steps = Empty).
    * Inputs are read from the TextBoxes.
2.  **The Loop (`For Each`):**
    * The app iterates from the `globalLower` limit to the `globalUpper` limit.
    * **Substitution:** Inside the loop, the app takes the user's function string and replaces the character `"n"` with the current loop number (`i`).
    * **Evaluation:** The `TaifunMath.Expression` block calculates the numerical value of that specific iteration.
3.  **Accumulation:**
    * The result is added to `globalRunningSum`.
    * The result is also appended to `globalStepstext` to create the visual string (handling " + " formatting between numbers).
4.  **Output:** Finally, the text and total sum are displayed to the user.

## 📥 Installation

1.  Download the `.aia` source file from this repository.
2.  Go to [MIT App Inventor](http://ai2.appinventor.mit.edu/).
3.  Click **Projects** > **Import project (.aia) from my computer**.
4.  Select the file and let it load.
5.  Ensure the `TaifunMath` extension is present in the bottom of the component palette.

## 📄 License

This project (the Blocks logic and source code) is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

**Third-Party Credits:**
* **TaifunMath Extension:** Copyright © Pura Vida Apps. Used under fair use/permission for functionality. (See: [puravidaapps.com](https://puravidaapps.com))
