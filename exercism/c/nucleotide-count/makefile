CFLAGS = -std=c99
CFLAGS += -Wall
CFLAGS += -Wextra
CFLAGS += -pedantic
CFLAGS += -Werror

test: tests.out
	@./tests.out

clean:
	rm -f *.o *.out

tests.out: src/nucleotide_count.c src/nucleotide_count.h test/test_nucleotide_count.c 
	@echo Compiling $@
	@cc $(CFLAGS) src/nucleotide_count.c test/vendor/unity.c test/test_nucleotide_count.c -o tests.out
