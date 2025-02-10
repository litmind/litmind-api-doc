---
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
---

# Logout

<mark style="color:red;">**POST**</mark> `/session/logout`

Log out from your Litmind account.

#### Headers

<table><thead><tr><th width="186">Name</th><th>Value</th><th width="100" data-type="checkbox">Required</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:purple;"><strong>X-Key</strong></mark></td><td>Your API Key</td><td>true</td><td></td></tr><tr><td><mark style="color:purple;"><strong>X-SessionId</strong></mark></td><td>Your session id</td><td>true</td><td></td></tr></tbody></table>

#### Body

<table><thead><tr><th width="187">Name</th><th>Description</th><th width="100" data-type="checkbox">Required</th></tr></thead><tbody><tr><td><mark style="color:purple;"><strong>userId</strong></mark></td><td>The user id to be logged out</td><td>true</td></tr></tbody></table>

#### Example

```bash
curl \
    -X POST https://litmind.com/api/v1/session/logout \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -H 'X-SessionId: 313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588' \
    -d 'userId=138829'
```

#### Response

```json
{
    "isSuccess": true,
    "errorDescription": null
}
```

* <mark style="color:blue;">**isSuccess**</mark> Whether the operation was performed successfully.
* <mark style="color:blue;">**errorDescription**</mark> If there was an error, a description.

