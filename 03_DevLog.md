# 03 - Development Log

**Timeframe:** Month 5–9  
**Target Month:** Month 9

## Navigation
⬅️ [Previous: Design](02_Design.md) | ➡️ [Next: Testing](04_Testing.md)

---

## What to Do

The Development Log is where you document your implementation process. This is NOT just about writing code - it's about recording your development journey, decisions, problems, and solutions.

### Key Activities

1. **Iterative Development**
   - Build your solution in small, manageable increments
   - Implement features one at a time
   - Test each feature before moving to the next

2. **Version Control**
   - Use Git or similar version control
   - Make regular, meaningful commits
   - Use descriptive commit messages

3. **Documentation**
   - Log every development session
   - Record problems encountered and solutions
   - Document code with comments
   - Screenshot key stages of development

4. **Stakeholder Feedback**
   - Show progress to stakeholder regularly
   - Incorporate feedback into development
   - Document feedback and responses

5. **Code Quality**
   - Follow coding standards and conventions
   - Write clean, readable code
   - Refactor as needed
   - Use meaningful variable/function names

## Checklist

### Development Process
- [ ] Implemented all essential requirements
- [ ] Developed in iterative cycles (not all at once)
- [ ] Tested each feature before moving to next
- [ ] Followed good coding practices and conventions

### Development Log Entries
- [ ] Created log entry for each development session
- [ ] Minimum 15-20 substantial log entries
- [ ] Each entry includes: date, time spent, what was done
- [ ] Documented problems and how they were solved
- [ ] Included code snippets showing key implementations

### Version Control
- [ ] Used Git (or similar) throughout development
- [ ] Made regular commits (not just one big commit)
- [ ] Commit messages are descriptive
- [ ] Can demonstrate project evolution through commits

### Code Quality
- [ ] Code is well-structured and modular
- [ ] Functions/methods are appropriately sized
- [ ] Variable/function names are meaningful
- [ ] Code includes appropriate comments
- [ ] No unnecessary repetition (DRY principle)

### Evidence
- [ ] Screenshots showing UI development stages
- [ ] Code snippets demonstrating key algorithms
- [ ] Error messages and debugging process documented
- [ ] Evidence of stakeholder feedback incorporated

### Problem-Solving Documentation
- [ ] Documented at least 5-8 significant problems
- [ ] Explained attempted solutions
- [ ] Described final solutions and why they worked
- [ ] Included research (Stack Overflow, documentation, etc.)

### Stakeholder Interaction
- [ ] Regular progress demos (minimum 3-4 during development)
- [ ] Documented stakeholder feedback
- [ ] Showed how feedback was incorporated
- [ ] Evidence of requirements being refined based on feedback

## Common Pitfalls

### ❌ Writing Log After the Fact
**Pitfall:** Writing all development log entries at the end of the project.  
**Solution:** Write entries AS YOU CODE. Contemporaneous documentation is obvious and valued by examiners.

### ❌ Trivial Log Entries
**Pitfall:** Entries like "Fixed a bug" or "Added a feature" with no detail.  
**Solution:** Each entry should be substantial - explain WHAT you did, WHY, HOW, and what problems you faced.

### ❌ No Evidence of Problems
**Pitfall:** Claiming development was smooth with no issues.  
**Solution:** Everyone faces problems. Document errors, bugs, and challenges - and how you solved them. This demonstrates problem-solving skills.

### ❌ Poor Code Quality
**Pitfall:** Writing messy, uncommented code with poor structure.  
**Solution:** Write professional code. Use functions/classes, follow naming conventions, add comments, and refactor as needed.

### ❌ Big Bang Development
**Pitfall:** Writing all the code in one go without testing.  
**Solution:** Use iterative development. Build feature by feature, test each one, then move on.

### ❌ No Version Control
**Pitfall:** Not using Git or only committing once at the end.  
**Solution:** Make regular commits throughout development. This provides evidence of iterative development.

### ❌ Ignoring Stakeholder
**Pitfall:** Not showing progress to stakeholder until the end.  
**Solution:** Demo your progress regularly (every 2-3 weeks). Get feedback and incorporate it.

### ❌ Copy-Paste Code
**Pitfall:** Copying large chunks of code without understanding.  
**Solution:** You can use libraries and reference code, but understand and adapt it. Document sources.

### ❌ No Screenshots
**Pitfall:** Text-only development log with no visual evidence.  
**Solution:** Include screenshots showing UI development, error messages, testing output, etc.

