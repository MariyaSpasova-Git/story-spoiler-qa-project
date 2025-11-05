# Story Spoiler API Specification

This document provides a summary of the Story Spoiler API endpoints and their intended functionality. All endpoints are tested using Postman and require proper authentication for spoiler-related actions.

## Methods supported  

All supported methods can be found on the following link: [https://d3s5nxhwblsjbi.cloudfront.net/api](https://d3s5nxhwblsjbi.cloudfront.net/api). 

The following endpoints are supported: 

## User Endpoints

### 1. Create User
**Method:** `POST`  
**URL:** `/api/User/Create`  
**Purpose:** Registers a new user account.
**Expected Response (201 Created):**
```json
{
    "msg": "Account created successfuly",
    "email": "User1@example.com",
    "username": "User1",
    "accessToken": null
}
```

### Authenticate User
**Method:** `POST`  
**URL:** `/api/User/Authentication`  
**Purpose:** Logs in an existing user and returns an access token.
**Expected Response (200 OK):**
```json
{
    "username": "User1",
    "password": "password123",
    "accessToken": "h3d2ty..."
}
```

## Spoiler Endpoints
⚠️ All Spoiler endpoints require Authorization: Bearer Token.

### 3. Get All Spoilers
**Method:** `GET`  
**URL:** `/api/Story/All`  
**Purpose:** Lists all spoilers created by the authenticated user.
**Expected Response (200 OK):** Returns an array of spoilers in JSON format.

### 4. Search Spoilers
**Method:** `GET`  
**URL:** `/api/Story/Search?keyword={storyTitle}`  
**Purpose:** Searches spoilers by title keyword.
**Expected Response (200 OK):** Returns a filtered list of spoilers matching the keyword.

### 4. Create Spoiler
**Method:** `POST`  
**URL:** `/api/Story/Create`  
**Purpose:** Creates a new spoiler entry.
**Expected Response (201 Created):**
```json
{
  "msg": "Successfully created",
  "storyId": "z4567-..."
}
```

### 5. Edit Spoiler
**Method:** `PUT`  
**URL:** `/api/Story/Edit/{storyId}`  
**Purpose:** Updates the title, description, or URL of an existing spoiler.
**Expected Response (200 OK):**
```json
{
  "msg": "Successfully edited",
  "storyId": "z4567-..."
}
```

### 6. Delete Spoiler
**Method:** `DELETE`  
**URL:** `/api/Story/Delete/{storyId}`  
**Purpose:** Deletes an existing spoiler.
**Expected Response (200 OK):**
```json
{
  "msg": "Deleted successfully"
}
```

## Notes
- The API is stateless — every operation requires a valid token.
- All request and response examples use dummy data.
- The image URLs point to public placeholder sources (e.g., picsum.photos).
- Endpoints conform to RESTful design principles.

*Document created as part of the Story Spoiler QA Project (API Testing Section).*  
*Last updated: November 2025*  
*Author: Mariya Spasova*