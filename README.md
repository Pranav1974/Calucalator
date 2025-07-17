# Calucalator
It's a basic calculator that performs operations like addition, subtraction, and more. I built it using HTML, CSS, and JavaScript as a simple web page.


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" href="outline_calculate_white_36dp.png" type="image/icon type">
    <title>Calculator</title>
    
    <link rel="stylesheet" href="style.css">
</head>
<script>
    function insertOpenBracket() {
        const display = document.forms[0].elements['display'];
        const lastChar = display.value.slice(-1);
        if (/\d|\)/.test(lastChar)) {
            display.value += '*(';
        } else {
            display.value += '(';
        }
    }

    function insertCloseBracket() {
        const display = document.forms[0].elements['display'];
        display.value += ')';
    }
</script>


    
<body>
    <div class="container">
        <div class="calculator">
            <form>
            <div class="display">
                <input type="text" name="display">
            </div>
            <div>
                <input type="button" value="AC" onclick="display.value='' ">
                <input type="button" value="DE" onclick="display.value=display.value.toString().slice(0,-1)">
                <input type="button" value="." onclick="display.value+='.'">
                <input type="button" value="/" onclick="display.value+='/'">
            </div>
            <div>
                <input type="button" value="7" onclick="display.value+='7'">
                <input type="button" value="8" onclick="display.value+='8'">
                <input type="button" value="9" onclick="display.value+='9'">
                <input type="button" value="*" onclick="display.value+='*'">
            </div>
            <div>
                <input type="button" value="4" onclick="display.value+='4'">
                <input type="button" value="5" onclick="display.value+='5'">
                <input type="button" value="6" onclick="display.value+='6'">
                <input type="button" value="+" onclick="display.value+='+'">
            </div>
            <div>
                <input type="button" value="1" onclick="display.value+='1'">
                <input type="button" value="2" onclick="display.value+='2'">
                <input type="button" value="3" onclick="display.value+='3'">
                <input type="button" value="-" onclick="display.value+='-'">
            </div>
            <div>
                <input type="button" value="(" onclick="insertOpenBracket()">
<input type="button" value=")" onclick="insertCloseBracket()">


                <input type="button" value="0"  onclick="display.value+='0'">
                <input type="button" value="=" onclick="display.value = eval(display.value)">

            </div>
            </form>
        </div>
    </div>
  
    <p class="footer-text">DESIGN BY MYLAVARAM PRANAV</p>


      

</body>
  #CSS code
* {
    margin: 0;
    padding: 0;
    font-family: 'Poppins', sans-serif;
    box-sizing: border-box;
}

.container {
    width: 100%;
    height: 100vh;
    background-color: #95aa63; /* Leaf green */
    display: flex;
    align-items: center;
    justify-content: center;
}

.calculator {
    background-color: #6F9580;
    padding: 25px;
    border-radius: 20px;
    box-shadow: -6px -6px 10px rgba(81, 40, 31, 0.2), 
                 6px 6px 10px rgba(0, 0, 0, 0.3);
}

form .display {
    display: flex;
    justify-content: flex-end;
    margin-bottom: 15px;
}

form .display input {
    text-align: right;
    flex: 1;
    font-size: 40px;
    padding: 15px;
    border-radius: 10px;
    border: none;
    background: #f8f8f8;
    box-shadow: inset 3px 3px 8px rgba(0, 0, 0, 0.1);
    outline: none;
}

.calculator form input {
    border: none;
    outline: none;
    width: 65px;
    height: 65px;
    border-radius: 12px;
    font-size: 25px;
    cursor: pointer;
    margin: 6px;
    background: #ddd;
    box-shadow: 3px 3px 8px rgba(0, 0, 0, 0.2);
    transition: 0.2s ease-in-out;
}

/* Button hover effect */
.calculator form input:hover {
    background: #bbb;
    box-shadow: 1px 1px 5px rgba(0, 0, 0, 0.3);
}

/* Special buttons */
.calculator form input[value="AC"],
.calculator form input[value="DE"] {
    background: #ff6b6b;
    color: white;
}

.calculator form input[value="AC"]:hover,
.calculator form input[value="DE"]:hover {
    background: #ff4c4c;
}

/* Operator buttons */
.calculator form input[value="+"],
.calculator form input[value="-"],
.calculator form input[value="*"],
.calculator form input[value="/"],
.calculator form input[value="="] {
    background: #ffbd69;
    color: white;
}

.calculator form input[value="+"]:hover,
.calculator form input[value="-"]:hover,
.calculator form input[value="*"]:hover,
.calculator form input[value="/"]:hover,
.calculator form input[value="="]:hover {
    background: #ff9f45;
}
.calculator-img {
    width: 80px; 
    height: auto;
    margin-bottom: 15px;
}
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.footer-text {
    background-color: #95aa63;
    text-align: center;
    margin: 0;
    padding: 10px 0;
    font-weight: bold;
    font-size: 25px;
    color: #333;
    font-family: 'Pacifico', cursive;
}
