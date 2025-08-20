TLDR; you will not be able to contribute PRs to the repos of two different students as you will not be able to fork two different student repos UNLESS you create another GitHub username you can use for that second fork (or if you already have another organization you belong to). Otherwise, you will see the message "No available destinations to fork this repo"

Why?

A fork is a copy of a given repo. GitHub does not allow having two copies of the same repo (or their forks) under the same account/organization.

The way GitHub Classroom does things is that it creates students’ repos by forking the starter repo I created.

Let's assume I'm a student

classorg/snadirepo —fork of—> classorg/starterrepo

Now, I will go and try to fork my colleague Bob's repo, which is called classorg/bobrepo. Because bobrerpo is a fork of classorg/starterrepo and I already have a fork of classorg/starterrepo in classorg, it will only allow me to create the fork in my personal account so something like snadi/bobrepo.

Now, let's say there's another student Alice whose repo I want to contribute to. When I come to create a fork of Alice, there are no accounts left for me to create a fork in.

So my only choice to help out Alice is to create another GitHub account and fork it there (or if I'm part of another organization).
