<!DOCTYPE html>
<html>
<head>
<title>Simple Calculator</title>
<script type="text/javascript">
  // Function to add two numbers
  function add(x, y) {
    return x + y;
  }
  // Function to subtract two numbers
  function subtract(x, y) {
    return x - y;
  }
  // Function to multiply two numbers
  function multiply(x, y) {
    return x * y;
  }
  // Function to divide two numbers
  function divide(x, y) {
    if (y === 0) {
      return "Error! Division by zero.";
    } else {
      return x / y;
    }
  }

  // Function to perform the operation based on user choice
  function calculate() {
    var num1 = parseFloat(document.getElementById('num1').value);
    var num2 = parseFloat(document.getElementById('num2').value);
    var operation = document.getElementById('operation').value;
    var result;
	
    switch (operation) {
      case 'add':
        result = add(num1, num2);
        break;
      case 'subtract':
        result = subtract(num1, num2);
        break;
      case 'multiply':
        result = multiply(num1, num2);
        break;
      case 'divide':
        result = divide(num1, num2);
        break;
      default:
        result = "Invalid Operation";
    }

    document.getElementById('result').innerHTML = "Result: " + result;
  }
</script>
</head>
<body>
<h2>Simple Calculator</h2>
<label for="num1">Enter first number:</label>
<input type="number" id="num1"><br><br>
<label for="num2">Enter second number:</label>
<input type="number" id="num2"><br><br>
<label for="operation">Select operation:</label>
<select id="operation">
<option value="add">Addition</option>
<option value="subtract">Subtraction</option>
<option value="multiply">Multiplication</option>
<option value="divide">Division</option>
</select><br><br>
<button onclick="calculate()">Calculate</button><br><br>
<div id="result"></div>
</body>
</html>
