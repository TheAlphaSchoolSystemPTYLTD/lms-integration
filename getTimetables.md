**getTimetables**
----
  Returns an array of structured details of timetables in JSON format.
  
* **Version History:**

  TASS v52.5 - Method Added

* **Version:**

  3

* **Permission:**

  Timetables > Timetable Setup > Timetable Definitions > View

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**

   `year_num [string]` -  Year Number

   `period [string]` -  Period Code
   
   **Optional:**
 
   none

   **Conditional:**
 
   none

* **Success Response:**

    ```javascript
      {
        "timetables":[
            {
                "sub_code":9998,
                "room_code":"A1",
                "tch_code":"RY",
                "prd_code":7,
                "table_id":"ttmast",
                "class":"A",
                "day_code":1,
                "semester":1,
                "year_grp_desc":8,
                "year_grp":8,
                "year_num":2019,
                "record_id":232326,
                "id":"1_87_2019_1_1_7_9998_8_A_RY_A1",
                "tt_id":87
            },
            {
                "sub_code":"0028",
                "room_code":"D1",
                "tch_code":"AMC",
                "prd_code":7,
                "table_id":"ttmast",
                "class":"E",
                "day_code":1,
                "semester":1,
                "year_grp_desc":10,
                "year_grp":10,
                "year_num":2019,
                "record_id":231936,
                "id":"2_87_2019_1_1_7_0028_10_E_AMC_D1",
                "tt_id":87
            }
        ],
        "token":{
            "year":2019,
            "period":7,
            "timestamp":"{ts '2020-02-28 12:07:15'}"
        }
      }
    ```
 
* **Error Response:**

    `year` not supplied
    ```javascript
    __invalid: {
      "year": "field is required"
    }
    ```

    `period` not supplied
    ```javascript
    __invalid: {
      "period": "field is required"
    }
    ```
    
* **Sample Parameters:**

  ```javascript
    { 
      "year":"2019",
      "period":"7"
    }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=getTimetables&appcode=API03&company=10&v=3&token=l1D8owEn111IHcXLRwXTB0oU2GX6rj%2BISqa9zXA8We1Gqx9%2Fzb%2BcbVFartivsDN%2FxGgAIIjtABAYfzYPqTCpLf3gb0nW3h%2FTrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="getTimetables">
       <input type="hidden" name="appcode" value="API03">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="3">
       <textarea name="token">l1D8owEn111IHcXLRwXTB0oU2GX6rj+ISqa9zXA8We1Gqx9/zb+cbVFartivsDN/xGgAIIjtABAYfzYPqTCpLf3gb0nW3h/TrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ</textarea>
    </form>
  ```