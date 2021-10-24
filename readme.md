# Deploying
set database config "config/config.js" with your own credentials
then run: 
npm i
sequelize db:migrate  
sequelize db:seed:all
npm run test (all should pass)
npm run dev 

# Routes
get('/products/'): List all available products in stock.
get('/combos/'): List all available product-combos. 
get('/cart/all'): List all items in cart (both open and closed)
get('/cart/remaining'): List remaining items in cart (only open)
get('/cart/calculate_total'): Display a Json of the final value to pay and a detail of raw value, tax value and discount value.
get('/cart/checkout'): Closes all items in the cart. 

post('/cart/add'): Adds a new item to the cart. 
post('/cart/close'): Closes an specific item of the cart. 

PostMan collection: https://app.getpostman.com/run-collection/16526102-a0677dac-bd45-4926-9789-b5bc02c2762d?action=collection%2Ffork&collection-url=entityId%3D16526102-a0677dac-bd45-4926-9789-b5bc02c2762d%26entityType%3Dcollection%26workspaceId%3D2b2dd24c-82d3-4574-b95e-6667264a6835



# Testing
At 2021-10-24 15:48, the following routes need to be tested: 
	get('/cart/calculate_total')
	get('/cart/checkout')
	