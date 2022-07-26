---
name: 'Task 1: Implement `PagingSystem` member accessor method'
about: Task 1 for Students
title: 'Task 1: Implement `PagingSystem` member accessor method'
labels: enhancement, good first issue
assignees: ''

---

**Description**

Implement missing `PagingSystem` accessor methods.  You will need to implement
the following 3 missing accessor methods

- `getMemorySize()`
- `getSystemTime()`
- `getNumPageReferences()`

There are subtask test defines for each of these 3, define the tests in order and implement these 3 methods.

All of these member methods are accessor methods.  That means they simply
return information about the state of the object, they do not modify
the state of the object.  Therefore all 3 of these accessor methods must
be declared to be `const` member methods.

All 3 methods take no input parameters, as is typical for an accessor method.
Also as is typical, all 3 return an appropriate result type, giving back
the indicated information.  All methods are simply accessing and returning
a member variable value from the `PagingSystem` class.

**Suggested Solution**




**Additional Requirements**

- All getter accessor methods must be declared to be `const` member methods.
- All methods must have correctly formatted Doxygen documentation before the
  implementation.  This includes a brief title of the method, a 1 or more
  sentence description, and documentation of input parameters using @param
  and return values using @returns tags.
