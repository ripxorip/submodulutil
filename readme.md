# sudmodutil

## What
A tool that can be used to ease working in projects with lots of submodules. It
acts as a _git wrapper_ so work can be performed on a super project level rather
than for each submodule. The utility shall be called **smu** which is short submoduleutil.

## Features
The utility shall be able to carry out the following commands
* **Git status**
* **Git add**
* **Git commit**
* **Git fetch**
* **Git push**

## Examples
In the following exmples we assume a super project consisting of 5 submodules named A->E.
Each submodule consists of 3 different files named Xa->Xc.

### **Git status**
`smu status`  
modified: Aa (submodule A)  
modified: Ba (submodule B)  
modified: Ba (submodule B)  

### **Git add**
`smu add Xx`  
Shall stage the change in file *Xx*.

### **Git commit**
`smu commit`  
Shall recursively create commits for all the staged changes in
respective submodule and super repo. This command shall accept the
same flags as the regular git commit command, especially the
_--amend_ flag.
