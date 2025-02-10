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

# Browse

<mark style="color:red;">**GET**</mark> `/profiles/browse`

Obtain a list of profiles of any type, including models and photographers.

#### Headers

<table><thead><tr><th width="177">Name</th><th>Value</th><th width="100" data-type="checkbox">Required</th><th data-hidden></th></tr></thead><tbody><tr><td><mark style="color:purple;"><strong>X-Key</strong></mark></td><td>Your API Key</td><td>true</td><td></td></tr><tr><td><mark style="color:purple;"><strong>X-SessionId</strong></mark></td><td>Your session id</td><td>true</td><td></td></tr><tr><td><mark style="color:purple;"><strong>X-UserId</strong></mark></td><td>The logged user id to browse profiles from</td><td>true</td><td></td></tr></tbody></table>

#### Body

<table><thead><tr><th width="174">Name</th><th>Description</th></tr></thead><tbody><tr><td><mark style="color:purple;"><strong>type</strong></mark></td><td><p>List only profiles of this type. One of the following values:</p><p><strong><code>photographers</code></strong> <strong><code>videographers</code></strong> <strong><code>retouchers</code></strong> <strong><code>models</code></strong> <strong><code>makeup</code></strong> <strong><code>hair</code></strong> <strong><code>stylist</code></strong> <strong><code>fashiondesigners</code></strong></p></td></tr><tr><td><mark style="color:purple;"><strong>country</strong></mark></td><td>List only profiles in the specified country, specified as an <a href="https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2">ISO 3166-1 alpha 2</a> standard code, e.g., <strong><code>ES</code></strong> for Spain.</td></tr><tr><td><mark style="color:purple;"><strong>region</strong></mark></td><td>List only profiles in a specific region of a country, specified as an <a href="https://en.wikipedia.org/wiki/ISO_3166-2">ISO 3166-2</a> standard code, e.g., <strong><code>ES-B</code></strong> for Barcelona.</td></tr><tr><td><mark style="color:purple;"><strong>level</strong></mark></td><td>List only experienced profiles or aspirants. One of the following values: <strong><code>experienced</code></strong> <strong><code>aspirant</code></strong><br><a href="https://litmind.com/help/howDoWeAssignLevel">How does Litmind determine whether a profile is experienced or aspirant?</a></td></tr><tr><td><mark style="color:purple;"><strong>isNew</strong></mark></td><td>Set to <strong><code>true</code></strong> to list only profiles that have recently joined Litmind.</td></tr><tr><td><mark style="color:purple;"><strong>isReviews</strong></mark></td><td>List only profiles with reviews</td></tr><tr><td><mark style="color:purple;"><strong>lightboxId</strong></mark></td><td>List only profiles you've added to one of your lightboxes</td></tr><tr><td><mark style="color:purple;"><strong>page</strong></mark></td><td>The results page to obtain. If not specified, the first page is obtained.</td></tr></tbody></table>

When searching for models, the following additional parameters can be specified:

