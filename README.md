# 🌟“END-TO-END DEVOPS PROJECT USING GITHUB :octocat: , MAVEN, JENKINS, AND TOMCAT SERVER”🌟
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
<br> Advanced SSH Settings = ✔️ use private key = ______(Provide private key which is in downloads) ➡️ ✔️x11 = Forwarding ➡️ ✔️Compression ➡️ Remote environment = interactive shell ➡️ SSH = browser-type = SFTP protocol = OK 
<br> **` Go to Terminal `**
<br> 👉 
