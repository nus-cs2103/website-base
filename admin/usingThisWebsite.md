{% macro show_main_text() %} 
<div id="main">
<div id="essential">

# Using this Website

{{ icon_important_big_red }} This _Schedule Page_ is your main source of information for {{ module }}/T. You will need to refer to it weekly. 

{{ icon_info }} More details for the upcoming weeks (and upcoming sections of the textbook) will be added as the weeks progress. In general, ==information given for more than 1 week into the future should be treated as _tentative_==.


:bulb: **For those who don't like the nested-info style used by this website**, we have also provided flat all-in-one versions of the textbook and the admin info.


<include src="../book/about/usage.md#browsers" />
<include src="../book/about/usage.md#layers"/>

</div>
<div id="more">

<include src="../book/about/usage.md#conventions" name="Conventions Used" />

* {{glyphicon_check}} : tasks to do 
* {{glyphicon_blackboard}} : lecture
* {{glyphicon_pencil}} : tutorial 
* {{glyphicon_folder_close}} : evidence you can use to prove you have achieved a learning outcome
* :alarm_clock: : deadline

### Searching for keywords

Use the search box in the top navigation bar to search for keywords in the website pages. If you cannot find the content related to a keyword, let us know by posting [in the website issue tracker]({{module_org}}/website/issues) so that we can add the missing keyword into our search index.

<include src="../book/about/usage.md#saving" />

### Printing Textbook Content

Printer-friendly version %%(indicated by {{glyphicon_print}} icon)%% have been provided for each chapter and the whole book. You can use them for saving as pdf files or printing.

### Making this Website Better

This website was generated using the [MarkBind](https://markbind.github.io/) software developed at NUS. **We welcome bug reports, suggestions, and contributions**, to be submitted [at the website issue tracker]({{module_org}}/website/issues).

</div>
</div>
{% endmacro %} 


{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("usingThisWebsite", show_main_text) }}