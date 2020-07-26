Prerequisites:
- At least Python 3.4
- SCons
- libGLFW (GLFW3)
- libdl

To compile, in the top directory, run `/usr/bin/env python3 $(which scons) .`
- You may be able to run just `scons .` to compile, but that may invoke Python 2 by default, depending on your system. If you see errors like the one below, then this is probably the reason why:
```
scons: Reading SConscript files ...
ImportError: No module named pathlib:
  File "/home/bar/foo/scons/SConstruct", line 6:
    from pathlib import Path
```