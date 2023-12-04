CC  = nvcc
CCFLAGS = -arch=sm_70

INCLUDES  = -I$(OMPI_DIR)/include
LIBRARIES = -L$(OMPI_DIR)/lib -lmpi

cuda_staged_pp: cuda_staged_ping_pong.o
	$(CC) $(CCFLAGS) $(LIBRARIES) cuda_staged_ping_pong.o -o cuda_staged_pp

cuda_staged_ping_pong.o: cuda_staged_ping_pong.cu
	$(CC) $(CCFLAGS) $(INCLUDES) -c cuda_staged_ping_pong.cu

clean:
	rm -f cuda_staged_pp *.o

.PHONY: clean