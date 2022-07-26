---
name: 'Task 3: Implement `isPageHit()` PagingSystem member method'
about: Task 3 for Students
title: 'Task 3: Implement `isPageHit()` PagingSystem member method'
labels: enhancement
assignees: ''

---

**Description**

Implement the `isPageHit()` information function of the `PagingSystem` class.
This function also returns a boolean result, and it also does not actually
modify the state of the running simulation, so it is required to be a `const`
member function.

The current page being referenced in the simulation will be
`pageReference[systemTime]`, that is to say, given the current
`systemTime` the page referenced at that time by the simulated page
reference stream is found in the array `pageReference[systemTime]`.
Given the current `systemTime`, the `isPageHit()` function should
return `true` if the page being referenced is currently in `memory`
(which is a page hit).  Otherwise it should return `false`.


**Suggested Solution**

A possible pseudocode implemention of this function is as follows:

```
for each physical frame of memory
   if this memory frame holds the current reference page
      return true, this reference was a hit, we found the page in memory
	  
otherwise if no frame currently has the referenced page loaded
then return false, this reference was a miss
```

**Additional Requirements**

- The `isPageHit()` member method must be declared to be `const`
  member methods as it does not change the simulation state, only
  returns information about current state of memory.
- All methods must have correctly formatted Doxygen documentation before the
  implementation.  This includes a brief title of the method, a 1 or more
  sentence description, and documentation of input parameters using @param
  and return values using @returns tags.


