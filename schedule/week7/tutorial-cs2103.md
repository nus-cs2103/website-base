{% from "common/macros.njk" import thumb, show_as_tab, timing_badge with context %}
{% from "schedule/studentData.njk" import team_review_allocation with context %}
{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(7, "tutorial") }}

#### {{ thumb(1) }} Exercise on Requirements: PR Tracker

* **Divide the team into sub-team** A and sub-team B, 2-3 members each.
* {{ timing_badge("7-8 minutes", "info") }} **Write the answers to the following questions** on the white-board. 

<div class="indented-level2">
<box>

%%{{ icon_info }} Question adapted from a past exam paper.%%

<span class="text-monospace">Pull Request Tracker (PRT) is a desktop application meant to help CS2103 tutors deal with GitHub PRs more efficiently (compared to the GitHub Web interface). For example, it will help tutors find and review PRs from their _mentees_ easily. It will help the _managers_ of the module (e.g., professor, head TA) to easily keep track of how tutors are dealing with mentee PRs. PRT will communicate with GitHub using the GitHub API.</span>

**Sub-team A:**
* Write 2 must-have and 2 nice-to-have user stories, covering user types `tutor` and `manager`.
* Write 2 <tooltip content="Non-Functional Requirements">NFRs</tooltip>, 1 related to performance/scalability, and one related to usability.
* Give 2 terms worth recording in the glossary.

**Sub-team B:**
* Complete the following use case. Give at least one extension. Note that the tutor should give comments in the order of PR size (i.e., give comments to smaller PRs first). Assume the following use cases exists already: `U1. Sort PRs by a criterion`, `U2. Add comments to a PR`

<div class="indented-level2 text-monospace"><blockquote>


System: PRT<br>
Use Case: U3. Add comments to mentee PRs<br> 
Actor: ...<br>
Precondition: ...<br>

...
</blockquote>
</div>

</box>
</div>

* {{ timing_badge("7-8 minutes", "info") }} **Discuss the answers** with the whole team and the tutor

#### {{ thumb(2) }} Review Requirements of a peer team

* **Find the team you have been allocated to discuss** in the panel below and click on the link to locate their team PR.

{% macro get_review_allocation_for_team(reviewing_team) -%}
{%- set reviewed_team = "" -%}
{% for allocation in team_review_allocation  -%}
{% if allocation[0] == reviewing_team %}{% set reviewed_team %}{{ allocation[1] }}{% endset %}{% endif %}
{%- endfor %}{{ reviewed_team }}
{%- endmacro %}

{% macro get_pr_link(team_id) -%}
[{{ team_id }}](https://github.com/nus-cs2103-AY1920S1/addressbook-level3/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Aopen+{{ team_id }})
{%- endmacro  %}

<div class="indented-level2">

<panel header="Team allocation for PR discussion" minimized >

Team          | Discuss PR of | Backup team to discuss
--------------|---------------|-----------------------
{% for team in team_review_allocation  %}
{%- set backup_team %}{{ get_review_allocation_for_team(team[1]) }}{% endset -%}
{{ team[0] }} | {{ get_pr_link(team[1]) }} | {{ get_pr_link(backup_team) }}
{% endfor %}
</panel>
</div>

* **Go to the PR**.
* **Go the to the preview of the Developer Guide** via the Netlify preview link.
  <img src="../../admin/images/prNetlifyPreview.png" />
* {{ timing_badge("7-8 minutes", "info") }} **Read the following sections and make notes** of areas to improve and doubts. To be done collectively with sub-team members.<br>
  %%**If the DG does not have enough content for you to review**, you can review the _backup_ team (see the third column in the allocation panel).%%
  * **Sub-team A:** use cases
    * Is the step numbering correct?
    * Are all possible extensions mentioned?
    * Are there any unnecessary UI details mentioned?
    * Any other formatting/notational errors?
  * **Sub-team B**:
    * User stories
      * Is the user story format correct?
      * All three parts present?
      * Does the benefit match the function?
      * Any important user stories missing?
    * NFRs
      * Are the NFRs are really _Non-Functional_?
      * Is each NFR _well-defined_ (i.e., possible to decide when it has been met)?
      * Is each NFR reasonably achievable?
      * Are more relevant NFRs have been left out?
* {{ timing_badge("7-8 minutes", "info") }} **Discuss with the tutor** and other team members.
* {{ timing_badge("5 minutes", "info") }} **Add a comment** (not a formal review) in the PR to give your comments to the team. Different members can comment about different things.<br>
  {{ icon_tip }} After adding comments, you may want to unsubscribe from the PR to avoid getting GitHub alerts from that PR in the future.
