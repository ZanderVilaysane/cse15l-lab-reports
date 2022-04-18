# Week 2 Lab Report
## Topic: Remote Access via VScode
#### Author: Zander Vilaysane

### How-To Tutorial on: logging into a course-specific account on `**ieng6**`
### Step 1: Install VScode
Download Visual Studio Code to your device by clicking [**HERE**][VScode Link]. Follow the steps prompted in the link. Make sure to download the correct program for your OS (Windows, Mac, Linux) which can be found in the drop-down menu. 

![Installing VScode][VScode SS]
> When you open up the VScode program, you should expect to see a similiar layout above! If so, you're doing great so far.

### Step 2: Connecting to a Remote Server
1.  (For Windows) Download OpenSSH to your device by clicking [**here**][SSH Link]. This is needed to connect remotely!
2. Navigate to your course-specific account by clicking [**here**][Course Link].
3. Be familiar with VScode's remote option with this [**reference**][Connect to a remote host].
4. Open VScode, open a terminal and run the following command: `$ ssh cs15lsp22zz@ieng6.ucsd.edu`
- *Note:* replace zz w/ your respective account
5. Follow the directions prompted by the terminal.

![Remotely Connecting][Remote SS]
> When you log in remotely through terminal, you should expect to see a similiar status pop up. *Note:* Some data may not look exactly the same as the one shown above!

### Step 3: Experiment and Familiarize w/ the Following Commands
Within the command prompt, test out these commands: 
- ```cd "directory name"``` will access the directory typed in
- ```cd ~``` will access the initial starting directory
- ```ls -lat``` retrieves name of directory and contents within it
- ```ls -a``` is similar to -lat but will also include hidden contents
- ```pwd``` retrieves the directory that we are currently in
![Trying Some Commands][Commands SS]
> This is an example of what `ls -a` may show. If something similiar appears for you, then you correctly accessed your acccount remotely so far!

### Step 4: Understanding scp & How to Move Files
- Access the directory where your selected file is located
- Run this command with your username and log-in: `scp fileName.java cs15lsp22zz@ieng6.ucsd.edu:~/` 
![Moving Files with scp][scp SS]
> The split terminals above showcases the server terminal and client terminal.

### Step 5: Setting an SSH Key
1. On the client terminal, enter `ssh-keygen` and hit enter twice when a passphrase is prompted.
2. Copy the public key found in the .ssh directory to the server terminal.
3. In this same terminal, input `mkdir .ssh` then log out `ctrl+D` to create an .ssh directory.
4. Use scp command (Step 4) to move the public key into the server's .ssh directory
![Setting an SSH Key][SSH SS]
> Mine was unable to work due to file directory mix-up but ultimately you should be able to log-in without a password! Setting an SSH saves a considerable amount of time when working remotely on servers.

### Step 6: Optimizing Remote Running 
- One method to optimize the remote running process is through the use of semicolons inbetween commands. This allows multiple commands to string in the same command line, optimizing runtime within the terminal. 
![Optimizing Remote Running][Remote Run SS]
> This is an example of how semicolons are utilized within the terminal.

---

[VScode Link]: https://code.visualstudio.com/
[VScode SS]: https://user-images.githubusercontent.com/103156131/162597326-4984a9c9-627c-4c1a-bafd-4ecc29601f57.JPG
[SSH Link]: https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse
[Course Link]: https://sdacs.ucsd.edu/~icc/index.php
[Connect to a remote host]: https://code.visualstudio.com/docs/remote/ssh#_connect-to-a-remote-host
[Remote SS]: https://user-images.githubusercontent.com/103156131/162674659-131bf6d6-f424-498e-915e-d9a101e56323.JPG
[Commands SS]: https://user-images.githubusercontent.com/103156131/162674863-4e54e620-bf9d-4d1a-a77f-b3dd7d389826.JPG
[scp SS]: https://user-images.githubusercontent.com/103156131/162674934-d3ed4d60-c2c4-4fd5-afed-0f52210acec2.JPG
[SSH SS]:https://user-images.githubusercontent.com/103156131/162676137-5b116445-3f38-4a89-8055-02d32473086b.JPG
[Remote Run SS]: https://user-images.githubusercontent.com/103156131/162676973-8d0fa227-ecec-4486-8040-648ba4447f90.JPG