## Development Log Entry Structure

Each log entry should include:

### 1. Entry Header
- **Date:** [DD/MM/YYYY]
- **Time Spent:** [Hours]
- **Development Cycle:** [e.g., Cycle 3]

### 2. Objectives
- What you planned to achieve in this session

### 3. Work Completed
- Detailed description of what was implemented
- Code snippets (if relevant)
- Screenshots of progress

### 4. Problems Encountered
- Any errors, bugs, or challenges
- Error messages (if applicable)
- Why the problem occurred

### 5. Solutions
- How you solved each problem
- Research conducted (with sources)
- Alternative approaches tried

### 6. Testing
- How you tested the new features
- Results of testing
- Any bugs found and fixed

### 7. Next Steps
- What you plan to do in the next session

### 8. Evidence
- Screenshots
- Code snippets
- Commit references

## Example Development Log Entry

```markdown
## Development Log Entry #7

**Date:** 15/12/2025  
**Time Spent:** 3 hours  
**Development Cycle:** Cycle 4 - User Authentication

### Objectives
- Implement password hashing
- Create login validation
- Add session management

### Work Completed
I implemented secure password hashing using the bcrypt library. Here's the 
key function:

```python
def hash_password(password):
    salt = bcrypt.gensalt()
    hashed = bcrypt.hashpw(password.encode('utf-8'), salt)
    return hashed
```

I also created the login validation function that checks the user's credentials
against the database...

[Include more detail]

### Problems Encountered
**Problem 1:** Passwords weren't validating correctly even when correct.

**Error:** `ValueError: Invalid salt`

I realized I was storing the salt separately from the hash, but bcrypt 
actually includes the salt in the hash string. This was causing validation
to fail.

### Solutions
I modified the database schema to store the complete hash (which includes 
the salt) in a single field. Then updated the validation function:

```python
def verify_password(password, stored_hash):
    return bcrypt.checkpw(password.encode('utf-8'), stored_hash)
```

I researched this on bcrypt documentation and Stack Overflow [1].

### Testing
- Tested with correct password: ✓ Login successful
- Tested with incorrect password: ✓ Login denied
- Tested with special characters in password: ✓ Works correctly

### Next Steps
- Implement session timeout
- Add "Remember Me" functionality
- Create password reset feature

### Evidence
[Screenshot of successful login]
[Screenshot of database showing hashed passwords]

### References
[1] https://stackoverflow.com/questions/...
```

## Tips for Success

- **Be Honest:** Don't pretend everything went perfectly. Problems and solutions show skill.
- **Be Regular:** Write entries as you work, not all at once at the end.
- **Be Detailed:** Explain your thinking, not just what you did.
- **Use Evidence:** Screenshots, code snippets, error messages - include everything.
- **Reference Sources:** If you used tutorials or Stack Overflow, cite them properly.

## Assessment Focus

Examiners look for:
- Evidence of regular, iterative development
- Substantial, detailed log entries (not token entries)
- Problem-solving and debugging skills
- Technical understanding of the code
- Good coding practices and standards
- Regular stakeholder engagement
- Appropriate use of version control
- Clear evolution of the project over time

## Recommended Development Cycles

Break development into 8-12 cycles:

1. **Cycle 1:** Basic project setup and structure
2. **Cycle 2:** Core data structures implementation
3. **Cycle 3:** First major feature
4. **Cycle 4:** Second major feature
5. **Cycle 5:** User interface implementation
6. **Cycle 6:** Data persistence (file/database)
7. **Cycle 7:** Third major feature
8. **Cycle 8:** Error handling and validation
9. **Cycle 9:** Integration of components
10. **Cycle 10:** Bug fixes and refinements
11. **Cycle 11:** Performance optimization
12. **Cycle 12:** Final polish and improvements

## Code Documentation Standards

- **File Headers:** Include purpose, author, date
- **Function/Method Comments:** Describe purpose, parameters, return values
- **Inline Comments:** Explain complex logic
- **README:** How to run your project

```python
def search_database(query, filters=None):
    """
    Search the database for items matching the query.
    
    Args:
        query (str): Search term to match against item names
        filters (dict): Optional filters to apply (category, price range, etc.)
    
    Returns:
        list: List of matching items sorted by relevance
        
    Raises:
        ValueError: If query is empty or None
    """
    # Implementation here
```

---

## Navigation
⬅️ [Previous: Design](02_Design.md) | ➡️ [Next: Testing](04_Testing.md)
