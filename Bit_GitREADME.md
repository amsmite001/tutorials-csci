# Introduction
This document walks through how to set up a Bitbucket account including:
* Creating an Account
* Adding ssh keys
* Adding a repository
* Pulling the repository to the local host (your machine)
* Basic commands
* Merge conflict handling

What is Bitbucket? Bitbucket is an enterprise solution to Github. It is code management with extra features that businesses use.

---
## <a name="head1234"></a>A Heading in this SO entry!
## Creating an Account
It's highly reccomended to use your school email to create an account.
* Go to: https://bitbucket.org/ 
    * If you already have an account, log in. If not, click `Get started` and follow the prompts.
    * You'll want to use your school email to get some additional perks with your account that you'd normally have to pay for.
* _Once you've logged in:_ You'll be brought to your home screen.
    * You can see all of your repositories from here, or by clicking _Repositories_ on the left hand side of the blue bar. (As seen below.)

---
## Creating Repositoires
A repository is an area that you can store like projects. For example, the repo (repository) that this document comes from is full of documents on tutorials. I have repo's for classes and for individual projects.

1. To create a new repo, click the `+` button from the left hand bar. Select _Repository_.
2. Give it a name. This is the name that will show up as a folder once you copy it. It's also the name that the world can see!
3. If you want the repo to be private, leave _Access Level_ checked. If you'd like it open for anyone to view - like this repo, uncheck it.
4. Ignore the _README_ option, unless you know how to write markdown or know how to use them.
5. Version Control: Git.
6. You're done! Hit the _Create Repository_ button to finish!

[goto heading?](#head1234)

![Image of Practice Repo](Practice)


With the student option (that you get automatically by using your CMU email) you can have a large (?) number of repos. Repos are not language limited and can hold a variety of file types (even if Git/Bit can't open them via the website).

__Advanced: Optional__

If you want to learn about how work environments use Bit/Git, under the advanced options, check the _Issue Tracking_ option under _Project Management_. Then, head over to the __Advanced Workflow Tutorial__ document to learn how to use issues.

Good practice also suggests you give it a description, but this can be added later with the README.

---
## Adding SSH Keys
__What are SSH Keys?__

 SSH keys help prevent man in middle attacks, and allow you to connect to Github/Bitbucket without the use of a username and password (though the password option is flakey, and will most likely still ask for it).

<i>Note:</i> Adding 2-factor authentication will make login via the console very difficult. While it's less secure, I'd reccomend not using 2-factor.

__How to add a SSH Key__
Start on the homepage of Bitbucket (the steps are the similar for Github as well). 
1. Select your icon in the lower left-hand side of the screen.
2. Select `Bitbucket Settings`
3. From the center column, near the bottom is `SSH keys`
4. Select `Add Key`

__WSL, Linux, GitBash__

1. Open one of the following listed above. [Git Definition Link](https://confluence.atlassian.com/x/X4FmKw) Enter the following:

    ```
    ssh-keygen
    ```
    The default save locations are okay. _Hit enter for any question it prompts._ It'll look like:

    ```
    Generating public/private rsa key pair.
    Enter file in which to save the key (/home/[Username]/.ssh/id_rsa):
    Enter passphrase (empty for no passphrase):
    Enter same passphrase again:
    Your identification has been saved in /home/[Username]/.ssh/id_rsa.
    Your public key has been saved in /home/[Username]/.ssh/id_rsa.pub.
    The key fingerprint is:
    SHA256:ehzT56yTQ80w7jssxAUvb+iQGcsVs5bGm+S+rxFcw7o [User]@[User]
    The key's randomart image is:
    +---[RSA 2048]----+
    |                 |
    |        +.       |
    |       . B+      |
    |      ..X+=.     |
    |     . %SO.=.    |
    |      *oB==+o    |
    |      .=E= .o    |
    |       .+.B.     |
    |        o=+=     |
    +----[SHA256]-----+
    ```
2. Start the ssh agent.

    * <details><summary>Windows and Linux:</summary>
        <p>

        ```
        eval $(ssh-agent) 
        ```
        </p>
        </details>
        
    * <details><summary>MacOS:</summary>
        <p>

        ```
        eval `ssh-agent`
        ```
        </p>
        </details>

3. Add the ssh key:
    * <details><summary>Windows and Linux:</summary>
        <p>

        ```
        ssh-add ~/.ssh/<private_key_file> 
        ```
        </p>
        </details>
    * <details><summary>MacOS:</summary>
        <p>

        ```
        ssh-add -K ~/.ssh/<private_key_file> 
        ```
        </p>
        </details>
For example, it should be:
```
ssh-add ~/.ssh/id_rsa.pub
```
_Note: If you get an unprotected key file warning, it's okay to ignore it._