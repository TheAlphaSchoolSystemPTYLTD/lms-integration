**getStudentTimetable**
----
  Returns an array of structured Student data comprising timetable details in JSON format.
  
* **Version History:**

  TASS v52.5 - Method Added

* **Version:**

  3

* **Permission:**

  Timetable > Print Student Timetables > View

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**

   `student_code [string]` -  Student Code
   
   **Optional:**

   none

   **Conditional:**
 
   none

* **Success Response:**

    ```javascript
    {
        "student_timetable": [
            {
                "HSE_CODE": "AC",
                "DESC_TEXT": "Senior Timetable 2020 S2",
                "HSE_NAME": "Acacia",
                "DAYS": {
                        "2": {
                            "PERIODS": {
                                        "3": {
                                            "SUBJECTS": [
                                                        {
                                                            "SUB_CODE": "0001",
                                                            "FROM_DATE": "",
                                                            "SUB_SHORT": "Goat",
                                                            "HASOVERRIDE": 0,
                                                            "ROOM_CODE": "A1",
                                                            "TO_DATE": "",
                                                            "TCH_CODE": "AJ,BBE",
                                                            "SUBTAB_YEAR_GRP_DESC": "PK",
                                                            "CLASS": "A",
                                                            "YEAR_GRP": 11,
                                                            "TT_PRIORITY": 999,
                                                            "SUB_DESC": "English",
                                                            "SUB_ABREV": "ENG",
                                                            "LINE_CODE": "",
                                                            "SUBTAB_YEAR_GRP": -1,
                                                            "DATE_RANGE": ""
                                                        }
                                            ],
                                            "PRD_END": "1900-01-01 11:29:00.0",
                                            "PRD_CODE": 3,
                                            "PRD_START": "1900-01-01 10:30:00.0",
                                            "PRD_DESC": "Lesson 2"
                                            },
                                        "4": {
                                            "SUBJECTS": [
                                                        {
                                                            "SUB_CODE": "0001",
                                                            "FROM_DATE": "",
                                                            "SUB_SHORT": "Goat",
                                                            "HASOVERRIDE": 0,
                                                            "ROOM_CODE": "P1",
                                                            "TO_DATE": "",
                                                            "TCH_CODE": "AJ",
                                                            "SUBTAB_YEAR_GRP_DESC": "PK",
                                                            "CLASS": "A",
                                                            "YEAR_GRP": 11,
                                                            "TT_PRIORITY": 999,
                                                            "SUB_DESC": "English",
                                                            "SUB_ABREV": "ENG",
                                                            "LINE_CODE": "",
                                                            "SUBTAB_YEAR_GRP": -1,
                                                            "DATE_RANGE": ""
                                                        }
                                            ],
                                            "PRD_END": "1900-01-01 12:29:00.0",
                                            "PRD_CODE": 4,
                                            "PRD_START": "1900-01-01 11:30:00.0",
                                            "PRD_DESC": "Lesson 3"
                                        }
                            
                            }
                        }
                },
                "PERIODMIN": 1,
                "DAYMAX": 10,
                "SEMESTER": 2,
                "DAYMIN": 1,
                "PCTUT_GRP": "A3",
                "YEAR_GRP": 11,
                "ARRLINES": [],
                "YEAR_NUM": 2020,
                "STRDAYS": {
                            "1": {
                                "PERIODS": {
                                            "1": {
                                                "PRD_END": "1900-01-01 09:29:00.0",
                                                "PRD_START": "1900-01-01 08:00:00.0",
                                                "PRD_DESC": "Pastoral Care"
                                            },
                                            "2": {
                                                "PRD_END": "1900-01-01 10:20:00.0",
                                                "PRD_START": "1900-01-01 09:30:00.0",
                                                "PRD_DESC": "Lesson 1"
                                            }
                                },
                                "DAY_DESC": "Monday A"
                            }
                },
                "FORM_CLS": "A",
                "ENTITYCODE": "93_0009110",
                "TT_ID": 93,
                "ENTITYNAME": "0009110 - Bolt, Julian",
                "PERIODMAX": 7,
                "STUD_YEAR_GRP": 11
            }
        ],
        "__tassversion": "01.053.3.000",
        "token": {
                "timestamp": "{ts '2021-01-21 14:30:46'}",
                "student_code": "0009110"
        }
    }
    ```
 
* **Error Response:**

    `student_code` not supplied
    ```javascript
    __invalid: {
      "student_code": "field is required"
    }
    ```
    
* **Sample Parameters:**

  ```javascript
    { 
      "student_code":"0009110"
    }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=GetStudentTimetable&appcode=API03&company=10&v=3&token=l1D8owEn111IHcXLRwXTB0oU2GX6rj%2BISqa9zXA8We1Gqx9%2Fzb%2BcbVFartivsDN%2FxGgAIIjtABAYfzYPqTCpLf3gb0nW3h%2FTrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="getStudentTimetable">
       <input type="hidden" name="appcode" value="API03">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="3">
       <textarea name="token">l1D8owEn111IHcXLRwXTB0oU2GX6rj+ISqa9zXA8We1Gqx9/zb+cbVFartivsDN/xGgAIIjtABAYfzYPqTCpLf3gb0nW3h/TrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ</textarea>
    </form>
  ```