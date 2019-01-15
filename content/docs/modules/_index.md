---
title: Modules
weight: 3
---

Modules add extra functionality to Bennu, as Bennu on its own is just a language and a virtual machine. The default modules contain the basics you need to make a game: video, audio, input, etc. More advanced external libraries are available, like network and 3D rendering.

Enabling a module is easy, using [import](#):

```
import " <modulename> "
```

Some external libraries use a header ([.INC](#)) instead, so use [include](#):

```
include " <includename> "
```
