# Internet Speed Test Automation Framework

## 🚀 Objective
Automate the process of running internet speed tests (Download, Upload, Combined, Latency) on a mobile app using LambdaTest real device cloud.

## 🧠 Thought Process
- Build a reusable test framework
- Ensure scalability using Page Object Model and TestNG
- Enable parallelism and retries to maximize efficiency and reliability
- Encrypt secrets and follow best practices for clean code and logs

## 🧰 Tech Stack
- Java + TestNG + Maven
- Appium for mobile automation
- LambdaTest for cloud execution
- dotenv for secret management
- ExtentReports for test reporting

## 🔍 Test Cases
| Test Case | Steps |
|----------|-------|
| Download Speed | Navigate to testmy.net → TEST MY INTERNET → DOWNLOAD → Read speed |
| Upload Speed   | Navigate to testmy.net → TEST MY INTERNET → UPLOAD → Read speed |
| Combined Speed | Navigate to testmy.net → TEST MY INTERNET → COMBINED → Read speed |
| Latency        | Navigate to testmy.net → TEST MY INTERNET → LATENCY → Read speed |

## 📦 How to Run
```sh
mvn clean test -DsuiteXmlFile=testng.xml
```

## 🔐 Secret Management
Use `.env` file and `dotenv-java` to avoid hardcoded credentials.

## 📍 LambdaTest Setup
- Upload app using CURL to get `lt://` URL
- Use that in `CapabilitiesManager.java`
- Check execution status at: https://appautomation.lambdatest.com/build

## 📄 Reports & Logs
- Logs saved under `logs/`
- Reports generated in `reports/`
