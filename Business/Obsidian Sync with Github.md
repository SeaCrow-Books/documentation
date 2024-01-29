> [!info] 
> This guide is to help sync a local obsidian vault with github. 
> 

- Ensure that you have a github account and it is part of the [SeaCrow-Books](https://github.com/SeaCrow-Books) organisation on GitHub. 
- You make have to ensure your [SSH credentials](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) have been set up. 
- Once this is done you will need to do the following to link up the to repo:
	1. Go into your terminal and add the repo: `git remote add originn https://github.com/SeaCrow-Books/documentation.git`
	2. Then move into the correct branch: `git branch -M main`
	3. Then push: `git push -u origin main`
- Now the next step is to add the 'git' community plugin to Obsidian.
- This should now work, but it can be a bit messy. 
	- You might have to set the custom base path to match your local folder setup.
	- You may find you have a problem with user acceptance, this is the solution - [switching-remote-urls-from-https-to-ssh](https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories#switching-remote-urls-from-https-to-ssh "https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories#switching-remote-urls-from-https-to-ssh")


