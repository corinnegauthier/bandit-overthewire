# bandit-overthewire
An in-depth guide through every level of OverTheWire's Bandit game.


# Level 0 
In this initial stage, our task is simply to access the game's server through SSH. All the necessary details are readily provided: the hostname is bandit.labs.overthewire.org, the username is bandit0, and connection is established via port 2220. The password for this level is also bandit0.

To initiate an SSH connection, simply employ the syntax: **ssh [username]@[hostname or IP address]** with the option **-p [port number]** to specify the port. 

So, to advance past this stage, we would execute the following command: 

**ssh bandit0@bandit.labs.overthewire.org -p 2220**

<img width="627" alt="Screenshot 2024-02-22 at 7 47 40 PM" src="https://github.com/corinnegauthier/bandit-overthewire/assets/99577276/204bc4b4-9727-4a0a-a8bb-ce68cb34805f">



# Level 1
In this level, our objective is to locate a file named **readme** situated in the home directory. This file holds the password for accessing the next level. Upon finding the password, we'll proceed to log into bandit1 via SSH.

To begin, let's employ the **ls** command, which retrieves a directory's file listing to locate the **readme** file. Once located, we'll proceed with the **cat** command. The **cat** command boasts numerous functionalities, including viewing, concatenating, creating, copying, merging, and manipulating file contents. Here, our aim is to utilize it for viewing the contents of the **readme** file.

To progress to the next stage, we would execute the following commands:

**ls**

**cat readme**

<img width="623" alt="Screenshot 2024-02-22 at 7 51 32 PM" src="https://github.com/corinnegauthier/bandit-overthewire/assets/99577276/e36df663-d7e9-4ad3-af7a-b2a959955fb3">


# Level 2
In this level, our objective is to find the password within a file named **-** located in the home directory. Once accomplished, we'll proceed to SSH into bandit2 using the retrieved password.

This level closely resembles the previous one. We'll start by using the familiar **ls** command to list all files within the directory. Once the list is displayed, we'll proceed with the **cat** command, but there's a catch. Using **cat** directly will result in an error due to the file name being a symbol. To work around this issue, we'll use the redirection operator **<**. This method allows us to view the contents of the **-** file without any problems.

The move onto the next level, we would execute the following commands:

**ls**

**cat < -**


<img width="562" alt="Screenshot 2024-02-22 at 8 21 31 PM" src="https://github.com/corinnegauthier/bandit-overthewire/assets/99577276/b8b15398-e382-42df-a4e0-7bc2c53b8382">


# Level 3
In the upcoming level, our objective is to access the contents of a file named **spaces in this filename**. This file holds the password for the next level, allowing us to SSH into bandit3.

Once more, this level bears resemblance to the previous one. We'll kick off by listing all files using the **ls** command. Just like the previous level, attempting to use the **cat** command on its own will lead to errors due to the spaces in the file name. To overcome this hurdle, we'll add a backslash key after each word. This simple adjustment will enable us to open the file smoothly.

To advance to the next level, we would execute the following commands: 

**ls**

**cat spaces\ in\ this\ filename**

<img width="556" alt="Screenshot 2024-02-22 at 8 28 02 PM" src="https://github.com/corinnegauthier/bandit-overthewire/assets/99577276/d50b0182-eb78-48a7-ad1f-628ad1159cfa">


# Level 4
In this level, our goal is to uncover the password stored in a hidden file within the **inhere** directory. Once obtained, we can progress to the next level and SSH into bandit4.

Let's begin by utilizing the **ls** command to locate the **inhere** directory. Once located, our next step is to navigate into it using the **cd** command, shorthand for "change directory". Upon entering the directory, we'll utilize the **ls** command once more. However, this time, we'll need to include an option to display hidden files. To achieve this, we'll utilize the **-a** option with **ls**, indicating "all", thus revealing all files, including hidden ones. Following this, we'll execute the **cat** command to inspect the contents of the hidden file named **.hidden**.

To progress to the next stage, we would execute the following commands:

**ls**

**cd inhere**

**ls -a**

**cat .hidden**

<img width="556" alt="Screenshot 2024-02-22 at 8 58 59 PM" src="https://github.com/corinnegauthier/bandit-overthewire/assets/99577276/8b62b912-f7da-44a2-ae22-0b7208e3adf4">
