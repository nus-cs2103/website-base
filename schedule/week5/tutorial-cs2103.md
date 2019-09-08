{% from "common/macros.njk" import thumb, show_as_tab with context %}
{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(5, "tutorial") }}

#### {{ thumb(1) }} Discuss iP progress

Quickly update the tutor about your iP progress:
* Has at least one team member managed to set up Travis?
* Has everyone completed `Level-10` (i.e., the GUI) and `A-Gradle`? Any GUIs that went beyond the JavaFx tutorial?
* Anyone has iP increments overdue more than one week?

#### {{ thumb(2) }} Discuss the code quality of iP PRs

<div class="indented">

{{ icon_team }} This activity is to be done as a team. One team member needs to be connected to the TV.
</div>

1. **Locate PRs to discuss**: Go to the [list of Duke PRs]({{ module_org }}/duke/pulls). Locate the PRs (you can filter using `tutorial.*` and `team.*` labels) from the team you are allocated to discuss (given below).

   <panel header="Team allocation for the code quality discussion" minimized >
   
   Team          | Discuss PRs of
   --------------|--------------
   CS2103T-W11-1 | CS2103T-W13-1
   CS2103T-W11-2 | CS2103T-W13-2
   CS2103T-W11-3 | CS2103T-W13-3
   CS2103T-W11-4 | CS2103T-W13-4
   CS2103T-W12-1 | CS2103T-W11-1
   CS2103T-W12-2 | CS2103T-W11-2
   CS2103T-W12-3 | CS2103T-W11-3
   CS2103T-W12-4 | CS2103T-W11-4
   CS2103T-W13-1 | CS2103T-W12-1
   CS2103T-W13-2 | CS2103T-W12-2
   CS2103T-W13-3 | CS2103T-W12-3
   CS2103T-W13-4 | CS2103T-W12-4
   CS2103T-T09-1 | CS2103-T16-3
   CS2103T-T09-2 | CS2103-T16-4
   CS2103T-T09-3 | CS2103T-T17-1
   CS2103T-T09-4 | CS2103T-T17-2
   CS2103T-T10-1 | CS2103T-T09-1
   CS2103T-T10-2 | CS2103T-T09-2
   CS2103T-T10-3 | CS2103T-T09-3
   CS2103T-T10-4 | CS2103T-T09-4
   CS2103T-T11-1 | CS2103T-T10-1
   CS2103-T11-1 | CS2103T-T10-2
   CS2103-T11-2 | CS2103T-T10-3
   CS2103T-T11-2 | CS2103T-T10-4
   CS2103T-T11-3 | CS2103T-T11-1
   CS2103-T11-3 | CS2103-T11-1
   CS2103T-T11-4 | CS2103-T11-2
   CS2103T-T12-1 | CS2103T-T11-2
   CS2103T-T12-2 | CS2103T-T11-3
   CS2103T-T12-3 | CS2103-T11-3
   CS2103T-T12-4 | CS2103T-T11-4
   CS2103T-T13-1 | CS2103T-T12-1
   CS2103T-T13-2 | CS2103T-T12-2
   CS2103T-T13-3 | CS2103T-T12-3
   CS2103T-T13-4 | CS2103T-T12-4
   CS2103-T14-1 | CS2103T-T13-1
   CS2103-T14-2 | CS2103T-T13-2
   CS2103-T14-3 | CS2103T-T13-3
   CS2103-T14-4 | CS2103T-T13-4
   CS2103-T16-1 | CS2103-T14-1
   CS2103-T16-2 | CS2103-T14-2
   CS2103-T16-3 | CS2103-T14-3
   CS2103-T16-4 | CS2103-T14-4
   CS2103T-T17-1 | CS2103-T16-1
   CS2103T-T17-2 | CS2103-T16-2
   CS2103-F09-1 | CS2103T-F14-1
   CS2103-F09-2 | CS2103T-F14-2
   CS2103-F09-3 | CS2103T-F14-3
   CS2103-F09-4 | CS2103T-F14-4
   CS2103-F10-1 | CS2103-F09-1
   CS2103-F10-2 | CS2103-F09-2
   CS2103-F10-3 | CS2103-F09-3
   CS2103T-F11-1 | CS2103-F09-4
   CS2103T-F11-2 | CS2103-F10-1
   CS2103T-F11-3 | CS2103-F10-2
   CS2103T-F11-4 | CS2103-F10-3
   CS2103T-F12-1 | CS2103T-F11-1
   CS2103T-F12-2 | CS2103T-F11-2
   CS2103T-F12-3 | CS2103T-F11-3
   CS2103T-F12-4 | CS2103T-F11-4
   CS2103T-F13-1 | CS2103T-F12-1
   CS2103T-F13-2 | CS2103T-F12-2
   CS2103T-F13-3 | CS2103T-F12-3
   CS2103T-F13-4 | CS2103T-F12-4
   CS2103T-F14-1 | CS2103T-F13-1
   CS2103T-F14-2 | CS2103T-F13-2
   CS2103T-F14-3 | CS2103T-F13-3
   CS2103T-F14-4 | CS2103T-F13-4
   </panel>
   <p/>

1. **Pick a PR to review.** When choosing, give priority to PRs with fewer comments.
1. **Discuss code quality** Go through the code, and discuss the code quality of the PR. Example aspects to consider:
   * abstraction: SLAP, arrow-head style code, too-long methods, too-deep nesting
   * comments: missing comments, redundant comments
   * magic literals
   * hard-to-understand code
   * coding standard violations
   * class/method/variable naming
1. **Add comments**: If the team agrees that the code quality of a specific piece of code should be improved some way, add a comment (team members can take turns on adding comments).<br/>
   If you are unsure about a case, you can also rope the tutor in to the discussion.
1. **Repeat for other PRs**: Spend ==no more than 10 minutes on one PR==. When you reach 10 minutes, move to another PR.<br/>
   Discuss ==at least 2 PRs==.

<div class="indented">

{{ icon_tip }} After the tutorial, you can apply the insights gained from this activity to **improve the code quality of your own iP**, if necessary.
</div>

#### {{ thumb(3) }} Prioritize tP user stories

* Show your list of tP user stories to the tutor %%(for progress tracking)%%.
* If you haven't done so already, prioritize tP user stories as explained in the [{{ show_as_tab('Project', icon_project) }}](project.html#2-prioritize-the-user-stories-before-or-during-the-tutorial).

