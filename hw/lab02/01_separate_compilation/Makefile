CXX = g++
CXXFLAGS = -Wall -Wextra -std=c++17

all: calculator

obj/%.o: %.cpp | obj
 $(CXX) $(CXXFLAGS) -c $< -o $@

obj:
 mkdir -p obj

calculator: obj/main.o obj/calc.o
 $(CXX) $(CXXFLAGS) $^ -o $@

clean:
 rm -rf obj calculator

.PHONY: all clean
