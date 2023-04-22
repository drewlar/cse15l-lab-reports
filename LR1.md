# Log-in Tutorial For "ieng6"

This a tutorial on logging into your course-specific account on ieng6. Have fun! :)

## Step 1: Accessing Your Course-Specific Account
You can look up your account on the following link,

[https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php)

The link should bring you to a page similar to the one below, enter your TritonLink Username in the first box and your PID in the second.

<img width="948" alt="image" src="https://user-images.githubusercontent.com/130115948/231043697-247cfbbe-a0f6-4260-a173-0780b309fc25.png">

Next you should be sent to a page that shows that account lookup information, your course account username should look like the one on the bottom left of the image below, make sure to take a note of it as you will need it later!

<img width="841" alt="image" src="https://user-images.githubusercontent.com/130115948/231045445-df7dd609-b61c-483a-a13a-046ae22f2dd5.png">

Once selected click on the **"Global Password Change Tool"** link in order to start the set up to change your course-account password. 
Afterwards click on **"Proceed to the Password Change Tool"** link. This is where you need your account
username! 
Once typed in click enter and then select **"I want to reset my course-specific account password"**, you will need to verify through DUO and email address so make sure to have a device at hand. You will be sent a link on the next steps of reseting your password from there. Make sure to take note of this information as well!

## Step 2: Installing Visual Studio Code

First go to the following website to access the installers for Visual Studio Code:

[https://code.visualstudio.com/](https://code.visualstudio.com/)

<img width="951" alt="image" src="https://user-images.githubusercontent.com/130115948/231048231-46f07fa7-26c7-4dfe-a6c4-9a472992e954.png">

The site should already prompt you to download the version designed for your device, if not then there is a drop down menu that allows you to download differnt platform versions of Visual Studio Code. Follow the steps that the installer gives you to download Visual Studio Code. Once installed you will see a screen similar to the one below.

<img width="1025" alt="image" src="https://user-images.githubusercontent.com/130115948/231048564-c333b7cc-95ca-4511-802b-cc1b106f4e0f.png">

## Step 3: Connecting Remotely

If you are on macOS you can skip the next step to downloading "git".

Otherwise if you are Windows you will have to follow the link below and download git.

[https://gitforwindows.org/)](https://gitforwindows.org/)

Once you are finished you will have to access Bash in the terminal. First use the shortcut (control + \`) to open the terminal, you will get something similar to below.

<img width="1026" alt="image" src="https://user-images.githubusercontent.com/130115948/231049798-d19d047c-ffd6-4221-aa0c-d1a580fb8b24.png">

Once that is open click on the "+" in the terminal area and then select Bash.

<img width="1138" alt="image" src="https://user-images.githubusercontent.com/130115948/231049917-701a68ca-6c19-4add-8d25-85292bb3c15e.png">

You are ready to connect!

You will use the ssh command to connect to your account by typing the following command, make sure to replace () with your coresponding username letter:

````$ ssh cs15lsp23()@ieng6.ucsd.edu````

You will get prompted if you would like to continue connect, type in:

**yes**

Afterwards you will be asked for a password, this is the newly set password you set up earlier. You will then get the following:

<img width="674" alt="image" src="https://user-images.githubusercontent.com/130115948/231050565-9c6bdebe-2449-4af0-8d78-588b89d42b11.png">


**YOU ARE IN!!**

## Step 4: Running commands!

Now this is the fun part! You can now play arround and see what commands will give you information relating on files linked to the account!

Here is the list of commands to try out for yourself, as well as an example of some code used.

````$ cd ~````

````$ cd*````

````$ ls -lat````

````$ ls-a````

````$ cp /home/linux/ieng6/cs15lsp23/public/hello.txt ~/````

````$ cat /home/linux/ieng6/cs15lsp23/public/hello.txt````

<img width="568" alt="image" src="https://user-images.githubusercontent.com/130115948/231051257-6ab761b8-965d-411b-a372-5b672fa5b23d.png">


To exit simply type in:

**exit**


## You did it congrats!


