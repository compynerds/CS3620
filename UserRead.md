# Read User 

----

* **URL**

    `/users`

* **Method:**

    `GET`
  
* **Success Response:**
    * **Code:** 200
 
* **Error Response:**

    * **Code:** 401 UNAUTHORIZED

    * **Code:** 503 SERVICE UNAVAILABLE 
      **Content:** `{ "error": "Unavailable storage" }`

* **Sample Call:**

```
curl -X "GET" "http://api.example.com/users" \
	-H "Content-Type: application/json; charset=utf-8" \
	-H "Cache-Control: no-cache" \
	-H "Authorization: Basic YWRtaW46MHJ0cjBuMWNz" \
	-H "Accept: application/json"
	-d $'{
    		"username": "username12",
	}'

```

* **Notes:**

    * Response body:
    ```
    {
	"Mobile": "123-456-7890",
	"name": "user's full name",
	"email": "user@user.com",
	"username": "username",
	
    }
    ```
