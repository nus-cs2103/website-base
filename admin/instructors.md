{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("instructors") %}
<div id="main">
{% if tic4001 or tic4002 %}

<div class="container">
  <div class="row bt-2">
    <div class="col-3">

<img src="images/damith.png" width="150" class="mt-1 rounded"/>
    </div>
    <div class="col">

<include src="instructor-damith-fragment.md" />
    </div>
  </div>
</div>

{% else %}
<iframe src="{{ url_instructors }}" width="800" height="1000" ></iframe>
{% endif %}

<br>

**Dev Team**:

This course is supported by a number of software tools developed by our students:

* [**CATcher** dev team](https://github.com/CATcher-org/CATcher#current-dev-team)
* [**MarkBind** dev team](https://markbind.org/about.html)
* [**PowerPointLabs** dev team](https://www.comp.nus.edu.sg/~pptlabs/contact.html)
* [**RepoSense** dev team](https://reposense.org/about.html)
* [**SE-EDU** dev team](https://se-education.org/docs/team.html)
* [**TEAMMATES** dev team](https://teammatesv4.appspot.com/web/front/about)

</div>

{% endcall %}
