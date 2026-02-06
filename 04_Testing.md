# 04 - Testing Phase

**Timeframe:** Month 8–10  
**Target Month:** Month 10

## Navigation
⬅️ [Previous: Development Log](03_DevLog.md) | ➡️ [Next: Evaluation](05_Evaluation.md)

---

## What to Do

Testing validates that your solution works correctly and meets the requirements. This phase overlaps with development - you should be testing as you build, not waiting until the end.

### Key Activities

1. **Create Test Plan**
   - Design comprehensive test cases
   - Link tests to requirements and success criteria
   - Plan different types of testing

2. **Conduct Testing**
   - Unit testing (individual functions/methods)
   - Integration testing (components working together)
   - System testing (whole system)
   - User acceptance testing (with stakeholder)

3. **Document Results**
   - Record all test results
   - Screenshot evidence of tests
   - Document bugs found and fixed

4. **Iterative Testing**
   - Test after each development cycle
   - Regression testing after bug fixes
   - Re-test failed cases after fixes

5. **Stakeholder Testing**
   - Get stakeholder to test the system
   - Record their feedback
   - Document any changes made as a result

## Checklist

### Test Planning
- [ ] Created comprehensive test plan
- [ ] Test cases cover all requirements
- [ ] Test cases cover all success criteria
- [ ] Included normal, boundary, and erroneous data
- [ ] Planned unit, integration, and system tests
- [ ] Test data prepared and documented

### Unit Testing
- [ ] Tested all major functions/methods individually
- [ ] Minimum 15-20 unit tests documented
- [ ] Test data includes valid and invalid inputs
- [ ] Expected vs actual results recorded
- [ ] Screenshots/evidence of test outputs

### Integration Testing
- [ ] Tested interactions between modules/components
- [ ] Tested data flow between components
- [ ] Verified error handling between components
- [ ] Documented integration issues found and fixed

### System Testing
- [ ] Tested complete workflows end-to-end
- [ ] Tested all user scenarios
- [ ] Verified all functional requirements met
- [ ] Verified non-functional requirements (performance, usability)

### User Acceptance Testing
- [ ] Stakeholder tested the complete system
- [ ] Tested against original requirements
- [ ] Tested against success criteria
- [ ] Stakeholder feedback documented
- [ ] User testing session recorded/photographed

### Bug Tracking
- [ ] All bugs documented with severity
- [ ] Bug fix process documented
- [ ] Re-tested after fixes to confirm resolution
- [ ] Any unfixed bugs explained and justified

### Test Evidence
- [ ] Screenshots of test executions
- [ ] Test data shown clearly
- [ ] Expected vs actual results documented
- [ ] All tests numbered and referenced

### Test Coverage
- [ ] Every requirement tested at least once
- [ ] Every success criterion tested
- [ ] Edge cases tested
- [ ] Error handling tested

## Common Pitfalls

### ❌ Testing Only Happy Path
**Pitfall:** Only testing with valid data and normal usage.  
**Solution:** Test boundary cases, invalid data, unexpected inputs, and error scenarios. Try to break your system.

### ❌ No Evidence
**Pitfall:** Claiming tests were done without screenshots or proof.  
**Solution:** Screenshot EVERYTHING. Show test inputs, outputs, and results clearly.

### ❌ Vague Test Cases
**Pitfall:** Test cases like "Test the login" with no specifics.  
**Solution:** Each test case should be specific: test data, expected result, actual result, pass/fail.

### ❌ Testing Only at the End
**Pitfall:** Waiting until all code is written before testing.  
**Solution:** Test continuously during development. This catches bugs early when they're easier to fix.

### ❌ No Failed Tests
**Pitfall:** Showing only passing tests with no failures.  
**Solution:** Real projects have bugs. Show failed tests, how you diagnosed them, and how you fixed them.

### ❌ Fake Test Results
**Pitfall:** Making up test results or editing screenshots.  
**Solution:** Always use genuine test results. Examiners can tell when results are fabricated.

### ❌ No User Testing
**Pitfall:** Not getting stakeholder to test the system.  
**Solution:** Have your stakeholder test the system thoroughly and document their experience.

### ❌ Testing Checklist Only
**Pitfall:** Just showing "Login: ✓" with no detail.  
**Solution:** Each test needs: test number, description, test data, expected result, actual result, screenshot.

### ❌ No Traceability
**Pitfall:** Tests not linked back to requirements or success criteria.  
**Solution:** Every test should reference which requirement/criterion it validates.

## Test Case Structure

Each test case should include:

### Test Case Template

```markdown
**Test ID:** TC-001  
**Test Type:** Unit Test / Integration Test / System Test  
**Requirement:** REQ-003 (User login functionality)  
**Success Criterion:** SC-002 (Login completes within 2 seconds)

**Description:** Test user login with valid credentials

**Test Data:**
- Username: "john_doe"
- Password: "SecurePass123!"

**Preconditions:**
- User account exists in database
- Application is running
- Database connection active

**Test Steps:**
1. Navigate to login page
2. Enter username "john_doe"
3. Enter password "SecurePass123!"
4. Click "Login" button

**Expected Result:**
- User successfully logged in
- Redirected to dashboard page
- Welcome message displays "Welcome, John Doe"
- Login completes in under 2 seconds

**Actual Result:**
- User successfully logged in
- Redirected to dashboard page
- Welcome message displays "Welcome, John Doe"
- Login completed in 1.3 seconds

**Status:** PASS ✓

**Evidence:** [Screenshot showing successful login and dashboard]

**Date Tested:** 15/01/2026  
**Tested By:** [Your Name]
```

