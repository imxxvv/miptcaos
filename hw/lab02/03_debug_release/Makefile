CXX = g++
CXXFLAGS_Common = -Wall -Wextra -std=c++17

ifeq ($(MODE),debug)
    CXXFLAGS = $(CXXFLAGS_Common) -g -O0
else
    CXXFLAGS = $(CXXFLAGS_Common) -O3
endif

SRCS = $(wildcard *.cpp)
OBJS = $(patsubst %.cpp, obj/%.o, $(SRCS))
DEPS = $(OBJS:.o=.d)

all: calculator

calculator: $(OBJS)
 $(CXX) $(CXXFLAGS) $^ -o $@

obj/%.o: %.cpp | obj
 $(CXX) $(CXXFLAGS) -c $< -o $@

obj:
 mkdir -p obj

-include $(DEPS)

clean:
 rm -rf obj calculator

.PHONY: all clean
