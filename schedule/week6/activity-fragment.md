{% from "common/macros.njk" import button, embed_topic, show_as_tab, show_as_rounded_tab, step, thumb, timing_badge with context %}

<box seamless type="success" icon=":fab-github:" add-class="lead" icon-size="2x">

**This activity teaches you how to merge parallel git branches**,
1. first, in your local repo (using git commands), 
1. and then, in a remote repo (using GitHub PRs).

</box>

<box type="success" icon=":fas-map-signs:" icon-size="2x">

To keep things simple, we use a simple repo that uses two files `food.txt` and `stationary.txt` to keep track of items in the shop. There are 2 shop employees (John and Amy) and two vendors (Ravi and Musa) who have updated the files, but each person using their own branch. Your job is to merge the four branches so that the files reflect the final tally of goods in the shop.

First, let us set up the repo and checkout the branches.
</box>

* {{ step('1.a') }} **Fork the {{ url_module_org }}/shop-inventory** to your Github account.

* {{ step('1.b') }} **Clone it to your computer.** ==No need to set it up in your IDE because it is not a Java project.==

* {{ step('1.c') }} **Note how the remote repo has 4 branches** in addition to the `master` branch. If you can't see the branches, make sure you have ticked the `Show Remote Branches` box %%(shown in the top center of the screenshot below)%%.<br>
  <img src="images/after-cloning.png" /><br>
  Now you are in the `master` branch. Open the `food.txt` file to check its contents.

* {{ step(2) }} **Checkout the `employee-john` branch** by double-clicking it.

<div class="indented-level2">
<panel type="light" header=":fas-play-circle: See an animation of this step" minimized >
<p/>
<pic src="images/checkout-branch.gif"/>
</panel>

Now, you should be in the `employee-john` branch. This also means now you have a local branch named `employee-john` which has the exact content of the remote branch `origin/employee-john` and it is <tooltip content="i.e., git knows that this branch is meant to be a copy of the corresponding remote branch">'tracking' the corresponding remote branch</tooltip>. This is how the revision graph should look like now:
<br>
<pic src="images/after-checking-out-branch.png" width="682"/>
</div>

* {{ step(3) }} **Checkout the other three branches** one at a time to get local copies of them too.<br>
**After that, go back to the `master` branch.** The revision graph should look this this now:<br>
<img src="images/checkout-master-again.png" />

<box type="success" icon=":fas-map-signs:" icon-size="2x">

Next, let us merge the branch created by John.
</box>

* {{ step(4) }} **Merge the `employee-john` branch to the `master` branch**: Right-click on the `employee-john` branch label and choose `merge`. Remember to request a merge commit even if a fast-forward merge is possible.

<div class="indented-level2">

<panel type="light" header=":fas-play-circle: See an animation of this step" minimized >

<pic src="images/merging-branch-employee-john.gif" />
</panel>
<p/>
The revision graph should look like this now:<br>
<img src="images/after-merging-branch-employee-john.png" />
</div>

