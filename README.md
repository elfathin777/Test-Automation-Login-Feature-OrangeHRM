# 🧪 OrangeHRM Login Automation Test with Cypress

This project contains automated tests for the login feature of [OrangeHRM Demo](https://opensource-demo.orangehrmlive.com/) using Cypress.  
It includes positive and negative test cases, and automatically captures a screenshot after each test.

---

## 📁 Project Structure

```

cypress/
└── e2e/
└── login.cy.js          # Main test file with all login test cases
└── screenshots/             # Automatically saved screenshots
└── support/
cypress.config.js              # Cypress configuration file
README.md                      # Project documentation

````

---

## ⚙️ Setup Instructions

### 1. Install Dependencies

Ensure you have Node.js installed. Then, run:

```bash
npm install
````

If Cypress is not installed yet:

```bash
npm install cypress --save-dev
```

---

### 2. Run the Tests

#### Option A: Interactive Mode

Launch Cypress UI to run tests manually:

```bash
npx cypress open
```

Select the test file `login.cy.js`.

#### Option B: Headless Mode

Run all tests in the terminal:

```bash
npx cypress run
```

Screenshots will be saved automatically after each test.

---

## 🧪 Test Scenarios

This suite tests the following login scenarios:

* ✅ User login with valid username and valid password
* ❌ Login fails with invalid username and invalid password
* ❌ Login fails with invalid username and valid password
* ❌ Login fails with valid username and invalid password
* ❌ Login fails with lowercase username and valid password
* ❌ Login fails with valid username and uppercase password
* ❌ Login fails with both fields empty
* ❌ Login fails with empty username and valid password
* ❌ Login fails with valid username and empty password

Each test case ends with a screenshot capture.

---

## 📸 Screenshots

Screenshots are saved to:

```
cypress/screenshots/
```

The filename will match the test title for easy identification.

---

## 📄 License

This is a demo automation project created for educational and testing purposes.


