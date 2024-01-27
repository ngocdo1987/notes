Run C++ code from NodeJS

// myCFile.c
#include <stdio.h>

int main(void){

    // Processor-intensive computations
    int x = 1+2+3;

    // Send to node via standard output
    printf("%d", x);

    // Terminate the process
    return 0;
}

Compile:
gcc -o myExecutable myCFile.c

And use child_process like this
// File myNodeFile.js
const { exec } = require("child_process");
exec("./myExecutable", (error, stdout, stderr) => console.log(stdout));
