CC = mpicc

pp: ping_pong.o
	$(CC) ping_pong.o -o pp

ping_pong.o: ping_pong.c
	$(CC) -c ping_pong.c

clean:
	rm -f pp *.o

.PHONY: clean