# Linux Commands - Cheatsheet

Commonly used Linux commands presented in a nutshell.

## Files and directories basic operations

**Commands to list files and directories**

List files and directories:

```bash
ls
```
List files and directories with detailed information:
```bash
ls -l
```
List all files including hidden ones:
```bash
ls -a
```

#

**Commands to change the directory**

Change location to a specific directory:

```bash
cd /path/to/directory
```

Go to home directory:

```bash
cd ~
```

Move up one directory:


```bash
cd ..
```


> If you want to move up more than one directory at once, you can simply type:
> ```bash
>cd ../../..
>```

#
**Commands to create new file or directory**

Create new text file:
```bash
touch filename.txt
```

Create new directory:

```bash
mkdir your_new_dir
```

or 

```bash
mkdir path/to/dir1/dir2/your_new_dir
```
>NOTE: 
> the second case will not work if one of the interminient directories doesn't exist (for example "dir1" or "dir2"). In that case, all you need to do is to add the *-p* argument to your command.:
>```bash
>mkdir -p path/to/dir1/dir2/your_new_dir
>```
> If all the directories in the path already exist, adding this argument will **not** return an error

#

**Commands to copy and/or (re)move files**

Copy a file:

```bash
cp src.txt dest.txt
```

Copy a directory recursively (with all its contents):

```bash
cp -r src_dir/ dest_dir/
```

Move (or rename) file:

```bash
mv old.txt new.txt
```

Move file to another directory:

```bash
mv file.txt /path/to/dir/
```

>NOTE: 
> If you want to move the file and change its name in one step, simply type in
>```bash
>mv old.txt /path/to/dir/new.txt
>```

Remove a file:
```bash
rm file.txt
```

>NOTE: 
> If you want to forcefully remove a file, just add *-f*:
>```bash
>rm -f file.txt
>```
> You'll not be asked to confirm your action

Remove a directory recursively:
```bash
rm -r directory/
```

#

## Managing processes

**View running processes**

Viev all running processes:

```bash
ps aux
```

View processes interactively:

```bash
top
```

Find process by name:

```bash
pgrep process_name
```

#

**Kill processes**


Kill a process by Process ID:

```bash
kill <PID>
```

Force kill a process:
```bash
kill -9 <PID>
```

Kill process by name:

```bash
pkill process_name
```
#

## System Monitoring

**Commands for system monitoring**

Show disk usage in a readable format:

```bash
df -h
```

Show the size of directories/files in the current directory:

```bash
du -sh *
```

Display memory usage:

```bash
free -h 
```

Display the Linux kernel version:

```bash
uname -r  
```

Display uptime:

```bash
uptime  
```

Uptime is a metric that shows how long the system has been running
#

## Basic commands for networking

**Network interfaces**

Check IP addresses of all interfaces:

```bash
ip addr  
```

or (older):

```bash
ifconfig
```


