# k380-fn-lock-for-windows
 Lock Fn keys on K380 (for windows)

## Goal
This program locks the fn key for the Logitech K380 bluetooth keyboard on Windows. 
Having the F1-F12 without pressing the Fn key is nice for developers.

I wanted a simple way to do the same as the Logitech Options/Options+ softwares WITHOUT their continuously running processes.

## How to use
Running `setFnKeys.exe` will lock Fn key till next reboot.  
Revert with `setMediaKeys.exe` to unlock and restore media keys.

## How to build
- prerequisite : install mingw
- build setFnKeys.exe with :   
    `gcc main.c -o dist/setFnKeys.exe -I hidapi/include -L hidapi/x86 -lhidapi`
- build setMediaKeys.exe with :   
    `gcc main.c -D setMediaKeys -o dist/setMediaKeys.exe -I hidapi/include -L hidapi/x86 -lhidapi`

# Inspiration
code from : https://github.com/keighrim/k810fn/blob/master/win/k810fn/k810fnCLI.cpp   
values from : https://github.com/jergusg/k380-function-keys-conf/blob/master/k380_conf.c
