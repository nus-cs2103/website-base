{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-BetterGui", "Improve the GUI", "primary") }}

Improve the GUI to make it more _polished_. Some examples:
* Tweak the GUI to match the asymmetric nature of the conversation: it is between the user and the app, not between two humans, so it makes sense not to display both sides in the same visual format. {{ numbers_roman }}
* Highlight errors, e.g., when the user types a wrong command, the error should be shown in a different format to catch the user's attention.
* Tweak padding, fonts, colors, alignments to make the GUI more pleasing to look at.<br>
  Given the app is likely to take only a small portion of the screen, and the bot replies can contain a lot of text, try to optimize for space (e.g., avoid wasting display space that simply shows the background graphics).
* Allow resizing of the Window, and ensure the content resizes appropriately as the Window changes size.
* Profile pictures: If your GUI shows profile pictures, you can tweak the way the picture is shown (e.g., crop as a circle or a square with rounded corners). In fact, an easy tweak is to use a picture with a transparent background so that it blends nicely with the background.<br>
  Given that the participants of the conversation are fixed (i.e., you and the chatbot), do you even need big profile pictures?
* Focus more on tweaks that actually _improve_ the user experience (UX). Some changes %%(e.g., profile pictures, background graphics)%% can be eye-catching but can even degrade the UX if not done right %%(e.g., it can make the text harder to read)%%

{{ icon_tip }} You can take inspiration from [these past projects](https://nus-cs2103-ay2526s1.github.io/website/admin/ip-showcase.html). If you adopt any ideas from them, don't forget to give credit to the original author.

{{ icon_info }} Minimal requirement: Implement at least one of the examples (i - vi) given above.

