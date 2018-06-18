<frontmatter>
{% import "se-book-adapted/config.md" as config %}
{% import "se-book-adapted/chapters/chapter-printable.md" as chapter_template %}
{% set chapter = config.chapters.testCaseDesign %}
{{ chapter_template.add_front_matter(chapter) }}
</frontmatter>

{{ chapter_template.show_chapter("../../book/", chapter) }}