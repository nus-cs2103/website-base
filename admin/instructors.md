{% macro show_main_text() %}
<div id="main">

<iframe src="{{ instructors_page }}" width="800" height="1000" ></iframe>

**Dev Team**:

This module is supported by a number of software tools developed by past students. Here are some of them whose work was directly relevant to the module for this semester:

* Aditya Agarwal
* Chng Zhi Xuan
* Devamanyu Hazarica
* Eugene Peh
* Jia Zhixin
* Lai Hoang Dung (Louis)
* Metta Ong
* Sidhdharth Aravindan
* Tan Jun An
* Tan Wang Leng
* Teng Yong Hao


</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("instructors", show_main_text) }}