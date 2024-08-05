{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("usingThisWebsite") %}
<div id="main">
<div id="essential">

{{ icon_important_big_red }} The [_Weekly Schedule Page_]({{baseUrl}}/schedule/index.html) is your main source of information for {{ course_pair }}. You will need to refer to it weekly. For an overview of the full schedule, refer to the [Full Timeline](../schedule/timeline.html) page.

{{ icon_info }} More details for the upcoming weeks will be added as the weeks progress. In general, ==information given for more than 1 week into the future should be treated as _tentative_==.

<include src="../book/about/usage.md#browsers" />
<include src="../book/about/usage.md#layers"/>

**:fas-layer-group: the ==_topic levels_ system== indicates the progression of contents** from basic/relevant topics to advanced/less-relevant topics. Open the panel below to see more details of that system.

{{ embed_topic("courseExpectations.md#topicLevels", "Admin " + icon_embedding + " Course Expectations → Topic Levels", "usingThisWebsite-topicLevels", indent="1") }}
<p/>

</div>
<div id="more">

<include src="../book/about/usage.md#conventions" name="Conventions Used" />

<div class="indented">

{{ icon_todo }} : tasks to do<br>
{{ icon_lecture }} : lecture/briefing<br>
{{ icon_tutorial }} : tutorial<br>
{{ icon_deadline }} : deadline<br>
</div>

### Searching for keywords{.text-white .bg-dark .p-2}

Use the search box in the top navigation bar to search for keywords in the website pages. If you cannot find the content related to a keyword, let us know by posting [in the forum]({{url_forum}}) so that we can add the missing keyword to our search index.

<include src="../book/about/usage.md#saving" />

### Printing Textbook Content{.text-white .bg-dark .p-2}

A PDF version of the full textbook (<tooltip content="i.e., contains examinable topics only">optimized for exam reference</tooltip>) will be provided at the start of the semester.

In addition, printer-friendly version %%(indicated by {{icon_print}} icon)%% have been provided for each chapter and the whole book. You can use them for saving as pdf files or printing.

### Making this Website Better{.text-white .bg-dark .p-2}

This website was generated using the [MarkBind](https://markbind.org/) software developed at NUS. **We welcome bug reports, suggestions, and contributions**, to be submitted [in the forum]({{url_forum}}).

</div>
</div>

{% endcall %}
