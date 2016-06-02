CFLAGS = -fopenmp -Wall
OPTFLAG = -O0 -g
CC = cc

AE_DIR=/home/greg/src/redis-3.2.0/src
AE_OBJS=$(AE_DIR)/ae.o $(AE_DIR)/zmalloc.o
AE_LIBS=$(AE_DIR)/../deps/jemalloc/lib/libjemalloc.a

# Adjust these as needed to find the X11 and adevs libs and headers
PREFIX = /usr/local
LIBS = -lglut -lGL
LIBPATH = -L/usr/X11R6/lib
INCLUDE = -I${PREFIX}/include

LIBNAME=/usr/local/lib/libhiredis
DYLIBSUFFIX=so
STLIBSUFFIX=a
DYLIBNAME=$(LIBNAME).$(DYLIBSUFFIX)
STLIBNAME=$(LIBNAME).$(STLIBSUFFIX)

##
# Should not need to edit below this line
##

OBJS = SubGlife.o

.SUFFIXES: .c
.c.o:
	${CC} ${CFLAGS} ${OPTFLAG} ${INCLUDE} -c $<

SubGlife: ${OBJS}
	${CC} -o $@ ${CFLAGS} ${OPTFLAG} ${OBJS} $(AE_OBJS) $(AE_LIBS) ${LIBS} ${LIBPATH} ${INCLUDE} $(STLIBNAME)

clean:
	rm -f *.o *~ core output SubGlife
