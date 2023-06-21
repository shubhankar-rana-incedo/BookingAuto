# BookingAuto
Automation of https://www.booking.com/

**Feature File (`booking.feature`):**
```gherkin
Feature: Hotel Booking

  Scenario: Book a hotel room
    Given I am on the hotel booking website
    When I search for available hotels in "New York" for the dates "2023-07-01" to "2023-07-05"
    And I filter the search results by "4 stars" and "Free Wi-Fi"
    And I sort the search results by "Price: Low to High"
    Then I select the first available hotel
    And I enter guest details and complete the booking
    And I verify that the booking is confirmed
```

**Step Definitions (`steps.js`):**
```javascript
const { Given, When, Then } = require('cucumber');
const { chromium } = require('playwright');

let browser, context, page;

Given('I am on the hotel booking website', async () => {
  // Code to navigate to the hotel booking website
});

When('I search for available hotels in {string} for the dates {string} to {string}', async (location, startDate, endDate) => {
  // Code to enter search criteria and perform the search
});

When('I filter the search results by {string} and {string}', async (starRating, amenity) => {
  // Code to apply filters to the search results
});

When('I sort the search results by {string}', async (sortingOption) => {
  // Code to sort the search results
});

Then('I select the first available hotel', async () => {
  // Code to select the first hotel from the search results
});

Then('I enter guest details and complete the booking', async () => {
  // Code to enter guest details, select room options, and complete the booking process
});

Then('I verify that the booking is confirmed', async () => {
  // Code to verify the booking confirmation, such as checking for a confirmation message or email
});

After(async () => {
  // Code to close the browser
});
```

In this scenario, we have a multi-step process for booking a hotel room. The step definitions are left empty for you to fill in with the appropriate Playwright.js actions and assertions.

- The `Given` step should contain code to navigate to the hotel booking website.
- The `When` steps should include the code to perform various actions, such as entering search criteria, applying filters, sorting the results, selecting a hotel, entering guest details, and completing the booking process.
- The `Then` steps should contain the code to verify the expected outcomes, such as confirming the booking and checking for a confirmation message or email.

You will need to complete the step definitions by utilizing Playwright.js methods to interact with the hotel booking website and perform the necessary actions to complete the booking process.

Remember to import the necessary Playwright.js functions and handle browser setup and teardown in the `Before` and `After` hooks.

Once you have completed the step definitions, you can run your tests using a test runner like `cucumber-js`.

Feel free to modify and expand upon this scenario based on your specific requirements and the functionality of the hotel booking website you are automating.
