{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-MoreTesting", "More automated tests", "primary") }}

Write more JUnit tests, to cover nearly all code that _can_ be tested automatically.

You may omit code that is hard to test automatically, e.g., GUI functionality (test it manually instead).

This can include more manual testing as well, e.g., testing on different OSes, different screen resolutions, different OS language settings (English vs Chinese)

