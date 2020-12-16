{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("standardsAndConventions") %}
<div id="main">

Given below are the standards and conventions to follow in this module.

<span tags="m--cs2103 m--tic4002">

##### Java

* {{ required }} Follow the ==_basic_ and _intermediate_ rules== in the [SE-EDU Java coding standard](https://se-education.org/guides/conventions/java/intermediate.html).
* {{ optional }} Follow [advanced rules](https://se-education.org/guides/conventions/java/index.html).

</span>

<span tags="m--cs2113 m--tic4001 m--tic2002">

##### Java

* {{ required }} Follow the ==_basic_ rules== in the [SE-EDU Java coding standard](https://se-education.org/guides/conventions/java/basic.html).
* {{ optional }} Follow [intermediate and advanced rules](https://se-education.org/guides/conventions/java/index.html).

</span>
<span tags="m--cs2103 m--cs2113 m--tic4001 m--tic4002">

##### Git

* {{ required }} Follow the Git ==commit message _subject_ conventions== in the [SE-EDU Git conventions](https://se-education.org/guides/conventions/git.html).
* {{ optional }} Follow conventions for the commit message body.

</span>
<span tags="m--cs2103 m--cs2113 m--tic4001 m--tic4002">

##### Markdown

* {{ optional }}  Follow [Markdown style guide at SE-EDU](https://se-education.org/guides/conventions/markdown.html).

</span>
<span tags="m--cs2103 m--cs2113 m--tic4001 m--tic4002">

##### Documentation

* {{ optional }}  Follow [Google developer documentation style guide](https://developers.google.com/style).
</span>

</div>

{% endcall %}
