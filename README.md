---
tags:
level:
languages:
resources:
---

# Submitting A Lab Osx

You solved the lab, your tests are passing, and now you need to submit a solution. There are two ways to submit a lab:

1. Using the `git` CLI
2. Using the `learn submit` command with the `learn` CLI. **The `learn submit` is the preferred way to submit a lab.**

## Submit a Lab with `git`

With the `git` Learn workflow, you'll need to stage your changes, commit them locally, push them to GitHub, and finally open a Pull Request. You don't need to fully understand everything because if you just execute the commands we describe in order, it'll work. But, let's take a second and briefly talk about what's actually going on when you run `git add .`, `git commit -am `, and `git push`.

### 1. Staging and Commiting Your Solution with `git add` and `git commit`

Remember that `git` was invented to allow developers to create discrete, isolated, yet shareable, versions of their code. That's Version Control. The first step in telling `git` what changes to your code you want to be included as a new version or "commit" is called "Staging".

We might make 100 changes while programming relating to 100 different features or bugs. After we're done coding, we want to isolate each of those different units of work, each different thread of code, each change that fixes something, into separate, organized versions so that the other developers on the team can easily integrate the changes.

If we integrated all 100 updates at once and just 1 of the updates breaks the code, our entire program breaks. Git allows us to craft granular and specific commits and versions by allowing us to explicitly tell `git` what changes we want to add to the next commit. When you "Stage" a change, you're not making a new version yet, you're simply telling Git, "Hey, this change is going to be included in the next version commit". Any change you don't tell git about will still exist, it just won't be considered a new version to git and everyone else on your team until you stage it and commit it.

I can only imagine how confusing that sounds, but really, don't worry about it, the truth is that for work on Learn, there is never an instance where you care about "Staging" vs "Committing". You'll always want to stage all your changes and commit them. Because that's always true, you can just follow the workflow below and it'll just work, even if you don't entirely understand it.

To stage your changes for a commit, we use `git add`. To stage all changes for a commit, you can type `git add .`, which means "Hey, Git, please stage all the new changes in the current directory."

`git add .`

