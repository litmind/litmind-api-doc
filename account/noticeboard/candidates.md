# Candidates

<mark style="color:red;">**GET**</mark> `/account/noticeboard/candidates`

Obtain a list of candidates in a casting, collaboration or another kind of noticeboard posting.

#### Headers

<table><thead><tr><th>Name</th><th width="100" data-type="checkbox">Required</th><th>Value</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:yellow;"><strong>X-Key</strong></mark></td><td>true</td><td>Your API Key</td><td></td></tr><tr><td><mark style="color:yellow;"><strong>X-SessionId</strong></mark></td><td>true</td><td>Your session id</td><td></td></tr><tr><td><mark style="color:yellow;"><strong>X-UserId</strong></mark></td><td>true</td><td>The logged user id to list noticeboard items from</td><td></td></tr></tbody></table>

#### Body

<table><thead><tr><th>Name</th><th width="100" data-type="checkbox">Required</th><th>Description</th></tr></thead><tbody><tr><td><mark style="color:yellow;"><strong>postingType</strong></mark></td><td>true</td><td>One of the following types of noticeboard postings to retrieve: <code>casting</code> <code>collaboration</code> <code>travelnotice</code> <code>others</code></td></tr></tbody></table>

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
    "pendingReviews": 0,
    "pendingSubmissions": 0,
    "pendingCastingCandidates": 6,
    "pendingCollaborationCandidates": 0,
    "pendingGroupMembers": 0,
    "pendingProjectQuotations": 0,
    "pendingNotifications": 3,
    "pendingMessengerMessages": 5
}
```

