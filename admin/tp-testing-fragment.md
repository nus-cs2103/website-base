<div id="testingPreparations">

* Ensure that you have accepted the invitation to join the GitHub org used by the course. Go to [{{ url_course_org }}]({{ url_course_org }}) to accept the invitation.
* Ensure you have access to a **computer that can run course projects** %%e.g., has the right Java version%%.
<div id="pe-create-repo">

* We will create a private repo `{{ pe_session }}-{your GitHub username}` in the [course's GitHub org]({{ url_course_org }}) about 24 hours before the {{ pe_session_name }} session starts. We'll let you know when it is ready. You will use that repo's issue tracker to report your {{ pe_session_name }} bugs.
* The issue tracker will already contain the necessary labels.
  * #r#Do not## edit the labels (i.e., text/color) that we have provided.
  * You may create more labels if you wish (for your own convenience). Such labels will be ignored by our bug processing scripts.<br>
    #r#Do not## use `type.` and `severity.` as prefixes of labels you create yourself.
</div>

</panel><p/>
</div>

* **Have a good screen grab tool** with annotation features so that you can quickly take a screenshot of a bug, annotate it, and post it using CATcher.<br>
  {{ icon_tip }} You can use <kbd>Ctrl</kbd>+<kbd>V</kbd> to paste a picture from the clipboard into a text box in a bug report.

* **[Optional] Have a good screen recording tool** if you plan to use screen recording clips as part of your bug reports.

* **<span class="text-danger">Download the product to be tested** as explained in **part [A]** of the panel below</span>.


<div id="zip-download-unzip-info" >
<box type="info" header="++Downloading and unzipping JAR files you will test in the PE++" icon=":fas-download:">

The files you need for the PE (i.e., `.jar` file, and a README.html file containing the URLs of the UG and DG) will be **given to you as an encrypted zip file**. Here are the steps involved in using it.

##### [A] Before the PE:

1. **Downloading the zip file**: After we inform you of the details (via email), go to the download location (a Dropbox folder), and download the zip file bearing your partial student number (e.g., `A---0000X.zip`).
   * The **Dropbox password needed to download this** file is `{{ course | lower }}`.
   * ==You must download this file in advance.== Trying to download it during the PE can cause Dropbox to block you due to 'too many attempts'.
1. **Constructing the password needed to unzip the file**: You will **need a second password** to unzip this file. That password has two parts.
   * The second part will be unique to each student, and will be given in the same email mentioned above. Keep it safe, and have it ready at the start of the PE.
   * The first part of the password (common to all) will only be announced in Canvas at the start of the PE period.
1. **Recommended: Try the unzipping steps** (given in part [B] below) using [this sample zip file](https://github.com/user-attachments/files/{{ '33901091' if cs2103 else '33901164' }}/A---0000X.zip) before the PE (first part of the password: `password1-`, second part: `password2` i.e., you should use `password1-password2` to unzip it).<br>
    Use the JAR file inside it to try the steps given below as well, to confirm that your computer's Java environment is as expected and can run PE JAR files.

---

##### [B] At the start of the PE:

1. **Use the combined password to unzip the file**, which should give you another zip file with the name suffix `_inner.zip`.
2. **Unzip that second zip file normally** (no password required). That will give you a folder containing the JAR file to test and a README.html containing the URL of their product website.
     * ==Warning: do not run the JAR file while it is still inside the zip file==.
     * Ignore the `padding_file` found among the extracted files. %%Its only purpose is to mask the true size of the JAR file so that someone cannot guess which team they will be testing based on the zip file size.%%

<box type="warning" icon=":fab-apple:" seamless>

macOS automatically unzips the inner zip file after you unzip the outer zip file using the password.

Newer macOS versions can run into a permission issue when trying to auto-extract the inner zip file with an error `Unable to expand "..._inner.zip" It is an unsupported format`. Just ignore the error message and manually extract the inner zip file by double-clicking it.
</box>

</box>
</div>

<div class="indented">

<box>

****SIDEBAR: Testing tips****{.text-success}

{% set tip %}<span class="text-success">**:fas-lightbulb:**</span>{% endset %}

{{ tip }} **Use easy-to-remember patterns in test data.** For example, if you use `12345678` as a test input, and it appears as `2345678` somewhere else in the UI, you can easily spot that the first digit has gone missing. But if you used a random number instead, detecting that bug won't be as easy.<br> Similarly, if you use `Alice Bee`, `Benny Choo`, `Charles Darwin` as test data (note how the names start with letters A B, B C, C D), it will be easy to detect if one goes missing, or if the app mixes them up in some way.

{{ tip }} **Go wide before you go deep**. Do light testing of all features first. That will give you a better idea of which features are likely to be more buggy. Spending equal time for all features or testing in the order the features appear in the UG is not always the best approach.

</box>
</div>
<p/>
<!--
* **Charge your computer** before coming to the session. The testing venue might not have enough charging points.
-->
</div>
