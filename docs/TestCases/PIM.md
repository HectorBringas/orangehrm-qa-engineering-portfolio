# PIM Test Cases

These test cases were selected using a Risk-Based Testing approach. Based on the Risk Assessment, Scope, and Test Strategy documents, the scenarios included in this file represent critical business workflows and high-risk areas of the application.

The objective of these test cases is to verify the most important functionalities and reduce the likelihood of business disruption, security issues, or operational failures if defects are introduced into the system.

These test cases focus on employee lifecycle management, data integrity, and business-critical CRUD operations.

## TC_PIM_001

**Title:** Create New Employee

**Priority:** P1

**Test Type:** Functional

**Preconditions:**

* User account exists
* User is active
* User is authenticated
* User has permission to access the PIM module

**Test Steps:**

1. Navigate to the PIM module.
2. Click **Add Employee**.
3. Enter **John** in the First Name field.
4. Enter **Smith** in the Last Name field.
5. Enter **QA1001** in the Employee ID field.
6. Click **Save**.
7. Navigate to the Employee List.
8. Search for Employee ID **QA1001**.

**Expected Result:**
The employee is successfully created and displayed in the Employee List with Employee ID **QA1001**.

**Risk Covered:**
New employees cannot be created.

---

## TC_PIM_002

**Title:** Modify Employee Information

**Priority:** P1

**Test Type:** Functional

**Preconditions:**

* User account exists
* User is active
* User is authenticated
* User has permission to access the PIM module

**Test Steps:**

1. Navigate to the PIM module.
2. Click **Add Employee**.
3. Enter **John** in the First Name field.
4. Enter **Smith** in the Last Name field.
5. Enter **QA1002** in the Employee ID field.
6. Click **Save**.
7. Navigate to the Employee List.
8. Search for Employee ID **QA1002**.
9. Click the Edit (Pencil) icon.
10. Clear the Last Name field.
11. Enter **Brown**.
12. Click **Save**.
13. Navigate to the Employee List.
14. Search for Employee ID **QA1002**.
15. Open the employee record.

**Expected Result:**
The employee information is successfully updated and the Last Name is displayed as **Brown**.

**Risk Covered:**
Employee information cannot be modified.

---

## TC_PIM_003

**Title:** Delete Employee

**Priority:** P1

**Test Type:** Functional

**Preconditions:**

* User account exists
* User is active
* User is authenticated
* User has permission to access the PIM module

**Test Steps:**

1. Navigate to the PIM module.
2. Click **Add Employee**.
3. Enter **John** in the First Name field.
4. Enter **Smith** in the Last Name field.
5. Enter **QA1003** in the Employee ID field.
6. Click **Save**.
7. Navigate to the Employee List.
8. Search for Employee ID **QA1003**.
9. Click the Delete icon.
10. Click **Yes, Delete**.
11. Search again for Employee ID **QA1003**.

**Expected Result:**
No employee record is returned for Employee ID **QA1003**.

**Risk Covered:**
Employees cannot be deleted.

---

## TC_PIM_004

**Title:** Search Employee

**Priority:** P1

**Test Type:** Functional

**Preconditions:**

* User account exists
* User is active
* User is authenticated
* User has permission to access the PIM module

**Test Steps:**

1. Navigate to the PIM module.
2. Click **Add Employee**.
3. Enter **John** in the First Name field.
4. Enter **Smith** in the Last Name field.
5. Enter **QA1004** in the Employee ID field.
6. Click **Save**.
7. Navigate to the Employee List.
8. Search for Employee ID **QA1004**.
9. Click **Search**.

**Expected Result:**
Only the employee with Employee ID **QA1004** is displayed.

**Risk Covered:**
Employee search cannot correctly filter results.

---

## TC_PIM_005

**Title:** Validate Employee Information After Creation

**Priority:** P1

**Test Type:** Data Validation

**Preconditions:**

