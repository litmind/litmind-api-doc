# Lightboxes contents

<mark style="color:red;">**GET**</mark> `/account/lightboxes/`<mark style="color:yellow;">**`{lightboxId}`**</mark>`/contents`

Obtain a list of the items inside one of your lightboxes.

#### Headers

<table><thead><tr><th width="177">Name</th><th>Value</th><th width="100" data-type="checkbox">Required</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:yellow;"><strong>X-Key</strong></mark></td><td>Your API Key</td><td>true</td><td></td></tr><tr><td><mark style="color:yellow;"><strong>X-SessionId</strong></mark></td><td>Your session id</td><td>true</td><td></td></tr><tr><td><mark style="color:yellow;"><strong>X-UserId</strong></mark></td><td>The logged user id to list lightbox contents from</td><td>true</td><td></td></tr></tbody></table>

#### Body

<table><thead><tr><th width="174">Name</th><th>Description</th></tr></thead><tbody><tr><td><mark style="color:yellow;"><strong>page</strong></mark></td><td>The results page to obtain. If not specified, the first page is obtained.</td></tr></tbody></table>

#### Example

```bash
curl \
    -G https://litmind.com/api/v1/account/lightboxes/388391/contents \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -H 'X-SessionId: 313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588' \
    -H 'X-UserId: 138829'
    -d 'status=accepted&ageMin=22&eyesColor=black,brown,lightBrown&isPolaroids=true'
```

#### Response

```json
{
    "entity": "LightboxItems",
    "paging": {
        "page": 1,
        "entitiesPerPage": 10,
        "totalPages": 2,
        "totalEntities": 18,
        "entitiesThisPage": 10
    },
    "lightboxItems": [
        <LightboxItem entities>
    ]
}
```

{% hint style="info" %}
See the [LightboxItem](../../entities/lightboxitem.md) entity
{% endhint %}
