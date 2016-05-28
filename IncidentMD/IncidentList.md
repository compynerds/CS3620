# List Incidents

----

* **URL**

    `/incidents`

* **Method:**

    `GET`

*  **URL Params**

    **Optional:**
 
    `fields=[uniqueID, type, action]`
    `limit=[integer]`
    `sort=[asc|desc]`
    `sort_by=[uniqueID|type|action]`
    `group_by=[type|action]`
  
* **Success Response:**
    * **Code:** 200
 
* **Error Response:**

    * **Code:** 401 UNAUTHORIZED

    * **Code:** 503 SERVICE UNAVAILABLE 
      **Content:** `{ "error": "Unavailable storage" }`

* **Sample Call:**

```
curl -X "GET" "http://api.example.com/incidents" \
	-H "Content-Type: application/json; charset=utf-8" \
	-H "Cache-Control: no-cache" \
	-H "Authorization: Basic YWRtaW46MHJ0cjBuMWNz" \
	-H "Accept: application/json"
```

* **Notes:**

    * The `sort` parameter defaults to `uniqueID`
    * The `sort_by` parameter defaults to `asc`
    * Response body:
    ```
    {
	    "count": 2,
	    "list": [
		    ["uniqueID", "type", "action"],
		    ["uniqueID01", "type", "action"]
	    ]
    }
    ```
