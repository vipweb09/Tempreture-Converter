# Tempreture-Converter
This is the web code to convert the ten+mpreture from one unit to another unit.
<!--
  level 1 task 3 
  it is the tenpreture converter page  
-->
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
  body {
    font-family: Arial, sans-serif;
    background-color: #bdeff0;
    text-align: center;
    margin: 0;
    padding: 0;
  }
  #container {
    max-width: 400px;
    margin: 100px auto;
    background-color: #fff;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
  }
  h1 {
    margin-top: 0;
  }
  input[type="number"] {
    width: 100%;
    padding: 10px;
    margin: 5px 0;
    box-sizing: border-box;
  }
  select {
    width: 100%;
    padding: 10px;
    margin: 5px 0;
    box-sizing: border-box;
  }
  button {
    background-color: #3abe22;
    color: rgb(124, 75, 151);
    border: none;
    padding: 10px 20px;
    cursor: pointer;
  }
</style>
<title>Temperature Converter</title>
</head>
<body>
  <div id="container">
    <h1>Temperature Converter</h1>
    <input type="number" id="inputTemp" placeholder="Enter temperature">
    <select id="inputUnit">
      <option value="celsius">Celsius</option>
      <option value="fahrenheit">Fahrenheit</option>
      <option value="kelvin">Kelvin</option>
    </select>
    <button id="convertButton">Convert</button>
    <h2>Result: <span id="outputTemp"></span></h2>
  </div>

  <script>
    const convertButton = document.getElementById("convertButton");
    const inputTemp = document.getElementById("inputTemp");
    const inputUnit = document.getElementById("inputUnit");
    const outputTemp = document.getElementById("outputTemp");

    convertButton.addEventListener("click", () => {
      const temperature = parseFloat(inputTemp.value);
      const unit = inputUnit.value;

      if (unit === "celsius") {
        outputTemp.textContent = `${temperature + 273.15} Kelvin / ${temperature * 9/5 + 32} Fahrenheit`;
      } else if (unit === "fahrenheit") {
        outputTemp.textContent = `${(temperature - 32) * 5/9 + 273.15} Kelvin / ${(temperature - 32) * 5/9} Celsius`;
      } else if (unit === "kelvin") {
        outputTemp.textContent = `${temperature - 273.15} Celsius / ${(temperature - 273.15) * 9/5 + 32} Fahrenheit`;
      }
    });
  </script>
</body>
</html>
