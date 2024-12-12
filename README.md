Fork ();

ALGORITHM:

Step 1: Start the program.

Step 2: Declare the variables pid and child id.

Step 3: Get the child id value using system call fork().

Step 4: If child id value is greater than zero then print as "i am in the parent process".

Step 5: If child id!=0 then using getpid() system call get the process id.

Step 6: Print "i am in the parent process" and print the process id.

Step 7: If child id!=0 then using getppid() system call get the parent process id..

Step 8: Print "i am in the parent process" and print the parent process id.

Step 9: Else If child id value is less than zero then print as "i am in the child process".

Step 10: If child id!=0 then using getpid() system call get the process id.

Step 11: Print "i am in the child process" and print the process id.

Step 12: If child id!=0 then using getppid() system call get the parent process id

Step 13: Print "i am in the child process" and print the parent process id.

Step 14: Stop the program.
code 
SOURCE code:
#include<stdio.h>
#include <unistd.h>
#include<sys/types.h>
int main()
{
int id,childid;
id=getpid();
if((childid=fork())>0)
{
printf("\n i am in the parent process %d",id);
printf("\n i am in the parent process %d",getpid());
printf("\n i am in the parent process %d\n",getppid());
}
else
{
printf("\n i am in child process %d",id);
printf("\n i am in the child process %d",getpid());
printf("\n i am in the child process %d".getppid());
}
}
OUTPUT:
fork.c
cc fork.c
./a.out
i am in child process 3766
i am in the child process 3766
i am in the child process 3765
i am in the parent process 3765
i am in the parent process 3765
i am in the parent process 3680
