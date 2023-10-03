<div class="indented border">
<panel type="seamless" {{ status }} no-close>
{% set displacement="" %}
<div slot="header"><md>**Duke** %%{{ header }}%% <span class="badge rounded-pill bg-secondary">{{ tag }}</span></md></div>
{% set displacement=".." %}
<include src="{{ displacement }}/book/projectDuke/{{ fragment }}" />
</panel>

</div>
