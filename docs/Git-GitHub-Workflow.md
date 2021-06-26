# Git & GitHub Workflow

This page serves the need for new contributors to get started with Git & GitHub. Through this section, we aim and expect the contributors to navigate their way through making contributions to MetaCall. It covers the entire process of contributing right from installing `git` to making contributions through Pull Requests.

Before you move ahead with this guide, we expect you to have a [GitHub](www.github.com) account and have properly installed and configured [Git](http://git-scm.org/) on your local machine. If you have not done them already, please follow these instructions to [setup Git](https://support.atlassian.com/bitbucket-cloud/docs/install-and-set-up-git/) and [make a GitHub Account](https://docs.github.com/en/github/getting-started-with-github/signing-up-for-a-new-github-account) respectively.

## Fork and Clone the Project

In your browser, visit: https://github.com/metacall. Find the apt project that you would like to contribute to and open the appropriate link. In the upper left corner, you will find an option to fork the project. Please click on it to create a fork/copy of the repository on your profile.

- On the terminal of your local machine, clone the repository by running the command where `your-username` represents your GitHub username while the `project-slug` signifies the name of the project you are cloning.

```bash
git clone https://github.com/<your-username>/<project-slug>/
```

For example if you would like to clone the MetaCall's Core library, fork the repository and clone it on your local machine:

```bash
git clone https://github.com/<your-username>/core/
```

- Enter into the newly created project folder by running the following command on your terminal:

```bash
cd <project-slug>
```

For example, to enter into the locally cloned copy of the Core Library you can push:

```bash
cd core
```

- Configure the upstream for your fork so that `git` can sync work from the upstream, if it has been updated by pushing the command:

```bash
git remote add upstream <link_of_original_repository>
```

For example, to configure the upstream for your MetaCall's Core fork, push in the following command:

```bash
git remote add upstream https://github.com/metacall/core/
```

- Check if upstream is configured by running the command and check if the upstream is being displayed:

```bash
git remote -v
```

## Make a Contribution

Before contributing, please check the default branch on GitHub. You can check that out by checking out the main page of the repository and having a look at the branches. For example, the stable branch for MetaCall Core is `develop`. Releases are scheduled periodically when codebase is production-ready and `develop` is merged into `master`. The `develop` branch is the latest updated branch and should be used as a base branch for development. For other projects, `master` branch might be used as a default so we would recommend to check that out before contributing.

Once you are done with finding the default branch, check it out on your local machine:

```bash
git checkout develop
```

You can use `master` instead of `develop`, in case the default branch is `master`. You can now start working on your issue or the task you are assigned to. Add tests and documentation for your changes if required. When you are done with your changes, you can check all the files changes using the following command:

```bash
git status
```

Add the relevant files and commit the changes. Please make sure that only those files required for this contribution are added. You can later modify your pull request to add other files as per your requirement.

```bash
git add <file> <file> ...
```

While committing the changes, make sure your commit message follows a standard commit-message guidelines:

```bash
git commit -m "relevant commit message"
```

Lastly make sure your fork is in sync with the latest changes of the default branch. For this rebase your branch against the latest default branch by following the commands below:

```bash
$ git pull --rebase upstream develop
```

You can use `master` instead of `develop`, in case the default branch is `master`. In case there are any merge conflicts on running the rebase command, follow [this](<(https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-using-the-command-line)>) guide to resolve them.

You can now push your changes onto your feature branch using the command below:

```bash
git push origin <your-branch-name>
```

## Create a Pull Request

You can now create a pull request to get your changes merged into the upstream branch. Follow this step-by-step guide to create a pull request on GitHub.

- Navigate to the pull requests tab under the project you pushed to. Click on the `New Pull Request` button. Compare your feature branch against the default branch to create the pull request. Fill the pull request template by linking the issue number solved, with any additional context.
- In case your pull request is a work in progress, don’t forget to add `WIP` in the title of your pull request to let the maintainers know that the pull request is not ready for review yet. Optionally make the Pull Request a draft.
- Be patient till the time the maintainer reviews your pull request and provide feedback. In case there are changes requested, you can follow the section below on how to update/modify your pull request.
- Also, make sure that your pull request is in sync with the default branch at all times.

## Modify your Pull Request

Incase your pull request needs further changes, you can update your pull request by following the steps below:

- Checkout on your feature branch of the pull request.
- Add the changes as required and commit using the `amend` flag. This will update the last commit thus keeping the commit history clean and within a single commit.

```bash
git add <file1> <file2>
git commit -amend
```

Push this onto your feature branch but this time with `force` flag. This will update the pull request automatically. The reviewer won’t be notified about this updation, so leave a comment in your pull request if you want a review.

```bash
git push origin <your-branch-name> --force
```
