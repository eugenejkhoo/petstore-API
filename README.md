# Petstore API Tests

This repository contains a set of API tests for the Swagger Petstore API using Postman. The tests cover CRUD operations (Create, Read, Update, Delete) for the "Pets" resource.

## Table of Contents

1. [Setup](#setup)
2. [Running the Tests](#running-the-tests)
3. [Test Scenarios](#test-scenarios)

## Setup

To set up and run these tests, follow these steps:

1. Install [Postman](https://www.postman.com/downloads/) if you haven't already.

2. Clone this repository or download the following files:
   - `Petstore - API Tests.postman_collection.json`
   - `PetStore.postman_environment.json`

3. Import the collection and environment into Postman:
   - Open Postman
   - Click on "Import" in the top left corner
   - Choose the two JSON files you downloaded
   - Confirm the import

4. Set up the environment:
   - In Postman, click on the gear icon in the top right corner to manage environments
   - Select the imported "PetStore" environment
   - Review and update any variables if necessary (e.g., `baseUrl`)

5. Access the Swagger Petstore API documentation at https://petstore.swagger.io/ for reference.

## Running the Tests

To run the tests:

1. In Postman, select the imported "Petstore - API Tests" collection.
2. Ensure the "PetStore" environment is selected in the environment dropdown.
3. Click the "Run" button to open the collection runner.
4. In the collection runner, you can choose to run all tests or select specific folders/requests.
5. Click the "Run" button in the collection runner to execute the tests.
6. Review the results in the "Run Results" tab.

## Test Scenarios

The test collection covers the following scenarios for the "Pets" resource:

### Create (POST /pet)

- Valid pet creation
  - Creates a new pet with valid data
  - Verifies the response status and pet details
- Invalid pet creation
  - Attempts to create a pet with invalid data
  - Verifies the appropriate error response

### Read (GET /pet/{petId})

- Retrieve existing pet
  - Fetches details of a previously created pet
  - Verifies the response status and pet details
- Retrieve non-existing pet
  - Attempts to fetch a pet with an invalid ID
  - Verifies the appropriate error response

### Update (PUT /pet)

- Valid update
  - Updates an existing pet's details
  - Verifies the response status and updated pet information
- Invalid update
  - Attempts to update a pet with invalid data
  - Verifies the appropriate error response

### Delete (DELETE /pet/{petId})

- Valid deletion
  - Deletes an existing pet
  - Verifies the response status
- Delete non-existing pet
  - Attempts to delete a pet with an invalid ID
  - Verifies the appropriate error response

### Retrieve (GET /pet/findByStatus) 

- Find pets by status (GET /pet/findByStatus)
  - Retrieves pets by their status (available, pending, sold)
  - Verifies the response status and pet details

