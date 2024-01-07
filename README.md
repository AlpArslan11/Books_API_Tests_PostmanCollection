# Books_API_Tests_PostmanCollection
## - Tools I used;
#### - Postman
#### - Newman (Node.js required)
#### - Newman-reporter-htmlextra
#### - Jenkins
#### -Jenkins – JUnit test result report - newman-reporter-htmlextra
#### - Jenkins - Build periodically and E-mail notification

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
#### * Created random variables in Globals Environment and cleared them all after the test execution.

### 2 - Newman 
#### Run test with Newman CLI -> https://learning.postman.com/docs/collections/using-newman-cli/installing-running-newman/ 
#### Generated Htmlextra Reports -> https://www.npmjs.com/package/newman-reporter-htmlextra

### 3 - Automated Newman with Jenkins and sent the reports via mail 
####  Created a FreeStyle project and configured from Execute Windows Batch Command -> " newman run "Via API link" --reporters cli,htmlextra,junit --reporter-htmlextra-export newman\report.html  --reporter-junit-export newman\report.xml "
#### Configured the project to build periodically. 
#### Configured Editable Email Notification from Post-build Actions to send the Build Log and HtmlExtra Report after each Build.
#### Used Jenkins variable to hide the API key. (secret text)
#### Added JUnit Test Result Report from Post-build actions.





### 4 -  Run smoke tests with Jenkins using the mvn code -> mvn test -Dtest=Runner -Dcucumber.filter.tags="@smoke"
