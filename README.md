# Testing Rediff Selenium Automation Framework

This project is a Selenium-based automation framework designed to test Rediff's web application functionalities such as managing portfolios, managing stocks, and sessions. The framework is implemented in Java, using TestNG for test orchestration and ExtentReports for reporting. It supports modular test data configuration via JSON and Excel files.

---

## Project Structure

### **1. Main Codebase (src/main/java)**
- **keywords**
  - `ApplicationKeywords.java`: Contains application-specific reusable keywords.
  - `GenericKeywords.java`: Provides generic utility functions for the framework.
  - `ValidationKeywords.java`: Includes validation-specific reusable methods.
- **reports**
  - `ExtentManager.java`: Manages ExtentReports for generating HTML test reports.
- **utils**
  - `ExcelUtils.java`: Handles Excel data operations (reading and writing).

### **2. Test Components (src/test/java)**
- **base**
  - `BaseTest.java`: Contains common setup and teardown methods for all test cases.
- **listeners**
  - `MyTestNGListener.java`: Implements TestNG listeners for advanced test monitoring.
- **runner**
  - `DataUtil.java`: Utility class for test data management.
  - `ExcelReader.java`: Reads test data from Excel files.
  - `JSONRunner.java`: Processes JSON test data files.
  - `TestNGRunner.java`: Configures and runs TestNG test suites.
  - `Runner.java`: Base runner class for orchestrating tests.
- **testcases**
  - `CreatePortfolioTest.java`: Tests portfolio creation functionality.
  - `ManagePortfolioTest.java`: Tests managing portfolios.
  - `ManageSessionTest.java`: Validates session management.
  - `ManageStocksTest.java`: Tests stock management functionalities.

### **3. Resources (src/test/resources)**
- **projectJSONs**
  - **suites**
    - `portfoliosuite.json`: Defines the portfolio test suite.
    - `stocksuite.json`: Defines the stocks test suite.
  - **testJSONData**: Contains JSON files with test data.
  - **XLS_Data**: Contains Excel files with test data.
- `classmethods.json`: Configuration for reusable methods.
- `testconfig.json`: General test configurations.
- `Project.properties`: Project-level configuration file.
- `PortfolioSuite.xml`: TestNG XML for the portfolio suite.
- `StockManage.xml`: TestNG XML for the stock management suite.
- `testng.xml`: Master TestNG suite configuration file.

---

## Features
- **Modular Framework:** All functionalities and configurations are modular for ease of maintenance and scalability.
- **Multi-Browser Support:** Compatible with Chrome and Firefox.
- **Parallel Execution:** Supports running test suites in parallel.
- **Data-Driven:** Uses JSON and Excel files to drive test data.
- **Advanced Reporting:** Generates detailed HTML reports using ExtentReports.
- **TestNG Integration:** Leverages TestNG for efficient test execution and management.

---

## Getting Started

### **Prerequisites**
- JDK 1.8 or higher
- Maven
- Selenium WebDriver
- TestNG

### **Setup Instructions**
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory and import it into your preferred IDE (e.g., IntelliJ, Eclipse).
3. Update the `Project.properties` file with the required configuration (e.g., browser, URL).
4. Add test data in the JSON or Excel files located under `src/test/resources/projectJSONs`.
5. Build the project using Maven:
   ```bash
   mvn clean install
   ```

---

## How to Run Tests

### **Using TestNG XML**
1. Open any of the predefined TestNG XML files:
   - `testng.xml`
   - `PortfolioSuite.xml`
   - `StockManage.xml`
2. Right-click on the XML file and select **Run As > TestNG Suite**.

### **Command-Line Execution**
1. Use Maven to run tests:
   ```bash
   mvn test -DsuiteXmlFile=<suite-file.xml>
   ```
   Example:
   ```bash
   mvn test -DsuiteXmlFile=PortfolioSuite.xml
   ```

---

## Reports
- Reports are generated in the `reports` directory.
- Use the generated HTML file to view detailed test execution reports.

---

## Contribution
1. Fork the repository.
2. Create a new branch for your feature or bug fix:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Description of changes"
   ```
4. Push to your fork and create a pull request.

---


