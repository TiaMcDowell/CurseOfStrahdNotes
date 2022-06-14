# Notes!

Welcome to my notes on Curse of Strahd!
You're welcome to browse as you see fit :)

~~If you plan on editing the GitHub, please let me know beforehand, just so I can actually use branches and such~~ I am now using branches, you are welcome to change the GitHub :)

If you don't want to edit the GitHub but want to contribute, just send it to me over discord! (I know, It's not quite as cool)

https://github.com/TiaMcDowell/CurseOfStrahdNotes


## How do I edit these notes?
Good question! Here's a tutorial on how to get yourself set up to edit these notes, I'll try to be as foolproof as possible, but if you run into any problems please let your closest tech friend know, and they can help you. 

### Step 1: Signing up and downloading
There are a few tools you need in order to get started.

#### Step 1a:
Download obsidian: https://obsidian.md/

#### Step 1b:
Create an Account: https://github.com/
Once you create an account message Tia on Discord your username, she will add your account to the GitHub repo.

#### Step 1c:
If you run Windows, download: https://gitforwindows.org/
If you run macOS, you are going to need to open a program called **terminal**. Once that is open, copy the following gibberish and paste it in there. 

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install git
echo 'good job ;)'
```

### Step 2: Setting up git and cloning
Git is god in computer science, and you are going to learn the basics!

#### Step 2a:
We're going to add your email to git. To do this, open **Terminal** (macOS) or **Git Bash** (Windows). Copy and paste (and hit enter) the following changing *Your name here* and *your_email@example.com* to your name and email, this is the same email you used to create your GitHub account in Step 1.  Your name will show up on GitHub, so it doesn't have to be your full name or even your actual name, just something to identify you.

```
git config --global user.name "Your name here"
git config --global user.email "your_email@example.com"
```

#### Step 2b:
SSH keys! Super important! Follow the below tutorial to create your own SSH keys and add them into GitHub. 

First, make sure you don't already have SSH keys on your computer, if you do, you can just use those: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys

if you **do not have** existing keys, follow this tutorial to generate them: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

We use SSH keys instead of passwords when using git, they are way faster and easier, and you only have to set them up once!

#### Step 2c:
Now that we have git set up, we can "clone" the files on to your computer. To do this, open **Terminal** (macOS) or **Git Bash** (Windows) again and copy and paste the following and hit enter the following command to download the files.

```
cd ~/Documents
git clone https://github.com/TiaMcDowell/CurseOfStrahdNotes.git
```

Great! Now you have the files! Next is setting you up to edit them.

### Step 3: Setting up to edit
Once we have the files, how do we edit them while staying up to date with other people who edit them? 

#### Step 3a:
Open obsidian on your computer, you are then going to open an existing vault. The "Vault" is what you downloaded from git. It should be in your Documents folder. Once you open it, you should be able to see all the notes in the docs folder.

### Step 4: Editing
This is **VERY** important. This is also the part of the tutorial you should come back to from time to time. These are the commands you run **BEFORE** and **AFTER** editing the notes for a session. 

#### Step 4a:
**BEFORE** editing, run the following commands in your terminal/git bash, **changing** NAME and NUMBER to your name/username/chosen identifier and session number. Please remember to do this, if you do not your changes may be saved to the wrong place and be annoying to get back. 
```
cd ~/Documents/CurseOfStrahdNotes
git checkout main
git pull
git checkout -b NAME-session-NUMBER
echo "you are now ready to make changes :)"
```

#### Step 4b:
**AFTER** you are completely done editing the notes for a session, run the following commands, **changing** NAME and NUMBER to the same thing you changed it to in 4a. If you do not run these commands, your changes will not be saved to GitHub and will not show up on the website
```
cd ~/Documents/CurseOfStrahdNotes
git add .
git commit -m "session notes"
git push --set-upstream origin NAME-session-NUMBER
echo "your changes have been saved, and in a few minutes be up on the website."
```


#### If you run into any issues, message your closest tech person :)