{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("instructors") %}
<div id="main">
{% if cs2103 %}

## Staff

<div class="container">
  <div class="row bt-2">
    <div class="col-3">

<img src="images/damith.png" width="150" class="mt-1 rounded"/>
    </div>
    <div class="col">

### **Damith** Chatura RAJAPAKSE

**Course Coordinator**<br>
%%:fas-envelope:%% `damith`[at]`comp.nus.edu.sg`<br>
%%:fas-map-marker-alt:%% COM2-02-57 | %%:fas-phone-square:%% 6516 4359<br>
%%:fas-home:%% https://www.comp.nus.edu.sg/~damithch | %%:fab-github:%% [@damithc](https://github.com/damithc)
    </div>
  </div>
</div>

-----------------------------

<div class="container">
  <div class="row bt-2">
    <div class="col-3">


<img src="{{ url_course_gihub_io }}/tutor-photos/prabhu-na.png" width="150" onerror="this.src='images/placeholder-large.png';" class="mt-1 rounded">
    </div>
    <div class="col">

### **Prabhu** NATARAJAN

**Lecturer**<br>
%%:fas-envelope:%% `prabhu`[at]`comp.nus.edu.sg`<br>
%%:fas-map-marker-alt:%% COM3-02-34 | %%:fas-phone-square:%% 6516 1105<br>
%%:fab-github:%% [@prabhu-na](https://github.com/prabhu-na)

<!--
<img src="{{ url_course_gihub_io }}/tutor-photos/ganeshniyer.png" width="150" onerror="this.src='images/placeholder-large.png';" class="mt-1 rounded">
    </div>
    <div class="col">

### **Ganesh** Neelakanta Iyer

**Lecturer**<br>
%%:fas-envelope:%% `gni`[at]`nus.edu.sg`<br>
%%:fas-map-marker-alt:%% COM2-03-55 | %%:fas-phone-square:%% 6601 7601<br>
%%:fab-github:%% [@ganeshniyer](https://github.com/ganeshniyer)
-->
    </div>
  </div>
</div>

-----------------------------

<div class="container">
  <div class="row bt-2">
    <div class="col-3">

<img src="{{ url_course_gihub_io }}/tutor-photos/bluesky0911.png" width="150" onerror="this.src='images/placeholder-large.png';" class="mt-1 rounded">
    </div>
    <div class="col">

### Kim hyeongcheol (**Danny**)

**Head TA**<br>
%%:fas-envelope:%% `dcskh`[at]`nus.edu.sg`<br>
%%:fas-phone-square:%% 8750 5674<br>
%%:fab-github:%% [@bluesky0911](https://github.com/bluesky0911)
    </div>
  </div>
</div>

-----------------------------
<!--
<div class="container">
  <div class="row bt-2">
    <div class="col-3">

<img src="{{ url_course_gihub_io }}/tutor-photos/anisyusof-sc.png" width="150" onerror="this.src='images/placeholder-large.png';" class="mt-1 rounded">
    </div>
    <div class="col">

### **Anis** Bin Yusof

**Graduate Tutor**<br>
%%:fas-envelope:%% `anis`[at]`comp.nus.edu.sg`<br>
%%:fas-phone-square:%% 6516 8557<br>
%%:fab-github:%% [@anisyusof-sc](https://github.com/anisyusof-sc)
    </div>
  </div>
</div>
-->

## Tutors

<include src="tutors-info.md" />

{% else %}
<iframe src="{{ url_instructors }}" width="800" height="1000" ></iframe>
{% endif %}


## Dev Team

This course is supported by a number of software tools developed by our students:

* [**CATcher** dev team](https://github.com/CATcher-org/CATcher#current-dev-team)
* [**MarkBind** dev team](https://markbind.org/about.html)
* [**PowerPointLabs** dev team](https://www.comp.nus.edu.sg/~pptlabs/contact.html)
* [**RepoSense** dev team](https://reposense.org/about.html)
* [**SE-EDU** dev team](https://se-education.org/docs/team.html)
* [**TEAMMATES** dev team](https://teammatesv4.appspot.com/web/front/about)

</div>

{% endcall %}
