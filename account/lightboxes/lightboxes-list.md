# Lightboxes list

<mark style="color:red;">**GET**</mark> `/account/lightboxes/list`

Obtain a list of your lightboxes

#### Headers

<table><thead><tr><th width="172">Name</th><th>Value</th><th width="100" data-type="checkbox">Required</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:purple;"><strong>X-Key</strong></mark></td><td>Your API Key</td><td>true</td><td></td></tr><tr><td><mark style="color:purple;"><strong>X-SessionId</strong></mark></td><td>Your session id</td><td>true</td><td></td></tr><tr><td><mark style="color:purple;"><strong>X-UserId</strong></mark></td><td>The logged user id to list lightboxes items from</td><td>true</td><td></td></tr></tbody></table>

#### Example

```bash
curl \
    -G https://litmind.com/api/v1/account/lightboxes/list \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -H 'X-SessionId: 313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588' \
    -H 'X-UserId: 138829'
```

#### Response

```json
{
    "entity": "Lightboxes",
    "lightboxes": [
        <Lightbox entities>
    ]
}
```

{% hint style="info" %}
See the [Lightbox](../../entities/lightbox.md) entity
{% endhint %}
