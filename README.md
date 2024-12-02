# API Testing Project with TestNG and RestAssured

## Objective
This project demonstrates API testing using *TestNG* and *RestAssured*, focusing on:
- Implementing temporary solutions.
- Reducing technical debt.
- Isolating problematic code without refactoring.

---

## Prerequisites
- Java JDK 8 or higher.
- Maven installed on your system.
- IDE (e.g., IntelliJ IDEA, Eclipse).
- Git for version control.

---

## Project Setup

### 1. Clone the Repository
```bash
git clone <repository-url>
cd <repository-folder>
<dependencies>
    <dependency>
        <groupId>org.testng</groupId>
        <artifactId>testng</artifactId>
        <version>7.4.0</version>
        <scope>test</scope>
    </dependency>
    <dependency>
        <groupId>io.rest-assured</groupId>
        <artifactId>rest-assured</artifactId>
        <version>4.4.0</version>
    </dependency>
</dependencies>

<!DOCTYPE suite SYSTEM "https://testng.org/testng-1.0.dtd">
<suite name="API Testing Suite">
    <test name="API Tests">
        <classes>
            <class name="com.example.api.ApiTest"/>
        </classes>
    </test>
</suite>
mvn test
@Test
public void testGetRequest() {
    Response response = RestAssured.get("https://jsonplaceholder.typicode.com/posts/1");
    Assert.assertEquals(response.getStatusCode(), 200);
}
