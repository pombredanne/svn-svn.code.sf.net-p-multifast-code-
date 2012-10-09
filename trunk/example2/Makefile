PATH_INCLUDE := ../ahocorasick
PATH_LIBRARY := ../ahocorasick
ACLIB := ahocorasick

ifeq ($(wildcard $(PATH_LIBRARY)/lib$(ACLIB).a),) 
all:;@echo 'Please go to ../ahocorasick directory and complie it first.'
else
all: example2
endif

example2: example2.o
	cc -o example2 example2.o -l$(ACLIB) -L$(PATH_LIBRARY)

example2.o: example2.c
	cc -I$(PATH_INCLUDE) -Wall -c example2.c

clean:
	rm -rf example2.o example2
