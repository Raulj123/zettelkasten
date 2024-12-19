Availability is the time a system remains operational to perform its required function in a specific period.
* Measured in 9's                 90% -> 36 days    99% -> 3 days etc.
# Availability in Sequence vs Parallel
**Key Idea**:  
The availability of a service depends on how its components (like "Foo" and "Bar") are connected — either **in sequence** or **in parallel**.

---
### Sequence (Components depend on each other)
- **Rule**: If one component fails, the whole service fails.
- **Formula**:  
	A = A1 * A2 
- **Example**:
    - If Foo = 99.9% and Bar = 99.9%, then:  
        A = 99.9 * 99.9 = 98%
    - **Takeaway**: Adding components **in sequence ==lowers availability**== because both need to work perfectly.
### Parallel (Components back each other up)
- **Rule**: Service still works as long as at least one component is working.
- **Formula**:  
	 A = 1 -(1 - A1) * (1 - A2)
- **Example**:
    - **Takeaway**: Adding components **in parallel ==increases availability**== because they provide backup for each other.

### Availability vs. Reliability
- **Availability**: A system is "up" and usable.
- **Reliability**: A system works without failure for a long time.
- **Relationship**:
    - **High reliability = High availability** (if it rarely breaks, it’s usually up).
    - **High availability ≠ High reliability** (even unreliable systems can stay "up" with enough backups).