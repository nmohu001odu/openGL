SRC_DIR = src
BUILD_DIR = build/debug
CC = clang++
SRC_FILES = $(wildcard $(SRC_DIR)/*.cpp)
OBJ_NAME = game
INCLUDE_PATHS = -Iinclude
LIBRARY_PATHS = -Llib -Llib/SDL2/SDL2 -Llib/GL/GL -Llib -Llib/include/ -Llib/SDL2/lib -Llib/GL/lib/GL -L/opt/homebrew/Cellar/glfw/3.4/include/GLFW
LIBDIRS = $(wildcard /lib/*)

INCLUDES = $(addprefix -I, $(LIBDIRS))


COMPILER_FLAGS = -std=c++11 -Wall -O0 -g -arch arm64
LINKER_FLAGS = -lsdl2 -framework OpenGL -lglew
all:
	$(CC) $(COMPILER_FLAGS) $(LINKER_FLAGS) $(INCLUDE_PATHS) $(LIBRARY_PATHS) $(SRC_FILES) -o $(BUILD_DIR)/$(OBJ_NAME)
clean:
	rm -r -f $(BUILD_DIR)/*