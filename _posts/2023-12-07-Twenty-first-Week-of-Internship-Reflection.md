---
layout: post
title: "Enhancing Deployment Workflows with Rsync and Git Tagging"
author: mtrinidad
categories: 
- internship
image: assets/images/mtrinidad-week21.png
---
During my 21st week of internship, I focused on enhancing the deployment workflows for both my Jekyll and Laravel projects. The aim was to simplify processes and introduce automation. Here's a breakdown of my efforts:

--- 
## Rsync for Jekyll Deployment

### Syncing Jekyll Updates

I started by enhancing the deployment of my Jekyll project. Initially, I manually used rsync to sync files to my subdomain after each update and build. This became cumbersome, so I automated the process. Our mentor advised us to deploy our Jekyll project to our subdomain instead of just relying on GitHub Pages. The goal was to have both our Jekyll and Laravel projects running together on the same subdomain. Essentially, two projects coexist in one subdomain.

### GitHub Action for Rsync

I discovered a GitHub Action for rsync, a tool that syncs files and directories. I integrated this action into my Jekyll's build job.

```
        # Sync the _site directory to the shared hosting specified directory
      - name: Deploy to Ronins Server using Rsync
        uses: burnett01/rsync-deployments@6.0.0
        with:
          switches: -avziO
          path: _site/
          remote_path: ${{ secrets.REMOTE_DEPLOYMENT_DIR }}
          remote_host: ${{ secrets.REMOTE_HOST }}
          remote_user: ${{ secrets.REMOTE_USER }}
          remote_key: ${{ secrets.SSH_PRIVATE_KEY_MC }}
```

At first, I used rsync to sync files from my computer to a directory on my subdomain called `public/miguel_blog`. I created this directory because my Jekyll project's base URL is `miguel_blog`. Even though I used rsync to update files, it felt a bit inconvenient. I thought, "Why not automate this?" So, I added it to my Jekyll's deployment process. Luckily, I found a helpful tool on GitHub called rsync. I added the rsync step to my build job because this build job creates the `_site` folder, which is the output of my Jekyll project. Then, rsync copies the `_site` folder to the subdomain directory named after Jekyll's base URL. What's great about rsync is that it's smart, it doesn't copy everything; it only transfers the changes, not the whole directory. Now, I've got two projects running on my subdomain. Cool, right?


---
## Modifying Laravel's Deployment Workflow

### Git Tagging for Versioning

For my Laravel project, I changed the deployment workflow by adopting Git tagging for versioning. Instead of pulling changes from a specific branch, I embraced the more organized and efficient approach of using Git tags.

### Automated Release Creation

I automated the creation of releases for both projects. When a tag is pushed to the GitHub repo, a GitHub Actions workflow kicks in, creating a release. This not only simplifies version management but also streamlines the deployment process. But it doesn't stop there, there's another workflow that runs when a new release is created. This is my deployment workflow. It checks for a new release and, if there is one, it deploys the app. Simple and efficient.

Additionally, I modified the deployment workflow to execute only when there were new releases. Embracing automation not only saves time but also ensures a more controlled and error-resistant deployment process. This experience reinforced the importance of leveraging tools like GitHub Actions for simplifying and enhancing our development workflows.

### Tag-Based Deployment

To align with the Git tagging strategy, I created a deployment script for my Laravel project in my subdomain. The script fetches the latest tags from the repository, identifies the most recent tag, and checks out to that tag. 

```
#Add ssh private key to ssh-agent.
eval "$(ssh-agent)" && ssh-add ~/.ssh/sample-private-key

#Fetch latest tags from remote repo.
git fetch --tags

#Get latest tag and store in a variable.
latestTag=$(git describe --tags `git rev-list --tags --max-count=1`)

#Checkout the latest tag.
git checkout $latestTag
```

---
## To wrap things up
These enhancements in deployment workflows not only save time but also improve the organization and version control of my projects. The integration of rsync and Git tagging brings efficiency and simplicity to the deployment process, allowing for smoother collaboration and updates.