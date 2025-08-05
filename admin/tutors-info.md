{% from "_course-" + course + "/studentData-fragment.md" import tutors with context %}

## Staff

<div id="Damith" class="container">
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


<div id="Michael" class="container">
  <div class="row bt-2">
    <div class="col-3">

<img src="{{ url_course_gihub_io }}/tutor-photos/adamsmd.png" width="150" onerror="this.src='images/placeholder-large.png';" class="mt-1 rounded">
    </div>
    <div class="col">

### **Michael** D. Adams

**Co-Lecturer**<br>
%%:fas-envelope:%% `adamsmd`[at]`nus.edu.sg`<br>
%%:fas-map-marker-alt:%% COM3‐02‐47<br>
%%:fab-github:%% [@adamsmd](https://github.com/adamsmd)

</div>
</div>
</div>

-----------------------------

<div id="Prabhu" class="container">
  <div class="row bt-2">
    <div class="col-3">

<img src="{{ url_course_gihub_io }}/tutor-photos/prabhu-na.png" width="150" onerror="this.src='images/placeholder-large.png';" class="mt-1 rounded">
    </div>
    <div class="col">

### **Prabhu** NATARAJAN

**Co-Lecturer**<br>
%%:fas-envelope:%% `prabhu`[at]`comp.nus.edu.sg`<br>
%%:fas-map-marker-alt:%% COM3-02-34 | %%:fas-phone-square:%% 6516 1105<br>
%%:fab-github:%% [@prabhu-na](https://github.com/prabhu-na)

</div>
</div>
</div>

<!--
-----------------------------

<div id="Ganesh" class="container">
  <div class="row bt-2">
    <div class="col-3">


<img src="{{ url_course_gihub_io }}/tutor-photos/ganeshniyer.png" width="150" onerror="this.src='images/placeholder-large.png';" class="mt-1 rounded">
    </div>
    <div class="col">

### **Ganesh** Neelakanta Iyer

**Lecturer**<br>
%%:fas-envelope:%% `gni`[at]`nus.edu.sg`<br>
%%:fas-map-marker-alt:%% COM2-03-55 | %%:fas-phone-square:%% 6601 7601<br>
%%:fab-github:%% [@ganeshniyer](https://github.com/ganeshniyer)

</div>
</div>
</div>

-----------------------------

<div id="Eric" class="container">
<div class="row bt-2">
<div class="col-3">


<img src="{{ url_course_gihub_io }}/tutor-photos/eric-vader.png" width="150" onerror="this.src='images/placeholder-large.png';" class="mt-1 rounded">
</div>
<div class="col">

### Han Liang Wee **Eric**

**Lecturer**<br>
%%:fas-envelope:%% `eric_han`[at]`nus.edu.sg`<br>
%%:fas-map-marker-alt:%% COM2-03-26 | %%:fas-phone-square:%% 6601 7639<br>
%%:fab-github:%% [@eric-vader](https://github.com/eric-vader)

</div>
</div>
</div>


-->
-----------------------------

<div id="Tzer-Bin" class="container">
  <div class="row bt-2">
    <div class="col-3">

<img src="{{ url_course_gihub_io }}/tutor-photos/tzerbin.png" width="150" onerror="this.src='images/placeholder-large.png';" class="mt-1 rounded">
    </div>
    <div class="col">

### **Tzer Bin**

**Head TA**<br>
%%:fas-envelope:%% `dcsnt`[at]`nus.edu.sg`<br>
%%:fab-github:%% [@tzerbin](https://github.com/tzerbin)
    </div>
  </div>
</div>

------------------------

## Tutors
{% for t in tutors %}
<div id="{{ t.nick | replace(" ", "-") }}" class="container">
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
