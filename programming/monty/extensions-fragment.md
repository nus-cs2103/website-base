## Extensions: Category B

<div id="B-Events">
<include boilerplate src="montyExtensionTitle.md" var-extId="B-Events" var-extStyle="primary"
         var-extHeading="Events"/>

Provide a way for the user to track _events_ (i.e., things with a start time and an end time such as a meeting), in addition to _todo_ and _deadline_ tasks.
</div><hr>
<div id="B-DoAfterTasks">
<include boilerplate src="montyExtensionTitle.md" var-extId="B-DoAfterTasks" var-extStyle="primary"
         var-extHeading="'Do after' tasks"/>

Support the managing of tasks that need to be _done_ after a specific time/task %%e.g., return book after the exam is over%%.
</div><hr>
<div id="B-DoWithinPeriodTasks">
<include boilerplate src="montyExtensionTitle.md" var-extId="B-DoWithinPeriodTasks" var-extStyle="primary"
         var-extHeading="'Do within a period' task"/>

Provide support for managing tasks that need to be done within a certain period %%e.g., collect certificate between Jan 15 and 25th%%.
</div><hr>
<div id="B-FixedDurationTasks">
<include boilerplate src="montyExtensionTitle.md" var-extId="B-FixedDurationTasks" var-extStyle="primary"
         var-extHeading="Unscheduled tasks with a fixed duration"/>

Provide support for managing tasks that takes a fixed amount of time but does not have a fixed start/end time %%e.g., reading the sales report (needs 2 hours)%%.
</div><hr>
<!-- ======================================================================================================= -->

## Extensions: Category C

<div id="C-DetectDuplicates">
<include boilerplate src="montyExtensionTitle.md" var-extId="C-DetectDuplicates" var-extStyle="success"
         var-extHeading="Deal duplicate items"/>

Add the ability to recognize and deal with duplicate items. %%e.g., the same task added multiple times%%.
</div><hr>
<div id="C-FlexibleDataSource">
<include boilerplate src="montyExtensionTitle.md" var-extId="C-FlexibleDataSource" var-extStyle="success"
         var-extHeading="Flexible data source"/>

Provide more flexibility with the data source %%e.g., the ability for the user to specify which file to use as the data source%%.
</div><hr>
<div id="C-DateTimes">
<include boilerplate src="montyExtensionTitle.md" var-extId="C-DateTimes" var-extStyle="success"
         var-extHeading="Meaningful date/times"/>

Make Monty understand the meaning of dates/times attached to a task. e.g., sort deadlines based on their dates/times
</div><hr>

<div id="C-Sort">
<include boilerplate src="montyExtensionTitle.md" var-extId="C-Sort" var-extStyle="success"
         var-extHeading="Sorting items managed by the App"/>

The ability to sort items %%e.g., sort deadlines chronologically%%.
</div>
<div id="C-Search">
<include boilerplate src="montyExtensionTitle.md" var-extId="C-Search" var-extStyle="success"
         var-extHeading="More flexibility in searching for items"/>

Provide the ability to find tasks based on a search criterion %%e.g., find items that contains the provided keyword in their description%%.
</div>
<div id="C-Update">
<include boilerplate src="montyExtensionTitle.md" var-extId="C-Update" var-extStyle="success"
         var-extHeading="Easily edit items"/>

Support a way to easily edit details of items %%e.g., change the deadline date without changing anything else%%.

Minimal: the ability to update an existing item without having to delete it first

Other ideas:
* the ability to _clone_ items (to easily create new items based on existing items)
</div>
<div id="C-Tagging">
<include boilerplate src="montyExtensionTitle.md" var-extId="C-Tagging" var-extStyle="success"
         var-extHeading="Tagging items"/>

Provide a way to tag items %%e.g., tag a task as `#fun`%%.
</div>
<div id="C-Priority">
<include boilerplate src="montyExtensionTitle.md" var-extId="C-Priority" var-extStyle="success"
         var-extHeading="Prioritizing items"/>

