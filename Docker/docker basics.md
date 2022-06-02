#### Docker installation
 * 1. Open the terminal on Ubuntu.
 * 2. Remove any Docker files that are running in the system, using the following command:
      `$ sudo apt-get remove docker docker-engine docker.io`
 * 3. Check if the system is up-to-date using the following command:
      `$ sudo apt-get update`
 * 4. Install Docker using the following command:
      `$ sudo apt install docker.io -y`
 * 5. Install all the dependency packages using the following command:
      `$ sudo snap install docker`
 * 6. Before testing Docker, check the version installed using the following command:
      `$ docker --version`
* We can also install docker using two simple commands
    `sudo apt-get update`
    `sudo apt install docker.io -y`

### Basic Commands
* 1) `docker  version` --> used to display the client and server versions of docker engine.
  * we will get the information like below.
            Client: Docker Engine - Community
            Version:           20.10.0
            API version:       1.41
            Go version:        go1.13.15
            Git commit:        7287ab3
            Built:             Tue Dec  8 18:54:00 2020
            OS/Arch:           linux/amd64
            Context:           default
            Experimental:      true

            Server: Docker Engine - Community
            Engine:
            Version:          20.10.0
            API version:      1.41 (minimum version 1.12)
            Go version:       go1.13.15
            Git commit:       eeddea2
            Built:            Tue Dec  8 18:58:04 2020
            OS/Arch:          linux/amd64
            Experimental:     true
            containerd:
            Version:          v1.4.3
            GitCommit:        269548fa27e0089a8b8278fc4fc781d7f65a939b
            runc:
            Version:          1.0.0-rc92
            GitCommit:        ff819c7e9184c13b7c2607fe6c30ae19403a7aff
            docker-init:
            Version:          0.19.0
            GitCommit:        de40ad0

* 2) `docker --help` --> to get the list of commands used in docker. 
* 3) `systemctl status docker` --> To check whether docker is running or not use the following command.
* 4) `systemctl start docker` ; `systemctl enable docker` --> to start and run docker. 
* 5) `systemctl enable --now docker` --> used to start and run docker at boot time.       
   After running this command you can find that docker uses dockerd and some other utilities to function.
* 6) `docker info` --> To show the total information about docker.
  If you get any error like 

  Server:
  ERROR: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get "http://%2Fvar%2Frun%2Fdocker.sock/v1.24/info": dial unix /var/run/docker.sock: connect: permission denied
  Use the following command to resolve the error.
  `sudo chmod 666 /var/run/docker.sock`
  You will get the information like containers information; how many are running, paused, stopped, how many images are there, server version, cgroup drivers, plugins, volumes, init version, swarm is active or not, default runtime(usually runc), kernel version, os, no of CPU's, architecture, total memory etc,
  name(if you install docker on ec2 instance it will be ec2 instance `private ipv4 address`)
  Docker root directory(`/var/lib/docker`). If we want we can change the root directory.
* 






















