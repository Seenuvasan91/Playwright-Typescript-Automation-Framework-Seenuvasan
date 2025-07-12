# 🎯 Playwright Automation Framework – TypeScript & Excel-Driven

An end-to-end test automation framework designed and developed by **Seenuvasan Velmurugan** using **Playwright**, **TypeScript**, and **Node.js**. This data-driven solution leverages Excel for flexible test configuration and supports UI + API (REST & SOAP) validations across modern browsers.

---

## 📌 Overview

This framework enables reusable and scalable test automation by cleanly separating test logic from test data. Test inputs are sourced dynamically from Excel sheets, making it ideal for validating multiple datasets using the same test logic.

The framework supports:

- UI testing on [Advantage Online Shopping](http://advantageonlineshopping.com)
- API testing across both [SOAP](https://www.advantageonlineshopping.com/accountservice/ws/accountservice.wsdl) and [REST](https://fakestoreapi.com) endpoints

It is optimized for continuous testing pipelines with support for environment-specific runs, result reports, and multi-mode execution.

---

## ⚙️ Features

- 🔁 Unified framework for UI, REST, SOAP API, and DB (MSSQL, DB2, Oracle)
- 📊 Data-driven execution via Excel sheets
- 🌍 Cross-browser support (Chromium, Edge, Firefox, WebKit)
- 🧪 Run modes: Normal, Serial, and Parallel
- 🔄 Data sharing between test cases
- 📥 File operations: PDF parsing, downloads
- 📈 Reports: Playwright HTML, Allure, JUnit (HTML)
- 📹 Screenshots and video recordings on failure
- ⚙️ Config-driven execution via `.env` and `playwright.config.ts`
- 🔧 Seamless integration into CI/CD tools (e.g., Jenkins, GitHub Actions)

---

## 🌐 Supported Browsers

| Browser   | Engine     |
|-----------|------------|
| Chrome    | Chromium   |
| Firefox   | Gecko      |
| MS Edge   | Chromium   |
| WebKit    | Safari     |

---

## 🚦 Run Modes (Excel Controlled)

| Mode     | Excel Entry | Description                                       |
|----------|-------------|---------------------------------------------------|
| Normal   | *blank*     | Sequential execution                              |
| Serial   | `serial`    | Sequential with stop-on-failure                   |
| Parallel | `parallel`  | Parallel execution of independent test cases      |

---

## 🛠️ Installation & Setup

> Requires [Node.js](https://nodejs.org/) v14 or higher.

### 1. Install Dependencies

```bash
npm ci
````

---

## 🧪 Creating Tests

* Create a test file inside `/tests` directory with `.spec.ts` extension
  *Example: `LoginTest.spec.ts`*

* In `testData.xlsx`, create a sheet with the same name as the test file
  *Example: `LoginTest`*

* Register the test in an execution sheet like `Regression` or `Smoke`

---

## ▶️ Test Execution

### A. Run Full Suite by Excel Sheet

```bash
npm run create:suite SHEET=Regression && npm test
```

### B. Run Individual Test (Local)

```bash
set TEST_NAME=LoginTest && npm run local:test
```

### C. Change Runtime Config (Optional)

```bash
set BROWSER=edge
```

> Update environment details via `.env` or `set` commands.

### D. Generate Allure Report

```bash
npm run report
```

---

## 📈 Reports & Logs

| Artifact      | Location                          |
| ------------- | --------------------------------- |
| HTML Report   | `test-results/results/index.html` |
| Logs          | `test-results/logs/execution.log` |
| Allure Report | `allure-report/index.html`        |

---

## 👨‍💻 Maintainer

**Seenuvasan Velmurugan**
QA Automation Engineer | SDET
📧 [seenuvasanvelmurugan@gmail.com](mailto:seenuvasanvelmurugan@gmail.com)
🔗 [LinkedIn](https://www.linkedin.com/in/seenuvasan-velmurugan-professional-social-profile)
🔗 [GitHub](https://github.com/Seenuvasan91)

---

> ⭐ If this project was helpful, consider starring the repository and following for more contributions.

```

---