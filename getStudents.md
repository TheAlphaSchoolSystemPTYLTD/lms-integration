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
      "students": [
        {
          "general_details": {
            "surname": "Angus",
            "first_name": "Paul",
            "other_name": "",
            "preferred_surname": "Angus",
            "next_year_indicator": "Advancing",
            "date_of_leaving": "",
            "student_code": 20073,
            "usi": "",
            "mobile_phone": "",
            "lui_number": "",
            "entry_year_group": 8,
            "religion": "Anglican",
            "preferred_name": "Paul",
            "gender": "Male",
            "date_of_entry": "19/01/1998",
            "portal_user_code":"pangus"
            "student_photo": {
              "file_info": {
                "image": "[Base64 encoded image string]",
                "file_name": "tn_20073.jpg",
                "mime_type": "image/jpeg"
              }
            },
            "date_of_birth": "15/10/1994",
            "alternate_id": "098765432",
            "given_names": "Paul"
          },
          "school_details": {
            "campus": "Senior School (Curlew St)",
            "email_address": "angu001@tassweb.com.au",
            "pc_tutor_group": "A1",
            "boarder": "Yes",
            "student_cafe_access": "No",
            "house": "Banksia",
            "year_group": 11,
            "form_class": "A",
            "residency_status": "Overseas Student"
          },
          "other_school_details": {
            "parish": "Chermside",
            "library_card_no.": "",
            "support_teacher_req.": "N",
            "scholarship": "",
            "returning_student": "Y",
            "media_consent": "Y",
            "learning_support": "N",
            "locker_number": "",
            "reason_for_leaving": "",
            "licence_plate": "",
            "external_tuition": "N",
            "international_stud.": "",
            "drivers_licence": "",
            "diet_restrictions": ""
          }
        }
      ]
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
    { 
      "currentstatus":"current",
      "includephoto":"true",
      "thumbnail":"true"
    }
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
