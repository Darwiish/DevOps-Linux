# Linux foundation
---
## Introduction
***

* Linux is an open-source operating system that:

* Manages hardware and runs applications

* Enables networking

* Powers servers, cloud platforms, and containers

* Why DevOps Needs Linux

* Most cloud servers (AWS, Azure, GCP) run Linux

* Tools like Docker, Kubernetes, Ansible rely on Linux

* Networking, security, and automation tasks run best on Linux
___

### 1. Linux Basics

Kernel → Core of Linux; communicates with hardware

Shell → Command interpreter (bash, zsh)

Terminal → Interface to enter commands

Distributions (Distros) → Ubuntu, CentOS, Debian, Amazon Linux

## Commands & Examples
```markdown
uname -a     # Kernel and system info
whoami      # Current user
```

### 2. File System Structure

Linux organizes data hierarchically:

/ → Root directory

/home → User files

/etc → Configuration files

/var → Logs and variable data

/bin → Essential binaries

/usr → User programs & libraries

/tmp → Temporary files

## Commands
```markdown
pwd          # Show current directory
ls -l        # List files with details
cd /path     # Change directory
mkdir test   # Create directory
rm file.txt  # Remove file
cp a b       # Copy file
mv a b       # Move/rename file
```

DevOps Use:
Organizing project folders, deploying files, backup scripts

### 3. File Permissions

Each file has permissions:

Read (r)

Write (w)

Execute (x)

Permissions apply to:

Owner (u)

Group (g)

Others (o)

## Commands
```markdown
ls -l                 # View file permissions
chmod 755 file.sh     # Change permissions (rwxr-xr-x)
chown user:group f    # Change ownership
```
## Example
Only owner can read/write, others read-only:
```markdown
chmod 644 file.txt
```
DevOps Use:
Secure scripts, limit access to production servers

### 4. Processes & Services
Linux runs background processes and services.
## Commands
```markdown
ps aux                  # List processes
top                     # Monitor processes
kill <PID>              # Kill process by ID
systemctl start nginx   # Start service
systemctl stop nginx    # Stop service
systemctl status nginx  # Check status
```
DevOps Use:
Monitor services, manage deployments, kill stuck processes

### 5. Package Management
Install and update software using package managers.
## Ubuntu / Debian (apt)
```markdown
sudo apt update
sudo apt upgrade -y
sudo apt install nginx -y
```
## CentOS / Amazon Linux (yum)
```markdown
sudo yum update -y
sudo yum install nginx -y
```

DevOps Use:
Install dependencies, automate CI/CD pipelines

### 6. Users & Groups

## Linux is multi-user; permissions are group-controlled.
Commands
```markdown
whoami                   # Show current user
id                       # Show user & groups
adduser devops           # Create user
passwd devops            # Set password
usermod -aG sudo devops  # Add to sudoers
groups                   # Show groups
```

DevOps Use:
Secure production servers, automate tasks, manage teams

### 7. Environment Variables

Dynamic values that configure programs without hardcoding.

Common variables:

PATH → Executable locations

HOME → User home directory

DB_HOST → Custom database host
## Commands
```markdown
printenv                 # List all variables
echo $VAR_NAME           # View variable
VAR_NAME=value           # Set for session
export VAR_NAME=value    # Available to child processes
unset VAR_NAME           # Remove variable
```

DevOps Use:
Config management, secrets, CI/CD pipelines

### 8. Binary & Octal Representation
Binary (Base 2)

Uses 0 and 1

Decimal 5 → Binary 101

Used in permissions: rwx = 111

Octal (Base 8)

Values 0–7

Decimal 64 → Octal 100

## Example:
```markdown
chmod 755 file.sh
```
DevOps Use:
Permissions, low-level configs, scripting

### 9. Basic Linux Commands
Command	Usage	DevOps Use
mkdir	mkdir test	Create project folders
cp	cp a b	Backup files
mv	mv old new	Rename deployments
rm	rm file	Clean old files
ls	ls -l	Validate deployments
pwd	pwd	Ensure correct directory

### 10. Programs, Binaries & Shells

Programs → Execute tasks (editors, scripts)

Binaries → Compiled machine code (ls, cp)

Shells → Command interpreters (bash, zsh)

DevOps Use:
Automation, scripting, server management

### 11. Configuration Files

Store settings for applications and services:

/etc/nginx/nginx.conf

.env

config.yaml

DevOps Use:
Separate config from code, enable automation, manage environments

### 12. Exercises / Practice
Recommended Practice

Bandit Game (OverTheWire) – Levels 1–20

Practice Topics

File navigation (cd, ls)

File viewing (cat, less, grep)

Permissions (chmod, chown)

Process monitoring (ps, top, kill)

Text processing (awk, sed)

Repetition builds confidence — Linux is the foundation of all DevOps practices.
