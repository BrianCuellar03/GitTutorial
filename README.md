# GitTutorial For Junior Seminar Class

Imagine you're working on a massive jigsaw puzzle with friends, where each piece represents a change or addition you make to a project. Now, imagine if you could save your progress at any moment, 
experiment with placing pieces without risking the entire puzzle, and even go back in time to see how you got to a certain point. Essentially, this is what Git does for software development. 

Git is a version control system, a tool that tracks every single change made to a project's files. It's like a detailed history book of your project, allowing you to pinpoint who made changes, what was changed, and when it happened. This is incredibly useful when you're working in a team and need to collaborate without interfering with other collaborators. 

# Before We Get Started

**Requirements**

Please have Git Installed. If you dont have Git, the next section will be a guide on how to download it on macOs. 

Please have an IDE or a text editor with python installed (Pycharm, Visual Studio Code, Juypter Notebook, Atom, Eclipse, etc)

Basic or Proficient understanding in Python or another programming language.

# Git Installion Instrucions for Mac 

Please install Git. You can install git through terminal in Mac. Or there are other ways that are listed on the Git website. This is the link. https://git-scm.com/download/mac

Once you've opened terminal in your mac, please type this in the terminal.

```
 xcode-select --install
```

A pop-up window will appear asking if you want to install the tools. Confirm by clicking “Install” and agree to the terms of service when prompted.
Once the installation is complete, Git will be installed on your system as part of the Xcode Command-Line Tools.

You can verify that git was installed by typing: 
```
git --version
```
This command will return the installed version of Git, indicating that Git has been successfully installed on your Mac.
If this has returned an issue where the terminal says that you havent accepted the terms of service, please follow the directions given to accept in terminal. 


# Getting Started with Git

Now that we have git installed, we can move on with the tutorial. 

***Initialize a Git Repository***

Create a New Directory for our Mood Checker Project: Open a terminal and run:

```
mkdir MoodChecker
cd MoodChecker
```

Then, run the following command in your project directory:

```
git init
```

# Creating Your Python Project: Mood Checker (IDE)

Open your project in your chosen IDE. For this project, we will make a mood checker, where the script will ask the user for their mood. A response will be generated based on the users input. 

I will be using Vs Code for this example: Launch Visual Studio Code and open the MoodChecker directory you created in the last step. Create a file in this MoodChecker folder and name it:

***mood_checker.py***


Please paste in this python code for our tutorial.

```python
# Ask the user to type their current mood
user_mood = input("How are you feeling today? (happy, sad, excited, tired): ")

# Response based on the user's input
if user_mood == "happy":
    print("It's great to see you happy!")
elif user_mood == "sad":
    print("I'm sorry to hear that. Hope you feel better soon!")
elif user_mood == "excited":
    print("Wow, that's exciting! Tell me more!")
elif user_mood == "tired":
    print("You should rest. Everyone deserves a break.")
else:
    print("Hmm, I don't know that mood.")
```

# Track Your File and Commit Changes (Terminal)

***Track your mew file:*** With mood_checker.py created, go back to your terminal (make sure you're in the MoodChecker directory) and run:
```
git add mood_checker.py
```

This command stages your file for the next commit.

**Commit your file:*** To commit your file to the repository with a message describing what you've done, run:

```
git commit -m "Initial commit of mood checker script"
```

This saves your changes to the project's history.

# Branching (Terminal)
Creating a branch allows you to work on new features without affecting the main project (usually referred to as the main or master branch).

***Create a new branch:*** Let's say you want to add more moods to your script. Create a branch for this feature:

```
git branch more-moods
```
***Switch to your new branch:*** Change to the new branch with:

```
git checkout more-moods
```
# Making Changes and Using Stashes (Terminal)

After branching in Step 4, where you've created and switched to a new branch for development, the next step involves making changes to your project within this new branch. 
This is where you can experiment and develop new features safely, separate from the main branch. 

Return to Your IDE: Make your desired changes to mood_checker.py in your IDE.
***Stash your changes:*** If at any point you need to switch to another activity or task but you're not ready to commit these changes on the branch you created, switch back to your terminal and run:

```
git stash
```
This command will save your changes away, allowing you to switch branches or tasks without losing your work.

# Apply Your Stash to Continue Working (Terminal) 

When you're ready to continue working on the stashed changes above:
In your terminal, run:

```
git stash pop
```

# Committing Branch Changes (Terminal)
Committing these changes in our branch allows us to capture our progress, making our experimental features a solid part of our project's history.

***Stage and commit your changes:*** After editing, switch back to the terminal to add and commit these changes:

```
git add mood_checker.py
git commit -m "Add more moods to the script"
```
# Merging Your Changes (Terminal)
Once we're satisfied with the developments and edits in our branch, the next step is to bring those changes back into our main project. 
Merging allows us to integrate our new features, combining our new branch and main branch into one single version. 

***Switch back to main branch:*** Use the terminal to switch branches by typing:

```
git checkout main
```

***Merge your feature branch:***

```
git merge more-moods
```


# Pushing To GitHub (Terminal)

Git and GitHub are often mentioned together and work hand in hand but serve different purposes. The core difference between Git and GitHub is that Git is a version control system that allows individuals and teams to track changes to a file over time, enabling any one of them to revert to previous versions if needed.

GitHub, in contrast, is a cloud-based hosting service that uses Git for version control but provides a graphical interface and additional features for collaboration across projects. 

Pushing to GitHub is the process of uploading your local repository's contents to a remote repository, enabling collaboration and backup of your project online. Heres how we can do this. 

Step 1. Create a Repository on Git Hub. You can name it GitTutorial. 

![Screenshot 2024-02-11 at 11 49 49 PM](https://github.com/BrianCuellar03/GitTutorial/assets/125411833/7fc19808-73a4-4455-ac3e-8c086eda3882)


After creating it, you will see this. 

***Step 2:*** Now in your terminal, link your local repository (first repository created in beginning of tutorial) to GitHub. 

```
git remote add origin <REPOSITORY_URL>
```

***Step 3:*** Push your local repository to GitHub by typing this in your terminal:

```
git push -u origin main
```

If steps done right and there wasnt a GitHub authentication error, this should appear in your terminal. 


![Screenshot 2024-02-12 at 12 03 20 AM](https://github.com/BrianCuellar03/GitTutorial/assets/125411833/46eb40fd-f5ec-4e52-b6af-d6766d0e835d)


# Conclusion

***Congratulations!*** You have reached the end of the git tutorial. This tutorial covered the basics of Git, from creating a local repository, commit your work, create and switch between branches, stash and apply changes, 
merch branches to add new changes to main branch, and push local repository onto Github for colloboration and version control.




