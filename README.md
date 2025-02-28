Dear Reviewer, 

In this file you can find instructions and explanations for the test task.

# Initial installations:

1. Please install the Postman tool.
2. Download **Airalo_Test.postman_collection.json** file from repository:
`Code > Download ZIP`. 
3. Unzip this file.
4. Go to the Postman tool.
5. Import downloaded file (Import button).
6. Go to the `Environments> Globals` and set your environmental variables
`client_id` and `client_secret`, select type `secret`


# Collection structure

Collection contains 3 requests

- GET Get packages (`Get Packages`)
- POST Make eSIM order(`Submit Order` endpoint)
- GET Check eSIM list (`Get eSIMs List` endpoint)

Each request contains: 
- Pre-request script that checking validity of the token and updates it if needed;
- Post-response scripts to check status code'

POST Make eSIM order request also contains a test that checks that correct data were sent (quantity, package id, description and type);

GET Check eSIM list request also contains tests that checks that the quantity of the eSIMs is equal to six and checks the package_id for each eSIM;

Please let me know if, for example, it was needed to consider a test scenario when we receive more than 6 esims in the GET request and it is needed to find 6 eSIMs that was posted last time.


# Test execution

You could run collection in the Postman directly

- Collection details (3 dots near Collection name) > Run Collection;
- Or you could send each request separately (SEND button)



Thank you for reviewing my test task!