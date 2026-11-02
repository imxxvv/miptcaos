
CXX = g++
CXXFLAGS = -Wall -Wextra -std=c++17

TARGET = calculator
OBJ_DIR = obj
OBJECTS = $(OBJ_DIR)/main.o $(OBJ_DIR)/calc.o

.PHONY: all clean

all: $(TARGET)

$(TARGET): $(OBJECTS)
	$(CXX) $(CXXFLAGS) -o $@ $^

$(OBJ_DIR)/%.o: %.cpp calc.h
	mkdir -p $(OBJ_DIR)
	$(CXX) $(CXXFLAGS) -c $< -o $@

clean:
	rm -rf $(OBJ_DIR) $(TARGET)
