# MWAD-EXP_04-Simple-caluculator
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
App.jsx
```
import { useState } from 'react';

function App() {
  const [input, setInput] = useState('');

  const handleClick = (value) => {
    setInput((prev) => prev + value);
  };

  const handleClear = () => {
    setInput('');
  };

  const handleEqual = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput('Error');
    }
  };

  return (
    <div className="calculator">
      <h1>Calculator</h1> {/* ✅ Heading on the page */}
      <input type="text" value={input} readOnly />
      <div className="buttons">
        <button onClick={handleClear}>C</button>
        <button onClick={() => handleClick('/')}>/</button>
        <button onClick={() => handleClick('*')}>*</button>
        <button onClick={() => handleClick('-')}>-</button>

        <button onClick={() => handleClick('7')}>7</button>
        <button onClick={() => handleClick('8')}>8</button>
        <button onClick={() => handleClick('9')}>9</button>
        <button onClick={() => handleClick('+')}>+</button>

        <button onClick={() => handleClick('4')}>4</button>
        <button onClick={() => handleClick('5')}>5</button>
        <button onClick={() => handleClick('6')}>6</button>
        <button onClick={handleEqual}>=</button>

        <button onClick={() => handleClick('1')}>1</button>
        <button onClick={() => handleClick('2')}>2</button>
        <button onClick={() => handleClick('3')}>3</button>
        <div></div>

        <button className="zero" onClick={() => handleClick('0')}>0</button>
        <button onClick={() => handleClick('.')}>.</button>
      </div>
    </div>
  );
}

export default App;
```
App.css
```
/* Calculator Styling */
.calculator {
  max-width: 320px;
  margin: 60px auto;
  background: #f9f9f9;
  padding: 30px;
  border-radius: 15px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  text-align: center;
  font-family: 'Segoe UI', sans-serif;
}

h1 {
  margin-bottom: 20px;
  color: #333;
}

input {
  width: 100%;
  height: 40px;
  font-size: 20px;
  padding: 5px;
  margin-bottom: 20px;
  text-align: right;
  border: 1px solid #ccc;
  border-radius: 8px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 15px;
  font-size: 18px;
  border: none;
  border-radius: 8px;
  background-color: #4caf50;
  color: white;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #388e3c;
}

button.zero {
  grid-column: span 2;
}

```


## OUTPUT
![image](https://github.com/user-attachments/assets/2a3ebc99-703a-4d01-b1e4-9480558cc870)



## RESULT
The program for developing a simple calculator in React.js is executed successfully.
