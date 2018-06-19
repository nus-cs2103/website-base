<frontmatter>
title: "Definitions"
</frontmatter>
{% import "se-book-adapted/config.md" as config with context %}

<link rel="stylesheet" href="{{baseUrl}}/book/css/textbook.css">

<div class="website-content">

# Definitions

{% for letter in config.definitions %}

## {{ letter.letter }}
  {% for def in letter.defs %}
  <include src="../../book/common/definitions.md#{{ def }}" />
  {% endfor %}
{% endfor %}

</div>





