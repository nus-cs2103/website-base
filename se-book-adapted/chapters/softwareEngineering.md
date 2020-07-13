{% if module != "TIC4001" %}
<frontmatter>
{% import "se-book-adapted/config.njk" as config with context %}
{% import "se-book-adapted/chapters/chapter.njk" as chapter_template with context %}
{% set chapter = config.chapters.softwareEngineering %}
{{ chapter_template.add_front_matter(chapter) }}
</frontmatter>

{{ chapter_template.show_chapter(chapter) }}
{% endif %}
