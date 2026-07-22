# Test Case: TC-002 - Complete Shopping & Checkout Process

- **Project:** SauceDemo E-Commerce
- **Module:** Cart & Checkout
- **Created By:** Anes Omerović
- **Type:** Functional / End-to-End (E2E)

---

## 🎯 Objective
Verify that a user can add items to the cart, proceed through checkout with valid details, and complete an order successfully.

---

## 📋 Test Steps & Execution

| Step ID | Test Step | Expected Result | Pass/Fail |
| :--- | :--- | :--- | :--- |
| **01** | Log in as `standard_user`. | Successfully logged in, viewing inventory. | **PASS** |
| **02** | Click "Add to cart" on *Sauce Labs Backpack*. | Cart badge updates to `1`. | **PASS** |
| **03** | Click Cart icon, then click "Checkout". | Redirected to "Checkout: Your Information" page. | **PASS** |
| **04** | Fill First Name, Last Name, Zip Code, and click "Continue". | Redirected to "Checkout: Overview" displaying item and total price. | **PASS** |
| **05** | Click "Finish". | Order completed page displays: *"Thank you for your order!"*. | **PASS** |