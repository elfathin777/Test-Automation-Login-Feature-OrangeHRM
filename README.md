# 🧪 OrangeHRM Login Automation Test with Cypress

This project automates the login functionality of [OrangeHRM Demo](https://opensource-demo.orangehrmlive.com/) using Cypress.  
It includes multiple login scenarios (valid, invalid, empty input), and captures a screenshot after each test run.

---

## 📁 Project Structure

cypress/
└── e2e/
└── login.cy.js # Main test file
└── screenshots/ # Screenshots saved here after each test
└── support/
cypress.config.js # Cypress configuration
README.md # This file

yaml
Copy code

---

## ⚙️ Setup Instructions

### 1. Install Dependencies

Make sure you have Node.js installed. Then install Cypress:

```bash
npm install
Or if Cypress isn't installed yet:

bash
Copy code
npm install cypress --save-dev
2. Run the Tests
You can run the tests using:

a. Cypress UI (Interactive Mode)
bash
Copy code
npx cypress open
Then select login.cy.js and run it.

b. Headless Mode (Terminal)
bash
Copy code
npx cypress run
This will also generate screenshots and videos (if enabled).

🧪 Test Scenarios
The test file includes the following cases:

✅ Login with valid username and valid password

❌ Login with invalid username and invalid password

❌ Login with invalid username and valid password

❌ Login with valid username and invalid password

❌ Login with lowercase username and valid password

❌ Login with uppercase password and valid username

❌ Login with empty username and password

❌ Login with empty username and valid password

❌ Login with valid username and empty password

Each test ends with a screenshot capture, saved automatically.

📸 Screenshots
Screenshots are stored in the folder:

bash
Copy code
cypress/screenshots/
Each file is named based on the test title (describe + it block).

🛠 Configuration
Make sure your cypress.config.js looks like this:

javascript
Copy code
const { defineConfig } = require('cypress');

module.exports = defineConfig({
  e2e: {
    setupNodeEvents(on, config) {
      // Add node events if needed
    },
    baseUrl: 'https://opensource-demo.orangehrmlive.com/',
  },
  screenshotOnRunFailure: true,
  screenshotsFolder: 'cypress/screenshots',
});
To capture screenshots after every test case (not only on failure), add this to your test file:

javascript
Copy code
afterEach(function () {
  cy.screenshot(Cypress.mocha.getRunner().test.fullTitle());
});
📄 License
This is a demo test suite for educational purposes.
