---
name: 'Task 5: Enable full `PagingSystem` simulation and fix Fifo class'
about: Task 5 for Students
title: 'Task 5: Enable full `PagingSystem` simulation and fix Fifo class'
labels: enhancement
assignees: ''
---

**Description**

Uncomment disabled code in the `PagingSystem` implementation file to
enable full simulations.  Check the following member functions to find
disable code and make sure it is enabled:

- `getPageStatys()` needs to call both `isPageHit()` and `isMemoryFull()` to determine
  status for output for full simulations.
- You should already have enabled the use of `isMemoryFull()` and `doPagePlacement()`
  in the `processNextPageReference()` method in previous task 4.
- `doPageReplacement()` also has commented out a call to `isMemoryFull()`, simply checking
  for an error condition.  Page replacement should NOT be done if there are still
  empty frames of memory.  The check here is similar to what you should have done in
  task 4 to test if memory is full when being asked to do a page placement.

Also fix implementation of the `FifoPageReplacementScheme` class.  Need to
add in code to get the memory size from the PagingSystem `sys` object in the
following member function of the Fifo scheme:

- `getSchemeStatus()`
- `makeReplacementDecision()`

**Suggested Solution**


**Additional Requirements**

