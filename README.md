# Programming in C Mini Projects
## 1. Create a project to demonstrate zombie process.
#### A zombie process or defunct process is a process that has completed execution (via the exit system call) but still has an entry in the process table. This occurs for the child processes, where the entry is still needed to allow the parent process to read its child's exit status. Once the exit status is read via the wait system call, the zombie's entry is removed from the process table and said to be "reaped". A child process always first becomes a zombie before being removed from the resource table.
![image](https://user-images.githubusercontent.com/86239697/153705648-c30fb89f-d219-44ee-ab2b-4f1f77412b28.png)
> Following is the C code to make a zombie process in a UNIX based Operating System:
```
#include <stdlib.h>
#include <sys/types.h>
#include <unistd.h>
int main (){
  pid_t child_pid;
  child_pid = fork ();
  if (child_pid > 0){
    sleep (10);
  }
  else {
    exit (0);
  }
  return 0;
}
```
## 2. Create a project to find sum of digits of a number until a single digit is occurred (without using recursion or iterative (loop) statements).
