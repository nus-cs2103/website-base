{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("instructors") %}
<div id="main">
{% if tic4001 %}

<div class="container">
  <div class="row bt-2">
    <div class="col-3">

<img src="images/damith.png" width="150" class="mt-1 rounded"/>
    </div>
    <div class="col">

**Damith Chatura RAJAPAKSE** (Module Coordinator)<br>
Associate Professor, NUS School of Computing<br>
PhD, Software Engineering, NUS, 2002-2006<br>
BSc, Computer Science & Engineering, University of Moratuwa, 1996-2001<br>
%%:fas-envelope:%% <span id="prof-email">`damith`[at]`comp.nus.edu.sg`</span><br>
%%:fas-map-marker-alt:%% COM2-02-57<br>
%%:fas-phone-square:%% 651 64359<br>
%%:fas-home:%% https://www.comp.nus.edu.sg/~damithch
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

This module is supported by a number of software tools developed by our students. Here are some of them whose work is directly relevant to the module for this semester:

* Daryl Tan
* Evangelos Sigalas
* James Pang Mun Wai
* Jin Minjia
* Koh Jun Wei
* Lee Jin Yao
* Lum Ka Fai Jeffry
* Prithivi Raj s/o Siva Kumar
* Ronak Lakhotia
* Tan Wang Leng
* Yip Seng Yeun (Alfred)

</div>

{% endcall %}