<table data-header-hidden><thead><tr><th width="174">Name</th><th>Description</th></tr></thead><tbody><tr><td><mark style="color:purple;"><strong>gender</strong></mark></td><td><p>List only models of a certain gender, one of the following values:</p><p><strong><code>man</code></strong> <strong><code>woman</code></strong> <strong><code>nonBinary</code></strong></p></td></tr><tr><td><mark style="color:purple;"><strong>ageMin</strong></mark></td><td>List only models who are at least this years old</td></tr><tr><td><mark style="color:purple;"><strong>ageMax</strong></mark></td><td>List only models who are at most this years old</td></tr><tr><td><mark style="color:purple;"><strong>heightMin</strong></mark></td><td>List only models who are at least this tall</td></tr><tr><td><mark style="color:purple;"><strong>heightMax</strong></mark></td><td>List only models who are at most this tall</td></tr><tr><td><mark style="color:purple;"><strong>sizeClothingMin</strong></mark></td><td>List only models with a minimum clothing size</td></tr><tr><td><mark style="color:purple;"><strong>sizeClothingMax</strong></mark></td><td>List only models with a maximum clothing size</td></tr><tr><td><mark style="color:purple;"><strong>sizeShoesMin</strong></mark></td><td>List only models with a minimum shoe size</td></tr><tr><td><mark style="color:purple;"><strong>sizeShoesMax</strong></mark></td><td>List only models with a maximum shoe size</td></tr><tr><td><mark style="color:purple;"><strong>sizeChestMin</strong></mark></td><td>List only models with a minimum chest size</td></tr><tr><td><mark style="color:purple;"><strong>sizeChestMax</strong></mark></td><td>List only models with a maximum chest size</td></tr><tr><td><mark style="color:purple;"><strong>sizeWaistMin</strong></mark></td><td>List only models with a minimum waist size</td></tr><tr><td><mark style="color:purple;"><strong>sizeWaistMax</strong></mark></td><td>List only models with a maximum waist size</td></tr><tr><td><mark style="color:purple;"><strong>sizeHipsMin</strong></mark></td><td>List only models with a minimum hips size</td></tr><tr><td><mark style="color:purple;"><strong>sizeHipsMax</strong></mark></td><td>List only models with a maximum hips size</td></tr><tr><td><mark style="color:purple;"><strong>eyesColor</strong></mark></td><td><p>List only models with a certain eye color. One or more of the following values, separated with commas:</p><p><strong><code>black</code></strong> <strong><code>brown</code></strong> <strong><code>blue</code></strong> <strong><code>green</code></strong> <strong><code>lightBrown</code></strong></p></td></tr><tr><td><mark style="color:purple;"><strong>hairColor</strong></mark></td><td><p>List only models with a certain hair color. One or more of the following values, separated with commas:</p><p><strong><code>black</code></strong> <strong><code>brown</code></strong> <strong><code>blonde</code></strong> <strong><code>ginger</code></strong> <strong><code>other</code></strong></p></td></tr><tr><td><mark style="color:purple;"><strong>hairStyle</strong></mark></td><td><p>List only models with a certain hair style. One or more of the following values, separated with commas:</p><p><strong><code>longStraight</code></strong> <strong><code>longCurly</code></strong> <strong><code>shortStraight</code></strong> <strong><code>shortCurly</code></strong> <strong><code>veryShort</code></strong></p></td></tr><tr><td><mark style="color:purple;"><strong>peculiarities</strong></mark></td><td><p>List only models with certain peculiarities. One or more of the following values, separated with commas:</p><p><strong><code>freckles</code></strong> <strong><code>tattoos</code></strong> <strong><code>piercings</code></strong> <strong><code>dancing</code></strong> <strong><code>skating</code></strong> <strong><code>horseRiding</code></strong></p></td></tr><tr><td><mark style="color:purple;"><strong>isPolaroids</strong></mark></td><td>List only models with polaroids</td></tr></tbody></table>

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
    -G https://litmind.com/api/v1/profiles/browse \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ' \
    -H 'X-SessionId: 313599f212429860887ef23ea326cc863a9186eb1a43a8f1739a1815ebe2a588' \
    -H 'X-UserId: 138829'
    -d 'status=accepted&ageMin=22&eyesColor=black,brown,lightBrown'
```

#### Response

<pre class="language-json" data-full-width="false"><code class="lang-json"><strong>{
</strong>    "entity": "Profiles",
    "paging": {
<strong>        "page": 1,
</strong>        "entitiesPerPage": 10,
        "totalPages": 1485,
        "totalEntities": 14842,
        "entitiesThisPage": 10
    },
    "profiles": [
        {
            "entity": "Profile",
            "id": 8492881,
            "joined": "2025-01-20T08:56:48+00:00",
            "accepted": "2025-01-20T17:03:37+00:00",
            "folder": {
                "id": 4039,
                "name": "Liked by the client"
            },
            "profile": &#x3C;Profile entity>
        }
    ]
}
</code></pre>

