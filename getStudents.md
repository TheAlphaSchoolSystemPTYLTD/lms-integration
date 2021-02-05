**getStudents**
----
  Returns an array of structured Student data comprising general, school, and other school details in JSON format.
  
* **Version History:**

  TASS v52.5 - Method Added

* **Version:**

  3

* **Permission:**

  Student Records > Students > View

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**

   `currentstatus [string]` -  Must be 'current' or 'future' or 'past' or 'noncurrent'
   
   **Optional:**

   `includephoto [boolean]` -  Must be 'true' or 'false' for whether returning student photo.

   `thumbnail [boolean]` -  Must be 'true' or 'false' for whether returning student thumbnail photo.

   **Conditional:**
 
   none

* **Success Response:**

    ```javascript
      {
        "students": [
            {
              "general_details": {
                        "surname": "Agnew",
                        "next_year_indicator": "Advancing",
                        "date_of_leaving": "",
                        "student_code": "0009069",
                        "usi": "000906910",
                        "portal_user_code": "",
                        "preferred_surname": "Agnew",
                        "first_name": "Edith Nell Blue Healer Bitzer",
                        "mobile_phone": "0412016500",
                        "entry_year_group": 8,
                        "religion": "Baptist",
                        "preferred_name": "Edie",
                        "other_name": "Edith Nell Other Bell Nell",
                        "gender": "",
                        "date_of_entry": "30/11/1994",
                        "date_of_birth": "02/05/1988",
                        "alternate_id": "",
                        "given_names": "Edith Nell Blue Healer Bitzer Edith Nell Other Bell Nell"
              },
              "school_details": {
                        "campus": "Senior School (Curlew St)",
                        "email_address": "agnew2@alphabus.com.au",
                        "pc_tutor_group": "AS",
                        "boarder": "No",
                        "student_cafe_access": "Yes",
                        "house": "Acacia",
                        "year_group": 11,
                        "form_class": "",
                        "residency_status": "Australian Citizen"
              },
              "other_school_details": {
                        "nationality": "American",
                        "early_depature": "Y",
                        "parish": "Chermside",
                        "learning_problems": "Y",
                        "extra_tuition": "Y",
                        "returning_student": "Y",
                        "medical_condition": "Asthmatic",
                        "sprecken_sie_deutche": "Y",
                        "campus": "Argyle St",
                        "alpha_code": "ABCD",
                        "locker_number": 1234,
                        "private_insurance": "Y",
                        "lives_with": "Boarding House",
                        "bus_route": "Doncaster",
                        "country_of_birth": "Australia",
                        "passport_number/date": 1234,
                        "rail_station": "Central",
                        "visa_number/date": 1234,
                        "residential_house": "Bell",
                        "late_arrival": "Y",
                        "repeat_year": "N",
                        "aaspa_address": "Y",
                        "address_home": 1234,
                        "external_tuition": "Y",
                        "application_date": 1234
              }
            }
        ],
        "__tassversion": "01.053.3.000",
        "token": {
              "timestamp": "{ts '2021-01-21 14:18:27'}",
              "currentstatus": "current"
        }
      }
    ```

    The State based Student numbers are returned based on the state code of the school.

      QLD LUI Number: 'lui_number'
      NSW BOS Number: 'bos_number'
      VIC VSN Number: 'vsn_number'
      TAS TQA Number: 'tqa_number'
      WA Student Number: 'wa_student_number'

* **Error Response:**

    `currentstatus` not supplied
    ```javascript
    __invalid: {
      "currentstatus": "field is required"
    }
    ```

    `currentstatus` must be 'current' or 'future' or 'past' or 'noncurrent'
    ```javascript
    __invalid: {
      "currentstatus": "Current Status must be 'current' or 'future' or 'past' or 'noncurrent'."
    }
    ```

    `includephoto` not a valid boolean
    ```javascript
    __invalid: {
      "includephoto": "Value is not a valid boolean."
    }
    ```

    `thumbnail` not a valid boolean
    ```javascript
    __invalid: {
      "thumbnail": "Value is not a valid boolean."
    }
    ```
    
* **Sample Parameters:**

  ```javascript
    {"currentstatus":"current"}
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=GetStudentsDetails&appcode=API03&company=10&v=3&token=l1D8owEn111IHcXLRwXTB0oU2GX6rj%2BISqa9zXA8We1Gqx9%2Fzb%2BcbVFartivsDN%2FxGgAIIjtABAYfzYPqTCpLf3gb0nW3h%2FTrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="getStudentsDetails">
       <input type="hidden" name="appcode" value="API03">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="3">
       <textarea name="token">l1D8owEn111IHcXLRwXTB0oU2GX6rj+ISqa9zXA8We1Gqx9/zb+cbVFartivsDN/xGgAIIjtABAYfzYPqTCpLf3gb0nW3h/TrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ</textarea>
    </form>
  ```
