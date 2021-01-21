**getStudentSubjects**
----
  Returns a structure of Students with an array of structured Subject data in JSON format.

* **Version History:**

  TASS v52.5 - Method Added

* **Version:**

  3

* **Permission:**

  Student Records > Students > Subjects Tab > View

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**

   `code [string]` -  Valid student code or 'all'
   
   **Optional:**

   `lmsflag [string]` -  Must be 'Y' or 'N' for whether returning lms subjects.

   **Conditional:**
 
   none

* **Success Response:**

    ```javascript
      {
        "0009112": [
              {
                "sub_code": "0080",
                "from_date": "",
                "sub_short": "Art",
                "to_date": "",
                "student_code": "0009112",
                "sub_long": "Art AR Desc",
                "class": "A",
                "sub_type": "ELE",
                "semester": 2,
                "year_grp_desc": 10,
                "year_grp": 10,
                "year_num": 2020
              },
              {
                "sub_code": 2204,
                "from_date": "",
                "sub_short": "IDT",
                "to_date": "",
                "student_code": "0009112",
                "sub_long": "Digital Technologies",
                "class": "A",
                "sub_type": "ELE",
                "semester": 2,
                "year_grp_desc": 10,
                "year_grp": 10,
                "year_num": 2020
              }
        ],
        "__tassversion": "01.053.3.000",
        "token": {
          "code": "0009112",
          "timestamp": "{ts '2021-01-21 14:27:51'}",
          "lmsflag": "Y"
        }
      }
    ```
 
* **Error Response:**

    `code` not supplied
    ```javascript
    __invalid: {
      "code": "field is required"
    }
    ```
    
    `code` not a valid student code
    ```javascript
    __invalid: {
      "code": "Invalid Student Code"
    }
    ```
    
    `lmsflag` not set to 'Y' or 'N'
    ```javascript
    __invalid: {
      "lmsflag": "lmsflag must be set to 'Y' or 'N'."
    }
    ```
   
* **Sample Parameters:**

  ```javascript
    { 
      "code":"0009112",
      "lmsflag":"Y"
    }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=GetStudentSubjects&appcode=API03&company=10&v=3&token=l1D8owEn111IHcXLRwXTB0oU2GX6rj%2BISqa9zXA8We1Gqx9%2Fzb%2BcbVFartivsDN%2FxGgAIIjtABAYfzYPqTCpLf3gb0nW3h%2FTrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="getStudentSubjects">
       <input type="hidden" name="appcode" value="API03">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="3">
       <textarea name="token">l1D8owEn111IHcXLRwXTB0oU2GX6rj+ISqa9zXA8We1Gqx9/zb+cbVFartivsDN/xGgAIIjtABAYfzYPqTCpLf3gb0nW3h/TrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ</textarea>
    </form>
  ```
