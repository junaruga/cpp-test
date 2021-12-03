# Follow the coding style written in the official GNU make document.
# https://www.gnu.org/software/make/manual/make.html
# Use C++ mainly, and use C as partly.
CXX = g++
CC = gcc
# CFLAGS: For C only.
# CXXFLAGS: For C++ only.
# CPPFLAGS: The CPP means "C PreProcessor". For both C and C++.
# https://stackoverflow.com/questions/495598/
CXXFLAGS = -g
CFLAGS = $(CXXFLAGS)
CPPFLAGS =
INCLUDES =
OBJS =
EXE = hello
LIBS =

.cpp.o :
	$(CXX) -c $(CXXFLAGS) $(CPPFLAGS) $(INCLUDES) $< -o $@

.c.o :
	$(CC) -c $(CFLAGS) $(CPPFLAGS) $(INCLUDES) $< -o $@

all : $(EXE)
.PHONY : all

$(EXE) : $(OBJS) main.o
	$(CXX) $(CXXFLAGS) $^ -o $@ $(LIBS)

clean :
	rm -f *.o $(EXE)
.PHONY : clean

test : all
	echo "Run the test"
.PHONY : test
