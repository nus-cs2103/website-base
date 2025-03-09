{% from "common/macros.njk" import thumb, show_faq, show_as_tab, timing_badge with context %}

<include src="../../admin/common-tutorials-fragment.md#hand-drawing-diagrams" />

{{ show_faq("umlIsItUsedInIndustry", is_compact=1) }}
{{ show_faq("umlAreWeOverdoing") }}

#### {{ thumb(1) }} Exercise: draw a class diagram and an object diagram

<include src="../../admin/common-tutorials-fragment.md#draw-stock-cd" />


#### {{ thumb(2) }} Exercise: draw a sequence diagram

<include src="../../admin/common-tutorials-fragment.md#draw-sd-personlist" />
