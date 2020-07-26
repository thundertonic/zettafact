#!/usr/bin/env python3

EnsureSConsVersion(3, 0, 0)

import os
from pathlib import Path

env = Environment()

srcdir = 'src'
includedir = 'include'

srcpath = Path(Dir('.').path) / srcdir
includepath = Path(Dir('.').path) / includedir

source = []

# add every file in src to the source
for f in os.listdir(srcpath):
    
    if os.path.isdir(f):
        continue
    
    elif f.endswith('.cpp') or f.endswith('.c') or f.endswith('.h'):
        source.append(srcdir + '/' + f)

print(source)


# # not sure if it is a bug with scons, but when you add the LIBS argument to the Program function, scons completely ignores these pkg-config...commenting this for now in case anybody has an answer as to why
# env.ParseConfig('pkg-config --cflags --libs glfw3')
# env.ParseConfig('pkg-config --cflags --libs gl')

# build
env.Program(target = 'bin/zettafact', source=source, CPPPATH=['src', 'include'], LIBS=['libdl', 'libglfw'])