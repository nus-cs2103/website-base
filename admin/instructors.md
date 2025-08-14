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

* [**CATcher** dev team](https://github.com/CATcher-org/CATcher#current-dev-team)
* [**Git-Mastery** dev team](https://git-mastery.github.io/team/)
* [**MarkBind** dev team](https://markbind.org/about.html)
* [**PowerPointLabs** dev team](https://www.comp.nus.edu.sg/~pptlabs/contact.html)
* [**RepoSense** dev team](https://reposense.org/about.html)
* [**SE-EDU** dev team](https://se-education.org/docs/team.html)
* [**TEAMMATES** dev team](https://teammatesv4.appspot.com/web/front/about)

</div>

{% endcall %}
