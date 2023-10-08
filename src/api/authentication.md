# Obtaining an Access Token using OAuth 2.0 Client Credentials Flow

OAuth 2.0 is a popular protocol used for securing API access. The Client Credentials Flow is one of the grant types in OAuth 2.0 that allows a client (typically a server or a trusted application) to obtain an access token directly from the authorization server without involving a user. This access token can then be used to access protected resources on the API. In this guide, we'll walk you through the steps to obtain an access token using the Client Credentials Flow, with JSON as the communication format.

## Prerequisites

Before you begin, make sure you have the following prerequisites in place:

- **Client Credentials:** You should have the client ID and client secret provided by the authorization server. You can obtain this by creating a client via the [identity site](https://id.tarkov-database.com).

## Steps to Obtain an Access Token

Follow these steps to obtain an access token using the Client Credentials Flow:

### 1. Construct the Token Request

Compose a POST request to the authorization server's token endpoint (`https://identity.tarkov-database.com/v1/oauth/token`). Include the following parameters in the request body as a JSON object:

- `grant_type`: Set this to "client_credentials" to specify the Client Credentials Flow.
- `client_id`: Your client ID.
- `client_secret`: Your client secret.
- ~~`scope`: Define the scope of access required.~~

Here is an example request:

```HTTP
POST https://identity.tarkov-database.com/v1/oauth/token HTTP/1.1
Content-Type: application/json

{
    "client_id": "<CLIENT-ID>",
    "client_secret": "<CLIENT-SECRET>",
    "grant_type": "client_credentials",
}
```

### 2. Send the Token Request

Send the POST request to the authorization server's token endpoint (`https://identity.tarkov-database.com/v1/oauth/token`). You can use your preferred HTTP client library or tool (e.g., cURL, Postman) to make the request.

### 3. Receive the Access Token

Upon successful authentication and authorization, the authorization server will respond with an access token in the JSON format. The response typically includes:

- `access_token`: The access token that you can use to access the protected resources.
- `token_type`: The type of the token (usually "Bearer").
- `expires_in`: The expiration time of the token (in seconds).
- ~~`scope`: The scope of access granted.~~

Here is an example response:

```json
{
    "access_token": "<ACCESS-TOKEN>",
    "token_type": "Bearer",
    "expires_in": 3600,
}
```

### 4. Use the Access Token

Now that you have obtained an access token, you can include it in the `Authorization` header of your API requests as follows:

```HTTP
GET /api/resource HTTP/1.1
Host: <SERVICE>.tarkov-database.com
Authorization: Bearer <ACCESS-TOKEN>
```

## Conclusion

That's it! You have successfully obtained an access token using the OAuth 2.0 Client Credentials Flow. Remember to handle the token securely and renew it as needed, as access tokens typically have a limited lifespan.

Happy coding!
