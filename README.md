# SolutionAnalyst

# API
- API User Registration
    - POST  : http://api.xyz.com/V1.0/user/registration
    
    Request
    ```json
    {
        "username": "string",
        "password": "string",
        "email": "user@example.com",
        "phoneNumber": "string",
        "ktp": "https://api.xyz.com/V1.0/photo-upload/KTP.jpg",
        "selfieKtp": "https://api.xyz.com/V1.0/photo-upload/selfieKTP.jpg"
    }
    ```

    Response
    ```json
    {
        "responseCode": "00",
        "responseMessage": "Success",
        "svcData": {
            "nama": "Rezza",
            "username": "rezza6789",
            "email": "rezza.anugrahm1@gmail.com",
            "phoneNo": "81250470845"
        }
    }
    ```

- API User Sign
    - POST  : http://api.xyz.com/V1.0/user/sign

    Request
    ```json
    {
        "username": "rezza6789",
        "password": "abc1234"
    }
    ```

    Response
    ```json
    {
        "responseCode": "00",
        "responseMessage": "Success"
    }
    ````

- API Loan Application
    - POST  : http://api.xyz.com/V1.0/loan-application

    Request
    ```json
    {
        "userID": "1234567890",
        "fullname": "Rezza Anugrah Mutiarawan",
        "email": "rezza.anugrahm1@gmail.com",
        "phoneNumber": "81250470845",
        "loanAmount": "10.000.000",
        "employeeStatus": "Karyawan swasta",
        "ktpNo": "1234567890",
        "additionalInfo": "string"
    }
    ```

    Response
    ```json
    {
        "responseCode": "00",
        "responseMessage": "Success",
        "svcData": {
            "userID": "1234567890",
            "fullname": "Rezza Anugrah Mutiarawan",
            "loanAmount": "10.000.000",
            "phoneNo": "81250470845",
            "tenor": "12",
            "startTenor": "27-08-2025",
            "endTenor": "27-07-2026",
            "status": "Sending"
        }
    }
    ```

- API Loan Application Status
    - POST  : http://api.xyz.com/V1.0/loan-application-status

    Request
    ```json
    {
    "userID": "1234567890",
    "fullname": "Rezza Anugrah Mutiarawan"
    }
    ```

    Response
    ```json
    {
        "responseCode": "00",
        "responseMessage": "Success",
        "svcData": {
            "userID": "1234567890",
            "fullname": "Rezza Anugrah Mutiarawan",
            "status": "Checking"
        }
    }
    ```

- API Loan Application Notif
    - POST  : http://api.xyz.com/V1.0/loan-application-notif

    Request
    ```json
    {
        "userID": "1234567890",
        "fullname": "Rezza Anugrah Mutiarawan",
        "email": "rezza.anugrahm1@gmail.com",
        "phoneNo": "81250470845"
    }
    ```

    Response
    ```json
    {
        "responseCode": "00",
        "responseMessage": "Success",
        "svcData": {
            "userID": "1234567890",
            "fullname": "Rezza Anugrah Mutiarawan",
            "loanAmount": "10.000.000",
            "phoneNo": "81250470845",
            "tenor": "12",
            "startTenor": "27-08-2025",
            "endTenor": "27-07-2026",
            "status": "Approved"
        }
    }
    ```

