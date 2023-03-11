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

```
git remote rename origin upstream
git remote add origin https://github...git
git fetch origin
```

## Workflow
Congratulations! You've successfully forked a repo and modified your local connection to this fork, while still preserving access to the original upstream repo. From here, you can deploy through various hosts. Additionally, you can continue to create branches, update your source code, commit changes, and push updates to your fork. You can further control access and control over your repository to collaborate.

### Branches

### Pushing Upstream

### Collaborating

## Deployment