# ONESTOP-INVOICE

This microservice generates an invoice and sends the invoice to the user via mail.

### Contact Information
- Name: Bibhu
- Email: [bibhusunder.b@prodapt.com](mailto:bibhusunder.b@prodapt.com)

### Project Link
- [Github Link](https://github.com/bibhup04/onestop/tree/main/onestop-invoice)

### Server Information
Generated server URL: `http://localhost:8085`

## Tags

### Invoice controller
It creates an invoice and sends the invoice via mail to the user.

## Paths

### /invoice/generate-invoice
- Method: POST
- Summary: Generate Invoice
- Description: It receives billId, SubscriptionId, and userID and sends the userId to the authService to receive all the details and generate an invoice and sends it to the user via mail.
- Operation ID: generateInvoice

### /invoice/displayPdf
- Method: POST
- Summary: Display PDF
- Description: It receives invoiceId and returns the invoice.
- Operation ID: displayPdf

### /invoice/create
- Method: POST
- Summary: Create Invoice
- Description: It is a test endpoint to create an invoice for given data.
- Operation ID: generateNewPDF

### /invoice/get/invoice
- Method: GET
- Summary: User Details
- Description: It is a test endpoint to test feing communication and receives user details.
- Operation ID: createFamilyDetails

## Schemas

### GenerateInvoiceDTO
- billId (integer)
- userId (integer)
- planId (integer)
- finalPrice (number)

### InvoiceIdDTO
- invoiceId (integer)

### InvoiceDTO
- planId (integer)
- planDescription (string)
- price (number)
- otts (array)
- emailId (string)
- nameAndPhones (array)

### NameAndPhone
- name (string)
- phoneNo (string)

### Ott
- ottId (integer)
- ottName (string)
- planTitle (string)

### Invoice
- id (integer)
- planId (integer)
- planDescription (string)
- finalPrice (number)
- emailId (string)
- userId (integer)
- userName (string)
- billId (integer)
- path (string)
- createdAt (string)
