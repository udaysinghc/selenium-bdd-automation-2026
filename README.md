### 🚀 Selenium BDD Automation Framework 2026

**Overview :**

The Selenium BDD Automation Framework 2026 is a robust, Maven-based test automation framework built using Selenium WebDriver, Cucumber (BDD), and TestNG.
It follows industry best practices such as the Page Object Model (POM) design pattern and provides rich reporting through Allure Reports. The framework is designed for scalability, maintainability, and cross-browser execution.
---

**Recommended Java Version: Java 17**
---

## Architecture & Design

- Maven-based project structure

- Behavior-Driven Development (BDD) using Cucumber

- Page Object Model (POM) for clean separation of test logic

- Test execution and parallelization using TestNG

- Environment-driven configuration (QA, Stage)

- Centralized utilities and reusable components

---

## Technology Stack

- Java 17

- Selenium WebDriver 4

- Cucumber (BDD)

- TestNG

- Maven

- Allure Reporting

- Log4j2

---

## Key Features

- Modular Maven project structure

- BDD implementation with readable Gherkin feature files

- Page Object Model for better maintainability

- Cross-browser testing (Chrome, Firefox, Edge)

- Headless browser execution support

- Environment-specific configurations

- Retry mechanism for flaky test cases

- Explicit wait and JavaScript utilities

- Centralized constants management

- Automatic screenshot capture on test failure

- Log4j2 logging (console and file)

- Detailed Allure HTML reports

---

## Project Structure (High Level)

- base – Test initialization and WebDriver setup

- config – Environment and property management

- pages – Page classes and reusable UI actions

- utils – Waits, JavaScript helpers, constants

- retryanalyzer – Retry logic for failed tests

- features – Cucumber feature files

- stepdefinitions – Step implementations and hooks

- runners – Test execution entry points

---

## Prerequisites

Ensure the following are installed:

- Java JDK 17 or higher

- Maven 3.6 or higher

- Allure Command Line

- Chrome / Firefox / Edge browser

**Verify installations:**

java -version
mvn -version

--- 

## Configuration

Environment configuration files are located under:
src/main/resources/

Example (qa.properties):

browser=chrome
url=https://www.example.com
headless=false
implicit.wait=10
explicit.wait=20
page.load.timeout=30

---

## Test Execution

**Run all tests:**

mvn clean test


**Run tests on a specific environment:**

mvn clean test -Denv=qa
mvn clean test -Denv=stage


**Run tests using tags:**

mvn clean test -Dcucumber.filter.tags="@smoke"
mvn clean test -Dcucumber.filter.tags="@regression"

---

## Reporting

Allure reports provide detailed execution insights including steps, screenshots, and logs.

**Generate report:**

allure generate target/allure-results --clean -o allure-report


**Open report:**

allure open allure-report

---

## Logging & Screenshots

Logs are generated at: logs/automation.log

Screenshots are automatically captured on test failure

Supported log levels: INFO, DEBUG, WARN, ERROR
