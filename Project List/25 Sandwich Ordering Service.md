
# Sandwich Ordering Service

In this project you will be developing a piece of software that allows people working in an office to place daily sandwich orders that will be delivered direct to their office.

---

## Testing

You are required to create the following accounts to allow the system to be tested. All accounts should have the password `p455w0rd`:

1. `customer1`
2. `customer2`
3. `customer3`
4. `owner`

---

## Feature 1

When the `admin` user is logged in they can see an **Add product** button. Clicking this takes them to a screen where they can add new product they want to sell.

The screen should display a form that contains the following:

1. A dropdown category selector where they can choose from "Sandwich", "Drink" or "Snack".
2. A textbox where they can enter the name of the item.
3. A multiline textbox where they can enter a short description of up to 100 characters.
4. A price slider where they can choose the price being charged in _pence_, this should have the scale 50-500p.
5. The _option_ to **upload** a picture of the item (not link to an online image).

> To demonstrate this feature and to prove that the form works correctly you will need to show that the data is being persisted correctly, either by running a database query or an API call depending on the platform and technology you are using.

## Feature 2

The `admin` user's **Home Screen** should display a list of the items they are selling. Each item should display:

1. its name.
2. A thumbnail photo (or a placeholder image if no photo is available).
3. A **Remove** button.

The items should be grouped into the three categories from the dropdown. Each group should include a heading such as **Sandwiches** followed by the products from that category.

Clicking on a **Remove** button should delete the product and update the screen.

## Feature 3

When a non-admin user logs in their homescreen should display a message **No Order Placed** followed by a big button **Place order**. This takes them to a screen displaying a list of the available sandwiches with each displaying the name, price and photo (or placeholder image).

When the user clicks on one of the thumbnails they are shown a list of all the **Drinks** (same information displayed). After clicking on their choice of drink they are finally shown the list of snacks.

After picking a snack they are shown an order summary screen including the photo, name and price of each item selected together with a total price.

## Feature 4

The summary screen should display a **Place order** button. Clicking this displays a form where they can enter their name and delivery address. If this is not their first order the form should contain the name and delivery address from their previous order which they can amend if needed. After confirming the order they get a receipt with an order number they can print off.

## Feature 5

The home screen for the admin/owner should contain similar information as the customer home screen with the following changes:

1. Only items that have been ordered by at least one customer should be displayed.
2. Each of these items should list the quantity that have been ordered by customers.
3. Each should have a **Picked** button which is clicked when the owner has packed the required produce and quantity ready for delivery. This removes the item from the list.
