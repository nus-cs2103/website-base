{% from "_course-" + course + "/studentData-fragment.md" import tutors with context %}

{% for t in tutors %}
<div class="container">
  <div class="row bt-2">
    <div class="col-3">

<img src="{{ url_course_gihub_io }}/tutor-photos/{{ t.github | lower }}.png" width="150" onerror="this.src='images/placeholder-large.png';" class="mt-1 rounded">
    </div>
    <div class="col">

### {{loop.index}}. {{ t.nick }}

**{{ t.name }}**<br>
%%:fas-envelope:%% `{{ t.nusnet }}[at]u.nus.edu`<br>
%%:fab-github:%% [@{{ t.github }}](https://github.com/{{ t.github }})
    </div>
  </div>
</div>

-----------------------------------------
{% endfor %}
