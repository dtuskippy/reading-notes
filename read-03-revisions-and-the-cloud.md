## Revisions and the Cloud Reading Notes  
### Defining Git and GitHub

* Excerpts from [(Git on Wikipedia)](https://en.wikipedia.org/wiki/Git): 

  * *Git is software for tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development.* 

  * *Git was originally authored by Linus Torvalds (Linux founder) in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development.*

* Excerpts from [(GitHub on Wikipedia)](https://en.wikipedia.org/wiki/GitHub): 
  
  * *GitHub, Inc. is a provider of Internet hosting for software development and version control using Git.*
  * *It offers the distributed version control and source code management (SCM) functionality of Git, plus its own features.*
  * *It provides access control and several collaboration features such as bug tracking, feature requests, task management, continuous integration, and wikis for every project.*
  * *Headquartered in California, it has been a subsidiary of Microsoft since 2018.*

### Git and GitHub Workflow
* Click the green “Code” button on the GitHub page of your fork. This will open a dropdown with a link to clone the repository.
* Click HTTPS and copy the link.
* Open your terminal and navigate to the location in your file system where you would like the local repository to be added.
* In your terminal, run the command *git clone url* followed by the HTTPS link. This will create a local copy of the git repository on your machine.
* You can open the local repository in your code editor from the command line using the *code .* command for VS Code
* You can run *git status* to see what files have changed
* Run *git add fileName* to stage all the changes.
* Run *git commit -m 'your commit message'* to commit the staged changes.
* You can run *git log* to see a log of all the commits to this repository.
* You can check the link to the remote repository by running the command *git remote -v*.
* If you would like to push changes to the “origin” remote repository , run the command *git push originRemote*.

### Git online resource
* For simple access to common Git commmands, here is a solid [Git cheat sheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet) from Atlassian.
