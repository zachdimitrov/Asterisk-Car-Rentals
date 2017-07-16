# Asterisk - Car Rentals

## Teamwork project plan

### 01. Models

1. user
2. admin - inherit user
3. support user
4. car category - collection of many cars
5. deals - collection of many cars
6. car
7. review
8. comment

### 02. Pages

#### Dynamic pages

**public pages:**

- `home` - nav + logo in header, banner, some car categories, some info, some reviews (from registered users), footer
- `login/register`
- `cars` - all cars (eventually sorting by: price, category (small to large; large to small))
- `search cars` - shows only cars that are available for the requested period
- `car details` - for a single car, comments (only auth users can post comment)
- `special offers` - only cars that have discounted price, ordered by category (compact, economy, premium etc.)

**pages for auth users:**

- `user profile` - name, telephone, email etc. (he can update all personal info and password)
	- if the user is admin - he also have administration page and there he can change info about cars and also select wich cars to have special offer and by how much (type % and it calculate the special price and also show's original price with style: line-trough)
- `my bookings/reservations` - history of all previous bookings
- `booking/reservation of a car` - choosing dates from calendar, extras (gps), additional insurance etc.
- `leave a review` (about this rent-a-car service)

### 03. Requirements

#### Application Back-end (Server) - up to 40%

1. At least 5 different public dynamic web pages
	- Using Pug														| https://pugjs.org/language/attributes.html
2. At least 3 different private (authenticated) dynamic web pages
	- Using Pug
3. At least 5 different public RESTful routes for AJAX
4. At least 1 private (authenticated) route for AJAX
5. Use Express for the server
	- Use an MV-* pattern
6. Use MongoDB
	- As data storage
	- Do not use Mongoose
7. Create a data/service layer for accessing the database
8. Use Passport - for managing users								| https://github.com/jaredhanson/passport-local
9. Implement WebSockets
	- Using Socket.io or anything else


#### Application front-end (client) - up to 25%

1. Use any framework of your choice for the front-end
	- Optional, not required
	- KendoUI, AngularJS, Angular 2, Knockout, Bootstrap, etc...
2. Implement responsive design
	- It may be based on Bootstrap, Materialize or any other UI framework
3. Use at least one AJAX form and/or WebSockets communication
	- maybe the form on home page - when the user type 3 characters - to make GET request for all cities with typed characters
4. Apply error handling and data validation to avoid crashes when invalid data is entered
	- maybe toastr of similar
5. Use loaders, modals and notifications when applicable 
	- modal from JQuery UI for posting comment
6. Prevent yourself from security holes (XSS, XSRF, Parameter Tampering, etc.)
	- Handle correctly the special HTML characters and tags like `<script>, <br />`, etc.
7. Create usable UI
	- No need to be pretty, but usable