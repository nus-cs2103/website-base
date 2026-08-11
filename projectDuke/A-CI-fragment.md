{% from "common/macros.njk" import ask_chatgpt, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-CI", "Set up CI", "primary") }}

Use GitHub Actions to set up Continuous Integration (CI).

The workflow specified by [this `.yml` file](https://github.com/se-edu/duke/blob/full-template/.github/workflows/gradle.yml) is a good candidate for this project.

Refer to the [_Using GitHub Actions_ @SE-EDU/guides](https://se-education.org/guides/tutorials/githubActions.html) to learn how to use that `.yml` file to set up GitHub Actions.

Also note that pushing a GitHub Actions-related file to GitHub requires you to authenticate using a <tooltip content="Personal Access Token">PAT</tooltip> that has `workflow` permissions (because you are modifying a workflow of your repo). If you are using Sourcetree, you can refer to [_Sourcetree Guide_ @SE-EDU/guides](https://se-education.org/guides/tutorials/sourcetree.html) to learn how to connect Sourcetree with GitHub using a PAT.
