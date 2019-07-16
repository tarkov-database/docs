# Authentication

The API uses the open standard and stateless authentication method **JSON Web Token \(JWT\)**. A token contains all the data required for authentication, so no database query is needed.  
  
To learn more visit the [official website](https://jwt.io/introduction/).

{% api-method method="get" host="https://api.tarkov-database.com" path="/v1/token" %}
{% api-method-summary %}
Refresh Token
{% endapi-method-summary %}

{% api-method-description %}
Every token has a fixed lifetime of **60 minutes**, after which time it must be refreshed. To get a new fresh token, a **GET** request to the `/token` endpoint must be made with a previous valid token.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Authentication token via the authorization header with the type `Bearer` **\(recommended\)**
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
Authentication token via query string
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Token successfully created
{% endapi-method-response-example-description %}

```javascript
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
No or invalid token
{% endapi-method-response-example-description %}

```javascript
{
    "status": "Unauthorized",
    "message": "<ERROR MESSAGE>",
    "code": 401
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Locked user
{% endapi-method-response-example-description %}

```javascript
{
    "status": "Forbidden",
    "message": "User is locked",
    "code": 403
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}
Token signing error
{% endapi-method-response-example-description %}

```javascript
{
    "status": "Unprocessable Entity",
    "message": "<ERROR MESSAGE>",
    "code": 422
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
There is a possibility that the lifetime of tokens will change in the future. Therefore, it's recommended to automatically check the expiration time of each token.
{% endhint %}

