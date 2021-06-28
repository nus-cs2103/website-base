<frontmatter>
title: "Combined Exercises"
layout: textbook.md
</frontmatter>
{% import "se-book-adapted/config.njk" as config with context %}

<link rel="stylesheet" href="{{baseUrl}}/book/css/textbook.css">

<div class="website-content">

## Combined Exercises

Here are some exercises that combine multiple topics.

{% for exercise in config.combinedExercises %}
  <include src="../../book/combined/exercises/{{ exercise }}.md" />
{% endfor %}

</div>