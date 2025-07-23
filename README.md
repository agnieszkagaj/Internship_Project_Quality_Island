# Automated Tests for Web Application - Internship at Quality Island

# Overview

This repository contains an automated regression testing project for an e-commerce web application. The project was developed during an internship at Quality Island by a team of 10 interns. The tests are structured and maintained to support continuous integration and efficient test execution.

Each team member was responsible for a specific scope of test cases — relevant modules were distributed among the members. For each module, the intern testers were responsible for designing and implementing automated regression and end-to-end (E2E) tests to verify key functionalities, report bugs, and provide a reliable, fail-proof test suite.

# Technologies Used

* JAVA
* Selenium WebDirver
* Maven
* TestNG
* Allure
* Git / GitHub (VSC)
* IntelliJ IDEA

# Features

* *Page Object Model (POM)* - ensures clear, reliable, modular and maintainable architecture
* *Page Factory* - simplifies the implementation of POM design pattern, reduces boilerplate code for element initialization, improves the structure and maintainability of test code, enhances readability and scalability by separating page logic from test logic
* *Resources file* - centralizes global configuration data (e.g. base URL, logins, passwords, e-mail addresses, browsers), enabling easier management and improved reusability
* *ExtentReport class* - a centralized utility for generating reports form each test execution
* *Waits class* - a global utility class containing custom wait operations, improves code reusability, keeps page classes clean by abstracting wait logic into seperate Waits class, enhances test stability for the web application which involves asychronous behaviour (e.g. waiting for a certain attribute to change)
* *TestBase class* - a centralised base class for test setup and teardown, eliminates code duplication across test classes, improves code reusability, ensures consistent test environment and easier maintenance 
* *Stuctured and consistent layout* - each class is divided into clear sections (i.e. configuration settings, web elements repository, operations on web elements)
* *Test annotations* - improve code readability by providing clear descriptions for each test method

# My Contribution
The sope of my work involved "Sales" and "Tools" modules (originally: "Sprzedaż" and "Narzędzia").
The modules are a part of an e-commerce web application that enables end-users to create, configure and sell courses, digital products and other services.

The tests I developed include:

### 1. Automated reggresion tests verifying:
* Page titles
* URLs
* Visibility, clickablility and default settings of UI elements
* Relevant files:
    * [Sales Pages](https://github.com/agnieszkagaj/Internship_Project_Quality_Island/tree/master/src/test/java/pages/sprzedaz) -> excluding KodyZnizkoweDodajNowyPage
    * [Sales Tests](https://github.com/agnieszkagaj/Internship_Project_Quality_Island/tree/master/src/test/java/tests/sprzedazTests)
    * [Tools Pages](https://github.com/agnieszkagaj/Internship_Project_Quality_Island/tree/master/src/test/java/pages/narzedzia)
    * [Tools Tests](https://github.com/agnieszkagaj/Internship_Project_Quality_Island/tree/master/src/test/java/tests/narzedziaTests)

### 2. End-to-end (E2E) automated test based on client requirements. Test scenario: adding new user ("Users" > "Create urser" modules):

* Filling in the user name field - requirements: at lest 12 characters and one upper-case letter
* Filling in e-mali adddress field
* Filling in first name and last name fields
* Changing language settings to Polish
* Clicking the "Generate password" button - verifying that the generated password is labeled as "Strong"
* Verifying that "Send notification to the user" checkbox is chcecked by default
* Clicking "Create user" button
* Verifying that the user has been successfully created by checking if the user appears in the user list - I implemented an iteration method for searching user data in the table that works independently of the current data sorting order
* Relevant files:
    * [Users Page](https://github.com/agnieszkagaj/Internship_Project_Quality_Island/blob/master/src/test/java/pages/uzytkownicy/UzytkownicyPage.java)
    * [Create User Page](https://github.com/agnieszkagaj/Internship_Project_Quality_Island/blob/master/src/test/java/pages/uzytkownicy/UtworzUzytkownikaPage.java)
    * [Users Tests](https://github.com/agnieszkagaj/Internship_Project_Quality_Island/blob/master/src/test/java/tests/uzytkownicyTests/UzytkownicyPageTest.java) -> see: @Test (priority = 20) public void weryfikacjaUtworzeniaNowegoUzytkownika()

# ! Important Notice !
The purpose of the repository is to showcase my individual contributions to the client's project during my internship at Quality Island.

All sensitive data (such as usernames, passwords, URLs, and the client's name) has been anonymized to ensure data privacy and security. 

The test scenarios and structure remain representative of the actual implementation and are shared for reference and educational purposes only.


