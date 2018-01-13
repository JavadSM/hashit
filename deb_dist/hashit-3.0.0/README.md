Project is hosted on [pypi](https://pypi.org/project/hashit/)

Hashit is an hashing program which can be uses to hash and verify muliple files on a system.
I got the idea from an ubuntu iso image which have this hash table, so i got the idea to make
such a program using python.

### Notice:
some hashes as blake2b and blake2s is not supported in python2
and all shake hashes is disabled for now

## Usage

------------------------------------
Command line wise 
```bash
(python3 -m) hashit [options] $disableFullPath
```
From python you can do it like this
```py
from hashit import hashlib, blockIter, hashIter

file = open("somefile", "rb")

# memory efficent generator
hash = hashIter(blockIter(file, blocksize=65536), hasher=hashlib.md5(), ashexstr=True)

print(hash)

```

## Changelog

------------------------------------------------------------
    3.0.0 - New release, added tests full color-support and CRC32 hashing! (Also added an -a option)

    2.3.0 - Fixed a bunch of code, made it faster better more powerful. Full support for sfv and more!

    2.1.3 - Fixed detect bugs added unit tests and some fixes

    2.1.2 - Done with detect.py working hash detection

    2.1.1 - Some more bugfixed, started working on detect.py

    2.1.0 - Updated to support newest version of argc

    2.0.1 - Bugfixes

    1.2.0 - Full Release

    1.1.0 - Added support for python2 and 

    1.0.2 - Double exits' fixed

    1.0.1 - Fixed printing bug

    1.0.0 - Major version

    0.0.3 - Added documentation and license

    0.0.2 - Fixing script bugs

    0.0.1 - Initial release, ready for use

Works with python2 and python3.