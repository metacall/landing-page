# Contribution to MetaCall

MetaCall is an open and accessible community aimed towards getting people started with the various open-source projects under MetaCall. This page serves the need of a Contributor Documentation and aims to serve as a starting point for contributors to get started. As an emerging open-source community, we have a plethora of work that we need to do and complete, and it is not just limited to code. As a Contributor, you can work on writing examples, review the code, suggest improvements, contribute to documentation and much more. In this page we will outline the specific path on what you can do to help.

## What skills are needed?

MetaCall is a large open-source organization and we have a large number of projects looking for some contributions. We are thrilled to host contributors from all walks of life in helping us with various avenues of contributions forming a diverse skill-set required.

Here is a table that would help you to find out the currently available projects to contribute to, along with the skills needed and a specific link to their contribution guide:

| Project       | Skills                                       | Repository                                                          | Documentation                         |
| ------------- | -------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------- |
| core          | C, C++, Python, Javascript, Typescript, Ruby | [metacall/core](https://github.com/metacall/core)                   | [docs](docs.md)                       |
| upload        | Typescript, Javascript                       | [metacall/upload](upload)                                           | [upload](upload.md)                   |
| install       | BASH                                         | [metacall/install](https://github.com/metacall/install)             | [install](install.md)                 |
| dlang-port    | D                                            | [metacall/dlang-port](https://github.com/metacall/dlang-port)       | [dlang-port](dlang-port.md)           |
| php-port      | PHP                                          | [metacall/php-port](https://github.com/metacall/php-port)           | [php-port](php-port.md)               |
| cli           | Docker                                       | [metacall/cli](https://github.com/metacall/cli)                     | [cli](cli.md)                         |
| guix          | Docker, BASH                                 | [metacall/guix](https://github.com/metacall/guix)                   | [guix](guix.md)                       |
| distributable | Scheme, Docker, C                            | [metacall/distributable](https://github.com/metacall/distributable) | [distributable](distributable.md)     |
| scala-port    | Scala                                        | [metacall/scala-port](https://github.com/metacall/scala-port)       | [scala-port](scala-port.md)           |
| get-started   | Markdown                                     | [metacall/get-started](https://github.com/metacall/get-started)     | [Getting Started](getting-started.md) |

There are multiple ways through which you can contribute, even without knowing programming or technical writing. If you plan to get involved with user experience, support, translation or anything else that sparks your interest, do consider reaching us out on our [community channels](/community).

## Landing your first contribution

Now that you know the project that you can contribute to, how exactly can you land your first contribution? This section highlights our recommended workflow through which you can land your first contribution. We assume that you have already setup the project on your local machine by following up the official documentation. If you are stuck, do reach out one of the maintainers to help you out in the process.

Our Contribution Workflow is very straightforward and follows an Issue-Pull Request workflow. The contributors need to fork the repository for having their contributions landed on the project. If you are looking to contribute, we have laid down a series of steps that we would like you to follow:

### Find an Issue to work on

The literal start for any contributor in an open-source project is to find something to start with. We would recommend you to go through the **Issues** section of the project that you are looking to contribute to and find some unassigned issues. If an issue is already assigned to someone, we would recommend you to skip that up because it is already a work under progress. If no substantial updates have been made, you can request the assignee to know what part of the issue is completed.

If you are not able to find any substantial thing to work on, we would recommend you to explore. Exploring a project is beneficial for some of the following reasons:

- You can understand and identify the gaps in the code and documentation.
- You can understand the code formatting, stylistic principles and comment format that is being followed.
- You can test the code and the project on your local machine and see if everything is running alright.

Exploring the above along with the Issues and Pull Requests, will give you a great idea on how the Issue-PR workflow goes and how you can integrate your contributions into the same. Once you have found something to work on, you can either request for the Issue to be assigned to you (if someone else has created the Issue) or you can make your own.

Making your first Issue is a holistic experience. It is because making an Issue comes with a huge amount of research that you have done prior and the specific contribution that you are planning to make. To ensure that the issue is received positively by the maintainers make sure of the following:

- If you are filling a Bug report, make sure that the Issue template is properly filled up with all the information that the maintainer needs to understand the problem at hand.
- If you are filling a feature request, make sure you pitch in your idea well and it should be constructive in nature and add some positive value to the project.
- Before making an Issue, make sure that the Issue you have has not been already created or is being worked on by someone else.

### Landing your Pull Request

Every Pull Request should have a corresponding Issue, unless and until it’s for a very minor fix. Making a Pull Request is a great experience, but requires specific insights to land up your code on the repository for the very first time. To make sure you land a great contribution, we would request you to follow the our [Git and GitHub workflow](Git-GitHub-Workflow.md) to know about code collaboration with GitHub. If you are not already familiar with Git, we would suggest you to follow the [official Git documentation](https://git-scm.com/doc) to have the basic understanding of the same.

Once you have made all the changes corresponding to the Issue you are supposed to work on, please make a commit. Once you have made a commit, go ahead and make a Pull Request. The Pull Request template gives you enough information but here are a few things that you are expected to follow:

- Every Pull Request should have the Issue linked to it.
- Pull Requests undergo an automated check by CI toolings. If the checks are failing, we would recommend you to open it up and find the error.
- You can keep your PR as a Draft if you are still working on it. Once your work has finished, feel free to mention us so that we can review it.
- Every Pull Request should be as atomic as possible. Once the review is complete, we will ask to squash the commits before merging it.

If the Pull Request that you made has run into Merge Conflicts, we would recommend you to solve them on your own. Merge Conflicts can be either solved from the Github Web User-Interface or from the Command Line. Here is a [great piece of documentation](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-using-the-command-line) to do it through the Command Line.

## Reviewing Pull Requests

Now that you have landed your PR and it is ready to review, one of the maintainers will review it and provide an actionable feedback for you to improve on. Once you have made a Pull Request, expect a maintainer to follow up within a day or two. Don't hesitate to contact the maintainers on the community channels as well if this isn't moving. While the Pull Request is being reviewed, make sure that the following requirements are satisfied:

- The Code is complete and satisfies the requirements laid out on the Issue. Incomplete Pull Requests would be marked as draft and we would request you to further work on the same.
- The Code should follow the standard style guidelines laid out on the project documentation. If you are unsure about the same, ask the maintainers during the PR reviews.
- The Code should pass all the checks and test cases laid out. If you are contributing some new code which forms a substantial part of the project, make sure to add tests for easy understanding and review.
- The Code should be self-explanatory with proper comments added on areas that are hard to understand and review.

Maintainers expect the comments to be resolved once a review has been completed. Providing updates on how far have the comments been resolved helps us with an easy understanding of the areas that the contributor needs help with. Every Review Comment would be directed towards a change or a question. Once the change or the question has been addressed, we will expect it to be resolved.

Once the Pull Request has been reviewed and approved, we would like all the commits to be squashed into one single atomic commit before we officially merge it. If you are stuck with anything or everything, and something doesn’t make sense, feel free to shoot us a mention on Github or drop us a message on our communication channels.

## Repeat the Process

Once the Pull Request has been reviewed and merged, you have made MetaCall open-source stronger than before. And we would like you to celebrate this success and further prompt you to become a MetaCall contributor.

Go back to the first step and repeat the process all over again. The maintainers might suggest a new bug, feature request or an update required, where your skills can come handy. The contributions should flow freely and you can make an Issue, take up an existing Issue, have a Pull Request and land your contributions. We are also on the hunt for new ideas and methodologies that would make the project more diverse and easy to contribute.

We have a plethora of places where we can improve and work on. Feel free to suggest anything that can help us make our projects better, more inclusive and bring forward a positive impact to our community. We are also participating in Open-Source mentorship programs, like [Google Summer of Code](https://summerofcode.withgoogle.com/organizations/5830976665550848/) which is a great start for new contributors to receive specific mentorship while working on a project that is valuable to the organization.
