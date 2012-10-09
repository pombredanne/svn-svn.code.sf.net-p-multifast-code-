PATH_INCLUDE := ../ahocorasick
PATH_LIBRARY := ../ahocorasick
ACLIB := ahocorasick

ifeq ($(wildcard $(PATH_LIBRARY)/lib$(ACLIB).a),) 
all:;@echo 'Please go to ../ahocorasick directory and complie it first.'
else
all: example1
endif

example1: example1.o
	cc -o example1 example1.o -l$(ACLIB) -L$(PATH_LIBRARY)

example1.o: example1.c
	cc -I$(PATH_INCLUDE) -Wall -c example1.c

clean:
	rm -rf example1.o example1
