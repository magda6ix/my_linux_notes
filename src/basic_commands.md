# Linux Commands - Cheatsheet

Commonly used Linux commands presented in a nutshell.

# Table of Contents

1. [Files and Directories Basic Operations](#files-and-directories-basic-operations)
2. [Managing Processes](#managing-processes)
3. [System Monitoring](#system-monitoring)
4. [Basic Commands for Networking](#basic-commands-for-networking)
5. [Compression](#compression)
6. [File Permissions](#file-permissions)
7. [Text Files Processing](#text-files-processing)


## Files and Directories Basic Operations

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
> the second case will not work if one of the interminient directories doesn't exist (for example `dir1` or `dir2`). In that case, all you need to do is to add the `-p` argument to your command.:
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
cp -r src_dir/ dest_dir
```

Move (or rename) file:

```bash
mv old.txt new.txt
```

Move file to another directory:

```bash
mv file.txt /path/to/dir
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
> If you want to forcefully remove a file, just add `-f`:
>```bash
>rm -f file.txt
>```
> You'll not be asked to confirm your action

Remove a directory recursively:
```bash
rm -r directory
```

#

## Managing Processes

**Basic process management operations**

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

#

**Test the connectivity**

Test network connectivity to specific domain:

```bash
ping webpage.com
```

or IP address:

```bash
ping <ip_addr>
```
#

**Download files**

Download files using wget:

```bash
wget http://webpage.com/file.zip
```
Using curl:

```bash
curl -O http://webpage.com/file.zip
```

Few differences between `curl` and `wget` are described in the table below:

| Feature | `curl` | `wget` |
|--- |--- |--- |
| Purpose | data transfer, APIs and protocols | files download |
| Supported Protocols | HTTP, HTTPS, FTP, SMTP and more. | HTTP, HTTPS, FTP |
| Used in Scripting | Commonly used | Rarely used |
| Output | stdout by default | saves downloaded file to disk by default |


#

## Compression

**Tar archive**

Create a tar archive:

```bash
tar -cvf archive.tar directory
```

Extract a tar archive:
```bash
tar -xvf archive.tar
```

#

**Gzip**

Compress file:

```bash
gzip filename.txt
```

Decompress file:
```bash
gunzip file.txt.gz
```
#

**Zip**

Create zip archive: 
```bash
zip archive.zip file1 file2
```
Extract zip file:

```bash
zip archive.zip file1 file2
```

#

## File Permissions

**Basic commands for managing file permissions**

View file permissions:

```bash
ls -l filename.txt
```

Change file permissions:

```bash
chmod 755 filename.txt
```
or (add execute permissions, using `+x`):

```bash
chmod +x file.sh
```
File permissions can be set using numeric values or letters. Both methods control read (r), write (w), and execute (x) permissions for the owner, group, and others.

Change file owner:

```bash
chown user:group file.txt
```

#

## Text Files Processing

**Basic operations on `.txt` files**

Search for a phrase in file:

```bash
grep "phrase" file.txt
```

Display first few lines of a file:

```bash
head filename.txt
```

>The `head` command, by default, displays the first 10 lines of a file, but it can be customized by specifying the number of lines using the `-n` option. 
>For example: 
>```bash
>head -n 16 filename.txt
>``` 
>will display the first 16 lines.

Display last few lines of a file:

```bash
tail filename.txt
```
>The `tail` command, by default, displays the last 10 lines of a file. Similar to `head`, it can be customized by specifying the number of lines using the `-n` option


