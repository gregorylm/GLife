PREFIX = ../..
include ../make.common

check: x1 x2 t1 t2 t3 t4 t5 t6 t7 t8 

x1:
	$(CC) $(CFLAGS) xtest1.cpp  
	$(TEST_EXEC) > tmp
	$(COMPARE) test1x.ok tmp

x2:
	$(CC) $(CFLAGS) xtest2.cpp  
	$(TEST_EXEC) > tmp
	$(COMPARE) test2x.ok tmp

t1:
	$(CC) $(CFLAGS) test1.cpp
	$(TEST_EXEC) > tmp
	$(COMPARE) test1.ok tmp

t2:
	$(CC) $(CFLAGS) test2.cpp
	$(TEST_EXEC) > tmp
	$(COMPARE) test2.ok tmp

t3:
	$(CC) $(CFLAGS) test3.cpp
	$(TEST_EXEC) > tmp
	$(COMPARE) test3.ok tmp

t4:
	$(CC) $(CFLAGS) test4.cpp
	$(TEST_EXEC) > tmp
	$(COMPARE) test4.ok tmp

t5:
	$(CC) $(CFLAGS) test5.cpp
	$(TEST_EXEC) > tmp
	$(COMPARE) test5.ok tmp

t6:
	$(CC) $(CFLAGS) test6.cpp
	$(TEST_EXEC) > tmp
	$(COMPARE) test6.ok tmp

t7:
	$(CC) $(CFLAGS) test7.cpp
	$(TEST_EXEC) > tmp
	$(COMPARE) test7.ok tmp

t8:
	$(CC) $(CFLAGS) test8.cpp
	$(TEST_EXEC) > tmp
	$(COMPARE) test8.ok tmp
