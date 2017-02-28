---
layout: post
title: "Introduction to Git and GitHub - Part II"
description: "Introduction to Branches in Git"
tags: ["Git","GitHub"]
---

* A lot of times it is difficult to manage using Version Control when there are more than one contributors in a particular repository! At such times it is important to a particular feature of Git called **branch** <br><br>
* The error caused due to such is known as **Merge Conflicts** and often solving Merge conflicts is tedious and often results in information being lost as a result.

##### What are branches and how to use them?

* Branches are basically used when multiple people want on different parts in the same projects.<br><br>
* The default branch in a GitHub repository is called __master__. To create a new branch you need to execute the following command:

{% highlight git %}
git checkout -b <branch_name>
Switched to a new branch 'salman'
{% endhighlight %}

* In case you are looking to switch back to your __master__ branch on your local repository, type in the following commands to get back again:
{% highlight git %}
git checkout master
git checkout <branch_name>
{% endhighlight %}
<br>
* If you are looking to delete a branch first **make sure you aren't currently on that branch**! Use `git checkout` to move to another branch and then use the following commands to delete the branch.
{% highlight git %}
git branch -d <branch_name>
{% endhighlight %}
<br>
* In case your branch is not being deleted because you have certain unmerged changes and you really want to delete them without merging your changes, you can use the following instructions!
{% highlight git %}
git branch -D <branch_name>
{% endhighlight %}

![git branch commands]({{ site.baseurl }}/images/post20.png)

##### How to sync your branch with the Master branch
* If you are looking to sync your branch as in update the online changes that someone else has made to the __master__ branch to your branch, put in the following commands:
{% highlight git %}
git pull origin master
{% endhighlight %}

* P.S. This can be extended to all branches and isn't restricted to the __master__ branch alone!<br>

{% highlight git %}
git pull origin <branch_name>
{% endhighlight %}


##### How to push branches on GitHub

* You can now start working on the same set of files without worrying about any Merge Conflicts.
* After you're done working on them use the following commands to push your new branch on to GitHub.

{% highlight git %}
git add --all
git commit -m "<your_message>"
git push origin <branch_name>
{% endhighlight %}
<br>