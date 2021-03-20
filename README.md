# Snap NOA Integration Docs

Documentation for Snap NOA API and Integration

See our:

1. Open API specifications describing how to integrate.

2. Swagger documentation making each endpoint easy to read and understand.


### What Is This?

This is the Snap NOA Orders REST API. It's a REST API endpoint that will allow you to:

1. Create Snap NOA documents orders.
1. Get status on your orders.
1. Download the document package when available.

### Who Is This For?

The intended audience for this document is applications developers who are integrating applications to use and consume services provided by Snap NOA.

### Integrating

The service is available for use in 2 environments:

1. Test (non-prod)
2. Production

Each environment requires an API key for you to act as a client in. Each environment has a different host/base URL.

Contact us for more details.

### Getting Started

1. You will need an API key provisioned for each environment. Contact us for details.
2. Use Postman or any other suitable tool to connect to the endpoints. Use the Postman collection and the environment variables.


## CHANGELOG

Version March 2020

1. Fixed issues with API uploads failing.
2. Fixed issues with file retrieiving returning 404 errors.


3. Added Mandatory field Client Email to the Order Request 
    -This field is required for all request and should contain the email address of the client that is having a request done on their behalf
   
4. Renamed Notify Customer Name to Broker Name to clarify and improve readbility on the Client and the server side
    - All API requests should utilizy "BrokerName" as part of the SnapOrder API parameter
5. Renamed Notify Customer Email to Broker Email to clarify and improve readbility on the Client and the server side
    - All API requests should utilizy "BrokerEmail" as part of the SnapOrder API parameter
6. Renamed Notify Customer SMS to Broker SMS to clarify and improve readbility on the Client and the server side
    - All API requests should utilizy "BrokerSMS" as part of the SnapOrder API parameter

7. Added new API call GetOrder to retreive a single specific order identified by the Rerence Order number. Details included in Postman Request

8. Provided readable Rerence Order Number to all order requests (List and Individual)

9. Added new secure links on all order requests that provide the Requested file downloads. This emails are only valid for 2 hours from the moment they are requested. After that the link will become invalid. Users can request a new download link from the API (list or individual order calls)

10. Improved notifications and email content to include the Reference order number. (Order received and Order Complete Notifications)
