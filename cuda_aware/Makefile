CC  = nvcc
CCFLAGS = -arch=sm_70

INCLUDES  = -I$(OMPI_DIR)/include
LIBRARIES = -L$(OMPI_DIR)/lib -lmpi

cuda_aware_pp: cuda_aware_ping_pong.o
	$(CC) $(CCFLAGS) $(LIBRARIES) cuda_aware_ping_pong.o -o cuda_aware_pp

cuda_aware_ping_pong.o: cuda_aware_ping_pong.cu
	$(CC) $(CCFLAGS) $(INCLUDES) -c cuda_aware_ping_pong.cu

clean:
	rm -f cuda_aware_pp *.o

.PHONY: clean