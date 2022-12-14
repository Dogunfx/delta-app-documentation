## List of APIs and their responds type

Check out the live demo here [Demo App](https://delta-state-smartwaste-app-frontend.vercel.app/).




Endpoint for Login [POST END POINT: https://delta-state-smart-waste.onrender.com/api/v1/user/login]( https://delta-state-smart-waste.onrender.com/api/v1/user/login).

Request Type {

        method: POST
        
        headers: {
            Content-Type: "application/json"
        }

        body: {
            email:  @required
            password: @required
        }

}


Responds type { 

    errors: []--- contains list of errors of a given request

    success: boolean --- show the success state of a request could be true or false,

    token: will contain a token when the user is authenticated or null if not

    message: string --  a string containing a message to see for the frontend users

 }


 Endpoint for Registration [POST END POINT: https://delta-state-smart-waste.onrender.com/api/v1/user/register]( https://delta-state-smart-waste.onrender.com/api/v1/user/login).

Request Type {

        method: POST
        
        headers: {
            Content-Type: "application/json"
        }

        body: {
            email:  @required
            password: @required
            name: @required
            phone: @required
            c_password: @required
        }

}


Responds type { 

    errors: []--- contains list of errors of a given request

    success: boolean --- show the success state of a request could be true or false,

    message: string --  a string containing a message to see for the frontend users

 }


  Endpoint for profile [GET END POINT: https://delta-state-smart-waste.onrender.com/api/v1/user/register]( https://delta-state-smart-waste.onrender.com/api/v1/user/profile).

Request Type {

        method: GET
        
        headers: {
            Content-Type: "application/json"
            Authorization: "bearer $token" ---  where token is the jwt sent after a successful login
        }

        body: {}

}


Responds type { 

    errors: []--- contains list of errors of a given request

    success: boolean --- show the success state of a request could be true or false,

    message: string --  a string containing a message to see for the frontend users

    payload: {
        user: UserModel -- details of the authenticated user
    }

 }



