# Login Test Cases

These test cases were selected using a Risk-Based Testing approach. Based on the Risk Assessment, Scope, and Test Strategy documents, the scenarios included in this file represent critical business workflows and high-risk areas of the application.

The objective of these test cases is to verify the most important functionalities and reduce the likelihood of business disruption, security issues, or operational failures if defects are introduced into the system.

## TC_LOGIN_001

**Title:** Successful Login with Valid Credentials

**Priority:** P1

**Test Type:** Functional

**Preconditions:**

* User account exists
* User is active
* Login page is accessible

**Test Steps:**

1. Navigate to Login page
2. Enter valid username
3. Enter valid password
4. Click Login

**Expected Result:**
User is successfully authenticated and redirected to the Dashboard page.

**Risk Covered:**
Authorized users cannot access the system.

---

## TC_LOGIN_002

**Title:** Successful Logout

**Priority:** P1

**Test Type:** Functional

**Preconditions:**

* User account exists
* User is active
* Login page is accessible

**Test Steps:**

1. Navigate to Login page
2. Enter valid username
3. Enter valid password
4. Click Login
5. Click on the user menu
6. Click Logout

**Expected Result:**
User is successfully logged out and redirected to the Login page.

**Risk Covered:**
Session cannot be terminated properly.

---

## TC_LOGIN_003

**Title:** Login with Non-Existent User

**Priority:** P1

**Test Type:** Negative

**Preconditions:**

* Login page is accessible

**Test Steps:**

1. Navigate to Login page
2. Enter an unregistered username
3. Enter a valid password
4. Click Login

**Expected Result:**
Access is denied and the message "Invalid Credentials" is displayed.

**Risk Covered:**
Unauthorized access.

---

## TC_LOGIN_004

**Title:** Login with Invalid Password

**Priority:** P1

**Test Type:** Negative

**Preconditions:**

* User account exists
* User is active
* Login page is accessible

**Test Steps:**

1. Navigate to Login page
2. Enter a valid username
3. Enter an invalid password
4. Click Login

**Expected Result:**
Access is denied and the message "Invalid Credentials" is displayed.

**Risk Covered:**
Unauthorized access.

---

## TC_LOGIN_005

**Title:** Login with Empty Password

**Priority:** P1

**Test Type:** Validation

**Preconditions:**

* User account exists
* User is active
* Login page is accessible

**Test Steps:**

1. Navigate to Login page
2. Enter a valid username
3. Leave the password field empty
4. Click Login

**Expected Result:**
The login attempt is rejected and a validation message is displayed.

**Risk Covered:**
Insufficient input validation.

---

## TC_LOGIN_006

**Title:** Session Persistence After Page Refresh

**Priority:** P1

**Test Type:** Session Management

**Preconditions:**

* User account exists
* User is active
* Login page is accessible

**Test Steps:**

1. Navigate to Login page
2. Enter valid username
3. Enter valid password
4. Click Login
5. Refresh the browser page

**Expected Result:**
The user remains authenticated and the Dashboard page is displayed.

**Risk Covered:**
Incorrect session handling.

---

## TC_LOGIN_007

**Title:** Access Protected URL After Logout

**Priority:** P1

**Test Type:** Security

**Preconditions:**

* User account exists
* User is active
* Login page is accessible

**Test Steps:**

1. Navigate to Login page
2. Enter valid username
3. Enter valid password
4. Click Login
5. Click on the user menu
6. Click Logout
7. Attempt to access the Dashboard URL directly

**Expected Result:**
The system redirects the user to the Login page instead of granting access to the Dashboard.

**Risk Covered:**
Authentication bypass.

---

## TC_LOGIN_008

**Title:** Session Expiration

**Priority:** P1

**Test Type:** Session Management

**Preconditions:**

* User account exists
* User is active
* Login page is accessible
* Session timeout period is known

**Test Steps:**

1. Navigate to Login page
2. Enter valid username
3. Enter valid password
4. Click Login
5. Remain inactive until the session timeout period expires
6. Attempt to perform any action within the application

**Expected Result:**
The user is redirected to the Login page and must authenticate again.

**Risk Covered:**
Orphaned or unsafe sessions.

---

## TC_LOGIN_009

**Title:** Hidden Password Field

**Priority:** P1

**Test Type:** UI Validation

**Preconditions:**

* Login page is accessible

**Test Steps:**

1. Navigate to Login page
2. Enter any value into the password field

**Expected Result:**
The entered characters are masked and not displayed in plain text.

**Risk Covered:**
Exposure of user credentials.

---

## TC_LOGIN_010

**Title:** Direct Access to Protected URL Without Authentication

**Priority:** P1

**Test Type:** Security

**Preconditions:**

* Login page is accessible

**Test Steps:**

1. Navigate to Login page
2. Attempt to access the Dashboard URL directly without authenticating

**Expected Result:**
The system redirects the user to the Login page and access to the Dashboard is denied.

**Risk Covered:**
Unauthorized access vulnerability.
