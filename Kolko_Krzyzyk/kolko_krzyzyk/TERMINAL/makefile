#
#  To sa opcje dla kompilacji
#
CXXFLAGS=-g -Iinc -Wall -pedantic -std=c++11

TRGDIR=/tmp/kolko

__start__: ./kolko
	./kolko

./kolko: obj obj/main.o # obj/scal.o 
                        
	g++ -Wall -pedantic -std=c++11 -o ./kolko obj/main.o # obj/scal.o 

obj:
	mkdir -p obj

obj/main.o: src/main.cpp #inc/scal.hh 
        
	g++ -c ${CXXFLAGS} -o obj/main.o src/main.cpp

#obj/scal.o: inc/scal.hh src/scal.cpp
#	g++ -c ${CXXFLAGS} -o obj/scal.o src/scal.cpp

clean:
	rm -f obj/*.o ./kolko