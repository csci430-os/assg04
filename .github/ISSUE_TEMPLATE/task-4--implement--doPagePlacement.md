---
name: 'Task 4: Implement `doPagePlacement()` PagingSystem member method'
about: Task 4 for Students
title: 'Task 4: Implement `doPagePlacement()` PagingSystem member method'
labels: enhancement
assignees: ''
---

**Description**

Before defining the task 4 tests, Start by uncommenting if/else at
bottom of `processNextPageReference()` for handling a page fault/miss.
Now that the `isMemoryFull()` is implemented, we can uncomment this
code, to do placements or replacements, and test your implementation
of `doPagePlacement()` next.

The code will not compile at this point until you create at least a
stub function for the `doPagePlacement()` method.  So as usual define
the tests for task 4, and create a header and stub function for
`doPagePlacement()`, and make sure code is compiling and running again
before proceeding.

The `doPagePlacement()` member method does change the state of the
simulation, so it is not a `const` member method.  This method does not
have any input parameters, and it is a `void` function that does not return any
result.  All of the work it performs is done as a side effect, it places
a newly referenced page into the simulated memory.


**Suggested Solution**

The following is an example of pseudocode that will implement the
page placement for the simulation:

```
if memory is full
   throw exception indicating this is a simulation error and this method should not be
   called when memory is full
   
   
for each frame of memory
   if this frame of memory is empty
      place the current reference page in this empty frame
	  and return immediatly (e.g. don't make mistake of putting page in multiple empty frames)
```

**Additional Requirements**

- You must test for and throw an exception in `doPagePlacement()` if this
  function is called when memory is full.  Page placements can only occur
  when there is at least 1 or more frames of memory currently empty to place
  the referenced page into.
- You are required to use the `EMPTY_FRAME` global defined constant, rather
  than using magic numbers like 0 to indicate empty frames in your code.
- All methods must have correctly formatted Doxygen documentation before the
  implementation.  This includes a brief title of the method, a 1 or more
  sentence description, and documentation of input parameters using @param
  and return values using @returns tags.
