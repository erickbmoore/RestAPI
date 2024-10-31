<h1>Rest API</h1>

<h2>Description</h2>

This project involves the development of a REST API for a medical facility, designed to manage patient information and medical records. Built using Visual Studio Code and tested with Postman, the API supports fundamental operations for handling patient data, including creation, retrieval, updating, and deletion of records.

## Features

- **Get Patient Medical Records**: Retrieve a patient's medical records by supplying their Social Security Number (SSN), first name, and last name.
- **Create a New Patient**: Add new patients to the system, including their SSN, first name, last name, and phone number.
- **Update Existing Patient Phone Number**: Modify a patient's phone number by verifying their identity with their SSN, first name, and last name.
- **Delete Patient Records**: Remove a patient's information and medical records from the system through their SSN and identity verification.

## API Endpoints

### 1. Get Patient Medical Records
- **Endpoint**: `GET /records`
- **Headers**:
  - `ssn`: Patient's Social Security Number
  - `firstname`: Patient's first name
  - `lastname`: Patient's last name
- **Body**:
  - `reasonforvisit`: Should be "medicalrecords"
- **Responses**:
  - `200 OK`: Returns the medical record.
  - `404 Not Found`: If the patient does not exist.
  - `401 Unauthorized`: If the name does not match the SSN.

### 2. Create a New Patient
- **Endpoint**: `POST /`
- **Headers**:
  - `ssn`: Patient's Social Security Number
  - `firstname`: Patient's first name
  - `lastname`: Patient's last name
  - `phone`: Patient's phone number
- **Responses**:
  - `200 OK`: Returns the updated patient list.

### 3. Update Existing Patient Phone Number
- **Endpoint**: `PUT /`
- **Headers**:
  - `ssn`: Patient's Social Security Number
  - `firstname`: Patient's first name
  - `lastname`: Patient's last name
- **Body**:
  - `phone`: New phone number
- **Responses**:
  - `200 OK`: Returns the updated patient information.
  - `404 Not Found`: If the patient does not exist.
  - `401 Unauthorized`: If the name does not match the SSN.

### 4. Delete Patient Records
- **Endpoint**: `DELETE /`
- **Headers**:
  - `ssn`: Patient's Social Security Number
  - `firstname`: Patient's first name
  - `lastname`: Patient's last name
- **Responses**:
  - `200 OK`: Confirms deletion of medical records.
  - `404 Not Found`: If the patient does not exist.
  - `401 Unauthorized`: If the name does not match the SSN.

<br />


<h2>Languages and Utilities Used</h2>

- <b>node.js express</b> 

<h2>Environments Used </h2>

- <b>Visual Studio Code</b>
- <b>Postman</b>

<h2>Program walk-through:</h2>

<p align="center">
Project Code Overview:  <br/>
<img src="https://imgur.com/yPUQqXe.png" height="80%" width="80%" alt="REST API"/>
<br />
<br />
GET Patient Medical Records Invalid SSN:  <br/>
<img src="https://imgur.com/vwq1E68.png" height="90%" width="100%" alt="REST API"/>
<br />
<br />
GET Patient Medical Records Invalid Name:  <br/>
<img src="https://imgur.com/e0T3mkl.png" height="90%" width="100%" alt="REST API"/>
<br />
<br />
GET Patient Medical Records Invalid Reason for Visit:  <br/>
<img src="https://imgur.com/mynPOvU.png" height="90%" width="100%" alt="REST API"/>
<br />
<br />
GET Patient Medical Records Verification Success:  <br/>
<img src="https://imgur.com/IsjreKy.png" height="90%" width="100%" alt="REST API"/>
<br />
<br />
POST Create New Patient: <br/>
<img src="https://imgur.com/GMw6XmH.png" height="90%" width="100%" alt="REST API"/>
<br />
<br />
PUT Update Existing Phone Number Invalid Name:  <br/>
<img src="https://imgur.com/Ttwlt3L.png" height="90%" width="100%" alt="REST API"/>
<br />
<br />
PUT Update Existing Phone Number Success:  <br/>
<img src="https://imgur.com/tYD8ZlC.png" height="90%" width="100%" alt="REST API"/>
<br />
<br />
DELETE Patient Record Invalid Name:  <br/>
<img src="https://imgur.com/6XNxCjT.png" height="90%" width="100%" alt="REST API"/>
<br />
<br />
DELETE Patient Record Success:  <br/>
<img src="https://imgur.com/vHcsZRz.png" height="90%" width="100%" alt="REST API"/>
<br />
<br />
  
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
