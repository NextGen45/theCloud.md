## How  are respositories used
respositories are used to organize a single project. Which can contain images and other filies as well.

## cloning repositories 
Well first Git will automatically give the origin name then you clone the  master name to your local branch.

### how to see Your Remotes
 When running the git remote command you will 
be able to  view the short names for example the “origin,”.
when using git remote -v, you can view all the remote URLs next
to their corresponding short names.
 
## Example

$ cd example

$ git remote -v

* remote1 https://github.com/remote1/example (fetch)

* remote1 https://github.com/remote1/example (push)

* remote2 https://github.com/remote2/example (fetch)

* remote2 https://github.com/remote2/example (push)

* remote3 https://github.com/remote3/example (fetch)

* remote3 https://github.com/remote3/example (push)


#### Adding Remotes
To make a new remote Git repository with a short name, use this format
git remote add shortname url

For example:

$ git remote

origin

$ git remote add js https://github.com/janesmith/project1

$ git remote -v

origin https://github.com/johndoe/project1 (fetch)

origin https://github.com/johndoe/project1 (push)

js     https://github.com/Tommy/project1 (fetch)

js     https://github.com/Tommy/project1 (push)


### Fetching
Fetching entails pulling data that you don’t have from a remote project.
Here is the command format
git fetch [remote-name]
Now, you should also possess the references to all branches for that remote (more on branching later).

##### Cloned Repositories
For cloned repositories, use the command git fetch origin to pull down any new changes that were pushed to the server since you cloned or last fetched from it.

git fetch solely pulls new data to a local repository; it does not merge changes with or modify your local work. We will discuss merging in a later section. Later, we will also discuss git pull , which allows for fetching and automatic merging.


##### Pushing
To push your changes “upstream” for sharing, you would use the following git push command format:

git push [remote-name][branch-name]
Example:

$ git push origin master
*This command pushes committed changes from your local “master” branch upstream to the “origin” server.

Note: You can only successfully push changes upstream if you have write access for the server from which you cloned, and if someone else has not pushed changes upstream that you haven’t pulled yet. If a collaborator pushed changes upstream after you had cloned, your push will not be successful. You will have to pull new changes and merge them with your branch before you can successfully push your changes upstream.

Renaming/Removing Remotes
Rename

To rename a remote’s short name, use the git remote rename command.

Example:

$ git remote rename js Tommy

$ git remote

origin

Tommy

For the example above, you can see that the remote’s short name has been changed from js to Tommy. The command git remote lists the existing remotes, which my name is now one of. There is rename action that alters the names of remote branches: js/master would change to Tommy/master.

* Remove

To remove a remote for whatever reason (e.g., a contributor has left the team, the server has moved), simply use the git remote rm command:

For example:

$ git remote rm Tommy

$ git remote

origin
“origin” is simply the default remote name when you use the git clone command.

