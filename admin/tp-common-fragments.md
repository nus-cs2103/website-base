{% macro show_common_error(id_slug) %}
<div id="{{ id_slug }}">
<box type="important" seamless icon=":fas-skull:">

**COMMON MISTAKE:**{ .text-danger } {{ caller() | trim }}
</box>
</div>
{% endmacro %}

{% call show_common_error("error-header-comment-phrasing") %}
**Not following the [required phrasing style for the first sentence](https://se-education.org/guides/conventions/java/{{ "basic" if cs2113 else "intermediate" }}.html#:~:text=In%20method%20header%20comments%2C%20the%20first%20sentence%20should)** of Java method header comments. { icon="fas-skull" i-class="text-danger" }
{% endcall %}

{% call show_common_error("error-commit-message-subject") %}
**Not following the [convention for Git commit message subject](https://se-education.org/guides/conventions/git.html#:~:text=Commit%20message%3A%20Subject)**.<br>
Caution: This is <span class="text-danger">very hard to rectify later</span>, after the PR containing the commits have been merged. %%Reason: While Git allows editing past commits, doing so changes their timestamp, which affects your weekly code contribution stats (which are factored into evaluating the consistency of your coding work over the project duration).%% { icon="fas-skull" i-class="text-danger" }
{% endcall %}

{% call show_common_error("error-pr-from-master") %}
**Forgetting to do each PR from a separate branch** (i.e., send PR from the `master` branch) of your fork. This error means your PR will not be considered as _following the forking workflow correctly_. { icon="fas-skull" i-class="text-danger" }
{% endcall %}

{% call show_common_error("error-low-pr-comments") %}
**Not giving enough PR review comments.** Remember to do proper PR reviews throughout the tP, at least for non-trivial changes, as the quality and quantity of PR review comments you have given to peers affect your [tP marks](tp-grading.html) (under the _project management_ aspect).
{% endcall %}