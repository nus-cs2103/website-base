<frontmatter>
title: "Definitions"
siteNav: se-book-adapted-sitenav.md
</frontmatter>
{% import "se-book-adapted/config.njk" as config with context %}

<link rel="stylesheet" href="{{baseUrl}}/book/css/textbook.css">

<include src="../../common/header.md" />

<div class="website-content">

# Definitions

{% for letter in config.definitions %}

## {{ letter.letter }}
  {% for def in letter.defs %}
  <include src="../../book/common/definitions.md#{{ def }}" />
  {% endfor %}
{% endfor %}

</div>





