
# Theatre Booking

Build a website for a local theatre company. They have a single stage and, due to the cost of building the stage sets, aim to have two performances per day (matinee and evening) and run each production for 5 days running Friday - Tuesday (10 performances). All play, performance and order dates should be stored in a database.

---

## Testing

You are required to create the following accounts to allow the system to be tested. All accounts should have the password `p455w0rd`:

1. `user1`
2. `user2`
3. `user3`
4. `admin`
---

## Feature 1

Users can view the website without needing to log in. If the `admin` user is logged in they should see an **Add show** link or button. This takes them to the _Add Show_ screen where they add a new show by completing a form with the following fields:

1. Name of Show
2. **multi-line formatted text area** for the description of the show.
3. The ability to upload a poster image.
4. Pick the start date using a date picker.
5. Pick the end data using a data picker (can't be before the start date).

In addition to this data, the database also needs to store the date and time when the show was added.

> To demonstrate this feature and to prove that the form works correctly you will need to show that the data is being persisted correctly, either by running a database query or an API call depending on the platform and technology you are using.

## Feature 2

The homepage needs to show the plays that are scheduled. For each play the following should be displayed:

1. The name.
2. A thumbnail of the poster image.
3. The date (but not the time) of the first performance in the format DD-MM-YYYY.
4. The number of days the show runs for.

## Feature 3

If the user is logged in there should be a **Details** link or button next to each show on the _Homepage_. This should take the user to the _Play_ screen. This should have a entry for each date the performance runs. This should include:

1. The play name (shown as part of the page header)..
2. A large image of the poster.
2. A list of all the performace dates.
3. The formatted description of the play.

## Feature 4

Assuming one performance per day and 30 seats all costing the same £10, the next functionality is to allow users to book seats. There needs to be a **Book seats** button next to each performance on the _Play_ screen. Clicking this adds one ticket for that particular day to the shopping cart for the logged-in user. As each ticket is added to the cart the remaining tickets for that performance should go down by one.

Once the required tickets have been chosen the user should be able to click on a **Checkout button**.

---

## Extras

In some assignment briefs you are given marks for the appropriate use of media and using sensors built into the user's device.

### Sensors

In some assignment briefs you are given marks for the appropriate use of sensors and sensor data. You should be implementing:

1. When a user books tickets the software should capture their current location and store it with the booking details.
2. For a given production the admin person should be able to see a map with the locations of people who bought tickets.
3. When the system asks for a photo it should provide access to the device camera (if available).

### Media

In the requirements listed above you need to provide the user with the ability to upload photos. For the extra media marks you will need to expand this by:

1. Providing the user with the choice of uploading photos, video clips or audio clips.
2. Giving users the option to directly capture images, audio and video clips using the built-in camera and/or microphone if available.

### Data

There are lots of online RESTful APIs you can make use of when developing this system. You should consider:

1. [Ingresso](https://docs.ingresso.co.uk)
2. [The List API](https://api.list.co.uk/getting-started)
3. [LocationIQ](https://locationiq.com)
