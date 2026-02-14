{% from "common/macros.njk" import embed_topic, thumb, show_as_tab, show_faq, timing_badge with context %}
{% from "common/topics.njk" import  panopto with context %}

#### {{ thumb(1) }} **Demo your debugging skills**

<box type="important" seamless>

This tutorial task prepares you for an upcoming tP task. So, do not skip it.
</box>
<box type="info" seamless>

Relevant textbook topic:

{{ embed_topic("../../book/intellij/debuggingBasic/text.md#body", "Textbook " + icon_embedding + " Tools → **IDEs → Debugging: Basic**", "1", indent=0) }}
<p/>

</box>

{% if semester == "AY2526S2" %}
**Deadline**: {{ timing_badge("by Friday 4pm", "warning") }}

<div class="indented-level1">

1. Open your iP or tP code in **your IDE or any other code editor that has reasonable debugging support**.
1. Set a breakpoint somewhere in the code.
1. Run the code in debug mode.
1. When the execution stops at the break point, use the debugger to 'step through' 1-2 more statements.
1. Optional: Set a <tooltip content="i.e., the execution will stop only if the specified condition is met">_conditional break-point_</tooltip>.
1. Take a screenshot of the full IDE, showing evidence of the work you've done in above steps, including some code in the IDE editor window.
1. ==Upload the screenshot to the [Canvas Assignment: Week 6 - Tutorial - Task 1 (Demo your debugging skills)](https://canvas.nus.edu.sg/courses/85377/assignments/240317)==.
</div>

{% else %}
{{ timing_badge("prior to the tutorial, or in the first 10 minutes:", "warning") }}

<div class="indented-level1">

1. Open your iP or tP code in **your IDE or any other code editor that has reasonable debugging support**.
1. Set a breakpoint somewhere in the code.
1. Run the code in debug mode.
1. When the execution stops at the break point, use the debugger to 'step through' 1-2 more statements.
1. Take a screenshot of the IDE.
1. Optional: Set a <tooltip content="i.e., the execution will stop only if the specified condition is met">_conditional break-point_</tooltip>, take a screenshot of it too.

</div>

{{ timing_badge("first 10 minutes:", "warning") }} Paste your screenshots in the `T6-Workspace.pptx` file the tutor will share with you via MSTeams.

{% endif %}

#### {{ thumb(2) }} **Sequence diagrams exercise**

{% if semester == "AY2526S2" %}
**Deadline:** {{ timing_badge("by Friday 4pm", "warning") }}

* Do the following two exercises, as guided by video. Also ==answer the questions given inside the video==.


<div class="indented-level1">

<include src="../../book/modeling/modelingBehaviors/sequenceDiagramsBasic/q-explainMachineSequenceDiagram.md" />
<include src="../../book/modeling/modelingBehaviors/sequenceDiagramsIntermediate/q-essay-expainParserFactory.md" />
<p/>
{{ panopto(desc="17 mins", id="d449098c-5ae0-4bf1-8722-b3f000f886e7", questions=1) }}
</div>

{% else %}
* Do the following two exercises, as guided by the tutor.

<div class="indented-level1">

<include src="../../book/modeling/modelingBehaviors/sequenceDiagramsBasic/q-explainMachineSequenceDiagram.md" />
<include src="../../book/modeling/modelingBehaviors/sequenceDiagramsIntermediate/q-essay-expainParserFactory.md" />
<p/>
</div>
{% endif %}

