# Postings

<mark style="color:red;">**GET**</mark> `/account/noticeboard/postings`

Obtain a list of castings, collaborations or other kinds of noticeboard postings that are currently running in one of your accounts.

{% hint style="info" %}
On Litmind, castings, collaborations and other similar kinds of postings are considered all noticeboard postings.&#x20;
{% endhint %}

#### Headers

<table><thead><tr><th width="172">Name</th><th>Value</th><th width="100" data-type="checkbox">Required</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:yellow;"><strong>X-Key</strong></mark></td><td>Your API Key</td><td>true</td><td></td></tr><tr><td><mark style="color:yellow;"><strong>X-SessionId</strong></mark></td><td>Your session id</td><td>true</td><td></td></tr><tr><td><mark style="color:yellow;"><strong>X-UserId</strong></mark></td><td>The logged user id to list noticeboard items from</td><td>true</td><td></td></tr></tbody></table>

#### Body

<table><thead><tr><th width="169">Name</th><th>Description</th><th width="100" data-type="checkbox">Required</th></tr></thead><tbody><tr><td><mark style="color:yellow;"><strong>postingType</strong></mark></td><td><p>One of the following types of noticeboard postings to retrieve:</p><p><strong><code>casting</code></strong> <strong><code>collaboration</code></strong> <strong><code>travelNotice</code></strong> <strong><code>others</code></strong></p></td><td>true</td></tr><tr><td><mark style="color:yellow;"><strong>status</strong></mark></td><td><p>Obtain a list of open or closed noticeboard postings. If not specified, the list will include all. One of the following values:</p><p><strong><code>open</code></strong> <strong><code>closed</code></strong></p></td><td>false</td></tr></tbody></table>

#### Example

```bash
curl \
    -G https://litmind.com/api/v1/account/noticeboard/postings \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -H 'X-SessionId: 313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588' \
    -H 'X-UserId: 138829'
    -d 'postingType=casting'
```

#### Response

```json
{
    "count": 1,
    "noticeboardPostings": [
        {
            "id": 38922,
            "title": "Models wanted for a magazine editorial",
            "section": "Castings",
            "type": "Photo shoots",
            "created": "2025-01-19T08:19:27+00:00",
            "published": "2025-01-19T08:28:43+00:00",
            "end": "2025-02-03T00:59:59+00:00",
            "lifespanDays": 14,
            "isPaid": true,
            "isRequiredExperience": false,
            "isCommercialUsage": 0,
            "isTfp": false,
            "url": "https://litmind.es.buzz/tablon/casting/models-wanted-for-a-magazine-editorial",
            "urlManager": "https://litmind.es.buzz/group/models-wanted-for-a-magazine-editorial",
            "urlEdit": "https://litmind.es.buzz/?a=50&aa=60&noticeboard_ad_id=38922",
            "urlStatistics": "https://litmind.es.buzz/account/stats/custom/casting/38922/20250119/20250203",
            "isManager": true,
            "candidatesAccepted": 4,
            "candidatesPending": 22,
            "views": 180,
            "folders": [
                {
                    "id": 4039,
                    "name": "Liked by the client"
                },
                {
                    "id": 4040,
                    "name": "Pending signing"
                }
            ]
        }
    ]
}
```

