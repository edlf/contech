PROJECT = libct_event.a
OBJECTS = ct_event.o
CFLAGS  = -O2 -g 
HEADERS = ct_event.h ct_event_st.h

all: $(PROJECT)

.cpp.o:
	g++ -c $(CFLAGS) $<

$(PROJECT): $(OBJECTS)
	ar rc $(PROJECT) $(OBJECTS)

install: all
	mkdir -p $(CONTECH_LLVM_HOME)/lib
	mkdir -p $(LLVM_SRC)/include
	cp $(PROJECT) $(CONTECH_LLVM_HOME)/lib
	cp $(HEADERS) $(LLVM_SRC)/include

clean:
	rm $(PROJECT) $(OBJECTS)
