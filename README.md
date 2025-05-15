# Internet Speed Test – Mobile Automation Framework (LambdaTest)

## 📌 Problem Statement

Automate the testing of an Android app using **LambdaTest App Automation** that opens a browser within the app, navigates to [testmy.net](https://testmy.net), and runs internet speed tests (DOWNLOAD, UPLOAD, COMBINED, LATENCY).

---

## ✅ Test Steps

1. In the bottom navigation bar, click the **Browser** icon.
2. Click the **"Enter web-name"** textbox.
3. Type `https://testmy.net/`.
4. Click the **FIND** button.
5. Collapse the keyboard.
6. Click **TEST MY INTERNET**.
7. Click each of the buttons in order:
   - DOWNLOAD
   - UPLOAD
   - COMBINED
   - LATENCY
8. Wait for each result to display (e.g., `101.7 Mbps`), extract it, and print to console.

---

## 🧠 Thought Process & Approach

### 🔹 Framework Choice
- Built using **Java + TestNG + Appium**, inspired by modular, reusable frameworks used in real-world projects.
- TestNG was chosen for its native support for parallelism, retry mechanism, and reporting flexibility.

### 🔹 Layered Architecture

```plaintext
src/
├── config/         # Driver, capabilities, env loading
├── pages/          # Page Object Models (encapsulated locators and actions)
├── tests/          # TestNG test classes for each scenario
├── retry/          # RetryAnalyzer for rerunning failed tests
├── utils/          # Helper functions, logging, wait utilities


Parallel Execution
Configured TestNG to run tests in 2 threads, ensuring speed and concurrency with real devices on LambdaTest.

🔹 Retry Mechanism
Implemented RetryAnalyzer class for failed test retries to handle network flakiness.

🔹 Reporting
Integrated ExtentReports to generate visually rich test execution reports.

🔹 Secret Management
All sensitive values (username, access key, credentials) are stored in a .env file and accessed using dotenv-java.
