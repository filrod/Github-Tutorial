# Github-Tutorial
Here are my findings on how to use github in the terminal


## What to know about github in linux:

	> github (remote) is what is up on your github website
	> git is on your computer ready to be added and pushed out to the github
	> A commit is usefull to do after adding and before pushing, this ensures that versions aren't just overwritten.
	> Branching is paramount when not working alone. (You do not want to mess up the master branch)
	> You can merge with master later and if working under someone else, they will have to authorize your request.


# Commands

## Getting Started (cloning, making a repository, making a commit, a branch, pushing)
	
1.a) Make a repository in your computer running some version of linux. Type in terminal:

	$mkdir Github-Tutorial

NOTE: Everytime the "$" sign is used only type what comes after it. And Github-Tutorial is the repository name (ie folder) we wish to create.

## ------------------------------------ OR --------------------------------------------------

1.b) From an existing repository in github, clone it:

	$git clone http://github.com/USERNAME/Github-Tutorial.git
    
## Setting up git with remote pointing to github

2) Change directories into the file in linux:

		$cd Github-Tutorial

3) Initialize path (Creates a refference like a pointer)

		$git init

4) Show github origin location and local git:

		$git remote -v

NOTE: This says nothing since we did not set it up with a link on the website.
	    A way around this is to in step 1 create a repository before by doing 1 b)
			
####                  ********** IF YOU CHOSE 1 a) ************

##### Write the following (which is similar to steps 8 and 11):


   i) Add a remote link of the github repository you made on the website (use same name)
		
	$git remote add origin http://github.com/USERNAME/Github-Tutorial.git   (Here Github-Tutorial.git is your FolderName.git)

   ii) Push this out to origin master

	$git push -u origin master

Now "$git remote -v" will give you a (fetch) and (push) location.
		

5) Create a file using touch command on linux:

		$touch gitTutorial.txt
	NOTE: File name is "gitTutorial.txt" it is a txt file.

6) Modify it in vi:

		$vi gitTutorial.txt
		
			a) Tap the i key on your keyboard to write in the file.
			b) Type anything
			c) Press Esc key
			d) Press the semi-colon for a command ":"
			e) Press w for write (save)
			f) press q for quit (alternatively to quit without saving steps e) and f) become "q!")

7) (Just for checking) You can now check to see if the file appears in red (which means it is untracked):

		$git status

8) Add the file to commit it. This is a command you must do in order to ready the file to be pushed out:

		$git add gitTutorial.txt

9) (Just for checking) You can now find your file appearing higher, tracked and in green:

		$git status

10) Commiting! You can either write the first command and need to write your comment in an ugly interface, or skip that with the second option:
		
		$git commit 

		or
  
		$git commit -m"Your comment here!"

11) Pushing. Now you push the file to your github (on the master branch)

		$git push origin master
    
		or
    
		$git push origin BRANCHNAME      #(if in a separate branch)

# Creating Branches and Merging them

1) In a cloned repository, write a comand to make a new branch.
		
		$git branch --create MyNewBranch

NOTE: To see this new branch write ... $git branch -l  #The * indicates where you are currently

2) The note will tell you that you are in master; switch branches with "git checkout" command:

		$git checkout MyNewBranch

3) Do steps 5) to 11) mentioned above.
	
4) Checkout to master and Merge with your created branch.

		$git checkout master

		$git merge MyNewBranch

# End Of Tutorial

  Special thanks to Alex (Prof. Haggard's Undergrad), Alex (Prof. Kaspi's Grad), Chitrang (FRB Group) & more.
	Sources: Those mentioned above, the terminal help and github's documentation. 
