# Nmake macros for building Windows 32-Bit apps
TARGETOS=BOTH
APPVER=5.0

!include <win32.mak>


objs=addrquery.obj

all: addrquery.exe

# Update the resource if necessary

# Update the object file if necessary

.c.obj: 
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c

# Update the executable file if necessary, and if so, add the resource back in.

addrquery.exe: $(objs) $(common_objs) 
    $(link) $(linkdebug) $(conlflags) -out:addrquery.exe $(objs) $(conlibsmt) ws2_32.lib


clean:
	del *.obj
	del *.exe
