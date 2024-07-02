# Hyundai Dealer Website Testing

This repository contains a Playwright test suite for validating various aspects of Hyundai websites across different regions.

## Overview

The main test file is `dahma-12.spec.ts`, which performs the following checks for each website:

1. Verifies that the website is accessible from Brazil.
2. Checks if the `providerID` meta tag exists in the DOM.
3. Validates that the `providerID` meta tag value matches the expected value.
4. Ensures that the `providerID` meta tag value can be accessed as a global variable, which is required for Google Tag Manager (GTM) configuration.
5. Waits for a Google Analytics 4 (GA4) page_view event to be triggered within 30 seconds.
6. Verifies that only one GA4 page_view event is triggered.
7. Checks if the `ep.provider_id` parameter is included in the GA4 page view event with the expected value.

## Running the Tests

To run the tests, you'll need to have Node.js and Playwright installed. Follow these steps:

1. Clone the repository
2. Navigate to the project directory
3. Install dependencies: `npm install`
4. Run the tests: `npx playwright test`
5. View the results: `npx playwright show-report`

## Test Data

The test data is defined as an array of strings in the `sites` variable within `dahma-12.spec.ts`. Each string represents a dealer website URL, the expected `providerID` meta tag value, and the expected `ep.provider_id` value for GA4, separated by commas.

## Contributing

If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.
