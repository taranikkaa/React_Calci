# Ex04 Simple Calculator - React Project
## Date: 28-03-2025
## Name: TARANIKKA A
## Reg no:212223220115

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
```
### calculator.js:
import React, { useState } from 'react';
import './index.css';

const Calculator = () => {
  const [input, setInput] = useState('');

  const handleClick = (value) => {
    setInput((prev) => prev + value);
  };

  const calculate = () => {
    try {
      // eslint-disable-next-line no-eval
      setInput(eval(input).toString());
    } catch {
      setInput('Error');
    }
  };

  const clear = () => {
    setInput('');
  };

  return (
    <div className="calculator">
      <h2>Simple Calculator</h2>
      <input type="text" value={input} readOnly />
      <div className="buttons">
        {'1234567890+-*/.'.split('').map((char) => (
          <button key={char} onClick={() => handleClick(char)}>{char}</button>
        ))}
        <button onClick={calculate}>=</button>
        <button onClick={clear}>C</button>
      </div>
      <footer>
        <p>Designed by TARANIKKA A| Reg No: 212223220115</p>
      </footer>
    </div>
  );
};

export default Calculator;
```
```
## app.js:

import React from 'react';
import Calculator from './Calculator';

function App() {
  return (
    <div className="App">
      <Calculator />
    </div>
  );
}

export default App;
```
```
## index.css:
body {
  font-family: Arial, sans-serif;
  background-color: #fafafa;
  text-align: center;
}

.calculator {
  background: rgb(251, 140, 140);
  padding: 20px;
  margin: 50px auto;
  border-radius: 12px;
  max-width: 300px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

input {
  width: 100%;
  padding: 10px;
  font-size: 1.2rem;
  margin-bottom: 10px;
}

.buttons button {
  width: 60px;
  height: 40px;
  margin: 5px;
  font-size: 1.1rem;
  border: none;
  background: #333;
  color: white;
  border-radius: 5px;
}

footer {
  margin-top: 20px;
  font-size: 0.9rem;
  color: gray;
}
```

## OUTPUT

![image](https://github.com/user-attachments/assets/852de647-9d8f-4949-a0d9-f08e57e052df)


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
