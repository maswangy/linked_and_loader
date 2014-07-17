all:
	gcc -g -fPIC -c -o test.o test.c
	gcc -g -shared -Wl,-soname,libtest.so -o libtest.so test.o -lc
	gcc -g -I. -L. main.c -o main.exe -ltest 

tar:
	tar zcvf main.tar.gz main.c test.c test.h Makefile

clean:
	rm -f *.so *.o *.exe

.PHONY: all tar clean
