## Name: PRAVEENA M
## Reg No: 212223040153

# Ex04 Simple Calculator - React Project
## Date:

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM

## App.jsx

```
import React, { useState } from "react";
import "./Modern.css"; // Import the CSS

const Calculator = () => {
  const [expression, setExpression] = useState("");
  const [result, setResult] = useState("");

  const handleClick = (value) => {
    if (value === "C") {
      setExpression("");
      setResult("");
    } else if (value === "←") {
      setExpression(expression.slice(0, -1));
    } else if (value === "=") {
      try {
        const res = new Function("return " + expression)();
        setResult(res);
      } catch {
        setResult("Error");
      }
    } else {
      setExpression(expression + value);
    }
  };

  const buttons = [
    "7", "8", "9", "/",
    "4", "5", "6", "*",
    "1", "2", "3", "-",
    "0", ".", "=", "+",
    "C", "←"
  ];

  return (
    <div className="calculator-wrapper">
      <div className="calculator">
        <h2>React Calculator</h2>
        <div className="display">
          <div>{expression || "0"}</div>
          <div className="result">{result !== "" ? "= " + result : ""}</div>
        </div>
        <div className="buttons">
          {buttons.map((btn) => (
            <button key={btn} onClick={() => handleClick(btn)}>
              {btn}
            </button>
          ))}
        </div>
        <footer className="footer">
        <p>Developed by: Praveena M</p>
        <p>Register Number: 212223040153</p>
      </footer>
      </div>
    </div>
    
  );
};

export default Calculator;








```
## App.css
```
/* Centering the calculator */
.calculator-wrapper {
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #eac2c2;
      border-width: 5px;
    }
    
    /* Calculator container */
    .calculator {
      max-width: 100%;
      
      padding: 20px;
      border-radius: 10px;
      background-color: #9c89f3;
      box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
      font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
      text-align: center;
      color: #050505;
      border-radius: 15px;
      border-color: #050505;
      border-width: 5px;
      border-color: #050505;
    }
    
    /* Display area */
    .display {
      border: 1px solid #070707;
      background: #2687b4;
      padding: 10px;
      min-height: 50px;
      margin-bottom: 10px;
      text-align: right;
      font-size: 18px;
      color: #050505;
      border-radius: 15px;
      border-width: 3px;
    }
    
    /* Result area */
    .result {
      font-weight: bold;
      font-size: 20px;
      color: #050505;
      border-color: #050505;
    }
    
    /* Grid buttons */
    .buttons {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 10px;
      color: #050505;
      border-width: 5px;
      border-color: #050505;
    }
    
    /* Button styles */
    .buttons button {
      padding: 15px;
      font-size: 18px;
      border: none;
      border-radius: 5px ;
      background: #3ac7b9;
      cursor: pointer;
      transition: background 0.2s ease;
      color: #050505;
      border-width: 10px;
      border-color: #050505;
    }
    
    .buttons button:hover {
      background: #dce8f4;
    }



























```

## OUTPUT

![image](https://github.com/user-attachments/assets/2b846896-ed73-4354-a16d-839c43d42e03)

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
