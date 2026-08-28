TARGET=main
CC=gcc
CFLAGS= -Wall -DBSD -DNDEBUG


all:$(TARGET)

$(TARGET): flip.o getopt.o
	$(CC) $(CFLAGS) -o $@ flip.o getopt.c

flip.o: flip.c flip.h
	$(CC) $(CFLAGS) -c $*.c

getopt.o: getopt.c
	$(CC) $(CFLAGS) -c $*.c

man: flip.1
	nroff -man flip.1 > flip.man

clean:
	rm -rf *.o $(TARGET)

