# API Test Cases – Story Spoiler

| **ID** | **Test Case** | **Endpoint** | **Method** | **Preconditions** | **Expected Result** | **Status** |
|:------:|----------------|---------------|-------------|-------------------|---------------------|:----------:|
| **TC-API-01** | Authenticate User | `/api/User/Authentication` | POST | Valid user credentials | Access token returned in JSON response | ✅ Passed |
| **TC-API-02** | Create New Spoiler | `/api/Story/Create` | POST | Valid access token | Spoiler successfully created and visible in list | ✅ Passed |
| **TC-API-03** | List All Spoilers | `/api/Story/All` | GET | Valid access token | Returns array of spoilers including newly created one | ✅ Passed |
| **TC-API-04** | Change Spoiler Title | `/api/Story/Edit/{storyId}` | PUT | Valid access token & existing spoiler ID | Spoiler updated successfully | ✅ Passed |
| **TC-API-05** | Delete Spoiler | `/api/Story/Delete/{storyId}` | DELETE | Valid access token & existing spoiler ID | Spoiler deleted successfully | ✅ Passed |