# jwt-authentication

# express App to validate user authenticity using jwt token

1.clone repo , and run command   npm i to install all node dependencies -- postman or any other client to hit api requests

2. create a .env file with following contents

  ```
     MONGO_URI ="<replace with your mongo db uri>"
     API_PORT = 3001
     TOKEN_KEY = "RAndomStringxyz"-- This can be any random String 
  ```
  
 3. for registering , hit post request from postman to http://localhost:3001/register with following keys in payload
 ```
 {
    "firstName":"ijaz",
    "lastName":"Ahamed",
    "email":"ijazahamed@gmail.com",
    "password":"12345"
}
 ```
 4. for login , hit post request from postman to http://localhost:3001/login with following keys in payload
 ```
 {
    "firstName":"ijaz",
    "lastName":"Ahamed"
  }
  ```
5.copy the token from response and  hit post request from postman http://localhost:3001/welcome
with header 
```
x-access-token : < your token >
```

here we validate jwt token , if validated return login success.
