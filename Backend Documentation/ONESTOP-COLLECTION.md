# ONESTOP-COLLECTION

This microservice runs the collection cycle of 14 days and sends collection details to the Billing Microservice.

### Contact Information
- Name: Bibhu
- Email: [bibhusunder.b@prodapt.com](mailto:bibhusunder.b@prodapt.com)

### Project Link
- [Github Link](https://github.com/bibhup04/onestop/tree/main/onestop-collection)

### Server Information
Generated server URL: `http://localhost:8086`

## Tags

### Collection controller
It collects the amount after payment and updates the payment status to paid. It suspends and terminates the account if the user does not make any payment till the end of the collection cycle.

## Paths

### /collection/update/status
- Method: POST
- Summary: Update Account Status
- Description: It is a test method to check whether the account status is changing from active to suspend, suspend to terminate if the bill is not paid.
- Operation ID: updateSubscriptionStatus

### /collection/payment
- Method: POST
- Summary: Receive Collection
- Description: Receives the collection amount, billId, and subscription id and sends them to the billing microservice to update.
- Operation ID: receiveCollectionDTO

### /collection/user
- Method: GET
- Summary: User Details
- Description: Receives user and plan details and adds those details to the Database.
- Operation ID: userDetails

## Schemas

### CollectionDTO
- subscriptionId (integer)
- userId (integer)
- amountCollected (number)
- billId (integer)

### UserDTO
- id (integer)
- name (string)
- email (string)
- phoneNo (string)
- password (string)
- role (string)
- status (string)
