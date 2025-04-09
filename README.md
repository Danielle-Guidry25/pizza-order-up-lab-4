ta charset="UTF-8">
ta name="viewport" content="width=device-width, initial-scale=1.0">
tle>Aurora's Pizza</title>
yle>
 body {
     font-family: Arial, sans-serif;
     margin: 20px;
     padding: 0;
 }
 body, html {
     height: 100%;
 }
 h1, h2, h3, h4, h5, h6 {
     font-family: "Amatic SC", sans-serif;
 }
 .menu {
     display: none;
 }
 .bgimg {
     background-repeat: no-repeat;
     background-size: cover;
     background-image: url("/w3images/pizza.jpg");
     min-height: 90%;
 }
 .container {
     max-width: 600px;
     margin: 0 auto;
 }
 h1 {
     text-align: center;
 }
 form {
     display: flex;
     flex-direction: column;
 }
 label {
     margin-top: 10px;
 }
 input, select, button, textarea {
     margin-top: 5px;
     padding: 10px;
     font-size: 16px;
 }
 button {
     background-color: #00c0bc;
     color: rgb(40, 14, 14);
     border: none;
     cursor: pointer;
 }
 button:hover {
     background-color: #217288;
 }
tyle>
</head>
v class="container">
 <h1>Order Your Pizza</h1>
 <form id="pizzaOrderForm">
     <label for="name">Name:</label>
     <input type="text" id="name" name="name" required>
     <label for="size">Pizza Size:</label>
     <select id="size" name="size" required>
         <option value="small">Small</option>
         <option value="medium">Medium</option>
         <option value="large">Large</option>
     </select>
     <label for="toppings">Toppings:</label>
     <select id="toppings" name="toppings" multiple>
         <option value="pepperoni">Pepperoni</option>
         <option value="mushrooms">Mushrooms</option>
         <option value="onions">Onions</option>
         <option value="sausage">Sausage</option>
         <option value="bacon">Bacon</option>
         <option value="extra_cheese">Extra Cheese</option>
         <option value="black_olives">Black Olives</option>
         <option value="green_peppers">Green Peppers</option>
     </select>
     <label for="instructions">Special Instructions:</label>
     <textarea id="instructions" name="instructions" rows="4"></textarea>
     <button type="submit">Place Order</button>
 </form>
iv>
ript>
 document.getElementById('pizzaOrderForm').addEventListener('submit', functi
     event.preventDefault();
     const name = document.getElementById('name').value.trim();
     const size = document.getElementById('size').value;
     const toppings = Array.from(document.getElementById('toppings').selecte
     const instructions = document.getElementById('instructions').value.trim
     if (!name) {
         alert('Please enter your name.');
         return;
     }
     if (!size) {
         alert('Please select a pizza size.');
         return;
     }
     if (toppings.length === 0) {
         alert('Please select at least one topping.');
         return;
     }
     alert(`Thank you, ${name}! Your ${size} pizza with ${toppings.join(', '
 });
cript>
</body>
</html>