Provide a way to attach priorities to items %%e.g., mark an item as a `high` priority (or priority level `1`)%%.
</div>
<div id="C-Archive">
<include boilerplate src="montyExtensionTitle.md" var-extId="C-Archive" var-extStyle="success"
         var-extHeading="Archiving items"/>

Provide a way to _archive_ items so that the user can remove items from the app but still keep a record of them somewhere %%e.g., archive all tasks in the list into a file so that the user can start over with a clean slate%%.
</div>
<div id="C-MassOps">
<include boilerplate src="montyExtensionTitle.md" var-extId="C-MassOps" var-extStyle="success"
         var-extHeading="Mass operations"/>

Provide a way to perform tasks on multiple items %%e.g., delete some specific items in one go%%.
</div>
<div id="C-Statistics">
<include boilerplate src="montyExtensionTitle.md" var-extId="C-Statistics" var-extStyle="success"
         var-extHeading="Statistics and insights"/>

Provide a way to leverage statistics about the items managed by the App %%e.g., show the number of tasks that have been completed in the past week%%. 
</div>
<div id="C-FriendlierSyntax">
<include boilerplate src="montyExtensionTitle.md" var-extId="C-FriendlierSyntax" var-extStyle="success"
         var-extHeading="Friendlier syntax for commands"/>

Make the command syntax more flexible.

Minimal: provide shorter aliases for keywords %%e.g., `t` can be shorter alias for `todo`%%.

Other ideas:
* Allow users to define their own aliases
* Remove the need for the parts of a command to be in a specific order
</div><!-- ======================================================================================================= -->

## Extensions: Category D

<div id="D-Contacts">
<include boilerplate src="montyExtensionTitle.md" var-extId="D-Contacts" var-extStyle="danger"
         var-extHeading="Support managing contacts"/>

Support managing info about contacts %%e.g., details of friends%%
</div>
<div id="D-Notes">
<include boilerplate src="montyExtensionTitle.md" var-extId="D-Notes" var-extStyle="danger"
         var-extHeading="Support managing notes"/>

Support managing info about small snippets of textual information the user wants to record %%e.g., one's own waist size, a name of a movie that the user wants to remember%%
</div>
<div id="D-Expenses">
<include boilerplate src="montyExtensionTitle.md" var-extId="D-Expenses" var-extStyle="danger"
         var-extHeading="Support managing expenses"/>

Support managing info about expenses %%e.g., the amounts spent on food, books, transport, etc.%%
</div>
<div id="D-Loans">
<include boilerplate src="montyExtensionTitle.md" var-extId="D-Loans" var-extStyle="danger"
         var-extHeading="Support managing loan records"/>

Support keeping records of loans given/taken %%e.g., money lent/owed to colleagues/friends%%
</div>
<div id="D-Places">
<include boilerplate src="montyExtensionTitle.md" var-extId="D-Places" var-extStyle="danger"
         var-extHeading="Support managing info about places"/>

Support recording info about places %%e.g., info about restaurants visited, for future reference%%
</div>
<div id="D-Trivia">
<include boilerplate src="montyExtensionTitle.md" var-extId="D-Trivia" var-extStyle="danger"
         var-extHeading="Support managing trivia"/>

Provide the ability to learn/memorize things%%e.g., learn vocabulary, answers to questions%%
</div>
<div id="D-Clients">
<include boilerplate src="montyExtensionTitle.md" var-extId="D-Clients" var-extStyle="danger"
         var-extHeading="Support managing client info"/>

Support managing info about clients %%e.g., for an insurance agent to keep track of clients%%
</div>
<div id="D-Merchandise">
<include boilerplate src="montyExtensionTitle.md" var-extId="D-Merchandise" var-extStyle="danger"
         var-extHeading="Support managing merchandise info"/>

Support managing info about merchandise %%e.g., a property agent to keep track of properties, a collector of stamps keep track of items in the collection%%
</div>
