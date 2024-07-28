# Solution Analyst

# API
Terdapat beberapa API dalam pengembangan mobile apps pada Pinjaman Online, Berikut API yang digunakan pada implementasi pengembangan.

1. **User Registration API**
    
    API ini digunakan untuk melakukan registrasi user baru melalui mobile apps
    
    Method
    ```api
    POST  : https://api.xyz.com/V1.0/user/registration
    ```
    
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

2. **User Signin API**

    API ini digunakan untuk melakukan signin user yang sudah terdaftar

    Method
    ```api
    POST  : https://api.xyz.com/V1.0/user/signin
    ```

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

3. **Loan Application API**

    API ini digunakan untuk user melakukan permohonan pinjaman melalui mobile apps

    Method
    ```api
    POST  : https://api.xyz.com/V1.0/loan-application
    ```

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

4. **Loan Application Status API**

    API ini digunakan untuk user mengetahui status dari permohonan pinjaman yang diajukan melalui mobile apps

    Method
    ```api
    POST  : https://api.xyz.com/V1.0/loan-application-status
    ```

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

6. **Loan Application Notif API**

    API ini digunakan untuk memberikan notif ke user terkait status(approve / reject) permohonan pinjaman yang nantinya diinformasikan melalui email dan whatsapp

    Method
    ```api
    POST  : https://api.xyz.com/V1.0/loan-application-notif
    ```

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


7. **Loan Status API**

    API ini digunakan untuk user melihat detail pinjaman saat ini

    
    Method
    ```api
    POST  : https://api.xyz.com/V1.0/loan-notif
    ```

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
            "loanAmount": "12.000.000",
            "paid": "7.000.000",
            "debt": "5.000.000",
            "tenor": "5",
            "monthlyFee": "1.000.000",
            "status": "Active"
        }
    }
    ```

6. **Repayment API**
    
    API ini digunakan untuk melakukan pembayaran pinjaman
    
    Method
    ```api
    POST  : https://api.xyz.com/V1.0/user/repayment
    ```
    
    Request
    ```json
    {
        "transcationID": "1234567890",
        "amount": "1.000.000",
        "paymentDate": "27-07-2024"
    }
    ```

    Response
    ```json
    {
        "responseCode": "00",
        "responseMessage": "Success",
        "svcData": {
            "fullname": "Rezza Anugrah Mutiarawan",
            "amount": "1.000.000",
            "tenorTo": "5",
            "status": "Success"
        }
    }
    ```