# Candidates

<mark style="color:red;">**GET**</mark> `/account/noticeboard/`<mark style="color:yellow;">**`{noticeboardPostingId}`**</mark>`/candidates`

Obtain a list of candidates in one of your castings, collaborations or another kind of noticeboard postings working with the candidates manager.

#### Headers

<table><thead><tr><th width="177">Name</th><th>Value</th><th width="100" data-type="checkbox">Required</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:yellow;"><strong>X-Key</strong></mark></td><td>Your API Key</td><td>true</td><td></td></tr><tr><td><mark style="color:yellow;"><strong>X-SessionId</strong></mark></td><td>Your session id</td><td>true</td><td></td></tr><tr><td><mark style="color:yellow;"><strong>X-UserId</strong></mark></td><td>The logged user id to list noticeboard items from</td><td>true</td><td></td></tr></tbody></table>

#### Body

<table><thead><tr><th width="174">Name</th><th>Description</th></tr></thead><tbody><tr><td><mark style="color:yellow;"><strong>status</strong></mark></td><td><p>List only candidates that have been accepted for the casting/collaboration, or those who haven't yet been accepted nor declined. If not specified, the list will include both. One of the following values:</p><p><strong><code>accepted</code></strong> <strong><code>pending</code></strong></p></td></tr><tr><td><mark style="color:yellow;"><strong>gender</strong></mark></td><td><p>List only candidates of a certain gender, one of the following values:</p><p><strong><code>man</code></strong> <strong><code>woman</code></strong> <strong><code>nonBinary</code></strong></p></td></tr><tr><td><mark style="color:yellow;"><strong>ageMin</strong></mark></td><td>List only candidates who are at least this years old</td></tr><tr><td><mark style="color:yellow;"><strong>ageMax</strong></mark></td><td>List only candidates who are at most this years old</td></tr><tr><td><mark style="color:yellow;"><strong>heightMin</strong></mark></td><td>List only candidates who are at least this tall, in centimeters</td></tr><tr><td><mark style="color:yellow;"><strong>heightMax</strong></mark></td><td>List only candidates who are at most this tall, in centimeters</td></tr><tr><td><mark style="color:yellow;"><strong>eyesColor</strong></mark></td><td><p>List only candidates with a certain eye color. One or more of the following values, separated with commas:</p><p><strong><code>black</code></strong> <strong><code>brown</code></strong> <strong><code>blue</code></strong> <strong><code>green</code></strong> <strong><code>lightBrown</code></strong></p></td></tr><tr><td><mark style="color:yellow;"><strong>hairColor</strong></mark></td><td><p>List only candidates with a certain hair color. One or more of the following values, separated with commas:</p><p><strong><code>black</code></strong> <strong><code>brown</code></strong> <strong><code>blonde</code></strong> <strong><code>ginger</code></strong> <strong><code>other</code></strong></p></td></tr><tr><td><mark style="color:yellow;"><strong>hairStyle</strong></mark></td><td><p>List only candidates with a certain hair style. One or more of the following values, separated with commas:</p><p><strong><code>longStraight</code></strong> <strong><code>longCurly</code></strong> <strong><code>shortStraight</code></strong> <strong><code>shortCurly</code></strong> <strong><code>veryShort</code></strong></p></td></tr><tr><td><mark style="color:yellow;"><strong>peculiarities</strong></mark></td><td><p>List only candidates with certain peculiarities. One or more of the following values, separated with commas:</p><p><strong><code>freckles</code></strong> <strong><code>tatoos</code></strong> <strong><code>piercings</code></strong> <strong><code>dance</code></strong> <strong><code>skate</code></strong> <strong><code>horseRiding</code></strong></p></td></tr></tbody></table>

#### Example

```bash
curl \
    -G https://litmind.com/api/v1/account/noticeboard/38922/candidates \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -H 'X-SessionId: 313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588' \
    -H 'X-UserId: 138829'
    -d 'status=accepted&ageMin=22&eyesColor=black,brown,lightBrown'
```

#### Response

```json
{
    "count": 1,
    "candidates": [
        {
            "id": 8492881,
            "joined": "2025-01-20T08:56:48+00:00",
            "profile": {
                "id": 48129,
                "profileImageUrl": "https://cdn.litmind.com/bix2ePMqWHWh4F8cnEie0S2Jqw7uiGpE.PhotoSingleImage.3465915.profile.jpg",
                "username": "frank-abagnale",
                "typeTitle": "Model",
                "isVerified": false,
                "isNew": false,
                "isRepresented": false,
                "isStaffPick": false,
                "isBanned": false,
                "profileUrl": "https://litmind.com/frankabagnale",
                "reviewsUrl": "https://litmind.com/frankabagnale/reviews",
                "sedCardUrl": "https://litmind.com/frankabagnale/composite",
                "polaroidsUrl": "https://litmind.com/frankabagnale/polaroids",
                "views": 21531,
                "clicks": 2803,
                "followers": 67,
                "reviews": 0,
                "stars": 0,
                "artworks": 6,
                "artworkViews": 49,
                "artworkClicks": 7,
                "slides": 0,
                "publicLightboxes": 0,
                "polaroids": 0,
                "isRecentPolaroids": false,
                "isSedCard": false
            }
        }
    ]
}
```