* User account exists
* User is active
* User is authenticated
* User has permission to access the PIM module

**Test Steps:**

1. Navigate to the PIM module.
2. Click **Add Employee**.
3. Enter **John** in the First Name field.
4. Enter **Smith** in the Last Name field.
5. Enter **QA1005** in the Employee ID field.
6. Click **Save**.
7. Navigate to the Employee List.
8. Search for Employee ID **QA1005**.
9. Open the employee record.

**Expected Result:**
The employee profile displays the same information entered during the creation process.

**Risk Covered:**
Data inconsistency between employee creation and stored information.

---

## TC_PIM_006

**Title:** Prevent Creation with Duplicate Employee ID

**Priority:** P1

**Test Type:** Negative

**Preconditions:**

* User account exists
* User is active
* User is authenticated
* User has permission to access the PIM module

**Test Steps:**

1. Navigate to the PIM module.
2. Create an employee with Employee ID **QA1006**.
3. Click **Add Employee**.
4. Enter **Sarah** in the First Name field.
5. Enter **Brown** in the Last Name field.
6. Enter **QA1006** in the Employee ID field.
7. Click **Save**.

**Expected Result:**
The employee is not created and the validation message **"Employee Id already exists"** is displayed.

**Risk Covered:**
Duplicate employee identifiers.

---

## TC_PIM_007

**Title:** Reset Employee Search

**Priority:** P2

**Test Type:** Functional

**Preconditions:**

* User account exists
* User is active
* User is authenticated
* User has permission to access the PIM module

**Test Steps:**

1. Navigate to the PIM module.
2. Create an employee with Employee ID **QA1007**.
3. Navigate to the Employee List.
4. Search for Employee ID **QA1007**.
5. Click **Search**.
6. Click **Reset**.

**Expected Result:**
All employee records are displayed again and all search filters are cleared.

**Risk Covered:**
Search filters cannot be cleared.

---

## TC_PIM_008

**Title:** Cancel Employee Creation

**Priority:** P2

**Test Type:** Functional

**Preconditions:**

* User account exists
* User is active
* User is authenticated
* User has permission to access the PIM module

**Test Steps:**

1. Navigate to the PIM module.
2. Click **Add Employee**.
3. Enter **John** in the First Name field.
4. Enter **Smith** in the Last Name field.
5. Enter **QA1008** in the Employee ID field.
6. Click **Cancel**.
7. Navigate to the Employee List.
8. Search for Employee ID **QA1008**.

**Expected Result:**
No employee record exists with Employee ID **QA1008**.

**Risk Covered:**
Employees are created after cancelling the operation.

---

## TC_PIM_009

**Title:** Cancel Employee Modification

**Priority:** P2

**Test Type:** Functional

**Preconditions:**

* User account exists
* User is active
* User is authenticated
* User has permission to access the PIM module

**Test Steps:**

1. Navigate to the PIM module.
2. Create an employee with Employee ID **QA1009**.
3. Search for Employee ID **QA1009**.
4. Open the employee record.
5. Change the Last Name from **Smith** to **Brown**.
6. Click **Cancel**.
7. Search again for Employee ID **QA1009**.
8. Open the employee record.

**Expected Result:**
The employee information remains unchanged and the Last Name is still **Smith**.

**Risk Covered:**
Employee information is modified after cancelling the operation.

---

## TC_PIM_010

**Title:** Cancel Employee Deletion

**Priority:** P2

**Test Type:** Functional

**Preconditions:**

* User account exists
* User is active
* User is authenticated
* User has permission to access the PIM module

**Test Steps:**

1. Navigate to the PIM module.
2. Create an employee with Employee ID **QA1010**.
3. Search for Employee ID **QA1010**.
4. Click the Delete icon.
5. Click **No, Cancel**.
6. Search again for Employee ID **QA1010**.

**Expected Result:**
The employee record is still displayed in the Employee List.

**Risk Covered:**
Employees are deleted after cancelling the operation.