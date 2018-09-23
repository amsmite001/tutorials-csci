# Introduction
This document goes over how to use Git commands, and will aid in understanding the basic workflow process. This includes:
* [Overall View of Workflow](#H1)
* [Review of Cloning](#H2)
* [Adding, Committing, and Pushing](#H3)

---
## <a name = "H1"></a>Workflow
A basic representation of Git's workflow is as pictured:
![Basic flow of Git](gitBasicFlow.jpg)

In the previous tutorial, we walked through the first two steps: How to create a repository and how to clone it to your computer. The next step is to work on the files you cloned. This may include making new files or editing the ones that already exist. Github and Bitbucket act like secondary save points that multiple people can access. In a way, it's like OneDrive or Dropbox. So it makes sense that after you finish working for the day, you want to push your changes _upstream_.

<b>_Upstream?_</b> When we talk about upstream, we mean that we're going to push all of our changes into Bitbucket - the top of the stream. That leads us into the next point - what entails pushing upstream?

Add, commit, and push - in that order - are how you push changes to your __local__ repository up to Bitbucket/Github. I'll discuss how to do so in commandline in the next few sections. After pushing your changes, you're free to start working again. __Just make sure that every once in a while you push your changes!__

Why would we want to use this workflow process?
* __Save Rollbacks:__ If you make a change to your code that entirely breaks it, with little hope of saving it, Bitbucket/Github makes it posssible to roll your code back to the any of the last versions that you pushed upstream.

* __Progress Tracking__ Github and Bitbucket provide time stamps, and other information about the code you push to the repo. Time stamps makes grading easier for professors, as they can look at the last, on-time version of code that you added. You can also see your own stats, as well as any group members.

* __Offsite Saving__ Repos are like Dropbox or OneDrive - they can save your files for you, safely. No more of the "my computer crashed and deleted everything excuse"
    * If you're wanting to use that excuse, maybe you shouldn't use this?

---
## <a name = "H2"></a> Review of Cloning



---
## <a name = "H3"></a> Adding, Committing, and Pushing

