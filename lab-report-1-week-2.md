__Week 2: Lab Report__
=========
__By: Camille Saldajeno__
=========

```
# code block
print '3 backticks or'
print 'indent 4 spaces'
```

STEP 1:
---------

__Download Visual Code Studio__ using the following link: 
[Link][1]

[1]: https://code.visualstudio.com/ 

and choose the version meant for your computer. For example, version OSX for Macs. The home page of the application should appear similarly to this:

![VisHomepage](https://user-images.githubusercontent.com/91626896/150620490-b7beec5f-846e-4daf-acbe-f07b8f978b3e.png)


STEP 2:
---------
Use Vscode to __remotely connect__ the computer over the internet by first opening a terminal (should be on top of the computer screen). In the terminal, use the a command with the following format:
$ ssh cs15lwi22aoq@ieng6.ucsd.edu  where the ‘aoq’ refers to a course-specific account. The command outputs a message request that initiates your UCSD password – the password input is invisible for security purposes. Press enter and the result is the following screenshot:

![remotelyconnect](https://user-images.githubusercontent.com/91626896/150620546-1ed72251-071b-4d7f-a7d7-a115d2cbc684.png)


STEP 3:
---------
__Try running some commands__ such as cd, ls, pwd, mkdir, and cp. The specific command used in the screenshot is ls -lat, which outputs a list of computer files in Unix or Unix-like systems (in this case, in MacOSX).

![runningcommands](https://user-images.githubusercontent.com/91626896/150620571-283992f7-6d6a-47e8-aa24-3067ca06b556.png)
![Image][1]

STEP 4:
---------
Create a folder called test Visual Code and then create a file in it called WhereAmI. Save the following text content:
class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
In the terminal, run java WhereAmI and __move files using the scp command__ by running scp WhereAmI.java cs15lwi22aoq@ieng6.ucsd.edu:~/ afterwards. Type password and the results are the following:

![step4_p1](https://user-images.githubusercontent.com/91626896/150620629-0bcf7b0e-f260-40ee-8b7d-8168984003f6.png)

Try logging into ssh again (ssh cs15lwi22aoq@ieng6.ucsd.edu and enter password) and run ls, which should show the file in the home directory like shown:

![step4_2](https://user-images.githubusercontent.com/91626896/150620641-4ab51f72-4ae8-4afa-a83a-691842e0054b.png)

STEP 5:
---------
__Set an SSH Key__ by using the command: ssh-keygen. This command outputs an enter file message where you will copy and paste the location that is set in the given (from the message) parentheses (/Users/donuts/.ssh/id_rsa). Press Enter for an empty passphrase upon output request. To ssh or scp without having to enter a password, ssh and run mkdir .ssh, then <logout>. Afterwards input:
scp /Users/donuts/.ssh/id_rsa.pub. cs15lwi22aoq@ieng6.ucsd.edu:~/.ssh/authorized_keys

![sshkey](https://user-images.githubusercontent.com/91626896/150620719-0a3298ec-0a59-4967-be3a-6ff4fddb21f3.png)

STEP 6:
---------
__Optimize remote running__
- Start off by downloading the remote ftp-sync extension
- Type command-p for search engine and type/click ftp-sync remote-local
- Change the following information in order to sync:
  
![step6](https://user-images.githubusercontent.com/91626896/150620730-3544b3d9-261d-47df-bd10-9106e0230406.png)
