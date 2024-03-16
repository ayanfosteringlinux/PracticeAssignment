

s
![image](https://github.com/simranpopli05/Jenkins/assets/153719945/789a9ad6-ad0e-4278-a47b-558601b62276)


# Jenkins
Jenkins is an open-source automation server that facilitates the automation of several stages of the software development lifecycle, including application development, testing, and deployment. Operating within servlet containers like Apache Tomcat, the technology is server-based.Continuous delivery (CD) and integration (CI) pipelines can be created and managed with Jenkins.
![image](https://github.com/simranpopli05/Jenkins/assets/153719945/9a9169cc-a390-4d9a-8bdc-30aee3033e5b)

## Workflow of jenkins
Jenkins is a continuous integration/continuous delivery (CI/CD) tool that automates various stages of software development, such as building, testing, and deploying. It uses a concept of pipelines, which are defined using a Jenkinsfile, a text file that contains the definition of the pipeline as code.

 


   1 Developer Uploads Code to GitHub:
        Developers store their code on GitHub.

   2 Jenkins Takes Over:
        Jenkins is set up to watch for changes on GitHub.

   3 Build with Maven:
        When there's a code change, Jenkins uses Maven to build the code, turning it into a usable application.

  4  Automated Testing with Selenium:
        After building, Jenkins hands over the code to Selenium for automatic testing to catch any issues.

 5   Store Artifacts in Artifactory:
        If everything's okay, Jenkins stores the code (artifacts) in Artifactory, ready for use.

  5  Optional: Continuous Deployment:
        Jenkins can also deploy the code to where it needs to go automatically.
       
![image](https://github.com/simranpopli05/Jenkins/assets/153719945/5195aca8-b68b-4f2e-87d1-22b88a3f0bad)

## Advantages of jenkis
1 Saves Time :
        Jenkins helps do repetitive tasks automatically, saving time for developers.
       
  2  Finds Problems Early:
        It quickly spots issues in the code, so developers can fix them early.
       
  3  Works Well with Others:
        Jenkins easily connects with different tools that developers use.
       
 4  Grows with Your Project:
        It can handle bigger projects and more work as your team and code grow.
       
 5   Free and Helpful Community:
        Jenkins is free to use, and lots of people help each other use it better .
       
## why Jenkins and how it is better from ant?

Jenkins is like a traffic cop for software development, making sure everything runs smoothly. It helps coordinate tasks like building, testing, and deploying code.

Ant is a handy worker that focuses on building and organizing Java projects. It's like a specialized tool for specific construction tasks.

Jenkins manages the whole traffic flow of development tasks, while Ant is a worker bee dedicated to building Java projects.

![image](https://github.com/simranpopli05/Jenkins/assets/153719945/96e6b4c9-784e-44b1-98dd-3340da6af70a)

## Architecture of jenkins
   1 Jenkins Master:
   Boss of the operation, makes the plans.
   Controls and directs everything.
   Has a web interface for managing tasks.

  2 Jenkins Nodes (Slaves):
    Workers that do the heavy lifting.
    Follow the master's instructions.
     Can be on different computers for teamwork.
       
       
       
 ![image](https://github.com/simranpopli05/Jenkins/assets/153719945/89c94da5-137c-4b0c-8270-0287a4dec4d9)

### Plugins

Jenkins plugins are software extensions that add new features and functionality to Jenkins. They can be used to support various version control systems, programming languages, build tools, and other technologies. Plugins can also provide additional integrations with other tools, such as issue trackers, chat platforms, and cloud services.
       

## Installtion of Jenkins
1 Debian/Ubuntu

  2  Fedora

 3  Red Hat/Alma/Rocky


## Installation of Jenkins
### Linux
Jenkins installers are available for several Linux distributions.

- Debian/Ubuntu

- Fedora

- Red Hat/Alma/Rocky

## Prerequisites

Minimum hardware requirements:

- 256 MB of RAM

- 1 GB of drive space (although 10 GB is a recommended minimum if running Jenkins as a Docker container)

Recommended hardware configuration for a small team:

- 4 GB+ of RAM

- 50 GB+ of drive space

Software requirements:
- Java

  ##  Steps for installation of Jenkins

 steps which you have fallow to install jenkins.

## Step1 Install Java

```bash
sudo apt-get install openjdk-11-jdk
```

To check java version


```bash
java --version
```

## Step 2 Download Jenkins Repository key:
```
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
```
![image](https://github.com/simranpopli05/Jenkins/assets/153719945/037c0ee6-37f0-4bb2-b617-604d0244237f)



### Step 3 Add Jenkins Repository to APT Sources

```
bash
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null
```
# Step4 Update System
go to etc/apt/

```bash
sudo apt-get update
```


Ign:1 https://pkg.jenkins.io/debian-stable binary/ InRelease
Get:2 https://pkg.jenkins.io/debian-stable binary/ Release [2,044 B]                                                                                                          
Get:3 https://pkg.jenkins.io/debian-stable binary/ Release.gpg [833 B]                                                                                                        
Get:4 http://packages.microsoft.com/repos/code stable InRelease [3,589 B]                                                                                                      
Hit:5 http://in.archive.ubuntu.com/ubuntu jammy InRelease                                                                                                                    
Get:6 https://pkg.jenkins.io/debian-stable binary/ Packages [26.4 kB]                                                                                  
Get:7 http://in.archive.ubuntu.com/ubuntu jammy-updates InRelease [119 kB]                                                                                
Get:8 http://packages.microsoft.com/repos/code stable/main arm64 Packages [16.4 kB]                                                
Get:9 http://packages.microsoft.com/repos/code stable/main amd64 Packages [16.3 kB]                                                                                  
Get:10 http://packages.microsoft.com/repos/code stable/main armhf Packages [16.4 kB]                                                                                
Hit:11 http://in.archive.ubuntu.com/ubuntu jammy-backports InRelease                                                                                                          
Get:12 http://in.archive.ubuntu.com/ubuntu jammy-updates/main i386 Packages [570 kB]                                    
Get:13 http://in.archive.ubuntu.com/ubuntu jammy-updates/main amd64 Packages [1,377 kB]                                            
Get:14 http://in.archive.ubuntu.com/ubuntu jammy-updates/restricted amd64 Packages [1,431 kB]                                                              
Get:15 http://in.archive.ubuntu.com/ubuntu jammy-updates/restricted i386 Packages [34.8 kB]                                                                  
Get:16 http://repo.mysql.com/apt/ubuntu jammy InRelease [20.2 kB]                                                                                            
Get:17 https://dl.google.com/linux/chrome/deb stable InRelease [1,825 B]                          
Get:18 http://security.ubuntu.com/ubuntu jammy-security InRelease [110 kB]                      
Get:19 https://dl.google.com/linux/chrome/deb stable/main amd64 Packages [1,066 B]
Err:16 http://repo.mysql.com/apt/ubuntu jammy InRelease                                                                                                                        
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY B7B3B788A8D3785C
Reading package lists... Done                                                                                                                                                  
W: GPG error: http://repo.mysql.com/apt/ubuntu jammy InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY B7B3B788A8D3785C
E: The repository 'http://repo.mysql.com/apt/ubuntu jammy InRelease' is not signed.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.


## Step5 Install Jenkins

```
sudo apt-get install jenkins -y
```

Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libfuse2 libgnome-bg-4-1 libntfs-3g89
Use 'sudo apt autoremove' to remove them.
The following additional packages will be installed:
  net-tools
The following NEW packages will be installed:
  jenkins net-tools
0 upgraded, 2 newly installed, 0 to remove and 50 not upgraded.
Need to get 86.1 MB of archives.
After this operation, 87.4 MB of additional disk space will be used.
Get:2 http://in.archive.ubuntu.com/ubuntu jammy/main amd64 net-tools amd64 1.60+git20181103.0eebece-1ubuntu5 [204 kB]
Get:1 https://pkg.jenkins.io/debian-stable binary/ jenkins 2.440.1 [85.8 MB]      
Fetched 86.1 MB in 3min 3s (470 kB/s)                                                                                                                                          
Selecting previously unselected package net-tools.
(Reading database ... 273474 files and directories currently installed.)
Preparing to unpack .../net-tools_1.60+git20181103.0eebece-1ubuntu5_amd64.deb ...
Unpacking net-tools (1.60+git20181103.0eebece-1ubuntu5) ...
Selecting previously unselected package jenkins.
Preparing to unpack .../jenkins_2.440.1_all.deb ...
Unpacking jenkins (2.440.1) ...
Setting up net-tools (1.60+git20181103.0eebece-1ubuntu5) ...
Setting up jenkins (2.440.1) ...
Created symlink /etc/systemd/system/multi-user.target.wants/jenkins.service → /lib/systemd/system/jenkins.service.
Processing triggers for man-db (2.10.2-1) ...

 ### check Jenkins which jenkins

  ```bash
  which jenkins
  ```
     

## Step 6 Jenkins Status

```bash
systemctl status jenkins
```


![image](https://github.com/simranpopli05/Jenkins/assets/153719945/38221f91-06d8-4b06-aa1d-5e4a4a1347cf)


   NOW, Open a web browser.
    In the address bar, type http:localhost:8080 and press Enter.

Jenkins will prompt you for a username and password, which were created during the Jenkins installation. To retrieve the initial admin password 

![image](https://drive.google.com/file/d/1vnX8GDgufdHTxiTRvIlpiwe5TgJ_jDKn/view?usp=sharing)

![alt text](image.png)

![alt text](image.png)

![alt text](image.png)



[def]: a.
