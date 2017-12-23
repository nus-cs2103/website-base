<tip-box type="important"> 
  This LO requires coordination and cooperation among team members. It also requires a few days to complete; we recommend that you start it early in the week rather than just before the tutorial day.
</tip-box>

<tip-box type="warning"> 

**Those who failed to produce working code at 1KLoC milestone** (in week 3) can recover the lost marks by doing _two_ enhancements at this milestone.

</tip-box>

<tip-box type="tip">

When working with existing code, a safe approach is to **change the code in very small steps, each resulting in a verifiable change** without breaking the app. For example, when adding a new `sort` command, the first few steps can be,
1. Teach the app to accept a `sort` command but ignore it.
2. Next, teach the app to direct the `sort` command to an existing command e.g. `sort` command simply invokes the `list` command internally.
3. Add a `SortCommand` class but make it simply a copy of the the existing `ListCommand`. Direct the `sort` command to the new `SortCommand`.
4. ...

</tip-box>

<tip-box type="tip">
  
Note that you can reuse the code you write here in your final project, if applicable.
 
</tip-box>

#### Individual component:

**You can omit this individual component if** you have worked with a code base that meets the following criteria:
* more than 2KLoC of the code base was written by other developers
* your code included automated tests
* your code was contributed via a proper revision control workflow e.g. pull requests

**Requirements**: Do an enhancement to [[AddressBook - Level2](https://github.com/nus-cs2103-AY1718S2/addressbook-level2)]  %%e.g. add a new command%%. It can be the same enhancement you did to AddressBook Level1 (at the 1KLoC milestone in week 3). The size of the enhancement does not matter but you must,
* update the User Guide
* update existing tests and add new tests if necessary, for both JUnit tests and I/O tests
* follow the coding standard
* follow the OOP style

Optional but encouraged:
* Update the Developer Guide

<include src="submission.md" />

#### Team component:

The team component is ==to be done by all members==, including those who were allowed to omit the individual component.

* Review PRs created by team members in the _Individual Component_ above %%i.e. add review comments in the PR created against module repo%%. You can either give suggestions to improve, or ask questions to understand, the code written by the team member. 

* **Requirements**: Try to ensure that each PR reviewed by _at least_ one team member and each team member's PR is reviewed by at least one other team member.  

* **Submission**: Just update PR created in the individual component by adding comments/commits to it.