## Test Types and Examples

### 1. Unit Tests
Testing individual functions/methods in isolation.

**Example Test Cases:**
- Test password validation with valid password
- Test password validation with too-short password
- Test password validation with no special characters
- Test search function with matching results
- Test search function with no matches
- Test calculation function with positive numbers
- Test calculation function with negative numbers
- Test calculation function with zero

### 2. Integration Tests
Testing how components work together.

**Example Test Cases:**
- Test login flow connecting UI → validation → database
- Test search connecting UI → search logic → database → results display
- Test file save connecting data → file handler → storage
- Test data flow from input form → processing → output display

### 3. System Tests
Testing the complete system end-to-end.

**Example Test Cases:**
- Complete user workflow from login to logout
- Full transaction process (add to cart → checkout → payment → confirmation)
- Data input → processing → report generation → export
- Admin workflow: add user → assign permissions → verify access

### 4. User Acceptance Tests
Stakeholder testing real-world scenarios.

**Example Test Cases:**
- Stakeholder completes their most common task
- Stakeholder tries edge cases they encounter
- Stakeholder verifies outputs meet their needs
- Stakeholder tests ease of use and learning curve

## Test Data Categories

### 1. Normal Data
Typical, expected inputs that should work correctly.
- Example: Valid email "user@example.com"

### 2. Boundary Data
Values at the limits of acceptable ranges.
- Example: Password with exactly 8 characters (if minimum is 8)
- Example: Age of 18 (if minimum age is 18)

### 3. Erroneous Data
Invalid inputs that should be rejected gracefully.
- Example: Email without @ symbol
- Example: Negative quantity for items
- Example: Text in numeric field

### 4. Extreme Data
Valid but unusual inputs.
- Example: Very long strings
- Example: Very large numbers
- Example: Empty optional fields

## Testing Documentation Structure

Your Testing section should include:

1. **Introduction** (0.5-1 page)
   - Testing strategy overview
   - Types of testing used

2. **Test Plan** (2-3 pages)
   - Comprehensive list of planned tests
   - Test data specifications
   - Testing schedule
   - Tools used for testing

3. **Unit Tests** (4-6 pages)
   - 15-20 detailed unit test cases
   - Mix of passing and failing tests
   - Evidence of bug fixes

4. **Integration Tests** (2-3 pages)
   - 5-8 integration test cases
   - Component interaction validation

5. **System Tests** (2-3 pages)
   - End-to-end workflow tests
   - Requirements validation

6. **User Acceptance Testing** (2-3 pages)
   - Stakeholder testing session documentation
   - Feedback and responses
   - Success criteria validation

7. **Bug Reports and Fixes** (2-3 pages)
   - Log of bugs found during testing
   - Diagnosis and fix process
   - Re-test results

**Total Expected Length:** 15-20 pages

## Testing Evidence Best Practices

### Screenshots Should Show:
- Test input clearly visible
- Expected result documented
- Actual result visible
- Pass/fail status obvious
- Test ID reference
- Date/time if relevant

### For Code Tests:
- Show test code
- Show test execution
- Show output/results
- Show assertions/verifications

### For UI Tests:
- Show before state
- Show action taken
- Show after state
- Show error messages (if testing errors)

## Traceability Matrix

Create a table linking tests to requirements:

| Test ID | Requirement | Success Criterion | Status | Evidence |
|---------|-------------|-------------------|--------|----------|
| TC-001 | REQ-001 | SC-001 | PASS | Screenshot 1 |
| TC-002 | REQ-001 | SC-001 | PASS | Screenshot 2 |
| TC-003 | REQ-002 | SC-003 | FAIL → FIXED | Screenshots 3-4 |
| TC-004 | REQ-003 | SC-005 | PASS | Screenshot 5 |

## Tips for Success

- **Test Early and Often:** Don't leave all testing until the end
- **Be Thorough:** Test normal, boundary, and erroneous data
- **Document Everything:** Screenshots, test data, results
- **Show Failures:** Failed tests show authenticity and problem-solving
- **Link to Requirements:** Every test should trace back to a requirement
- **Get Real User Feedback:** Stakeholder testing is invaluable

## Assessment Focus

Examiners look for:
- Comprehensive test coverage of all requirements
- Appropriate mix of test types
- Clear test documentation with evidence
- Normal, boundary, and erroneous data testing
- Evidence of bugs found and fixed
- Genuine stakeholder/user testing
- Traceability to requirements and success criteria
- Professional presentation of results

## Testing Tools Recommendations

- **Python:** unittest, pytest, doctest
- **Java:** JUnit, TestNG
- **JavaScript:** Jest, Mocha, Jasmine
- **C#:** NUnit, xUnit, MSTest
- **General:** Selenium (UI testing), Postman (API testing)

---

## Navigation
⬅️ [Previous: Development Log](03_DevLog.md) | ➡️ [Next: Evaluation](05_Evaluation.md)
