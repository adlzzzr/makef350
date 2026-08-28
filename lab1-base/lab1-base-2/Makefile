TARGET=main
CC=gcc
CFLAGS=- Wall -DBSD -DNDEBUG


all:$(TARGET)

$(TARGET): flip.o getop.o
	$(CC) $(CFLAGS) -o $@ flip.o getop.o

flip.o: flip.c flip.h
	$(CC) $(CFLAGS) -c $*.c

getop.o: getopt.c
	$(CC) $(CFLAGS) -c $*.c

flip.man: flip.1
	$(CC) $(CLFAGS) -C $*.c

clean:
	rm -rf *.o $(TARGET)

