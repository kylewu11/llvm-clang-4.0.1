Fix two errors in compliler-rt
1. #include <sys/ustat.h>  missing
a. remove the included header in the line 157,
b. remove its usage in the line 250 which contains this code:
unsigned struct_ustat_sz = sizeof(struct ustat);

2. Fix sanitizer build against latest glibc
follow the solution in https://reviews.llvm.org/D35246
