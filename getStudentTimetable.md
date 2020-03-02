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
        "student_timetable":[
            {
                "HSE_CODE":"AC",
                "DESC_TEXT":"Senior Timetable 2019 S2",
                "HSE_NAME":"Acacia",
                "DAYS":{
                    "1":{
                        "PERIODS":{
                            "1":{
                                "SUBJECTS":[
                                    {
                                        "SUB_CODE":"ASSEMBLY",
                                        "FROM_DATE":"",
                                        "SUB_SHORT":"ASSEMB",
                                        "HASOVERRIDE":0,
                                        "ROOM_CODE":"LIB",
                                        "TO_DATE":"",
                                        "TCH_CODE":"JSH",
                                        "SUBTAB_YEAR_GRP_DESC":"",
                                        "CLASS":"A",
                                        "YEAR_GRP":11,
                                        "TT_PRIORITY":999,
                                        "SUB_DESC":"ASSEMBLY",
                                        "SUB_ABREV":"",
                                        "LINE_CODE":"",
                                        "SUBTAB_YEAR_GRP":"",
                                        "DATE_RANGE":""
                                    },
                                    {
                                        "SUB_CODE":"HOME9997",
                                        "FROM_DATE":"",
                                        "SUB_SHORT":"HMR",
                                        "HASOVERRIDE":0,
                                        "ROOM_CODE":"A4",
                                        "TO_DATE":"",
                                        "TCH_CODE":"AJ",
                                        "SUBTAB_YEAR_GRP_DESC":"",
                                        "CLASS":"A",
                                        "YEAR_GRP":11,
                                        "TT_PRIORITY":999,
                                        "SUB_DESC":"Home Room",
                                        "SUB_ABREV":"HMR",
                                        "LINE_CODE":"",
                                        "SUBTAB_YEAR_GRP":"",
                                        "DATE_RANGE":""
                                    }
                                ],
                                "PRD_END":"1900-01-01 09:29:00.0",
                                "PRD_CODE":1,
                                "PRD_START":"1900-01-01 08:00:00.0",
                                "PRD_DESC":"Pastoral Care"
                            }
                        }
                    }
                },
                "PERIODMIN":1,
                "DAYMAX":10,
                "SEMESTER":2,
                "DAYMIN":1,
                "PCTUT_GRP":"A3",
                "YEAR_GRP":11,
                "ARRLINES":[

                ],
                "YEAR_NUM":2019,
                "STRDAYS":{
                    "1":{
                        "PERIODS":{
                            "1":{
                                "PRD_END":"1900-01-01 09:29:00.0",
                                "PRD_START":"1900-01-01 08:00:00.0",
                                "PRD_DESC":"Pastoral Care"
                            },
                            "2":{
                                "PRD_END":"1900-01-01 10:20:00.0",
                                "PRD_START":"1900-01-01 09:30:00.0",
                                "PRD_DESC":"Lesson 1"
                            },
                            "3":{
                                "PRD_END":"1900-01-01 11:29:00.0",
                                "PRD_START":"1900-01-01 10:30:00.0",
                                "PRD_DESC":"Lesson 2"
                            },
                            "4":{
                                "PRD_END":"1900-01-01 12:29:00.0",
                                "PRD_START":"1900-01-01 11:30:00.0",
                                "PRD_DESC":"Lesson 3"
                            },
                            "5":{
                                "PRD_END":"1900-01-01 13:29:00.0",
                                "PRD_START":"1900-01-01 12:30:00.0",
                                "PRD_DESC":"Lesson 4"
                            },
                            "6":{
                                "PRD_END":"1900-01-01 14:29:00.0",
                                "PRD_START":"1900-01-01 13:30:00.0",
                                "PRD_DESC":"Lesson 5"
                            },
                            "7":{
                                "PRD_END":"1900-01-01 17:00:00.0",
                                "PRD_START":"1900-01-01 14:30:00.0",
                                "PRD_DESC":"Lesson 6"
                            }
                        },
                        "DAY_DESC":"Monday A"
                    },
                    "2":{
                        "PERIODS":{
                            "1":{
                                "PRD_END":"1900-01-01 10:27:00.0",
                                "PRD_START":"1900-01-01 08:30:00.0",
                                "PRD_DESC":"Pastoral Care"
                            },
                            "2":{
                                "PRD_END":"1900-01-01 10:29:00.0",
                                "PRD_START":"1900-01-01 10:28:00.0",
                                "PRD_DESC":"Lesson 1"
                            },
                            "3":{
                                "PRD_END":"1900-01-01 11:29:00.0",
                                "PRD_START":"1900-01-01 10:30:00.0",
                                "PRD_DESC":"Lesson 2"
                            },
                            "4":{
                                "PRD_END":"1900-01-01 12:29:00.0",
                                "PRD_START":"1900-01-01 11:30:00.0",
                                "PRD_DESC":"Lesson 3"
                            },
                            "5":{
                                "PRD_END":"1900-01-01 13:29:00.0",
                                "PRD_START":"1900-01-01 12:30:00.0",
                                "PRD_DESC":"Lesson 4"
                            },
                            "6":{
                                "PRD_END":"1900-01-01 15:00:00.0",
                                "PRD_START":"1900-01-01 13:30:00.0",
                                "PRD_DESC":"Lesson 5"
                            },
                            "7":{
                                "PRD_END":"1900-01-01 17:29:00.0",
                                "PRD_START":"1900-01-01 16:50:00.0",
                                "PRD_DESC":"Lesson 6"
                            }
                        },
                        "DAY_DESC":"Tuesday A"
                    },
                    "3":{
                        "PERIODS":{
                            "1":{
                                "PRD_END":"1900-01-01 09:28:00.0",
                                "PRD_START":"1900-01-01 08:30:00.0",
                                "PRD_DESC":"Before L1"
                            },
                            "2":{
                                "PRD_END":"1900-01-01 10:29:00.0",
                                "PRD_START":"1900-01-01 09:30:00.0",
                                "PRD_DESC":"Lesson 1"
                            },
                            "3":{
                                "PRD_END":"1900-01-01 11:29:00.0",
                                "PRD_START":"1900-01-01 10:30:00.0",
                                "PRD_DESC":"Lesson 2"
                            },
                            "4":{
                                "PRD_END":"1900-01-01 12:29:00.0",
                                "PRD_START":"1900-01-01 11:30:00.0",
                                "PRD_DESC":"Lesson 3"
                            },
                            "5":{
                                "PRD_END":"1900-01-01 13:29:00.0",
                                "PRD_START":"1900-01-01 12:30:00.0",
                                "PRD_DESC":"Lesson 4"
                            },
                            "6":{
                                "PRD_END":"1900-01-01 14:29:00.0",
                                "PRD_START":"1900-01-01 13:30:00.0",
                                "PRD_DESC":"Lesson 5"
                            },
                            "7":{
                                "PRD_END":"1900-01-01 15:29:00.0",
                                "PRD_START":"1900-01-01 14:30:00.0",
                                "PRD_DESC":"Lesson 6"
                            }
                        },
                        "DAY_DESC":"Wednesday A"
                    },
                    "4":{
                        "PERIODS":{
                            "1":{
                                "PRD_END":"1900-01-01 09:29:00.0",
                                "PRD_START":"1900-01-01 08:30:00.0",
                                "PRD_DESC":"Pastoral Care"
                            },
                            "2":{
                                "PRD_END":"1900-01-01 10:29:00.0",
                                "PRD_START":"1900-01-01 09:30:00.0",
                                "PRD_DESC":"Lesson 1"
                            },
                            "3":{
                                "PRD_END":"1900-01-01 11:29:00.0",
                                "PRD_START":"1900-01-01 10:30:00.0",
                                "PRD_DESC":"Lesson 2"
                            },
                            "4":{
                                "PRD_END":"1900-01-01 12:29:00.0",
                                "PRD_START":"1900-01-01 11:30:00.0",
                                "PRD_DESC":"Lesson 3"
                            },
                            "5":{
                                "PRD_END":"1900-01-01 13:29:00.0",
                                "PRD_START":"1900-01-01 12:30:00.0",
                                "PRD_DESC":"Lesson 4"
                            },
                            "6":{
                                "PRD_END":"1900-01-01 14:29:00.0",
                                "PRD_START":"1900-01-01 13:30:00.0",
                                "PRD_DESC":"Lesson 5"
                            },
                            "7":{
                                "PRD_END":"1900-01-01 17:29:00.0",
                                "PRD_START":"1900-01-01 14:30:00.0",
                                "PRD_DESC":"Lesson 6"
                            }
                        },
                        "DAY_DESC":"Thursday A"
                    },
                    "5":{
                        "PERIODS":{
                            "1":{
                                "PRD_END":"1900-01-01 09:29:00.0",
                                "PRD_START":"1900-01-01 08:30:00.0",
                                "PRD_DESC":"Pastoral Care"
                            },
                            "2":{
                                "PRD_END":"1900-01-01 10:29:00.0",
                                "PRD_START":"1900-01-01 09:30:00.0",
                                "PRD_DESC":"Lesson 1"
                            },
                            "3":{
                                "PRD_END":"1900-01-01 11:29:00.0",
                                "PRD_START":"1900-01-01 10:30:00.0",
                                "PRD_DESC":"Lesson 2"
                            },
                            "4":{
                                "PRD_END":"1900-01-01 12:29:00.0",
                                "PRD_START":"1900-01-01 11:30:00.0",
                                "PRD_DESC":"Lesson 3"
                            },
                            "5":{
                                "PRD_END":"1900-01-01 13:29:00.0",
                                "PRD_START":"1900-01-01 12:30:00.0",
                                "PRD_DESC":"Lesson 4"
                            },
                            "6":{
                                "PRD_END":"1900-01-01 14:29:00.0",
                                "PRD_START":"1900-01-01 13:30:00.0",
                                "PRD_DESC":"Lesson 5"
                            },
                            "7":{
                                "PRD_END":"1900-01-01 17:29:00.0",
                                "PRD_START":"1900-01-01 14:30:00.0",
                                "PRD_DESC":"Lesson 6"
                            }
                        },
                        "DAY_DESC":"Friday A"
                    }
                },
                "FORM_CLS":"B",
                "ENTITYCODE":"89_0009110",
                "TT_ID":89,
                "ENTITYNAME":"0009110 - Bolt, Julian",
                "PERIODMAX":7,
                "STUD_YEAR_GRP":11
            }
        ],
        "token":{
            "timestamp":"{ts '2020-02-28 10:15:37'}",
            "student_code":"0009110"
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