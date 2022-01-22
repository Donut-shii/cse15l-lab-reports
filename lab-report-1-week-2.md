__Week 2: Lab Report By: Camille Saldajeno__
=========

STEP 1:
---------

__Download Visual Code Studio__ using the following link: 
[Link][1]

[1]: https://code.visualstudio.com/ 

and choose the version meant for your computer. For example, version OSX for Macs. The home page of the application should appear similarly to this:

![Image][1]

[1]:
![VisHomepage](https://user-images.githubusercontent.com/91626896/150620384-080cd64a-5867-4fae-aaee-affa25821a16.png)


STEP 2:
---------
Use Vscode to __remotely connect__ the computer over the internet by first opening a terminal (should be on top of the computer screen). In the terminal, use the a command with the following format:
$ ssh cs15lwi22aoq@ieng6.ucsd.edu  where the ‘aoq’ refers to a course-specific account. The command outputs a message request that initiates your UCSD password – the password input is invisible for security purposes. Press enter and the result is the following screenshot:

![Image][1]

[1]: https://lh3.googleusercontent.com/PGIU4-R_N5XRduFreNPI-CKvYqLfZdIvvSMJubAspiGkSPKop-HKukS3HEL0qApSecFYJA7Sodci5y6-4KfhZ9PFS-g5nQ14ca454tENjVPnnBCmQVyW2uNwQzUuKkBPMR7yIbPg


STEP 3:
---------
__Try running some commands__ such as cd, ls, pwd, mkdir, and cp. The specific command used in the screenshot is ls -lat, which outputs a list of computer files in Unix or Unix-like systems (in this case, in MacOSX).

![Image][1]

[1]: https://lh6.googleusercontent.com/Tg63I83GFA-JPKlwRBx0gUSAVoYesclDDst1aAJqNL5no2FRFyIi4qnu8hOmpgJGezQcUcNyO1IXu2OUBNKk_bSF7LVXVPj7xHQCwERsbeO2pdCQ-oZpbhW4I0l9aHdkdfxatHJ1

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

![Image][1]

[1]: https://lh6.googleusercontent.com/kx2Qo73BtReiiblms0K4ofdjbRRk9PHjwKi0kwNVF3_hp9X7CsifhTP07gE-paGbX5HpOa86PqnWy15ODK0i5W4LywvMnp1NmGtrL0UTFYGS56_aIzHgySmquQbkR_d4EIoeZyEz

Try logging into ssh again (ssh cs15lwi22aoq@ieng6.ucsd.edu and enter password) and run ls, which should show the file in the home directory like shown:

![Image][1]

[1]: https://lh3.googleusercontent.com/c_XLWqAA1ZhW3OgFwOGNXzvKfQOvrEjSD63OaBBNzR-CCaPx9MlnH6OWGPR6guQG5zyCb7U0x0VvwFH3cZcqKNCAsEJ-xbl6cI-qeYuZnFZ7WfSyxWMKGVEn0z6_eqUAtHd7Dezj

STEP 5:
---------
__Set an SSH Key__ by using the command: ssh-keygen. This command outputs an enter file message where you will copy and paste the location that is set in the given (from the message) parentheses (/Users/donuts/.ssh/id_rsa). Press Enter for an empty passphrase upon output request. To ssh or scp without having to enter a password, ssh and run mkdir .ssh, then <logout>. Afterwards input:
scp /Users/donuts/.ssh/id_rsa.pub. cs15lwi22aoq@ieng6.ucsd.edu:~/.ssh/authorized_keys

![Image][1]

[1]: https://lh3.googleusercontent.com/s4jepu2RcjyHDuDbj1eUheY_zFe2iVjhgeJkioZwi_e5S408hR4RADZ3HauC5a_16GphiuDJOTv3h5O5_qQbI--eA9XuhcHQ9MjAejW5JOQbTbAJ7y6d2ejLw9q0p_rnQl-_szeQ

STEP 6:
---------
__Optimize remote running__
- Start off by downloading the remote ftp-sync extension
- Type command-p for search engine and type/click ftp-sync remote-local
- Change the following information in order to sync:
  
![Image][1]

[1]: https://lh6.googleusercontent.com/a-Cphj5PWUj2r9C9Gmu2U5uEOj-DAYIpIS4fgDBbDJrN0tzV6itrBOyh68q6llLjqKnNYh49U2Rk8m9_yh5261wEUj1c-HdG_gvgE7VHXZBdG2m3xfVHR_brpkIAhnbzExerTKag
