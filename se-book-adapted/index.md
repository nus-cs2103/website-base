<frontmatter>
title: "Software Engineering for Self-Directed Learners [CS2103/T Version]"
footer: footer.md
</frontmatter>

<link rel="stylesheet" href="{{baseUrl}}/book/css/textbook.css">

<include src="../common/header.md" />

<div class="website-content" id="all">

## Software Engineering for Self-Directed Learners

### About this Book

* [Acknowledgements](about/acknowledgements.html)
* [How to use this book](about/usage.html)

### Software Engineering

<include src="../book/softwareEngineering/topicToc.md" />

### Object-Oriented Programming (with UML)

<include src="../book/oopDesign/topicToc.md" />

<include src="../book/oopImplementation/topicToc.md" />

### Requirements

<include src="../book/requirements/topicToc.md" />

<include src="../book/gatheringRequirements/topicToc.md" />

<include src="../book/specifyingRequirements/topicToc.md" />


{% import "se-book-adapted/config.md" as config %}


{% macro show_chapter(section, chapter) %}

* [{{ chapter.heading }}]({{baseUrl}}/se-book-adapted/chapters/{{ chapter.name }}.html)
  <trigger for="pop:{{ chapter.name }}-preview">{{glyphicon_eye_open}}</trigger> [{{glyphicon_print}}]({{baseUrl}}/se-book-adapted/chapters/{{ chapter.name }}-printable.html)

<popover id="pop:{{ chapter.name }}-preview" title="{{ chapter.heading}} {{glyphicon_eye_open}}" placement="right">
  <div slot="content">
    <include src="../book/{{chapter.name}}/preview.md" />
  </div>
</popover>

{% endmacro %}


{% macro show_section(section) %}
### {{ section.heading}}
{% for chapter in section.chapters %}
  {{ show_chapter(section, chapter) }}
{% endfor %}
{% endmacro %}


{% for section in config.topics %}
  {{ show_section(section) }}
{% endfor %}


### Quality Assurance

<include src="../book/qualityAssurance/topicToc.md" />

<include src="../book/testing/topicToc.md" />

<include src="../book/testCaseDesign/topicToc.md" />

### Project Management

<include src="../book/revisionControl/topicToc.md" />

<include src="../book/projectPlanning/topicToc.md" />

<include src="../book/teamwork/topicToc.md" />

<include src="../book/processModels/topicToc.md" />

### Tools

<include src="../book/uml/topicToc.md" />

<include src="../book/intellij/topicToc.md" />

<include src="../book/gitAndGithub/topicToc.md" />

<include src="../book/javaTools/topicToc.md" />

<include src="../book/junit/topicToc.md" />

### Supplementary

<include src="../book/principles/topicToc.md" />

<!-- TODO: add review -->

* [List of Definitions](common/definitions.html)
* [List of References](common/references.html)
* [List of Learning Outcomes](common/outcomes.html)
* [Printable Version {{glyphicon_print}}](common/print.html)

</div>
