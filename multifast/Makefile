PROGRAM := multifast
PATH_INCLUDE := ../ahocorasick
PATH_LIBRARY := ../ahocorasick
ACLIB := ahocorasick
CFLAGS := -Wall
HERADERS := multifast.h pattern.h reader.h strmm.h walker.h
OBJS := multifast.o pattern.o reader.o strmm.o walker.o

ifeq ($(wildcard $(PATH_LIBRARY)/lib$(ACLIB).a),) 
all:;@echo 'Please go to ../ahocorasick directory and complie it first.'
else
all: $(PROGRAM)
endif

$(PROGRAM): $(OBJS)
	cc -o $(PROGRAM) $(OBJS) $(CFLAGS) -L$(PATH_LIBRARY) -l$(ACLIB)

multifast.o: multifast.c $(HERADERS)
	cc -c multifast.c $(CFLAGS) -I$(PATH_INCLUDE)
pattern.o: pattern.c $(HERADERS)
	cc -c pattern.c $(CFLAGS) -I$(PATH_INCLUDE)
reader.o: reader.c $(HERADERS)
	cc -c reader.c $(CFLAGS) -I$(PATH_INCLUDE)
strmm.o: strmm.c $(HERADERS)
	cc -c strmm.c $(CFLAGS) -I$(PATH_INCLUDE)
walker.o: walker.c $(HERADERS)
	cc -c walker.c $(CFLAGS) -I$(PATH_INCLUDE)

clean:
	rm -f $(PROGRAM) $(OBJS)
