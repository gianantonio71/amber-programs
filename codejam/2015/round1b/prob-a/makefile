RTDIR=../../../../../amber-runtime

solve: generated.cpp generated.h
	g++ -I. -I$(RTDIR) -O3 -DNDEBUG generated.cpp $(RTDIR)/*.cpp -o solve

solve-dbg: generated.cpp generated.h
	g++ -I. -I$(RTDIR) -O3 generated.cpp $(RTDIR)/*.cpp -o solve-dbg

solve-lldbg: generated.cpp generated.h
	g++ -ggdb -I. -I$(RTDIR) generated.cpp $(RTDIR)/*.cpp -o solve-lldbg

generated.cpp generated.h: main.ar
	amberc prj.txt

clean:
	rm -f solve solve-dbg solve-lldbg generated.cpp generated.h core