* {{ step('5.a') }} **Undo the merge**: To learn how to undo a merge, let's undo the merge we did just now.
  * First, ensure that you are still in the branch that received the merge (in this case, that's the `master` branch).
  * Next, right-click on the commit in that branch that is just below the merge commit.
  * Choose `Reset current branch to this commit` and choose the `Hard` option in the next dialog.
  * Proceed with the reset and note how the revision graph is in the state it was before the merge.


<panel type="light" header=":fas-play-circle: See an animation of this step" add-class="d-block pl-5" minimized >

<pic src="images/undo-merge.gif" />
</panel>
<p/>

* {{ step('5.b') }} That was just to practice undoing of a merge. Let's merge the `employee-john` again by re-doing the {{ step('4', step_style='secondary') }} again. The revision tree should look like this again:<br>
  <img src="images/after-merging-branch-employee-john.png" />

<box type="success" icon=":fas-map-signs:" icon-size="2x">

Now that you know how to merge a branch, and undo a merge, let's try to merge Amy's branch. We are going to encounter a dreaded merge conflict this time around.
</box>


* {{ step('6.a') }} **Merge the `employee-amy` branch to the `master` branch**, similar to the previous step. Note how git reports a `merge conflict` halfway into the merge, with a dialog like this:<br>
  <img src="images/merge-conflict-dialog.png" /><br>
  Close the dialog.

<span id="6b">

* {{ step('6.b') }} **Resolve the conflict**: The conflict happened because both branches modified the same location of the same file and git could not decide which changes to keep. The straight-forward way to resolve this is to open the file yourself and manually edit the content to fit the desired state. Given below are the steps:
<div class="indented-level2">

1. When you open the conflicted file `food.txt`, the content will be like this:
   ```
   banana
   <<<<<< HEAD
   carrot
   cheese
   =======
   beans
   >>>>>> employee-amy
   dates
   egg
   fish
   grapes

   ```

1. Note how git has marked the conflicting changes done by the two branches using markers `<<<<<<`, `=======`, and `>>>>>>`
1. We can modify that part in any way we like. For example, we can edit the file to make the content look like this.
   ```
   banana
   cheese
   beans
   dates
   egg
   fish
   grapes

   ```
1. When we are happy with the content of the conflicted file(s), we can simply stage the changes we did and complete the merge by committing the changes %%(similar to how you do a normal commit)%%.

<div class="indented-level2">

<panel type="light" header=":fas-play-circle: See an animation of this step" minimized >

<pic src="images/commit-after-deconflicting.gif" />
</panel>
<p/>
</div>

</div>
</span>

<box type="success" icon=":fas-map-signs:" icon-size="2x">

Good. Now we can handle branch merging in our local repo even if there are merge conflicts. Next, let us find out how to do the same in a remote repo, using GitHub PRs.

But first, let's learn how to create PRs using branches, within the same remote repo.

{{ icon_info }} Creating PRs between branches in the same repo is a way for different team members to propose changes to the code and get the changes reviewed by others.
</box>

* {{ step(7) }} **Push the `master` branch to the fork**, to upload the new merge commits to the fork.<br>
  <img src="images/push-master.png" />

* {{ step(8) }} **Create a PR within your own fork, from the `vendor-ravi` branch to the `master` branch**:
  1. Go to your fork on Github and click on the {{ button('New pull request') }} button.<br><br>
    <img src="images/new-pull-request.png" />
  1. By default, GitHub tries to create a PR from your fork to the upstream repo. Change the base repo to your own fork instead.<br>
     <pic src="images/choose-fork-as-base.png">
  1. Set the `compare` field to the `vendor-ravi` branch.<br>
     <img src="images/choose-vendor-ravi.png" />
  1. Complete the PR creation by filling in appropriate info as directed by GitHub.<br>
     <pic src="images/create-pr-for-vendor-ravi.png" class="border" />
  1. Observe how you have one PR in your own fork now.<br>
     <pic src="images/after-creating-pr-for-vendor-ravi.png" />

* {{ step(9) }} **Create another PR for the `vendor-musa` branch**. As you did in the previous step, create another PR to the `master` branch from the `vendor-musa` branch.

* {{ step(10) }} **Update the PR of `vendor-musa` with reviews and new commits**, to simulate PRs going through a review process.
  1. Add a review to the PR. Here is an example<br>
     <pic src="images/review-pr.png">
  1. In your local repo, switch to the `vendor-musa` branch, add a line at the end of the `stationary.txt` and commit it. This is to simulate a developer updating a PR based on review comments.<br>
     <pic src="images/add-commit-to-vendor-musa.png">
  1. Push the `vendor-musa` to your fork %%to upload the new commit to the fork.%%
  1. Go to the corresponding PR and observe how the PR has updated itself to reflect the new commit you pushed.

<box type="success" icon=":fas-map-signs:" icon-size="2x">

The next step is to learn how to merge PRs, thereby merging the corresponding branch.
</box>
<span id="11">

* {{ step(11) }} **Merge the PR**. Use the GitHub UI to merge the PR you updated in the previous step %%(i.e., the one for the `vendor-musa` branch)%%.
  1. Click on the {{ button('Merge pull requset', button_style="success") }} button (at the bottom of the {{ show_as_rounded_tab('conversation') }} tab)<br>
     <pic src="images/click-merge-button.png" />
  1. Click {{ button('Confirm merge', button_style="success") }} in the next step.<br>
     <pic src="images/confirm-merge.png" />
  1. You should see something like this after the merge is complete:<br>
     <pic src="images/pr-merged.png" /><br>
     Do not click the {{ button('Delete branch') }} button as our scripts will look for the branch in your fork.
</span>

<box type="success" icon=":fas-map-signs:" icon-size="2x">

So far so good. Next, let's learn how to merge PRs when there are merge conflicts.
</box>

* {{ step(12) }} **Observe the other PR is now showing conflicts**: If you go to the `vendor-ravi` PR, it will show something like this at the bottom, indicating that the code in that branch has a conflict with the `master` branch (caused by the other PR we merged just now).<br>
  <img src="images/pr-shows-conflict.png">

* {{ step(13) }} **Resolve the conflict**. Note that GitHub gives a {{ button('Resolve conflicts') }} button that provides a way to resolve conflicts on the Web UI itself. However, that method is more suited for simple conflicts. In this activity, let's use the method that works for even more complicated conflicts.
  1. As the merging the PRs on GitHub updates the `master` branch on the fork only, pull the `master` branch from your fork to your repo to get the latest `master` branch onto your Computer.
  1. Next, merge the local `master` branch to the `vendor-ravi` branch to _sync_ the `vendor-ravi` branch with the latest `master`. This will result in a conflict due to both vendors editing the same location of the `stationary.txt`.
  1. Resolve the conflict, <trigger trigger="click" for="modal:w6activity-6.b">as you did in {{ step('6.b', step_style='secondary') }}</trigger>.
  1. Push the de-conflicted `vendor-ravi` branch to the fork.
  1. Go to the PR again and note the warning about the conflict does not appear any more.

<modal large header="Step 6.b (for reference)" id="modal:w6activity-6.b">
  <include src="activity.mbdf#6b"/>
</modal>

* {{ step(14) }} **Merge the `vendor-ravi` PR** as you merged the previous PR in {{ step('11', step_style='secondary') }}.

<panel header="Step 11 (for reference)" add-class="d-block ml-5" minimized>
<include src="activity.mbdf#11" />
</panel>
<p/>

* {{ step(15) }} **Sync your local repo with the latest `master`** by pulling the `master` branch from your fork. After that, your revision graph should look like this:<br>
  <img src="images/after-pulling-updated-master.png">

<box type="success" icon=":fas-map-signs:" icon-size="2x">

Nice! Now you know how to merge work done in parallel branches.
</box>
