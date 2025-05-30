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

<mark style="color:red;">**GET**</mark> `/account/noticeboard/list`

Obtain a list of castings, collaborations or other kinds of noticeboard postings that are currently running in one of your accounts.

{% hint style="info" %}
On Litmind, castings, collaborations and other similar kinds of postings are considered all noticeboard postings.&#x20;
{% endhint %}

#### Headers

<table><thead><tr><th width="172">Name</th><th>Value</th><th width="100" data-type="checkbox">Required</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:purple;"><strong>X-Key</strong></mark></td><td>Your API Key</td><td>true</td><td></td></tr><tr><td><mark style="color:purple;"><strong>X-SessionId</strong></mark></td><td>Your session id</td><td>true</td><td></td></tr><tr><td><mark style="color:purple;"><strong>X-UserId</strong></mark></td><td>The logged user id to list noticeboard items from</td><td>true</td><td></td></tr></tbody></table>

#### Body

<table><thead><tr><th width="169">Name</th><th>Description</th><th width="100" data-type="checkbox">Required</th></tr></thead><tbody><tr><td><mark style="color:purple;"><strong>postingType</strong></mark></td><td><p>One of the following types of noticeboard postings to retrieve:</p><p><strong><code>casting</code></strong> <strong><code>collaboration</code></strong> <strong><code>travelNotice</code></strong> <strong><code>others</code></strong></p></td><td>true</td></tr><tr><td><mark style="color:purple;"><strong>status</strong></mark></td><td><p>Obtain a list of open or closed noticeboard postings. If not specified, the list will include all. One of the following values:</p><p><strong><code>open</code></strong> <strong><code>closed</code></strong></p></td><td>false</td></tr></tbody></table>

#### Example

```bash
curl \
    -G https://litmind.com/api/v1/account/noticeboard/list \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -H 'X-SessionId: 313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588' \
    -H 'X-UserId: 138829'
    -d 'postingType=casting'
```

#### Response

```json
{
    "entity": "NoticeboardPostings",
    "noticeboardPostings": [
        // Noticeboard posting entities
    ]
}
```

