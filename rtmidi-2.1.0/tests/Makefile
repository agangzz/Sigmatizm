### Do not edit -- Generated by 'configure --with-whatever' from Makefile.in
### RtMidi tests Makefile - for various flavors of unix

PROGRAMS = midiprobe midiout qmidiin cmidiin sysextest
RM = /bin/rm
SRC_PATH = ..
INCLUDE = ..
OBJECT_PATH = Release
vpath %.o $(OBJECT_PATH)

OBJECTS	=	RtMidi.o

CC       = g++
DEFS     =   -D__LINUX_ALSA__
CFLAGS   = -O3 -Wall -Wextra
CFLAGS  += -I$(INCLUDE) -I$(INCLUDE)/include
LIBRARY  = -lpthread -lasound 

%.o : $(SRC_PATH)/%.cpp
	$(CC) $(CFLAGS) $(DEFS) -c $(<) -o $(OBJECT_PATH)/$@

all : $(PROGRAMS)

midiprobe : midiprobe.cpp $(OBJECTS)
	$(CC) $(CFLAGS) $(DEFS) -o midiprobe midiprobe.cpp $(OBJECT_PATH)/RtMidi.o $(LIBRARY)

midiout : midiout.cpp $(OBJECTS)
	$(CC) $(CFLAGS) $(DEFS) -o midiout midiout.cpp $(OBJECT_PATH)/RtMidi.o $(LIBRARY)

qmidiin : qmidiin.cpp $(OBJECTS)
	$(CC) $(CFLAGS) $(DEFS) -o qmidiin qmidiin.cpp $(OBJECT_PATH)/RtMidi.o $(LIBRARY)

cmidiin : cmidiin.cpp $(OBJECTS)
	$(CC) $(CFLAGS) $(DEFS) -o cmidiin cmidiin.cpp $(OBJECT_PATH)/RtMidi.o $(LIBRARY)

sysextest : sysextest.cpp $(OBJECTS)
	$(CC) $(CFLAGS) $(DEFS) -o sysextest sysextest.cpp $(OBJECT_PATH)/RtMidi.o $(LIBRARY)

clean : 
	$(RM) -f $(OBJECT_PATH)/*.o
	$(RM) -f $(PROGRAMS) *.exe
	$(RM) -f *~
	$(RM) -fR *.dSYM

distclean: clean
	$(RM) -f Makefile

strip : 
	strip $(PROGRAMS)
