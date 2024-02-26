
![github repo banner](https://github.com/AlpArslan11/Books_API_Tests_PostmanCollection/assets/101150339/ed3c56ca-fdaa-4d2e-9321-7889096f47a5)
---
## 🛠️ Tools I used;
#### - Postman
#### - Newman (Node.js required)
#### - Newman-reporter-htmlextra
#### - Jenkins
#### - Jenkins – JUnit test result report 
#### - Jenkins - Build Periodically and E-mail Notification

---
###  <img align="left" alt="Coding" width="35" src="https://github.com/AlpArslan11/Books_API_Tests_PostmanCollection/assets/101150339/2363b8fd-5e6b-41e0-a602-4e43fa97cbe4"> Postman;
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
#### * Created variables using the Collection Environment. (No need any other Postman-Environment to execute the Tests.)
#### * Created random variables in Globals Environment and cleared them all after the test execution.
#### * Used Monitors to execute the tests periodically


---
### <img align="left" alt="Coding" width="30" src="https://github.com/AlpArslan11/Books_API_Tests_PostmanCollection/assets/101150339/0d1025d8-e272-4ecb-ab45-4babf6102142"> Newman 
#### Run test with Newman CLI -> https://learning.postman.com/docs/collections/using-newman-cli/installing-running-newman/
Newman CLI -> `newman`<br>
`newman run "Location_Of_Collection.json" –e “locationOfEnvironment”`
#### Generated Htmlextra Reports -> https://www.npmjs.com/package/newman-reporter-htmlextra
Newman CLI ->  `newman run "Location_Of_Collection.json" --reporters cli,htmlextra`

---
### <img align="left" alt="Coding" width="70" src="https://github.com/AlpArslan11/Books_API_Tests_PostmanCollection/assets/101150339/c85c752a-bfb7-4b2d-a41b-e2a2bfb91494"> Automated Newman with Jenkins and sent the reports via mail 
####  Created a FreeStyle project and configured from Execute Windows Batch Command -> 
`newman run "Via API link" --reporters cli,htmlextra,junit --reporter-htmlextra-export newman\report.html  --reporter-junit-export newman\report.xml`
#### Configured the project to build periodically. 
#### Configured Editable Email Notification from Post-build Actions to send the Build Log and HtmlExtra Report after each Build.
#### Used Jenkins variable to hide the API key. (secret text)
#### Added JUnit Test Result Report from Post-build actions in Jenkins.
---
![image](https://github.com/AlpArslan11/Books_API_Tests_PostmanCollection/assets/101150339/7edea943-ab5f-435e-8797-f0dcd0ddbcb6)

![image](https://github.com/AlpArslan11/Books_API_Tests_PostmanCollection/assets/101150339/d57b5f35-4196-432f-825d-abc6fcf2a6b5)

![image](https://github.com/AlpArslan11/Books_API_Tests_PostmanCollection/assets/101150339/3f4ac9ac-7a9e-4d81-920c-cfbe1cddc2fa)

![image](https://github.com/AlpArslan11/Books_API_Tests_PostmanCollection/assets/101150339/faee3fd4-dd87-4b88-89c1-fa26a5f48053)

![image](https://github.com/AlpArslan11/Books_API_Tests_PostmanCollection/assets/101150339/3334d0b1-f7d6-4f33-baf7-0b98ea87f6f4)

![image](https://github.com/AlpArslan11/Books_API_Tests_PostmanCollection/assets/101150339/931ff256-e286-45ba-b692-9e3c26234e7e)

![image](https://github.com/AlpArslan11/Books_API_Tests_PostmanCollection/assets/101150339/8f75bf40-2ef0-4ccf-9c1b-e0ffb4afbc03)

![image](https://github.com/AlpArslan11/Books_API_Tests_PostmanCollection/assets/101150339/c4284f28-62e2-4346-aa41-5886c3d15703)
