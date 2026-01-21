---
icon: bullseye-arrow
---

# Making a request

API requests are done via HTTPS requests to <mark style="color:red;">**litmind.com/api/v1**</mark>, with the following header:

* <mark style="color:purple;">**X-Key**</mark> Your API key

This is an example of a simple request:

```bash
curl \
    -G https://litmind.com/api/v1/status/version \
    -H 'X-Key: bfRCu5GAEP9eMZ7fS6yvPwGxB9Nu7FzUfdnasrCkKkHAyCBZ'
```

The API will respond with a standard HTTP code indicating the status of the request and a JSON body. Here's an example:

```json
{
    "entity": "Version",
    "availableVersions": [
        "1"
    ],
    "requestVersion": "1",
    "latestVersion": "1"
}
```

## Requesting user endpoints

Simple endpoints like the example above are not very helpful. The important endpoints that allow you to operate on Litmind using the API will additionally require you to create a session and send the <mark style="color:purple;">**X-SessionId**</mark> and <mark style="color:purple;">**X-UserId**</mark> additional headers along with your requests.

Advance to the next section to learn how to create a session and start requesting an endpoint:
