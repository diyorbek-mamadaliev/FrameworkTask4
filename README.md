# Test Automation Framework

## Configuration Options

### Browser Options

You can choose from the following web browsers for testing:
- `chrome`
- `edge`
- `firefox`

### Environments

You can select one of the following environments:
- `dev` (Development)
- `qa` (Quality Assurance)

### Test Suite Files

There are two test suite files available:
- `testing-all.xml` (Comprehensive Test Suite)
- `testing-smoke.xml` (Smoke Test Suite)

## Running Tests

### Positive Testing

To run positive tests, use the following command in the terminal:
```bash
mvn test -Dbrowser=<BROWSER> -Denvironment=<ENVIRONMENT> -Dsurefire.suiteXmlFiles=src/test/resources/<SUITE_XML_FILE>
```
Example:
```bash
mvn test -Dbrowser=chrome -Denvironment=dev -Dsurefire.suiteXmlFiles=src/test/resources/testing-all.xml
```

### Negative Testing

To run negative tests, use the following command in the terminal:
```bash
mvn test -Dbrowser=<BROWSER> -Denvironment=<ENVIRONMENT> -Dsurefire.suiteXmlFiles=src/test/resources/<SUITE_XML_FILE>
```
Example:
```bash
mvn test -Dbrowser=chrome -Denvironment=qa -Dsurefire.suiteXmlFiles=src/test/resources/testing-all.xml
```

## Test Configuration

- Testing is mainly performed with Chrome browser version 114.

## Maven and Dependencies

Below are the Maven dependencies used in this project:

```xml
<!-- Selenium WebDriver -->
<dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-java</artifactId>
    <version>4.14.1</version>
</dependency>

<!-- TestNG Testing Framework -->
<dependency>
    <groupId>org.testng</groupId>
    <artifactId>testng</artifactId>
    <version>7.7.0</version>
    <scope>test</scope>
</dependency>

<!-- Log4j Logging Framework -->
<dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-core</artifactId>
    <version>2.20.0</version>
</dependency>

<dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-api</artifactId>
    <version>2.20.0</version>
</dependency>

<!-- WebDriverManager -->
<dependency>
    <groupId>io.github.bonigarcia</groupId>
    <artifactId>webdrivermanager</artifactId>
    <version>5.3.2</version>
    <scope>test</scope>
</dependency>
```
