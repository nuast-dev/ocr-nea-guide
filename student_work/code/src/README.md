# Source Code

This folder contains the **source code** for your OCR NEA project.

## What to Include

All your application code files:
- Main application files
- Module/class files
- Configuration files
- Utility/helper functions
- Database scripts (if applicable)
- Frontend code (HTML, CSS, JavaScript)
- Backend code (Python, Java, C#, etc.)
- Build scripts
- Package configuration files (package.json, requirements.txt, etc.)

## Organization

Organize your code logically:

```
src/
├── main.py (or main entry point)
├── models/
│   ├── user.py
│   └── data.py
├── controllers/
│   └── app_controller.py
├── views/
│   ├── templates/
│   └── static/
├── utils/
│   └── helpers.py
└── config/
    └── settings.py
```

Or for web projects:
```
src/
├── frontend/
│   ├── index.html
│   ├── css/
│   └── js/
├── backend/
│   ├── api/
│   ├── models/
│   └── services/
└── database/
    └── schema.sql
```

## Code Quality Guidelines

### 1. Commenting
- Add comments to explain complex logic
- Document all functions/methods
- Include file headers with purpose and author
- Don't over-comment obvious code

### 2. Naming Conventions
- Use clear, descriptive names
- Follow language conventions (snake_case, camelCase, etc.)
- Be consistent throughout your project
- Avoid abbreviations unless common

### 3. Code Structure
- Keep functions/methods focused and small
- Use appropriate design patterns
- Separate concerns (MVC, etc.)
- Follow DRY principle (Don't Repeat Yourself)

### 4. Professional Practices
- Remove debugging print statements
- Remove commented-out old code
- Use version control (Git)
- Keep code clean and readable

## File Naming

Good examples:
- `user_authentication.py`
- `database_manager.js`
- `StudentRecord.java`
- `homepage.html`

Bad examples:
- `stuff.py`
- `test123.js`
- `final_FINAL.java`
- `untitled.html`

## What NOT to Include in Source

- ❌ Compiled files (.pyc, .class, .exe)
- ❌ Build artifacts
- ❌ IDE-specific files (.idea, .vscode)
- ❌ Dependencies (node_modules, venv)
- ❌ Passwords or API keys
- ❌ Large binary files
- ❌ Temporary files

Use `.gitignore` to exclude these!

## Documentation in Code

### Function Documentation Example (Python)
```python
def calculate_total(items, tax_rate):
    """
    Calculate the total cost including tax.
    
    Args:
        items (list): List of item prices
        tax_rate (float): Tax rate as decimal (e.g., 0.2 for 20%)
    
    Returns:
        float: Total cost including tax
    """
    subtotal = sum(items)
    return subtotal * (1 + tax_rate)
```

### Class Documentation Example (Java)
```java
/**
 * Represents a student record in the system.
 * 
 * @author Your Name
 * @version 1.0
 */
public class Student {
    // Class implementation
}
```

## Setup Instructions

Include a README.md in this folder or the parent /code/ folder with:
- Prerequisites (Python version, Node.js, etc.)
- Installation steps
- How to run the application
- Environment variables needed
- Dependencies and how to install them

## Assessment Focus

Examiners look for:
- Well-structured, organized code
- Clear, meaningful comments
- Professional coding standards
- Working, error-free code
- Evidence of good programming practices
- Appropriate use of programming constructs

## Tips

- **Write clean code**: Others need to read it
- **Comment as you go**: Don't leave it to the end
- **Test frequently**: Make sure code works
- **Version control**: Commit regularly
- **Be consistent**: Follow the same style throughout
- **Keep it simple**: Don't over-complicate

## Related Resources

- Keep your actual code here
- Keep tests in `/code/tests/`
- Keep code documentation in `/code/docs/`
- Reference your design documentation

---

**Remember**: Your code should demonstrate your programming skills. Make it clean, professional, and well-documented!
