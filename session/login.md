# Login

<mark style="color:red;">**POST**</mark> `/session/login`

Log in to your Litmind account. This is needed for all endpoints that perform actions related to your account at Litmind (for example: retrieving a list of candidate models in your castings)

**Body**

<table><thead><tr><th>Name</th><th width="100">Type</th><th>Description</th></tr></thead><tbody><tr><td>emailOrUsername</td><td>string</td><td>The username or the email of your Litmind account</td></tr><tr><td>password</td><td>string</td><td>The password of your Litmind account</td></tr></tbody></table>

**Example**

```bash
curl \
    -X POST https://litmind.com/api/v1/session/login \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -d 'emailOrUsername=imagine-production&password=Dq4juHcnJBw8'
```

**Response**

```json
{
    "isSuccess": true,
    "errorDescription": null,
    "sessionId": "313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588",
    "profile": {
        "id": 138829,
        "profileImage": {
            "urls": {
                "thumbnail": "https://cdn.litmind.com/mvqP0JaEkjbdEAA0sTPHwY9vAjsNDSAd.UserLogoSingleImage.193978.profile_non_retina.jpg",
            }
        },
        "username": "imagine-production",
        "typeTitle": "Production company"
    }
}
```

* <mark style="color:green;">**isSuccess**</mark> Whether the login was performed successfully.
* <mark style="color:green;">**errorDescription**</mark> If there was an error while logging in, a description.
* <mark style="color:green;">**sessionId**</mark> Your session id, to be passed from now on as the value for the **X-SessionId** header when [making requests that require it](../connecting/quickstart.md).
* <mark style="color:green;">**profile.id**</mark> Your user id, to be passed from now on as the value for the **X-UserId** header when [making requests that require it](../connecting/quickstart.md).

