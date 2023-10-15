# Day 7 Task: Understanding package manager and systemctl

### What is a package manager in Linux?

A package manager in Linux is a software tool that automates the process of installing, upgrading, configuring, and removing computer programs. It typically handles the installation of software from pre-compiled packages, which are files that contain the program's code, data, and instructions.

### What is a package?

A package markdown is a file that provides detailed information about a software package. It is typically written in Markdown, a lightweight markup language that is easy to read and write. Package markdowns are commonly used in software development to document the features, usage, and installation process of a package.

Here is an example of a package markdown:

`Package Name`

A brief description of the package.

`Installation`

To install the package, run the following command:

### Different kinds of package managers

- **APT (Advanced Package Tool)**: APT is the default package manager for Debian-based Linux distributions, such as Ubuntu. It provides a command-line interface for managing packages and supports automated updates.

- **YUM (Yellowdog Updater, Modified)**: YUM is a package manager for RPM-based Linux distributions, such as CentOS and Fedora. It provides a command-line interface for managing packages and supports automated updates.

- **DNF (Dandified YUM)**: DNF is an improved version of YUM, which is the default package manager for Fedora 22 and later. It offers better dependency resolution and supports parallel downloads.

- **Pacman**: Pacman is the default package manager for Arch Linux and its derivatives. It provides a command-line interface for managing packages and supports automated updates.

## Tasks: 1. You have to install docker and jenkins in your system from your terminal using package managers.

For Ubuntu

- Install Docker
  1. Open the terminal on Ubuntu.
  2. Remove any docker file that are running in the system, using the following command:
     sudo apt-get remove docker docker-engine docker.io

Check if the system is up-to-date using the following command: sudo apt-get update

1. Install Docker using the following command: sudo apt install docker.io
2. Install all the dependency packages using the following command: sudo snap install docker
3. Before testing Docker, check the version installed using the following command: docker --version

For Ubuntu: Install Jenkins

Step 1: Install Java
Jenkins requires the Java Runtime Environment (JRE).

1. Check if you already have java installed on your Ubuntu system: java --version
2. Depending on which Java version you want to install, Java 8 or 11, run one of the following commands:

To install OpenJDK 8, run: sudo apt install openjdk-8-jdk -y

To install OpenJDK 11, run: sudo apt install openjdk-11-jdk -y

sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
 https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
 https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
 /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins

## Difference between systemctl and service

The systemctl command interacts with the SystemD service manager to manage the services. In Service command, it manages the services by interacting with the SystemD process instead of running the init script.

To start, stop, and restart the service, we can run the respective commands with systemctl:

1. To start jenkins service Syntax : systemctl start jenkins
2. To stop jenkins service Syntax: systemctl stop jenkins
3. To check jenkins status Syntax: systemctl status jenkins
4. To enable jenkins service Syntax: systemctl enable jenkins

To start, stop, and restart the service, we can run the respective commands with service:

1. To start jenkins service Syntax : service jenkins start
2. To stop jenkins service Syntax: service jenkins stop
3. To check jenkins status Syntax: service jenkins status
4. To enable jenkins service Syntax: service jenkins enable
