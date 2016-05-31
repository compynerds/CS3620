# Authenticate User

----

* **URL**

    `/auth`

* **Method:**

    `POST`
  
* **Data Params**

```json
{
	"auth": "authCode123"
}

```

* **Success Response:**
    * **Code:** 201
 
* **Error Response:**

    * **Code:** 401 UNAUTHORIZED

    * **Code:** 422 UNPROCESSABLE ENTRY
      **Content:** `{ "error": "Invalid auth code" }`

    * **Code:** 503 SERVICE UNAVAILABLE 
      **Content:** `{ "error": "Unavailable storage" }`

* **Sample Call:**

```
curl -X "POST" "http://api.example.com/auth" \
	-H "Content-Type: application/json; charset=utf-8" \
	-H "Cache-Control: no-cache" \
	-H "Authorization: Basic YWRtaW46MHJ0cjBuMWNz" \
	-H "Accept: application/json" \
	-d $'{
	"auth": "authCode123"
}'



```