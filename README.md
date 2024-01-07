# Books_API_Tests_PostmanCollection
## - Tools I used;
#### - Postman
#### - Newman (Node.js required)
#### - Newman-reporter-htmlextra
#### - Jenkins
#### -Jenkins – JUnit test result report
#### - Jenkins mail notification

### 1- In Postman;
#### * Created Positive Tests, Negative Tests and EndToEnd Test(
##### -> User Gets the books list
##### -> User Gets the book info 
##### -> User Posts an order with bookId
##### -> User Gets the order info 
##### -> User Patches (Updates)the order 
##### -> User Gets the updated order info 
##### -> User Deletes the order 
##### -> User Gets the deleted order info  )

#### * Created tests for requests with JavaScript codes
#### * Asserted Status Code and Response Body
#### * Created variables using the Collection Environment. No need any other Postman-Environment to execute the Tests.
#### * Created random variables in the Globals Environment and cleared them all after the test execution.

### 2 -  
### 3 -  To run in parallel mode use maven test/verify/install. It wil run parallel test execution according to the tags written in Runner and TestRunner classes.

### 4 -  Run smoke tests with Jenkins using the mvn code -> mvn test -Dtest=Runner -Dcucumber.filter.tags="@smoke"
