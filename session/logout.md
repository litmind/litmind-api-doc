# Logout

<mark style="color:red;">**POST**</mark> `/session/logout`

Log out from your Litmind account.

**Body**

<table><thead><tr><th>Name</th><th width="100">Type</th><th>Description</th></tr></thead><tbody><tr><td>userId</td><td>integer</td><td>The user id to be logged out.</td></tr></tbody></table>

**Example**

```bash
curl \
    -X POST https://litmind.com/api/v1/session/logout \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -d 'userId=138829'
```

**Response**

```json
{
    "isSuccess": true,
    "errorDescription": null
}
```

* <mark style="color:green;">**isSuccess**</mark> Whether the operation was performed successfully.
* <mark style="color:green;">**errorDescription**</mark> If there was an error, a description.

