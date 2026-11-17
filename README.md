# 2401MC50_Yashwanth_Varma_LABEXAM


NAME: K. Yashwanth Varma
ROLL NUMBER: 2401MC50
SLOT: 4pm-6pm




Question 2: Priority Scheduling without aging


1)In proc.h we defined priority in struct.
2)In proc.c in allocproc we initialized variables and in scheduler() function given code for priority based scheduling algo
3) In syscall.h we defined this #define SYS_set_priority 24
4) In syscall.c also we defined them for user space like extern int sys_set_priority(void);
And [SYS_set_priority] sys_set_priority,
5) In user.h and usys.S we added these calls int set_priority(int, int);
And SYSCALL(set_priority) respectively for user to function schedtest.c to interact with theme directly. 


These are the major changes,( in Make File uprogs we added schedtest.c/)


Question 1: Page Protection 


1)Implemented int mprotect(void *addr, int len) and int munprotect(void *addr, int len)
in vm.c and helper function is defined in defs.h as eros are coming when I implemented in vm.c itself
2) In syscall.h which acts as interface between user and kernel we defined both #define SYS_mprotect 22
#define SYS_munprotect 23
3) In syscall.c we defined [SYS_mprotect] sys_mprotect,
[SYS_munprotect] sys_munprotect,
And extern int sys_mprotect(void);
extern int sys_munprotect(void);


5) Finally made prottest.c which is the main user function, took one aligned page using sbrk(4096) and made further test of protections throught it.


These are the major changes (in Make File uprogs we added last prottest.c/)
