{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(3, "tutorial") }}

**{{ module }} students only**: 
* Form teams at the beginning of the tutorial. See the panel below for _team forming constrains_ and other related info.<br>
  <panel src="../../admin/project-teams.md#main" header="Admin {{ icon_embedding }} Team Forming :star:" minimized />
* Get your team ID from the tutor and submit it via the LumiNUS poll. Note the ==team ID follows <trigger trigger="click" for="modal:t2-teamId">a specific format</trigger>==.

<modal large title="Admin {{ icon_embedding }} Team Forming → Team ID format" id="modal:t2-teamId">
  <include src="../../admin/project-teams.md#teamIdFormat"/>
</modal>
