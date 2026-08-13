# Cloud Infrastructure Components

## 1. Compute Resources

### Example
CPU Cores: 1
### Purpose
Compute resources handle the instructions and tasks performed by a computer. The CPU processes commands and allows programs to run.

### Importance in Cloud Computing
Compute power is needed to run websites, applications, databases, and other cloud services. More computing resources can help a system handle more tasks.

### KillerCoda Environment
The KillerCoda environment provides 1 CPU core. I used the nproc command to check the number of available CPU cores.
## 2. Storage Resources

### Example
Disk Capacity: 19 G
### Purpose
Storage resources keep files, programs, system files, and other information on the computer.
### Importance in Cloud Computing
Cloud systems need storage to keep application files and user data. Reliable storage also allows information to remain available when it is needed.

### KillerCoda Environment
The KillerCoda environment has a 19 G main disk. I checked the available storage using the df -h command.
## 3. Networking Resources

### Example
IP Addresses: 172.30.1.2 and 172.17.0.1
### Purpose
Networking allows computers and services to send and receive information.
### Importance in Cloud Computing
Networking allows users to connect to cloud applications and allows different cloud services to communicate with one another.
### KillerCoda Environment
My KillerCoda environment has the IP addresses 172.30.1.2 and 172.17.0.1. I used the hostname -I command to view the IP addresses.

## 4. Operating System

### Example
Operating System: Ubuntu 24.04.4 LTS

### Purpose
The operating system controls computer resources and provides the environment where programs and commands can run.
### Importance in Cloud Computing
An operating system provides the foundation for running applications and managing the resources of a cloud server.

### KillerCoda Environment
The KillerCoda environment uses Ubuntu 24.04.4 LTS. I identified the operating system using the cat /etc/os-release command.
