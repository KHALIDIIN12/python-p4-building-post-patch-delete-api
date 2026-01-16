# TODO: API Implementation Plan

## Information Gathered:
- Current `server/app.py` has GET routes for games, reviews, and users
- `server/models.py` has Game, Review, and User models with proper relationships
- Need to implement POST, PATCH, and DELETE methods for reviews
- The solution code shows the expected implementation pattern

## Plan:
1. **Update `/reviews` route to handle POST requests**
   - Add POST method to handle review creation
   - Accept score, comment, game_id, user_id from request form data
   - Return 201 status code on successful creation

2. **Update `/reviews/<int:id>` route to handle PATCH and DELETE requests**
   - Add error handling (404 if review not found)
   - Implement PATCH for updating review attributes
   - Implement DELETE for removing reviews from database

3. **Add error handling to `/games/<int:id>` route**
   - Return 404 if game is not found

4. **Test the implementation**
   - Run the server and test endpoints with Postman or curl
   - Ensure all CRUD operations work correctly

## Implementation Steps:
- [x] Modify `/reviews` route to accept POST method
- [x] Modify `/reviews/<int:id>` route to accept GET, PATCH, DELETE methods
- [x] Add error handling for missing records
- [ ] Test the API endpoints

