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
        "0009080": [
          {
            "semester": 1,
            "year_grp_desc": 11,
            "sub_code": "ANCH20",
            "from_date": "",
            "sub_short": "AnHist",
            "year_grp": 11,
            "year_num": 2018,
            "to_date": "",
            "student_code": "0009080",
            "sub_long": "Ancient History",
            "class": "A",
            "sub_type": "COR"
          },
          {
            "semester": 1,
            "year_grp_desc": 11,
            "sub_code": "0080",
            "from_date": "",
            "sub_short": "Art",
            "year_grp": 11,
            "year_num": 2018,
            "to_date": "",
            "student_code": "0009080",
            "sub_long": "Art AR Desc",
            "class": "C",
            "sub_type": "ELE"
          },
          {
            "semester": 1,
            "year_grp_desc": 11,
            "sub_code": "ASSEMBLY",
            "from_date": "",
            "sub_short": "ASSEMB",
            "year_grp": 11,
            "year_num": 2018,
            "to_date": "",
            "student_code": "0009080",
            "sub_long": "School Assembly",
            "class": "A",
            "sub_type": "NON"
          }
        ],
        "0009704": [
          {
          "semester": 1,
          "year_grp_desc": 6,
          "sub_code": "ASSEMBLY",
          "from_date": "",
          "sub_short": "ASSEMB",
          "year_grp": 6,
          "year_num": 2018,
          "to_date": "",
          "student_code": "0009704",
          "sub_long": "School Assembly",
          "class": "A",
          "sub_type": "NON"
          }
        ]
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
      "code":"0009080",
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
