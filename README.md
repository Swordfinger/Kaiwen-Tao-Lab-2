# Kaiwen-Tao-Lab-2

The Mythical Man-Month

1.In your own words, summarize the chapter into 3-4 sentences.

  First, when software teams often estimate tasks based on overly optimistic assumptions, perhaps due to their young age, arrogance, and inherent personality traits, and believe that writing code will be simple as long as the ideas are correct, they will set unrealistic deadlines without any buffers or contingency plans. Because duo to optimistic, people always expect the least time they spend for themselves, once inevitable setbacks arise, the entire schedule will collapse. Second, this situation, coupled with the general lack of “courteous stubbornness”, which is lack of a firm defence of experience based assessments among project managers, and the lack of  frequent of rigorous progress tracking and milestone measurement, means that software projects only discover that they are seriously behind schedule when delivery is imminent. As a result, third, the team usually responds by adding more people, but the training and communication costs of new members can further delay the original schedule， also adding more variables to the team, which means adding more possible conflict and problems. Especially in highly sequential or collaborative phases such as debugging and system testing, the idea that “adding people can catch up” is extremely unproductive and can easily lead to a vicious cycle of “adding more people and more delays”. Finally, the commissioning and system testing phase is often severely underestimated, as it actually takes up about half the time. Therefore, to avoid horrible delays, it is necessary to insist on setting aside sufficient time for testing and quality, assess the actual value of additional personnel if necessary, and use small teams or streamlined communication strategies as much as possible, while resisting the urge to blindly compress the schedule.

2. In your opinion, would adding more developers to a project that is running behind schedule be beneficial for the project? Explain your answer in 3-4 sentences, provide an quote from the chapter to support your answer.

   I don't think adding more developers to a project that is behind schedule will benefit the project. First of all, the myth that adding manpower shortens the time spend of a project does not hold true for projects that require a lot of communication, such as software development. The author mentioned that “men and months are interchangeable commodities only when a task can be partitioned among many workers with no communication among them.” It is precisely because a software development project is not like manual labor or other work, a software development project requires a lot of cooperation and communication to build the project, adding more manpower late in the project will lead to a loss of cooperation and cooperative communication, and bringing in new manpower to provide emergency relief requires additional “communication”. The author mentions that “the added burden of communication is made up of two parts, training and intercommunication. Each worker must be trained in the technology, the goals of the effort, the overall strategy, and the plan of work. This training cannot be partitioned, so this part of the added effort varies linearly with the number of workers.” It is precisely for these reasons that simply adding manpower late in the project may do more harm than good, especially when tasks are closely related, also like I mentioned above adding more variables to the team means there is a potential for increased conflict and problems.

3. Think back to a group project or teamwork experience you've had. Did you observe any parallels with the challenges described in "The Mythical Man-Month"? Explain your answer in 3-4 sentences and provide a specific example.

   In high school, I participated in a group presentation on food culture. The group originally had four people, two of whom were my friends. Due to being busy with other courses, we didn't realize until the week before the presentation that we needed to conduct in-depth research and find at least 20 documents. After selecting the topic, we had just worked for three or four days when one member suddenly dropped out of school due to moving, disrupting the original tight schedule. The teacher added two new members, but they already had their own research directions and came from different cultures, which caused division within the group. Consensus was barely reached only one day before the presentation, but because we spent a lot of time introducing our cultures and work, we ultimately did not finish the presentation.

4. Given that "The Mythical Man-Month" was written decades ago, how do you think cultural and technological shifts since then might change or affirm Brooks' assertions? Explain your answer in 3-4 sentences and provide a specific example.

  I believe these problems will gradually decrease over time, because mankind has always moved forward through mistakes and reflection. The author's points about overoptimistic estimates, the “man-month” myth, insufficient testing time, lack of “courteous stubbornness” and weak progress monitoring are all directions for our future improvement and research. We need to find the optimal plan in practice, and with the help of collaboration from all parties and advanced tools, we can set aside enough time for debugging and testing to avoid the burden of “temporary staff increases” later. By continuously accumulating experience, optimizing processes and improving tools, we can make project management more efficient and robust.

5. How do you plan on using the concepts from this book and applying it to your project in this course?

   First, the time allocation strategy mentioned in the article can be referred to at the beginning of the project: 1/3 of the time is used for planning, 1/6 for coding, 1/4 for component testing and early system testing, and 1/4 for final system testing. When scheduling time and personnel, the team members' experience with different programming languages or technical fields and their strengths in modules should be taken into account to ensure a more reasonable distribution of tasks. At the same time, a certain additional buffer time should be reserved at each stage to deal with changes in requirements, unexpected problems or other uncontrollable factors. If some subtasks cannot be split in parallel or require a lot communication, then instead of trying to shorten the schedule by adding manpower, more time should be reserved to avoid the mistake of “adding people = adding progress”. In addition, clear milestones and metrics should be used to continuously and strictly monitor the project schedule – once a milestone delay is detected, timely measures should be taken, adjust priorities, increase testing resources or re-evaluate the scope of tasks, rather than blindly adding people. If additional staff is necessary, they should be brought in at the beginning or at an early stage of the project, with sufficient time allowed for training and integration. Do not wait until the project is already “significantly behind schedule” before temporarily expanding the team. Finally, try to intersperse testing throughout development like continuous integration, continuous testing rather than accumulating it at the end of the project, to avoid a surge in defects shortly before delivery, which can lead to delays and cost spikes.

In your own words, describe the following git commands and provide an example

git checkout:

git checkout can be used to switch between different branches, view, or continue developing the content on each branch.

Example:

  git checkout master

which move the head on the master branch

git checkout can be also used for view code from previous versions or debug

Example:

  git checkout a1b2c3d4

At this point, HEAD is in a “detached HEAD” state, which is you can viewing and debugging. a1b2c3d4 is the hash value of a single commit. Git will restore your working directory to the state it was in when this commit was made. So, you can view old versions of the code or debug.


git revert:
Example: 

  git revert a1b2c3d4

Reversing (undoing) changes made by a commit by creating a new commit. When you run git revert, Git automatically compares the differences between the a1b2c3d4 commits and then creates a new “reverse commit” on the current branch that “offsets” those differences. It does not remove or rewrite the original a1b2c3d4 commit record; it simply adds an additional new commit that indicates “which commit was undone.” The a1b2c3d4 commit is still retained in history, but there is an additional record saying “we undid this commit.”

git reset:

Example:

  git reset a1b2c3d4

When you call git reset, it only moves HEAD and empties the staging area, which means that the staged changes are restored to the unstaged state, but the changes in the working directoryare retained. Both the changes that have been committed and reverted, and the changes that have not been committed and remain in the working directory, will still exist in your local files after this operation, but they have become “unstaged”. At this point, there is still a chance to modify, review, or re-batch submit these files without forcing them to be discarded.

Example:

  git reset a1b2c3d4 --hard

When you call git reset — hard, it will completely move HEAD and at the same time discard the changes in the staging area and the working directory. The working directory will return to the file state corresponding to a1b2c3d4.
