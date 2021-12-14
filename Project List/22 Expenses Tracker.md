# Expenses Tracker

A web app where users can track their business expenses.

---

## Testing

You are required to create the following accounts to allow the system to be tested. All accounts should have the password `p455w0rd`:

1. `user1`
2. `user2`
3. `manager1` (line manager for `user1`, only needed for stage 2 functionality).
4. `manager2` (line manager for `user2`, only needed for stage 2 functionality).

---

## Feature 1

Users need to be logged in to see the system. Anyone not logged in should be redirected to the _Login_ screen. When a user is logged in they should see an **Add expenses** button or link. This sends them to a screen where new expenses can be added. This should ask the user for:

1. The date (this should default to the current date and be selected using a date picker).
2. A category to be picked from one of the following four categories: travel, food & drink, accomodation, other.
3. A short label (used on the home screen).
4. A box where the user enters the amount being claimed.
5. An optional multi-line description of the expense that supports _markdown_ formatting.
56. An upload tool to upload a scanned copy of the receipt from the `user's` computer.

In addition to this data, the database should also store:

1. The username of the person adding the item.
2. The current date and time.
3. The status of the expense which should be set to `not-approved`.

> To demonstrate this feature and to prove that the form works correctly you will need to show that the data is being persisted correctly, either by running a database query or an API call depending on the platform and technology you are using.

## Feature 2

The home screen should display a list of all the expenses they have added plus a running total. Each user should only see their own expenses and it should only show items with a status of `not-approved` Each item should display:

1. The date the expense was incurred.
2. The date the expense was added to the system (but not the time).
2. A short one line label.
3. The amount in GBP.

## Feature 3

Clicking on an expense label should display the details for that particular expense which should include:

1. The date of the expense (but not the time using the format DD/MM/YYYY). expenses should be listed in date order with the most recent at the top.
2. The category.
3. The label.
4. The description of the expense.
5. A thumbnail image of the scanned receipt, clicking this should enlarge it.

## Feature 4

This feature requires you to add a `manager's` console to the web app. One of the accounts needs to be flagged as the manager's and the following screens must only be accessible to this user:

The manager's home screen should show:

1. The number of expenses claims that are waiting for approval (this should update as they approve/cancel requests).
2. The total amount of the expenses waiting to be dealt with.

There should be a summary all the users including:

1. Their profile picture.
2. Their name (first and last).
3. The total unclaimed expenses (see third screen).
    
Clicking on the name or profile picture of a user should display the detailed expenses screen for that user (the same information as the normal user's home screen). It should also allow each expense to be clicked to view the details page (same as the normal user in the feature 3 functionality).

The detailed expense screen should include a button/link against each user labelled "Approve" and another called "Decline". Clicking on either should Set the status of all these expense items to **approved** or **declined**.
