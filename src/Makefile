
CXX=g++

CXXFLAGS=-Wall -g 

PBINC=./dependency/protobuf-2.6.1/include
PBLIB=./dependency/protobuf-2.6.1/lib/libprotobuf.a

INCS=-I./ -I${PBINC} -I./dependency/rapidjson-1.0.2/
LIBS=${PBLIB} -lpthread

%.o : %.cpp
	${CXX} -c ${CXXFLAGS} ${INCS} $< -o $@

%.o : %.cc
	${CXX} -c ${CCFLAGS} ${INCS} $< -o $@
	
CORE_OBJECTS := pbjson.o

all: libpbjson.a

libpbjson.a:  ${CORE_OBJECTS}
	ar -rcs $@ $^

clean:
	rm libpbjson.a *.o
