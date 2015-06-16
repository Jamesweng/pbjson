
CXX=g++

CXXFLAGS=-Wall -g 

PBINC=../src/dependency/protobuf-2.6.1/include
PBLIB=../src/dependency/protobuf-2.6.1/lib/libprotobuf.a

INCS=-I./ -I../src -I${PBINC} -I../src/dependency/rapidjson-1.0.2/
LIBS=${PBLIB} -lpthread

%.o : %.cpp
	${CXX} -c ${CXXFLAGS} ${INCS} $< -o $@

%.o : %.cc
	${CXX} -c ${CCFLAGS} ${INCS} $< -o $@
	
CORE_OBJECTS := test.o test.pb.o ../src/pbjson.o

all: exe

exe:  ${CORE_OBJECTS}
	${CXX} -o pbjson_test ${CORE_OBJECTS} $(LIBS)
