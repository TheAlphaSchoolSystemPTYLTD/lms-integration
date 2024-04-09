**getTeacherSubjects**
----
  Returns a structure of Teachers with an array of structured Subject data in JSON format.

* **Version History:**

  TASS v52.5 - Method Added
  TASS v59.5 - Added new return fields sub_dept_code and sub_dept_desc. These represent the subject department.
  
* **Version:**

  3

* **Permission:**

  Teacher Records > Teachers > Subjects Tab > View

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**

   `code [string]` -  Valid teacher code or 'all'
   
   **Optional:**

   `lmsflag [string]` -  Must be 'Y' or 'N' for whether returning lms subjects.

   **Conditional:**
 
   none

* **Success Response:**

    ```javascript
      {
        "AJ": [
            {
              "semester": 2,
              "year_grp_desc": 11,
              "sub_code": "0060",
              "sub_short": "Acct",
              "year_grp": 11,
              "year_num": 2020,
              "sub_long": "Accounting 1",
              "class": "A",
              "employee_code": 1000016,
              "sub_type": "COR",
              "teacher_code": "AJ",
              "sub_dept_code": "MTH",
              "sub_dept_desc": "Mathematics"
            },
            {
              "semester": 2,
              "year_grp_desc": 8,
              "sub_code": "ANCH20",
              "sub_short": "AnHist",
              "year_grp": 8,
              "year_num": 2020,
              "sub_long": "Ancient History",
              "class": "A",
              "employee_code": 1000016,
              "sub_type": "COR",
              "teacher_code": "AJ",
              "sub_dept_code": "MTH",
              "sub_dept_desc": "Mathematics"
            }
        ],
        "__tassversion": "01.053.3.000",
        "token": {
                "code": "AJ",
                "timestamp": "{ts '2021-01-21 14:46:22'}",
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

    `code` not a valid teacher code
    ```javascript
    __invalid: {
      "code": "Invalid Teacher Code"
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
      "code":"AJ",
      "lmsflag":"Y"
    }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=GetStudentsSubjects&appcode=API03&company=10&v=3&token=l1D8owEn111IHcXLRwXTB0oU2GX6rj%2BISqa9zXA8We1Gqx9%2Fzb%2BcbVFartivsDN%2FxGgAIIjtABAYfzYPqTCpLf3gb0nW3h%2FTrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="getStudentsSubjects">
       <input type="hidden" name="appcode" value="API03">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="3">
       <textarea name="token">l1D8owEn111IHcXLRwXTB0oU2GX6rj+ISqa9zXA8We1Gqx9/zb+cbVFartivsDN/xGgAIIjtABAYfzYPqTCpLf3gb0nW3h/TrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ</textarea>
    </form>
  ```
