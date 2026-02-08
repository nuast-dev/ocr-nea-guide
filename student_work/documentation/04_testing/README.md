# Testing Phase

This folder contains all documentation for the **Testing Phase** of your OCR NEA project.

## What to Include

### 1. Test Plan
- Comprehensive test strategy
- Types of testing to be performed
- Test schedule and approach
- Link tests to requirements and success criteria

### 2. Test Cases
- **Unit Tests**: Testing individual functions/methods
- **Integration Tests**: Testing components working together
- **System Tests**: Testing the whole system
- **User Acceptance Tests**: Testing with stakeholder

### 3. Test Data
- Normal data (typical expected inputs)
- Boundary data (edge cases, limits)
- Erroneous data (invalid inputs, error conditions)
- Justification for test data choices

### 4. Test Results
- Detailed results for each test
- Pass/fail status
- Evidence of testing (screenshots)
- Actual vs. expected results
- Bugs discovered

### 5. Bug Reports and Fixes
- Documentation of bugs found
- Severity and priority
- Steps to reproduce
- How bugs were fixed
- Re-testing after fixes

### 6. Stakeholder Testing
- User acceptance test results
- Stakeholder feedback
- Issues raised by stakeholder
- Actions taken based on feedback

## Test Case Format Suggestion

```markdown
## Test Case #X: [Test Name]

**Requirement Tested:** [Link to specific requirement]
**Test Type:** Unit/Integration/System/UAT
**Test Data:** [What data is being used]
**Expected Result:** [What should happen]
**Actual Result:** [What actually happened]
**Pass/Fail:** [Status]
**Evidence:** [Screenshot reference]
**Notes:** [Any additional information]
```

## File Naming Suggestions

- `test_plan.md`
- `test_cases.md` or split into multiple files
- `unit_tests.md`
- `integration_tests.md`
- `system_tests.md`
- `user_acceptance_tests.md`
- `bug_report_001.md`
- `test_results_YYYY-MM-DD.md`

## Tips

- **Test as you develop**: Don't wait until the end
- **Be systematic**: Cover all requirements
- **Use varied data**: Normal, boundary, and erroneous
- **Document everything**: Record all test results
- **Screenshot evidence**: Capture test execution
- **Test after fixes**: Re-run tests after bug fixes (regression testing)
- **Be honest**: Report failures as well as successes

## Assessment Focus

Examiners look for:
- Comprehensive test coverage
- Appropriate test data selection
- Clear link between tests and requirements
- Evidence of actual testing (screenshots)
- Professional test documentation
- Iterative testing throughout development
- Stakeholder involvement in testing

## Types of Testing

### Unit Testing
- Test individual functions/methods
- Use test frameworks if appropriate
- Test with various inputs

### Integration Testing
- Test how components work together
- Test data flow between modules
- Test interfaces and connections

### System Testing
- Test the complete system
- Test all features working together
- Test against all requirements

### User Acceptance Testing (UAT)
- Stakeholder tests the system
- Real-world usage scenarios
- Final validation before deployment

## Common Test Data Types

- **Normal**: Typical, expected inputs
- **Boundary**: Edge cases (min/max values)
- **Erroneous**: Invalid inputs, wrong types
- **Extreme**: Very large or very small values

## Related Resources

- See `/04_Testing.md` in the root directory for detailed guidance
- Use testing frameworks appropriate for your language
- Store test evidence screenshots in `/evidence/test_results/`

---

**Remember**: Good testing validates that your solution works correctly and meets requirements!
