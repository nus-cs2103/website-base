<div id="testingPreparations">

* Ensure that you have accepted the invitation to join the GitHub org used by the course. Go to [{{ url_course_org }}]({{ url_course_org }}) to accept the invitation.
* Ensure you have access to a **computer that is able to run course projects** %%e.g., has the right Java version%%.
<div id="pe-create-repo">

* We will create a private repo `{{ pe_session }}-{your GitHub username}` in the [course's GitHub org]({{ url_course_org }}) about 24 hours before the {{ pe_session_name }} session starts. We'll let you know when it is ready. You will use that repo's issue tracker to report your {{ pe_session_name }} bugs.
* The issue tracker will already contain the necessary labels.
  * #r#Do not## edit the labels (i.e., text/colour) that we have provided.
  * You may create more labels if you wish (for your own convenience). Such labels will be ignored by our bug processing scripts.<br>
    #r#Do not## use `type.` and `severity.` as prefixes of labels you create yourself.
</div>

</panel><p/>
</div>

* **Have a good screen grab tool** with annotation features so that you can quickly take a screenshot of a bug, annotate it, and post in using CATcher.<br>
  {{ icon_tip }} You can use <kbd>Ctrl</kbd>+<kbd>V</kbd> to paste a picture from the clipboard into a text box in a bug report.

* **[Optional] Have a good screen recording tool** if you plan to use screen recording clips as part of your bug reports.

* **<span class="text-danger">Download the product to be tested</span>**.

<tabs active="{{ pe_active_tab }}" add-class="ml-4">
<tab header="PE Dry Run (at **{{ version_penultimate }}**)">

* First, wait till you are notified which team to test (likely to be in the morning of PE-D day)<br>
  Then, #r#wait until the start of the PE-D period## (i.e., 12 noon).<br>
  After that, download the JAR file and the UG/DG PDF file from the team's latest release. Downloading the files any earlier runs the risk of you testing an outdated version of the product.

</tab>
<tab header="PE (at **{{ version_final }}**)">

<div id="zip-download-unzip-info" >
<box type="info" header="++Downloading and unzipping JAR/PDF files you will test in the PE++" icon=":fas-download:">

The files you need for the PE (i.e., `.jar` file, UG and DG `.pdf` files) will be **given to you as an encrypted zip file**. Here are the two steps involved in using it.

1. **Downloading the zip file**: After we inform you the details (via email), go to the download location (a Dropbox folder), and download the zip file bearing your partial student number (e.g., `A---0000X.zip`).
   * The **dropbox password needed to download this** file is `{{ course | lower }}`.
   * ==You must download this file in advance.== Trying to download it during the PE can cause Dropbox to block you due to 'too many attempts'.
1. **Unzipping the zip file**: You will **need a second two-part password** to unzip this file. That password has two parts.
   * The second part will be unique to each student, and will be given in the same email mentioned above.
   * The first part of the password (common to all) will only be announced in Canvas at the start of the PE period.
</box>
</div>

</tab>
</tabs>
<p/>

<div class="indented">

<box>

****SIDEBAR: Testing tips****{.text-success}

{% set tip %}<span class="text-success">**:fas-lightbulb:**</span>{% endset %}

{{ tip }} **Use easy-to-remember patterns in test data.** For example, if you use `12345678` as a test input, and it appears as `2345678` somewhere else in the UI, you can easily spot that the first digit has gone missing. But if you used a random number instead, detecting that bug won't be as easy.<br> Similarly, if you use `Alice Bee`, `Benny Choo`, `Charles Darwin` as test data (note how the names start with letters A B, B C, C D), it will be easy to detect if one goes missing, or if the app mix them up in some way.

{{ tip }} **Go wide before you go deep**. Do a light testing of all features first. That will give you a better idea of which features are likely to be more buggy. Spending equal time for all features or testing in the order the features appear in the UG is not always the best approach.

</box>
</div>
<p/>
<!--
* **Charge your computer** before coming to the session. The testing venue might not have enough charging points.
-->
</div>
