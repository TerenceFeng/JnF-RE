RELEASE		= -w -std=c++14 -O2
DEBUG		= -std=c++14 -g
MODELS		= Material.cpp
UTILITIES	= sampler.cpp
TARGET		= renderer

default: clean release

test: clean $(TARGET)
	time ./$(TARGET)
	open result.ppm

release:
	g++ main.cpp $(MODELS) $(UTILITIES) $(RELEASE) -o $(TARGET)

debug: clean_debug
	g++ main.cpp $(MODELS) $(UTILITIES) $(DEBUG) -o debug

clean:
	rm -f renderer

clean_debug:
	rm -f debug
