# irixswextract

Tool to extract IRIX archives with idb descriptor files

Original program by [camthesaxman](https://github.com/camthesaxman). Added some modifications.

Modifications:
Symbolic Links supported.
Program doesnt terminate on decompression failure.
Better handling of archives, temp .z archives get deleted

Specific Compilation Prerequisites:
[liblzw](https://github.com/vapier/liblzw)

For some reason, liblzw needs to be linked with -static on my computer, else I get a library can't be found error.

Example compilation:
``gcc irixswextract.c -static -o irixswextract -llzw``

Known bugs:
Path to output directory only supports a relative path.

Example usage:
``irixswextract . c_dev.idb ../../n64dev/root``

iirc, there is another idb file format that is not implemented in this program at this moment.
