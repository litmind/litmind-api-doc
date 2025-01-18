# List

<mark style="color:red;">**GET**</mark> `/session/list`

Obtain a list of the users you've currently logged in within your session.

{% hint style="info" %}
If you've logged in into multiple accounts within the same session, you're able to specify the **userId** of the account you want to operate with when calling other endpoints.
{% endhint %}

**Example**

```bash
curl \
    -G https://litmind.com/api/v1/session/list \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ'
```

**Response**

```json
{
    "count": 1,
    "sessionUsers": [
        {
            "userId": 193978,
            "isCurrent": true
        }
    ]
}
```



