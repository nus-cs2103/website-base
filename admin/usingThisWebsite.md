{% macro show_main_text() %} 
<div id="main">
<div id="essential">

{{ icon_important_big_red }} The {{ schedule_link }} is your main source of information for {{ module_pair }}. You will need to refer to it weekly.

{{ icon_info }} More details for the upcoming weeks will be added as the weeks progress. In general, ==information given for more than 1 week into the future should be treated as _tentative_==.

<include src="../book/about/usage.md#browsers" />
<include src="../book/about/usage.md#layers"/>

This website ==uses a star rating system== to indicate the priority level of contents.

{{ embed_topic("moduleExpectations.md#starRatingSystem", "Admin " + icon_embedding + " Module Expectations → Star Rating System", "usingThisWebsite-starRatingSystem") }}


</div>
<div id="more">

<include src="../book/about/usage.md#conventions" name="Conventions Used" />

<div class="indented">

{{ icon_todo }} : tasks to do<br> 
{{ icon_lecture }} : lecture<br>
{{ icon_tutorial }} : tutorial<br> 
{{ icon_evidence }} : evidence you can use to prove you have achieved a learning outcome<br>
:alarm_clock: : deadline<br>
</div>

### Searching for keywords

Use the search box in the top navigation bar to search for keywords in the website pages. If you cannot find the content related to a keyword, let us know by posting [in the forum]({{forum_link}}) so that we can add the missing keyword to our search index.

<include src="../book/about/usage.md#saving" />

### Printing Textbook Content

Printer-friendly version %%(indicated by {{icon_print}} icon)%% have been provided for each chapter and the whole book. You can use them for saving as pdf files or printing.

### Making this Website Better

This website was generated using the [MarkBind](https://markbind.github.io/) software developed at NUS. **We welcome bug reports, suggestions, and contributions**, to be submitted [at the website issue tracker]({{module_org}}/website/issues).

</div>
</div>
{% endmacro %} 

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("usingThisWebsite", show_main_text) }}