# redis library Makefile

# source files.
SRC =   redis_lib.c

OBJ =   redis_lib.o
 
#OBJ = $(SRC:.c=.o)
 
OUT = ../libredis.a
 
# include directories
INCLUDES = -I. -I../deps/hiredis -I/usr/include -I/usr/include/linux -I/usr/include/c++/4.8/tr1/ -I/usr/include/c++/4.8/
 
# C++ compiler flags (-g -O2 -Wall)
CCFLAGS = -g
 
# compiler
CCC = gcc
 
# library paths
LIBS = -L../ -L/usr/local/lib ../deps/hiredis/libhiredis.a -lpthread -levent
 
# compile flags
LDFLAGS = -g
 
.SUFFIXES: .c

all: default
 
default: dep $(OUT)
 
redis_lib.o : redis_lib.c
	$(CCC) $(CCFLAGS) -c redis_lib.c
 
$(OUT): $(OBJ)
	ar rcs $(OUT) $(OBJ)
 
depend: dep
 
dep:
	makedepend -- $(CCFLAGS) -- $(INCLUDES) $(SRC)
 
clean:
	rm -f $(OBJ) $(OUT) Makefile.bak
# DO NOT DELETE

redis_lib.o: redis_lib.h ../deps/hiredis/hiredis.h /usr/include/stdio.h
redis_lib.o: /usr/include/features.h /usr/include/stdc-predef.h
redis_lib.o: /usr/include/linux/stddef.h /usr/include/libio.h
redis_lib.o: /usr/include/_G_config.h /usr/include/wchar.h
redis_lib.o: ../deps/hiredis/async.h ../deps/hiredis/hiredis.h
redis_lib.o: /usr/include/string.h /usr/include/xlocale.h
redis_lib.o: /usr/include/signal.h /usr/include/time.h /usr/include/stdint.h
redis_lib.o: /usr/include/stdlib.h /usr/include/alloca.h
redis_lib.o: /usr/include/pthread.h /usr/include/endian.h
redis_lib.o: /usr/include/sched.h
