# reactive_programming

This repository contains the legacy react module from the Flexx project.
This was an attempt at reactive programming in Python, which seemed
fine at first, but was eventually replaced by a more conventional event
system (`flexx.event`). This repo is kept as a reference. All code
should work, but the tests would need updating (because they have
references to flexx).

Reactive programming is a nice concept, but it fails (for me) for a
couple of reasons:

* It does not work well for GUI apps. For simple ones it may, but once you
  need to distinguish between whether the left or right mouse button was 
  pressed, it breaks down.
* Having to keep signals in sync degraded performance in Flexx, because
  it meant having to update signals between Python and JS. With an event
  system you only need to sync events when there are handlers subscribed
  on the other side.
* The reactive programming paradigm requires a different mind-set that
  inceases the burdon on programmers new to the idea.
