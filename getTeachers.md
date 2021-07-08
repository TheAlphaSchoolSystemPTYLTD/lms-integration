**getTeachers**
----
  Returns an array of structured Teacher data comprising general, school, and other school details in JSON format.
  
* **Version History:**

  TASS v52.5 - Method Added
  
  TASS v53.3 (PR7) -  first_name, other_name, preferred_name and teacher_name have been added
  
  TASS v54.3 (PR1) -  first_name, other_name, preferred_name and teacher_name have been added

  TASS v54.4 - Enhancement to include "pc_tutor_group" in the result

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
      "__tassversion":"01.054.4.000",
      "teachers":[
        {
          "surname":"Allibone",
          "active_flag":"Y",
          "teacher_name":"Mr N A'llibone",
          "pc_tutor_group":"",
          "department":"LAN",
          "portal_user_code":"",
          "teacher_photo":{
            "file_info":{
              "image": "[Base64 encoded image string]",
              "file_name":"1000066.jpg",
              "mime_type":"image/jpeg"
            }
          },
          "employee_code":1000066,
          "teacher_code":"NA1",
          "first_name":"Nikola",
          "email_address":"tester@example.com",
          "salutation":"Assoc. Prof",
          "preferred_name":"Niki",
          "other_name":"Craig",
          "school_email_address":"Nikola.Allibone@alphabus.com.aubnm",
          "given_names":"Nikola Craig"
        }
      ],
      "token":{
        "timestamp":"{ts '2021-07-08 12:20:25'}",
        "includephoto":true,
        "thumbnail":false,
        "currentstatus":"current"
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
