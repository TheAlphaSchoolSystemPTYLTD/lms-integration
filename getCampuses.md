**getCampuses**
----
  Returns an array of structured Teacher data comprising timetable details in JSON format.
  
* **Version History:**

  TASS v52.5 - Method Added

* **Version:**

  3

* **Permission:**

  Student Records > Student Records Setup > Campuses Tab > View

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**
 
  `codeonly [boolean]` - Return Code only. Must be 'true' or 'false' (MUST be a String).

   **Optional:**

  none

   **Conditional:**

  none

* **Success Response:**

    ```javascript
      {
        "campuses": [
            {
              "code": "JU",
              "desc": "Junior School (Billabong Road)"
            },
            {
              "code": "SE",
              "desc": "Senior School (Curlew St)"
            }
        ],
        "__tassversion": "01.053.3.000",
        "token": {
            "timestamp": "{ts '2021-01-21 12:20:23'}",
            "codeonly": false
        }
      }
    ```
 
* **Error Response:**

    `codeonly` not supplied
    ```javascript
    "__msg": "'codeonly' IS REQUIRED"
    ```

    `codeonly` invalid
    ```javascript
    "__msg": "'codeonly' MUST BE 'true' or 'false'" 
    ```
    
* **Sample Parameters:**

  ```javascript
  {"codeonly":"false"}
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
  http://api.tasscloud.com.au/tassweb/api/?appcode=API03&v=3&method=GetCampuses&token=3w6XHPP1j163aHf%2FHRAnLA%3D%3D&company=10
  ```
  
* **Sample POST:**

  ```HTML
  <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
    <input type="hidden" name="method" value="GetCampuses" />
    <input type="hidden" name="appcode" value="API03" />
    <input type="hidden" name="company" value="10" />
    <input type="hidden" name="v" value="3" />
    <textarea name="token">3w6XHPP1j163aHf\/HRAnLA==</textarea>
  </form>
  ```