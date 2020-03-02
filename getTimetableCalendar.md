**getTimetableCalendar**
----
  Returns an array of structured details of one timetable in JSON format.
  
* **Version History:**

  TASS v52.5 - Method Added

* **Version:**

  3

* **Permission:**

  Timetables > Timetable Calendar Setup > View

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**

   `tt_id [string]` -  Timetable Id

   **Optional:**

   none

   **Conditional:**
 
   none

* **Success Response:**

    ```javascript
      {
        "tt_calendar":[
            {
                "CAT_NUM":"",
                "CMPY_CODE":10,
                "TTDATE":"2019-07-01 00:00:00.0",
                "RECORD_ID":135902,
                "LABEL":"Mon 01/07/2019",
                "ID":"89-2019-07-01",
                "TABLE_ID":"ttcalendar",
                "VALUE":"2019-07-01",
                "TT_ID":89,
                "DAY_CODE":1
            },
            {
                "CAT_NUM":"",
                "CMPY_CODE":10,
                "TTDATE":"2019-07-02 00:00:00.0",
                "RECORD_ID":135903,
                "LABEL":"Tue 02/07/2019",
                "ID":"89-2019-07-02",
                "TABLE_ID":"ttcalendar",
                "VALUE":"2019-07-02",
                "TT_ID":89,
                "DAY_CODE":2
            }
        ],
        "token":{
            "timestamp":"{ts '2020-02-28 12:16:39'}",
            "tt_id":89
        }
      }
    ```
 
* **Error Response:**

    `tt_id` not supplied
    ```javascript
    __invalid: {
      "tt_id": "field is required"
    }
    ```
    
* **Sample Parameters:**

  ```javascript
    { 
      "tt_id":"89"
    }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=getTimetableCalendar&appcode=API03&company=10&v=3&token=l1D8owEn111IHcXLRwXTB0oU2GX6rj%2BISqa9zXA8We1Gqx9%2Fzb%2BcbVFartivsDN%2FxGgAIIjtABAYfzYPqTCpLf3gb0nW3h%2FTrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="getTimetableCalendar">
       <input type="hidden" name="appcode" value="API03">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="3">
       <textarea name="token">l1D8owEn111IHcXLRwXTB0oU2GX6rj+ISqa9zXA8We1Gqx9/zb+cbVFartivsDN/xGgAIIjtABAYfzYPqTCpLf3gb0nW3h/TrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ</textarea>
    </form>
  ```