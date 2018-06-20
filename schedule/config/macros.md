

{% macro show_outcome(id, heading, priority, file) %}
<panel no-close >
<span slot="header" class="panel-title"><md>`{{ id }}` **{{ heading }}**</md> <span class="label label-danger">{{ glyphicon_star }}&nbsp;</span></span>
  <include src="{{ file }}" />
</panel>
{% endmacro %}