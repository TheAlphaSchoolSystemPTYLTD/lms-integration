**getTeacherTimetable**
----
  Returns an array of structured Teacher data comprising timetable details in JSON format.
  
* **Version History:**

  TASS v52.5 - Method Added

* **Version:**

  3

* **Permission:**

  Timetable > Print Teacher Timetables > View

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**

   `teacher_code [string]` -  Teacher Code

   `year_num [string]` -  Year Number

   `semester [string]` -  Semester
   
   **Optional:**

   `tt_id [string]` -  Timetable Id

   **Conditional:**
 
   none

* **Success Response:**

    ```javascript
      {
        "teacher_timetable": [
            {
              "DESC_TEXT": "Junior Timetable 2020 S2",
              "DAYS": {
                  "1": {
                    "PERIODS": {
                          "3": {
                              "SUBJECTS": [
                                  {
                                    "SUB_CODE": "0001",
                                    "SUB_SHORT": "Goat",
                                    "HASOVERRIDE": 0,
                                    "ROOM_CODE": "D3",
                                    "TCH_CODE": "AJ",
                                    "SUBTAB_YEAR_GRP_DESC": "PK",
                                    "CLASS": "A",
                                    "YEAR_GRP": 3,
                                    "SUB_DESC": "English",
                                    "SUB_ABREV": "ENG",
                                    "LINE_CODE": "",
                                    "SUBTAB_YEAR_GRP": -1
                                  }
                              ],
                              "PRD_END": "1900-01-01 11:29:00.0",
                              "PRD_CODE": 3,
                              "PRD_START": "1900-01-01 10:30:00.0",
                              "PRD_DESC": "Lesson 3"
                          }
                    }
                  }
              },
              "PERIODMIN": 1,
              "DAYMAX": 5,
              "SEMESTER": 2,
              "DAYMIN": 1,
              "YEAR_GRP": "",
              "ARRLINES": [],
              "YEAR_NUM": 2020,
              "STRDAYS": {
                    "1": {
                      "PERIODS": {
                            "1": {
                              "PRD_END": "1900-01-01 09:35:00.0",
                              "PRD_START": "1900-01-01 08:30:00.0",
                              "PRD_DESC": "Lesson 1"
                            },
                            "2": {
                              "PRD_END": "1900-01-01 10:29:00.0",
                              "PRD_START": "1900-01-01 09:36:00.0",
                              "PRD_DESC": "Lesson 2"
                            }
                      },
                      "DAY_DESC": "Monday"
                    }
              },
              "ENTITYCODE": "92_AJ",
              "TT_ID": 92,
              "ENTITYNAME": "AJ - Mr A O'Johnstone",
              "PERIODMAX": 7
            }
        ],
        "__tassversion": "01.053.3.000",
        "token": {
            "semester": 2,
            "year_num": 2020,
            "timestamp": "{ts '2021-01-21 15:16:41'}",
            "teacher_code": "AJ"
        }
      }
    ```
 
* **Error Response:**

    `teacher_code` not supplied
    ```javascript
    __invalid: {
      "teacher_code": "field is required"
    }
    ```

    `year_num` not supplied
    ```javascript
    __invalid: {
      "year_num": "field is required"
    }
    ```

    `semester` not supplied
    ```javascript
    __invalid: {
      "semester": "field is required"
    }
    ```
    
* **Sample Parameters:**

  ```javascript
    { 
      "teacher_code":"AJ",
      "year_num":"2020",
      "semester":"2"
    }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=GetTeacherTimetable&appcode=API03&company=10&v=3&token=l1D8owEn111IHcXLRwXTB0oU2GX6rj%2BISqa9zXA8We1Gqx9%2Fzb%2BcbVFartivsDN%2FxGgAIIjtABAYfzYPqTCpLf3gb0nW3h%2FTrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="getTeacherTimetable">
       <input type="hidden" name="appcode" value="API03">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="3">
       <textarea name="token">l1D8owEn111IHcXLRwXTB0oU2GX6rj+ISqa9zXA8We1Gqx9/zb+cbVFartivsDN/xGgAIIjtABAYfzYPqTCpLf3gb0nW3h/TrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ</textarea>
    </form>
  ```