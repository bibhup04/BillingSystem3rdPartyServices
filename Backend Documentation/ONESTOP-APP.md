# ONESTOP-APP

This microservice contains all the plan details and user family details.

### Contact Information
- Name: Bibhu
- Email: [bibhusunder.b@prodapt.com](mailto:bibhusunder.b@prodapt.com)

### Project Link
- [Github Link](https://github.com/bibhup04/onestop/tree/main/onestop-app)

### Server Information
Generated server URL: `http://localhost:8082`

## Tags

### App Controller
Allow users to login and register.

## Paths

### /app/plan/buy
- Method: POST
- Summary: Buy a Plan
- Description: Allows users to buy a plan (Identifies the user from the token).
- Operation ID: buyPlan

### /app/invoice-details
- Method: POST
- Summary: Invoice Details
- Description: Receives a list of generateInvoiceDTOs and returns a list of InvoiceDTO with all the details to generate an invoice.
- Operation ID: generateInvoice

### /app/delete/member
- Method: POST
- Operation ID: deleteFamilyMember

### /app/addMember
- Method: POST
- Summary: Add Members
- Description: Identifies the user from the token and adds members to the family account of the user.
- Operation ID: addFamilyMember

### /app/user
- Method: GET
- Summary: User Details
- Description: Fetches the token from the header, sends the token to Auth-service, gets user details, and creates an entry in the family table if there is no entry for that user.
- Operation ID: createFamilyDetails

### /app/home
- Method: GET
- Summary: Home Page
- Description: This endpoint doesn't require authentication. It displays the homepage directly.
- Operation ID: getPlans

### /app/getMember
- Method: GET
- Summary: Display Members
- Description: Identifies the user from the token and adds members to the family account of the user.
- Operation ID: getAllMember

## Schemas

### PlanIdDTO
- planId (integer)

### GenerateInvoiceDTO
- billId (integer)
- userId (integer)
- planId (integer)
- finalPrice (number)

### InvoiceDTO
- planId (integer)
- planDescription (string)
- price (number)
- otts (array of Ott)
- emailId (string)
- nameAndPhones (array of NameAndPhone)

### NameAndPhone
- name (string)
- phoneNo (string)

### Ott
- ottId (integer)
- ottName (string)
- planTitle (string)

### NewMemberDTO
- members (array of NameAndPhone)

### UserDTO
- id (integer)
- name (string)
- email (string)
- phoneNo (string)
- password (string)
- role (string)
- status (string)

### PlanDTO
- planId (integer)
- billingCycle (integer)
- memberCount (integer)
- planDescription (string)
- ottCount (integer)
- streams (integer)
- price (number)
- discount (number)
- finalPrice (number)
- otts (array of Ott)
