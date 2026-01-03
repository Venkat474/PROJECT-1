# 🌟“END-TO-END DEVOPS PROJECT USING GITHUB :octocat: , MAVEN, JENKINS, AND TOMCAT SERVER”🌟
![Project Image](PHOTOS/Project1.PNG)

- 👨‍💻 Developer writes code on local machine
- 📤 Code is committed and pushed to GitHub using Git
- 🔄 Jenkins pulls the latest code from GitHub repository
- 🛠️ Jenkins triggers Maven to build the project
- 📦 Maven generates the WAR file (build artifact)
- 🚀 Jenkins deploys the WAR file to Apache Tomcat
- 🌐 Application is live and accessible from Tomcat server
## 🔹 1️⃣  INSTALL AND CONFIGURE JENKINS 🔹
**` Go to Aws `**
<br> 👉 EC2 ➡️ Launch Instance ➡️ Name = [JENKINS-SERVER] ➡️ AMI=Amazon Linux(QuickStart) ➡️ Amazon.Linux 2 AMI(HVM)-Kernel 5.10 , SSD Volume Type (Free Tier Eligible) ➡️ Architecture = 64-bit(x86) ➡️ Instance type = t2.micro(Free Tier Eligible) ➡️ Key pair = Createnewone ➡️ Network Settings = Firewall = create security group = ✔️ Allow SSH traffic from 0.0.0.0/0 ➡️ Configure storage = 1x8 GiB gp2 Root Volume = Launch Instance = copy public IPV4 address
<br> **` Go to MobaXtrem `** *[ is a Windows tool that lets you connect to Linux servers using SSH and also provides a built-in terminal and file transfer in one application. ]*
<br> 👉 Session ➡️ SSH ➡️ Remote host (Paste here IPV4) ➡️ ✔️specify username = ec2-user , Port 22 
<br> Advanced SSH Settings = ✔️ use private key = ______(Provide private key which is in downloads) ➡️ ✔️x11 = Forwarding ➡️ ✔️Compression ➡️ Remote environment = interactive shell ➡️ SSH-browser-type = SFTP protocol = OK 
<br> **` Go to Terminal `**
<br> 👉[ec2-user@ip-172-31-47-91 ~]$ sudo su 
<br> 👉[root@ip-172-31-47-91 ec2-user]# cd ~
<br> 🔗 https://www.jenkins.io/doc/tutorials/tutorial-for-installing-jenkins-on-AWS/ (for reference use this link)
- Updates all installed packages to the latest version. It may not remove old packages.
<br> 👉`[root@ip-172-31-47-91 ~]# sudo yum update -y `
- This is used to add the Jenkins repo to our system
<br> 👉`[root@ip-172-31-47-91 ~]# sudo wget -O /etc/yum.repos.d/jenkins.repo \  https://pkg.jenkins.io/redhat-stable/jenkins.repo`
- This command tells your system to trust Jenkins packages so you can install them safely.
<br> 👉`[root@ip-172-31-47-91 ~]# sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key`
- Updates all installed packages to the latest version and can remove obsolete packages if needed.
<br> 👉`[root@ip-172-31-47-91 ~]# sudo yum upgrade`
- Amazon Linux has only basic software,so adding EPEL repo lets U easily install extra useful packages like htop, nginx, and dev tools using yum.
- EPEL =  Extra Packages for Enterprise Linux
<br> 👉`[root@ip-172-31-47-91 ~]# amazon-linux-extras install epel`
- “Install Java 11 on Amazon Linux automatically without asking me questions.”
<br> 👉`[root@ip-172-31-47-91 ~]# sudo amazon-linux-extras install java-openjdk11 -y`
- “Install Amazon’s Java 11 automatically on my system.”
<br> 👉`[root@ip-172-31-47-91 ~]# yum install java-11-amazon-corretto -y`
- “Install Jenkins automatically on my system without asking me any questions.”
<br> 👉`[root@ip-172-31-47-91 ~]# yum install jenkins -y`
- “Make Jenkins start automatically whenever my system turns on.”
<br> 👉`[root@ip-172-31-47-91 ~]# sudo systemctl enable jenkins`
- “Turn on Jenkins right now so I can use it.”
<br> 👉`[root@ip-172-31-47-91 ~]# sudo systemctl start jenkins`
- Shows which version of Java is installed and running on your system. `java -version`
- Shows which version of Java compiler is installed. `javac -version`
<br> 👉`[root@ip-172-31-47-91 ~]# systemctl status jenkins`

