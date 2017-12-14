# GitHub 
#### A Version Control System 

----

##### Basic History : 

Linus Torvalds developed the GIT : the HEART of GitHub Website .
While developing the Linux Project , needed a version controller for managing the project well!

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
               
               

Working :

local pc ->(commit)-> central version control system ->(push)->GitHub server 
commit -> made a change in local given to vcs
push -> to server 


Two imp /special files :
meant for GitHub repo

readme.md : md :
-> mark down lang
-> gives an info abt your repo
-> an md file is much similar to decorating your file 
good eg : alamofire 
{
markdown cheat sheet
guides.github.com
}

.gitignore :
->when our code is built , eg besides .cpp  no other file should be uploaded
-> some imp files can be saved on local copy but wont be pushed to GitHub
they are “ignored” bu GitHub


%%% GitHub cheat sheet %%%

services.github.com
 make a cheat sheet in repo 
how i run my program

{
python :

pip allows u to install public libraries
pip —version
python —version
}

JARGONS RELATED TO GITHUB :

Sourcetree / Git Client - both are equivalent 

Clone :
a local copy of GitHub repo
creating repo using terminal :
git clone [url]




Commit :
made a file in clone -> save this to vcs 
commit msg : a desc of what changes i made , 70 to 80 words
{ use the three dots to ignore the file }
 
Push :
to GitHub 
it gives an ssh  for your commit

 Pull Request :


Grp Project :

{ NILOY AVIRAL AYUSH }
AVIRAL : Creates a repo 
method 1 :
nil and ayush both push to this same repo

meths 2:
nilu and aayush perform fork 
{
Fork :
i want your folder in my repo collection
clone that repo in your local pc 
to work
}


rebase 
merge
push 

clone

6 -7 hrs git course 
learn git
from code academy




