# Tests

This folder contains **test code** for your OCR NEA project.

## What to Include

### Test Files
- Unit test files
- Integration test files
- Test utilities and helpers
- Test configuration files
- Test fixtures and mock data

## Test Organization

Organize tests to mirror your source code structure:

```
tests/
├── unit/
│   ├── test_user_model.py
│   ├── test_authentication.py
│   └── test_utils.py
├── integration/
│   ├── test_api.py
│   └── test_database.py
├── fixtures/
│   ├── sample_data.json
│   └── test_config.py
└── conftest.py (or test setup file)
```

## Testing Frameworks

Choose appropriate testing framework for your language:
- **Python**: unittest, pytest, nose
- **JavaScript**: Jest, Mocha, Jasmine
- **Java**: JUnit, TestNG
- **C#**: NUnit, xUnit, MSTest

## Test Naming Conventions

Good test names are descriptive:
- `test_user_login_with_valid_credentials()`
- `test_calculate_total_with_empty_list()`
- `test_search_returns_no_results_for_invalid_query()`

Bad test names:
- `test1()`
- `test_stuff()`
- `it_works()`

## Types of Tests

### Unit Tests
Test individual functions or methods in isolation:
```python
def test_calculate_discount():
    """Test discount calculation with normal values."""
    result = calculate_discount(100, 0.2)
    assert result == 80
```

### Integration Tests
Test how components work together:
```python
def test_user_registration_flow():
    """Test complete user registration process."""
    # Test database connection + user creation + email sending
    user = register_user("test@example.com", "password123")
    assert user is not None
    assert user.email_verified == False
```

### Test Data Types

Include tests with:
- **Normal data**: Typical expected inputs
- **Boundary data**: Edge cases, min/max values
- **Erroneous data**: Invalid inputs, wrong types

Example:
```python
def test_age_validation_normal():
    assert validate_age(25) == True

def test_age_validation_boundary():
    assert validate_age(18) == True  # minimum
    assert validate_age(100) == True  # maximum

def test_age_validation_erroneous():
    assert validate_age(-5) == False
    assert validate_age("twenty") == False
```

## Running Tests

Document how to run your tests:
```bash
# Python
python -m pytest

# JavaScript
npm test

# Java
mvn test
```

## Test Coverage

Good test coverage includes:
- All critical functions tested
- Edge cases covered
- Error conditions tested
- Integration points verified

## Example Test File (Python)

```python
"""
Unit tests for user authentication module.

Author: Your Name
Date: 2026-02-08
"""

import unittest
from src.auth import authenticate_user, hash_password

class TestAuthentication(unittest.TestCase):
    """Test cases for authentication functions."""
    
    def test_hash_password_creates_hash(self):
        """Test that password hashing creates a hash."""
        password = "secret123"
        hashed = hash_password(password)
        self.assertNotEqual(password, hashed)
    
    def test_authenticate_valid_user(self):
        """Test authentication with valid credentials."""
        result = authenticate_user("user@test.com", "password123")
        self.assertTrue(result)
    
    def test_authenticate_invalid_password(self):
        """Test authentication with invalid password."""
        result = authenticate_user("user@test.com", "wrongpassword")
        self.assertFalse(result)

if __name__ == '__main__':
    unittest.main()
```

## Documentation in Tests

- Comment each test to explain what it tests
- Include docstrings for test classes and methods
- Document any complex test setup
- Explain expected behavior

## Assessment Notes

While automated tests are excellent practice:
- They're **not required** for OCR NEA
- Manual testing is acceptable
- Focus on demonstrating testing was done
- Document your testing approach

However, if you do use automated tests:
- Shows advanced technical skills
- Makes testing more rigorous
- Easier to re-test after changes
- Professional development practice

## Tips

- **Write tests as you develop**: Don't wait until the end
- **Test both success and failure cases**
- **Keep tests simple and focused**
- **Make tests independent**: Each test should work alone
- **Use meaningful assertions**
- **Document your tests**

## Related Resources

- Store test results in `/evidence/test_results/`
- Document testing in `/documentation/04_testing/`
- Reference tests in your development log

---

**Remember**: Good testing demonstrates that your code works correctly. Whether manual or automated, document your testing thoroughly!
