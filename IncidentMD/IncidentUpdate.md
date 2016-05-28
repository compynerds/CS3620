# Update Incident

----

* **URL**

    `/incidents`

* **Method:**

    `PUT`
  
* **Data Params**

```json
{
    "type": "type of incident",
    "content": "additional info for event",
    "action" : "what action is needed"
}

```

* **Success Response:**
    * **Code:** 200
 
* **Error Response:**

    * **Code:** 401 UNAUTHORIZED

    * **Code:** 422 UNPROCESSABLE ENTRY
      **Content:** `{ "error": "Invalid email" }`

    * **Code:** 503 SERVICE UNAVAILABLE 
      **Content:** `{ "error": "Unavailable storage" }`

* **Sample Call:**

```
curl -X "PUT" "http://api.example.com/incidents" \
	-H "Content-Type: application/json; charset=utf-8" \
	-H "Cache-Control: no-cache" \
	-H "Authorization: Basic YWRtaW46MHJ0cjBuMWNz" \
	-H "Accept: application/json" \
	-d $'{
    "type": "type of incident",
    "content": "additional info for event",
    "action" : "what action is needed"
}'

```