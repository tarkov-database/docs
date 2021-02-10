# Authentication

The API uses the open standard and stateless authentication method **JSON Web Token (JWT)**. A token contains all the data required for authentication, so no database query is needed.

To learn more visit the [official website](https://jwt.io/introduction/).

## Get A Token
If you do not have a token yet, you can apply for one using the following form.

[API Request Form](https://forms.gle/A67VotJK8FPZeDKK9)

## Use A Token
For every request, a valid token must be transmitted. This can be done with passing the token via the [authorization header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Authorization) with the type `Bearer`.
```HEADER
Authorization: Bearer <TOKEN>
```

## Refresh A Token
Every token has a fixed lifetime, after which time it must be refreshed.
To get a new fresh token, a `GET` request to the `/token` endpoint must be made with a previous valid token.


### **GET** `/token`

#### `201` Created
Token successfully created
```JSON
{
    "token": "<TOKEN>",
    "expires": 1610591017
}
```

#### `401` Unauthorized
No or invalid token
```JSON
{
    "status": "Unauthorized",
    "message": "<ERROR MESSAGE>",
    "code": 401
}
```

#### `403` Forbidden
Locked user
```JSON
{
    "status": "Forbidden",
    "message": "User is locked",
    "code": 403
}
```

#### `422` Unprocessable Entity
Token signing error
```JSON
{
    "status": "Unprocessable Entity",
    "message": "<ERROR MESSAGE>",
    "code": 422
}
```
