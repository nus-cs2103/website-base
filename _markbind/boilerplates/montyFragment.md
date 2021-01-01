<div class="indented-level2">
<panel type="info" {{ status }} no-close >
{% set displacement="" %}
<div slot="header" class="text-white"><md>Programming {{ icon_embedding }}&nbsp; {{ header }} <span class="badge badge-pill badge-warning">{{ tag }}</span></md></div>
{% set displacement=".." %}
<include src="{{ displacement }}/programming/monty/{{ fragment }}" />
</panel>
</div>
