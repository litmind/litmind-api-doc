---
icon: arrow-right-to-arc
---

# How sessions work

All useful Litmind endpoints require you to create a session and send the <mark style="color:purple;">**X-SessionId**</mark> and <mark style="color:purple;">**X-UserId**</mark> additional headers along with your requests.

{% hint style="info" %}
You create a session by making a login request to the API passing along Litmind username and password, the same credentials you use to login manually on the Litmind website.
{% endhint %}

To obtain your <mark style="color:purple;">**X-SessionId**</mark> and <mark style="color:purple;">**X-UserId**</mark>**,** call the [/session/login](login.md) endpoint, which accepts your Litmind's account credentials, and answers back with this values, like this:

```bash
curl \
    -X POST https://litmind.com/api/v1/session/login \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -d 'emailOrUsername=imagine-production&password=Dq4juHcnJBw8'
```

You should get a response containing your <mark style="color:purple;">**X-SessionId**</mark> and <mark style="color:purple;">**X-UserId**</mark>, like this:

```json
{
    "entity": "Login",
    "isSuccess": true,
    "errorDescription": null,
    "sessionId": "313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588",
    "profile": {
        ...
        "id": 138829
        ...
    }
}
```

Now you're logged in and ready to request all endpoints that require a logged account. Remember to store your <mark style="color:purple;">**X-SessionId**</mark> and <mark style="color:purple;">**X-UserId**</mark> programmatically and send the proper headers from now on. Here's an example:

```bash
curl \
    -G https://litmind.com/api/v1/account/status/notifications \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -H 'X-SessionId: 313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588' \
    -H 'X-UserId: 138829'
```

## Sessions are reusable

You don't need to login each time you want to make a request. Login just once, automatically store your <mark style="color:purple;">**X-SessionId**</mark> and <mark style="color:purple;">**X-UserId**</mark> and re-use them for all consecutive requests.

## Logging in with multiple users

If you have more than one user at Litmind, you can login with all of them to perform actions from each of your accounts.

To do so, call the [/session/login](login.md) endpoint again with the new user and password credentials, but this time pass along the <mark style="color:purple;">**X-SessionId**</mark> you obtainer earlier. You'll get the corresponding <mark style="color:purple;">**X-UserId**</mark> that you can now use to call the api acting as that Litmind account.

{% hint style="info" %}
If you're a model agency, depending on your API credentials, you will be even able to log in into the accounts of the models in your agency to manage their profiles.
{% endhint %}

When logging with multiple users, call the [/session/list](list.md) endpoint to obtain a list of all the accounts currently logged into your session.

## Sessions can expire

For security purposes, session can expire over time. When your session expires, you'll obtain a **40x** HTTP error.

When this happens, your system should create a new session by logging in again and storing the new <mark style="color:purple;">**X-SessionId**</mark> and <mark style="color:purple;">**X-UserId**</mark> values.
