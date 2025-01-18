---
icon: bullseye-arrow
---

# Making a request

API requests are done via HTTPS requests to <mark style="color:yellow;">**api.litmind.com/api/v1**</mark>, with the following header:

* <mark style="color:yellow;">**X-Key**</mark> Your API key

This is an example of a simple request:

```bash
curl \
    -G https://litmind.com/api/v1/status/version \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ'
```

The API will respond with a standard HTTP code indicating the status of the request and a JSON body. Here's an example:

```json
{
    "availableVersions": [
        "1"
    ],
    "requestVersion": "1",
    "latestVersion": "1"
}
```

## Requesting user endpoints

Most endpoints will additionally require you to provide a **session id** and a **user id** by providing the following additional headers:

* <mark style="color:yellow;">**X-SessionId**</mark> The session id
* <mark style="color:yellow;">**X-UserId**</mark> The user id

To obtain your **X-SessionId** and **X-UserId,** call the [/session/login](../session/login.md) endpoint, which accepts your Litmind's account credentials, and answers back with this value&#x73;**.**

Here's an example of a request to an endpoint that requires a logged account:

```bash
curl \
    -G https://litmind.com/api/v1/account/status/notifications \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -H 'X-SessionId: 313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588' \
    -H 'X-UserId: 138829'
```

