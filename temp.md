<!DOCTYPE html>
<html>
<head>
  <title>Cash Calculator</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

    <div class="container">
        <h1>Cash Calculator</h1>
        <div class="row">
          <img src="images/two_thousand_note.png"></img>
          <input type="number" id="et2000" class="cash-input" placeholder="Enter No. of Rs.2000 Notes">
          <span id="txt2000" class="cash-text">0</span>
        </div>
        <div class="row">
          <img src="images/five_hundred_note.png"></img>
          <input type="number" id="et500" class="cash-input" placeholder="Enter No. of Rs.500 Notes">
          <span id="txt500" class="cash-text">0</span>
        </div>
        <div class="row">
          <img src="images/two_hundred_note.png"></img>
          <input type="number" id="et200" class="cash-input" placeholder="Enter No. of Rs.200 Notes">
          <span id="txt200" class="cash-text">0</span>
        </div>

        <div class="row">
          <img src="images/one_hundred.png"></img>
          <input type="number" id="et100" class="cash-input" placeholder="Enter No. of Rs.100 Notes">
          <span id="txt100" class="cash-text">0</span>
        </div>


        <div class="row">
          <img src="images/fifty_note.png"></img>
          <input type="number" id="et50" class="cash-input" placeholder="Enter No. of Rs.50 Notes">
          <span id="txt50" class="cash-text">0</span>
        </div>

        <div class="row">
          <img src="images/twenty_note.png"></img>
          <input type="number" id="et20" class="cash-input" placeholder="Enter No. of Rs.20 Notes">
          <span id="txt20" class="cash-text">0</span>
        </div>


        <div class="row">
          <img src="images/ten_note.png"></img>
          <input type="number" id="et10" class="cash-input" placeholder="Enter No. of Rs.10 Notes">
          <span id="txt10" class="cash-text">0</span>
        </div>

        <div class="row">
          <img src="images/five_note.png"></img>
          <input type="number" id="et5" class="cash-input" placeholder="Enter No. of Rs.5 Notes">
          <span id="txt5" class="cash-text">0</span>
        </div>

        <div class="row">
          <img src="images/two_note.png"></img>
          <input type="number" id="et2" class="cash-input" placeholder="Enter No. of Rs.2 Notes">
          <span id="txt2" class="cash-text">0</span>
        </div>

        <div class="row">
          <img src="images/one_note.png"></img>
          <input type="number" id="et1" class="cash-input" placeholder="Enter No. of Rs.1 Notes">
          <span id="txt1" class="cash-text">0</span>
        </div>

        <div class="row">
          <button id="btnReset">Reset</button>
        </div>

        <div class="row result-part">
          <span id="txtFinalCash">Total Cash: 0</span>
          <span id="txtFinalCashInWords">Zero</span>
        </div>
    </div>
  
  <script src="script.js"></script>
</body>
</html>
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css');

body {
  margin: 0;
  padding: 0;
  background: linear-gradient(to right,  #593bc4,#c9a31b);
  font-family: Arial, sans-serif;
  color: #333;
}

.container {
  max-width: 600px;
  margin: 50px auto;
  padding: 20px 5px;
  background: linear-gradient(to right, #c9a31b, #593bc4);
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  animation: fadeIn 1s ease;
  display: flex;
  flex-direction: column;
  align-items: center;
  box-shadow: 2px 6px 10px rgba(0, 0, 0, 0.5);;
}

header {
  text-align: center;
  margin-bottom: 20px;
}

h1 {
  color: #ffffff;
}

.row{
  margin-top: 10px;
  display: flex;
  justify-content: center;
  align-items: center;

}

img {
  margin-right: 10px;
}

input[type="number"] {
  padding: 10px;
  font-size: 15px;
  width: 250px;
  border-radius: 4px;
  border: 1px solid #ccc;
  flex: 1;
  transition: border-color 0.3s ease;
  background-color: #fff;
  color: #333;
  font-weight: 600;
  
}

input[type="number"]:focus {
  border-color: #ff7e5f;
  outline: none;
  box-shadow: 0 0 0 2px #ff7e5f;
}

input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

input[type="number"]::-moz-inner-spin-button,
input[type="number"]::-moz-outer-spin-button {
  -moz-appearance: none;
  margin: 0;
}

input[type="number"]::-ms-clear {
  display: none;
}

input[type="number"]::-webkit-contacts-auto-fill-button {
  visibility: hidden;
  display: none !important;
  pointer-events: none;
  position: absolute;
  right: 0;
}

.cash-text {
  font-weight: bold;
  margin-left: 10px;
  width: 40px; /* Adjust the width as needed */
  display: inline-block;
  text-align: center;
  color: white;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  background-color: #ff7e5f;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
  align-self: flex-end;
}


button:hover {
  background-color: #ff6c4a;
}

#txtFinalCash {
  font-size: 18px;
  font-weight: bold;
  margin-top: 20px;
  color: #ffffff;
}

.result-part{
  display: flex;
  flex-direction: column;
}

#txtFinalCashInWords {
  margin-top: 10px;
  font-style: italic;
  color: #d4d0d0;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
    transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

document.addEventListener('DOMContentLoaded', () => {
    const et2000 = document.getElementById('et2000');
    const et500 = document.getElementById('et500');
    const et200 = document.getElementById('et200');
    const et200 = document.getElementById('et200');
    const et100 = document.getElementById('et100');
    const et50 = document.getElementById('et50');
    const et20 = document.getElementById('et20');
    const et10 = document.getElementById('et10');
    const et5 = document.getElementById('et5');
    const et2= document.getElementById('et2');
    const et1 = document.getElementById('et1');

    const txt2000 = document.getElementById('txt2000');
    const txt500 = document.getElementById('txt500');
    const txt200 = document.getElementById('txt200');
    const txt100 = document.getElementById('txt100');
    const txt50 = document.getElementById('txt50');
    const txt20 = document.getElementById('txt20');
    const txt10 = document.getElementById('txt10');
    const txt10 = document.getElementById('txt10');
    const txt5 = document.getElementById('txt5');
    const txt2 = document.getElementById('txt2');
    const txt1 = document.getElementById('txt1');

    const txtFinalCash = document.getElementById('txtFinalCash');
    const txtFinalCashInWords = document.getElementById('txtFinalCashInWords');
    const btnReset = document.getElementById('btnReset');
