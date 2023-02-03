# Lambda-AWS
PUt &amp; GET request from API Rest to DynamoDB via Lambda functions.


## Missions -

### mission 1 - 
develop Rest API that will be responsible to store the product user’s IDs. 
Rest API methods:
1)	Put – insert a new ID into the company Dynamo DB table.
2)	Get – Create the proper lambda function to handle get requests from the server and will return a simple JSON response that will indicate whether the ID is in the DB or not.

### Mission 2 - 
deploy a static website using a NGINX server on an Ubuntu machine.

## Usage

AWS services, Python and Dynamo DB .

## Contributing
 * Mission 1 - 
1. AWS region - ew-west-2
2. DynamoDB table name - customer_ids
 ** PUT request - 
3. PUT request function - insert new ID into the company DynamoDB table

    3.1. use boto3,json librarise

    3.2. the function serch the customer_ids table and add the user ID to there.

    3.3. if the table name was found - ID insert to customer_ids table and we will receive json with status code 200, and msg body for sucssesful.

    3.4. if the table name not found - user will not insert into customer_ids table, and we will receive json with status code 400, and msg body for table not found. 

    3.5. **running via Postman API Platform code **

    here you can see the Postman command for run PUT request function with ID "211" -
    curl --location --request PUT 'https://2j8o0g1s0l.execute-api.eu-west-2.amazonaws.com/dev/customers/211'
         **running via Postman API Platform code **

     **GET request 
4. GET request function - search ID in customer_ids table

    4.1. use boto3,json,botocore librarise 

    4.2. the function recive from user an ID, serch him in customer_ids table and return json msg.

    4.3. if table exsist and user found there - we will receive json with user id.

    4.4. if table exsists but user not - we will receive json with status code 404, and msg  for customer ID not found.

    4.5. if table not exsists- we will receive json with status code 400, and msg  for table not found.

    4.6. **running via Postman API Platform code **

    the Postman command for run GET request function with ID "211" -
    curl --location --request GET 'https://2j8o0g1s0l.execute-api.eu-west-2.amazonaws.com/dev/customers/211'
         **running via Postman API Platform code **


  * Mission 2: 
1. Ubuntu machine 
2. instance type - t2.micro
3.CloudeZone IP 147.234.32.17 over Http permissions.

NGINX server url - 
http://3.11.153.7/cloudzone/index.html

command via postman:
curl --location --request GET 'http://3.11.153.7/index.html'

## Prerequisite knowledge
Python, AWS Services (Lambda, API Gateway, Dynamo DB, IAM,EC2)
