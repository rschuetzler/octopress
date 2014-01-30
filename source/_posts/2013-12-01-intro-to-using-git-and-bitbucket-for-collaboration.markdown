---
layout: post
title: Why I left Qiqqa for Mendeley
categories: blog
status: publish
type: post
published: true
---
I have been trying for a few years to get my coworkers to work on projects together using Git repositories for version control, and usually to varying levels of success. I finally took the time to hammer out a beginner's guide to collaborating with git, using Github for Windows as the software interface and Bitbucket as the online repo host.\n\nI chose Github for Windows because it's easy to use and it's pretty. Also, it works just as well with Bitbucket repositories as it does with Github repos. I use Bitbucket mostly because it lets me have as many private repos as I need for free. That way if I have information or stats that I don't feel like sharing with the world just yet, I can keep them private.\n\nAs a newbie to Git myself, it was good for me to write these things down so I can understand what's going on a little better. Also, I have never quite found a guide that explained how to actually collaborate in a way that made sense to me. Hopefully this will do the trick.\n\nSo here's the guide. Feel free to use this for your own projects, or to introduce the git workflow to colleagues. I'll probably add to this as I learn more and better understand common problems.\n\n## Setup\n\n1. Download and install Github\n2. Create Bitbucket account\n3. Add Github SSH keys to Bitbucket account\n  1. Log into Bitbucket\n  2. Click your profile picture --> Manage account\n  3. From the left menu, select SSH Keys\n  4. Click the button to Import keys from Github\n4. Clone the bitbucket repository to somewhere on your computer\n  1. Open the Git Shell installed by Github (or another one if you'd rather)\n  2. Navigate Unix-style (cd) to the directory you want the repository to be\n  in. Actually do the directory above that. Git clone will create a directory for the repository. Don't use the shared Dropbox folder. We don't want multiple people committing to the same copy of the repository. That will cause problems.\n  3. Get the URL for the repository from Bitbucket\n  ![Repository URL](http://i.imgur.com/lWycXqt.png)\n  3. Type the command `git clone repoURL [FOLDER NAME]`, replacing [FOLDER NAME] with the name you want to directory to have.\n5. Add the repository to Github by opening the Github program and dragging the folder onto the window.\n6. Boom! You now have copy of the MAVATAR project folder, all gitified and everything.\n\n## Editing stuff\nWorking with version control will be a little bit different from working with files in Dropbox or something. We'll go into the process in depth here.\n\n### Getting started\n\nThe first step to keeping things clean and nice is to create the branch you will be working on.\n\n1. Open Github for Windows and double-click the repository.\n2. Make note of the sync status in the upper-right corner (red box). Also double-check the branch you are current on (blue box).\n![Starting up](http://i.imgur.com/Svaoeyl.png)\n\n3. If your repository is out of date, meaning more updates have been posted to Bitbucket, you will see a blue down arrow next to the sync button. Press sync to pull down all changes.\n![Repo out of date](http://i.imgur.com/nj1WRAG.png)\n\n4. It's definitely best to not do your main work on the Master branch. This will be the definitive version, but while you're working you can keep drafts in another branch to keep things from getting muddled if others are adding stuff. Create a branch by clicking the master button in the top right and entering the name of your branch. You can name it whatever you like, but either your name or the current feature you are working on are good names. Make it something understandable.\n5. Now you're set to work. You should have the most up-to-date stuff from the server, and your own branch to work on.\n\n### Commits while working\nIt is good VC practice to not only commit when you are done working, but in the middle as well. That way if you mess something up you can easily go back to where you were. Here are the steps you can take while you are working on a project.\n\n1. Open the Github program.\n2. Open the repository you are working on.\n3. You will see a list of all files that have changed since you began working. Click the little arrow to the left of the filename to view the changes. Additions are highlighted in green, while deletions are highlighted in red. Changes to a line will show as the deletion of the old version and the addition of the new.\n![Committing](http://i.imgur.com/f8qwB8o.png)\n4. Select the files that you would like to commit. It's best to combine changes that are doing the same thing to one commit, but separate unrelated changes to multiple files into several commits.\n\t1. If you've made a change you want to get rid of, you can discard the changes and revert to the last committed version of the file by right-clicking the file and choosing \"Discard changes.\" Be careful when doing this, as all of your changes to that file will be lost.\n5. Type a commit message in the box on the left. This message should be a short description of the change, written in the imperative (e.g., \"Fix bug\" rather than \"Fixed bug\" or \"Fixes bug.\"\n6. Type a longer description of the change in the box below if necessary. If the change can be summarized with just the commit message, that's fine, but if you're doing anything fancy, be sure to explain the change in the commit\nmessage.\n7. If you want, you can publish your branch to Bitbucket by clicking the Publish button. You can also keep that branch to yourself if you'd rather not share. Since we'll be merging our own changes into Master, there's no need to push things up, but it can be helpful if you want somebody else to look at your branch.  \n\n### Merging branches\nOnce you've finished changing things for this session, it's time to merge your changes into the main branch. Since we all have access to do this in the main branch, we'll go through how to do it here. You'll only want to merge things that are working. If you merge changes to master that give error messages, that's called \"breaking the build,\" and you owe the team lunch. Or something.\n\n1. Make sure all your changes on your own branch have been committed or discarded.\n2. Switch back to the master branch by clicking the branch button in the top right.\n3. Re-sync any changes to the master branch to make sure any changes somebody else has made are synced to your computer.\n4. Open the manage/merge menu from the branches menu.\n\n![Manage merge](http://i.imgur.com/2Iy6UuF.png)\n\n5. Drag your branch to the first box in the \"merge\" area at the bottom.\n6. Drag the master branch to the second box. master should appear in the blue box to the right.\n\n![Merging](http://i.imgur.com/o5NpTt8.png)\n\n7. Click \"merge\" to merge your changes.\n8. Press the sync button to push your changes to the Bitbucket repository so everyone can see them.\n\nWell, that should cover the simplest uses of git, Github, and Bitbucket. If we run into problems as the project progresses, I can update this guide as we figure out how to deal with them. This will be the first time for most of us using Git for any sort of collaboration, so it'll be a learning adventure for all of us.
I love software that makes my life easier. As an academic, I do a lot of
reading. I read a lot (I mean a lot) of PDF articles on a huge variety of
topics. I have a virtual stack of papers that would probably reach half-way to
Phoenix and cost a forest if I printed them all out. Of course I'll never get to
read them all, but just in case.

So as a new student of academia, I started looking for a good way to organize my
files. Surely there must be a better system than storing random PDFs in whatever
nonsensical names their publishers give them in a million places on my hard
drive. That's when I first discovered [Mendeley](http://www.mendeley.com/). It
was a dream come true.

Mendeley is a cross-platform software program for managing research. It can
consolidate files into a single directory, manage metadata for each article,
search the metadata, tag and highlight PDFs, and a whole bunch
more. Additionally it can sync all that data to a BibTeX file for easy inclusion
in a paper. On top of all this, it provides a cloud syncing functionality to
keep your information consistent across devices.

After a few months with Mendeley I discovered
[Qiqqa](http://www.qiqqa.com). Qiqqa was sexy. Qiqqa was newer. Qiqqa had more
features. Qiqqa could highlight with different colors. Qiqqa could OCR my
documents to allow me to search ugly old PDFs. Qiqqa had neat brainstorming
tools (that it turns out I never ever used). The biggest reason I switched is
that I like software that is being actively developed, and Qiqqa was. Mendeley
seemed to have stagnated, with no real new features in the months I'd been using
it. Qiqqa had a new release every month with cool stuff that I could actually
use.

But after spending almost 2 years as a Qiqqa user, I'm switching back. I was a
Qiqqa Premium user for over a year, but when my premium subscription ran out, I
felt it was time to move on. The interface felt too bloated. The features I
loved (like multi-color highlights) were just not enough to keep me there. I
also felt that in the years I'd been using it, Qiqqa had spent more time
developing features I didn't care about and added fewer and fewer things I did.

So I'm back with Mendeley now. UA has purchased a site license to give me extra
storage and a few cool features. It's still not perfect, but it's good enough
for free. In case Mendeley is listening, here are some killer features I want,
in order of awesomeness:

* Get smarter about gathering metadata. I have to correct the data about 75% of
  the time.
* Make a Papers-esque ability to grab BibTeX keys from
  anywhere. Writing a paper in LaTeX and inserting citations could be seamlessly
  integrated with my synced BibTex file.
* Highlights should appear in the notes section
* Qiqqa's hierarchical tags were pretty neat. The ability to
  drill down within a set of tagged documents is a cool feature.