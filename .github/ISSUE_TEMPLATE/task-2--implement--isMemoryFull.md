---
name: 'Task 2: Implement `isMemoryFull` member function'
about: Task 2 for Students
title: 'Task 2: Implement `isMemoryFull` member function'
labels: enhancement
assignees: ''

---

**Description**

Implement the `isMemoryFull()` member method.  This method returns a
`bool` result.  It should return `true` if memory is currently full,
that is to say if all frames have a page currently loaded into them
(or equivalently, no frame is currently an `EMPTY_FRAME`).  This
function does not change the state of the simulation, it only returns
information about the current state of memory, so it should be a `const`
member function.  This function does not have any parameters as input.

**Suggested Solution**

```
for each physical frame of memory
   if this frame in memory is EMPTY_FRAME
       return false, the memory is not yet full
	   
otherwise if all frames were not empty, return true, the memory is full
```


**Additional Requirements**

- The `isMemoryFull()` member method must be declared to be `const`
  member methods as it does not change the simulation state, only
  returns information about current state of memory.
- You are required to use the `EMPTY_FRAME` global defined constant, rather
  than using magic numbers like 0 to indicate empty frames in your code.
- All methods must have correctly formatted Doxygen documentation before the
  implementation.  This includes a brief title of the method, a 1 or more
  sentence description, and documentation of input parameters using @param
  and return values using @returns tags.


