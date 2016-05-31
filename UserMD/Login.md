# Login User

----

* **URL**

    `/login`

* **Method:**

    `POST`
  
* **Data Params**

```json
{
    "username": "username12",
    "password": "1234password",
    "time": "24:00.00"
}

```

* **Success Response:**
    * **Code:** 201
 
* **Error Response:**

    * **Code:** 401 UNAUTHORIZED

    * **Code:** 422 UNPROCESSABLE ENTRY
      **Content:** `{ "error": "Invalid email" }`

    * **Code:** 503 SERVICE UNAVAILABLE 
      **Content:** `{ "error": "Unavailable storage" }`

* **Sample Call:**

```
curl -X "POST" "http://api.example.com/login" \
	-H "Content-Type: application/json; charset=utf-8" \
	-H "Cache-Control: no-cache" \
	-H "Authorization: Basic YWRtaW46MHJ0cjBuMWNz" \
	-H "Accept: application/json" \
	-d $'{
    "username": "username12",
    "password": "1234password"
}'



```