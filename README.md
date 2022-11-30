# How to start

- Clone the repository
- Run the command npm install in root directory of this project to install dependencies
- Start the server using the command **node server.js**

# Available routes
There are two routes available in this project.

## Base url 
http:localhost:5000

## GET /users/test 
This route is a test route to confirm everything is working.

### Response 
| Response code| Response Type | Example |
|:---------|:--------------|:--------|
| 200    |  Success | { msg: 'Test route works' }| 




## POST /users/create
This route creates a new user in the database.

### Request Body Parameters

| Parameter| Type | Example |
|:---------|:-----|:--------|
| email    | String| john@email.com| 
| name    | String| John Doe|

### Response 
| Response code| Response Type | Example |
|:---------|:--------------|:--------|
| 200    | Success | { success: true, msg: 'User created successfully' } | 
| 400    | Failure | { success: false, msg: 'Both name and email are required' } |
| 500    | Error | { success: false, msg: 'Some error occurred' } |

## GET /users 
This route fetches all the users from the database.

### Response 
| Response code| Response Type | Example |
|:---------|:--------------|:--------|
| 200    |  Success | List of users | 
| 500    |  Error fetching database | { success: false, msg: 'Some error occurred' } | 