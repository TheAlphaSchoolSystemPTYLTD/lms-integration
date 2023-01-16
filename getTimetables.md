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

   `year [string]` -  Year Number

   `period [string]` -  Period Code
   
   **Optional:**
 
   none

   **Conditional:**
 
   none

* **Success Response:**

    ```javascript
      {
        "timetables": [
              {
                "sub_code": "0001",
                "room_code": "001",
                "tch_code": "OB",
                "prd_code": 2,
                "table_id": "ttmast",
                "class": "S",
                "day_code": 1,
                "semester": 1,
                "year_grp_desc": 7,
                "year_grp": 7,
                "year_num": 2020,
                "record_id": 272334,
                "id": "2_91_2020_1_1_2_0001_7_S_OB_001",
                "tt_id": 91
              },
              {
                "sub_code": "0019",
                "room_code": "B1",
                "tch_code": "AJ",
                "prd_code": 2,
                "table_id": "ttmast",
                "class": "B",
                "day_code": 1,
                "semester": 1,
                "year_grp_desc": 11,
                "year_grp": 11,
                "year_num": 2020,
                "record_id": 272378,
                "id": "3_91_2020_1_1_2_0019_11_B_AJ_B1",
                "tt_id": 91
              }
        ],
        "__tassversion": "01.053.3.000",
        "token": {
            "year": 2020,
            "period": 2,
            "timestamp": "{ts '2021-01-21 15:24:18'}"
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
      "year":"2020",
      "period":"2"
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
