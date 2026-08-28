TARGET=main
CC=gcc
CFLAGS= -Wall -DBSD -DNDEBUG


all:$(TARGET)

$(TARGET): flip.o getop.c
	$(CC) $(CFLAGS) -o $@ flip.o getop.c

flip.o: flip.c flip.h
	$(CC) $(CFLAGS) -c $*.c

getop.c: getop.C
	$(CC) $(CFLAGS) -c $*.c

flip.man: flip.1
	$(CC) $(CFLAGS) -C $*.c

clean:
	rm -rf *.o $(TARGET)

