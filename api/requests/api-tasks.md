# Story Spoiler API – Postman Request Tasks

This section describes the five API request tasks performed during testing in Postman. Each request was added to the Story Spoiler API Tests collection and executed in sequence.

---

## 1️. Authenticate User

Send a POST request to log in with valid credentials created in the Story Spoiler web app. 
If successful, the response will include an access token, which must be used as a Bearer Token for all subsequent requests.

## 2️. Create New Spoiler

Send a POST request to create a new spoiler entry. 

## 3. Retrieve All Spoilers

Send a GET request to fetch all spoilers created under the current user profile.
The response includes spoilers created through both the API and the web interface.

## 4. Update Spoiler Title

Send a PUT request to modify the spoiler created in the previous steps.
Use the spoiler’s unique id obtained from the list of spoilers.

## 5. Delete Spoiler

Send a DELETE request for the spoiler updated in the previous step.
Provide the correct spoiler ID to remove the record.

---

## 🔗 Postman Collection File

The complete Postman collection used for these tests can be found at:

**`/api/requests/storyspoiler-api-tests.postman_collection.json`**

To re-run the tests:
1. Open Postman.
2. Click **Import** → select the file above.
3. Run the collection in sequence or use the **Runner** tool.
