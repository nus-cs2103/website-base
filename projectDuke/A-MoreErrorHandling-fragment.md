{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-MoreErrorHandling", "More error handling", "primary") }}

Improve the code to handle all errors you anticipate the product will encounter during usage.

Some examples of errors:
* command format errors: multiple spaces where only one is expected, trailing/leading spaces in the command, an essential parameter missing, a parameter specified multiple times, special characters used where they are not expected, ...
* environment issues: an expected file is missing, access to a file is denied, a file's content is not as expected, ...
* data is not as expected: start date/time is later than (or same as) end date/time, a value that should be unique is duplicated (e.g., two tasks with the same exact details), non-existent dates (e.g., Feb 30).

