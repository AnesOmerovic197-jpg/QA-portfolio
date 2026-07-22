# Test Case: TC-001 - User Login Functionality

- **Project:** SauceDemo E-Commerce
- **Module:** Authentication
- **Created By:** Anes Omerović
- **Type:** Functional / Positive & Negative Testing

---

## 🎯 Objective
Verify that users can log in with valid credentials and receive appropriate error messages when using invalid credentials or locked-out accounts.

---

## 📋 Test Steps & Execution

| Step ID | Test Step | Expected Result | Pass/Fail |
| :--- | :--- | :--- | :--- |
| **01** | Open browser and navigate to `https://www.saucedemo.com/` | Login page opens successfully. | **PASS** |
| **02** | Enter valid username `standard_user` and password `secret_sauce`. Click Login. | User is redirected to Inventory Page (`/inventory.html`). | **PASS** |
| **03** | Log out, then enter `locked_out_user` and password `secret_sauce`. Click Login. | Error message displayed: *"Epic sadface: Sorry, this user has been locked out."* | **PASS** |
| **04** | Enter invalid username `invalid_user` and password `secret_sauce`. Click Login. | Error message displayed: *"Epic sadface: Username and password do not match..."* | **PASS** |
| **05** | Leave username and password blank. Click Login. | Error message displayed: *"Epic sadface: Username is required"*. | **PASS** |