# Read Event

----

* **URL**

    `/events`

* **Method:**

    `GET`
  

* **Success Response:**
    * **Code:** 201
 
* **Error Response:**

    * **Code:** 401 UNAUTHORIZED

    * **Code:** 422 UNPROCESSABLE ENTRY
      **Content:** `{ "error": "Invalid type" }`

    * **Code:** 503 SERVICE UNAVAILABLE 
      **Content:** `{ "error": "Unavailable storage" }`

* **Sample Call:**

```
curl -X "POST" "http://api.example.com/events" \
	-H "Content-Type: application/json; charset=utf-8" \
	-H "Cache-Control: no-cache" \
	-H "Authorization: Basic YWRtaW46MHJ0cjBuMWNz" \
	-H "Accept: application/json" \
	-d $'{
    "uniqueID": "something"
}'

```

* **Notes:**

    * Response body:
    ```
	{
 	   "uniqueID": "something",
  	   "type": "type of event",
  	   "content": "additional info for event",
  	   "action" : "what action is needed"
	}
    ```

