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
          "teacher_timetable":[
              {
                  "DESC_TEXT":"Junior Timetable 2019 S2",
                  "DAYS":{
                      "1":{
                          "PERIODS":{
                              "1":{
                                  "SUBJECTS":[
                                      {
                                          "SUB_CODE":9998,
                                          "SUB_SHORT":"HomeRm",
                                          "HASOVERRIDE":0,
                                          "ROOM_CODE":"LIB",
                                          "TCH_CODE":"LB",
                                          "SUBTAB_YEAR_GRP_DESC":"",
                                          "CLASS":"A",
                                          "YEAR_GRP":2,
                                          "SUB_DESC":"Home Room",
                                          "SUB_ABREV":"HM",
                                          "LINE_CODE":"",
                                          "SUBTAB_YEAR_GRP":""
                                      }
                                  ],
                                  "PRD_END":"1900-01-01 09:35:00.0",
                                  "PRD_CODE":1,
                                  "PRD_START":"1900-01-01 08:30:00.0",
                                  "PRD_DESC":"Lesson 1"
                              }
                          }
                      }
                  },
                  "PERIODMIN":1,
                  "DAYMAX":5,
                  "SEMESTER":2,
                  "DAYMIN":1,
                  "YEAR_GRP":"",
                  "ARRLINES":[

                  ],
                  "YEAR_NUM":2019,
                  "STRDAYS":{
                      "1":{
                          "PERIODS":{
                              "1":{
                                  "PRD_END":"1900-01-01 09:35:00.0",
                                  "PRD_START":"1900-01-01 08:30:00.0",
                                  "PRD_DESC":"Lesson 1"
                              },
                              "2":{
                                  "PRD_END":"1900-01-01 10:29:00.0",
                                  "PRD_START":"1900-01-01 09:36:00.0",
                                  "PRD_DESC":"Lesson 2"
                              },
                              "3":{
                                  "PRD_END":"1900-01-01 11:29:00.0",
                                  "PRD_START":"1900-01-01 10:30:00.0",
                                  "PRD_DESC":"Lesson 3"
                              },
                              "4":{
                                  "PRD_END":"1900-01-01 12:29:00.0",
                                  "PRD_START":"1900-01-01 11:30:00.0",
                                  "PRD_DESC":"Lesson 4"
                              },
                              "5":{
                                  "PRD_END":"1900-01-01 13:29:00.0",
                                  "PRD_START":"1900-01-01 12:30:00.0",
                                  "PRD_DESC":"Lesson 5"
                              },
                              "6":{
                                  "PRD_END":"1900-01-01 14:29:00.0",
                                  "PRD_START":"1900-01-01 13:30:00.0",
                                  "PRD_DESC":"Lesson 6"
                              },
                              "7":{
                                  "PRD_END":"1900-01-01 15:29:00.0",
                                  "PRD_START":"1900-01-01 14:30:00.0",
                                  "PRD_DESC":"Lesson 7"
                              }
                          },
                          "DAY_DESC":"Monday"
                      },
                      "2":{
                          "PERIODS":{
                              "1":{
                                  "PRD_END":"1900-01-01 09:29:00.0",
                                  "PRD_START":"1900-01-01 08:30:00.0",
                                  "PRD_DESC":"Lesson 1"
                              },
                              "2":{
                                  "PRD_END":"1900-01-01 10:29:00.0",
                                  "PRD_START":"1900-01-01 09:30:00.0",
                                  "PRD_DESC":"Lesson 2"
                              },
                              "3":{
                                  "PRD_END":"1900-01-01 11:29:00.0",
                                  "PRD_START":"1900-01-01 10:30:00.0",
                                  "PRD_DESC":"Lesson 3"
                              },
                              "4":{
                                  "PRD_END":"1900-01-01 12:29:00.0",
                                  "PRD_START":"1900-01-01 11:30:00.0",
                                  "PRD_DESC":"Lesson 4"
                              },
                              "5":{
                                  "PRD_END":"1900-01-01 13:29:00.0",
                                  "PRD_START":"1900-01-01 12:30:00.0",
                                  "PRD_DESC":"Lesson 5"
                              },
                              "6":{
                                  "PRD_END":"1900-01-01 14:29:00.0",
                                  "PRD_START":"1900-01-01 13:30:00.0",
                                  "PRD_DESC":"Lesson 6"
                              },
                              "7":{
                                  "PRD_END":"1900-01-01 15:29:00.0",
                                  "PRD_START":"1900-01-01 14:30:00.0",
                                  "PRD_DESC":"Lesson 7"
                              }
                          },
                          "DAY_DESC":"Tuesday"
                      },
                      "3":{
                          "PERIODS":{
                              "1":{
                                  "PRD_END":"1900-01-01 09:29:00.0",
                                  "PRD_START":"1900-01-01 08:30:00.0",
                                  "PRD_DESC":"Lesson 1"
                              },
                              "2":{
                                  "PRD_END":"1900-01-01 10:29:00.0",
                                  "PRD_START":"1900-01-01 09:30:00.0",
                                  "PRD_DESC":"Lesson 2"
                              },
                              "3":{
                                  "PRD_END":"1900-01-01 11:29:00.0",
                                  "PRD_START":"1900-01-01 10:30:00.0",
                                  "PRD_DESC":"Lesson 3"
                              },
                              "4":{
                                  "PRD_END":"1900-01-01 12:29:00.0",
                                  "PRD_START":"1900-01-01 11:30:00.0",
                                  "PRD_DESC":"Lesson 4"
                              },
                              "5":{
                                  "PRD_END":"1900-01-01 13:29:00.0",
                                  "PRD_START":"1900-01-01 12:30:00.0",
                                  "PRD_DESC":"Lesson 5"
                              },
                              "6":{
                                  "PRD_END":"1900-01-01 14:29:00.0",
                                  "PRD_START":"1900-01-01 13:30:00.0",
                                  "PRD_DESC":"Lesson 6"
                              },
                              "7":{
                                  "PRD_END":"1900-01-01 15:29:00.0",
                                  "PRD_START":"1900-01-01 14:30:00.0",
                                  "PRD_DESC":"Lesson 7"
                              }
                          },
                          "DAY_DESC":"Wednesday"
                      },
                      "4":{
                          "PERIODS":{
                              "1":{
                                  "PRD_END":"1900-01-01 09:29:00.0",
                                  "PRD_START":"1900-01-01 08:30:00.0",
                                  "PRD_DESC":"Lesson 1"
                              },
                              "2":{
                                  "PRD_END":"1900-01-01 10:29:00.0",
                                  "PRD_START":"1900-01-01 09:30:00.0",
                                  "PRD_DESC":"Lesson 2"
                              },
                              "3":{
                                  "PRD_END":"1900-01-01 11:29:00.0",
                                  "PRD_START":"1900-01-01 10:30:00.0",
                                  "PRD_DESC":"Lesson 3"
                              },
                              "4":{
                                  "PRD_END":"1900-01-01 12:29:00.0",
                                  "PRD_START":"1900-01-01 11:30:00.0",
                                  "PRD_DESC":"Lesson 4"
                              },
                              "5":{
                                  "PRD_END":"1900-01-01 13:29:00.0",
                                  "PRD_START":"1900-01-01 12:30:00.0",
                                  "PRD_DESC":"Lesson 5"
                              },
                              "6":{
                                  "PRD_END":"1900-01-01 14:29:00.0",
                                  "PRD_START":"1900-01-01 13:30:00.0",
                                  "PRD_DESC":"Lesson 6"
                              },
                              "7":{
                                  "PRD_END":"1900-01-01 15:29:00.0",
                                  "PRD_START":"1900-01-01 14:30:00.0",
                                  "PRD_DESC":"Lesson 7"
                              }
                          },
                          "DAY_DESC":"Thursday"
                      },
                      "5":{
                          "PERIODS":{
                              "1":{
                                  "PRD_END":"1900-01-01 09:29:00.0",
                                  "PRD_START":"1900-01-01 08:30:00.0",
                                  "PRD_DESC":"Lesson 1"
                              },
                              "2":{
                                  "PRD_END":"1900-01-01 10:29:00.0",
                                  "PRD_START":"1900-01-01 09:30:00.0",
                                  "PRD_DESC":"Lesson 2"
                              },
                              "3":{
                                  "PRD_END":"1900-01-01 11:29:00.0",
                                  "PRD_START":"1900-01-01 10:30:00.0",
                                  "PRD_DESC":"Lesson 3"
                              },
                              "4":{
                                  "PRD_END":"1900-01-01 12:29:00.0",
                                  "PRD_START":"1900-01-01 11:30:00.0",
                                  "PRD_DESC":"Lesson 4"
                              },
                              "5":{
                                  "PRD_END":"1900-01-01 13:29:00.0",
                                  "PRD_START":"1900-01-01 12:30:00.0",
                                  "PRD_DESC":"Lesson 5"
                              },
                              "6":{
                                  "PRD_END":"1900-01-01 14:29:00.0",
                                  "PRD_START":"1900-01-01 13:30:00.0",
                                  "PRD_DESC":"Lesson 6"
                              }
                          },
                          "DAY_DESC":"Friday"
                      }
                  },
                  "ENTITYCODE":"88_LB",
                  "TT_ID":88,
                  "ENTITYNAME":"LB - Lyn Helen Bell",
                  "PERIODMAX":7
              }
          ],
          "token":{
              "semester":2,
              "year_num":2019,
              "timestamp":"{ts '2020-02-28 10:29:12'}",
              "teacher_code":"LB"
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
      "teacher_code":"LB",
      "year_num":"2019",
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