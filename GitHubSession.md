# GitHub 
#### A Version Control System 

----

##### Basic History : 

Linus Torvalds developed the GIT : the HEART of GitHub Website .
While developing the Linux Project ,version controller was required for managing the project well!

##### Why GitHub ?

* distributed version control 
* source code management functionality 
* provides access control and collaboration features such as bug tracking, feature requests

-----

#### Some Features :

##### Repository :
        
        * similar to a folder ; assume it to be just like a drive on your PC.
        * you must always provide description : brief : for your repo
        * Controls possible : public/private (as the name suggest public is visible to all and Private is visible to only us.)
        * Private repos are possible 
          ** after paying
          ** For students: You can have GitHub Student Developer Pack (Use your Id card and the subsrciption last for 2 years.
          ** Link : https://education.github.com/pack
          
##### Fork :

        * Its functionality is similar to Copying.
        * Fork the projects you find useful for yourself and the repo would appear in your repo list for wheneer you might want to have a look.
        
##### Branch :

        * branches as the name suggest .. they are part of the same tree/ project 
        * you can have a main branch containing the original code and create new branches to add new features with newer features
        * for synching the same project 
        * introducing changes to some official code 
        * Source Tree Jargon : checkout : means you are working on this branch 

##### Pull Request :

        * This is the feature which allows us to point out changes to a project , we can "pull a request" in someone's or our repo to suggest a change.
        * Pull Request can be created by two methods: 
               ** Using Fork :
               Basically you can perform a fork , and the repo (someone else's) appear in your repo list 
               You now can generate changes in that repo and click on the pull request button to suggest the owner some changes.                
               ** Using Branch :
               This is for your own use , create branches of your own repo , once the new features added are compatible and fully final you can pull a reuqest from the new branch on the master branch , to "merge"(we will discuss this how) the changes .
               
##### Merge Pull Request :
        
        * This is in coalition with Pull Request.
        * When someone sends in a Pull Request then a 1 appear in the bar above , click there and you can review what changes have been suggested and you can also reject/merge the changes
        * Merged Changes appear in the repo thereafter.
        

----

#### Some Jargons Related to GitHub :

##### Sourcetree/Git Client :

        * these are two software.
        * you can have either of them ,both are equivalent.
        * Why to have them ?
                ** simple answer : you can handle your github from your pc 
                ** management of your repos is much easier using the software

##### Clone :

        * a local copy of GitHub repo
        * cloned copy resides on your pc and any changes made can be pushed to / pulled from repo.
        * you can create repo using terminal : git clone [url]
        

##### Commit ( in the Source Tree Software ) :

        * made a file in clone -> save this to vcs ( version control system )
        * commit msg : a desc of what changes i made , 70 to 80 words 
        * you want to ignore a file while commiting data to GitHub Repo ,in the software, use the three dots to ignore the file to avail the option (this is the case when u forgot have a gitignore file in repo)
        
##### Push ( in the Source Tree Software )/A Commit on GitHub Website :

        * to GitHub (the original account) 
        * it gives an ssh  for your commit

###### Main Difference between : push is reflected in the GitHub Account and a commit is only intimation for the GitHub Version Controller to save the changes , Several Commit can be pushed altogether.

----

##### Two Special files : 
        
        * MarkDown :.md:
                ** ReadME.md : you should always initialize a repo with a read me, which briefly and beautifully describes your repo ! 
                
        -> MD files are written in : mark down lang
        -> gives an info abt your repo/or whatever other description (eg: a cheatsheet) you want to add
        -> an md file is much similar to decorating your file 
        -> good eg : alamofire 
        -> use a markdown cheat sheet 
        ->  you can search : https://guides.github.com


        * .gitignore :
        -> when our code is built , besides .xyz (Let xyz- be the extension of the file ) no other file should be uploaded
        -> you can utilize the feature so as to protect some imp files which can be saved on clone but wont be pushed to GitHub
        -> they are “ignored” by GitHub

----

#### Tips:

        %%% GitHub cheat sheet %%%
        
                https://services.github.com
                make a cheat sheet in repo : how i run my program
        
        ----
        
        %%% Grp Project %%% 
       
        Let Three people X, Y, Z be working together on a project.
        X : Creates a repo 
        
                Method 1 :
                Y and Z both push to this same repo

                Method 2:
                Y and Z perform fork 
                {
                Fork
                Clone that repo in your local pc 
                Work
                Pull Request
                X merges if Ok
                }

        ----
        
        %%% Some Courses on GitHub or Help Available online %%%
        
                https://help.github.com
                https://in.udacity.com/course/how-to-use-git-and-github--ud775
                https://www.codecademy.com/learn/learn-git


Working :

local pc ->(commit)-> central version control system ->(push)->GitHub server 
commit -> made a change in local given to vcs
push -> to server 




6 -7 hrs git course 
learn git
from code academy




