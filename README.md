# ICS-QUADRATIC-GRADER-MUKANDO-HAMWENDA 

Introduction
------------
I developed this lightweight, single-file web application to provide two practical utilities useful in educational and small-scale computational contexts: a quadratic equation solver (for equations of the form ax² + bx + c = 0) and a numeric-to-letter grade calculator. The application is self-contained (HTML, CSS and JavaScript in one file), responsive, and designed to be clear and easily customizable.

Quick start
-----------
1. Obtain the project files and open `index.html` in a modern web browser:
   - Double-click `index.html` or serve the directory with any static file server.
2. Use the interface:
   - Quadratic Solver: supply coefficients a, b, and c (a must be non-zero) and select "Solve Equation".
   - Grade Calculator: supply an integer score between 0 and 100 and select "Calculate Grade".

Features
--------
- Quadratic solver:
  - Input validation ensuring numeric inputs and nonzero coefficient a.
  - Computation of the discriminant and classification of root nature:
    - Two distinct real roots (D > 0)
    - One real repeated root (D = 0)
    - Two complex conjugate roots (D < 0)
  - Outputs are formatted to four decimal places for readability.
- Grade calculator:
  - Accepts integer scores between 0 and 100.
  - Uses a fixed grading scale to map scores to letter grades (A+, A, B+, B, C+, C, D).
  - Provides concise textual feedback corresponding to each grade.
- User interface:
  - Responsive layout suitable for desktop and mobile.
  - Inline validation messages and distinct result panels for success and error states.
  - No external dependencies or build steps.

File structure
--------------
- `index.html` — complete application containing:
  - Inline CSS for styling.
  - Inline JavaScript containing functions:
    - solveQuadratic()
    - resetQuadratic()
    - calculateGrade()
    - resetGrade()
    - helper functions for validation and display.

Usage examples
--------------
- Quadratic:
  - a = 1, b = -3, c = 2 → D = 1 → roots: x₁ = 2.0000, x₂ = 1.0000
  - a = 1, b = 2, c = 1 → D = 0 → root: x = -1.0000
  - a = 1, b = 0, c = 1 → D < 0 → roots: x = 0.0000 ± 1.0000i
- Grade:
  - 92 → A+
  - 78 → A
  - 67 → B+
  - 58 → C+
  - 45 → D

Customization
-------------
I structured the application for straightforward modification:
- Grade thresholds: edit the conditional logic in `calculateGrade()` to change ranges or labels.
- Precision: adjust the `toFixed(4)` calls in the quadratic solver to change numeric precision.
- Styling: modify the embedded CSS in `index.html` to apply a different visual theme.
- Input handling: remove the integer-only restriction on scores if fractional scores should be accepted.

Browser compatibility
---------------------
The application uses standard, contemporary HTML, CSS, and JavaScript and is compatible with modern evergreen browsers (Chrome, Firefox, Edge, Safari). It does not require transpilation or a build pipeline.

Limitations
-----------
- The grade calculator currently enforces integer-only scores; fractional scores require a minor code change.
- The project is intended as a compact utility or demonstration and does not include persistence, user accounts, or server-side components.
- Accessibility is reasonable (clear labels and visible validation); further improvements (ARIA roles, aria-live regions, and enhanced keyboard focus management) are advisable for full accessibility compliance.

Accessibility considerations
----------------------------
- Controls include explicit labels and visible error messages.
- If required, I can add ARIA attributes and live regions to announce results to assistive technologies and further refine keyboard navigation behavior.

Development and contribution
----------------------------
If you would like to extend the project, recommended next steps include:
- Extracting CSS and JavaScript into separate files for modular development.
- Adding unit tests for the numerical logic (discriminant handling, complex root formatting, grade boundary tests).
- Introducing a small build/dev workflow if you plan to expand functionality or integrate packages.

Contact
-------
If you require modifications, feature additions (for example, support for decimal grades, CSV export, or conversion to a reusable component), or assistance with accessibility improvements, I will implement the requested change thank you.
