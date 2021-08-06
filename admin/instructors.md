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

<include src="instructor-damith.mbdf" />
    </div>
  </div>
  <div class="row pt-4 border-top border-bottom">
    <div class="col-3">

<img src="images/boyd.png" width="150" class="mt-1 rounded"/>
    </div>
    <div class="col">

**Boyd ANDERSON** (Co-Lecturer)<br>
Lecturer, NUS School of Computing<br>
Ph.D. (National University of Singapore, Singapore)<br>
M.Sc. (Victoria University of Wellington, New Zealand)<br>
B.Sc. (Victoria University of Wellington, New Zealand)<br>
%%:fas-envelope:%% <span id="prof-email">`boyd`[at]`comp.nus.edu.sg`</span><br>
%%:fas-map-marker-alt:%% COM2-03-26<br>
%%:fas-phone-square:%% 660 17900<br>
%%:fas-home:%% https://www.comp.nus.edu.sg/cs/bio/boyd/
    </div>
  </div>
</div>

{% else %}
<iframe src="{{ url_instructors }}" width="800" height="1000" ></iframe>
{% endif %}

<br>

**Dev Team**:

This module is supported by a number of software tools developed by our students:

* [**CATcher** dev team](https://github.com/CATcher-org/CATcher#current-dev-team)
* [**MarkBind** dev team](https://markbind.org/about.html)
* [**PowerPointLabs** dev team](https://www.comp.nus.edu.sg/~pptlabs/contact.html)
* [**RepoSense** dev team](https://reposense.org/about.html)
* [**SE-EDU** dev team](https://se-education.org/docs/team.html)
* [**TEAMMATES** dev team](https://teammatesv4.appspot.com/web/front/about)

</div>

{% endcall %}
