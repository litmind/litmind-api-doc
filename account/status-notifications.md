# Status / notifications

<mark style="color:red;">**GET**</mark> `/account/status/notifications`

Obtain a list of pending notifications in your account. For example: The number of models that have requested accessing your castings but you haven't yet approved or declined.

**Example**

```bash
curl \
    -G https://litmind.com/api/v1/account/status/notifications \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ'
```

**Response**

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

