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

# Pending events

<mark style="color:red;">**GET**</mark> `/account/events/pending`

Obtain the number of events in your account that require your attention. For example: The number of models that have requested accessing your castings but you haven't yet approved or declined.

#### Headers

<table><thead><tr><th width="181">Name</th><th>Value</th><th width="100" data-type="checkbox">Required</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:purple;"><strong>X-Key</strong></mark></td><td>Your API Key</td><td>true</td><td></td></tr><tr><td><mark style="color:purple;"><strong>X-SessionId</strong></mark></td><td>Your session id</td><td>true</td><td></td></tr><tr><td><mark style="color:purple;"><strong>X-UserId</strong></mark></td><td>The logged user id to get pending events from</td><td>true</td><td></td></tr></tbody></table>

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
    "entity": "PendingEvents",
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

<table><thead><tr><th width="320">Name</th><th>Value</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:purple;"><strong>pendingReviews</strong></mark></td><td>The number of reviews written about you that are waiting for your approval</td><td></td></tr><tr><td><mark style="color:purple;"><strong>pendingSubmissions</strong></mark></td><td>The number of publication submissions you've received that are waiting for your approval</td><td></td></tr><tr><td><mark style="color:purple;"><strong>pendingCastingCandidates</strong></mark></td><td>The number of candidates in your castings that are waiting for your approval</td><td></td></tr><tr><td><mark style="color:purple;"><strong>pendingCollaborationCandidates</strong></mark></td><td>The number of candidates in your collaborations that are waiting for your approval</td><td></td></tr><tr><td><mark style="color:purple;"><strong>pendingGroupMembers</strong></mark></td><td>The number of members in your groups that are waiting for your access approval</td><td></td></tr><tr><td><mark style="color:purple;"><strong>pendingProjectQuotations</strong></mark></td><td>The number of photographers that are waiting for your approval to enter your projects and send their quotations</td><td></td></tr><tr><td><mark style="color:purple;"><strong>pendingNotifications</strong></mark></td><td>The number of unread notifications; e.g., comments your received, or places where you've been mentioned</td><td></td></tr><tr><td><mark style="color:purple;"><strong>pendingMessengerMessages</strong></mark></td><td>The number of unread messages in your messenger</td><td></td></tr></tbody></table>
