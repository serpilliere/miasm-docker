This file is part of Miasm2-Docker.

Copyright 2014 [Camille MOUGEY](mailto:commial@gmail.com)

Miasm2-Docker
=============

Automated build for Miasm2

Containers descriptions
=======================

"**Miasm2**" fully functionnal build ([Sources][1]).

Image "**base**" includes:

 - Debian *Jessie*
 - Miasm2
 - Elfesteem
 - TinyCC compiled with *-fPIC* option
 - py-llvm (supported version)


----------

Without arguments, launch test (mono process).

Session example:

    $>  docker run -i -t miasm/base bash
    miasm2@8ee98f936055:/opt/miasm2/test$ cd ../example/
    miasm2@8ee98f936055:/opt/miasm2/example$ python test_jit_arm.py -j python md5_arm A684
    input bytes:       
    00000:  54 45 53 54 31 31 32 32 33 33 34 34 35 35 36 36  |TEST112233445566|
    00010:  37 37 38 38 39 39 41 41 42 42 43 43 44 44 45 45  |778899AABBCCDDEE|
    00020:  46 46 00                                         |FF.|
    
    md5:
    00000:  73 44 2d a7 f7 f9 62 1d ec 3e f2 9c 0c 5f 96 5f  |sD-...b..>.._._|
    miasm2@8ee98f936055:/opt/miasm2/example$


Image "**tested**" includes:

 - Image **base**
 - Success of regression tests



  [1]: http://code.google.com/p/miasm/ "Sources"