# Ex.05 Design a Website for Server Side Processing
## Date:

## AIM:
 To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side. 


## FORMULA:
P = I<sup>2</sup>R
<br> P --> Power (in watts)
<br> I --> Intensity
<br> R --> Resistance

## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Create python programs for views and urls to perform server side processing.

### Step 5:
Create a HTML file to implement form based input and output.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
math.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lamp Filament Power Calculator</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Lamp Filament Power Calculator</h1>
        <form id="power-form">
            <div class="input-group">
                <label for="intensity">Intensity (I in Amperes):</label>
                <input type="number" id="intensity" name="intensity" step="0.01" min="0" required>
            </div>
            <div class="input-group">
                <label for="resistance">Resistance (R in Ohms):</label>
                <input type="number" id="resistance" name="resistance" step="0.01" min="0" required>
            </div>
            <button type="submit">Calculate Power</button>
        </form>

        <div class="result" id="result">Enter values to calculate power.</div>
    </div>

    <script>
        document.getElementById('power-form').addEventListener('submit', function(event) {
            event.preventDefault();
            const intensity = parseFloat(document.getElementById('intensity').value);
            const resistance = parseFloat(document.getElementById('resistance').value);
            
            if (intensity >= 0 && resistance >= 0) {
                const power = Math.pow(intensity, 2) * resistance;
                document.getElementById('result').innerText = "Power: " + power.toFixed(2) + " Watts";
            } else {
                document.getElementById('result').innerText = "Please enter non-negative values.";
            }
        });
    </script>
</body>
</html>

```
math.css
```
/* Reset */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
}

/* Body Styling */
body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color: #e3f2fd;
}

/* Container Styling */
.container {
    width: 90%;
    max-width: 420px;
    padding: 25px;
    background-color: #fff;
    border-radius: 12px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
    text-align: center;
    animation: fadeIn 1s ease-in-out;
}

/* Title Styling */
h1 {
    font-size: 1.6em;
    color: #333;
    margin-bottom: 20px;
    border-bottom: 2px solid #90caf9;
    padding-bottom: 10px;
    font-weight: bold;
}

/* Input Group Styling */
.input-group {
    margin-bottom: 20px;
    text-align: left;
}

/* Label Styling */
label {
    font-size: 1em;
    color: #555;
    display: inline-block;
    margin-bottom: 5px;
    font-weight: bold;
}

/* Input Styling */
input[type="number"] {
    width: 100%;
    padding: 10px;
    border: 2px solid #cfd8dc;
    border-radius: 8px;
    font-size: 1em;
    background-color: #f7f9fc;
    color: #333;
    transition: border-color 0.3s;
}

input[type="number"]:focus {
    border-color: #64b5f6;
    outline: none;
    background-color: #ffffff;
}

/* Button Styling */
button {
    width: 100%;
    padding: 12px;
    font-size: 1.1em;
    color: #fff;
    background-color: #1e88e5;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #1565c0;
}

/* Result Box Styling */
.result {
    margin-top: 25px;
    padding: 15px;
    background-color: #e3f2fd;
    color: #1a237e;
    font-size: 1.2em;
    border: 1px solid #bbdefb;
    border-radius: 8px;
    font-weight: bold;
}

/* Animation for Container */
@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(-10px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

```

## HOMEPAGE:

![alt text](<2025-05-13 (1).png>)

## RESULT:
The program for performing server side processing is completed successfully.
