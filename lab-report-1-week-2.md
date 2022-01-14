# Installing VScode
![Image](add.link)
I already had VScode installed. When you open the application, the above window appears. To open an existing project, click the "open folder".

---
# Remotely Connecting
* enter `ssh cs15lw22apu@ieng.ucsd.edu`
* enter password. the text will not show up. hit enter
![Image](add.link)
* the list of available host computers will be displayed (like above)

---
# Trying Commands
![Image](add.link)
**Basic Commands**
* cd: takes you to the specified directory
* ls: shows the files in the folder
* ls -lat: shows the files in the directory with additiona information
* ls -a: shows additional files in the directory

---
# Moving Files with scp
![Image](add.link)
* create/edit a file on your client device, save changes
* without signing in to the remote server, enter `scp <path to file on your computer> <enter username + folder path or :\~> `
* enter password

---
# Setting an SSH Key
![Image](add.link)
* for windows enter `ssh-keygen -t ed25519`
* when prompted to enter the file to save the key enter `<path to .ssh folder>/id_rsa`
* do not create an id_rsa file before the above step
* ssh into the remote server and us `mkdir` to create a .ssh folder in the remote server
* move the public key file to the `.ssh` remote server using `scp` (you will need to enter your password)
* you should now be able to `ssh` and `scp` without entering your password

---
# Making Remote Running More Efficient
`ssh cs15lwi22apu@ieng.ucsd.edu "<command, separated with semicolons if there are multiple>"`
this will ssh into the remote server, run the commands, then logout
