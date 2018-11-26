# Search GST TaxPayer API
GST TaxPayer API by [Masters India](https://www.mastersindia.co/) helps the customer to integrate the [GST number search API](https://www.mastersindia.co/gst-number-verification-api-bulk-utility/) on their website or application. Using this API user can know the details of GSTIN Number  and other details too for example date of registration, type of business, type of taxpayer ( regular or quarterly based), name of the city where the GSTIN was registered in and also the status of taxpayer (active or inactive whichever the case may be.)

**API Method**: GET
URL: https://commonapi.mastersindia.co/commonapis/searchgstin

**Headers**

| Property | Sample Value| Description |
| --- | --- | --- |
| Content-Type | application/json | Content Type
| Authorization | Bearer 3d80fd20d4540798919e48d7c872d09c8eb93036 | Access Token Received After Authentication
| Client_id | 242324v424244255545343 | Client Id Provided by Autotax

**Query Parameters**

| Property | Sample Value| Description |
| --- | --- | --- |
| gstin | 12GSPTN0792G1Z2 | GSTIN of TaxPayer to Search for.

**Sample for URL Based API**:
URL: https://commonapi.mastersindia.co/commonapis/searchgstin?gstin=GSTINOfTaxPayerToSearch

**Sample Header for Above Request**

**Content-Type** : application/json
**Authorization** : Bearer 3d80fd20d4540798919e48d7c872d09c8eb93036
**Client_ID** : 242324v424244255545343

**Sample Response JSON**

{"error":false,"data":"{\"rgdt\":\"01\/07\/2017\",\"ctb\":\"Public Limited Company\",\"sts\":\"Active\",\"lgnm\":\"Masters TN TaxPayer 2 Ltd\",\"stj\":\"ADYAR\",\"ctj\":\"ALLAHABAD-I\",\"dty\":\"Regular\",\"cxdt\":\"\",\"gstin\":\"12GSPTN0507G1Z3\"}"} 

## View and Track Returns API

View and Track Returns API by Masters India can be purchased by any company or individual. This helps the users to track the status of their Return so filed (current or previous) details by just entering the financial year and GSTIN of the taxpayer. 

**API Method**: GET

URL: https://commonapi.mastersindia.co/commonapis/trackReturns

**Headers**

| Property | Sample Value| Description |
| --- | --- | --- |
| Content-Type | application/json | Content Type
| Authorization | Bearer 3d80fd20d4540798919e48d7c872d09c8eb93036 | Access Token Received After Authentication
| Client_id | 242324v424244255545343 | Client Id Provided by Autotax

**Query Parameters**

| Property | Sample Value| Description |
| --- | --- | --- |
| gstin | 12GSPTN0792G1Z2 | GSTIN of TaxPayer to Search for.
| fy | 2018-19 | Financial Year

**Sample for URL Based API:**
URL: https://commonapi.mastersindia.co/commonapis/trackReturns?gstin=GSTINOfTaxPayerToSearch&fy=Financial Year

**Sample Header for Above Request**

Content-Type : application/json
Authorization : Bearer 3d80fd20d4540798919e48d7c872d09c8eb93036
client_id : 242324v424244255545343

**Sample Response JSON**

{"error":false,"data":"{\"EFiledlist\":[{\"valid\":\"Y\",\"mof\":\"ONLINE\",\"dof\":\"02-03-2018\",\"rtntype\":\"GSTR3B\",\"ret_prd\":\"012018\",\"arn\":\"AA150118002746G\",\"status\":\"Filed\"},{\"valid\":\"Y\",\"mof\":\"ONLINE\",\"dof\":\"02-02-2018\",\"rtntype\":\"GSTR3B\",\"ret_prd\":\"112017\",\"arn\":\"AA151117002990K\",\"status\":\"Filed\"},{\"valid\":\"Y\",\"mof\":\"ONLINE\",\"dof\":\"02-02-2018\",\"rtntype\":\"GSTR3B\",\"ret_prd\":\"122017\",\"arn\":\"AA151217002550U\",\"status\":\"Filed\"},{\"valid\":\"Y\",\"mof\":\"ONLINE\",\"dof\":\"24-11-2017\",\"rtntype\":\"GSTR3B\",\"ret_prd\":\"092017\",\"arn\":\"AA150917002033N\",\"status\":\"Filed\"},{\"valid\":\"Y\",\"mof\":\"ONLINE\",\"dof\":\"24-11-2017\",\"rtntype\":\"GSTR3B\",\"ret_prd\":\"102017\",\"arn\":\"AA151017001650X\",\"status\":\"Filed\"},{\"valid\":\"Y\",\"mof\":\"ONLINE\",\"dof\":\"07-11-2017\",\"rtntype\":\"GSTR2\",\"ret_prd\":\"072017\",\"arn\":\"AA150717006731D\",\"status\":\"Filed\"},{\"valid\":\"Y\",\"mof\":\"ONLINE\",\"dof\":\"11-10-2017\",\"rtntype\":\"GSTR3B\",\"ret_prd\":\"082017\",\"arn\":\"AA150817002245G\",\"status\":\"Filed\"},{\"valid\":\"Y\",\"mof\":\"ONLINE\",\"dof\":\"09-10-2017\",\"rtntype\":\"GSTR1\",\"ret_prd\":\"072017\",\"arn\":\"AA150717005733A\",\"status\":\"Filed\"},{\"valid\":\"Y\",\"mof\":\"ONLINE\",\"dof\":\"28-08-2017\",\"rtntype\":\"GSTR3B\",\"ret_prd\":\"072017\",\"arn\":\"AA1507170025189\",\"status\":\"Filed\"}]}"}

## Get Count API

Get Count API by Masters India helps the company who has integrated this API  to know how many API counts have been hit by the users. This API will help the company to know if they have exhausted the APIs so purchased for example If a company purchases 1,00,000 APIs from Masters India and the user has hit 99,000 APIs count then the company will come to know that there are only 1,000 APIs are left with them which can be used by the GSTIN taxpayer.

**API Method**: GET

URL: https://commonapi.mastersindia.co/commonapis/countapi

**Headers**

| Property | Sample Value| Description |
| --- | --- | --- |
| Content-Type | application/json | Content Type
| Authorization | Bearer 3d80fd20d4540798919e48d7c872d09c8eb93036 | Access Token Received After Authentication
| Client_id | 242324v424244255545343 | Client Id Provided by Autotax

**Query Parameters**

| Property | Sample Value| Description |
| --- | --- | --- |
| gstin | 12GSPTN0792G1Z2 | GSTIN of TaxPayer to Search for.
| fy | 2018-19 | Financial Year

**Sample for URL Based API**:
URL: https://commonapi.mastersindia.co/commonapis/countapi?action=count

**Sample Header for Above Request**

**Content-Type** : application/json
**Authorization** : Bearer 3d80fd20d4540798919e48d7c872d09c8eb93036
**client_id** : 242324v424244255545343

**Sample Response JSON**

{"error":false,"count":"12564"}

## Authentication

Authentication API by Master India supports access-token based authentication. After user login request, our API generates an access token to a user after validating his credentials. This key can be used in subsequent requests but expires after a set time interval after which it must be requested again by re-initiating a login. The key needs to be passed as a request parameter.

**API Method**: POST

URL: https://commonapi.mastersindia.co/oauth/access_token

**Headers**

| Property | Sample Value| Description |
| --- | --- | --- |
| Content-Type | application/json | Content Type

**Body Parameters**

| Property | Sample Value| Description |
| --- | --- | --- |
| Cusername | sampletest@mastersindia.co | Username Provided by Autotax
| password | Test@12345 | User Password
| client_id | NASgLPiRQYlYt0E4dW | Client Id Provided by Autotax
| client_secret | BMUR179a3jv1d24UgE0Osqw23 | Secret Key Provided by Autotax
| grant_type | password | Grant Type  Value should be password

**Sample for URL Based API:**

URL:https://commonapi.mastersindia.co/oauth/access_token

**Sample Header for Above Request**

**Content-Type** : application/json

**Sample Request JSON**

{
"username": "sampletest@mastersindia.co",
"password" : "Test@12345",
"client_id":"NASgLPiRQYlYt0E4dW",
"client_secret":"BMUR179a3jv1d24UgE0Osqw23",
"grant_type":"password"
}

**Sample Response JSON:**

{"access_token":"3d80fd20d4540798919e48d7c872d09c8eb93036","expires_in":14400,"token_type":"bearer"}
