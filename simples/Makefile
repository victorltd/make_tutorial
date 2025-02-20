simples: simples.o
	gcc simples.o -o simples

simples.o: simples.c
	gcc -c simples.c -o simples.o

simples.c:
	echo "int main(){return 0;}" > simples.c

clean:
	rm -f simples
	rm -f simples.o
	rm -f simples.c