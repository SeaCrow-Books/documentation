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
- This should now work,



git init git commit -m "first commit" git branch -M main git remote add origin [https://github.com/SeaCrow-Books/documentation.git](https://github.com/SeaCrow-Books/documentation.git "https://github.com/SeaCrow-Books/documentation.git") git push -u origin main (edited)