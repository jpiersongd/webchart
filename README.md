# webchart
web based charting tool


**Project Overview: Mathematical Function Sound Visualization**

**Objective:** 
To visualize and audibly represent mathematical functions in a browser-based application. The user inputs a mathematical formula, which is then plotted on a chart and simultaneously played as sound based on the y-values (mapped as frequencies). Additionally, the system provides an estimation of the frequency based on peaks in the formula.

**Key Components:**

1. **User Input**: 
   - Mathematical formula input via a text box (`functionInput`).
   - Dropdown with pre-defined mathematical formulas.
   - A, B, and C knobs which can be used to adjust formula parameters.
   - Frequency estimation displayed in the `formulaDescription` text box.

2. **Visualization**:
   - Chart plotting the mathematical function.
   - A vertical scrolling bar indicating the current position of the sound being played.

3. **Sound Representation**:
   - Mathematical functions are translated into sound using the Web Audio API.
   - The y-values of the function are used to determine the frequency of the sound.
   - Limitations are set to ensure frequencies remain within human hearing range (clamped between -1 and 1).
   - A base tone can be modulated based on the y-values for certain non-sinusoidal functions.

4. **Frequency Estimation**:
   - The average distance between peaks in the y-values is used to estimate the frequency of the function.
   - Results are displayed in the `formulaDescription` text box.

5. **Error Handling**:
   - Try-catch blocks are used to handle potential errors, especially for out-of-bounds frequencies and invalid mathematical functions.

---

**Code Highlights**:

- Mathematical function parsing using JavaScript's `Function` constructor.
- Use of the Web Audio API to create and manipulate sounds in the browser.
- Frequency clamping to ensure generated sounds are within safe and audible ranges.
- An algorithm to estimate function frequency based on peaks and troughs in the y-values.
- UI feedback via a scrolling vertical bar on the chart to indicate sound playback position.

---

