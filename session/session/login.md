# Login

<mark style="color:red;">**POST**</mark> `/session/login`

Log in to your Litmind account. This is needed for all endpoints that perform actions related to your account at Litmind (for example: retrieving a list of candidate models in your castings)

#### Headers

<table><thead><tr><th width="191">Name</th><th width="100" data-type="checkbox">Required</th><th>Value</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:purple;"><strong>X-Key</strong></mark></td><td>true</td><td>Your API Key</td><td></td></tr><tr><td><mark style="color:purple;"><strong>X-SessionId</strong></mark></td><td>false</td><td>Your session id. If not specified, a new session will be created</td><td></td></tr></tbody></table>

#### Body

<table><thead><tr><th width="228">Name</th><th>Description</th><th width="100" data-type="checkbox">Required</th></tr></thead><tbody><tr><td><mark style="color:purple;"><strong>emailOrUsername</strong></mark></td><td>The username or the email of your Litmind account</td><td>true</td></tr><tr><td><mark style="color:purple;"><strong>password</strong></mark></td><td>The password of your Litmind account</td><td>true</td></tr></tbody></table>

#### Example

```bash
curl \
    -X POST https://litmind.com/api/v1/session/login \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -d 'emailOrUsername=imagine-production&password=Dq4juHcnJBw8'
```

#### Response

```json
{
    "entity": "Login",
    "isSuccess": true,
    "errorDescription": null,
    "sessionId": "313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588",
    "profile": {
        <Profile entity>
    }
}
```

* <mark style="color:blue;">**isSuccess**</mark> Whether the login was performed successfully.
* <mark style="color:blue;">**errorDescription**</mark> If there was an error while logging in, a description.
* <mark style="color:blue;">**sessionId**</mark> Your session id, to be passed from now on as the value for the <mark style="color:purple;">**X-SessionId**</mark> header when [making requests that require it](../../connecting/quickstart.md).
* <mark style="color:blue;">**profile.id**</mark> Your user id, to be passed from now on as the value for the <mark style="color:purple;">**X-UserId**</mark> header when [making requests that require it](../../connecting/quickstart.md).

