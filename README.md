# DevOps-Linux

Introduction

Linux is an open-source OS that:

Manages hardware and runs applications

Enables networking

Powers servers, cloud platforms, and containers

Why DevOps needs Linux:

Most cloud servers (AWS, Azure, GCP) run Linux

Tools like Docker, Kubernetes, Ansible rely on Linux

Networking, security, and automation tasks run best on Linux

1. Linux Basics
Kernel → Core of Linux; communicates with hardware
Shell  → Command interpreter (bash, zsh)
Terminal → Interface to enter commands
Distros → Versions like Ubuntu, CentOS, Debian, Amazon Linux


Commands & Examples

uname -a     # Kernel and system info
whoami       # Current user

2. File System

Linux organizes data hierarchically:

/      → Root directory
/home  → User files
/etc   → Configuration files
/var   → Logs and variable data
/bin   → Essential binaries
/usr   → User programs & libraries
/tmp   → Temporary files


Commands

pwd          # Show current directory
ls -l        # List files with details
cd /path     # Change directory
mkdir test   # Create directory
rm file.txt  # Remove file
cp a b       # Copy file
mv a b       # Move/rename file


DevOps Use: Organizing project folders, deploying files, backup scripts

3. File Permissions

Each file has permissions: Read (r), Write (w), Execute (x)

Permissions apply to:

Owner (u)
Group (g)
Others (o)


Commands

ls -l                # View file permissions
chmod 755 file.sh    # Change permissions (rwxr-xr-x)
chown user:group f   # Change ownership


Example: Only owner can read/write, others read-only:

chmod 644 file.txt


DevOps Use: Secure scripts, limit access to production servers

4. Processes & Services

Linux runs background processes and services:

Commands

ps aux                  # List processes
top                     # Monitor processes
kill <PID>              # Kill process by ID
systemctl start nginx   # Start service
systemctl stop nginx    # Stop service
systemctl status nginx  # Check status


DevOps Use: Monitor services, manage deployments, kill stuck processes

5. Package Management

Install/update software using package managers:

Ubuntu/Debian (apt):

sudo apt update
sudo apt upgrade -y
sudo apt install nginx -y


CentOS/Amazon Linux (yum):

sudo yum update -y
sudo yum install nginx -y


DevOps Use: Install dependencies, automate CI/CD pipelines

6. Users & Groups

Linux is multi-user; permissions are group-controlled.

Commands

whoami                   # Show current user
id                       # Show user & groups
adduser devops           # Create user
passwd devops            # Set password
usermod -aG sudo devops  # Add to sudoers
groups                   # Show groups


DevOps Use: Secure production servers, automate tasks, manage teams

7. Environment Variables

Dynamic values that configure programs without hardcoding.

PATH    → directories for executables
HOME    → user's home directory
DB_HOST → custom database host


Commands

printenv             # List all variables
echo $VAR_NAME       # View specific variable
VAR_NAME=value       # Set for session
export VAR_NAME=value # Make available to child processes
unset VAR_NAME       # Remove variable


DevOps Use: Config management, secrets, CI/CD pipelines

8. Binary & Octal Representation

Binary (base 2): 0,1

Decimal 5 → Binary 101

Used in chmod: rwx = 111

Octal (base 8): 0–7

Decimal 64 → Octal 100

File permissions: chmod 755 file

DevOps Use: Permissions, low-level configs, scripting

9. Basic Linux Commands
Command	Usage	DevOps Use
mkdir	mkdir test	Create project folders
cp	cp a b	Backup files
mv	mv old new	Organize/rename deployments
rm	rm file	Clean old files
ls	ls -l	Validate deployments
pwd	pwd	Ensure correct directory
10. Programs, Binaries, and Shells
Programs → Execute tasks (editors, scripts)
Binaries → Compiled machine code (ls, cp)
Shells   → Command interpreter (bash, zsh)


DevOps Use: Automation, scripting, server management

11. Configuration Files

Store settings for apps/services:

/etc/nginx/nginx.conf
.env
config.yaml


DevOps Use: Separate config from code, enable automation, manage environments

12. Exercises / Practice

Bandit Game (OverTheWire): Practice Linux commands by completing Levels 1–20

Navigate files and directories (cd, ls)

View and edit files (cat, less, grep)

Manage permissions (chmod, chown)

Monitor processes (ps, top, kill)

Use scripting and text processing (awk, sed)

Repetition builds confidence — Linux is the foundation of all DevOps practices.
