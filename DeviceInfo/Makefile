CXX      := g++
CXXFLAGS := 
LIBS     := -lOpenCL

SRCDIR   := .
INCL_DIR := 

TARGET = ./clDeviceQuery

SRCS := $(wildcard $(INCL_DIR)/*.cpp)
SRCS += $(wildcard $(SRCDIR)/*.cpp)
OBJS := $(SRCS:.cpp=.o)

all: clean $(OBJS)
	$(CXX) $(CXXFLAGS) -o $(TARGET) $(OBJS) $(LIBS)

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -o $@ -c $<

run: all
	@./$(TARGET)

clean:
	rm -fr *.o $(INCL_DIR)/*.o