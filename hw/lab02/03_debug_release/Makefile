
CXX = g++
MODE ?= release

ifeq ($(MODE),debug)
    CXXFLAGS = -Wall -Wextra -g -O0
else ifeq ($(MODE),release)
    CXXFLAGS = -Wall -Wextra -O3
else
    $(error Unknown MODE: $(MODE). Use debug or release)
endif

TARGET = calculator
OBJ_DIR = obj/$(MODE)

SRCS = $(wildcard *.cpp)
OBJS = $(patsubst %.cpp,$(OBJ_DIR)/%.o,$(SRCS))

.PHONY: all clean FORCE

all: $(TARGET)

$(TARGET): $(OBJS) FORCE
	$(CXX) $(CXXFLAGS) -o $@ $(OBJS)

$(OBJ_DIR)/%.o: %.cpp
	mkdir -p $(OBJ_DIR)
	$(CXX) $(CXXFLAGS) -c $< -o $@

FORCE:

clean:
	rm -rf obj calculator
