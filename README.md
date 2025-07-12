# 🎯 Playwright Test Automation Framework with TypeScript

A data-driven end-to-end test automation framework built using **Playwright**, **TypeScript**, and **Node.js**, designed and maintained by **Seenuvasan Velmurugan**. This framework ensures scalable UI and API test execution with cross-browser support, Excel-driven data configuration, and CI/CD compatibility.

---

## 📌 Overview

This framework separates test logic from test data using Excel-based input sheets. It supports testing for multiple datasets using a single test script and includes prebuilt utilities for UI automation, API testing (REST & SOAP), and basic DB operations.

Test cases are structured with **Playwright’s test runner**, allowing seamless execution in headless/headful mode, video recording, and screenshot capture upon failure. Tests can run sequentially or in parallel, and the system includes flexible runtime configuration using `.env` files.

---

## 🛠️ Features

- ✅ Supports **UI**, **REST**, **SOAP API**, and **DB** automation
- 🎯 **Excel-driven data execution** for test control and reuse
- 🌐 **Cross-browser compatibility**: Chrome, Edge, Firefox, WebKit
- 🧪 Execute in **Normal**, **Serial**, or **Parallel** run modes
- 🔄 Supports **data transfer** between test cases
- 📊 Built-in support for **Playwright**, **Allure**, and **JUnit HTML reports**
- 📂 Captures **logs**, **videos**, and **screenshots** for failures
- 🧩 Easy runtime configuration using `.env` + `set` command
- 🔧 Designed for **CI/CD integration** (e.g., Jenkins, GitHub Actions)

---

## 🧪 Supported Browsers

| Browser  | Engine   |
|----------|----------|
| Chrome   | Chromium |
| Firefox  | Gecko    |
| Edge     | Chromium |
| WebKit   | Safari   |

---

## 🔀 Run Modes (From Excel Sheet)

| Mode     | Excel Entry | Description                                        |
|----------|-------------|----------------------------------------------------|
| Normal   | *blank*     | Sequential execution of test cases                |
| Serial   | `serial`    | Stops test batch on first failure                 |
| Parallel | `parallel`  | Parallel execution of independent test scenarios  |

---

## 🚀 Getting Started

### 1. 📦 Installation

Ensure [Node.js](https://nodejs.org/) v14+ is installed.

```bash
npm ci
````

### 2. 🧪 Creating Tests

* Add new test files under `/tests` with `.spec.ts` extension (e.g., `LoginTest.spec.ts`)
* Create a new sheet in `testData.xlsx` matching the test name
* Register the test in the desired execution sheet (`Regression`, `Smoke`, etc.)

---

## ▶️ Execution Options

### A. Run Test Suite via Excel Sheet

```bash
npm run create:suite SHEET=Regression && npm test
```

> Replace `Regression` with any valid sheet name

### B. Run Single Test (Local)

```bash
set TEST_NAME=LoginTest && npm run local:test
```

### C. Run Single Test in UI Mode (Debug)

```bash
set TEST_NAME=LoginTest && npm run local:test:ui
```

### D. Change Env Config at Runtime

```bash
set BROWSER=edge
```

### E. Generate Allure Report

```bash
npm run report
```

---

## 📊 Reports & Logs

| Report/Log Type    | Location                          |
| ------------------ | --------------------------------- |
| Playwright HTML    | `test-results/results/index.html` |
| Allure HTML Report | `allure-report/index.html`        |
| Execution Logs     | `test-results/logs/execution.log` |

---

## 🧠 Framework Highlights

* Page Object Model (POM) with reusable locator components
* Excel-based test management
* Runtime switching of browsers, environments, and modes
* Centralized config in `.env` and `playwright.config.ts`
* CI/CD friendly with parallel execution support

---

## 📌 Author

This project is authored and maintained by:

**Seenuvasan Velmurugan**
QA Automation Engineer | SDET | ISTQB Certified | Professional Scrum Master II | Professional Scrum Product Owner II
📍 Chennai, India
📧 [seenuvasanvelmurugan@gmail.com](mailto:seenuvasanvelmurugan@gmail.com)
🔗 [LinkedIn](https://www.linkedin.com/in/seenuvasan-velmurugan-professional-social-profile) | [GitHub](https://github.com/Seenuvasan91)

---

## 🤝 Licensing & Usage

Feel free to fork, modify, and integrate this framework for learning or team use. Attribution appreciated if reusing this structure in production.

---
