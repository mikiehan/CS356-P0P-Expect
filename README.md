## Installation
- Ubuntu
```
sudo apt-get install expect
```
- MacOS with Homebrew
```
brew install expect
```
- UTCS Machine
  - Download the binary file we provide
  - Unzip it wiht ```tar -xf expect.tar```
  - exec this command **once** ```echo 'export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:./' >> ~/.bashrc```
  - logout and re-login UTCS machine
  - try to execute ```./expect``` if you can see like "expect1.1>". It means you could run expect now. Type exit and then enter to exit.

## Testing script with expect
When we grade your assignment, we will run several **expect** script to do auto-grading. We will give you three script for self testing.
- Download the testing script
- Extract files with ```tar -xf script.tar```
- Make sure your client, server, testing script and expect (if you are in UTCS machine) are in same directory
- Run Server (Terminal 1)
  - If you use 'apt-get' or 'brew' version:  ```expect ./server.exp [port]```
  - If you use binary file we provide: ```./expect ./server.exp [port]```
  - Server will be closed after 30s.
- Run Client (Terminal 2)
  - If you use 'apt-get' pr 'brew' version: ```expect ./naive.exp [hostname] [port]```
  - If you use binary file: ```./expect ./naive.exp [hostname] [port]```
  - We also provide a longer input file call *Dostoyevsky.exp*. You could use it to test client too.
