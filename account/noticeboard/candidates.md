# Candidates

<mark style="color:red;">**GET**</mark> `/account/noticeboard/`<mark style="color:yellow;">**`{noticeboardPostingId}`**</mark>`/candidates`

Obtain a list of candidates in one of your castings, collaborations or another kind of noticeboard postings working with the candidates manager.

#### Headers

<table><thead><tr><th width="177">Name</th><th>Value</th><th width="100" data-type="checkbox">Required</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:yellow;"><strong>X-Key</strong></mark></td><td>Your API Key</td><td>true</td><td></td></tr><tr><td><mark style="color:yellow;"><strong>X-SessionId</strong></mark></td><td>Your session id</td><td>true</td><td></td></tr><tr><td><mark style="color:yellow;"><strong>X-UserId</strong></mark></td><td>The logged user id to list noticeboard items from</td><td>true</td><td></td></tr></tbody></table>

#### Body

<table><thead><tr><th width="174">Name</th><th>Description</th></tr></thead><tbody><tr><td><mark style="color:yellow;"><strong>status</strong></mark></td><td><p>List only candidates that have been accepted for the casting/collaboration, or those who haven't yet been accepted nor declined. If not specified, the list will include both. One of the following values:</p><p><strong><code>accepted</code></strong> <strong><code>pending</code></strong></p></td></tr><tr><td><mark style="color:yellow;"><strong>gender</strong></mark></td><td><p>List only models of a certain gender, one of the following values:</p><p><strong><code>man</code></strong> <strong><code>woman</code></strong> <strong><code>nonBinary</code></strong></p></td></tr><tr><td><mark style="color:yellow;"><strong>ageMin</strong></mark></td><td>List only models who are at least this years old</td></tr><tr><td><mark style="color:yellow;"><strong>ageMax</strong></mark></td><td>List only models who are at most this years old</td></tr><tr><td><mark style="color:yellow;"><strong>heightMin</strong></mark></td><td>List only models who are at least this tall</td></tr><tr><td><mark style="color:yellow;"><strong>heightMax</strong></mark></td><td>List only models who are at most this tall</td></tr><tr><td><mark style="color:yellow;"><strong>sizeClothingMin</strong></mark></td><td>List only models with a minimum clothing size</td></tr><tr><td><mark style="color:yellow;"><strong>sizeClothingMax</strong></mark></td><td>List only models with a maximum clothing size</td></tr><tr><td><mark style="color:yellow;"><strong>sizeShoesMin</strong></mark></td><td>List only models with a minimum shoe size</td></tr><tr><td><mark style="color:yellow;"><strong>sizeShoesMax</strong></mark></td><td>List only models with a maximum shoe size</td></tr><tr><td><mark style="color:yellow;"><strong>sizeChestMin</strong></mark></td><td>List only models with a minimum chest size</td></tr><tr><td><mark style="color:yellow;"><strong>sizeChestMax</strong></mark></td><td>List only models with a maximum chest size</td></tr><tr><td><mark style="color:yellow;"><strong>sizeWaistMin</strong></mark></td><td>List only models with a minimum waist size</td></tr><tr><td><mark style="color:yellow;"><strong>sizeWaistMax</strong></mark></td><td>List only models with a maximum waist size</td></tr><tr><td><mark style="color:yellow;"><strong>sizeHipsMin</strong></mark></td><td>List only models with a minimum hips size</td></tr><tr><td><mark style="color:yellow;"><strong>sizeHipsMax</strong></mark></td><td>List only models with a maximum hips sizes</td></tr><tr><td><mark style="color:yellow;"><strong>eyesColor</strong></mark></td><td><p>List only models with a certain eye color. One or more of the following values, separated with commas:</p><p><strong><code>black</code></strong> <strong><code>brown</code></strong> <strong><code>blue</code></strong> <strong><code>green</code></strong> <strong><code>lightBrown</code></strong></p></td></tr><tr><td><mark style="color:yellow;"><strong>hairColor</strong></mark></td><td><p>List only models with a certain hair color. One or more of the following values, separated with commas:</p><p><strong><code>black</code></strong> <strong><code>brown</code></strong> <strong><code>blonde</code></strong> <strong><code>ginger</code></strong> <strong><code>other</code></strong></p></td></tr><tr><td><mark style="color:yellow;"><strong>hairStyle</strong></mark></td><td><p>List only models with a certain hair style. One or more of the following values, separated with commas:</p><p><strong><code>longStraight</code></strong> <strong><code>longCurly</code></strong> <strong><code>shortStraight</code></strong> <strong><code>shortCurly</code></strong> <strong><code>veryShort</code></strong></p></td></tr><tr><td><mark style="color:yellow;"><strong>peculiarities</strong></mark></td><td><p>List only models with certain peculiarities. One or more of the following values, separated with commas:</p><p><strong><code>freckles</code></strong> <strong><code>tattoos</code></strong> <strong><code>piercings</code></strong> <strong><code>dancing</code></strong> <strong><code>skating</code></strong> <strong><code>horseRiding</code></strong></p></td></tr><tr><td><mark style="color:yellow;"><strong>isPolaroids</strong></mark></td><td>List only models with polaroids</td></tr><tr><td><mark style="color:yellow;"><strong>isReviews</strong></mark></td><td>List only profiles with reviews</td></tr></tbody></table>

{% hint style="info" %}
Sizes like chest, waist, hips and heights are specified in centimeters
{% endhint %}

{% hint style="info" %}
Clothing sizes are specified in European standard. These are the accepted values:

* For men: **`40`** **`42`** **`44`** **`46`** **`48`** **`50`** **`52`** **`54`** **`56`** **`58`** **`60`**
* For women: **`34`** **`36`** **`38`** **`40`** **`42`** **`44`** **`46`** **`48`** **`50`** **`52`** **`54`** **`56`**
{% endhint %}

{% hint style="info" %}
Shoe sizes are specified in European standard. These are the accepted values:

* For men, from **`38`** to **`48`**
* For women, from **`35`** to **`46`**
{% endhint %}

#### Example

```bash
curl \
    -G https://litmind.com/api/v1/account/noticeboard/38922/candidates \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -H 'X-SessionId: 313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588' \
    -H 'X-UserId: 138829'
    -d 'status=accepted&ageMin=22&eyesColor=black,brown,lightBrown&isPolaroids=true'
```

#### Response

```json
{
    "count": 1,
    "candidates": [
        {
            "id": 8492881,
            "joined": "2025-01-20T08:56:48+00:00",
            "accepted": "2025-01-20T17:03:37+00:00",
            "folder": {
                "id": 4039,
                "name": "Liked by the client"
            },
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

