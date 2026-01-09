{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("instructors") %}
<div id="main">
{% if cs2103 %}

<include src="tutors-info.md" />

{% else %}
<iframe src="{{ url_instructors }}" width="800" height="1000" ></iframe>
{% endif %}


## Dev Team

This course is supported by a number of software tools developed by our students:

* [**Git-Mastery** dev team](https://git-mastery.org/about/)
* [**MarkBind** dev team](https://markbind.org/about.html)
* [**RepoSense** dev team](https://reposense.org/about.html)
* [**SE-EDU** dev team](https://se-education.org/docs/team.html)
* [**TEAMMATES** dev team](https://teammatesv4.appspot.com/web/front/about)

</div>

{% endcall %}
