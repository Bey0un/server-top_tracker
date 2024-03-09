# Makefile sioux
SOURCES = $(wildcard *.c)
OBJECTS = $(SOURCES:.c=.o)
TARGET = serveur
LDFLAGS =  -L../libs/IPC -lpartage -L../libs/Reseau -lserveur -pthread

default:
	gcc -c $(SOURCES) 
	gcc -g $(OBJECTS) -o $(TARGET) $(LDFLAGS)


clean:
	rm -f *.o $(TARGET)
