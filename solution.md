# Software Testing: Types and Differences

## 1. Define 8 Testing Types with Examples

### 1. Unit Testing

**Definition:** Unit testing is the process of testing individual components or functions of an application to verify that they work correctly.

**Example:** Testing a login validation function to check whether it correctly accepts valid email addresses and rejects invalid ones.

### 2. Integration Testing

**Definition:** Integration testing verifies whether different modules or components of an application work correctly together.

**Example:** Testing whether the login API correctly communicates with the database to verify a user's credentials.

### 3. Functional Testing

**Definition:** Functional testing checks whether an application works according to its specified functional requirements.

**Example:** Testing whether clicking the "Add to Cart" button correctly adds a product to the shopping cart.

### 4. System Testing

**Definition:** System testing evaluates the complete application to ensure that all its components work together as expected.

**Example:** Testing an entire e-commerce application, including registration, login, product search, cart, payment, and order confirmation.

### 5. Acceptance Testing

**Definition:** Acceptance testing verifies whether an application meets business requirements and is ready for delivery to the end user.

**Example:** A client tests a college management system to confirm that student registration, fee payment, and examination features meet their requirements.

### 6. Smoke Testing

**Definition:** Smoke testing is a preliminary test performed on a new software build to check whether its critical features work and the build is stable enough for further testing.

**Example:** After deploying a new application build, a tester checks whether the application opens, login works, and the dashboard loads successfully.

### 7. Sanity Testing

**Definition:** Sanity testing is a focused test performed after a minor change or bug fix to verify that the affected functionality works correctly.

**Example:** After fixing a password reset issue, a tester checks whether users can reset their passwords successfully.

### 8. Regression Testing

**Definition:** Regression testing checks whether existing functionality still works correctly after code changes, bug fixes, or new feature additions.

**Example:** After adding a discount feature to an e-commerce application, a tester checks whether login, product search, cart, payment, and order placement still work correctly.

---

## 2. Difference Between Smoke Testing and Sanity Testing

| Smoke Testing | Sanity Testing |
|---|---|
| Checks the basic functionality of a new software build. | Checks specific functionality affected by a change or bug fix. |
| Covers the major features of the application. | Focuses on a limited area of the application. |
| Determines whether the build is stable enough for further testing. | Verifies whether a particular change or fix works correctly. |
| Usually performed after receiving a new build. | Usually performed after a minor change or bug fix. |
| **Example:** Checking login, dashboard, and navigation after a new build. | **Example:** Checking the password reset feature after fixing a related bug. |

**In short:** Smoke testing checks whether the main features of a build work, while sanity testing checks whether a specific change or fix works correctly.

---

## 3. Difference Between Retesting and Regression Testing

| Retesting | Regression Testing |
|---|---|
| Verifies whether a previously reported bug has been fixed. | Verifies whether existing features still work after code changes. |
| Focuses on the specific functionality where the bug occurred. | Covers existing functionality that could be affected by the changes. |
| Uses test cases that previously failed because of the bug. | Uses relevant test cases for previously working functionality. |
| Performed after a developer fixes a reported defect. | Performed after changes that might affect existing functionality. |
| **Example:** Checking whether a fixed login button now works correctly. | **Example:** After fixing the login button, checking whether login, logout, and dashboard navigation still work. |

**In short:** Retesting confirms that a specific bug has been fixed, whereas regression testing ensures that the fix has not broken other existing features.

---

## Conclusion

Software testing helps ensure that an application meets its requirements, works correctly, and provides a reliable user experience.

Different testing types serve different purposes, from testing individual components to validating the complete application. Smoke testing and sanity testing help verify builds and changes, while retesting and regression testing help confirm bug fixes and protect existing functionality.
