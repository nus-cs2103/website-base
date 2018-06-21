{% import "common/macros.md" as macros with context %}

{% macro show_unit_outcome(unit_outcomes, id_prefix) %}
{% set letters = "abcdefghijklmnop" | list %}
{% for unit in unit_outcomes %}
<panel type="{{ macros.show_priority_style(unit.priority) }}" expanded no-close >
<span slot="header" class="panel-title"><md>`{{ id_prefix }}{{ letters[loop.index-1] }}` <include src="../../book/{{  unit.location }}/text.md#outcomes" inline/> {{ macros.show_stars(unit.priority) }}</md></span>
  <include src="../../book/{{ unit.location }}/unit-inElsewhere-asFlat.md" boilerplate />
</panel>
{% endfor %}
{% endmacro %}

{% set unit_outcomes = [
  {location: "revisionControl/what", priority: "1"},
  {location: "revisionControl/repositories", priority: "1"},
  {location: "gitAndGithub/init", priority: "1"},
  {location: "revisionControl/savingHistory", priority: "1"},
  {location: "gitAndGithub/commit", priority: "1"},
  {location: "gitAndGithub/ignore", priority: "2"}
] %}

{{ show_unit_outcome(unit_outcomes, "W2.6") }}


<panel type="danger" header="`W2.6a` Can explain revision control :star:" expanded no-close>
  <include src="../../book/revisionControl/what/unit-inElsewhere-asFlat.md" boilerplate />
  <panel header="{{glyphicon_folder_close}} Evidence" expanded>
  
Be able to answer questions such as these:
  
<include src="../../book/revisionControl/what/q-essay-rcs-explain.md" />

  </panel>
</panel>

<panel type="danger" header="`W2.6b` Can explain repositories :star:" expanded no-close>
  <include src="../../book/revisionControl/repositories/unit-inElsewhere-asFlat.md" boilerplate />
  <panel header="{{glyphicon_folder_close}} Evidence" expanded>
  
Be able to answer questions such as these:

<include src="../../book/revisionControl/repositories/q-essay-repo-definition.md" />
    
  </panel>
</panel>

<panel type="danger" header="`W2.6c` Can create a local Git repo :star:" expanded no-close>
  <include src="../../book/gitAndGithub/init/unit-inElsewhere-asFlat.md" boilerplate />
  <panel header="{{glyphicon_folder_close}} Evidence" expanded>

Have a local repo that you created.

  </panel>
</panel>

<panel type="danger" header="`W2.6d` Can explain saving history :star:" expanded no-close>
  <include src="../../book/revisionControl/savingHistory/unit-inElsewhere-asFlat.md" boilerplate />
</panel>

<panel type="danger" header="`W2.6e` Can commit using Git :star:" expanded no-close>
  <include src="../../book/gitAndGithub/commit/unit-inElsewhere-asFlat.md" boilerplate />
  <panel header="{{glyphicon_folder_close}} Evidence" expanded>

Have a local repo that has commits you created.

  </panel>
</panel>

<panel type="warning" header="`W2.6f` Can set Git to ignore files :star::star:" expanded no-close>
  <include src="../../book/gitAndGithub/ignore/unit-inElsewhere-asFlat.md" boilerplate />
  <panel header="{{glyphicon_folder_close}} Evidence" expanded>

Have a local repo that has git-ignored files.

  </panel>
</panel>
