
# Book Shop

Build an online tool for an online company selling books.

---

## Testing

The system should include the data for at least 10 real books and include the correct details for each. The customer details should also be valid.

You are required to create the following accounts to allow the system to be tested. All accounts should have the password `p455w0rd`:

1. `customer1`
2. `customer2`
3. `admin`.

---

## Feature 1

If the user is logged in with the **admin** account they should see a **Stock levels** button on the home page. This should take them to a _Stock Levels_ screen which should have an **Add stock** button. Clicking this should take them to an _Add Stock_ screen which contains a form where they can add new books to the system. This should request the following information:

1. The name of the book.
2. The author of the book.
3. A data picker allowing the pubication date to be set.
4. The ISBN-13 number.
5. The multiline book description.
6. A picture of the front cover.
7. A slider allowing the trade price to be set (max £100).
8. A slider allowing the retail price to be set (max £100).
9. A slider allowing the quantity of books to be set (max 20).

The ISBN-13 number should be considered the _primary key_. If stock is added for a book that is already in the system it should update the existing record rather than adding a new one.

> To demonstrate this feature and to prove that the form works correctly you will need to show that the data is being persisted correctly, either by running a database query or an API call depending on the platform and technology you are using.

## Feature 2

The _Stock Levels_ screen should display the books that have been added to stock using the form from the part 1 task. This page should display:

1. A thumbnail picture of the front cover.
2. The book title.
3. The ISBN-13 number.
4. The quantity in stock.

## Feature 3

Currently the home screen is blank. Feature 3 requires the home screen to display a list of the books that are currently in stock, only the title and a thumbnail image should be shown. There should be an **Add to cart** button or link next to each of these and clicking it needs to add that book to the customer's shopping cart. The home page should also display a shopping cart icon with the number of books added displayed next to it together with the total cost of the items.

## Feature 4

Now you will display the shopping cart.

Clicking on the _shopping cart icon_ should display the user's shopping cart. This should include a link or button to take them back to the home screen so they can add more books.

Each item added to the cart should display:

1. The name of the book.
2. A thumbnail image showing the book cover.
3. The unit price.
4. The quantity selected (if the user adds the same book more tha once it should increment the quantity not add duplicate books.
5. A **delete** link or button that deletes the book and updates the shopping cart.

The overall cost of the order should be clearly shown along with  a cancel option that deletes the cart and returns the user to the home screen.

## Feature 5

The final step is to implement the checkout steps.

There now needs to be a **Checkout** button or link. This checks that the are sufficient books in stock to fulfill the order and takes the user to a **Complete order** screen which displays the final order details. If the book is not in stock this should be clearly shown in the list of items ordered and the total price adjusted accordingly.

It should also show a postage cost. This should be based on the number of books ordered and be £3 for one item with an extra £1 per additional book.

There should be a **Pay now** button. Clicking on this takes the user to a payment screen where they enter their card details (for this assignment you can fake this screen). When the order has been placed it should adjust the stock levels for the books ordered.

----

## Extras

In some assignment briefs you are given marks for the appropriate use of media and using sensors built into the user's device.

### Sensors

In some assignment briefs you are given marks for the appropriate use of sensors and sensor data. You should be implementing:

1. When a custotomer places an order the system should automatically determine which country they are ordering from and use this to calculate the delivery cost.
2. When the customer checks out the order, the address field(s) should be prefilled based on their current location but  they should be able to correct this.
3. The user should be able to use their device camera (if available) to scan a barcode which either adds the book to the cart or flags it up as invalid.

### Media

In the requirements listed above you need to provide the user with the ability to upload photos. For the extra media marks you will need to expand this by:

1. Providing the user with the choice of uploading photos, video clips or audio clips.
2. Giving users the option to directly capture images, audio and video clips using the built-in camera and/or microphone if available.

### Data

There are lots of online RESTful APIs you can make use of when developing this system. You should consider:

1. The [Google Books API](https://www.googleapis.com/books/v1/volumes?q=isbn:9780596517748)
2. [LocationIQ](https://locationiq.com)
