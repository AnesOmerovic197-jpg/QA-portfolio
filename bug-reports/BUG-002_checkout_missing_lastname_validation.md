# [BUG-002] Checkout Form Allows Proceeding Without Required 'Last Name' Field on 'error_user' Profile

## 1. Summary / Title
Checkout form fails to validate the required 'Last Name' field, allowing 'error_user' to proceed with empty data.

## 2. Environment
- **Environment:** Production / Demo
- **URL:** https://www.saucedemo.com/checkout-step-one.html
- **OS:** Windows 11
- **Browser:** Chrome v124 (64-bit)
- **Test Data / User:** `error_user` / `secret_sauce`

## 3. Steps to Reproduce (STR)
1. Navigate to https://www.saucedemo.com/
2. Log in using username `error_user` and password `secret_sauce`.
3. Add any item to the cart and proceed to Checkout (`/checkout-step-one.html`).
4. Enter 'First Name' and 'Zip/Postal Code', but leave 'Last Name' completely empty.
5. Click the **Continue** button.

## 4. Expected Result
The system should block form submission, display an error message stating "Error: Last Name is required", and remain on the current page (`/checkout-step-one.html`).

## 5. Actual Result & Console Logs
The application bypasses validation, accepts the empty field, and redirects the user to the 'Checkout: Overview' page (`/checkout-step-two.html`).

```javascript
// No console errors logged (Silent validation bug)