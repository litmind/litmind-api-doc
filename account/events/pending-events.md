# Pending events

<mark style="color:red;">**GET**</mark> `/account/events/pending`

Obtain the number of events in your account that require your attention. For example: The number of models that have requested accessing your castings but you haven't yet approved or declined.

#### Headers

<table><thead><tr><th width="181">Name</th><th>Value</th><th width="100" data-type="checkbox">Required</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:yellow;"><strong>X-Key</strong></mark></td><td>Your API Key</td><td>true</td><td></td></tr><tr><td><mark style="color:yellow;"><strong>X-SessionId</strong></mark></td><td>Your session id</td><td>true</td><td></td></tr><tr><td><mark style="color:yellow;"><strong>X-UserId</strong></mark></td><td>The logged user id to get pending events from</td><td>true</td><td></td></tr></tbody></table>

#### Example

```bash
curl \
    -G https://litmind.com/api/v1/account/events/pending \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -H 'X-SessionId: 313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588' \
    -H 'X-UserId: 138829'
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

