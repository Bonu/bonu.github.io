```
Feature: Home Page
  In order to test Home Page of application
  As a Registered user
  I want to specify the features of home page

  Background: flow till home page
    Given user is on Application home page
    When user enters username
    And user enters password
    And user clicks on login button
    Then user is on Application home page

  Scenario: Home Page Default content
    Then user gets a GitHub bootcamp section

  Scenario: GitHub Bootcamp Section
    When user focuses on GitHub Bootcamp Section
    Then user gets an option to setup git

  Scenario: Top Banner content
    When user focuses on Top Banner
    Then user gets an option of home page

```

All the Steps mentioned in the Background keyword will be executed before each Scenario or Scenario Outline in a Feature file.


```
Scenario: Existing user Verification
    Given user is on Application landing page
    Then we verify user "Shankar" with password "P@ssword123", phone "999" exists
    Then we verify user "Ram" with password "P@ssword456", phone " 888" exists
    Then we verify user "Sham" with password "P@ssword789", phone "666" exists
    
Scenario: Existing user Verification
 
Given user is on Application landing page
    Then we verify following user exists
      | name    | email           | phone |
      | Shankar | sgarg@email.com | 999   |
      | Ram     | ram@email.com   | 888   |
      | Sham    | sham@email.org  | 666   |
      
 ```     
 
 A Scenario Outline is run once for each row in the Examples section beneath it (not counting the first row of column headers).
 
 ```
 Scenario Outline: Login fail - possible combinations
    Given user is on Application landing page
    When user clicks on Sign in button
    Then user is displayed login screen
    When user enters "<UserName>" in username field
    And user enters "<Password>" in password field
    And user clicks Sign in button
    Then user gets login failed error message

    Examples: 
      | UserName      | Password      |
      | wrongusername | 123456        |
      | ShankarGarg   | wrongpassword |
      | wrongusername | wrongpassword |
      
  ```
  
  
      
      
    
