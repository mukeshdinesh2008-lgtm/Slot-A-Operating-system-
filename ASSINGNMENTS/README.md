# CSA04 Assignment 1 (CO1) - Smart Hospital Operating-System Design

Name: ____________   Register number: ____________

- OS: Ubuntu 24.04.5 LTS (kernel 6.18), 1 CPU core VM
- Compiler: gcc 13.3.0
- Compile: gcc -std=c11 -Wall -Wextra -pthread -o <name> <name>.c
- Tracing: strace 6.8

| Folder | Run | Result |
|---|---|---|
| Task05 | gcc ... rd.c -o rd; strace -e trace=openat,read,write,close ./rd | 10,000 fgetc() calls -> 4 read() calls |
| Task06 | gcc ... copy.c -o copy; ./copy; strace -c ./copy | 10001 / 21 / 4 read() calls (matches expected) |
| Task07 | gcc ... shell.c -o shell; ./shell; ./shell_variant > variant_out.txt | Matches expected; duplicate lines explained in report |
| Task10 | gcc ... -pthread spawn.c / spawn2.c / mem.c / bigcopy.c | 1000 fork ~48 ms vs 1000 threads ~8.7 ms |

Tasks 1-4, 8, 9, 11, 12 are design/evaluation sections in the report.
