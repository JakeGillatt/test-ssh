# Using SSH with git bash and GitHub

First, navigate to your Home directory by entering 'cd', and create the .ssh folder using 'mkdir .ssh'.
Use cd .ssh to enter the .ssh folder.

![image1.jpg](image1.jpg)

Generate the public/private key pairs using the code “ssh-keygen -t rsa -b 4096 -C "your_email". You can then enter the file name you wish to save your keys into
Enter the passphrase if required, if not, leave blank and press enter.
Enter the same passphrase if required, if not, press enter again.

![image2.jpg](image2.jpg)

Git bash has now created your key pairs.

Display your public key with the code “cat ‘name’-github-key.pub”. ensure to add .pub to obtain the public key.
Once the key is displayed, copy the full key from “ssh-rsa” to the end of the email. Now head over to GitHub.

![image3.jpg](image3.jpg)

Once you are on GitHub, go into your account settings and select the ‘SSH and GPG keys’ tab on the left. Then click ‘New SSH key’ on the top right.

![image4.jpg](image4.jpg)

Now you can paste your public key into the ‘key’ section and title it with preferably the same name as the key file. Click “Add SSH key” when complete to add the key.

![image5.jpg](image5.jpg)

Now in git bash we need to register the key to the SSH agent using “eval `ssh-agent -s` and then “ssh-add jake-github-key”. Use the code “ssh -T git@github.com to test whether it has successfully authenticated.

![image6.jpg](image6.jpg)

Now in GitHub, create a new repository. 

![image7.jpg](image7.jpg)

Once the new repository is created, select the SSH button.

![image8.jpg](image8.jpg)

Back in Git bash, navigate to your github folder using the cd commands. Then create a new ssh folder. Within this folder create a new README.md file using “touch README.md”. Use LS to check the file has been created.

![image9.jpg](image9.jpg)

Use “nano README.md” to access the file within git bash. Use CTRL + S to save the file and CTRL + X to exit the file.

![image10.jpg](image10.jpg)

Use “git init” to create a git repo and then use “git add .” to add the files to the repo.

![image11.jpg](image11.jpg)

Now use “git commit -m ‘message’” to commit

![image12.jpg](image12.jpg)

Rename the branch to main with “git branch -M main”
Copy the ‘git remote add origin’ link from GitHub and enter it.
Push the files to GitHub with “git push -u origin main”

![image13.jpg](image13.jpg)
