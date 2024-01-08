# Simple-Calculator

```javascript
 let display = document.getElementById('display');

        function appendInput(value) {
            display.value += value;
        }

        function clearDisplay() {
            display.value = '';
        }

        function calculate() {
            try {
                display.value = eval(display.value);
            } catch (error) {
                display.value = 'Error';
            }
        }
```

1. **`let display = document.getElementById('display');`**:
   - This line declares a variable named `display` using the `let` keyword.
   - It uses `document.getElementById('display')` to select the HTML element with the ID "display." This element is assumed to be an input field, as it is later manipulated as a text input.

2. **`function appendInput(value) { display.value += value; }`**:
   - This is a function named `appendInput` that takes a parameter `value`.
   - When this function is called, it appends the provided `value` to the existing value of the `display` input field. Essentially, it is used to add characters (numbers, operators, etc.) to the display.

3. **`function clearDisplay() { display.value = ''; }`**:
   - This is a function named `clearDisplay`.
   - When called, it sets the `value` of the `display` input field to an empty string (`''`). This function is used to clear the contents of the display.

4. **`function calculate() { try { display.value = eval(display.value); } catch (error) { display.value = 'Error'; } }`**:
   - This is a function named `calculate`.
   - It attempts to evaluate the mathematical expression entered in the `display` input field using `eval(display.value)`.
   - If the evaluation is successful, the result is assigned to the `value` property of the `display` input field, updating the display with the calculated result.
   - If an error occurs during evaluation (e.g., due to an invalid expression), the `catch` block is executed. In this case, it sets the `value` of the `display` input field to the string 'Error', indicating that there was an issue with the calculation.

This JavaScript code defines the behavior of a simple calculator. The `appendInput` function is used to input values, the `clearDisplay` function resets the display, and the `calculate` function evaluates the expression and updates the display with the result or an error message.
