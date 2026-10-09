{% from "common/macros.njk" import thumb, show_faq, show_as_tab, timing_badge with context %}

<include src="../../admin/common-tutorials-fragment.md#hand-drawing-diagrams" />

{{ show_faq("umlIsItUsedInIndustry", is_compact=1) }}
{{ show_faq("umlAreWeOverdoing") }}

#### {{ thumb(1) }} Exercise: draw a class diagram and an object diagram

<include src="../../admin/common-tutorials-fragment.md#draw-stock-cd" />


#### {{ thumb(2) }} Exercise: draw a sequence diagram

<include src="../../admin/common-tutorials-fragment.md#draw-sd-personlist" />

{% if semester == 'AY2627S1' %}

#### {{ thumb(3) }} Watch the recorded tutorial and answer in-video quizzes

Watch the video below and submit the in-video quiz.<br>
#r#Deadline: Mon 12th Oct, 23:59##

<panel type="seamless" expanded>
  <div slot="header"><span style="font-size: 100%;" class="badge rounded-pill bg-danger">{{ icon_video }} Video</span><md> Week 8 Tutorial (recorded) {{ icon_q }}</md> <span style="font-size: large;" class="badge rounded-pill bg-warning text-dark">Q+</span></div>
<iframe src="https://mediaweb.ap.panopto.com/Panopto/Pages/Embed.aspx?id=1b0f7a18-35d5-424a-8e8a-b4da00b4ced5&autoplay=false&offerviewer=true&showtitle=true&showbrand=false&start=0&interactivity=all" style="width: 684px; height: 513px; border: 1px solid #464646;" allowfullscreen allow="autoplay"></iframe>
</panel>

{% endif %}
