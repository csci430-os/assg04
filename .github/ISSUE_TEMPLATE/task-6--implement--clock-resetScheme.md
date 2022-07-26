---
name: 'Task 6: Clock resetScheme() and useBit initializations'
about: Task 6 for Students
title: 'Task 6: Clock resetScheme() and useBit initializations'
labels: enhancement
assignees: ''
---

**Description**

Create a `framePointer` integer and a `useBit` array of booleans
as private member variable data structures of the 
`ClockPageReplacementScheme` class.  Copy over from Fifo and implement
the `resetScheme()` member method for the Clock scheme.  This
method should initialize the `framePointer` to 0.  It also needs
to dynamically allocate an array of `bool` use bits, and initialize
all of the use bits to `true`.

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
