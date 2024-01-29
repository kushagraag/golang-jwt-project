## A simple application which implements jwt authentication in golang

## Steps to run
-- install golang and mongodb if not already.
-- run go mod tidy to install necessary packages
-- run "go run main.go" to run project
-- default port is 9000, changeable in .env file
-- default db name is "JWT-Auth", changeable in database/databaseConnection.go

### For any api -> localhost:9000/

### 6 apis are created which can be tested in postman or any other way
| /users/signup | for signup, set fields as in models/userModel.go. keep an eye on required fields
| /users/login | for login, use only email and password. user_id and token can be obtained from here
| /users | to get all users. only admin can get all users. copy token after login, create a new header "token", paste token value in value field to get all users
| /users/:user_id | to get user by specific id. admin can access any user, USER can access only self information. use token as mentioned above for both
| /api-1 | unusable 
| /api-2 | unusable
