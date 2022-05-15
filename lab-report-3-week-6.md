# **CSE 15L Lab Report 3**
## Krishna Reddy
*******

## **Streamlining `ssh` Configuration:**
**Creating/Editing the Config file:**

![Config](config.png)

After opening `.ssh` directory on your local machine using the path `.ssh/config` we have to edit the file to add text that will help us login to our server account with the help of our username. We can set the name of the host to anything that is convenient and easy to type.

**Logging in with the `ssh` alias:**

![ssh](sshKrishna.png)

Here we can see that I can easily login to my ssh account using `ssh Krishna` because I set the name of my host to `Krishna`. We can be sure that this is my account because I set up the config file to my specific `cs15lsp22` username.

**Using `scp` to copy files with the alias:**

![scp](scpMain.png)

I can copy over a file from the local machine to the server using the `scp Main.java Krishna:~/` command.

*****

## **Setup Github Access from ieng6:**

**Public Key on Github:**

![Github](sshGithub.png)

Here, I have stored the ieng6 server's public as an `ssh` key on github so that we can easily use commands like git pull or push directly between the remote Sever and Github.

**Public and Private Keys on User Account:**

![pub&prikeys](keysOnServer.png)

If we login to the server, we can see only see `.ssh` directory if we use `ls -a` which helps see the hidden files. If we `cd` into `.ssh` and use `ls`, we can notice that the public and private keys for the server are stored in here as files. The public key is stored in `id_rsa.pub` and the private key is stored in the file `id_rsa`.

**Git commands to commit and push changes:**

![gitPush](gitPush.png)

When we use the `git status` command it shows us that the MarkdownParse.java file was modified. So we can now use the commands `git add` and `git commit` to add these changes to the staging area and commit them. After that we use `git push origin main` to push the changes to the origin (Github). We can see that the changes were because of our public key stored on the github website.

**This is the [link](https://github.com/kreddy/markdown-parser/commit/9c7a4dca48f6f5277de0792913bb38158460f847) to the commit on the github website**.

*******

## **Copy whole directories with `scp -r`:**

**Copying the markdown-parse directory to ieng6 account:**

![copyOver](copyOver.png)

We can copy over our entire directory recursively using the `scp -r` command. Here is `.` after the `scp` command represents the current directory we are in that we want to copy over to the server. We can do this by providing the Hostname and a directory name to store the contents.

**Logging into ieng6 account to compile and run the test files:**

![test](TestnoScp.png)

We can login to the server and see that our file has been recursively copied over. Now we can into the directory to which we copied our files and run the test files to see if they actually run. From the picture above we can see that the files do run!

**Running all commands on the same line:**

![oneline](testoneLine.png)

Using the command in the image we can copy over all of our files, login to the remote server, and run the files to check if they are actually running and working properly. As you can see above, all the files are being recursively copied over. Below you can see that after the files are copied to a directory on the server, we login to the server and `cd` into the directory we're storing our files in and then run the test file to see if everything is working properly.

![oneLine2](testoneLine2.png)

As we can see here, everything has been copied over and the test runs and we can see that it passes! Another important thing here is that, by doing this we can notice that, it saves us a lot of time and keystrokes.

******



