---
name: 'Task 7: Clock pageHit() member function'
about: Task 7 for Students
title: 'Task 7: Clock pageHit() member function'
labels: enhancement
assignees: ''
---

**Description**

Implement the `pageHit()` member function.  The FIFO class
doesn't need to do anything for a page hit (so there is nothing to
copy to begin with here).  But for the Clock scheme, you have to set
the use bit to true (1) for a page hit.  When the `pageHit()` function
is called, the frame number of the page that was hit is provided as
the parameter, so you simply need to set the use bit of that
corresponding frame to 1 to handle a page hit.

**Suggested Solution**


**Additional Requirements**

- The name of the use bits array is `useBit`.  This is required by
  the tests of this part of the Clock scheme implementation.
- The use bits have to be of type `bool` and they have to be initially
  initialized to `true` in anticipation of initial page placements.
- The use bits need to be dynamically allocated, using the `new`
  c++ keyword to dynamically allocate memory.  Enough memory needs
  to be allocated to hold use bits for all frames of memory, so you
  need to access the `memorySize` of the paging system simulation
  object that is controlling this Clock object.
