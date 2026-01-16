{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("usingThisWebsite") %}
<div id="main">
<div id="essential">

{{ icon_important_big_red }} The [_Weekly Schedule Page_]({{baseUrl}}/schedule/index.html) is your main source of information for {{ course_pair }}. You will need to refer to it weekly. For an overview of the full semester's schedule, refer to the [Full Timeline](../schedule/timeline.html) page.

{{ icon_info }} More details for the upcoming weeks will be added as the weeks progress. In general, ==information given for more than 1 week into the future should be treated as _tentative_==.

<include src="../book/about/usage.md#browsers" />
{% set icon_layers = ":fas-layer-group:" %}
### Information layers{.text-white .bg-secondary .p-2}

We try to _layer_ information so that readers have the freedom to omit less important layers if they wish to. Some 'layering' techniques used are explained below:

**{{ icon_layers }} More important information are in bold** or ==highlighted== while %%less important information are dimmed%% or in collapsed panels such as the below.

<div class="indented-level2">
<box>

<panel header="Some less important info in a minimized panel" minimized>

Less important info

</panel><p/>

<panel header="%%Some less important info in a boarder-less panel%%" type="seamless">

Less important info

</panel><p/>

<panel header="%%Some less important info in a panel%%">

Less important info

</panel><p/>

</box>

<span id="tip-about-popup-url">You can use the <span class="btn btn-light ps-1 pe-1 pb-0 pt-0 border"><small>:glyphicon-new-window:</small></span> button in a panel to open it as a new tab (it can be expanded in-place too). This feature is available only for panels containing another _full_ page of the website (i.e., not available if the panel contains an _extract_ of a page).</span> e.g.,

<panel header="A panel that can be opened as another tab" popup-url="{{ baseUrl }}/admin/acknowledgements.html">

<include src="acknowledgements.md" />
</panel>
<p/>


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

### Searching for keywords{.text-white .bg-secondary .p-2}

Use the search box in the top navigation bar to search for keywords in the website pages. If you cannot find the content related to a keyword, let us know by posting [in the forum]({{url_forum}}) so that we can add the missing keyword to our search index.

<include src="../book/about/usage.md#saving" />

### Printing Textbook Content{.text-white .bg-secondary .p-2}

**[The Textbook page]({{ baseUrl }}/se-book-adapted/index.html) provides a printer-friendly and a study-friendly version** — omitting non-examinable topics, and limiting to things more relevant to studying for the exam — for each chapter and the whole book %%(indicated by {{icon_print}} icon)%%. You can use them for saving as pdf files or printing.

### Making this Website Better{.text-white .bg-secondary .p-2}

This website was generated using the [MarkBind](https://markbind.org/) software developed at NUS. **We welcome bug reports, suggestions, and contributions**, to be submitted [in the forum]({{url_forum}}).

</div>
</div>

{% endcall %}
