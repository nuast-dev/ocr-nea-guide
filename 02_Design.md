# 02 - Design Phase

**Timeframe:** Month 3–4  
**Target Month:** Month 4

## Navigation
⬅️ [Previous: Analysis](01_Analysis.md) | ➡️ [Next: Development Log](03_DevLog.md)

---

## What to Do

The Design phase is where you plan HOW you will build your solution. This is where you make key technical decisions before writing any code.

### Key Activities

1. **System Architecture**
   - Define overall system structure
   - Identify major components/modules
   - Plan how components interact

2. **Algorithm Design**
   - Design key algorithms using pseudocode
   - Consider efficiency and complexity
   - Plan data processing logic

3. **Data Structures**
   - Choose appropriate data structures
   - Design database schema (if applicable)
   - Plan data validation and storage

4. **User Interface Design**
   - Create wireframes/mockups
   - Plan user workflows
   - Design for usability

5. **Technical Decisions**
   - Select programming language(s)
   - Choose development tools and libraries
   - Plan testing approach

## Checklist

### System Architecture
- [ ] Created system architecture diagram showing all components
- [ ] Identified all major modules/classes
- [ ] Documented component interactions
- [ ] Justified architectural choices

### Algorithm Design
- [ ] Designed 3-5 key algorithms in pseudocode
- [ ] Included flowcharts for complex logic
- [ ] Analyzed time/space complexity where relevant
- [ ] Explained algorithm choices and alternatives considered

### Data Design
- [ ] Chosen appropriate data structures for all major data
- [ ] Designed database schema (if using database)
- [ ] Created entity-relationship diagrams (if applicable)
- [ ] Planned data validation rules
- [ ] Designed file formats (if using files)

### User Interface Design
- [ ] Created wireframes/mockups for all main screens
- [ ] Designed navigation flow between screens
- [ ] Planned error messages and user feedback
- [ ] Considered accessibility and usability
- [ ] Obtained stakeholder feedback on designs

### Technical Specifications
- [ ] Justified choice of programming language
- [ ] Listed all libraries/frameworks to be used
- [ ] Identified development tools (IDE, version control, etc.)
- [ ] Planned project structure and file organization

### Test Planning
- [ ] Defined test strategy (unit, integration, user testing)
- [ ] Created initial test plan linked to requirements
- [ ] Planned test data and scenarios

### Documentation Quality
- [ ] All diagrams are clear and properly labeled
- [ ] Justifications provided for all major decisions
- [ ] Alternative approaches discussed
- [ ] Proofread for clarity and professionalism

## Common Pitfalls

### ❌ Diving Straight into Code
**Pitfall:** Starting to code without completing design.  
**Solution:** Complete ALL design work first. Good design saves time and prevents major rewrites later.

### ❌ Vague Diagrams
**Pitfall:** Creating unclear or unlabeled diagrams.  
**Solution:** Use standard notation (UML, flowchart symbols). Label everything clearly. Include a key if needed.

### ❌ No Justification
**Pitfall:** Not explaining why you made design choices.  
**Solution:** For every major decision (language, algorithm, data structure), explain why you chose it and what alternatives you considered.

### ❌ Over-Ambitious Design
**Pitfall:** Designing a system too complex to implement.  
**Solution:** Keep designs realistic. It's better to fully implement a simpler design than partially implement a complex one.

### ❌ Missing UI Design
**Pitfall:** Focusing only on backend/logic and neglecting UI.  
**Solution:** Create detailed wireframes/mockups. UI design is crucial and should be well-documented.

### ❌ No Data Validation
**Pitfall:** Not planning how to validate user input.  
**Solution:** For every input, specify validation rules, error handling, and user feedback.

### ❌ Ignoring Stakeholder Feedback
**Pitfall:** Not showing designs to your stakeholder.  
**Solution:** Review designs with stakeholder and incorporate their feedback. Document this process.

### ❌ Pseudocode = Real Code
**Pitfall:** Writing pseudocode that's actually just code.  
**Solution:** Pseudocode should be language-agnostic and focus on logic, not syntax.

### ❌ No Algorithm Complexity
**Pitfall:** Not considering efficiency of algorithms.  
**Solution:** For key algorithms, discuss Big O notation and why your choice is appropriate.

## Section Structure

Your Design section should include:

1. **Introduction** (0.5-1 page)
   - Overview of design approach
   - Summary of key design decisions

2. **System Architecture** (2-3 pages)
   - High-level system diagram
   - Component descriptions
   - Component interaction diagrams
   - Justification of architecture

3. **Algorithm Design** (3-5 pages)
   - Pseudocode for 3-5 key algorithms
   - Flowcharts for complex logic
   - Complexity analysis
   - Alternative algorithms considered

4. **Data Design** (2-3 pages)
   - Data structure choices and justifications
   - Database schema/ER diagrams
   - Data dictionary
   - Validation rules

5. **User Interface Design** (2-4 pages)
   - Wireframes/mockups for all screens
   - Navigation diagrams
   - UI element specifications
   - Stakeholder feedback on designs

6. **Technical Specifications** (1-2 pages)
   - Programming language justification
   - Libraries and frameworks
   - Development tools
   - Project structure

7. **Test Plan** (1-2 pages)
   - Test strategy overview
   - Initial test cases
   - Test data requirements

**Total Expected Length:** 15-20 pages

## Tips for Success

- **Use Standard Notation:** UML class diagrams, flowcharts, ER diagrams - use recognized standards.
- **Be Detailed:** Don't just show a diagram - explain it thoroughly.
- **Show Alternatives:** For major decisions, discuss what else you considered and why you didn't choose those options.
- **Get Feedback:** Share designs with your stakeholder and teacher - incorporate their suggestions.
- **Think About Edge Cases:** Design for error handling and unusual inputs.

## Assessment Focus

Examiners look for:
- Clear, detailed system architecture
- Well-designed algorithms with justification
- Appropriate data structures and database design
- Professional UI designs with usability considerations
- Justified technical choices
- Comprehensive test planning
- Evidence of iterative design with stakeholder input

## Example Diagrams to Include

### System Architecture Diagram
```
[User Interface Layer]
         ↓
[Business Logic Layer]
         ↓
[Data Access Layer]
         ↓
    [Database]
```

### Flowchart Example
```
[Start] → [Input Data] → <Valid?> 
                           ├─ No → [Error Message] → [Input Data]
                           └─ Yes → [Process] → [Output] → [End]
```

### Class Diagram Example
```
┌─────────────────┐
│     User        │
├─────────────────┤
│ - username: str │
│ - email: str    │
├─────────────────┤
│ + login()       │
│ + logout()      │
└─────────────────┘
```

## Example Pseudocode Format

```
FUNCTION searchItems(query)
    results ← EMPTY LIST
    
    FOR EACH item IN database
        IF item.name CONTAINS query THEN
            ADD item TO results
        END IF
    END FOR
    
    SORT results BY relevance
    RETURN results
END FUNCTION
```

## Design Tools Recommendations

- **Diagrams:** draw.io, Lucidchart, Microsoft Visio
- **Wireframes:** Figma, Balsamiq, Adobe XD
- **Flowcharts:** draw.io, Microsoft Visio
- **Database Design:** dbdiagram.io, MySQL Workbench

---

## Navigation
⬅️ [Previous: Analysis](01_Analysis.md) | ➡️ [Next: Development Log](03_DevLog.md)
