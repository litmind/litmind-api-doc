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

# List

<mark style="color:red;">**GET**</mark> `/session/list`

Obtain a list of the users you've currently logged in within your session.

{% hint style="info" %}
If you've logged in into multiple accounts within the same session, you're able to specify the **userId** of the account you want to operate with when calling other endpoints.
{% endhint %}

#### Headers

<table><thead><tr><th width="191">Name</th><th>Value</th><th width="100" data-type="checkbox">Required</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:yellow;"><strong>X-Key</strong></mark></td><td>Your API Key</td><td>true</td><td></td></tr><tr><td><mark style="color:yellow;"><strong>X-SessionId</strong></mark></td><td>Your session id</td><td>true</td><td></td></tr></tbody></table>

#### Example

```bash
curl \
    -G https://litmind.com/api/v1/session/list \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -H 'X-SessionId: 313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588'
```

#### Response

```json
{
    "entity": "SessionUsers",
    "sessionUsers": [
        {
            "entity": "SessionUser",
            "userId": 193978,
            "isCurrent": true
        }
    ]
}
```

