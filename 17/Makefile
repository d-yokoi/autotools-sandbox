include Makefile.config

SOURCE = $(wildcard *.c)
OBJS = $(SOURCE:.c=.o)
DEPS = $(SOURCE:.c=.d)
-include ${DEPS}

lib: libex.a(${OBJS})

libex.${SHARED_LIBRARY_EXTENSION}: ${OBJS}
	${CC} ${SHARED_LIBRARY_FLAG} -o $@ $^

etags:
	etags *.c *.h

help:
	-@echo "make ex: make the executable"
	-@echo "make etags: build the etags file"
