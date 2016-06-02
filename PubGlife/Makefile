CFLAGS = -fopenmp -Wall
OPTFLAG = -O0 -g
CC = g++

# Adjust these as needed to find the X11 and adevs libs and headers
PREFIX = /usr/local
LIBS = -lglut -lGL
LIBPATH = -L/usr/X11R6/lib
INCLUDE = -I${PREFIX}/include -I${PREFIX}/adevs/include -I${PREFIX}/include/hiredis

LIBNAME=/usr/local/lib/libhiredis
DYLIBSUFFIX=so
STLIBSUFFIX=a
DYLIBNAME=$(LIBNAME).$(DYLIBSUFFIX)
STLIBNAME=$(LIBNAME).$(STLIBSUFFIX)

##
# Should not need to edit below this line
##

OBJS = Cell.o PubGlife.o

.SUFFIXES: .cpp
.cpp.o:
	${CC} ${CFLAGS} ${OPTFLAG} ${INCLUDE} -c $<

PubGlife: ${OBJS}
	${CC} -o $@ ${CFLAGS} ${OPTFLAG} ${OBJS} ${LIBS} ${LIBPATH} ${INCLUDE} $(STLIBNAME)

clean:
	rm -f *.o *~ core PubGlife
