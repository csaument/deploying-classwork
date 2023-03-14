# Deplying Classwork

## Background
After working with a group or partner to develop a React application on a class repository, the next step is to take that project to deployment. There are many great methods to deployment, with interesting options and decisions to make. This 

## Forking
Most great deployment sites provide direct integration with GitHub. This requires granting the site access to the repo where the application is stored. Applications developed on the LEARN Academy organization do not allow students to grant access to these sites. Instead, students need to create a local version of the application within their own GitHub profile.

Thankfully, students do not need to recreate the entire project within a new repo. Git provides a "forking" to copy an entire repo. The original repo is known as an "upstream," while the copy is known as a "fork." The general workflow will be very much similar to working from the original repo, and additional details can be found in below sections.

The steps for creating a fork are:
1. In a web browser, navigate to the original repo.
1. Click the fork menu button and select "Create a new fork".
1. Select yourself as the owner and click "Create fork".
1. In the forked repo, copy the link provided by GitHub.
1. In the terminal, navigate to the local copy of the original repo.
1. Enter the below commands to modify local settings, replacing the link below with the repo link:

```console
git remote rename origin upstream
git remote add origin https://github...git
git fetch origin
```

## Workflow
Congratulations! You've successfully forked a repo and modified your local connection to this fork, while still preserving access to the original upstream repo. From here, you can deploy through various hosts. Additionally, you can continue to create branches, update your source code, commit changes, and push updates to your fork. You can further control access and control over your repository to collaborate.

### Working on Branches
Working on a fork looks similar to working on the original project. Create a branch, make additions and changes, stage the files, commit changes, push to origin, and create a pull request. For refresher/reference, these commands are listed below. Simply replace the <> content with appropriate information

* Create a new branch
```console
git pull origin main
git checkout -b <branch-name>
```

* Continue working on a branch created by another collaborator
```console
git pull origin main
git fetch origin <branch-name>
git checkout <branch-name>
git pull origin <branch-name>
```

* Submit a PR
```console
git add <filename>
git commit -m "<useful message>"
git push origin <branch-name>
```
1. On a browser, navigate to the repo and create a pull request

### Pushing Upstream
Perhaps you'd like to recommend a new feature or component to the original repo's owner. Maybe you'd like to update the original repo with all of your shiny, new features. Please note that you'll need write access to submit a PR to the upstream.

* Update from Upstream
```console
git checkout main
git fetch upstream
git merge upstream/main
```

* Create a PR on the upstream
1. Navigate to the upstream repo on your browser
1. Click Pull Request
1. Click compare across forks
1. Under base branch, select the desired upstream branch to merge into
1. Under head fork, select the forked branch to merge from
1. Continue to submit your PR as normal

## Collaborating
See below link for GitHub's description of permission levels.

## Deployment

### Deploying with Render

1. Create an account on Render (recommend linking your GitHub account directly)
1. Choose whether to share all or select repos
1. Navigate to the repo on Render's website
1. Click create static site, and follow the default prompts
1. Use the hyperlink provided to access and share your deployed site

### Deploying with Netlify

1. Create an account on Netlify (recommend creating a new team for each project)
1. Provide Netlify with access to your repo
1. ** Pending update **

## Further Reading
* https://docs.github.com/en/get-started/quickstart/fork-a-repo
* https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork
* https://render.com/docs/deploy-create-react-app
* https://www.netlify.com/blog/2016/07/22/deploy-react-apps-in-less-than-30-seconds/
* https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork
* https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/repository-roles-for-an-organization
