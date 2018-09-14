# Tiny Oberon System

Tiny Oberon System, a native subset of [projectoberon.com](http://www.projectoberon.com) that provides a minimal base system to build upon.

This project focuses on the bare essentials that make it an Oberon System (i.e. the main system loop, input and output (Viewer) handling.
This implementation has the following goals:

* Very small and understandable code base (a subset of the [Project Oberon](http://www.projectoberon.com) code, not a re-imagination)
* Native compilation using the [OBNC](http://miasap.se/obnc/) compiler
* [SDL](https://www.libsdl.org/) based graphics

The most important goal is to have a small code base that can be understood in its entirety in a couple of hours.
In other words you bootstrap your own Oberon System based on this tiny implementation and do either of the following:

1. Extend it in small steps while studying the [Project Oberon](http://www.projectoberon.com) book towards a more complete implementation
2. Use it as an example or starting point to explore a different approach in systems design

Things that are deliberately left out in a Tiny Oberon System:

* Linker/Loader
* Compiler
* Networking
* Applications

As a consequence a Tiny Oberon System has no way to load and execute applications on its own, requiring applications to be hardcoded and to recompile the system.
The most logical subsequent step is to add a loader, which arguably would need a compiler first (OBNC doesn't produce Oberon .Obj files). To shorten the distance one could decide to [use an existing assembler to build a raw binary](https://www.nasm.us/doc/nasmdoc7.html#section-7.1.3) formatted as Oberon module object file and focus on building the loader first.

![](https://i.imgur.com/CU32coq.png)
