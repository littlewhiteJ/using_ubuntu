## Run program without a continuous net connect

there is a problem when we train model on server

we can not cut the net connection when we leave.

such as taking the laptop to classroom

when we are walking on the street

it is hard to keep the net connect

and the ssh may be stop

and our program may be stopped

so sad...

so we use a tool named as screen

- start the screen
```
  screen
```
- run the program
- use 'ctrl+A' and 'ctrl+D'

then the process is detached
it is running but you can 

**disconnect and shut it down are ok too**
- come back
```
  screen -ls
```
list the detached process

- take the control again
```
  screen -r [pnum]
```
