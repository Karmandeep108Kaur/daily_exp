# My 15-days Training Journey
--- 
## Day-1
- To begin with, we all gathered in the college auditorium at 8:30 sharp with great enthusiasm, where our department faculty members explained the following
  - norms and regulations
  - syllabus
  - societis
  - projects, etc
    

- Furthermore, around 9:30 we headed towards our respective labs, where faculty members taugth us for four hours with following outcomes:
    - Here, we learned about product based, service based companies and startups.
    - Our teacher started the basics of linux OS in order the built our basic foundation in this field.
    - We explored the features of linux which make it is one of the best OS
        - Open source
        - Ease of use
        - Highly secure
        - Customization
        - Licensing
        - Software Compatibility, etc
    - To add more, our teacher shared her own expering of working in a company and provide various crucial tips
    - Furthermore, she interacted with us and and enquired our future aspirations and goals
    - To proceed with, we downloaded Virtual Box, Ubuntu and Microsoft Visual C++
    - Finally, once the linux setup completed, we concluded our 4-hours session with certain words of wisdom form our Mentor
- In a nutshell, our first day at training was quite productive and inspirative
----
## Day-2

### Fundamentals of Linux/Unix and Bash

-	**Booting of computer and its types**
    1.	Cold boot   
        - Starting a computer from power off state
    3.	Warm boot  
        - Restarting the computer without off power

- **Kernel (a computer program)**
    1.	Like a chef , can’t see, but working with hardware
    2.	Waiter is shell
    3.	Complete control over everything in the system
    4.	Core of  computer operating system
      	- File management
        - i/o management
        - memory management, etc

  ```mermaid
  graph LR
    USER["User"]
    SHELL["Shell (Command Interpreter)"]
    KERNEL["Kernel (Core OS)"]
    HARDWARE["Hardware"]
  
    USER --> SHELL
    SHELL --> KERNEL
    KERNEL --> HARDWARE


-	**Shell (Waiter) & Bash**
    -	A program – interface between the user and OS
    -	Gives instructions to computer – opening files, etc
    -	Commands -> computer language
    -	Types of shell
        -	Bash – most common
        -	Sh – original 
        -	ksh
        -	csh
    -	Categories
        -	Command line 
        -	Graphics User

  - **File Structure**
     
      |Directory   |Function        |
      |---|---|
      | `/` | Root of the filesystem |
      | `/home` | User folders |
      | `/lib`  | System libraries |
      | `/bin`  | Basic commands |
      | `/boot` | Boot files |
      | `/dev` | Device files |
      | `/media` | Auto-mounted drives |
      | `/mnt` | Manual mounts |
      | `/opt` | Optional apps |
      | `/sbin` | Admin commands |
      | `/var` | Logs & data |
      | `/tmp` | Temporary files |

    **File Structure (Flowchart)**

    ```mermaid
    graph TD
    ROOT["/ (Root)"]
    ROOT --> HOME["home"]
    ROOT --> LIB["lib"]
    ROOT --> BIN["bin"]
    ROOT --> BOOT["boot"]
    ROOT --> DEV["dev"]
    ROOT --> MEDIA["media"]
    ROOT --> MNT["mnt"]
    ROOT --> OPT["opt"]
    ROOT --> SBIN["sbin"]
    ROOT --> VAR["var"]
    ROOT --> TMP["tmp"]
         

- **Commands**
    - **`ls`** – Lists contents of the current folder.

      ![](images/Picture1.png)

      
    - **Don’t access `/` directly** – Root directory; changing things here can break the system.  
    - **`mkdir`** – Creates a new directory.
      
      ![](images/mkdir.png)

      
    - **`cat`** – Creates or displays file content.  
    - **`touch`** – Creates an empty file.
      
      ![](images/touch.png)

        
    - **`whoami`** – Shows your current username.
      
      ![](images/whoami.png)

      
    - **`date`** – Displays the current date and time.
      
      ![](images/date.png)

      
    - **`cd`** – Changes the current directory.
      
      ![](images/cd.png)

      
    - **`cd -`** – Switches to the previous directory.
      
      ![](images/cd-.png)

      
    - **`cp`** – Copies files or folders.
      
      ![](images/cp.png)

      
    - **`pwd`** – Prints the current directory path.
      
      ![](images/pwd.png)

        
    - **`whereis`** – Finds the location of command’s binary, source, and manual.
      
      ![](images/whereis.png)

      
    - **`whatis`** – Shows a short description of a command.
      
      ![](images/whatis.png)

      
    - **`mv`** – Moves or renames files and directories.
      
      ![](images/mv.png)

      
    - **`rmdir`** – Removes an empty directory.
      
      ![](images/rmdir.png)

      
    - **`Ctrl + Alt + T`** – Opens the terminal directly.
  ---
  ## Day 3
  - **Bare Metal Installation**
    1. Installation directly using USB
    2. Direct installation in computer hardware
    3. No OS in between
    4. Example – you delete windows-> install Ubuntu using USB ->no windows, no 
       mac only linux as main OS

  - **Partitioning schemes**
    1. Dividing a hard disk into separate sections.
    2. Each section (partition) acts like an independent disk.
    3. Helps organize data and install multiple OS.
    4. Types:
        - MBR (Master Boot Record)
            - Max 4 primary partitions.
            - Supports up to 2 TB.
            - Older, used with BIOS.
            - less flexible
        - GPT (GUID Partition Table)
            - Supports 128+ partitions.
            - Works with disks >2 TB.
            - Newer, used with UEFI.
            - more flexible
  - **File and Directory permissions**
       - Types of Users  
    ```mermaid
    graph TD
        A[Users] --> B[Owner]  
        A --> C[Group]  
        A --> D[Others]
    
    ```


       - Types of permissions
      ```mermaid
            graph TD
            P[Permissions] --> R[Read \`r\']
            P --> W[Write \`w\`]
            P --> X[Execute \'x\`]
      ```

       - Types of Commands
           - `chmod`
               - Changes file permissions (read, write, execute).  
                    1. chmod 755 file.txt  
                       Sets permissions:  
                       7 = Owner → read, write, execute  
                       5 = Group → read, execute  
                       5 = Others → read, execute  
                       Used to make a file executable and readable by everyone  
                    2. chmod 444 – read only permission to everyone  
                    3. chmod 644 – permissions to owner only  
                    4. chmod +x filename  
                           +x – execute the file  
                           ./filename  
                           ./ - To run a file  

 
  

          - `chown`  
               - Changes file owner or group.      
                 1. chown user:group file.txt     
                    Change the owner to user       
                    Change the group to group      
                    So that other users in that group can access the file
      

  - **Redirection**
      1. i/o redirect to a file
      2. Echo hello > day3.txt
      3. Redirecting the message ‘hello’ to file ‘day3.txt’
      4. Operators – ‘>’, ‘>>’, ‘<’ etc
  - **Pipes**
      1. Particular files in a particular folder
      2. Types

       # to be continued.....




 
  
      




       


      





    




    
