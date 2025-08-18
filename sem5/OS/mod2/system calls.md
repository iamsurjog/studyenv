- Programming interface to the services provided by OS
- typically written in high level language (C++ or C)
- accessed with API calls rather than direct system call use
# Methods to pass parameters:
- Simplest: pass the parameters in registers
- Parameters stored in block and the address of the block is passed as parameter
- Parameter is pushed into stack and the os could pop them
# Types of System Calls
## Process Control
- End, Abort
- Load, execute
- Create/terminate Process
- Get/set process attr
- wait for time
- wait event, signal event
- allocate and free memory
## File management
Create/Delete/open/close/read/write/move files
get/set file attributes
## Device management
- request/release device
- read write reposition
- get/set device attributes
- logically attach/detach devices
## Information maintenance
- get/set datetime
- get/set system data
- get/set process, file or device attribute
## Communications
- create, delete communication connection
- send receive messages
- transfer status information
- attach and detach remote devices
