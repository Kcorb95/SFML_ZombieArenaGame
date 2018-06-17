CXX = g++
CXXFLAGS = -std=c++11
CXXLIBS = -lsfml-audio -lsfml-graphics -lsfml-window -lsfml-system

all: ZombieArena ZombieArenaDebug

ZombieArena: code/ZombieArena.o code/Player.o code/CreateBackground.o \
			 code/Zombie.o code/Pickup.o code/Bullet.o code/CreateHorde.o \
			 code/TextureHolder.o
	$(CXX) -O3 $? -o $@ $(CXXLIBS)

ZombieArenaDebug: code/ZombieArena.o code/Player.o code/CreateBackground.o \
			 code/Zombie.o code/Pickup.o code/Bullet.o code/CreateHorde.o \
			 code/TextureHolder.o
	$(CXX) -g $? -o $@ $(CXXLIBS)

code/%.o: %.cpp %.h
	$(CXX) $< -o $@

clean:
	rm ZombieArena code/*.o

