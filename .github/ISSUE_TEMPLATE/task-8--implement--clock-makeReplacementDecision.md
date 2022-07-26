---
name: 'Task 8: Clock makeReplacementDecision() member function'
about: Task 8 for Students
title: 'Task 8: Clock makeReplacementDecision() member function'
labels: enhancement
assignees: ''
---

**Description**

Implement the `makeReplacementDecision()` function next.  The
replacement decision for Clock is more complex than for Fifo, though you
can start by copying the Fifo replacement decision function.

For Clock, you have a `framePointer`, just like for the Fifo scheme.
But you don't just immediately replace the frame that the
`framePointer` is pointing to.  You first need to scan memory until
you find the next frame that has a use bit set to false (0).  So if the frame
that the frame pointer has a use bit of true (1), you need to flip it to false (0)
and move to the next frame.  Thus you need to implement a loop here
that keeps checking the use bit, and flipping it to false until it finds a
use bit that is unset.

Once a frame is found with a use bit of false, that should be the
frame that is selected to be replaced.  That frame number should be
returned from this function.  But before you return, you should make
sure that the `framePointer` points to the frame after the one that
will be replaced.  You should also set the use bit of the frame that
will be replaced to be 1, because whenever a new page is loaded its
use bit should initially be set to 1.

**Suggested Solution**

The pseudocode to implement the `makeReplacementDecision()` 
looks something like the following:

```
while use bit at current frame pointer is set (true)
    flip the use bit to false
	increment the frame pointer by 1, wrapping around the end of the buffer back to 0 if needed
	
// frame pointer now points to first frame found with use bit of false
remember this frame pointer as it should be returned as the candidate frame to replace

but before returning set the use bit of the frame to replace to true
and increment the frame pointer by 1, wrapping around the end of the buffer if needed

return the rememered frame pointer for replacement
```


**Additional Requirements**

- You have to correctly scan memory for the first frame whose `useBit` is not
  set (set to false).  The first such frame found with a `useBit` of `false`
  should be returned as the frame to replace.
- You have to correctly wrap around memory, treating it as a circular buffer,
  to correctly implement your scan (same as Fifo scheme does with its 
  `framePointer`)
- In order to implement the Clock scheme correctly, you have to set the
  `useBit` of the frame that will be replaced to `true`, in anticipation of
  loading the next new page.
- Likewise to implement Clock correctly, you also have to increment the
  `framePointer` (possibly wrapping it around the buffer) in anticipation for
  the start of the next scan for an unset `useBit`.
