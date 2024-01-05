# MushclientSimpleStepper
```
This plugin allows loading paths from an external master file and executing commands step by step.
 Use '- [filename]' to load a path file. Each path should be in the format 'pathName=command1;command2;...'.
 Use '.' to execute the next command in the loaded path.
 Use '..' to go backwards one step. This will only work if there is a reverse command specified in the plugin code.
 Use 'stepperhelp' to print this help.
 
Edit the plugin and reload to modify:
 1. masterFilePath: the path to your master file containing all of your path data.
    NOTE: the slashed go forward in the masterFilePath (ex: C:/whatever/)/
 2. reverseCommands: add reverse commands as needed.
 
The master file can contain several lines. Example line:
 test=n;w;s;e;kill guard;smile,nod;cheer;bow

To load this path from the master file, you would use the command: - test
- test
Current path set to: test
Total steps: 8, First step: n

Now to take a step: .
. 
Executing command: n
n
Steps left: 7, Next step: w
Maybe you should look for another exit.

Now to step backward:
..
Going back one step: s
s
Maybe you should look for another exit.

Note: if your path has commas like smile,nod then both commands will be executed at once
.
Executing command: smile
smile
Executing command: nod
nod
Steps left: 2, Next step: cheer
You smile happily.
You nod solemnly.
```
