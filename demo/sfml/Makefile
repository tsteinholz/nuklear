# Install
BIN = demo

# Flags
CFLAGS = -pedantic -O2

SRC = main.cpp
OBJ = $(SRC:.c=.o)

ifeq ($(OS),Windows_NT)
BIN := $(BIN).exe
LIBS = -lmingw32 -lsfml-graphics -lsfml-window -lsfml-system -lm
else
LIBS = -lsfml-graphics -lsfml-window -lsfml-system -lm
endif

$(BIN):
	@mkdir -p bin
	rm -f bin/$(BIN) $(OBJS)
	g++ $(SRC) $(CFLAGS) -o bin/$(BIN) $(LIBS)
