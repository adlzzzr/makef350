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

flip.man: flip.1
	$(CC) $(CFLAGS) -C $*.c

clean:
	rm -rf *.o $(TARGET)

