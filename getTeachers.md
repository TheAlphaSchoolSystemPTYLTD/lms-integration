**getTeachers**
----
  Returns an array of structured Teacher data comprising general, school, and other school details in JSON format.
  
* **Version History:**

  TASS v52.5 - Method Added

* **Version:**

  3

* **Permission:**

  Teacher Records > Teachers > View

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**

   `currentstatus [string]` -  Must be 'current' or 'noncurrent'
   
   **Optional:**

   `includephoto [boolean]` -  Must be 'true' or 'false' for whether returning teacher photo.

   `thumbnail [boolean]` -  Must be 'true' or 'false' for whether returning teacher thumbnail photo.

   **Conditional:**
 
   none

* **Success Response:**

    ```javascript
      {
        "teachers": [
              {
                "surname": "Allan",
                "active_flag": "Y",
                "email_address": "C.Allan@alphabus.com.au",
                "salutation": "Capt",
                "department": "OTH",
                "portal_user_code": "",
                "school_email_address": "Cody.Allan@alphabus.com.au",
                "teacher_photo": {
                "file_info": {
                      "image": "[Base64 encoded image string]",
                      "file_name": "Unavailable.gif",
                      "mime_type": "image/gif"
                }
              },
              "employee_code": 9000001,
              "teacher_code": "CAL",
              "given_names": "Cody Ethan"
              }
        ],
        "__tassversion": "01.053.3.000",
        "token": {
            "timestamp": "{ts '2021-01-21 14:42:22'}",
            "includephoto": true,
            "thumbnail": false,
            "currentstatus": "current"
        }
      }
    ```
 
* **Error Response:**

    `currentstatus` not supplied
    ```javascript
    __invalid: {
      "currentstatus": "field is required"
    }
    ```

    `currentstatus` must be 'current' or 'noncurrent'
    ```javascript
    __invalid: {
      "currentstatus": "Current Status must be 'current' or 'noncurrent'."
    }
    ```

    `includephoto` not a valid boolean
    ```javascript
    __invalid: {
      "includephoto": "Value is not a valid boolean."
    }
    ```

    `thumbnail` not a valid boolean
    ```javascript
    __invalid: {
      "thumbnail": "Value is not a valid boolean."
    }
    ```
    
* **Sample Parameters:**

  ```javascript
    { 
      "currentstatus":"current",
      "includephoto":"true",
      "thumbnail":"false"
    }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=GetTeachers&appcode=API03&company=10&v=2&token=l1D8owEn111IHcXLRwXTB0oU2GX6rj%2BISqa9zXA8We1Gqx9%2Fzb%2BcbVFartivsDN%2FxGgAIIjtABAYfzYPqTCpLf3gb0nW3h%2FTrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="getTeachers">
       <input type="hidden" name="appcode" value="API03">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="2">
       <textarea name="token">l1D8owEn111IHcXLRwXTB0oU2GX6rj+ISqa9zXA8We1Gqx9/zb+cbVFartivsDN/xGgAIIjtABAYfzYPqTCpLf3gb0nW3h/TrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ</textarea>
    </form>
  ```
