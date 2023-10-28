# ONESTOP-BILLING

This microservice contains subscription and billing entities and generates bills every 30 days.

### Contact Information
- Name: Bibhu
- Email: [bibhusunder.b@prodapt.com](mailto:bibhusunder.b@prodapt.com)

### Project Link
- [Github Link](https://github.com/bibhup04/onestop/tree/main/onestop-billing)

### Server Information
Generated server URL: `http://localhost:8083`

## Tags

### Update controller
It updates the account and payment status.

### Subscription controller
It keeps a record of subscriptions and creates bills.

## Paths

### /subscribe/update/status
- Method: POST
- Summary: Update Account Status
- Description: This method gets called periodically and updates the account status from Active to Suspend or Terminate based on the payment status.
- Operation ID: updateStatus

### /subscribe/update/payment
- Method: POST
- Summary: Update Payment Status
- Description: This method receives the details of the user and updates the payment status to paid.
- Operation ID: receiveCollectionDTO

### /subscribe/plan
- Method: POST
- Summary: Subscribe plans
- Description: Receives user and plan details and adds those details to the database.
- Operation ID: subscribePlan

### /subscribe/end/subscription
- Method: POST
- Summary: End Subscription
- Description: This method ends the subscription for the given user.
- Operation ID: endSubscribedPlan

### /subscribe/create-invoice
- Method: POST
- Summary: Create Invoice
- Description: This method sends the GenerateInvoiceDTO to the invoice service to generate an invoice.
- Operation ID: createInvoice

### /subscribe/user/subscription
- Method: GET
- Summary: Display Subscription
- Description: This method displays the subscribed plan of the logged-in user.

### /subscribe/user/bill
- Method: GET
- Summary: Display Bill
- Description: This method displays the last bill of the user.

### /subscribe/bill
- Method: GET
- Summary: Generate Bills
- Description: This method generates a bill when a user ends a subscription manually.

### /subscribe/all
- Method: GET
- Operation ID: getAllSubscriptions

## Schemas

### CollectionDTO
- subscriptionId (integer)
- userId (integer)
- amountCollected (number)
- billId (integer)

### SubscribeDTO
- familyId (integer)
- userId (integer)
- planId (integer)
- finalPrice (number)

### Subscription
- subscriptionId (integer)
- familyId (integer)
- userId (integer)
- planId (integer)
- finalPrice (number)
- createdAt (string, date-time)
- endDate (string, date-time)
- status (string)
- autoRenewal (boolean)

### GenerateInvoiceDTO
- billId (integer)
- userId (integer)
- planId (integer)
- finalPrice (number)

### Billing
- billingId (integer)
- subscriptionId (integer)
- userId (integer)
- createdAt (string, date-time)
- amount (number)
- paymentStatus (string)
