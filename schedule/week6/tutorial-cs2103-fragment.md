{% from "common/macros.njk" import embed_topic, thumb, show_as_tab, show_faq with context %}

#### {{ thumb(1) }} **Demo your debugging skills**

<box type="important" seamless>

This tutorial task prepares you for an upcoming tP task. So, do not skip it.
</box>
<box type="info" seamless>

Relevant textbook topic:

{{ embed_topic("../../book/intellij/debuggingBasic/text.md#body", "Textbook " + icon_embedding + " Tools → **IntelliJ IDEA → Debugging: Basic**", "1", indent=0) }}
<p/>

If you are new to debugging with an IDE, we recommend you **have a look at [[guide@se-edu] Intellij IDEA: Using the debugger](https://se-education.org/guides/tutorials/intellijDebugger.html)**.
</box>

1. Open your iP or tP code in your IDE.
1. Set a breakpoint somewhere in the code.
1. Run the code in debug mode.
1. When the execution stops at the break point, use the debugger to 'step through' 1-2 more statements.
1. Take a screenshot of the IDE and paste in the _tutorial workspace_ file.
1. Optional: Set a <tooltip content="i.e., the execution will stop only if the specified condition is met">_conditional break-point_</tooltip>, take a screenshot of it, and paste it in the same file.

{{ show_faq("warmUpTaskRushed") }}

#### {{ thumb(2) }} **Sequence diagrams exercise**

* Do the following two exercises, as guided by the tutor.

<div class="indented-level1">

<include src="../../book/modeling/modelingBehaviors/sequenceDiagramsBasic/q-explainMachineSequenceDiagram.md" />
<include src="../../book/modeling/modelingBehaviors/sequenceDiagramsIntermediate/q-essay-expainParserFactory.md" />
<p/>
</div>
