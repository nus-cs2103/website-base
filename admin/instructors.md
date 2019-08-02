{% macro show_main_text() %}
<div id="main">

<iframe src="{{ instructors_page }}" width="800" height="1000" ></iframe>

**Dev Team**:

This module is supported by a number of software tools developed by our students. Here are some of them whose work is directly relevant to the module for this semester:

* Chin Jian Hao Kevin
* Daryl Tan
* Evangelos Sigalas
* Herty Liany
* James Pang Mun Wai
* Jin Minjia
* Koh Jun Wei
* Lee Jin Yao
* Lee Yi Jie Joel
* Low Shi Lei, Deborah
* Lum Ka Fai Jeffry
* Prithivi Raj s/o Siva Kumar
* Ronak Lakhotia
* Tan Wang Leng
* Yip Seng Yeun (Alfred)

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("instructors", show_main_text) }}