![1](https://dl.dropboxusercontent.com/s/55myv88uo7gu24d/2015-09-30%20at%208.34%20PM.png)

Now that all the changes are staged, you can create a new commit, a new version of the code with your changes, with `git commit`. When we make a commit, we need to provide Git with a message describing the work done. Since you've solved a lab, "Solution" is a great commit message. You can commit all changes with a commit message by using `git commit -am "Message"`.

`git commit -am "My first commit"`

![1](https://dl.dropboxusercontent.com/s/9y3zt153pvaabh0/2015-05-03%20at%209.14%20PM.png)

After this you have a new version of your code in a new git commit on your local copy of the lab. But you got to get your solution code to Learn, how does that work?

### 2: Pushing Your Solution to GitHub

With your commit created, you're now have upload your local code and commits to your fork/copy of the lab, "Origin", on GitHub. We do that with the `git push` command, instructing `git` to take your local changes and upload them to the `origin` remote, which is always your fork, on your GitHub account.

<img width="100%" height="auto" src="http://ironboard-curriculum-content.s3.amazonaws.com/front-end/lab-assets/git-workflow-4.png" alt="Git Workflow 4">

You can think of `git push` as the opposite of `git clone`.

To push your local code to GitHub, just type `git push` in Terminal.

![1](https://dl.dropboxusercontent.com/s/7qta395mpnmst7x/2015-05-03%20at%209.15%20PM.png)

The code you wrote to solve the lab is now up on GitHub, stored on your forked version of the original lab repository.

![1](http://flatiron-videos.s3.amazonaws.com/ironboard/ironboard-tutorial/7-solving-the-lab.png)

We're not done yet, the final step is to tell Learn that you have finished the lab. We do this using a feature of GitHub called a Pull Request.

### Step 3: Submitting Your Solution via a GitHub Pull Request

A Pull Request is a feature of GitHub that allows developers to collaborate on code safely.

#### Pull Requests are Worth Over a Billion Dollars. Here's Why.

Imagine working on a project with 1000s of people across the planet that you've never met. And then imagine that this spontaneous collaboration was all happening at the exact same time, for free, without anyone ever asking anyone to do anything. That's open source software. The Ruby on Rails framework is written by 4,083 people. Linux has had over 12,000 people contribute to the free operating system. Open Source is the entire world working together to build free, superior software. It's magic.

Literally thousands of people that have never met, who share no bond or  common language beyond a love of code, all over the planet, are working together every single second. How is that even possible? How is it not chaos? How are people not breaking things, stepping on each other's toe, doing redundant unneeded work, and just creating a giant unmanageable mess?

The answer to what makes this massively open, spontaneous, free, and world-wide collaboration possible, is GitHub. Specifically, it is GitHub Pull Requests.

Remember that when you work on a project via GitHub the first step is always forking it? When you fork a project, you're creating your own copy so that you can work on it without conflicting with other people. The official project on GitHub is called the "Upstream" remote, it is the code you based your fork or copy on. Your fork or copy is called your "Origin". When you want to integrate changes from your fork/copy to the official project, you create a Pull Request.

<img width="100%" height="auto" src="http://ironboard-curriculum-content.s3.amazonaws.com/front-end/lab-assets/git-workflow-5.png" alt="Git Workflow 5">

A Pull Request on GitHub informs the owners and maintainers of the official project that you want to submit some of your code changes in the form of commits to the official project. The entire world gets to review your changes and manage integrating them in an organized fashion. Through Pull Requests we can make sure that the code that gets added to an open source project is correct and desired. Everyone gets to work but when they want to contribute, Pull Requests give us a chance to vet, discuss, and integrate. At any given point on an open source project, there are literally [hundreds of open Pull Requests](https://github.com/rails/rails/pulls).

Suffice to say, Pull Requests are a powerful social feature that allow the developers to collaborate in an unprecedented scale. The Pull Request workflow is what makes GitHub social. Pull Requests are why GitHub is worth over 2 billion dollars. GitHub Pull Requests are the music of a global software orchestra.

If any of that sounded intimidating, great news, you're not going to be using Pull Requests in that Open Source Workflow because you're not trying to contribute to Open Source yet.

The entire point of our workflow is to prepare you for that - to be in the top 1% percent of developers who contribute to Open Source and make the world a better place through software every single day.

#### Creating a Pull Request to Submit Your Solution

For the purposes of Learn, we only require a GitHub Pull Request as a mechanism to inform Learn that you're done with a lab and you're to submit it, have your solution automatically tested so you get credit for solving the lab, and providing a mechanism for the community to review and comment on your solution.

Here's how to open a Pull Request form GitHub to submit your solution to a lab you've forked and have pushed your solution commit to.

Open your fork by clicking "View" in GitHub from Learn or just opening your forked repo on GitHub directly. From your forked repository on GitHub, click the green Pull Request Button.

<img width="100%" height="auto" src="https://dl.dropboxusercontent.com/s/oj85qs5u079i8ub/2015-10-02%20at%201.14%20AM.png" alt="Ironboard Labs Step 4">

GitHub will prompt you to review the Pull Request before submitting and tell you to "Create Pull Request". Click the green "Create Pull Request" button on the review page. You do not need to review anything on this page and can skip it entirely by just immediately click the "Create Pull Request" button.

<img width="100%" height="auto" src="http://ironboard-curriculum-content.s3.amazonaws.com/front-end/lab-assets/ironboard-labs-step-4e.jpg" alt="Ironboard Labs Step 4e">

GitHub will then again prompt you to describe the Pull Request and you can just skip this and again click the green "Create Pull Request" button.

<img width="100%" height="auto" src="http://ironboard-curriculum-content.s3.amazonaws.com/front-end/lab-assets/ironboard-labs-step-4f.jpg" alt="Ironboard Labs Step 4f">

Once the Pull Request is created, you're done and Learn will update the lesson progress accordingly and allow you to proceed to the next lesson.

![PR](https://dl.dropboxusercontent.com/s/zw5axlrl07e4yj3/2015-10-02%20at%201.25%20AM.png)

### Conclusion of `git` workflow

The `git` CLI workflow might seem tedious and unnecessary to learning to program. People call `git`, GitHub, and Version Control an "incidental complexity" to learning how to code and insist that you can learn to code without ever even needing to learn about `git`, GitHub, or Version Control. We're not sure, but who knows.

What we do know, what we are absolutely sure about, is that there is no way you're ever becoming a professional software developer without `git` and GitHub.

Learn is about teaching you how to be a professional using and embracing professional tools. And our hope is that not only do you learn to code and get a job, but that you become a part of the open source software community and contribute to humanity through code. That's what we're preparing you for, that's why Learn is hard, because we don't just want you to teach you to code, we want you to make the improve the world with your code.

## Submitting a lab with `learn submit`

Every single step described and explained in this README is automated via the Learn CLI that we describe in the next lesson. You can get through every single lesson on Learn without ever interacting with `git`, GitHub, open source, version control, pull requests, commits, or any of these technical details.

We don't force you to learn everything at once, but we also won't ever shy away from telling you about the profoundly powerful tools programmers use to make the world a better place. We took a moment to tell you about `git` and GitHub because those technologies are important. Don't worry if it all didn't make sense, Git is actually hard. After this README, if you choose, you will never have to worry about Git again.

### 1. Submit a lab with `learn submit`

Once you've written the code that solves a lab, and confirmed that your solution is correct using the `learn` command, you then need to submit your solution to Learn so that you can get credit for completion and move on to the next lesson.

In order to submit your solution to Learn, just run:

```
learn submit
```

That's all it takes, you can run `learn submit` from any lab directory and your solution will be submitted to Learn for review.

![learn submit](http://learn-co-videos.s3.amazonaws.com/learn-co-orientation/learn-submit-cli-osx.gif)

You'll notice that on Learn, the light labelled "Pull Request" will turn green when your code has been submitted.

![PR](https://dl.dropboxusercontent.com/s/zw5axlrl07e4yj3/2015-10-02%20at%201.25%20AM.png)

#### What does `learn submit` do?

The `learn submit` and the Learn CLI automate all the low-level `git` interactions. When you type `learn submit`, here's what happens:

1. Your local changes are staged via `git add .` and committed via `git commit -am`.
2. Your local commits are pushed to your fork on GitHub with `git push`
3. A Pull Request from your fork is opened.

## Conclusion

With `learn open` and `learn submit` you are ready to work on Learn. You now know how those commands work and interact with `git`, which is great, but you should feel comfortable not using `git` right now, it's low-level and everything is automated by the `learn` CLI.

**The only two commands you need to know to work on Learn are:**

**1. `learn open` to fork and clone your lab locally so you can work on it.**
**2. `learn test` to run your local tests.**
**3. `learn submit` to submit your solution.**
