<panel type="info" header="### DANIEL WONG YONG SHEN `@dawo5010` (22 contributions)" expanded>
<panel header="**2. :fas-info-circle: Member detail not showing up on Project List page**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/175" expanded>

Hi Prof,



One of my teammates does not have her profile picture available on the Project List webpage, despite it being uploaded. My guess was that it was not uploaded to the repo in all-lower caps. We've since fixed it (renamed to all lower caps).



Do we have to make sure that the photo shows up on the project list page before submission?

My group is CS2103T-T13-3. 



Thank you in advance!
</panel>

<panel header="**3. :fas-info-circle: Modifying Duke to take commands from the user interactively**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/57" expanded>

Hi Prof,



Is it a requirement that Duke takes in commands within one line?

Currently the command syntax goes roughly like this:

/<command> <description> </by or /at> <date>



I have been thinking of modifying Duke to interface with a user interactively, e.g.

Duke: Hello, what can I do for you today?

User: add deadline

Duke: Sure, what will your deadline's description be?

User: return book

Duke: And when is it due?

User: 10/09/2019 2100

Duke: Okay, I've added a new task: [D][x] return book (by: 10/09/2019 2100)



or would this be in violation of the fundamental purpose/target audience/intended use/learning point of Duke?



Thanks in advance!
</panel>

<panel header="**4. :fas-info-circle: Encountering difficulties setting default formatting for IntelliJ**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/18" expanded>

Hi,



I'm trying to get IntelliJ to be compliant with the [specified code style](https://nus-cs2103-ay1920s1.github.io/website/coding-standards/java/intermediate.html).



However, I seem to be having some difficulties with trying to get IntelliJ to save the settings:

![2019-08-27 10-07-32 2019-08-27 10_09_12](https://user-images.githubusercontent.com/4518827/63735579-ded8e100-c8b2-11e9-9d64-979ffd15183f.gif)



As can be seen from the gif, no matter how many times I try to get IntelliJ to accept the new settings, the indentation for switch cases resets upon clicking OK.



I've already unticked 'Detect and use existing file indents for editing.' but that hasn't helped.



Would appreciate if anyone has any insight into the issue, thank you!


</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/11#issuecomment-523836922" expanded>

I followed this tutorial:

https://git-scm.com/book/en/v2/Git-Basics-Tagging



tl;dr for you: `git push origin <tagname>` for a single tag, `git push origin --tags` to upload all tags not already present remotely.
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/18#issuecomment-525108753" expanded>

Thanks! That fixed the formatting. Appreciate the help!
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/27#issuecomment-526141819" expanded>

Heyyo,



I had the same issue when trying to complete Level-7 as well, and I didn't want to make it such that the file had to pre-exist/be created by the user before using the program.



Here's some articles on stackoverflow that I referred to for this problem: [Create File if not exists](https://stackoverflow.com/questions/9620683/java-fileoutputstream-create-file-if-not-exists), [Create whole path automatically](https://stackoverflow.com/questions/2833853/create-whole-path-automatically-when-writing-to-a-new-file).



In short, use .getParentFile().mkdirs() on your file object to create the necessary directory, and use .createNewFile() to create the file itself. Hope that helps!
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/28#issuecomment-526235238" expanded>

I presume you're on Windows 10.

Try editing your System Environment Variables:



1. Search Environment Variables in your start menu search bar:

![Untitled](https://user-images.githubusercontent.com/4518827/63953016-18783a80-cab3-11e9-9cb9-08d1b37f8557.png)



2. Click Environment Variables:

![Annotation 2019-08-29 231404](https://user-images.githubusercontent.com/4518827/63953062-30e85500-cab3-11e9-93ef-4a17aea1f461.jpg)



3. Under system variables, look for a JAVA_HOME and double click it and modify the variable value to the path of your JDK 11 (without the /bin folder).

If it doesn't exist, create one (but I presume it should, since gradle is already working, else it would throw an error message.)

![Annotation 2019-08-29 231346](https://user-images.githubusercontent.com/4518827/63953040-25952980-cab3-11e9-8853-7607680cffce.jpg)



The steps would differ if you use Mac OS (and I am not too sure, since it worked out of box for me), but you can try referring to [this Medium article](https://medium.com/zendesk-engineering/setting-java-home-on-mac-os-acd44e3a6027) for that.


</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/45#issuecomment-528828866" expanded>

I cloned your repo and managed to replicate the error:



<img width="1680" alt="Screenshot 2019-09-06 at 8 03 46 PM" src="https://user-images.githubusercontent.com/4518827/64426559-74f5de00-d0e1-11e9-80be-2facf55d1944.png">



The issue at hand is quite easily fixed: simply remove the trailing space after the file path for the two statements you posted:



`private Image user = new Image(this.getClass().getResourceAsStream("/images/DaUser.png "));`

`private Image duke = new Image(this.getClass().getResourceAsStream("/images/DaDuke.png "));`

to

`private Image user = new Image(this.getClass().getResourceAsStream("/images/DaUser.png"));`

`private Image duke = new Image(this.getClass().getResourceAsStream("/images/DaDuke.png"));`



The program executes successfully:

<img width="512" alt="Screenshot 2019-09-06 at 8 05 18 PM" src="https://user-images.githubusercontent.com/4518827/64426632-ac648a80-d0e1-11e9-91e1-f4791f6decf9.png">



I infer that you're on Mac OS from the directory structure your indicated. It seems that Prof and Jeffry didn't encounter the issue as Mac OS/Unix systems in general are much more anal than Windows when it comes to file naming conventions (being case-sensitive by default, amongst other things).



edit: I just did some quick research and it turns out that Windows automatically removes whitespaces from directories while macOS/Unix does not. So do take note when addressing your file names!



Hope that helps and don't forget to close the issue if it's been resolved!
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/56#issuecomment-529920401" expanded>

Can you take a screenshot of the Modules tab?
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/56#issuecomment-529923007" expanded>

Delete 'main' under the Modules tab by selecting it and clicking the '-' button above it. (don't touch the one under seedu.duke.duke)

That should fix it. 
</panel>

<panel header="**12 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/56#issuecomment-529930327" expanded>

Awesome, don't forget to close the issue :)
</panel>

<panel header="**13 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/57#issuecomment-529964886" expanded>

Right, that's something I'll keep in mind when thinking about the tP and it's implementation too, then. Thanks prof!
</panel>

<panel header="**14 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/58#issuecomment-530004708" expanded>

See https://github.com/nus-cs2103-AY1920S1/forum/issues/54



Have you changed your shadowJar configuration to use Launcher as your main class instead?
</panel>

<panel header="**15 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/58#issuecomment-530007120" expanded>

Yep, then try `./gradlew shadowJar` again and see if it works :)
</panel>

<panel header="**16 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/58#issuecomment-530010311" expanded>

That looks like a print statement, so I dug through your code to find it. 



Your program uses the file /data/duke.txt relative to the directory that the jar file is launched. 

In your case, you likely launched the jar file from the `build` folder and since it didn't already have a data/duke.txt, that triggered the print statement in Line 46 of your Duke.java (according to [your latest commit here](https://github.com/ChangUo79/duke/blob/master/src/main/java/Duke.java)), hence printing 'File not found.'


</panel>

<panel header="**17 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/62#issuecomment-530687428" expanded>

Can you push your branch-Level-10 in its current (broken) state to your repo so that it can be cloned? 
</panel>

<panel header="**18 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/62#issuecomment-531097069" expanded>

Hmm, as @Nanosync suggested, you probably need to refresh your gradle configuration within IntelliJ. It might have been the case that you did not click the prompt to import gradle configuration changes within IntelliJ when you modified your build.gradle.



Try refreshing again? I've attached a gif of how to do so just in case:



![2019-09-13 12-49-16 2019-09-13 12_50_47](https://user-images.githubusercontent.com/4518827/64838311-21294e80-d625-11e9-8f35-203fa493a389.gif)



Otherwise, can you also try re-importing your project?



1. File > Close Project

2. File > New > Project from Existing Sources 

3. Select the folder where duke is located

4. Select Import Project from Existing Model and make sure Gradle is selected

5. Let IntelliJ do its work

6. Try launching the application again.
</panel>

<panel header="**19 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/60#issuecomment-531124948" expanded>

Thought I’d break the silence - cloned your code 2 days ago but no dice for me either. Mine returns an exit code of 255 instead, however.



Have you made any progress/found any new leads?
</panel>

<panel header="**20 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/134#issuecomment-542736815" expanded>

I think this is best illustrated with an example.



Let's say we have a while loop that can loop **up to** 100 times. 



For us to achieve a 100% statement coverage - we just need to test one iteration of the while loop. That executes all the statements within the while loop's code block - thereby achieving full statement coverage.



To achieve full path coverage, we have to test for every possible path - that means that we test the while loop for 1, 2, 3 ... 99, 100 iterations each time, to ensure that it produces the correct result each time. That's a far more comprehensive test, and only when all paths have been exhausted through testing can it be considered full path coverage. And definitely a lot more work to be done, testing-wise.



This applies to any form of conditionals or loops within a program - you'd have to test all possible number of iterations and/or all possible branches to ensure 100% path coverage, as compared to once for statement coverage.



Hope that illustrates it for you!
</panel>

<panel header="**21 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/138#issuecomment-544228983" expanded>

Remove the following lines from your build.gradle



`id 'org.openjfx.javafxplugin' version '0.0.7' //javafx` (line 6)

and

`javafx {

    version = "11.0.2"

    modules = [ 'javafx.controls', 'javafx.fxml' ]

}` (line 23-27)

they are no longer required as the JavaFX dependencies will be specified by lines 43 - 60 instead (you can also optionally choose to remove line 55 - 60 as they are unnecessary).



Your jar file generated by shadowJar should then be able to run on any system.



However, I noticed another bug during testing - your program won't launch if the file data/duke.txt is not present. You might want to look into ways to create the file automatically instead of throwing an exception and closing - see https://github.com/nus-cs2103-AY1920S1/forum/issues/27



Hope that helps! :)
</panel>

<panel header="**22 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/175#issuecomment-552260677" expanded>

Ah yes, I just checked this morning that it's now showing. It was probably browser caching. Thanks Prof!
</panel>

<panel header="**23 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/174#issuecomment-552355054" expanded>

This seems to only occur on Preview. Open the PDF in Chrome's PDF reader, or Acrobat Reader DC, and links work fine.



Maybe the tutors and peers grading can note that they should not use Preview to open PDF files.
</panel>

</panel>
<panel type="info" header="### JEONG YU HAN `@jeongyh99` (21 contributions)" expanded>
<panel header="**2. :fas-info-circle: Showing class variables in Object UML Diagrams**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/184" expanded>

How do we show static variables in Object Diagrams? Do we omit them or draw them in every instance of an object with underlining to show `static`-ness? Thank you!
</panel>

<panel header="**3. :fas-info-circle: Usage of VV**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/183" expanded>

Where any valid values are allowed in a test case, will we be penalized if we give the actual value instead? If so, what is the correct usage of VV (when do we use it as opposed to specifying the actual value?) Same goes for invalid values. Thank you!
</panel>

<panel header="**4. :fas-info-circle: Constructors in UML**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/182" expanded>

How do you show constructors in UML? Is it a class level variable (underlined) or instance with return type same as the method name?
</panel>

<panel header="**5. :fas-info-circle: Travis Tutorial/Requirements**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/82" expanded>

Regarding our pull requests, is it sufficient to follow the tutorial or do we have to ensure that Travis

"ticks" our pull requests? Thank you!!
</panel>

<panel header="**6. :fas-info-circle: Post Lecture Quiz**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/80" expanded>

Regarding the grading of the quiz, does the grader use the most recent completed quiz?

I have already completed my quiz and accidentally opened another quiz that I left unanswered. Will that affect how the grader? Thank you.
</panel>

<panel header="**7. :fas-info-circle: Week 5 Duke Query**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/49" expanded>

The project for week 5 mentions "Add at least one extension of your choice, selected from category B, C, or D". Does this mean that we should implement one of the tasks from one of the category or implement of of the categories? e.g. would doing "B-TentativeScheduling" from category B suffice or do I need to complete B-*tasks? Thank you!
</panel>

<panel header="**8. :fas-info-circle: Issue: No Tests were found**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/19" expanded>

All the methods look fine, followed the steps as explained. java test directory marked as green with no error. However, when I right click the class and run 'Test' it says "No tests were found".



The only thing I did differently was that when the step 5 where the suggestion was for me to add JUnit 4, which I opted to get JUnit 5.4 instead . Not sure if that is the issue, I would appreciate if anyone could help me.



Thank you!
</panel>

<panel header="**9. :fas-info-circle: Changing Pushed Code**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/6" expanded>

If we already pushed our code to Github with the tag for a certain level, what are the steps we should take if we later realized it is wrong and want to change our code to rectify the problem, assuming we already have moved on to higher levels? Thank you!!
</panel>

<panel header="**10. :fas-info-circle: IntelliJ created new package for me**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/5" expanded>

Suggestions and Auto Import somehow got disabled and it worked by setting src as my source directory. However, the IDE created a new directory for me and says I need to import java.main as it is now a package. Or something along those lines... is that going to be a problem for the bots to track my code?
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/5#issuecomment-522397588" expanded>

Thank you!
</panel>

<panel header="**12 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/6#issuecomment-522460553" expanded>

Thank you! I will try it out :)
</panel>

<panel header="**13 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/19#issuecomment-525153733" expanded>

![Result](https://user-images.githubusercontent.com/50542926/63745189-26bc3000-c8d4-11e9-885a-306966e8c254.PNG)

![TestCase](https://user-images.githubusercontent.com/50542926/63745192-26bc3000-c8d4-11e9-8016-4631c1cf0729.PNG)

![iml file](https://user-images.githubusercontent.com/50542926/63745194-26bc3000-c8d4-11e9-8532-2af97de77bde.PNG)

![Directories](https://user-images.githubusercontent.com/50542926/63745213-30459800-c8d4-11e9-8543-aea7b41f4e46.PNG)



Attached are the relevant screenshots! Once again thank you :-)
</panel>

<panel header="**14 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/19#issuecomment-525156962" expanded>

The icons when pressed are also unable to find the test cases.

Another method I tried but to do avail was by right clicking the methods in my code and generating each corresponding test method through IntelliJ, which also failed to detect my test cases.
</panel>

<panel header="**15 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/19#issuecomment-525198034" expanded>

Thank you for the help! My directory used to look like that until i started introducing packages, I am still trying to figure out what the issue is with my structure. My Run Configuration looks fine, but I am probably missing out something. I feel like I am going nowhere on Google either. I would be grateful if someone could point me in the right direction. Thank you!



![image](https://user-images.githubusercontent.com/50542926/63754576-aef80080-c8e7-11e9-88b7-130262d75542.png)
</panel>

<panel header="**16 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/19#issuecomment-525236488" expanded>

The issue has been resolved after the folders have been included. Thank you for the assistance 👍 
</panel>

<panel header="**17 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/49#issuecomment-528774332" expanded>

Thank you!
</panel>

<panel header="**18 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/80#issuecomment-532701993" expanded>

Thank you
</panel>

<panel header="**19 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/82#issuecomment-532702266" expanded>

Thank you for the clarification!
</panel>

<panel header="**20 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/182#issuecomment-554755394" expanded>

My concern is the methods compartment for Class Diagrams. Thanks prof! 💯 
</panel>

<panel header="**21 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/183#issuecomment-554755422" expanded>

Thank you!
</panel>

<panel header="**22 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/182#issuecomment-554768921" expanded>

Thank you!
</panel>

</panel>
<panel type="info" header="### ERWIN CHAN GUO XIN `@ChangUo79` (17 contributions)" expanded>
<panel header="**2. :fas-info-circle: Reading an image file in the same directory as the jar file**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150" expanded>

Please read up on how to write a [good question](https://stackoverflow.com/help/how-to-ask)



## Environment



Describe your development environment



- IntelliJ version: Intellij IDEA 2019.2.3

- Java version: 11.0.2

- Operating system version: Windows 10 Version 1903

- _other packages' versions_



## Issue

I am trying to implement a function to add an image to a profile of a person. Currently, I am retrieving the image files through the `resources/images/` directory. What I am trying to implement allows the user to add/edit the profile image by choosing their own image files that is in a folder `images` that is in the same directory as the jar file generated. I am having issues getting this to work. I have tried looking for solutions online but it doesn't seem to work.



Example:

![image](https://user-images.githubusercontent.com/54112270/67691710-fe3ada00-f9d9-11e9-9dba-d51c9f6d674b.png)



![image](https://user-images.githubusercontent.com/54112270/67691808-275b6a80-f9da-11e9-9703-1b660faa8b22.png)



## Code/Log Trace



For the first image, the way I retrieved my images is shown as:



```

private static final String IMAGE_DIRECTORY = "/images/";



    public Photo(String image) {

        requireNonNull(image);

        checkArgument(isValidFilePath(image), MESSAGE_CONSTRAINTS);

        value = image;

        photo = new Image(this.getClass().getResourceAsStream(IMAGE_DIRECTORY + image));

    }

```

The second image is my attempt to retrieve an image file in the `images` folder.

```

public Photo(String image) {

        requireNonNull(image);

        checkArgument(isValidFilePath(image), MESSAGE_CONSTRAINTS);

        value = image;

        File imageFile = new File(IMAGE_DIRECTORY + value);

        photo = new Image(imageFile.toURI().toString());

    }

```


</panel>

<panel header="**3. :fas-info-circle: Clarification for week 5s increment as pull request**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/67" expanded>

Previously, I did my increments on a separate branch but did a pull instead of a pull request and had already merged. I wanted to do the pull request anyway, so I added a commit each to the CodeQuality branch and the Assertions branch and created the pull request this way:



![image](https://user-images.githubusercontent.com/54112270/64906425-01735280-d719-11e9-801a-18eceb60f760.png)



Afterwards, I did a pull on my master branch on sourcetree and it became like this:

![image](https://user-images.githubusercontent.com/54112270/64906459-a42bd100-d719-11e9-9f52-6746a3f68071.png)



Now I am slightly hesitant to pull for CodeQuality and Assertions as more problems might arise. I looked through and it seemed fine but felt that it would be better to have a second opinion before proceeding.



Any help is greatly appreciated!


</panel>

<panel header="**4. :fas-info-circle: Error when executing jar file**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/58" expanded>

I have generated a new jar file using gradle. I am currently having issue executing the jar file as the same error keeps popping up:

![image](https://user-images.githubusercontent.com/54112270/64629717-4d2ab100-d426-11e9-81c3-b783e2a65bbd.png)



I have a launcher class which has the main method as well as a main class that extends javafx.application.Application but it seems that it is unable to detect either. Any solution on how to solve this problem?



Any help is appreciated.


</panel>

<panel header="**5. :fas-info-circle: Housekeeping done after level-6?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/8" expanded>

Are we penalized if we did the minimum requirement for a certain level and only do housekeeping/additional amendments after level 6? E.g. Minimum requirement for level-5 was to handle the 2 errors shown but I would like to make amendments after level-6.



Thanks for any help.
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/8#issuecomment-523354848" expanded>

Understood and thank you prof for your reply.
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/58#issuecomment-530006478" expanded>

do you mean changing the mainClassName to Launcher?

![image](https://user-images.githubusercontent.com/54112270/64630371-8fa0bd80-d427-11e9-9426-ccf5eb5bfb8c.png)


</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/58#issuecomment-530007872" expanded>

Its working now. Thanks! Do I need to be concern with this even though the jar is working:

![image](https://user-images.githubusercontent.com/54112270/64630609-0f2e8c80-d428-11e9-8372-7b5f20a6a42f.png)


</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/58#issuecomment-530190754" expanded>

Ahh missed that out. Thanks for the help!
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/67#issuecomment-531545407" expanded>

My concern was whether the pull request was done correctly as the master was merged into A-Assertions and A-CodeQuality shown in the picture.
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/67#issuecomment-531547827" expanded>

Understood! Thank you prof for the clarification 👍 
</panel>

<panel header="**12 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547052860" expanded>

> 

> 

> In the second case, `File imageFile = new File(IMAGE_DIRECTORY + value);` assumes that the given path starts from the project root directory (i.e. starting from `/main/...`). However, your image is actually stored in the resource folder, which is not the root level directory. The first case works because `getResourceAsStream` reads a file from `src/main/resources`.

> 

> You might want to consider letting your `IMAGE_DIRECTORY` = `src/main/resources/images/`. This will allow `new File(IMAGE_DIRECTORY + value)` to get the file from the root directory.



But what if the jar file isn't inside the project directory and moved to another directory with an `images` folder? For example, i moved the jar file to `Documents` and there is an `images` folder. How then would I retrieve the images? 
</panel>

<panel header="**13 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547261903" expanded>

> Ah I see! I suspect your solution would work if the jar file is actually the case as you mentioned. However, if you are still running from your IDE, this method would break down since `new File(...)` will attempt to read from the root project directory.

> 

> Have you tried building the jar file and manually testing to see if it works?



i built the jar file with an `images` folder and the relevant images in the `Documents` directory but it doesn't seem to work.






</panel>

<panel header="**14 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547262932" expanded>

> First, understand that files that are packaged in your jar file has to be accessed in a certain way (getResource). Files outside your jar can be accessed as usual.



I understand files in my jar file is accessed via `getResource`. So how should i access files outside of my jar in this case? 




</panel>

<panel header="**15 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547431043" expanded>

> 

> 

> > i built the jar file with an `images` folder and the relevant images in the `Documents` directory but it doesn't seem to work.

> 

> I examined your code further and realised that your `IMAGE_DIRECTORY` = `/images/` instead of `images/`.

> Placing a leading slash makes the path an absolute file path instead of a relative path, thus this references to `C:/images/` (assuming you're using Windows), instead of `C:/path/to/jar/folder/images/`.

> 

> In addition, `new Image(path)` requires `path` to start with `file://` in order to load the image through `ImageView`.

> 

> Hence, to sum up, you might want to try the following changes:

> 

>     * `IMAGE_DIRECTORY = images/`

> 

>     * `new Image("file://" + imageFile.toURI().getPath())`

> 

> 

> I've tried these changes on my end and it works through the jar file. Hope it works for you as well! :)



Thank you so much! Definitely working now. Really appreciate the help from everyone! Just one more question. Will this work only with jar files? I tried it in the IDE and the images dont show up. I imagine I will need to switch between methods depending on whether I'm working on it in the IDE or the jar file.
</panel>

<panel header="**16 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547439804" expanded>

> 

> 

> > Thank you so much! Definitely working now. Would this work with the IDE or only for jar files?

> 

> Glad to hear it works!

> 

> It should be able to work in the IDE as well, provided you have an `images` folder in your root project directory i.e. `main/images/`. You can specify this folder in `.gitignore` so that it won't be pushed into the remote repo.

> 

> Additionally, note that your application does not automatically create an `images` folder in the root directory, so you might want to consider automatically creating this folder when your user launches the app to aid your user.

Will take note of it. Thanks again for the help!
</panel>

<panel header="**17 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547781573" expanded>

Hello again! A new issue has arise after the previous issue was solved. Currently many of my test cases are failing due to this line ` photo = new Image("file://" + imageFile.toURI().getPath());` for some reason. From what I know, there is some initialization problem and there is trouble getting the images.



Some screenshots of the exceptions and errors:

![image](https://user-images.githubusercontent.com/54112270/67839179-0441cf80-fb2e-11e9-8cf3-b8d801012834.png)

![image](https://user-images.githubusercontent.com/54112270/67839256-2f2c2380-fb2e-11e9-857a-0291ceec1f17.png)



I tried looking for similar issue and came upon this: https://bugs.openjdk.java.net/browse/JDK-8093075 

The latest reply from the link says that this issue will not be fixed. Does anyone know any way around this problem? Greatly appreciate the help!
</panel>

<panel header="**18 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547832689" expanded>

> 

> 

> Hi!

> 

> I suspect the bulk of these errors goes down to the failure to initialize `Photo`. More specifically, this RuntimeException: `java.lang.RuntimeException: Internal graphics not initialized yet`.

> 

> In `Photo.java`, you are instantiating `photo` with type `Image`, which is a JavaFX component that depends on the JavaFX toolkit. This adds dependency to the JavaFX library right from the lower level classes. Thus, in unit testing, the JavaFX toolkit is not set up since only classes that extend `Application` (or subclasses of these classes) will start up the toolkit but here, only `MainApp.java` extends `Application`. Hence, `Image photo` cannot be instantiated.

> 

> Perhaps you can let the `Photo` class have an instance variable that contains the file path of the image file, then instantiate the `Image` within the `Ui` component using this file path!



Genius! Test cases have all passed. Thanks again for your help!
</panel>

</panel>
<panel type="info" header="### DANIEL TAN JUN XIAN `@CarbonGrid` (16 contributions)" expanded>
<panel header="**2. :fas-info-circle: Request to use TestFX**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/124" expanded>

## Library



https://github.com/TestFX/TestFX



## Purpose



GUI Testing
</panel>

<panel header="**3. :fas-info-circle: What is best practice for Serialization?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/52" expanded>

## Question



Since Java.io has a nifty way to serializing objects.

Is it recommended to always prefer using STL than writing base code from scratch?

Even if the object requires some obfuscation, the modification would be much easier while using STL.



## Intent



To reduce additional workload and size of code base than writing custom serialization to File for each required class. Implementing STL as CodeQuality improvement.
</panel>

<panel header="**4. :fas-info-circle: Tag A-Jar or v0.1?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/24" expanded>

As per title. I noted this issue when feedback-bot was looking for A-Jar instead.

https://nus-cs2103-ay1920s1.github.io/website/schedule/week3/project.html#2-do-increments-a-moreoop-a-packages-a-junit-a-jar



Above section states to use v0.1
</panel>

<panel header="**5. :fas-info-circle: Level-9**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/22" expanded>

Upon user input



find by

should the list return the following:

1. [E][1] talk to bystanders

2. [D][0] assignment (by: December 3 2019, 6:00PM)



or does the scope only applies to description with distinct separating whitespace?
</panel>

<panel header="**6. :fas-info-circle: Level-8**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/14" expanded>

How do we process the datetime requirement? 

Must the user provide a datetime or is it optional?

Do we strictly require user to provide entire datetime or do we allow for partial inputs?

E.g "22/08/2019 1300" vs "22/08/2019" or even "08/2019"
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/11#issuecomment-523878746" expanded>

You probably only need to understand the following:

git tag

git tag -d \<tagname\>

git tag -f \<tagname\>

git push --tags
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/14#issuecomment-524178167" expanded>

Noted.
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/22#issuecomment-525363191" expanded>

Noted.
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/24#issuecomment-526035794" expanded>

Noted.
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/34#issuecomment-526826514" expanded>

Are you running on JDK 11?
</panel>

<panel header="**12 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/52#issuecomment-529124683" expanded>

Sorry for some confusion.

What I meant:

Obfuscation - transient fields where we alternatively provide a hash in place.

STL - Wrong usage. I forgot STL doesn't mean Standard Libraries.

Modification - writing additional data alongside with serialized data.
</panel>

<panel header="**13 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/52#issuecomment-529125295" expanded>

I think the only factors whether to use standard libraries or not are: 

-Ease of implementation and future extensions

-Visibility

-Size of Overheads



From this

`E0music festival2/12/2019T2000T1borrow bookE0movie4/12/2019T1355D0D1 Project Assignment5/12/2019T1357`



to this

`¬í sr 

duke.TaskListÑlM¬ã,Á L lst Ljava/util/ArrayList;xpsr java.util.ArrayListxÒ™Ça I sizexp   w   sr duke.task.Eventh¡NvDZ2Ì L att Ljava/time/LocalDateTime;xr duke.task.Taskk]ž9“ú Z isDoneL descriptiont Ljava/lang/String;xp t Music Festivalsr 

java.time.Ser•]„º"H²  xpw	  ãÄxsr duke.task.TodoÓ»æËgï—  xq ~ t borrow booksq ~  t Moviesq ~ w	  ã þxsr duke.task.DeadlineR66<˜I L byq ~ xq ~  t D1 Project Assignment | Team 1sq ~ w	  ã þxx`
</panel>

<panel header="**14 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/52#issuecomment-529128044" expanded>

It's not explicitly shown but avoidance of custom written parser and serialization should reduce the possibilities of bugs, I think? Since standard libraries are battle-tested.



IMO, I'm currently thinking that using standard libraries instead of custom written code base improves:

- Reliability

- Maintainability

- Testability

- Portability

- Reusability



Not too sure if that kind of concept is true.
</panel>

<panel header="**15 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/55#issuecomment-529921392" expanded>

Is your build.gradle application targeting Launcher?
</panel>

<panel header="**16 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/55#issuecomment-529942898" expanded>

https://stackoverflow.com/questions/48396274/how-to-enable-assertions-in-the-gradle-run-task
</panel>

<panel header="**17 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/55#issuecomment-529943240" expanded>

Lol didn't test if -ea works configured in VM options. I assumed it did.
</panel>

</panel>
<panel type="info" header="### JEREMY TAN JIERUI `@Parcly-Taxel` (13 contributions)" expanded>
<panel header="**2. :fas-info-circle: Closing issues from the PE-D/PE**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/161" expanded>

Can we close (but obviously not delete, since both repositories will be checked in the tutor grading) the bugs we created in the dedicated repositories for the practical exam dry run and (in two weeks' time) the practical exam itself?
</panel>

<panel header="**3. :fas-info-circle: The 100th issue**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/100" expanded>

This is the 100th issue in this forum. Congratulations! :100:



I have a question for discussion. We are developing software that can quite easily be changed and tested, without much cost, and in doing so we are following some software engineering principles. However, there are some software projects where the relevant software **cannot** be changed once it is deployed, and where any error **is** fatal to the system (and possibly to people too).



![](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1c/Parker_Solar_Probe.jpg/640px-Parker_Solar_Probe.jpg)



One example is the Parker Solar Probe (NASA illustration above). Because it goes so close to the sun, any error in the alignment of its solar shield **will** permanently damage its electronics. The same applies for almost all space probes and manned spaceflights.



What kinds of software engineering principles would apply to these special projects?
</panel>

<panel header="**4. :fas-info-circle: 💡 Dont get the dreaded This branch is out-of-date with the base branch error**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/99" expanded>

I made a note in [my most recent pull request](https://github.com/AY1920S1-CS2103T-F11-4/main/pull/10) on my team's project repo:

![Remember to set your upstream repo and fetch from the latest base branch version before opening a pull request!](https://user-images.githubusercontent.com/54175463/65835291-1950f600-e317-11e9-81df-c4da4a96bdea.png)



Our team was getting many "this branch is out-of-date with the base branch" messages on pull requests, like the one below:

![out of date](https://user-images.githubusercontent.com/54175463/65835326-8bc1d600-e317-11e9-82b0-34e5764625e0.png)



But this causes headaches when syncing with the local repos. To avoid this:

* follow the instructions in [the GitHub help page linked in the pull request description above](https://help.github.com/en/articles/configuring-a-remote-for-a-fork) to add the upstream repo (`git remote add upstream ...`)

* `git pull` the latest changes from upstream (`git pull upstream master`)

* `git push` to the forked repo

* and finally check that in the branch to be merged there is no "_n_ commits behind" in the commit count description above the file list. The first one is bad and will cause the out-of-date error, the second one is good and will not:

![Will cause an out-of-date error](https://user-images.githubusercontent.com/54175463/65835410-80bb7580-e318-11e9-850b-04d405bcec94.png)

![Won't cause an out-of-date error](https://user-images.githubusercontent.com/54175463/65835360-fc68f280-e317-11e9-8459-907c80b58722.png)



P.S.

![Iroha](https://user-images.githubusercontent.com/54175463/65835309-50270c00-e317-11e9-9ecb-e7eb6dc0dd7f.png)
</panel>

<panel header="**5. :fas-info-circle: Tangled Git logs**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/87" expanded>

I have this strange Git log for [my personal repository](https://github.com/Parcly-Taxel/main) which is my fork of [my team's repository](https://github.com/AY1920S1-CS2103T-F11-4/main) (I am the team repo's owner):



![Strange Git log](https://user-images.githubusercontent.com/54175463/65345997-321e2500-dc0e-11e9-9be1-b939fc96cde6.png)



I've finished the two tutorials for week 6, and both requisite branches are present. I've also made a PR for my ``tutorial-adding-command`` branch, and the tangled lines in the log are a result of me pushing a few more commits to get used to the workflow and integrations for the team project, which caused my PR to have merge conflicts with the team repo's master branch (these conflicts, I fixed, naturally).



Do I need to do anything about the gnarly graphs? Or is it fine?


</panel>

<panel header="**6. :fas-info-circle: Renaming the individual project after week 7**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/68" expanded>

After week 7, our individual projects will have been graded. Can we rename our iP repositories to anything we like after that point?



(By tradition, all my repositories are named after real-world places: Selwyn [College, Cambridge], Kinross [Scotland], Dounreay [Scotland], Shinjuku [Tokyo] and here Bari [Italy]. In the first four repos listed here, the actual name of the repo &ndash; what goes into the URL &ndash; matches the assigned name as used in the readme. But we are under orders not to change the repo name for our Duke forks until an indeterminate time in the future, which is why this question was asked.)
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/20#issuecomment-531510517" expanded>

_The Mythical Man-Month_ advises that if there is a software construct (or library you can use) that already provides the functionality you want, why bother reinventing the wheel? Vis-à-vis exceptions, this means eschewing writing extensions to exceptions.



In my iP as it has been recently released, there are no custom exceptions; the only exception used is `IllegalArgumentException`.
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531510959" expanded>

That's the team project. You can pretty much ignore checkstyle for that; only the unit tests need to pass. (Changing the imports to please checkstyle would take too long.)
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/88#issuecomment-533763651" expanded>

The strange thing is, even after complaining about the test failures in the lecture, I managed to fix them with the IDE debugger, around nine hours before this announcement (see #87 and my branch's commits linked from there, e.g. [this](https://github.com/Parcly-Taxel/main/commit/8475c2f822eecf570a475af7250f18d313acd292)). Setting breakpoints in the code helped to show which test objects had not been updated to use the new remark syntax.
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/88#issuecomment-536283869" expanded>

When are you going to close this one?
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/106#issuecomment-537769952" expanded>

The way to push the tags to the team repo from the command line is as follows:



* one who has write access to the team repo does `git tag -a "v1.1" -m "v1.1"` (the `-m` option is just for completeness), then `git push` on said team repo

* all team members do the same steps as detailed in #99 to get the tag on their forks, except that the `--tags` option is added to both commands
</panel>

<panel header="**12 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/114#issuecomment-539900988" expanded>

If you don't want to highlight and press R, this specific markup is achieved with `>` at the start of a line.

`>quoted text`

>_Right._



- [ ] Question: how do you create that keycap look? ![image](https://user-images.githubusercontent.com/54175463/66465407-61101400-eab3-11e9-9766-4827a4fdd646.png)




</panel>

<panel header="**13 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/161#issuecomment-549135468" expanded>

@damithc In any case, when can we mark them as closed?
</panel>

<panel header="**14 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/161#issuecomment-549203407" expanded>

I heard that some things I wanted to do could not be done until 2020, what are they?
</panel>

</panel>
<panel type="info" header="### GE SHUMING `@geshuming` (13 contributions)" expanded>
<panel header="**2. :fas-info-circle: 💡 Get rid of trailing whitespace or no newline at EOF errors on Travis**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/140" expanded>

## Issue



Travis seems to fail the build and emit `Trailing whitespace` or `No newline at EOF` errors, despite our team passing the corresponding gradle tasks `checkstyleMain`, `checkstyleTest` 



![image](https://user-images.githubusercontent.com/43642522/67226276-2456fc00-f467-11e9-9b30-a0a442047193.png)



## Solution



Apparently this is due to the extra `run-checks.sh` script being run on travis. I added the following lines to the `build.gradle` file so that the `check` task also runs the travis script. Any suggestions are welcome.



```gradle

task extrachecks(type: Exec) {

    commandLine 'bash', './config/travis/run-checks.sh'

}



tasks.check {

    dependsOn extrachecks

}

```



This way, you can run the `check` task on your local repo and fix any issues before submitting to travis.
</panel>

<panel header="**3. :fas-info-circle: iP: Level 3: Java displays ? instead of tick or cross**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/4" expanded>

**OS**: Microsoft Windows [Version 10.0.17134.950]

**Java**: 

```

java 11.0.2 2019-01-15 LTS

Java(TM) SE Runtime Environment 18.9 (build 11.0.2+9-LTS)

Java HotSpot(TM) 64-Bit Server VM 18.9 (build 11.0.2+9-LTS, mixed mode)

```

**Expected Result**:

```

list

1.[✓] add book

2.[✘] read book

```



**Actual Result**:

```

list

1.[?] add book

2.[?] read book

```



**Additional info**:

I tried echoing the unicode characters in `cmd.exe` and `bash.exe` and both worked fine. However, running jshell tells me that java is somehow not properly converting the unicode character into a string.



I used the partial solution given:

```java

    public String getStatusIcon() {

        return (isDone ? "\u2713" : "\u2718"); // return tick or X symbols

    }

```



Any help will be appreciated.
</panel>

<panel header="**4. :fas-info-circle: OK to implement increments out of order?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/1" expanded>

Is it an issue if we do some increments out of order? For example doing `A-Gradle` at the very beginning, before `Level-1`. 
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/1#issuecomment-522250367" expanded>

Thank you for the response professor.



I just realised that you can apply lightweight tags to the same commit multiple times. I suppose I can then tag the increment before/after `A-Gradle` with `A-Gradle`, thus keeping the tags in the same order. 
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/41#issuecomment-527713431" expanded>

https://github.com/nus-cs2103-AY1920S1/duke/blob/master/tutorials/gradleTutorial.md#checkstyle



Follow the tutorial exactly and include this config into your build.gradle



```

checkstyle {

    toolVersion = '8.23'

}

```



If you don't have the above config, the default tool version won't work with the checkstyle xml provided


</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/64#issuecomment-531179659" expanded>

The problems is in the log :)



Lines 221 and 222
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/86#issuecomment-533248033" expanded>

Just look at the exception thrown by your java files: 



```

Caused by: java.time.format.DateTimeParseException: Text '12/12/12 1000-1800' could not be parsed, unparsed text found at index 13

        at java.base/java.time.format.DateTimeFormatter.parseResolved0(DateTimeFormatter.java:2052)

        at java.base/java.time.format.DateTimeFormatter.parse(DateTimeFormatter.java:1951)

        at java.base/java.time.LocalDateTime.parse(LocalDateTime.java:492)

        at misc.Parser.formatDeadline(Parser.java:153)

        at misc.Parser.convertStringToTime(Parser.java:90)

        at task.Deadline.<init>(Deadline.java:32)

        at misc.Parser.readTextAsTask(Parser.java:64)

        at misc.Storage.readTasksIntoTaskList(Storage.java:87)

        at misc.Storage.readSaveFile(Storage.java:77)

        at duke.Duke.<init>(Duke.java:33)

        at duke.Main.<init>(Main.java:16)

        ... 14 more

```



It seems like your deadline object is trying to parse an event datetime string, hence the errors. 
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/86#issuecomment-533251574" expanded>

Nothing wrong with the above output, but the stack trace shows there might be a problem with your storage parsing. 



I'm just guessing it's untested behavior from saving an event task and loading it (somehow tries to load it as a deadline task). You can try clearing your savefile and see if your jar file opens without issue?
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547012702" expanded>

Have you checked if the `photo` is actually created, and that no errors were raised and dropped by the AddressBook?



I suspect that the URI does not actually translate into URL. Otherwise, I think it might be due to the lack of escape slashes in the string.
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552066906" expanded>

You can try triggering a custom build on travis, and run `./gradlew asciidoctor --info` to see what could be causing the issue?
</panel>

<panel header="**12 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552067286" expanded>

Under "more options", click on the "Trigger build" option and insert a custom yaml config to 



![image](https://user-images.githubusercontent.com/43642522/68523268-a19cc080-02f1-11ea-94ee-78ed46680304.png)


</panel>

<panel header="**13 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/168#issuecomment-552164586" expanded>

For positioning in HTML, I modified the `asciidoctor.css` file in `/stylesheets` to align the imageblocks. 

[The commit I made can be found here](https://github.com/AY1920S1-CS2103T-W13-1/main/commit/1637f6f60f1423dd00a76585ec49ce15723ef91d) It was a small fix that didn't warrant installing applications/plugins, in my opinion. 



> it is currently not possible to do so for captions in HTML



My commit also aligns the caption, so for anyone wondering if you can, you can.
</panel>

<panel header="**14 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/168#issuecomment-552166720" expanded>

> Edit: Didn't manage to get this to work for me though :(



I don't think it shows up in the preview on the IDE, but it shows up for my team's site as well as deployment previews
</panel>

</panel>
<panel type="info" header="### KHENG YAU DONG `@ChrisKheng` (13 contributions)" expanded>
<panel header="**2. :fas-info-circle: Project Portfolio Page**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/177" expanded>

Hi Prof, can we use the same overview across all project portfolio pages of team members to ensure consistency?
</panel>

<panel header="**3. :fas-info-circle: Submission of Product on Week 13 Monday**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/160" expanded>

Hi prof, regarding the submission of product on week 13 Monday, does everyone from the group need to submit all the submissions listed [here](https://nus-cs2103-ay1920s1.github.io/website/schedule/week13/project.html#2-submit-the-deliverables-by-monday-2359) to Luminus? Or just one representative from the group submit them?
</panel>

<panel header="**4. :fas-info-circle: Project Root Directory**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/16" expanded>

Hi prof, is the term "project root directory" refers to the "src/main/" folder or the topmost folder that consists of all the folders including "src/main/" ?
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/16#issuecomment-524497027" expanded>

Alright thanks!
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-527309677" expanded>

Maybe it would be good to remove the duplicated module by going to project structure >> module, and remove the 'main' module which is duplicated, cuz the issue of duplicated modules has just caused problems for my code when trying to use some javafx methods.
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/53#issuecomment-529379489" expanded>

I think the main course behind the issue "could not find or load main class Duke" is because java cannot find the `.class` file of Duke to load it. When Duke was in the `package duke`, was the `mainClassName` in your gradle is `duke.Duke`? 
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/78#issuecomment-532497316" expanded>

Uhm what did you put for the `mainClassName` in your `build.gradle` file though? Is it `duke.Launcher`? If yes, did you put your `Launcher` class inside a package called `duke`?
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/78#issuecomment-532501232" expanded>

Hmm did you push your latest change to github? Maybe I can help to inspect the jar error
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/78#issuecomment-532501493" expanded>

By the way, did you use gradle to make the jar?
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/88#issuecomment-533758439" expanded>

I faced similar issues as well and what I did is I first determine which test fails first and also why it fails (from the console which shows the assertions error). The most common problem I faced is the actual `Command` or `CommandResult` generated is **not equal** to the expected one. It's usually due to differences in some values, for example, the content of the `remark` in the `CommandResult`, which is usually because of putting different values for the field in where the expected result is generated and where the actual command is generated. (sometimes the result is generated from the data file)





I put a breakpoint at the relevant line before the assertion in the test method (which fails) and run the debugger and track the value of `Command` and/or `CommandResult` step by step, stepping into the relevant methods as necessary. I focus especially on the value(inner content) of `Command` or `CommandResult`, e.g. `name` and `address`. When I found out the point **where the difference in value occurred**, I will do some backtrack to find **where** the actual `Command` and/or `CommandResult` is generated to see what causes the differences in value and then fix it accordingly.





Hope this helps! 
</panel>

<panel header="**12 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/106#issuecomment-536930492" expanded>

I think you can click on `releases` in the repo page of your team, then click on `new release`. You can then add a tag there which will tag the latest commit of your team repo.

<img width="747" alt="Screenshot 2019-10-01 at 4 32 51 PM" src="https://user-images.githubusercontent.com/42091735/65946677-401f4180-e469-11e9-94f5-980a309dd43c.png">


</panel>

<panel header="**13 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/160#issuecomment-549132446" expanded>

Alright, thanks prof!
</panel>

<panel header="**14 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/177#issuecomment-552430529" expanded>

Ok thanks prof!


</panel>

</panel>
<panel type="info" header="### TAN YUANHONG `@le0tan` (12 contributions)" expanded>
<panel header="**2. :fas-info-circle: If your UG/DG doesnt build, its probably GitHubs fault, not yours 💡**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/165" expanded>

![image](https://user-images.githubusercontent.com/28982486/68223852-851a3300-0028-11ea-83a1-f6a9155cb0e1.png)



Looks like GitHub doesn't respond to page rebuilding requests for several hours, right before the milestone check for tonight =)
</panel>

<panel header="**3. :fas-info-circle: Module websites description on PPP is incorrect**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/149" expanded>

In [this section](https://nus-cs2103-ay1920s1.github.io/website/admin/tp-deliverables.html#deliverable-tp-portfolio-page-ppp) of the module website, the format of the code contributed URL is incorrect. It should be:



https://nus-cs2103-ay1920s1.github.io/tp-dashboard/#search=le0tan



where "le0tan" is replaced with your GitHub username.
</panel>

<panel header="**4. :fas-info-circle: Update library.md**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/pull/126" expanded>

Fixed a typo and add markdown style URL template
</panel>

<panel header="**5. :fas-info-circle: Request to use ControlsFX**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/125" expanded>

## Library



[ControlsFX](https://github.com/controlsfx/controlsfx)



## Purpose



Provide auto-completion for textfields.


</panel>

<panel header="**6. :fas-info-circle: How to configure IDEA so that Optimize Imports doesnt ruin styleCheck?:thinking:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66" expanded>

I configured IDEA's Java code style according to [this](https://nus-cs2103-ay1920s1.github.io/addressbook-level3/SettingUp.html). However the check style still complains about the import style:



![image](https://i.imgur.com/VL1MLM6.png)
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531530064" expanded>

> > That's the team project. You can pretty much ignore checkstyle for that; only the unit tests need to pass. (Changing the imports to please checkstyle would take too long.)

> 

> Not true :-) Following a consistent style is even more important for a team project.

> 

> @le0tan Are you able to pass the checkstyle check via gradle?



No =(
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531530097" expanded>

> @le0tan also post screenshots of the relevant parts of your IDEA code style settings.



![pic1](https://i.imgur.com/CyLuFNs.png)

![pic2](https://i.imgur.com/I4u7mfV.png)
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531533607" expanded>

> > No =(

> 

> That's odd. AB3 is passing the checkstyle check on Travis. Unless you changed the code, it should pass for you as well. BTW, perhaps you should set up IDE coding style for each project rather than change the default settings.

> 

> Let's wait to see if anyone else faces this problem. In the meantime, not use _optimize imports_ feature?



The thing is... I set IDEA to automatically organize the imports for every commit. So it messed up the import order of **EVERY** .java file in the project and there's no easy way of reverting it.



I didn't push this change to our team's repo so currently it's not a big problem. It only affects my "get familiar with AB3" tutorial branches.



This is the [branch](https://github.com/le0tan/main/tree/tutorial-adding-command) I pushed to.
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531533678" expanded>

Is it possible for someone whose IDEA properly optimizes imports to upload their `.idea` folder so that we can overwrite ours?
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531535544" expanded>

> I notice that your checkstyle.xml is blue (i.e. has been edited). Are you certain that you're using the checkstyle as-is from the repo?



I made sure it's exactly the same by copy-pasting the content from the AB3 repo =)
</panel>

<panel header="**12 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531535778" expanded>

As mentioned in slack, I commented out import sections in checkstyle.xml
before to stop Travis from complaining... I copy-pasted to ensure the
changes are reverted properly.

On Sun, 15 Sep 2019 at 1:19 PM, Damith C. Rajapakse <
notifications@github.com> wrote:

> I made sure it's exactly the same by copy-pasting the content from the AB3
> repo =)
>
> The file is already in the repo. Can use as is. Why need to copy-paste?
>
> —
> You are receiving this because you were mentioned.
> Reply to this email directly, view it on GitHub
> <https://github.com/nus-cs2103-AY1920S1/forum/issues/66?email_source=notifications&email_token=AG5DZVS5MI4TTQRRAGY4XVLQJXAV7A5CNFSM4IWWSZO2YY3PNVWWK3TUL52HS4DFVREXG43VMVBW63LNMVXHJKTDN5WW2ZLOORPWSZGOD6XJOGI#issuecomment-531535641>,
> or mute the thread
> <https://github.com/notifications/unsubscribe-auth/AG5DZVR34IHFA7GGWLSHPRLQJXAV7ANCNFSM4IWWSZOQ>
> .
>
-- 
Regards,

Tan Yuanhong

</panel>

<panel header="**13 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531538515" expanded>

> I think a diff of your CommandTestUtil class will tell you what's wrong.



Looks like IDEA would only optimize imports on changed files, and that was the reason why it didn't apply the new rules to all files. I right clicked on src folder and optimized every file inside and now it passed tests. Thanks!
</panel>

</panel>
<panel type="info" header="### EUGENE TEU CHU WEI `@EugeneTeu` (12 contributions)" expanded>
<panel header="**2. :fas-info-circle: Broken Reposense link when generating PDF due to url encoding  (Mac issue, see comment for fix)**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/174" expanded>

Hello guys, I'm facing an issue where the hyper link to the reposense code is changed during the conversion to pdf (likely due to URL encoding) : 



in particular, from 



`https://nus-cs2103-ay1920s1.github.io/tp-dashboard/#search=eugeneteu&sort=groupTitle&sortWithin=title&since=2019-09-06&timeframe=commit&mergegroup=false&groupSelect=groupByRepos&breakdown=false&tabOpen=false`



[working link](https://nus-cs2103-ay1920s1.github.io/tp-dashboard/#search=eugeneteu&sort=groupTitle&sortWithin=title&since=2019-09-06&timeframe=commit&mergegroup=false&groupSelect=groupByRepos&breakdown=false&tabOpen=false)



to 



`https://nus-cs2103-ay1920s1.github.io/tp-dashboard/%23search=eugeneteu&sort=groupTitle&sortWithin=title&since=2019-09-06&timeframe=commit&mergegroup=false&groupSelect=groupByRepos&breakdown=false&tabOpen=false`





note the # turning into %23. 



I been searching around for a fix so was wondering if anyone here managed to fix this already. Note that all other hyper links work in the pdf. 



Many thanks!
</panel>

<panel header="**3. :fas-info-circle: Travis build fails to respond after integrating GUI test**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/141" expanded>

## Environment



Describe your development environment



- IntelliJ version: 11.0.3

- Java version: java 11 2018-09-25

- Operating system version: MacOs

- _other packages' versions_



## Issue



Hey guys I integrated the GUI tests from AB4 and wrote some unit tests. On my local terminal, everything works fine (all tests pass) and check style passes but somehow on Travis, the build stalls after starting the GUI tests. 



This causes Travis to trigger an error message stating that there's no output. 



Was wondering if anyone has ran into this issue when setting up their GUI test.



## Code/Log Trace



For code, you can link to your branch on GitHub. For short code snippets, you can copy and paste in code block:





[link to failing PR Build](https://github.com/AY1920S1-CS2103T-T09-4/main/pull/139)



[link to my branch](https://github.com/EugeneTeu/main/tree/GUI-tests)





This is the log from the Travis build. 

```

 seedu.address.ui.CustomerListPanelTest > performanceTest() STARTED



No output has been received in the last 10m0s, this potentially indicates a stalled build or something wrong with the build itself.

Check the details on how to adjust your build configuration on: https://docs.travis-ci.com/user/common-build-problems/#build-times-out-because-no-output-was-received



The build has been terminated



```



The fix that travis directs me to is to simply wait for longer (right now the build terminates after 10 mins)but as my tests are working fine, its probably an issue of me not integrating the gui test properly with travis.



 I have also tried manually running the Gradle method that travis runs and it works fine on my local terminal! 



Will appreciate it if someone could point me in the right direction  


</panel>

<panel header="**4. :fas-info-circle: Request to use Statistics Generation library**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/118" expanded>

## Library



Commons Math: The Apache Commons Mathematics Library

https://commons.apache.org/proper/commons-math/userguide/stat.html



## Purpose



To use it to calculate statistics on my data


</panel>

<panel header="**5. :fas-info-circle: 💡IntelliJ Debugger cant run? AB3 Project seems broken on intellij? Setup your project properly**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/85" expanded>

Lesson learnt in reading your documentation: 

https://nus-cs2103-ay1920s1.github.io/addressbook-level3/SettingUp.html



From section ```2```

To get ur debugger/Intellij to run properly, remember to import the project by clicking

 ```import project``` -> selecting your ```build.gradle``` file. 

Your intellij should import the entire project correctly and everything should work. 



PS: spent an hour trying to figure out why my Intellij was not running properly and even reinstalled my jdk ._. 
</panel>

<panel header="**6. :fas-info-circle: Request to use Apache POI to write to excel files**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/76" expanded>

## Library

Apache POI 

https://poi.apache.org/



## Purpose



We like to be able to read input from excel file and then write to excel file using the APACHE POI api 

(For TP)  


</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/76#issuecomment-532312329" expanded>

Thanks prof! 
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/141#issuecomment-545354452" expanded>

yes. 



My output is this, ignoring ascii doctor warnings (which does not seem to have an effect on the tests): 

<img width="1336" alt="Screenshot 2019-10-23 at 5 24 15 PM" src="https://user-images.githubusercontent.com/43085751/67378582-0fd74880-f5ba-11e9-8153-a3cb5a01645e.png">


</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/141#issuecomment-545477846" expanded>

Good news! found a fix for this: 

enabling xvfb mode to run before the script in the travis.yml file seems to fix it, under `services` and the `before_script` section. My build successfully pass after including that. 



```

language: java

matrix:

  include:

    - jdk: openjdk11

services:

  - xvfb



before_script:

  - export DISPLAY=:99.0



script: >-

    ./config/travis/run-checks.sh &&

    ./gradlew clean checkstyleMain checkstyleTest test coverage coveralls asciidoctor



deploy:

  skip_cleanup: true

  provider: script

  script: ./config/travis/deploy_github_pages.sh

  on:

    branch: master



before_cache:

  - rm -f  $HOME/.gradle/caches/modules-2/modules-2.lock

  - rm -fr $HOME/.gradle/caches/*/plugin-resolution/



cache:

  directories:

    - $HOME/.gradle/caches/

    - $HOME/.gradle/wrapper/

```



[From official documentation](https://docs.travis-ci.com/user/gui-and-headless-browsers/)



Hopefully anyone else wanting to integrate GUI-tests into their TP can refer to this fix if their tests fail too! Thanks @damithc and @j-lum for your input!
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/174#issuecomment-552272793" expanded>

> I checked a PPP from last year and it doesn't seem to have this problem 🤔

> ![image](https://user-images.githubusercontent.com/1673303/68554879-d16cd500-0465-11ea-9164-72e1c5ddf31e.png)



Attached is my friend's PPP after conversion to PDF. I have tried opening the link in chrome and using other pdf generation methods but still give me the same 404 result : 



![image](https://user-images.githubusercontent.com/43085751/68557344-899f7b00-0470-11ea-8bca-b0056c6cf396.png)



Very strange behaviour
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/174#issuecomment-552277320" expanded>

Did some digging, seems like this issue is limited to Mac users :/
</panel>

<panel header="**12 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/174#issuecomment-552281206" expanded>

@damithc 

Strange, the link works when I sent the pdf to my windows / linux users, but Mac users face similar issues on their local files.  



I confirmed this result with a spare windows laptop I have lying around. 



So it seems like we would still be able to submit the pdf, just that Mac users will face a broken reposense link 
</panel>

<panel header="**13 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/174#issuecomment-552282310" expanded>

Ok. Changed the title of the pr to reflect this issue for Mac users! 
</panel>

</panel>
<panel type="info" header="### LOW JUN KAI, SEAN `@seanlowjk` (12 contributions)" expanded>
<panel header="**2. :fas-info-circle: Error For Team Tags When Using Catcher**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/179" expanded>

It seems after Using Catcher, the Tags for the Team will change: 



![image](https://user-images.githubusercontent.com/42912708/68995823-0301f800-08cd-11ea-990d-4972c506814e.png)



Whereas the original tags are like this: 



![image](https://user-images.githubusercontent.com/42912708/68995826-0b5a3300-08cd-11ea-9522-d38a415d4ef5.png)



My question is: are we supposed to follow the team tags for the first or second photo? 

Thanks!
</panel>

<panel header="**3. :fas-info-circle: Bug:Post-Lecuture LumiNUS Quiz 7 Part 2 Sends to wrong URL**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/113" expanded>

![image](https://user-images.githubusercontent.com/42912708/66266429-86084b00-e857-11e9-9402-bc6137355d9c.png)



Another bug spotted! 🐛 
</panel>

<panel header="**4. :fas-info-circle: Bug: Post-Lecture LumiNUS Quiz 6 Sends to wrong URL**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/94" expanded>

![image](https://user-images.githubusercontent.com/42912708/65671649-2ef5bf80-e07a-11e9-875c-820ac6e56e9a.png)



![image](https://user-images.githubusercontent.com/42912708/65671634-29987500-e07a-11e9-86ea-d0aa3832d895.png)



There might be a bug here! 🐛 
</panel>

<panel header="**5. :fas-info-circle: What if used JDK 12 instead of JDK 11 to compile?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/74" expanded>

Hi important question! 



If we were to use JDK 12 to compile my program, will we be penalized if done so? 

Is it a must to use JDK 11 instead of JDK 12 to compile?



Thanks!
</panel>

<panel header="**6. :fas-info-circle: cs2103-feedback-bot does not give feedback for students on Friday tutorial slots**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/65" expanded>

Hi! 



It appears for students who have Friday CS2103T tutorial slots, they do not have the relevant feedback given to them via the cs2103-feedback bot. 



![image](https://user-images.githubusercontent.com/42912708/64902651-e0414080-d6dd-11e9-8c3e-be85a758dec2.png)



May I know if this is intentional or there might be some bug? As me and my friends who take Friday Tutorial slots have yet to receive the Issue from the bot.



Thanks! 
</panel>

<panel header="**7. :fas-info-circle: javaFX: correct way to fix error for Launcher run?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/30" expanded>

![image](https://user-images.githubusercontent.com/42912708/64006282-96d0ed00-cb44-11e9-9827-6c980a93fa39.png)

In the event that you receive this error while trying to run the Launcher class

![image](https://user-images.githubusercontent.com/42912708/64006370-c4b63180-cb44-11e9-9b35-4b6ec969923b.png)

This is what I did to fix this error. To change the constructor to take in 0 parameters. 

![image](https://user-images.githubusercontent.com/42912708/64006675-5d4cb180-cb45-11e9-8ab0-0b68677f30b8.png)

Not sure if this is supposed to be intended to work as above, appreciate any advice to be given, thanks! 






</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/30#issuecomment-526816381" expanded>

Ok thanks! :)
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/65#issuecomment-531473607" expanded>

Ok thank you Prof! 😄 
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/74#issuecomment-532016859" expanded>

Ok thank you for the answer Prof! 😄 
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/115#issuecomment-539069667" expanded>

Thanks for sharing this piece of information Yu Ting! 


</panel>

<panel header="**12 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/121#issuecomment-543012264" expanded>

Do change the url to: 



`https://coveralls.io/repos/github/YOUR_REPOS/badge.svg?branch=master&service=github`for the image. 



Do let me know if there are still problems with your coveralls not updating. 
</panel>

<panel header="**13 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/179#issuecomment-554651774" expanded>

Ok thank you Prof! 👍 
</panel>

</panel>
<panel type="info" header="### SAHIL S/O SANJEEV GATHANI `@Sahilgat` (11 contributions)" expanded>
<panel header="**2. :fas-info-circle: Issue when setting up Travis CI for group project and enabling auto-publishing of documentation**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/64" expanded>

Please read up on how to write a [good question](https://stackoverflow.com/help/how-to-ask)



## Environment



Describe your development environment



- IntelliJ version: IntelliJ IDEA 2019.2.2 (Community Edition)

- Java version: 11.0.4

- Operating system version: Windows 10 Home Version 1809



## Issue



![Error](https://user-images.githubusercontent.com/38809578/64851714-90fe0000-d64a-11e9-8b61-c48b9ffe23f8.PNG)

*Break*

![Error 2](https://user-images.githubusercontent.com/38809578/64852262-99a30600-d64b-11e9-8730-4296b1e8e18b.PNG)

*Break*

![Error 3](https://user-images.githubusercontent.com/38809578/64852266-9c056000-d64b-11e9-80a6-2b5cd0719f6d.PNG)

*Break*



Hi I've been having this issue when trying to set-up Travis CI for the group project and enable the auto-publishing of docs. The error seems to be the line in red, and I've tried running the gradle test and checkstyle tests individually with both pass so I'm not sure what's wrong. The only files changed were the readme.adoc and the .iml files that got added I believe from setting it up as an IntelliJ project. Does anyone have any idea what might be wrong?


</panel>

<panel header="**3. :fas-info-circle: Error when trying to run checkstyle with Gradle**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/41" expanded>

Hi,



I'm getting the following error when using the "gradlew checkstyleMain checkstyleTest" command (Screenshot below):

Unable to instantiate 'MissingJavadocMethod' class, it is also not possible to instantiate it as .MissingJavadocMethod, MissingJavadocMethodCheck, .MissingJavadocMethodCheck. Please recheck that class name is specified as canonical name or read how to configure short name usage https://checkstyle.org/config.html#Packages. Please also recheck that provided ClassLoader to Checker is configured correctly.



![Capture](https://user-images.githubusercontent.com/38809578/64212746-f2043600-cedc-11e9-8d0e-9648a849b5a9.PNG)





When run from the command line, I get the following message:



Starting a Gradle Daemon, 1 incompatible Daemon could not be reused, use --status for details

> Task :checkstyleMain FAILED



FAILURE: Build failed with an exception.



* What went wrong:

Execution failed for task ':checkstyleMain'.

> Unable to create Root Module: config {C:\Users\nisga\OneDrive\Desktop\duke\config\checkstyle\checkstyle.xml}, classpath {C:\Users\nisga\OneDrive\Desktop\duke\build\classes\java\main;C:\Users\nisga\OneDrive\De

sktop\duke\build\resources\main}.



* Try:

Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.



* Get more help at https://help.gradle.org



BUILD FAILED in 5s

2 actionable tasks: 1 executed, 1 up-to-date



Could anyone advise on what may be causing the issue?


</panel>

<panel header="**4. :fas-info-circle: Test events not received when running JUnit tests with Gradle**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/39" expanded>

![Code](https://user-images.githubusercontent.com/38809578/64129514-197cd500-cdef-11e9-9ab1-e19d79f668cb.PNG)

![Log](https://user-images.githubusercontent.com/38809578/64129523-2994b480-cdef-11e9-9336-e9e182061eb5.PNG)

Hi, when running my JUnit tests from Gradle I get the following output but I'm not sure what to make of it. I've reread the instructions and am fairly certain my set-up is correct and the folder structure is fine as well, is there something else I might be doing wrong? I've done some googling but they suggest other dependency issues and I find the code quite difficult to understand as well as it is usually part of larger projects. I've attached the code of my JUnit tests below was well.

![1](https://user-images.githubusercontent.com/38809578/64129613-bfc8da80-cdef-11e9-8346-b32806c1f5b4.PNG)

![2](https://user-images.githubusercontent.com/38809578/64129615-c35c6180-cdef-11e9-896d-3ad06ef48cfe.PNG)




</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/39#issuecomment-527220007" expanded>

> Have you tried running gradle from the terminal?



Using the command "gradlew test" from the terminal results in the following output when run from the duke folder (C:\Users\nisga\OneDrive\Desktop\duke):

BUILD SUCCESSFUL in 990ms

3 actionable tasks: 3 up-to-date



Is this expected output or is there something else I am missing? Thanks for your quick response!
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/39#issuecomment-527222413" expanded>

> That appears to be fine.

> 

> You might want check if your project structure is in order because it seems to be a problem with your IDE config.



Is there a specific way to be checking this? As far as I understand project structure refers to the order of my files but when I select "Tests" from my project menue I am being directed to the correct folder so I believed my project structure is in order as shown in the screenshot below. Did you mean something else by project structure? Thanks again for your help!

![Capture](https://user-images.githubusercontent.com/38809578/64130454-f8b77e00-cdf4-11e9-8afc-d3274aaed1b3.PNG)


</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/39#issuecomment-527225137" expanded>

> I was referring to the `Project Structure...` feature in IntelliJ IDEA. Try this:

> 

> 1. Enter `gradlew cleanTest` in a terminal.

> 2. Try running your tests again from IntelliJ.



Thanks so much for your help! I think that indeed was the issue! I'll try moving the folders and restructuring the project accordingly. Also ran the gradlew cleanTest and output was: 



BUILD SUCCESSFUL in 896ms

1 actionable task: 1 executed



![Capture](https://user-images.githubusercontent.com/38809578/64130763-01a94f00-cdf7-11e9-8231-44f901e1eb00.PNG)


</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/39#issuecomment-527226595" expanded>

> Technically, that's not a problem. Gradle just recognized that there were no new changes and skipped testing. As a result, no results were reported to IntelliJ. By running `:cleanTest`, you basically forced Gradle to compile and run the tests again.



Yea I just realised taking a closer look that the folder structure doesn't seem to be an issue. However, I still get the "Test events were not recieved" original error even after running gradlew cleanTest and can't see the output of the tests passing as shown in the examples I've seen. Am I correct in assuming my tests work for now though and is there anything I need to change to get the same output as shown below? Or am I correct in assuming everything is fine and the result shown in the example below is because Gradle was not used?

![Capture](https://user-images.githubusercontent.com/38809578/64130968-3d90e400-cdf8-11e9-827a-8893254ee895.PNG)


</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/39#issuecomment-527232896" expanded>

> You can change the test runner to IntelliJ in the settings.

> ![image](https://user-images.githubusercontent.com/22460123/64131056-b7c16880-cdf8-11e9-864a-0dd381a8a636.png)



Ok thanks again for your help I think I more or less figured it out! One last question, when I swapped to IntelliJ IDEA and then selected "Add JUnit 5.* to classpath" under Test as per the instructions under Week 3, my test files now get errors highlighted and when I try to run all tests I get the error:

"No tests were found" and the popup "Tests were not found in module "test". Use module "main" instead" as shown in the screenshot below. When I switched back to Gradle the tests still ran fine. Is there any way to configure it such that I can switch between both easily? I suspect the adding JUnit to classpath was what caused the error as simply swapping to using IntelliJ in the settings did not cause the issue at first. Else it seems I'll stick to using Gradle though I want to understand what's happening here.

![Capture](https://user-images.githubusercontent.com/38809578/64131816-c3fbf480-cdfd-11e9-9687-cded4a55d510.PNG)



Edit: Even after switching back to Gradle in the settings, right-clicking and running all tests results in the errors shown above. Only when I run gradlew test from the command line does the test complete successfully.


</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/39#issuecomment-527385154" expanded>

> ![image](https://user-images.githubusercontent.com/22460123/64149629-f2f38400-ce58-11e9-9fff-8820f0b78e9f.png)

> You have two extra modules.



Thank you so much! I think all the issues are finally resolved :)
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/41#issuecomment-527726402" expanded>

Yep silly mistake forgot to add the checkstyle config, thanks for your help!
</panel>

<panel header="**12 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/64#issuecomment-531373133" expanded>

Thanks for your help, silly of me to miss that!
</panel>

</panel>
<panel type="info" header="### KOH ZHENG QIANG SHAWN `@shawnkoh` (11 contributions)" expanded>
<panel header="**2. :fas-info-circle: Unable to import AB3 checkstyle.xml**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/111" expanded>

## Environment



Describe your development environment



- IntelliJ version:

```

IntelliJ IDEA 2019.2.3 (Ultimate Edition)

Build #IU-192.6817.14, built on September 24, 2019

Non-Bundled Plugins: CheckStyle-IDEA

```

- Java version:

```

openjdk 11.0.2 2019-01-15

OpenJDK Runtime Environment 18.9 (build 11.0.2+9)

OpenJDK 64-Bit Server VM 18.9 (build 11.0.2+9, mixed mode)

```

- Operating system version: macOS Mojave 10.14.6



## Issue



Attempted but unable to import checkstyle.xml using [CheckStyle-IDEA](https://plugins.jetbrains.com/plugin/index?xmlId=CheckStyle-IDEA), through Preferences --> Checkstyle --> +



## Code/Log Trace



```

com.puppycrawl.tools.checkstyle.api.CheckstyleException: cannot initialize module TreeWalker - cannot initialize module FileContentsHolder - Unable to instantiate 'FileContentsHolder' class, it is also not possible to instantiate it as .FileContentsHolder, FileContentsHolderCheck, .FileContentsHolderCheck. Please recheck that class name is specified as canonical name or read how to configure short name usage https://checkstyle.org/config.html#Packages. Please also recheck that provided ClassLoader to Checker is configured correctly.

	at com.puppycrawl.tools.checkstyle.Checker.setupChild(Checker.java:477)

	at com.puppycrawl.tools.checkstyle.api.AutomaticBean.configure(AutomaticBean.java:198)

	at org.infernus.idea.checkstyle.service.cmd.OpCreateChecker.execute(OpCreateChecker.java:61)

	at org.infernus.idea.checkstyle.service.cmd.OpCreateChecker.execute(OpCreateChecker.java:26)

	at org.infernus.idea.checkstyle.service.CheckstyleActionsImpl.executeCommand(CheckstyleActionsImpl.java:130)

	at org.infernus.idea.checkstyle.service.CheckstyleActionsImpl.createChecker(CheckstyleActionsImpl.java:60)

	at org.infernus.idea.checkstyle.service.CheckstyleActionsImpl.createChecker(CheckstyleActionsImpl.java:51)

	at org.infernus.idea.checkstyle.checker.CheckerFactoryWorker.run(CheckerFactoryWorker.java:46)

Caused by: com.puppycrawl.tools.checkstyle.api.CheckstyleException: cannot initialize module FileContentsHolder - Unable to instantiate 'FileContentsHolder' class, it is also not possible to instantiate it as .FileContentsHolder, FileContentsHolderCheck, .FileContentsHolderCheck. Please recheck that class name is specified as canonical name or read how to configure short name usage https://checkstyle.org/config.html#Packages. Please also recheck that provided ClassLoader to Checker is configured correctly.

	at com.puppycrawl.tools.checkstyle.TreeWalker.setupChild(TreeWalker.java:136)

	at com.puppycrawl.tools.checkstyle.api.AutomaticBean.configure(AutomaticBean.java:198)

	at com.puppycrawl.tools.checkstyle.Checker.setupChild(Checker.java:472)

	... 7 more

Caused by: com.puppycrawl.tools.checkstyle.api.CheckstyleException: Unable to instantiate 'FileContentsHolder' class, it is also not possible to instantiate it as .FileContentsHolder, FileContentsHolderCheck, .FileContentsHolderCheck. Please recheck that class name is specified as canonical name or read how to configure short name usage https://checkstyle.org/config.html#Packages. Please also recheck that provided ClassLoader to Checker is configured correctly.

	at com.puppycrawl.tools.checkstyle.PackageObjectFactory.createModule(PackageObjectFactory.java:210)

	at com.puppycrawl.tools.checkstyle.TreeWalker.setupChild(TreeWalker.java:127)

	... 9 more



```


</panel>

<panel header="**3. :fas-info-circle: Can we switch to branching workflow?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/108" expanded>

Hi Prof,

For the TP, we would like to stop using the forking workflow and instead adopt the [Git Feature Branch workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow#targetText=Git%20Feature%20Branch%20Workflow,without%20disturbing%20the%20main%20codebase.)

May I know if this is allowed?
</panel>

<panel header="**4. :fas-info-circle: Wrapped lines indentation auto-formatting**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/47" expanded>

Is there a way to instruct IntelliJ to use 8 spaces for wrapped lines?

I can't find the setting anywhere; not even on stackoverflow / google.

FWIW I'm using the Mac version 2019.2.1
</panel>

<panel header="**5. :fas-info-circle: Style of switch statements with curly brackets**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/15" expanded>

Hi Prof,

I understand from the style guide that switch statements should look like this.

```

String test = "abc";

switch (test) {

case "abc":

    # doStuff

    break;

case "bcd":

    # doOtherStuff

    break;

default:

    throw new Exception();

}

```



May I know what the style should be when the switch statement uses scopes in their cases.

Should it be like this?

```

String test = "abc";

switch (test) {

case "abc": {

    # doStuff

    break;

}

case "bcd": {

    # doOtherStuff

    break;

}

default: {

    throw new Exception();

}

}

```



The rationale for having curly brackets in switch statements is to provide a scope for the case's variables.

Consider this scenario:

It will fail to compile because the variable foo is being declared twice.



```

switch (test) {

case "abc":

    String foo = "bar";

    break;

case "bcd":

    String foo = "baz";

    break;

}

```
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/17#issuecomment-524898670" expanded>

What if we created the classes sporadically in prior commits? At which commit do we tag A-MoreOOP?
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/20#issuecomment-525246771" expanded>



> On 27 Aug 2019, at 4:21 PM, Damith C. Rajapakse <notifications@github.com> wrote:

> 

> For Level-8 (saving), are we allowed to implement it by object serialization, or must we strictly make our own "interpreter" to store it in a custom text form, then load it back by parsing through the text file?

> Up to you.

> 

> Regarding SE practice for defining custom exceptions:

> 

> For different custom exceptions in Duke, is it a better SE practice to

> a. define new sub-classes of Exception for each different error (eg. NoSuchTaskType, ShutDownException, InvalidTaskId), or

> b. use one exception (DukeException) with initialised with different error messages in its constructor?

> If 1a is preferred, should we continue to extend all these custom exceptions from Exception, or should we extend them from DukeException instead?

> Good questions. Let's see what others have to say about this.

> 

> —

> 

Regarding exceptions



I’m of the view that strictly following 1a or 1b is not an optimal solution.



Instead, I think that wherever possible, we should use Java’s exceptions instead.



For instance, InvalidTaskId should use IndexOutOfBoundsException.



In the rare scenario where we have a duke-specific exception that does not fit any of Java’s exceptions, we should extend it from DukeException.



However, if the exception can be used outside of duke, and is not covered by any of Java’s exceptions, we should extend it from Exception. An example of this would be DuplicateDataException.



Please correct me if I’m wrong! Would love to hear other opinions about this.
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/21#issuecomment-525324241" expanded>

Git log
Find the commit hash before you merged level 7

git reset —hard hash

Merge them again

git push -f

> On 27 Aug 2019, at 10:11 PM, Gabriel Chia <notifications@github.com> wrote:
> 
> Hello,
> 
> For Level 7, I've unintentionally committed the merge of Level 7 with fast forward (by default) and I'm unsure of how to revert this commit.
> 
> After committing Level 7, I have also committed Level 8 (successfully without fast forward; can see "merge branch" commit) and that was when I realised what it meant by merging without fast forward.
> 
> How do I safety revert the commits for me to be able to merge branch Level 7 into master again without fast forward?
> 
> —
> You are receiving this because you are subscribed to this thread.
> Reply to this email directly, view it on GitHub, or mute the thread.

</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/21#issuecomment-525344430" expanded>

Thanks for taking the time to explain ```git revert``` in detail Iskandar!



I'd like to add on a cautionary note about tags since we are on the note of reverting/reseting commits.



If you have pushed your tags to your remote repo with ```git push --tags``` reverting or deleting your commits will not remove your tags on the remote repo.



So how do we resolve this?



You may be tempted to use ```git tag --delete``` but this only deletes them locally.



Instead, you have to use ```git push origin :tagname```



Alternatively, you may also update your git tags locally, then ```git push --tags -f```



Please refer to this stackoverflow post for a more in depth discussion about removing tags on remote repos. https://stackoverflow.com/questions/5480258/how-to-delete-a-remote-tag
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/48#issuecomment-528712047" expanded>

Update your fx:controller to duke.MainWindow (or whichever package it is located in)

> On 6 Sep 2019, at 1:16 PM, Neo Weihong <notifications@github.com> wrote:
> 
> Hi,
> 
> I have been following the JavaFx tutorials and up till Tutorial 3, I haven't experienced any issues. However, in tutorial 4, a ClassNotFoundException is thrown when loading MainWindow.fxml (called from Main class).
> 
> The following screenshots contain the Main class and fxml code from the tutorial, my project directory and the exception stack trace.
> 
>  <https://user-images.githubusercontent.com/41929699/64402119-4a3a6400-d0a6-11e9-9793-91828cf384e6.png>
>  <https://user-images.githubusercontent.com/41929699/64402120-4a3a6400-d0a6-11e9-975f-5d77ca11439f.png>
>  <https://user-images.githubusercontent.com/41929699/64402121-4ad2fa80-d0a6-11e9-999a-c3171a503e66.png>
>  <https://user-images.githubusercontent.com/41929699/64402122-4ad2fa80-d0a6-11e9-9367-e496fbcfb16d.png>
> My github repo currently contains my latest commits (with these exceptions): https://github.com/whneo97/duke <https://github.com/whneo97/duke>
> Anyone happens to be able to help advise on this exception? I'm currently using Mac OS 10.14.5 and I'm using Java 11.0.2 (as advised in #44 <https://github.com/nus-cs2103-AY1920S1/forum/issues/44> and have configured Intellij to use it)
> 
> —
> You are receiving this because you are subscribed to this thread.
> Reply to this email directly, view it on GitHub <https://github.com/nus-cs2103-AY1920S1/forum/issues/48?email_source=notifications&email_token=AAU5MF47ATUK456IX2OPWWDQIHRR3A5CNFSM4IUFBIE2YY3PNVWWK3TUL52HS4DFUVEXG43VMWVGG33NNVSW45C7NFSM4HJW3AYA>, or mute the thread <https://github.com/notifications/unsubscribe-auth/AAU5MF6MZQGRIRILBBH7YM3QIHRR3ANCNFSM4IUFBIEQ>.
> 


</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/47#issuecomment-528799510" expanded>

Thanks for the reply!

But I can't find the same setting on my version (IntelliJ Ultimate Mac 2019.2.1)
</panel>

<panel header="**12 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/47#issuecomment-528825245" expanded>

Got it! Thank you Prof!

> On 6 Sep 2019, at 7:19 PM, Damith C. Rajapakse <notifications@github.com> wrote:
> 
> Search in project settings?
> 
> 
> —
> You are receiving this because you authored the thread.
> Reply to this email directly, view it on GitHub, or mute the thread.

</panel>

</panel>
<panel type="info" header="### WILLIAM RYAN KUSNADI `@WilliamRyank` (11 contributions)" expanded>
<panel header="**2. :fas-info-circle: Coveralls issue**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/121" expanded>

Recently, coveralls do not show the statistics in our team's PR. Anyone has experienced his before? We did not modify any coveralls settings. Thank you
</panel>

<panel header="**3. :fas-info-circle: Question regarding Add feature**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/93" expanded>

Our team will have around 10 fields for each person type. Since we feel that typing a whole string is quite messy, we came up with an idea that for adding, it will be more like `form`. So when we type `add`, it will create a `form` with all the fields and their values are empty. Then the app will prompt like `Name?` then the user will type in the Name, everytime the user type in a field's value, the form will be updated so the user will now whether what he has inputed is correct. Then he can undo if he input wrongly. Is it advisable to have such feature?
</panel>

<panel header="**4. :fas-info-circle: Error: Could not open the jar produced by shadowJar**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/54" expanded>

Hi, after generating the jar file using shadowJar i cant seem to open my jar file. Instead i got this error `Error: JavaFX runtime components are missing, and are required to run this application`. Any idea as why this happen? Thank you
</panel>

<panel header="**5. :fas-info-circle: could not import package in test folder**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/23" expanded>

![1](https://user-images.githubusercontent.com/50859694/63828894-18cce480-c992-11e9-9be3-ffa17f4bdfa5.PNG)

![2](https://user-images.githubusercontent.com/50859694/63828895-18cce480-c992-11e9-8e24-486efdee0b16.PNG)

![3](https://user-images.githubusercontent.com/50859694/63828897-19657b00-c992-11e9-8ed4-46ba06be1244.PNG)

![4](https://user-images.githubusercontent.com/50859694/63828898-19657b00-c992-11e9-88aa-9f3f8b8981b7.PNG)


</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/23#issuecomment-525602125" expanded>

but my test module has no dependencies on top, im not sure why, but i followed the tutorial.
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/23#issuecomment-525642604" expanded>



![5](https://user-images.githubusercontent.com/50859694/63839417-77518d00-c9a9-11e9-82d6-94cbe605f444.PNG)

![6](https://user-images.githubusercontent.com/50859694/63839419-77ea2380-c9a9-11e9-9afa-8c136022b956.PNG)



Still cant user the class prof
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/23#issuecomment-528451772" expanded>

Hi prof yes, thank you
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/23#issuecomment-528451792" expanded>

J
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/54#issuecomment-529324357" expanded>

Hi @junnbang, thank you for the help, managed to solve it.
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/54#issuecomment-529328383" expanded>

Hi @damithc, yes i used his solution and it works now. Thanks.
</panel>

<panel header="**12 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/93#issuecomment-535063993" expanded>

Okay prof, thanks for your suggestion. Yeah cause i do think there is a benefit in making such a feature, as our application will be used by hospital and people need to be careful and typically the user will want to double check if what they keyed in is correct. Will try to do both modes. Thanks prof!
</panel>

</panel>
<panel type="info" header="### JIN SHUYUAN `@CoderStellaJ` (10 contributions)" expanded>
<panel header="**2. :fas-info-circle: Association label vs association role**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/135" expanded>

Can anyone help to point out why this diagram is false? And what's the difference between association role and association label? Thanks!



Quiz question:

Which diagrams are acceptable representations of the **highlighted association role**?

![Capture](https://user-images.githubusercontent.com/40347063/66929240-461a4280-f065-11e9-846e-2da5da680960.PNG)


</panel>

<panel header="**3. :fas-info-circle: Comparison between path coverage and statement coverage**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/134" expanded>

Why is 100% path coverage more intense than 100% statement coverage?
</panel>

<panel header="**4. :fas-info-circle: Unable to find main class when running jar file**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/78" expanded>

When running jar file, it shows the following error:

`Error: Could not find or load main class duke.Launcher

Caused by: java.lang.ClassNotFoundException: duke.Launcher`



My guess is there is something wrong with class path setting, but haven't figured out how to solve it.
</panel>

<panel header="**5. :fas-info-circle: run .bat in intellij**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/3" expanded>

Any detailed instructions on how to configure and run .bat/.sh in intellij for A-TextUiTesting ?
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/3#issuecomment-522251416" expanded>

Yes, but in terms of the last step, do we need to set up the configuration again? I searched online and some people say need to add "External tools" for .bat
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/3#issuecomment-522297030" expanded>

Thanks a lot. I've found my problems.

**1. JNI error occurs during compilcation.**

My solution: This error may happen if you have changed your JDK version before. delete old JDK version and reopen duke project worked for me.

**2. If you have created multiple files for different classes.** Modified my .bat as follows

`javac  -cp ..\src -Xlint:none -d ..\bin ..\src\main\java\Task.java ..\src\main\java\Todo.java ..\src\main\java\Event.java ..\src\main\java\Deadline.java ..\src\main\java\DukeException.java ..\src\main\java\Duke.java`
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/78#issuecomment-532500142" expanded>

> Uhm what did you put for the `mainClassName` in your `build.gradle` file though? Is it `duke.Launcher`? If yes, did you put your `Launcher` class inside a package called `duke`?



Yes. I put Launcher inside package duke and change mainclass in build.gradle. And gradle run command is successful without any problem. This error occurs only when I run my jar file.
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/78#issuecomment-532580972" expanded>

> By the way, did you use gradle to make the jar?



Thanks a lot! I found the error. My fxml file path is wrong in the code and this causes the problem.
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/135#issuecomment-542999854" expanded>

Thanks for your contribution to this question. 

Because the quiz question asks whether the diagram shows the correct association role but the diagram shows association label. The diagram fails to show the role.
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/134#issuecomment-543000014" expanded>

Thanks a lot! It solves my confusion.
</panel>

</panel>
<panel type="info" header="### CHOW JIA YING `@C-likethis123` (10 contributions)" expanded>
<panel header="**2. :fas-info-circle: Problems with rendering correct data**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/142" expanded>

Please read up on how to write a [good question](https://stackoverflow.com/help/how-to-ask)



## Environment



Describe your development environment



- IntelliJ version: IntelliJ IDEA 2019.2 (Ultimate Edition)

- Java version: java 12.0.2

- Operating system version: macOS 10.14.6

- _other packages' versions_



## Issue

For context, our team is trying to build an organ-matching desktop application, which matches Patients to Donors. Currently, I am trying to add in a command to match a particular Patient to all the donors in the database. After matching the Patient to the Donor, a list with matching Donors and its success rate should be displayed. 



Example output: 

<img width="1437" alt="Screenshot 2019-10-23 at 4 29 09 PM" src="https://user-images.githubusercontent.com/27060502/67373691-a3a51680-f5b2-11e9-8e67-01a8c2410541.png">



The issue comes when instead of displaying the Donors and its success rate of matching, it displays the Donors only, without the match result. There is no pattern as to when it displays the wrong output. For example, the first time I type in `match ic/NRIC`, it displays the Donors with the match results. But when I type in the same command, it displays the Donors without the match results. I have tried many combinations of commands but still cannot find a reason as to why this problem occurs. 



### How to replicate the bug



1. Launch the application

2. Type in the following commands to add testing data:

```

add t/patient n/John Doe ic/S1234568R p/98765432 a/21 pr/high b/A tt/1,2,3,4,5,6 o/kidney d/S1111111A



add t/donor n/John Doe Donor ic/S1234562R p/98888888 a/21 b/O tt/1,2,3,4,5,6 o/kidney exp/20-Jan-2020

```

3. Type in the following command: `match ic/S1234568R`. Repeat the typing of this command several times. 



## Code/Log Trace



Here is my branch where this feature is added: https://github.com/AY1920S1-CS2103T-T13-1/main/tree/add-match-feature/



Here are some details about the implementation of this feature that may help. 

1. When we type in `match ic/S1234567R`, the user input is parsed by the `MatchCommandParser` to create a `MatchCommand`. The `MatchCommand` executes the matching in the `ModelManager` and updates the filteredPersonList in ModelManager. 

2. To display the match results, in `PersonListPanel.java`, there is a `PersonListViewCell` class with an `updateItem` method to decide what should be rendered:



```

/**

     * Custom {@code ListCell} that displays the graphics of a {@code Person} using a {@code PersonCard}.

     */

    class PersonListViewCell extends ListCell<Person> {

        @Override

        protected void updateItem(Person person, boolean empty) {

            super.updateItem(person, empty);



            if (empty || person == null) {

                setGraphic(null);

                setText(null);

            } else {

                if (person instanceof Doctor) {

                    setGraphic(new DoctorCard((Doctor) person, getIndex() + 1).getRoot());

                } else if (person instanceof Donor) {

                    Donor donor = (Donor) person;

                    if (donor.isMatched()) {

                        setGraphic(new MatchCard(donor, getIndex() + 1).getRoot());

                        donor.setMatched(false);

                    } else {

                        setGraphic(new DonorCard(donor, getIndex() + 1).getRoot());

                    }

                } else if (person instanceof Patient) {

                    setGraphic(new PatientCard((Patient) person, getIndex() + 1).getRoot());

                } else {

                    setGraphic(new PersonCard(person, getIndex() + 1).getRoot());

                }

            }

        }

    }

```




</panel>

<panel header="**3. :fas-info-circle: Squash when merging?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/107" expanded>

After a PR to the team repo is approved, we can either choose to squash and merge the PR to the team repo or to create a merge commit. My team prefers to squash and merge. Is there any requirement on which option to choose, or is it up to our team to decide what to do? Also, how about rebasing?
</panel>

<panel header="**4. :fas-info-circle: Tagging to the team repo**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/106" expanded>

The tutorial mentions we should use the 'git tag' feature to tag our team repo version as v1.1. However, our team cannot directly push to our team repo, and can only make PRs. 



How do we tag with our milestones if we cannot directly push to our team repo? Any guidance would be appreciated. 
</panel>

<panel header="**5. :fas-info-circle: JavaFX: unable to launch application**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/33" expanded>

I have included these lines in my build.gradle file:

<img width="1438" alt="Screenshot 2019-08-31 at 6 38 31 PM" src="https://user-images.githubusercontent.com/27060502/64062838-9a38a700-cc1e-11e9-853d-458fac8ff119.png">

I have added the start method in the Duke.java file and a Launcher class according to JavaFX tutorial part 1. 

<img width="1013" alt="Screenshot 2019-08-31 at 6 40 45 PM" src="https://user-images.githubusercontent.com/27060502/64062860-de2bac00-cc1e-11e9-8130-c890591550ce.png">



However when I run ./gradlew build then ./gradlew run, I get directed to my Desktop and my command line interface looks like this:

<img width="1438" alt="Screenshot 2019-08-31 at 6 37 19 PM" src="https://user-images.githubusercontent.com/27060502/64062836-9442c600-cc1e-11e9-8d05-c4c520d9397f.png">



<img width="1438" alt="Screenshot 2019-08-31 at 6 37 11 PM" src="https://user-images.githubusercontent.com/27060502/64062841-9c9b0100-cc1e-11e9-8529-b4745badc2bf.png">



I am also unable to exit the program via the 'bye' command. 


</panel>

<panel header="**6. :fas-info-circle: A-Gradle: Indentation for wrapped lines**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/31" expanded>

<img width="842" alt="Screenshot 2019-08-31 at 4 05 51 PM" src="https://user-images.githubusercontent.com/27060502/64061184-89316b00-cc09-11e9-91e1-bdc6e3591596.png">

Based on the style guide in the module website, indentation of wrapped lines should be 8 spaces more than the parent line. By this principle, it means that lines 18-20 should be indented with 16 lines. 



However, as seen in the picture below, when I run ./gradlew build, I get an error stating that the indentation of lines 18-20 should not be 16. I would like to get some advice on what is the correct indentation, do I follow the checkStyle warnings or the style guide? 

<img width="1438" alt="Screenshot 2019-08-31 at 4 06 14 PM" src="https://user-images.githubusercontent.com/27060502/64061183-83d42080-cc09-11e9-818a-2e56afd780a9.png">




</panel>

<panel header="**7. :fas-info-circle: Must I strictly complete minimal tasks before completing stretch goals?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/17" expanded>

For level A-MoreOOP, I find it easier to create the 4 required classes and the Command class (specified in the stretch goal) from the start. 

Do I need to create the 4 required classes, tag the commit, before creating the Command class or can I just go ahead and create the Command class?
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/17#issuecomment-525292376" expanded>

Okay, thanks everyone for your input!
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/31#issuecomment-526812056" expanded>

Noted, thank you for your reply.
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/33#issuecomment-526918210" expanded>

I managed to solve the issue by changing mainClassName to Launcher, and commenting out my main method in the Duke class. 



Thank you for your inputs!
</panel>

<panel header="**11 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/107#issuecomment-536946018" expanded>

Noted. Thank you for your reply!
</panel>

</panel>
<panel type="info" header="### THO WEN LONG, PAUL `@dragontho` (9 contributions)" expanded>
<panel header="**2. :fas-info-circle: Request to use Gson for file storage**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/83" expanded>

## Library



Gson - https://github.com/google/gson



## Purpsoe



An alternative way to store information as a .json


</panel>

<panel header="**3. :fas-info-circle: Bundling other dependencies into the shadowJar jar file**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/79" expanded>

Please read up on how to write a [good question](https://stackoverflow.com/help/how-to-ask)



## Environment



Describe your development environment



- IntelliJ version: 2019.2

- Java version: 11.0.3

- Operating system version: Windows 10

- _other packages' versions_ Gson 2.8.5



## Issue



I decided to use a third party library for my data storage called Gson instead of the normal .txt storage methods for extension D-Trivia. The application works fine when I was testing it in IntelliJ, however, when I exported it out to a jar file, there was a NullPointerException pointing to what should have been something that Gson took care of. My question now is is there a way to manually include the dependency inside shadowJar? And if such a solution is not possible, is there any other way to make it work through gradle configurations?



## Code/Log Trace



```

Caused by: java.lang.NullPointerException

        at seedu.duke.util.UI.viewAllTrivia(UI.java:147)

        at seedu.duke.commands.trivia.TriviaViewAllCommand.execute(TriviaViewAllCommand.java:12)

        at seedu.duke.Duke.getResponse(Duke.java:40)

        at seedu.duke.javafxui.MainWindow.handleUserInput(MainWindow.java:50)

```



```

dependencies {

    testImplementation 'org.junit.jupiter:junit-jupiter:5.5.0'

    implementation 'com.google.code.gson:gson:2.8.5'

}

```


</panel>

<panel header="**4. :fas-info-circle: How to push git tags**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/11" expanded>

Hi prof,

Quick question, but how exactly do you push git tags? After a quick search online I came across this answer:

https://stackoverflow.com/questions/5195859/how-do-you-push-a-tag-to-a-remote-repository-using-git

However, after adding the --follow-tags option to the end of git push, I could not find any evidence that the tag has been pushed. Furthermore, the answer also discourages the use of git push --tags, for which I also still do not know the reason. Are there multiple ways to push tags to the repository and if so which is the most appropriate? Also, how do you find evidence of your tags being pushed? Please redirect to another answer if the issue has been resolved already.
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/11#issuecomment-524172309" expanded>

Thanks all for the help!
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/79#issuecomment-532636960" expanded>

Also, how does one change labels of issues?
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/79#issuecomment-532641743" expanded>

To add on, it is not only the trivia part that fails, anything regarding storage is not working, including the already implemented .txt storage for tasklist as well.
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/79#issuecomment-532667715" expanded>

Oh sorry, I've found my own problem. It's because I did not implement my saving and loading properly from the beginning. Now I've fixed it. On another note, prof, would Gson be allowed for my iP?
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/79#issuecomment-532768264" expanded>

Alright thank you prof!
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/83#issuecomment-533410805" expanded>

Ok thanks prof!
</panel>

</panel>
<panel type="info" header="### SHUI YAO `@shuiyao-sg` (9 contributions)" expanded>
<panel header="**2. :fas-info-circle: Duke last line truncated when wrapText=true**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98" expanded>

## Issue:

When I set wrapText="true" in the Label "dialog" in DialogBox.fxml, the last line of my list will always be truncated and replaced with ellipses. May I know how should I fix it?



Here's my repo if you want to replicate it https://github.com/shuiyao-sg/duke.git

The code can be found in `branch-GUI`



Here's how the bug looks like:

![b7136fbf95d89c5e10a725b6e9a6139](https://user-images.githubusercontent.com/46176136/65759953-a72db500-e14e-11e9-9d43-07c202329b1d.png)



Here's the screenshot of DialogBox.fxml:

![image](https://user-images.githubusercontent.com/46176136/65760020-ce848200-e14e-11e9-8478-10e7deabd588.png)



Here's the screenshot of MainWindow.fxml:

![image](https://user-images.githubusercontent.com/46176136/65760087-e52ad900-e14e-11e9-92d7-8c770cef80b4.png)



What's strange is that when I ask my friend to replicate this problem, it seems that he doesn't have such kind of issue with the same code (he's using Linux system):

![image](https://user-images.githubusercontent.com/46176136/65760335-684c2f00-e14f-11e9-9c85-55f58004e459.png)



## Something not sure whether it is related to this problem:

When I run Duke, I always get this warning of wrong JavaFx runtime version:

![image](https://user-images.githubusercontent.com/46176136/65760517-c11bc780-e14f-11e9-917e-74f17d911c1a.png)



## Environment:

OS: Windows 10

IntelliJ version: 2019.2

Java version:

java 11.0.1 2018-10-16 LTS

Java(TM) SE Runtime Environment 18.9 (build 11.0.1+13-LTS)

Java HotSpot(TM) 64-Bit Server VM 18.9 (build 11.0.1+13-LTS, mixed mode)








</panel>

<panel header="**3. :fas-info-circle: Failed to enable assertions in IntelliJ despite adding -ea**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/55" expanded>

I followed the instruction given on [this site](https://stackoverflow.com/questions/18168257/where-to-add-compiler-options-like-ea-in-intellij-idea) to add "-ea" to my VM option (I also tried "-enableassertions") in Run Configuration. However, when I run the program there's no assertion error appearing (the program run as per normal). Can someone help me figure out how to solve this problem?



Here's the link for [my project](https://github.com/shuiyao-sg/duke.git). The relevant code can be found in the branch "branch-A-Assertions".



Below are the screenshots of my code snippet and IntelliJ setting.



![7ad2e1418b77d1ac59ccd3a8a19dd9f](https://user-images.githubusercontent.com/46176136/64613531-f367be00-d408-11e9-9494-b8f9830de307.png)

![ccb300f1a75a3c77c19623b2bb3893e](https://user-images.githubusercontent.com/46176136/64613540-f8c50880-d408-11e9-865f-3afc0debd9a5.png)




</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/55#issuecomment-529939611" expanded>

> Is your build.gradle application targeting Launcher?



If you are referring to the application{ } block in build.gradle, I think yes.



![09f7b0e0e439380b300878761d13f01](https://user-images.githubusercontent.com/46176136/64618683-4cd4ea80-d413-11e9-9b03-2e9fb2a36031.png)


</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/55#issuecomment-529948422" expanded>

> https://stackoverflow.com/questions/48396274/how-to-enable-assertions-in-the-gradle-run-task



It works! Thank you so much!
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-535910093" expanded>

> Did you try removing the max height field from your DialogBox.fxml?



I tried but it doesn't work.
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-535945960" expanded>

> Maybe you can try setting your VBox / Hbox (which ever u use to wrap your content) Min height/width to USE_PREF_SIZE via the SceneBuilder.



It does not work as well...Thanks anyways!
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-535946620" expanded>

> For the warning, refer to this issue: [nus-cs2103-AY1819S2/forum#30](https://github.com/nus-cs2103-AY1819S2/forum/issues/30)

> 

> As for JavaFX styling issues, in theory there should be no differences across platforms. However, weird quirks like this are not unheard of. If @junnbang's suggestion does not work, you can investigate using a listener to dynamically resize the dialog box to fit as a workaround.



I think my friend mistakenly ran the code from my master branch (with wrapText=false), where it should have been from branch-GUI. So it should not be a platform-related problem. So I guess there are some problem with my code...
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-536146626" expanded>

> What I did was that I changed from `Label` to the shape `Text` in both my `MainWindow.java` and `DialogBox.fxml` (changed in `DialogBox.fxml` using Scene Builder). I had read up a bit on online forums and it seems that `Label` does not adjust based on the size of your text (in this case, the tasks that Duke prints), so there was a recommendation to use `Text` shape instead. Let me know if this works!



It works! Thanks!
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-536197282" expanded>

> Thanks everyone for the inputs

> @shuiyao-sg go ahead and close if the issue is resolved.



Thanks Prof!
</panel>

</panel>
<panel type="info" header="### TAN LIKAI `@tanlk99` (9 contributions)" expanded>
<panel header="**2. :fas-info-circle: Format for PE response**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/178" expanded>

For the PE developer responses, the website said to give responses in the following format:



```

# Team's Response

{replace this with your response}

## Duplicate status (if any):

```



For non-duplicate issues, is it fine to leave the duplicate status field empty, or do we have to indicate `--`? (since I saw some responses do that)


</panel>

<panel header="**3. :fas-info-circle: UML Diagrams with draw.io**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/143" expanded>

Our team is currently using draw.io to create our UML diagrams. It has a feature to export diagrams as XML files. Should we then include these XML files inside the `docs/diagram` directory?
</panel>

<panel header="**4. :fas-info-circle: Question about version numbering**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/103" expanded>

Were there meant to be any features implemented in v1.1? Or is that just meant to be a planning phase?
</panel>

<panel header="**5. :fas-info-circle: User Guide Draft Submission & Update**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/101" expanded>

When is the deadline for the UG draft submission on LumiNUS, and for the UG update on the product website?
</panel>

<panel header="**6. :fas-info-circle: Using javax.json library and its implementation**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/50" expanded>

Oracle has a JSON processing library [javax.json](https://javaee.github.io/jsonp/) which is included in Java EE. Are we allowed to use this for the iP or tP? If we are, does this count as a third-party library for reuse purposes?
</panel>

<panel header="**7. :fas-info-circle: A-Gradle and A-Checkstyle branches**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/29" expanded>

If we have already set up Gradle and checkStyle using Gradle before week 4, do we still have to create branches for these features?
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/50#issuecomment-528900551" expanded>

Thanks for the suggestion! Do we have to credit it as stated in the [Policy on Reuse](https://nus-cs2103-ay1920s1.github.io/website/schedule/week4/project.html)?
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/143#issuecomment-546203225" expanded>

Yes, they can be used to update the diagrams. So we should store them in the docs/diagrams directory?
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/178#issuecomment-554644887" expanded>

Sorry, I did some responses on mobile while I was away from the computer.
</panel>

</panel>
<panel type="info" header="### SUDHARSHAN MADHAVAN `@uggi121` (9 contributions)" expanded>
<panel header="**2. :fas-info-circle: 💡Unit Testing Floating Point Numbers**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/147" expanded>

As a direct consequence of the IEEE 754 format for floating point numbers, it is impossible to achieve 100% accuracy and precision in testing floating point values. A pragmatic heuristic to follow involves factoring in the inputs to the method and padding the expected return value with a suitable error threshold.



For example, 0.1 + 0.2 is not equal to 0.3 in this format. Keep this in mind while designing unit tests and choose an appropriate error tolerance range. Another good practice for mathematical methods is to test them against similar existing implementations
</panel>

<panel header="**3. :fas-info-circle: Sequence Diagram Destroy Markers**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/146" expanded>

In the unabridged developer guide presented in AB3, the sequence diagram for the delete command doesn't destroy the instance 'd' of the 'DeleteCommand' class. Upon scrutinizing the code in the LogicManager class, it is evident that 'd' is futile after the command has been executed. This is because the resultant details are contained in a 'CommandResult' object.



Below the sequence diagram associated with the developer guide, there is an annotation that highlights an inherent defect of PlantUML which makes it unable to render object lifelines correctly when the object is pre-maturely destroyed, as in the case of the 'DeleteCommandParser' object.



This prompts me to ask - is the lifeline of the 'DeleteCommand' object inaccurately shown as continuing because of an error with PlantUML, or is it because of a subtler additional usage later on?
</panel>

<panel header="**4. :fas-info-circle: How much SLAP is too much?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/51" expanded>

How much abstraction is too much? Adding an extra layer of abstraction has its costs and benefits. In most cost-benefit analyses of abstraction, benefits would be a clear winner. 



SLAP seems to be a good guideline in general. However, it is highly likely we reach a stage where further abstractions cause more harm than good. That is, after a point, the costs (refactoring and debugging) would outweigh the benefits. What is a good guideline to follow to ensure that we're adding another layer of abstraction that has enough information to be significant? Is there a quantitative measure, like the reduction in the LoC in the original method, to determine the 'impact'?
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/9#issuecomment-523773496" expanded>

If I could opine in on this issue, I'd say both approaches have their pros and cons, which you've highlighted in the above comments. While Object-Level validations align with the essence of OOP, it could be a bit tedious to deal with similar cases in multiple objects. This will ultimately lead to a lot of redundant and repeated code.



A partial solution could be to handle common cases like white-space/empty inputs at the input-class level, leaving the object constructors to deal with more specific invalid inputs relevant to their associated objects.



To add on, we could abstract the input class at a higher level to a machine that accepts input. The machine has no idea what the valid input for other machines (objects) are. However, there are certain inputs that are invalid inputs for ALL objects. These can be handled at the input class level.
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/11#issuecomment-523836959" expanded>

In the command-line, type : -

    **git ls-remote --tags origin**



You should see a list of pushed tags
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/49#issuecomment-528772706" expanded>

Implementing all the tasks under that sub-section seems tedious and unnecessary. A pragmatic approach would be to discuss with your team and individually implement non-overlapping features relevant to the tP
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/47#issuecomment-528778871" expanded>

File -> Settings -> Editor -> Code Style -> Java -> Continuation Indent = 8
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/146#issuecomment-546230816" expanded>

Thank you for the reply Prof. What about DeleteCommand? There is no `x` marked in the diagram, but I see no further use for it in the caller's code
</panel>

<panel header="**10 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/146#issuecomment-546279659" expanded>

Thank you Master Damith
</panel>

</panel>
<panel type="info" header="### LIM HUI MIN `@huiminlim` (8 contributions)" expanded>
<panel header="**2. :fas-info-circle: Travis build fails due to coveralls/asciidoctor**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167" expanded>

Please read up on how to write a [good question](https://stackoverflow.com/help/how-to-ask)



## Environment



Describe your development environment



- IntelliJ version: IntelliJ IDEA 2019.2.1

- Java version: 

- Operating system version: Windows 10

- _other packages' versions_



## Issue



I carried on my coding activities as per normal and I created a pull request to submit to my team repo. However, travis keeps failing my PR and codes even though the travis for my own repo passes and says that build is successful.



This is the screenshot of Travis (failed) build from my team repo:

![image](https://user-images.githubusercontent.com/43434313/68325466-6be6b480-0104-11ea-8a62-3dec340aa383.png)

This is the link:

https://travis-ci.org/AY1920S1-CS2103-F09-2/main/builds/608332992?utm_medium=notification&utm_source=github_status

Build number is #556



This is the screenshot of my own repo's Travis

![image](https://user-images.githubusercontent.com/43434313/68325558-a2243400-0104-11ea-93f3-18b1522bb763.png)



https://travis-ci.org/huiminlim/main/builds/608332966?utm_medium=notification&utm_source=github_status




</panel>

<panel header="**3. :fas-info-circle: Repo Sense: issue with invalid filepath**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/137" expanded>

## Environment



Describe your development environment



- IntelliJ version: IntelliJ IDEA Ultimate 2019.2.1

- Java version: java 11.0.2

- Operating system version: Windows 10

- _other packages' versions_



## Issue



I was trying to make RepoSense work in my local repo by trying the following instructions from this page:

https://github.com/reposense/RepoSense/blob/release/docs/UserGuide.md#configuring-a-repo-to-provide-additional-data-to-reposense



I added the config.json and followed all the way up to this step

`java -jar RepoSense.jar --repo  C:/Users/user/Desktop/tp/main`

where my RepoSense.jar exists.



However, RepoSense shows a "Invalid filepath" error, which I am not too sure why.



![image](https://user-images.githubusercontent.com/43434313/67087290-3588da00-f1d5-11e9-9838-bc6bad194394.png)



I also tried to go to the file path `.\\src\\test\\java\\dream\\fcard\\util\\data\\Test.java` in my code to check and commented out lines with slashes in related test files, but does not solve the issue as well.



This is the link to the filepath in github for easy reference: https://github.com/huiminlim/main/blob/master/src/test/java/dream/fcard/util/data/Test.java



Any advice on why this error exist? Thanks in advance!



## Code/Log Trace



My local repo currently has the code from this master branch: https://github.com/huiminlim/main


</panel>

<panel header="**4. :fas-info-circle: Level 10: cannot load fxml in Main**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/35" expanded>

Hi I am receiving some issues when I try to run part 4 of Level-10. 

I have done as the tutorial has suggested, changed the main class in launcher to Main.class and I still receive the following error messages. 



![image](https://user-images.githubusercontent.com/43434313/64079360-2fb86180-cd19-11e9-84e2-69be70d1c2bc.png)

![image](https://user-images.githubusercontent.com/43434313/64079361-3cd55080-cd19-11e9-8cb0-8c54ab7c4114.png)



This is my project directory:

![image](https://user-images.githubusercontent.com/43434313/64079416-d7ce2a80-cd19-11e9-9ba7-ebf021f10f6f.png)





Is there any mistake I made and solution to this problem? Thanks!
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/35#issuecomment-526935388" expanded>

Hi, thanks for help, works perfectly now!
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/137#issuecomment-543671754" expanded>

@damithc I think I resolved the problem, by removing a file with name " .\src\test\java\dream\fcard\util\data\Test.java " from my repo. Then, RepoSense produced a valid report after I removed this file with slashes in the name.



https://github.com/huiminlim/main/commit/c3215ba03a6d3d2c126d98f9b6c0b2376a3ffebc



I think that RepoSense does not accept files with slash in names.



Thank you and RepoSense dev team for the help anyway!
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552066329" expanded>

Hi Prof Damith, looks like this is the output i obtained on Windows 10, and no error is shown when I run both the gradle and just the task alone. Not sure if I did the correct way as you advised.



![image](https://user-images.githubusercontent.com/43434313/68523114-5aadcb80-02ef-11ea-9b28-c83dc176e3b0.png)




</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552066492" expanded>

We executed the same command on a mac



This is the complete task

![image](https://user-images.githubusercontent.com/43434313/68523159-ede70100-02ef-11ea-8111-8b24a55171ff.png)



This is the asciidoctor only task

 

![image](https://user-images.githubusercontent.com/43434313/68523162-fb03f000-02ef-11ea-92d8-6fc4f6acfbae.png)


</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552420328" expanded>

Thanks Prof, that works.
</panel>

</panel>
<panel type="info" header="### NEO WEIHONG `@whneo97` (8 contributions)" expanded>
<panel header="**2. :fas-info-circle: JavaFx Tutorial 4: Class Not Found Exception**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/48" expanded>

Hi,



I have been following the JavaFx tutorials and up till Tutorial 3, I haven't experienced any issues. However, in tutorial 4, a ClassNotFoundException is thrown when loading MainWindow.fxml (called from Main class).



The following screenshots contain the Main class and fxml code from the tutorial, my project directory and the exception stack trace.



<img width="1179" alt="Screenshot 2019-09-06 at 12 41 57 PM" src="https://user-images.githubusercontent.com/41929699/64402119-4a3a6400-d0a6-11e9-9793-91828cf384e6.png">

<img width="700" alt="Screenshot 2019-09-06 at 12 46 33 PM" src="https://user-images.githubusercontent.com/41929699/64402120-4a3a6400-d0a6-11e9-975f-5d77ca11439f.png">

<img width="1294" alt="Screenshot 2019-09-06 at 12 52 24 PM" src="https://user-images.githubusercontent.com/41929699/64402121-4ad2fa80-d0a6-11e9-999a-c3171a503e66.png">

<img width="257" alt="Screenshot 2019-09-06 at 12 57 41 PM" src="https://user-images.githubusercontent.com/41929699/64402122-4ad2fa80-d0a6-11e9-9367-e496fbcfb16d.png">



My github repo currently contains my latest commits (with these exceptions): https://github.com/whneo97/duke



Anyone happens to be able to help advise on this exception? I'm currently using Mac OS 10.14.5 and I'm using Java 11.0.2 (as advised in https://github.com/nus-cs2103-AY1920S1/forum/issues/44 and have configured Intellij to use it)
</panel>

<panel header="**3. :fas-info-circle: Is there any way to double-check if cs2103 bot has access to my duke repository?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/12" expanded>

After configuring my git username as according to the instructions on the cs2103 website last week, I submitted the pre-lecture survey and submitted the git username that I have configured.



However, I just noticed that despite not having tracking enabled, I did not receive any emails from cs2103 bot about it (like my friends did), nor received any other emails for any other purposes. It came to my realisation that my git username has been reset to my full name rather than the username I had previously configured (and suspect this was possibly due to entering the rm -R .git command last week in an attempt to reset some terminal display features that were affected by the setting up of git)



I have now enabled issues tracking, and reconfigured my username back to what I believe I previously submitted in the pre-lecture survey, but I'm not entirely sure whether it is correct.



Is there any way to double-check or confirm whether cs2103 bot is now able to track my progress on the duke repository that was forked on my account?



Thank you and sorry for any inconvenience caused.
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/12#issuecomment-523884104" expanded>

Hi prof, thank you fo the reply and assurance! Will it be possible to check if my current git username corresponds to the one submitted in the pre-lecture survey?
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/12#issuecomment-523886032" expanded>

Okay sure, yes should be the same, thank you prof for the clarification!
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/48#issuecomment-528764520" expanded>

> Update your fx:controller to duke.MainWindow (or whichever package it is located in)

> […](#)

> On 6 Sep 2019, at 1:16 PM, Neo Weihong ***@***.***> wrote: Hi, I have been following the JavaFx tutorials and up till Tutorial 3, I haven't experienced any issues. However, in tutorial 4, a ClassNotFoundException is thrown when loading MainWindow.fxml (called from Main class). The following screenshots contain the Main class and fxml code from the tutorial, my project directory and the exception stack trace. <https://user-images.githubusercontent.com/41929699/64402119-4a3a6400-d0a6-11e9-9793-91828cf384e6.png> <https://user-images.githubusercontent.com/41929699/64402120-4a3a6400-d0a6-11e9-975f-5d77ca11439f.png> <https://user-images.githubusercontent.com/41929699/64402121-4ad2fa80-d0a6-11e9-999a-c3171a503e66.png> <https://user-images.githubusercontent.com/41929699/64402122-4ad2fa80-d0a6-11e9-9367-e496fbcfb16d.png> My github repo currently contains my latest commits (with these exceptions): https://github.com/whneo97/duke <https://github.com/whneo97/duke> Anyone happens to be able to help advise on this exception? I'm currently using Mac OS 10.14.5 and I'm using Java 11.0.2 (as advised in #44 <#44> and have configured Intellij to use it) — You are receiving this because you are subscribed to this thread. Reply to this email directly, view it on GitHub <#48?email_source=notifications&email_token=AAU5MF47ATUK456IX2OPWWDQIHRR3A5CNFSM4IUFBIE2YY3PNVWWK3TUL52HS4DFUVEXG43VMWVGG33NNVSW45C7NFSM4HJW3AYA>, or mute the thread <https://github.com/notifications/unsubscribe-auth/AAU5MF6MZQGRIRILBBH7YM3QIHRR3ANCNFSM4IUFBIEQ>.



Thank you! This helped (replaced MainWindow with seedu.duke.MainWindow as according to my project directory structure)
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/48#issuecomment-528764916" expanded>

> Why you didn't use the template?

> 

> Taking screenshot is not a good practice as it is not copy-paste friendly.



Okay, will take note to use the template in the future, thanks for the advice!
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/161#issuecomment-549558894" expanded>

Hi prof @damithc , sorry just to double-check, will the following then be correct?



- We are not to close the issues we posted until Dec 9th (unless we intend to withdraw them.



- For the PED issues posted on our team repo, we may close the issue by the bot as soon as we have resolved the problems described (?). However, we are not to close the corresponding issues opened by the original author. (?)



- For PE issues, we are not to rectify or close the issues at all, be it by the bot or by the original author. (?)
</panel>

<panel header="**9 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/161#issuecomment-549693247" expanded>

> > * We are not to close the issues we posted until Dec 9th (unless we intend to withdraw them.

> > * For the PED issues posted on our team repo, we may close the issue by the bot as soon as we have resolved the problems described (?). However, we are not to close the corresponding issues opened by the original author. (?)

> > * For PE issues, we are not to rectify or close the issues at all, be it by the bot or by the original author. (?)

> 

> Yes, that's correct. You are free to do anything with the PED issues posted on your team repo. We do not take them for grading.



Okay noted, thank you prof for the clarification!
</panel>

</panel>
<panel type="info" header="### HONG SHAO YI `@shaoyi1997` (7 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/111#issuecomment-538287389" expanded>

Is your `Checkstyle version` in your settings set to **8.1**?



![image](https://user-images.githubusercontent.com/44439414/66190140-e9f70c00-e6bd-11e9-946b-217e3498ad46.png)



I looked through the release notes for Checkstyle and found that version 8.2 removed the `FileContentsHolder` module, which would explain the failure to instantiate the module and thereby, the exception thrown since Gradle uses version 8.1.



I changed my checkstyle version to 8.24 and received the same error that you received as well.
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/133#issuecomment-541769120" expanded>

Hmmm, based on the Travis job log it seems like the build failure is not due to `constructor_missingFileUrl_throwsAssertionError()` and `constructor_invalidFileUrl_throwsAssertionError()` tests failures.



Rather, it's due to an `AssertionFailedError` in your `TutorialTest`, as seen below.



![image](https://user-images.githubusercontent.com/44439414/66765781-3670f180-eedf-11e9-80eb-4b6cc381b5a2.png)
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547050497" expanded>

In the second case, `File imageFile = new File(IMAGE_DIRECTORY + value);` assumes that the given path starts from the project root directory (i.e. starting from `main/...`). However, your image is actually stored in the resource folder, which is not the root level directory. The first case works because `getResourceAsStream` reads a file from `src/main/resources`.



You might want to consider letting your `IMAGE_DIRECTORY` = `src/main/resources/images/` for the time being, while still running in the IDE. This will allow `new File(IMAGE_DIRECTORY + value)` to get the file from the root directory.
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547058653" expanded>

> But what if the jar file isn't inside the project directory and moved to another directory with an `images` folder? For example, i moved the jar file to `Documents` and there is an `images` folder. How then would I retrieve the images?



Ah I see! I suspect your solution would work if the jar file is actually the case as you mentioned. However, if you are still running from your IDE, this method would break down since `new File(...)` will attempt to read from the root project directory.



Have you tried building the jar file and manually testing to see if it works?
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547293827" expanded>

> i built the jar file with an `images` folder and the relevant images in the `Documents` directory but it doesn't seem to work.



I examined your code further and realised that your `IMAGE_DIRECTORY` = `/images/` instead of `images/`. 

Placing a leading slash makes the path an absolute file path instead of a relative path, thus this references to `C:/images/` (assuming you're using Windows), instead of `C:/path/to/jar/folder/images/`.



In addition, `new Image(path)` requires `path` to start with `file://` in order to load the image through `ImageView`.



Hence, to sum up, you might want to try the following changes:



 - `IMAGE_DIRECTORY = images/`

- `new Image("file://" + imageFile.toURI().getPath())`



I've tried these changes on my end and it works through the jar file. Hope it works for you as well! :)
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547438984" expanded>

> Thank you so much! Definitely working now. Would this work with the IDE or only for jar files?



Glad to hear it works! 



It should be able to work in the IDE as well, provided you have an `images` folder in your root project directory i.e. `main/images/`. You can specify this folder in `.gitignore` so that it won't be pushed into the remote repo.



Additionally, note that your application does not automatically create an `images` folder in the root directory, so you might want to consider automatically creating this folder when your user launches the app to aid your user.
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547815998" expanded>

Hi!



I suspect the bulk of these errors goes down to the failure to initialize `Photo`. More specifically, this RuntimeException: `java.lang.RuntimeException: Internal graphics not initialized yet`. 



In `Photo.java`, you are initializing `photo` with type `Image`, which is a JavaFX component that depends on the JavaFX toolkit. This adds dependency for the JavaFX library right from the lower level classes. Thus, in unit testing, the JavaFX toolkit is not set up since only classes that extend `Application` (or subclasses of these classes) will start up the toolkit but here, only `MainApp.java` extends `Application`. Hence, `Image photo` cannot be initialized.



Perhaps you can let the `Photo` class have an instance variable that contains the file path of the image file, then instantiate the `Image` within the `Ui` component using this file path!
</panel>

</panel>
<panel type="info" header="### ISKANDAR ZULKARNAIEN B SUHAINI `@TheRealRavager` (7 contributions)" expanded>
<panel header="**2. :fas-info-circle: Remove SE-EDU navigation bar for tP product page?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/128" expanded>

Hi, can I check whether we are allowed/supposed to remove the SE-EDU navi bar? It says that we are to include it if the project is an official SE-EDU project but I'm not sure if that includes tP or whether its for educators to include in SE-EDU software.



![image](https://user-images.githubusercontent.com/43085796/66712628-1acbf500-edd2-11e9-83b0-eacf8a553904.png)


</panel>

<panel header="**3. :fas-info-circle: Object-level validation vs validating user input**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/9" expanded>

From what I know, there are two main ways to approach error handling. Object-Level validations (raise exception in constructor) and validating user input (in whatever class handles user input). 



Seems like the general consensus from [this](https://softwareengineering.stackexchange.com/questions/258275/oop-behavior-data-but-what-about-validation-behaviors) Stack Overflow question is that object level validation is the "right" way to approach things from an OO perspective (e.g. one response reads "The constructor should always return an instance which is in a valid state. There is no excuse for doing otherwise.") as you are more likely to accidentally create a god class that handles everything if you choose to validate user input. 



It seems that most of us chose to validate user input. Anyone have any opinions regarding this? Is validating both an excessive measure?
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/9#issuecomment-523763674" expanded>

Let's look at the Todo object for example. We could do validation in two ways:



1. Validate input before passing it to the constructor (perhaps by having a method in `Duke.java` raise exception if `description` is blank).



2. Validate user input in Todo constructor (perhaps by raising exception if `this.description` is `null`)



I'm thinking of whether option 2 would be more appropriate, since it results in the Todo class being responsible for not allowing "invalid" Todo objects to exist, as opposed to having the main class handle it or creating a new class specifically to validate inputs.
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/9#issuecomment-523882122" expanded>

Thanks for the response Sudharshan, really appreciate your contribution to the discussion.



About the input class, that makes a lot of sense. It just acts as a filter to remove inputs that are obviously gibberish or incomplete, while the respective objects deal with whether the input is "correct" (e.g. startTime < endTime).
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/11#issuecomment-523889772" expanded>

The difference between the two commands is that `git push --follow-tags` only pushes tags that are both annotated (similar idea to commit message) and reachable (in the current commit history).



Let's start with reachability. Imo it doesn't make sense to have a tag pointing to an unreachable commit (unless you, for some reason, want to keep a copy of it) and more importantly may confuse people.



As for annotations, they are there to give meaning to the tag you have created by giving a short summary of what the tag is for (e.g. what does "Level-6" of your project mean? What major change does it introduce?).



Hope this helped to clarify some of your doubts. I've only recently read up on tags so please correct me if I'm wrong. The Stack Overflow post links to [another](https://stackoverflow.com/questions/11514075/what-is-the-difference-between-an-annotated-and-unannotated-tag) post that explains annotated tags and their use cases quite well, I recommend giving it a read.
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/21#issuecomment-525341493" expanded>

Thanks Shawn, I believe your solution should quickly solve OP's issue. Lets take a moment to appreciate the difference between a revert and reset. [This](https://stackoverflow.com/questions/8358035/whats-the-difference-between-git-revert-checkout-and-reset) StackOverflow post should explain things pretty clearly.



TL:DR, a revert introduces another commit that basically undoes the reverted commit. A reset however, undoes changes by changing the commit history. 



An analogy would be as such: 

Imagine you were writing an essay and for every revision you would have a new copy (i.e. essay1.docx, essay2.docx, essay3.docx, essay4.docx). You mistakenly deleted your entire intro paragraph in essay3.docx and need to fix it. A revert would be to undo the deletion and save it as essay5.docx while a reset would be to delete everything from essay3.docx onwards and start from essay2.docx.



If you have the time to spare, I highly recommend [this](https://learngitbranching.js.org/) git tutorial. It gives really simple and elegant real-time visualisations of git branches as you perform commands, so you get a rough idea of whats happening to the commit history instead of it feeling like you're just playing with magical commands.



If anyone else has any tips regarding reverting/resetting please feel free to add on to the discussion
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/128#issuecomment-541397912" expanded>

Thanks Prof!
</panel>

</panel>
<panel type="info" header="### LEOW WEN BIN `@LeowWB` (7 contributions)" expanded>
<panel header="**2. :fas-info-circle: What exactly constitutes a bug?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/181" expanded>

I am somewhat confused as to what constitutes a "bug" for the PE. Which of the following count as bugs?



1. Application behaves in a manner described in the UG, but this behavior is unintuitive/confusing to user, or does not make sense.



2. Application behaves in a manner described in the UG. UG notes that this behavior is expected for certain inputs, but instructs user not to enter such inputs.



3. Application feature does not support an operation. UG does not mention this operation at all, however, user thinks the operation should be supported.
</panel>

<panel header="**3. :fas-info-circle: How to depict static method calls in sequence diagram?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/145" expanded>

Refer to question title. If a class is never instantiated, we can still call static methods of that class. How would we show this in a sequence diagram? In particular, what would the entity tag show? Should it still show `:ClassName` even when we are not calling methods on an instance of the class?
</panel>

<panel header="**4. :fas-info-circle: Requesting Permission to use Apache POI**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/117" expanded>

## Library



Apache POI

https://poi.apache.org



## Purpose



Write to .doc and/or .docx files
</panel>

<panel header="**5. :fas-info-circle: Clarification on tP constraints**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/92" expanded>

This is regarding `Constraints-Single-User` (shown [here](https://nus-cs2103-ay1920s1.github.io/website/admin/tp-constraints.html)).



If I were to add a feature that allows sharing of data (via exporting and importing a file), would that count as a violation of the constraint? I figure it might not be because it should be quite easy for a single user to test this feature, but I just want to be sure.
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/92#issuecomment-535003632" expanded>

I see. Thank you for the quick reply, Prof!
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/145#issuecomment-545805340" expanded>

Got it, thanks for the quick reply, prof!
</panel>

<panel header="**8 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/181#issuecomment-554728146" expanded>

Alright, thanks, prof!
</panel>

</panel>
<panel type="info" header="### ELLIE YEE WEN NA `@Ellieyee` (6 contributions)" expanded>
<panel header="**2. :fas-info-circle: Javafx lag**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/157" expanded>

## Environment



## Issue

I'm currently using panes to switch between certain displays. However, in the process of switching/displaying the panes, there is a significant lag (10s) during this process. I've confirmed that this isn't due to the generate() function as my logger (both before and after the function call) updates almost immediately. 



## Code/Log Trace

![image](https://user-images.githubusercontent.com/28653628/67935763-8224da00-fc05-11e9-8bca-4944f635b8de.png)


</panel>

<panel header="**3. :fas-info-circle: UIPartTest fail**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/133" expanded>

## Environment



main forked from addressbook3, runs on java11



## Issue



After adding new UI increments my tests for UiPartTest seem to fail. Specifically the 

constructor_missingFileUrl_throwsAssertionError() and 

constructor_invalidFileUrl_throwsAssertionError(). 

However, I have not modified the existing UIPart neither have I created any new UIPart within this iteration. (previous iterations have all passed).

Moreover, gradlew test shows Build Successful as well as my build report), whereas travis shows a build failed during the PR.

https://travis-ci.org/AY1920S1-CS2103-T14-2/main



## Code/Log Trace



My changes can be viewed here: https://github.com/AY1920S1-CS2103-T14-2/main/pull/61/files


</panel>

<panel header="**4. :fas-info-circle: Travis not auto-publishing docs**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/102" expanded>

## Environment



Describe your development environment



- IntelliJ version:

- Java version:

- Operating system version:

- _other packages' versions_



## Issue



Travis stopped auto-publishing docs https://github.com/AY1920S1-CS2103-T14-2/main/commits/gh-pages



I tried changing the github page source to master. But there is still no change. My local repo copy is also experiencing the same issue. Even though my repo shows the correct display, it's not being reflected in my team's github website and the module's Project List Page.






</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/102#issuecomment-536844782" expanded>

Fixed the issue by setting a new access token. Thanks for your help prof!
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/133#issuecomment-543559861" expanded>

yes! Thanks @shaoyi1997 :)
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/157#issuecomment-548310786" expanded>

commented out and tested. It seems to still be occurring but less frequent.
</panel>

</panel>
<panel type="info" header="### LUM WEI BOON `@lumwb` (6 contributions)" expanded>
<panel header="**2. :fas-info-circle: Request to use PDFBox Library**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/148" expanded>

## Library



[PDFBox](https://pdfbox.apache.org/2.0/getting-started.html)



## Purpose



To print JavaFX nodes into PDF file



## License



Apache Org


</panel>

<panel header="**3. :fas-info-circle: JavaFX scene throws cannot access evenTarget**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37" expanded>

Under part 1 of the JavaFX tutorial, my stage.setScene(scene) and stage.show() methods within the overriden start(Stage stage) method throws cannot access javafx.event.eventTarget?



How should I resolve this?
</panel>

<panel header="**4. :fas-info-circle: Enabling Issue Tracker**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/10" expanded>

Hi, 



May I ask how I should enable the issue tracker in my repository and how I can verify that the CS2103T bot can track my commits / labels for the duke project.



The "issue" checkbox has already been ticked in my github settings (see picture below):

![image](https://user-images.githubusercontent.com/25117015/63502623-898e7f80-c500-11e9-8f86-1d615187aeec.png)





Thank you.




</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/10#issuecomment-523827170" expanded>

@damithc thanks prof!



Just to confirm, the setting was already checked before I received a notification from the CS2103T bot. Is there a way I can verify the bot has access the issues page of my repo?
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-526970032" expanded>

![image](https://user-images.githubusercontent.com/25117015/64085039-e987f000-cd62-11e9-9496-2f20dc2bc933.png)





Apologies, please find attached the image of my Duke class. 
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-527195416" expanded>

Yes. You could try following the steps for non-gradle, and adding the JavaFX references manually.
</panel>

</panel>
<panel type="info" header="### LAWNCE GOH JIA WEI `@lawncegoh` (6 contributions)" expanded>
<panel header="**2. :fas-info-circle: Encountered error while trying to integrate reposense**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/139" expanded>

## Environment



Describe your development environment



- IntelliJ version: 11.0.4

- Java version: 12.0.2

- Operating system version: Mac Catalina



## Issue

Tried to integrate reposense into the repo but encountered errors while doing so that didn't allow for reading of the report



![Screenshot 2019-10-21 at 8 56 02 PM](https://user-images.githubusercontent.com/48293591/67206966-37f16b00-f445-11e9-92e6-fcdf626f99af.png)




</panel>

<panel header="**3. :fas-info-circle: Cant load image through the given file path**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/45" expanded>

**Have these 2 lines in my duke main class.** 



private Image user = new Image(this.getClass().getResourceAsStream("/images/DaUser.png "));

private Image duke = new Image(this.getClass().getResourceAsStream("/images/DaDuke.png "));



**These are the file paths:**



/Users/lawnce/Desktop/duke/src/main/resources/images/DaUser.png 

/Users/lawnce/Desktop/duke/src/main/resources/images/DaDuke.png 



This is the error i encounter. I tried solving through the Slack channel's way of renaming the file directly to resources or adding / in front of images but it doesn't work somehow



<img width="1038" alt="Screenshot 2019-09-05 at 11 29 28 AM" src="https://user-images.githubusercontent.com/48293591/64339637-08161180-d017-11e9-991e-68e65d10e8e1.png">
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/45#issuecomment-528482772" expanded>

Hi Prof, 



This is the link my duke.java



https://github.com/lawncegoh/duke/blob/master/src/main/java/Duke.java
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/45#issuecomment-528715745" expanded>

https://github.com/lawncegoh/duke
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/139#issuecomment-544590028" expanded>

@damithc I ran it with this command and it worked and I was able to see the report, but not with the usual command. What are the files I am missing?
</panel>

<panel header="**7 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/139#issuecomment-547196790" expanded>

If the above files are those we want to be considered, that means our group's reposense is fine right? Given the fact that we do not need to include any other types of files @damithc 
</panel>

</panel>
<panel type="info" header="### KENG JUN XIAN `@jxofficial` (5 contributions)" expanded>
<panel header="**2. :fas-info-circle: Process finished with exit code -1**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/60" expanded>

## Environment

- IntelliJ version: IntelliJ IDEA Community Edition 2019.2

- Java version: jdk-12.0.2

- Operating system version: Windows 10 Home



## Issue

After squash and merge branch A-CodeQuality and pushing it to the remote, I pulled using source tree back to the local repo. I encountered merge conflicts, resolved them and committed. I then pushed my master branch.  After that, I am unable to run Launcher class. No stack trace. 



I have tried reverting back to my previous changes, but all my attempts showed the same error.



```

Process finished with exit code -1

```



My source tree looks like this.

![image](https://user-images.githubusercontent.com/49927092/64669221-5736c900-d493-11e9-97b0-86426dc662ee.png)




</panel>

<panel header="**3. :fas-info-circle: No error stack trace, only Process finished with exit code -1.**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/59" expanded>

Please read up on how to write a [good question](https://stackoverflow.com/help/how-to-ask)



## Environment



Describe your development environment



- IntelliJ version: IntelliJ IDEA Community Edition 2019.2

- Java version: jdk-12.0.2

- Operating system version: Windows 10 Home

- _other packages' versions_



## Issue



After squash and merge branch A-CodeQuality and pushing it to the remote, I pulled using source tree back to the local repo. I encountered merge conflicts, resolved them and committed. I then pushed my master branch.  After that, my program keeps showing only one line of error when running Launcher class.





```

Process finished with exit code -1

```


</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-527272635" expanded>

It was working completely fine yesterday. But when I opened IntelliJ again today, I experienced the same error. Any ideas why?



Edit: Solved. No idea how, I suddenly got the option to add to classPath .... when i pressed Alt + Enter 

I'm not exactly sure what happened.


</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-527313740" expanded>

Ah yes, something useful to know. 



I have no idea what the duplicated modules are doing. Don't even know what a module is O: Hopefully Prof can explain a little bit about classpath, duplicated modules, what gradle does behind the scenes etc.



Shall not mess with the structure for the time being, but its always good to know how to remove modules. 
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/60#issuecomment-531178068" expanded>

OOPS I JUST SOLVED IT. 



```

  public String hiMessage() {

        String message = "Hello! I'm Duke.\n";



        try {

            storage.readFromTasksFileToList(tasks);

            message += "This is where you left off previously:\n";

        } catch (FileNotFoundException e) {

            message += "Fetching failed. " + e.getMessage() + "\n";

            message += "Creating file now...\n";

            File dukeTxt = new File(Duke.filePath);

            try {

                dukeTxt.createNewFile();

                message += "File created! " + dukeTxt.getAbsolutePath() + "\n";

                message += "Reading file...\n";

            } catch (IOException ioe) {

                message += "\t File creation was not successful. \n";

                message += "\t Exiting system.";

                System.exit(-1);

            }

        }



        message += getAllTasksAsString();



        assert !message.isEmpty();



        return message;

    }

```



THIS BLOCK OF CODE ): Please give @wilfredbtan 10 extra marks for his very helpful contribution during this very traumatizing period of my life LOL. 
</panel>

</panel>
<panel type="info" header="### FUNG BRIAN PEI-EN `@briyanii` (5 contributions)" expanded>
<panel header="**2. :fas-info-circle: Are testers still allowed to report bugs after the PE session?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/180" expanded>

Are testers allowed to report new bugs after the allocated hour of the PE session? Are these bugs reported after the hour-long session counted towards the grading?
</panel>

<panel header="**3. :fas-info-circle: Request to use RichTextFX**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/132" expanded>

## Library



[RichTextFX](https://github.com/FXMisc/RichTextFX)



## Purpose

Syntax highlighting in CLI and auto completion



## License



Dual-licensed under [BSD 2-Clause License](https://opensource.org/licenses/BSD-2-Clause) and [GPLv2 with the Classpath Exception](http://openjdk.java.net/legal/gplv2+ce.html).


</panel>

<panel header="**4. :fas-info-circle: Problem with iP Peer Evaluation on Luminus not saving properly.**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/122" expanded>

I had to close the survey before completing it, and load it again. 



However, I noticed that further changes to my response for question 12 are lost, even after I press the save for later button.
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/122#issuecomment-541327342" expanded>

Actually I found out why it was not saving.



It was because I had some text with < > around it and it was being removed.

The text including and after the first <something> was removed 
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/180#issuecomment-554663633" expanded>

Nevermind.
</panel>

</panel>
<panel type="info" header="### HON HAO CHEN `@honhaochen` (5 contributions)" expanded>
<panel header="**2. :fas-info-circle: Pushing branches to remote-repo**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/25" expanded>

-----------------------------------------------------------------------

fatal: The current branch branch-level-7 has no upstream branch.

To push the current branch and set the remote as upstream, use



    git push --set-upstream origin branch-level-7

-----------------------------------------------------------------------



Issue bot requested branches to be presented on the remote-repo

Thus, i checked out my branch-level-7 and try to push from there but i got this warning



Previously i just did branches, commited, then i checkout to my master and merge the branches without fast-forwarding



Any help on how to resolve this issue? Thanks!
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/25#issuecomment-526042362" expanded>

Yeah, no problem doing that, and I have completed way beyond the other branches in the master branch then this problem pops out ._.
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/25#issuecomment-526405540" expanded>

yeap, solved it. Thanks :D
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-527191712" expanded>

Hi, I have the same issue. Did you resolved it?
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-527263275" expanded>

Alright, thank you!
</panel>

</panel>
<panel type="info" header="### RAMACHANDRAN SANDHYA `@sandydays` (5 contributions)" expanded>
<panel header="**2. :fas-info-circle: Doubt in sequence diagrams loops**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/75" expanded>

This one of the sequence diagrams given in this week's material. 



![image](https://user-images.githubusercontent.com/50706672/65043865-608dcd00-d98e-11e9-8ca4-e8031e527f1d.png)



I have a doubt: Is it allowed to have the `while` loop outside an activation bar? I think I have seen both being drawn but I wasn't too sure. That is can a loop start before an activation bar is present i.e. considering the only three objects present are instances of `Foo`, `Bar`, and `Gee`? Would this answer change if there is are objects apart from these not shown in this diagram (from where the function calls like `do()` are coming, for example)?
</panel>

<panel header="**3. :fas-info-circle: Just creating new File object does not create a new File in a certain directory**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/27" expanded>

I tried this example on my desktop:



![image](https://user-images.githubusercontent.com/50706672/63935299-bb1ec200-ca8f-11e9-9e56-90c7bc253b2d.png)

When I run this Java program, I get this result instead:

```

file exists?: false

is Directory?: false

```



The file isn't created just by creating a new instance of the `File` object. As a result, I am also having trouble implementing `Level-7`. Any help as to how we can create a new file?
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/27#issuecomment-529116997" expanded>

Yes, it has been resolved! Thanks a lot for the help @dawo5010 and sorry for replying back to this a bit late!
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/75#issuecomment-532923893" expanded>

I see Prof, thanks for clarifying!
</panel>

<panel header="**6 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-536137250" expanded>

What I did was that I changed from `Label` to the shape `Text` in both my `MainWindow.java` and `DialogBox.fxml` (changed in `DialogBox.fxml` using Scene Builder). I had read up a bit on online forums and it seems that `Label` does not adjust based on the size of your text (in this case, the tasks that Duke prints), so there was a recommendation to use `Text` shape instead. Let me know if this works! 
</panel>

</panel>
<panel type="info" header="### NING SHENGYING `@ning-sy210` (4 contributions)" expanded>
<panel header="**2. :fas-info-circle: Junit Tests not able to run.**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/90" expanded>

## Environment



Describe your development environment



- IntelliJ version: Intellij IDEA Community Edition 2019.2.2 x64

- Java version: 11.0.4

- Operating system version: Windows 10 Home 1903



## Log Trace



```

"C:\Program Files\Java\jdk-11.0.4\bin\java.exe" -ea -Didea.test.cyclic.buffer.size=1048576 "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2019.2.2\lib\idea_rt.jar=58181:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2019.2.2\bin" -Dfile.encoding=UTF-8 -classpath "C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2019.2.2\lib\idea_rt.jar;C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2019.2.2\plugins\junit\lib\junit-rt.jar;C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2019.2.2\plugins\junit\lib\junit5-rt.jar;C:\Users\NINGS\.gradle\caches\modules-2\files-2.1\org.junit.jupiter\junit-jupiter-api\5.4.0\1a09f25a160f71c267f9ebe3b229b17805c683e9\junit-jupiter-api-5.4.0.jar;C:\Users\NINGS\.gradle\caches\modules-2\files-2.1\org.openjfx\javafx-base\11\ad3a4acfaa28b484d30c40c1f009445cc3f6e68b\javafx-base-11-win.jar" com.intellij.rt.execution.junit.JUnitStarter -ideVersion5 -junit5 @w@C:\Users\NINGS\AppData\Local\Temp\idea_working_dirs_junit.tmp @C:\Users\NINGS\AppData\Local\Temp\idea_junit.tmp -socket58180

Exception in thread "main" java.lang.NoClassDefFoundError: org/junit/platform/launcher/TestExecutionListener

	at java.base/java.lang.ClassLoader.defineClass1(Native Method)

	at java.base/java.lang.ClassLoader.defineClass(ClassLoader.java:1016)

	at java.base/java.security.SecureClassLoader.defineClass(SecureClassLoader.java:174)

	at java.base/jdk.internal.loader.BuiltinClassLoader.defineClass(BuiltinClassLoader.java:802)

	at java.base/jdk.internal.loader.BuiltinClassLoader.findClassOnClassPathOrNull(BuiltinClassLoader.java:700)

	at java.base/jdk.internal.loader.BuiltinClassLoader.loadClassOrNull(BuiltinClassLoader.java:623)

	at java.base/jdk.internal.loader.BuiltinClassLoader.loadClass(BuiltinClassLoader.java:581)

	at java.base/jdk.internal.loader.ClassLoaders$AppClassLoader.loadClass(ClassLoaders.java:178)

	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:521)

	at com.intellij.junit5.JUnit5IdeaTestRunner.createListeners(JUnit5IdeaTestRunner.java:39)

	at com.intellij.rt.execution.junit.IdeaTestRunner$Repeater.startRunnerWithArgs(IdeaTestRunner.java:45)

	at com.intellij.rt.execution.junit.JUnitStarter.prepareStreamsAndStart(JUnitStarter.java:242)

	at com.intellij.rt.execution.junit.JUnitStarter.main(JUnitStarter.java:70)

Caused by: java.lang.ClassNotFoundException: org.junit.platform.launcher.TestExecutionListener

	at java.base/jdk.internal.loader.BuiltinClassLoader.loadClass(BuiltinClassLoader.java:583)

	at java.base/jdk.internal.loader.ClassLoaders$AppClassLoader.loadClass(ClassLoaders.java:178)

	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:521)

	... 13 more

```

The attached are my settings for Gradle in Intellij. The problem here is that I can't run Junit tests by right-clicking but the same operation can be done using gradlew test. I can't seem to find the reason as to why this is happening.



![capture](https://user-images.githubusercontent.com/54129748/65566454-7a7a7180-df85-11e9-8db9-430874de332d.png)


</panel>

<panel header="**3. :fas-info-circle: Duke suddenly just does not run anymore.**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/86" expanded>

## Environment



Describe your development environment



- IntelliJ version: IntelliJ IDEA Community Edition 2019.2.2 x64

- Java version: 12.0.2

- Operating system version: Windows 10 1903

- _other packages' versions_



## Issue



Duke was running perfectly fine in Intellij when I input "gradlew run" into the console. So I created the jar file for Duke and tried running it, the Duke program loads when the jar file is run. However, Duke is now completely incapable of reading/writing into a local save file. 



Going back into Intellij, when I input "gradlew run" into the terminal again, I'm being thrown a bunch of error messages which I do not know the cause of. 



The code block below contains the errors that I faced when I input "gradlew run".

```

  > Task :run FAILED

Exception in Application constructor

Exception in thread "main" java.lang.RuntimeException: Unable to construct Application instance: class duke.Main

        at javafx.graphics/com.sun.javafx.application.LauncherImpl.launchApplication1(LauncherImpl.java:890)

        at javafx.graphics/com.sun.javafx.application.LauncherImpl.lambda$launchApplication$2(LauncherImpl.java:195)

        at java.base/java.lang.Thread.run(Thread.java:835)

Caused by: java.lang.reflect.InvocationTargetException

        at java.base/jdk.internal.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method)

        at java.base/jdk.internal.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62)

        at java.base/jdk.internal.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45)

        at java.base/java.lang.reflect.Constructor.newInstanceWithCaller(Constructor.java:500)

        at java.base/java.lang.reflect.Constructor.newInstance(Constructor.java:481)

        at javafx.graphics/com.sun.javafx.application.LauncherImpl.lambda$launchApplication1$8(LauncherImpl.java:802)

        at javafx.graphics/com.sun.javafx.application.PlatformImpl.lambda$runAndWait$12(PlatformImpl.java:455)

        at javafx.graphics/com.sun.javafx.application.PlatformImpl.lambda$runLater$10(PlatformImpl.java:428)

        at java.base/java.security.AccessController.doPrivileged(AccessController.java:389)

        at javafx.graphics/com.sun.javafx.application.PlatformImpl.lambda$runLater$11(PlatformImpl.java:427)

        at javafx.graphics/com.sun.glass.ui.InvokeLaterDispatcher$Future.run(InvokeLaterDispatcher.java:96)

        at javafx.graphics/com.sun.glass.ui.win.WinApplication._runLoop(Native Method)

        at javafx.graphics/com.sun.glass.ui.win.WinApplication.lambda$runLoop$3(WinApplication.java:174)

        ... 1 more

Caused by: java.time.format.DateTimeParseException: Text '12/12/12 1000-1800' could not be parsed, unparsed text found at index 13

        at java.base/java.time.format.DateTimeFormatter.parseResolved0(DateTimeFormatter.java:2052)

        at java.base/java.time.format.DateTimeFormatter.parse(DateTimeFormatter.java:1951)

        at java.base/java.time.LocalDateTime.parse(LocalDateTime.java:492)

        at misc.Parser.formatDeadline(Parser.java:153)

        at misc.Parser.convertStringToTime(Parser.java:90)

        at task.Deadline.<init>(Deadline.java:32)

        at misc.Parser.readTextAsTask(Parser.java:64)

        at misc.Storage.readTasksIntoTaskList(Storage.java:87)

        at misc.Storage.readSaveFile(Storage.java:77)

        at duke.Duke.<init>(Duke.java:33)

        at duke.Main.<init>(Main.java:16)

        ... 14 more



FAILURE: Build failed with an exception.



* What went wrong:

Execution failed for task ':run'.

> Process 'command 'C:\Program Files\Java\jdk-12.0.2\bin\java.exe'' finished with non-zero exit value 1



* Try:

Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.



* Get more help at https://help.gradle.org



BUILD FAILED in 1s

3 actionable tasks: 1 executed, 2 up-to-date



```


</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/86#issuecomment-533249842" expanded>

I wouldn't think it's an error with any of my java files in the project. Like I mentioned, the only thing that I did was creating a JAR file. I did no modifications whatsoever to the java files so I wouldn't think that the error lies there. Plus, when I sent the same JAR file to a friend of mine, he was able to run it without any problems. 



More specifically, I'm particularly concerned about these lines right here:

```

* What went wrong:

Execution failed for task ':run'.

> Process 'command 'C:\Program Files\Java\jdk-12.0.2\bin\java.exe'' finished with non-zero exit value 1

```



I could be wrong here but it seems something related to the jdk is wrong instead, and I don't know what it is.
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/86#issuecomment-533254350" expanded>

Wow thanks, deleting the saved file worked! I figured out that there was an entry in the save file that was written incorrectly, which resulted in the parse error.
</panel>

</panel>
<panel type="info" header="### GABRIEL CHIA WENHAO `@gachia` (4 contributions)" expanded>
<panel header="**2. :fas-info-circle: How do I get Gradle to use JDK 11 to build**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/28" expanded>

Hello,



I tried to implement Gradle into my project and wanted to test if Gradle is working correctly as per tutorial instructions. However, the build failed and it mentions that it is using my old jdk 8 folder (the source of the error) instead of my current jdk 11, which the project is running on. How do I point Gradle to use the jdk 11 folder to build?
</panel>

<panel header="**3. :fas-info-circle: Question on how to revert commits**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/21" expanded>

Hello,



For Level 7, I've unintentionally committed the merge of Level 7 with fast forward (by default) and I'm unsure of how to revert this commit.



After committing Level 7, I have also committed Level 8 (successfully without fast forward; can see "merge branch" commit) and that was when I realised what it meant by merging without fast forward.



How do I safety revert the commits for me to be able to merge branch Level 7 into master again without fast forward?
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/21#issuecomment-525358488" expanded>

Thank you Shawn and Iskandar for the help and info! I did Shawn's quick solution and managed to get the Merge commit up. Nonetheless, I appreciate and have noted the information both of you have shared😊.
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/28#issuecomment-526244831" expanded>

Thanks for the help! I managed to resolve it. Initially it didn't work even though I've set the system variable, so I had to restart my com and it worked afterwards.
</panel>

</panel>
<panel type="info" header="### TSAI, HSIAO-HAN `@TSAI-HSIAO-HAN` (4 contributions)" expanded>
<panel header="**2. :fas-info-circle: 💡 Mac OS user please use jdk11.0.2**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/44" expanded>

When I used jdk11.0.4, I encountered the error : **Graphics Device initialization failed for : es2, sw**. It seems to be a bug in java, and switching to jdk11.0.2 works for me.
</panel>

<panel header="**3. :fas-info-circle: javafx.controls not found**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/43" expanded>

When I tried to run Launcher, the FIndException always came out.

<img width="971" alt="Screenshot 2019-09-04 at 5 25 08 PM" src="https://user-images.githubusercontent.com/46244796/64243359-ce230d80-cf39-11e9-951a-1def9acc7978.png">





I follows the tutorial on Github, but still cannot figure out how to fix it.



This is the build.gradle file

<img width="493" alt="Screenshot 2019-09-04 at 5 25 30 PM" src="https://user-images.githubusercontent.com/46244796/64243402-de3aed00-cf39-11e9-924a-8e2ef309053a.png">



The configure and library

<img width="858" alt="Screenshot 2019-09-04 at 5 25 56 PM" src="https://user-images.githubusercontent.com/46244796/64243496-09254100-cf3a-11e9-8772-7c7f309fdb6d.png">

<img width="1056" alt="Screenshot 2019-09-04 at 5 26 22 PM" src="https://user-images.githubusercontent.com/46244796/64243507-0c203180-cf3a-11e9-9682-e96ef3b48278.png">

<img width="1078" alt="Screenshot 2019-09-04 at 5 26 36 PM" src="https://user-images.githubusercontent.com/46244796/64243530-18a48a00-cf3a-11e9-8453-6c33a2745740.png">



The javafx file path

<img width="605" alt="Screenshot 2019-09-04 at 5 24 51 PM" src="https://user-images.githubusercontent.com/46244796/64243599-307c0e00-cf3a-11e9-9fdd-359f5d2c8706.png">










</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/43#issuecomment-527848157" expanded>

Error message

<img width="1225" alt="Screenshot 2019-09-04 at 6 46 22 PM" src="https://user-images.githubusercontent.com/46244796/64248703-7d64e200-cf44-11e9-9088-db19b7994a8d.png">


</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/43#issuecomment-528242548" expanded>

I solved this problem by right click the libs in Project Structure and add it in module manually.(Although I have other error after this, but that is related to jdk version)
</panel>

</panel>
<panel type="info" header="### JOLYN TAN SI QI `@jolynnn8D` (4 contributions)" expanded>
<panel header="**2. :fas-info-circle: error: package javafx.application does not exist**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/62" expanded>

## Environment



- IntelliJ version: IntelliJ IDEA Ultimate 2019.2

<img width="815" alt="Screenshot 2019-09-11 at 3 40 15 PM" src="https://user-images.githubusercontent.com/41572120/64677611-7bea6b00-d4aa-11e9-8d76-283e2644588f.png">



## Issue



I am unable to implement JavaFX into my duke project - I've added the JavaFX library to the Project Structure as well as in the Edit Configurations window for both Duke and Launcher classes:

<img width="1022" alt="Screenshot 2019-09-11 at 3 41 39 PM" src="https://user-images.githubusercontent.com/41572120/64677741-c4a22400-d4aa-11e9-9d5d-ed0bdf124187.png">

<img width="1125" alt="Screenshot 2019-09-11 at 3 42 05 PM" src="https://user-images.githubusercontent.com/41572120/64677745-c66be780-d4aa-11e9-9eb7-f769dc9e0279.png">



However, when I run Launcher.main(), I get the following error even though the libraries seem to have been successfully imported within the code.

<img width="774" alt="Screenshot 2019-09-11 at 3 43 24 PM" src="https://user-images.githubusercontent.com/41572120/64677832-f1563b80-d4aa-11e9-83d3-7596a87c257c.png">



I have also attempted the Gradle method but it gives rise to another error which I suspect stems from the same issue:

<img width="774" alt="Screenshot 2019-09-11 at 3 44 38 PM" src="https://user-images.githubusercontent.com/41572120/64677922-1480eb00-d4ab-11e9-8f33-ff2408e4653f.png">



Any help would be greatly appreciated!! T__T
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/62#issuecomment-530680524" expanded>

Yep :( I still get the same error.
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/62#issuecomment-530937198" expanded>

I've pushed it onto the repo!
</panel>

<panel header="**5 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/62#issuecomment-531127685" expanded>

Fixed by deleting the wrapper folder, running gradle wrapper, then gradlew run
</panel>

</panel>
<panel type="info" header="### CHOONG YONG XIN `@choongyx` (3 contributions)" expanded>
<panel header="**2. :fas-info-circle: Level 10: Null Pointer Exception for Tutorial Part 4**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/36" expanded>

Hi, I have followed the tutorial for the steps but is currently facing a Null Pointer Exception error when running Launcher.



![image](https://user-images.githubusercontent.com/39525563/64082352-4de58800-cd40-11e9-99d2-f8caede708b3.png)



which seems to be caused from Main.

![image](https://user-images.githubusercontent.com/39525563/64089179-6de46e00-cd77-11e9-81d4-7a4c5cd02b16.png)



This is my directory for the .fxml files.

![image](https://user-images.githubusercontent.com/39525563/64082374-8a18e880-cd40-11e9-8f67-d635a2894b0d.png)



Would appreciate if anyone knows how to solve this!
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/36#issuecomment-526993256" expanded>

This is the link to my code: https://github.com/choongyx/duke/tree/branch-Level-10
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/36#issuecomment-526995416" expanded>

It works now, thank you!
</panel>

</panel>
<panel type="info" header="### LOONG JIAN HUNG, JOEL `@joloong` (3 contributions)" expanded>
<panel header="**2. :fas-info-circle: 💡 How to Safe-Delete a Field**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/70" expanded>

In week 6 tutorial 2 step 1, we need to safe delete the field `address` in `EditPersonDescriptor`. To safe delete, just highlight the field `address` and `alt-del`. Then move on to step 2.
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/79#issuecomment-532646316" expanded>

It might be due to your savedPath and triviaPath. The relative paths to the .txt and .json files from duke.jar and Duke.java are not the same.
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/110#issuecomment-537932048" expanded>

> The following question's answer is `False`. Why is Bot considered not keeping track of Mat class? Bot has Mat attribute.

> ![question](https://user-images.githubusercontent.com/25873970/66126467-0fcbd480-e61c-11e9-86c7-3e96fecab417.png)



For the first question, I believe it is because it is stated in the question to only refer to the



> **highlighted association in the code**






</panel>

</panel>
<panel type="info" header="### VOONG YU XUAN `@ambervoong` (3 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/33#issuecomment-526901026" expanded>

While I'm not sure if this will solve the specific problem, I did change mainClassName to Launcher and that made gradle run the application properly.
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/88#issuecomment-534026305" expanded>

Along with the debugger, using _Go To -> Implementation_ is very useful to quickly view a method's code. In addition to the above, here are fixes for two other failing test cases. Hope it will be of use to someone. 



1. `parseCommand_remark()`

- In `AddressBookParserTest.java`, update `assertEquals(new RemarkCommand(INDEX_FIRST_PERSON, remark), command);` to make `remark` a Remark object instead of a String.



2. `parseCommand_add()`

- `AddCommandParser.java` only returns new Remark(""). As mentioned above, update the code and add a new method to parse remarks in `ParserUtil.java`.

- `PersonUtil.getAddCommand(person)` calls `getPersonDetails(Person person)` which extracts the Person's details. Update it to support remarks by adding `sb.append(PREFIX_REMARK + person.getRemark().value + “ “);`


</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/135#issuecomment-542742685" expanded>

Association roles are used to indicate the **role played by the classes** in the association. For example, in an association between classes A and B, class A could play the role of the husband and class B plays the role of the wife. 



Association labels are the ones shown in the diagram you linked. They **describe the meaning of the association**.  An easy way to distinguish between them is the black arrow present in association labels. Also, it often describes a relationship whereas association roles tend to be nouns like 'friend' or 'helper'!



This diagram is false because an association label is shown in the diagram, not an association role. I can't remember exactly but I think the question was asking if this was a valid association role! Otherwise, it is a perfectly valid association label.
</panel>

</panel>
<panel type="info" header="### CHUA HUA LUN `@hua-lun` (3 contributions)" expanded>
<panel header="**2. :fas-info-circle: Request to use Asciidoctor Gradle plugin**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/151" expanded>

## Library

Asciidoctor, a fast text processor & publishing toolchain for converting AsciiDoc to HTML5, DocBook & more.

[Asciidoctor](https://asciidoctor.org)



## Purpose

Use the library to help with the writing of adoc files for user/developer guide.

{Explain for what kind of functionality you intended to use it for}



## License

MIT License - https://github.com/asciidoctor/asciidoctor/blob/master/LICENSE 

{Mention the license under which the library is released (e.g., MIT, GPL, Apache etc.) and give a link to the relevant page on their website}


</panel>

<panel header="**3. :fas-info-circle: Debugger: Target VM is not paused by breakpoint request**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/77" expanded>

Hi 

I am currently stuck at the Tutorial 1 - Tracing a Command Execution Path. When I enter 

`edit 1 n/Alice Yeoh` into addressbook3

the debugger states that the application is still running. 



I've paused the debugger and the message given was:

**Target VM is not paused by breakpoint request. Evaluation of methods is not possible in this mode**.



I've searched online and apparently, it is skipping breakpoints because of the source code in my console not matching with the one I'm running with. 



However, I am still rather confused as to how to go about and solve it.
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/151#issuecomment-547537562" expanded>

oh right, I've missed it by accident. Thanks for the tip!
</panel>

</panel>
<panel type="info" header="### KOH YI DA `@kohyida1997` (3 contributions)" expanded>
<panel header="**2. :fas-info-circle: What is the proper way to represent Functional Interfaces and call-backs using UML?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/154" expanded>

Hi Prof and classmates/tutors,



I am using Functional Interfaces in my tP to implement call-back functions and am wondering what the proper way to represent them in UML (class diagram?) is. 



From online sources I have found this: https://stackoverflow.com/questions/28095981/how-represent-a-java-functional-interface-in-a-component-diagram 

which doesn't seem to be in the scope of the textbook.



My usage is as such:



The class `AppManager` passes a method reference of one of it's own methods into a `Timer` class.

This method is stored inside the `Timer` class as a nested Functional Interface.



```

class AppManager {

    void appMethod() {

        // do something ...

    }



    public static void main(String[] args) {

        AppManager app = new AppManager();

        new Timer().set(app::appMethod);

    }

}



class Timer {

    

    CallBack callback;



    void set(CallBack callback) {

        this.callback = callback;

    }



    void eventOccured() {

        callback.inform();

    }



    @FunctionalInterface

    interface CallBack {

        void inform();

    }



}  

```
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/154#issuecomment-547983932" expanded>

Hmm... I understand what you mean, Prof. My main intention in using call-backs at all was to avoid cylic dependency and high coupling between `AppManager` and `Timer`. 



Initially, my idea was to describe the structural relationship this way:



1. `AppManager` is aware of `Timer`. 

2. `Timer` however is not directly aware of `AppManager` (`Timer` is only aware of a method of `AppManager`).



However, I realise if I were to draw this out as a Class Diagram, I would have

1. A solid arrow from `AppManager` to `Timer`

2. A dotted-arrow (?) from `Timer` to `AppManager` as `Timer` is "dependent" on `AppManager`'s method.



This depiction would suggest a cyclic dependency between `AppManager` and `Timer` ... which is what I am attempting to avoid. 
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/154#issuecomment-548325881" expanded>

Ah, understood- yes Timer can compile without AppManager indeed! Thanks for the insight and reply, Prof!! 
</panel>

</panel>
<panel type="info" header="### YAP JIA AUN `@Joanna-YJA` (3 contributions)" expanded>
<panel header="**2. :fas-info-circle: Request to use FontAwesomefx Library**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/164" expanded>

## Library 

FontAwesomefx  https://bitbucket.org/Jerady/fontawesomefx/src/master/



## Purpose

The library provides icons and vector graphics to be used in the Graphical User Interface.

{Explain for what kind of functionality you intende to use it for}



## License



FontAwesomeFX is licensed under the Apache 2.0 license. 


</panel>

<panel header="**3. :fas-info-circle: Request to use Jfeonix Library**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/163" expanded>

## Library

Jfeonix  https://github.com/jfoenixadmin/JFoenix





## Purpose

Jfeonix is a framework to create custom components for the Graphical User Interface. More specifically, JFXButton and JFXTextField is used. Can these components and the rest of the custom components in the library be used?



## License

Apache License 2.0


</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/163#issuecomment-550244854" expanded>

Apache License 2.0 is used.
</panel>

</panel>
<panel type="info" header="### LIM JUN HUP `@junhuplim` (3 contributions)" expanded>
<panel header="**2. :fas-info-circle: Format of HTML wrong when on website**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/176" expanded>

## Environment



- Java version: 11

- Operating system version: macOS Catalina Version 10.15.1



## Issue



[Here is my UG which you can see has the wrong format](https://ay1920s1-cs2103t-t12-3.github.io/main/UserGuide.html)



## Code/Log Trace



[Here are the commits](https://github.com/AY1920S1-CS2103T-T12-3/main/commits/master)



I believe that it is this commit [#243](https://github.com/AY1920S1-CS2103T-T12-3/main/commit/40587285f4fa59dc89cc59c6557d40b13185bb79) that has caused the behaviour. However, I have pushed another commit that revert these changes but the format of HTML remains wrong.



Would appreciate any help! Thank you!

<img width="1438" alt="Screenshot 2019-11-11 at 11 25 03 AM" src="https://user-images.githubusercontent.com/48384672/68560340-ae4d2000-047b-11ea-896a-e3a5151a12e6.png">


</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/176#issuecomment-552286679" expanded>

Edited the question to be more informative! Yes I have pushed another commit to revert the changes.
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/176#issuecomment-552289013" expanded>

Resolved! It is the presence of the whitespace at line 2 and 6 of the commit 

[#243](https://github.com/AY1920S1-CS2103T-T12-3/main/commit/40587285f4fa59dc89cc59c6557d40b13185bb79)
</panel>

</panel>
<panel type="info" header="### TIU WEE HAN `@tiuweehan` (3 contributions)" expanded>
<panel header="**2. :fas-info-circle: 💡 Image and Caption formatting in asciidoc**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/168" expanded>

Hi all, the following is a short guide on how to resize and position images and captions nicely in `asciidoc` for both HTML and PDF.



I couldn't find any resources only so it took a while to figure out how to format the images for my PPP. Hopefully this might be helpful for some of you =)



## Resizing Images



**Step 1.** The following is the standard way to embed images in `asciidoc`. By default, the width of the image in HTML will be 100% of the image size or 100% of the page width, whichever is smaller.



Example:

```

.This is my image

image::my_image.png[]

```

translates to

![image](https://user-images.githubusercontent.com/39181981/68538267-bf7b2b80-03ac-11ea-8027-e27f90d49486.png)



**Step 2.** To resize the image for HTML, use the `width` attribute of the image. You can adjust the size using either the percentage of page width (e.g. `width=50%`) or by absolute size of the image (e.g. `width=10cm`).



Example:

```

.This is my image

image::my_image.png[width=50%]

```

translates to

![image](https://user-images.githubusercontent.com/39181981/68538304-534cf780-03ad-11ea-910a-b4e8baebb849.png)



However, this might cause formatting issues when exporting to PDF, as seen below

![image](https://user-images.githubusercontent.com/39181981/68538750-8941aa00-03b4-11ea-8663-6f3c5d57d5cf.png)



**Step 3.** To adjust the width of an image in PDF, use the `scaledwidth` attribute instead. The `scaledwidth` attribute can be used together with the `width` attribute without causing formatting issues for HTML. However, do note that the `scaledwidth` attribute can only be adjusted by absolute size (e.g. `scaledwidth=12cm`)



Example:

```

.This is my image

image::my_image.png[width=50%, scaledwidth=12cm]

```

which translates to

![image](https://user-images.githubusercontent.com/39181981/68538777-c1e18380-03b4-11ea-9748-c875d717202d.png)





## Positioning images

Images like UML diagrams and captions should ideally be aligned to center.  While it is possible to align images to the center in HTML, ~**it is currently not possible to do so for captions in HTML**.~ See @geshuming comments on this PR on how to do it for captions in HTML. However, it is still possible to do so in PDF.



**Step 1.** To align images (but not captions) in the center for both HTML and PDF,. use the `align` attribute.



Example:

```

.This is my image

image::my_image.png[align="center", width=50%, scaledwidth=12cm]

```

which translates to

![image](https://user-images.githubusercontent.com/39181981/68538462-c5bed700-03af-11ea-8bd5-8dc6ed91dd0e.png)



**Step 2.** To align both images AND captions in the center for PDF, a few more steps are needed. Instead of using the PDF feature in Intellij, we have to install a command line version of `asciidoctor-pdf` from [this link](https://asciidoctor.org/docs/asciidoctor-pdf/).



**Step 3.** By default, `asciidoc-pdf` aligns images and captions to the left, so we need to change this configuration. In the command line, execute the following command to find the directory where the ruby gems are stored



Example:

```

gem environment 

```

![image](https://user-images.githubusercontent.com/39181981/68538545-3ca89f80-03b1-11ea-8ca4-c12bf115219b.png)



In this case, my gems are stored at `/Users/tiuweehan/.rbenv/versions/2.6.3/lib/ruby/gems/2.6.0`



**Step 4.** Find the directory where `asciidoctor-pdf` is stored. In this case, mine is stored at `/(ruby gems directory)/gems/asciidoctor-pdf-1.5.0.beta.7/`.

![image](https://user-images.githubusercontent.com/39181981/68538604-3e269780-03b2-11ea-8db6-26a613f008bf.png)



**Step 5.** Edit the configuration file at `/(current directory)/data/theme/default-theme.yml`.

![image](https://user-images.githubusercontent.com/39181981/68538629-8c3b9b00-03b2-11ea-8d91-57963056c496.png)



**Step 6.** Change the value under `caption > align` from `left` to `center` (See line 132)



Example:

```

caption:

    align: center

```

![image](https://user-images.githubusercontent.com/39181981/68538638-d1f86380-03b2-11ea-9b28-368da5f8782c.png)



**Step 7.** Now cd to the directory where the adoc file is and use `asciidoctor-pdf` to export the adoc file to PDF.



Example:

```

asciidoctor-pdf my_ascii_doc.adoc -o my_ascii_doc.pdf

```

The exported PDF should now be aligned nicely

![image](https://user-images.githubusercontent.com/39181981/68538409-b8edb380-03ae-11ea-83fc-52e67f7af60f.png)


</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/168#issuecomment-552165243" expanded>

> For positioning in HTML, I modified the `asciidoctor.css` file in `/stylesheets` to align the imageblocks.

> [The commit I made can be found here](https://github.com/AY1920S1-CS2103T-W13-1/main/commit/1637f6f60f1423dd00a76585ec49ce15723ef91d) It was a small fix that didn't warrant installing applications/plugins, in my opinion.

> 

> > it is currently not possible to do so for captions in HTML

> 

> My commit also aligns the caption, so for anyone wondering if you can, you can.



This is even better!



Edit: Didn't manage to get this to work for me though :(
</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/168#issuecomment-552169273" expanded>

> > Edit: Didn't manage to get this to work for me though :(

> 

> I don't think it shows up in the preview on the IDE, but it shows up for my team's site as well as deployment previews



Oh you're right, I see it in my deployment previews now. But this method doesn't seem to work for exporting to pdf through IntelliJ though
</panel>

</panel>
<panel type="info" header="### MURUGESAN KARTHIKA `@kzrthikz` (3 contributions)" expanded>
<panel header="**2. :fas-info-circle: 2 modules in a project cannot share same content root**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/56" expanded>

I am facing some issues with setting up the GUI. I tried to set up via gradle but am getting compilation errors like package javafx.Application does not exist. So I tried to manually download and import the lib into intellij but get the following error. 

<img width="1061" alt="Screenshot 2019-09-10 at 6 03 48 PM" src="https://user-images.githubusercontent.com/50614346/64613819-ac2dfd00-d409-11e9-83d1-6200cac84bdc.png">




</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/56#issuecomment-529921947" expanded>

<img width="1440" alt="Screenshot 2019-09-10 at 8 56 14 PM" src="https://user-images.githubusercontent.com/50614346/64615647-90c4f100-d40d-11e9-9b96-bf7f1aa51228.png">

<img width="1067" alt="Screenshot 2019-09-10 at 8 56 41 PM" src="https://user-images.githubusercontent.com/50614346/64615665-9b7f8600-d40d-11e9-9f08-ea9e8a504efc.png">


</panel>

<panel header="**4 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/56#issuecomment-529929372" expanded>

yes that fixed the problem! Thank you 
</panel>

</panel>
<panel type="info" header="### NG YONG KUAN `@SendorasLeft` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Good Practices for Exception classes / Level-7 Implementation**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/20" expanded>

Regarding SE practice for defining custom exceptions:

1. For different custom exceptions in Duke, is it a better SE practice to

a. define new sub-classes of Exception for each different error (eg. NoSuchTaskType, ShutDownException, InvalidTaskId), or

b. use one exception (DukeException) initialised with different error messages in its constructor?

2. If 1a is preferred, should we continue to extend all these custom exceptions from Exception, or should we extend them from DukeException instead?



Regarding Level-8 implementation:

1. For Level-8 (saving), are we allowed to implement it by object serialization, or must we strictly make our own "interpreter" to store it in a custom text form, then load it back by parsing through the text file?
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/20#issuecomment-531649927" expanded>

All the suggestions here have been great so far. Admittedly, my original examples were a little contrived for the sake of the discussion (if anyone was wondering, no, I definitely did not use an invalidTaskId custom exception). 



To sum up for any future readers, the general consensus seems to be that we first re-use any exceptions that's already defined in the Standard Java SDK (I would think that this applies even to third-party SDKs if there's a heavy reliance on them in the project), and if that is not sufficient for describing the exception, we extend our own from wherever is applicable/most-related. The aim is to make the Exceptions as understandable as possible to future programmers, and one clearest way of doing it is to use Exceptions that are already standardised among all programmers in the standard SDK.



My personal take on this issue so far has been to define a custom DukeException class with an overloaded constructor that takes in both an exceptionMessage as well as a Throwable cause (essentially, the original exception that caused it eg. IndexOutOfBoundsException). The DukeException wrapper around the the original exception makes it neater to deal with the way Duke handles most exceptions (by throwing the message to the user in some user-readable form eg. "You need to provide me with a task ID!" when no task ID is given). Chaining the exception with a DukeException also makes it clear that I as the programmer expected this specific error to occur and have attempted to handle it for the specific usage (instead of having a random IndexOutOfBoundsException occur, which is very clear in what was violated but not so much as to what it means for the specific functioning of the program ie. the cause-effect relationship). It's kind of a compromise, so to speak. 

Furthermore, in the rare cases when I need more specific information to handle the exception at a lower-level (which is unlikely at this stage, but you never know in the future), I can simply retrieve the root cause of the DukeException by calling getCause() on the DukeException or by performing a detailed stackTrace print.



Hope this is helpful. Since it's well into week 6, and this being a week 3 issue with satisfactory answers, I'll be closing the issue here. Do feel free to re-open this if you feel there are more points that merit discussion! Thanks to everyone who took their time to reply.
</panel>

</panel>
<panel type="info" header="### CHONG GUANG JUN `@tcgj` (2 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/16#issuecomment-524396616" expanded>

Yup, basically the root directory is your main "duke" folder, which contains your .git directory, the src folder, and everything else.
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/115#issuecomment-539075371" expanded>

Thanks for sharing!
</panel>

</panel>
<panel type="info" header="### ZHANG XUAN `@zhangxuan97` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Request to use JFreeChart**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/130" expanded>

## Library



[JFreeChart](http://www.jfree.org/)



## Purpose



To generate charts to better visualise data and statistics.


</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/130#issuecomment-541406069" expanded>

[GNU Lesser General Public Licence](http://www.jfree.org/lgpl.php)
</panel>

</panel>
<panel type="info" header="### LING ZHI WEI `@lzw12345` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Request to use Jackson/standard JSON library**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/96" expanded>

## Library



{https://github.com/FasterXML/jackson}



## Purpsoe



{To aid in storing and reading data in JSON format}


</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/96#issuecomment-535518673" expanded>

Actually this is for my IP, is it still ok?
</panel>

</panel>

<panel type="info" header="### TUAN DING WEI `@tuandingwei` (2 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552096062" expanded>

Try checking your test cases. It could be that you might have failed one of the test cases.
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/157#issuecomment-552096555" expanded>

Could it be because:



1. Certain execution takes some time to run?? i.e. code might not be efficient

2. getChildren() adds to the delay



If the delay is from the switch command, you might want to trace your code from the switch. 

If this happens when you start the app, this might mean that certain code is taking too long to run. 
</panel>

</panel>
<panel type="info" header="### TAN YAN ZHEN, NATALIE `@nattanyz` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Error: Could not find or load main class Duke**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/53" expanded>

## Environment

I am using IntelliJ 2019.2 on Windows 10, with JDK 12.0.2.



## Issue

Sometimes, I will be unable to run my code, as I will receive "Error: Could not find or load main class Duke", as shown in the following screenshot.

This error seems to appear intermittently. Occasionally, closing and reopening IntelliJ seems to fix it.

![image](https://user-images.githubusercontent.com/27663706/64501418-d5f50000-d2f3-11e9-82d4-bde9561f3086.png)

Please see my directory structure and part of my build.gradle file in the screenshot above.



I suspect this error has something to do with the Java Classpath, because the previous time it occurred, I was able to fix it by removing environment variables associated with older versions of Java.

However, I have not changed any environment variables in the past few days before this error occurred again this morning. Please see this screenshot of my environment variables:

![image](https://user-images.githubusercontent.com/27663706/64501525-4ac83a00-d2f4-11e9-8689-60c1657c2dfe.png)



`where java` seems to return the correct version of JDK:

![image](https://user-images.githubusercontent.com/27663706/64501901-0342ad80-d2f6-11e9-8960-b78f58e5a8f8.png)

The Project SDK in my project settings seems to be correct as well:

![image](https://user-images.githubusercontent.com/27663706/64501996-659bae00-d2f6-11e9-9e7b-96cbdb1b7e30.png)

Could I check if the content root is set correctly?

![image](https://user-images.githubusercontent.com/27663706/64502024-7a784180-d2f6-11e9-8645-d737ea374e4f.png)



Any help is greatly appreciated! :)
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/53#issuecomment-529289072" expanded>

Hmm... seems like removing `package duke;` from Duke.java fixes this issue. Is this expected? Should Duke.java not be in the package? Furthermore, should the `mainClassName` in build.gradle be set to "Duke" or "duke.Duke"? Thanks!
</panel>

</panel>


<panel type="info" header="### WANG RUNDING `@R-D-D-D` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Could not open jar file**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/69" expanded>

Please read up on how to write a [good question](https://stackoverflow.com/help/how-to-ask)



## Environment



Describe your development environment



- IntelliJ version: 2019.2

- Java version: 11.0.4

- Operating system version: Mac OS Mojave 10.14.6

- _other packages' versions_



## Issue



When I am trying to double click and open the jar file compiled using gradle shadowJar on a mac with Jar launcher(A mac utility app to open jar file), it prompts me saying it cant be lauched and check console for error message. The closest two things in my console that looks like an error message is in the code below, but after much googling I cant seem to figure out what is the problem, may I get some help? The jar file runs perfectly fine when opened from terminal. Will this affect grading since grading is based on jar file?



```

LSExceptions shared instance invalidated for timeout.



NSApp cache appearance:

-NSRequiresAquaSystemAppearance: 0

-appearance: (null)

-effectiveAppearance: <NSCompositeAppearance: 0x600000a686e0

 (

    "<NSDarkAquaAppearance: 0x600003c6f6c0>",

    "<NSSystemAppearance: 0x600003c6f240>"

)>

```


</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/69#issuecomment-531756099" expanded>

It runs fine with java -jar command. I tried using java 11.0.2 instead but it does not change anything.
</panel>

</panel>
<panel type="info" header="### FABIAN CHIA HUP PENG `@fabbbbbbyy` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Unable to import changes for JavaFX using Gradle**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/34" expanded>

Caused by: java.lang.UnsupportedClassVersionError: org/openjfx/gradle/JavaFXPlugin has been compiled by a more recent version of the Java Runtime (class file version 55.0), this version of the Java Runtime only recognizes class file versions up to 52.0
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/34#issuecomment-526829463" expanded>

I wasn't, so I switched it under Project Structure but I still got the same error.
</panel>

</panel>
<panel type="info" header="### LIM YONG SHEN, KEVIN `@lyskevin` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Request to use javafx-calendar library**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/127" expanded>

## Library



[javafx-calendar](https://github.com/SirGoose3432/javafx-calendar)



## Purpose



Implement calendar view in TP application


</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/127#issuecomment-541409708" expanded>

Ok thanks for the advice! I will look into other libraries first then.
</panel>

</panel>
<panel type="info" header="### TAN DE NING, KLEMENT `@klementtan` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Request to use Google Maps API and NUS Mods API**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/84" expanded>

## Library



Google Maps - https://cloud.google.com/maps-platform/?apis=maps

Nus Mods - https://api.nusmods.com/v2/



## Purpsoe



Google Maps to find the closest common meeting spaces for friends



NUS Mods API to find the common free time among friends


</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/84#issuecomment-533453174" expanded>

Thank you prof!
</panel>

</panel>
<panel type="info" header="### POH JIA HAO `@limerencee` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: [Potential Spoilers] Questions on Lecture 7 Quiz (Part 1)**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/110" expanded>

Hello everyone, after doing the quiz, I am confused by some of the answers.



The following question's answer is `False`. Why is Bot considered not keeping track of Mat class? Bot has Mat attribute.

![question](https://user-images.githubusercontent.com/25873970/66126467-0fcbd480-e61c-11e9-86c7-3e96fecab417.png)



The following question's answer is `False`, with the reason being that: `This is not an association role. It's an association label.` Why is this not a valid diagram? In the textbook, the label `used by` is valid for Admin<->Student. From what I understand, these association labels are to describe the verb, so `helped by` should be a valid label.

![image](https://user-images.githubusercontent.com/25873970/66126703-aa2c1800-e61c-11e9-99f1-29298897d895.png)



The following question's answer is `False`, with the reason being that: `A Mat can have up to 5 helpers, not exactly 5 helpers.` The code shows `new Bot[5]` so that made me confused.

![image](https://user-images.githubusercontent.com/25873970/66126931-2aeb1400-e61d-11e9-83b9-fb534ccacdb2.png)


</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/110#issuecomment-537962485" expanded>

Thank you for your replies, my doubts are cleared. :smile: 
</panel>

</panel>
<panel type="info" header="### LEE BO QIANG `@lightz96` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Level 2**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/2" expanded>

Do we need to save the command "bye" and "list" to the list?
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/2#issuecomment-522245929" expanded>

Ok, thanks Prof.
</panel>

</panel>
<panel type="info" header="### BENEDICT PAK HONG JUN `@Nanosync` (2 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/62#issuecomment-530502678" expanded>

Have you tried re-importing the gradle project by hitting the refresh button in the Gradle tab of IntelliJ?
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/64#issuecomment-531274087" expanded>

As @geshuming mentioned, those are the errors. To prevent such issues, you can try adding `*.iml` to `.gitignore` and remove the related files from the repository since they are generated by IntelliJ.
</panel>

</panel>
<panel type="info" header="### TAN JUN BANG `@junnbang` (2 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/54#issuecomment-529295976" expanded>

Hello, I also ran into the same problem. For me, it was due to the mainClassName in build.gradle. After i changed it to "Launcher", then the error is gone.



> application {

    mainClassName = "Launcher"

}



Otherwise, check if you imported the javafx files into ur jar file before building it.
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-535928582" expanded>

Maybe you can try setting your VBox / Hbox (which ever u use to wrap your content) Min height/width to USE_PREF_SIZE via the SceneBuilder.
</panel>

</panel>
<panel type="info" header="### YEHEZKIEL RAYMUNDO THEODOROES `@Yehezkiel01` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Labelling an issue which is not exactly the user story but part of the story.**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/119" expanded>

What should I label an issue which is not exactly the user story but part of the story?



For instance, my user story is "As a user I want to add a new contact".

Later on, I break it into 2 smaller issues, which are:

1. "Parse 'contact create' command into CreateCommand object"

2. "Implement CreateCommand object"



Should I label both of them as type.Task or type.Story?
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/119#issuecomment-540214664" expanded>

Thank you very much
</panel>

</panel>
<panel type="info" header="### SEOW ZHI XIAN GABRIEL `@gabrielseow` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Request to use iCal4j library**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/170" expanded>

## Library



iCal4j : https://github.com/ical4j



## Purpose



iCal4j library used to parse .ics calendar files for our application feature to compare timetables and schedule meetings during common available times.



## License



The license is owned by Ben Fortuna

URL: https://github.com/ical4j/ical4j/blob/develop/LICENSE.txt
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/170#issuecomment-552168179" expanded>

Sorry, I updated the links
</panel>

</panel>
<panel type="info" header="### JASMINE YEO JIA MIN `@jaesimin` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Unable to open JAR file**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/138" expanded>

Please read up on how to write a [good question](https://stackoverflow.com/help/how-to-ask)



## Environment



Describe your development environment



- IntelliJ version: 2019.2.2

- Java version: 11.0.2

- Operating system version: Windows 10

- _other packages' versions_



## Issue



Unable to double-click / run the command 'java -jar duke-0.2.jar' for the JAR file that I had created using 'gradlew shadowJar' . I am only able to right-click the JAR file and run it in IntelliJ. 



I had added and removed the dependencies according to #72.



There's no error in all the steps. The JAR file just doesn't work. Why?



## Code/Log Trace



Executing 'gradlew run' works:



![image](https://user-images.githubusercontent.com/54024708/67156031-1cef0000-f34c-11e9-86c3-96b4184dff8b.png)



Running 'java -jar duke-0.2.jar' command:



![image](https://user-images.githubusercontent.com/54024708/67156005-ced9fc80-f34b-11e9-80fe-c921f305ea6f.png)



Right-clicking JAR file in Intellij works:



![image](https://user-images.githubusercontent.com/54024708/67156013-ea450780-f34b-11e9-9422-5c9b8ceadb68.png)



![image](https://user-images.githubusercontent.com/54024708/67156025-f92bba00-f34b-11e9-96c6-a65c26c051fb.png)




</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/138#issuecomment-544230106" expanded>

Thank you! It works already :)
</panel>

</panel>
<panel type="info" header="### ONG PANG YI MARCUS `@marqueurs404` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Request to use ical4j Library**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/95" expanded>

## Library



ical4j - https://github.com/ical4j/ical4j



## Purpsoe



To parse iCalendar (.ics) files for importing/exporting calendars.


</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/95#issuecomment-535506285" expanded>

Thanks prof!
</panel>

</panel>
<panel type="info" header="### WEN SHUFA `@woon17` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Activity diagram for switch case**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/144" expanded>

For the activity diagram, if I have switch case (4 cases), can I just use one diamond and output 4 lines for 4 different cases?
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/144#issuecomment-545720412" expanded>

Reference: 

https://deploy-preview-142--nus-cs2103-ay1920s1.netlify.com/images/GotoActivityDiagram.png
</panel>

</panel>
<panel type="info" header="### SONG TIANYI `@tysng` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: PE Dryrun: can CS2103T students still join the 12-2pm lecture slot?**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/152" expanded>

Hi Prof,



The PE Dry Run is scheduled during this Friday's lecture slot. My original lecture slot is 4-6pm, may I still join the 12-2pm slot this week too?
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/140#issuecomment-545887173" expanded>

Just to add on, you will need `git add` the files that you have fixed before running the above command again. Otherwise, you may see the same error thrown despite having fixed the problem. The reason is that `run-checks.sh` will call `git grep --cached` which searches in the staging area.
</panel>

</panel>
<panel type="info" header="### LEE LI YING IRENE `@irene-lly` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Location is not set exception**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/71" expanded>

## Environment



- IntelliJ version: 2019.2

- Java version: 11.0.4

- Operating system version: Windows 10



## Issue



I am having some problems opening the jar file, when I try running java -jar duke.jar this is what is shown:



![Screenshot (10)](https://user-images.githubusercontent.com/54141404/64935368-7793c880-d883-11e9-9515-585e9ec26ce6.png)



here is my project structure:



![Screenshot (12)](https://user-images.githubusercontent.com/54141404/64935380-867a7b00-d883-11e9-8ecf-78216a53c5d5.png)



and here is my Main.java:



![Screenshot (15)](https://user-images.githubusercontent.com/54141404/64935505-4798f500-d884-11e9-827a-d4fa26abee50.png)



does anyone know why this exception is shown?
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/71#issuecomment-531847842" expanded>

Okay I have finally managed to solve it by marking the "resources" directory (../src/main/resources) as a "Resources Root" in intellij.



![Screenshot (16)](https://user-images.githubusercontent.com/54141404/64974670-d8e98500-d8df-11e9-80d9-977d94f8708e.png)




</panel>

</panel>
<panel type="info" header="### CHEN ANQI `@anqichen9856` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Used ArrayList data structure right from the start**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/13" expanded>

I used ArrayList structure for storing tasks since Level-2, and added both tags "A-Collections" and "Level-2" to the same commit. Do I need to use Array instead and redo the levels?
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/13#issuecomment-523883723" expanded>

@damithc I see. Thank you!
</panel>

</panel>
<panel type="info" header="### LIU XIAOYU `@xiaoyu-nus` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Cannot Use Gradle from within Intellij**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/42" expanded>

![image](https://user-images.githubusercontent.com/51201915/64225838-acad2c00-cf0f-11e9-9221-43a134753e92.png)

I believe my Gradle has been added to the project successfully. However, under "_Using Gradle from within Intellij_" , all three methods fail. In my Intellij under Settings -> Build -> Build Tools, I cannot find Gradle either.

![image](https://user-images.githubusercontent.com/51201915/64225938-0f062c80-cf10-11e9-8bcb-8530c52ac44f.png)

I am not sure which step went wrong. Can anyone help?


</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/42#issuecomment-527782298" expanded>

I have realised I have to install Gradle on Intellij on the starting page under config. Installing Gradle solved the problem.
</panel>

</panel>
<panel type="info" header="### KWONG CHUNG YUE JERRY `@jerryk1997` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Error: JavaFX runtime components are missing, and are required to run this application**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/63" expanded>

- IntelliJ version:2019.2.2

- Java version:11.0.2



When I created the jar file as per the first instructions of the week 5 project tasks using shadowJar, when I run the jar file this error appears and I've went online to check what to do and tried most of it but the problem still persists.



Did some things that the others who encountered this problem used to resolve this problem such as building again and refreshing the dependencies etc but nothing seems to work.



Anyone has any idea what might be causing this?



Below: are screenshots of some of my configurations:

<img width="1025" alt="Screenshot 2019-09-11 at 4 27 01 PM" src="https://user-images.githubusercontent.com/54168384/64681219-e0f58f00-d4b1-11e9-8079-fad5230499a4.png">

<img width="1025" alt="Screenshot 2019-09-11 at 4 27 21 PM" src="https://user-images.githubusercontent.com/54168384/64681225-e3f07f80-d4b1-11e9-91d0-3f83dd7f9829.png">

<img width="1028" alt="Screenshot 2019-09-11 at 4 27 35 PM" src="https://user-images.githubusercontent.com/54168384/64681240-ea7ef700-d4b1-11e9-8b31-6a3754932d74.png">

<img width="1025" alt="Screenshot 2019-09-11 at 4 27 48 PM" src="https://user-images.githubusercontent.com/54168384/64681244-ebb02400-d4b1-11e9-8277-7a6575aac1c4.png">

<img width="486" alt="Screenshot 2019-09-11 at 4 29 21 PM" src="https://user-images.githubusercontent.com/54168384/64681249-ee127e00-d4b1-11e9-93c1-2148bb21c368.png">

<img width="677" alt="Screenshot 2019-09-11 at 4 29 35 PM" src="https://user-images.githubusercontent.com/54168384/64681255-f1a60500-d4b1-11e9-93e2-332646de4217.png">




</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/63#issuecomment-530287751" expanded>

Yes, thank you! I didn't see that sorry.
</panel>

</panel>
<panel type="info" header="### VEGI MANAS `@ManasVegi` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: Not Able To Run JUnit Tests**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/32" expanded>

![Screenshot (18)](https://user-images.githubusercontent.com/53593482/64061363-5046c580-cc0c-11e9-98f9-3d3cbe43f759.png)

I made a test folder in 'src', marked it as test source root, made the DukeTest.java with a dummyTest to try if it works.

No matter how many times I tried, I get an "Error: java: error: release version 13 not supported."



I tried running it using gradle.

I have tried keeping the test folder in different places, set up the project again and imported junit 5.4 from maven libraries since it was asking me to add android studio sdk to ass directly.



Couldn't really find a helpful solution on the internet. 

Any suggestions on how to go about with this? 



Addition1: Testing works just fine in a local repo of mine. The issue is in the dukerepo.



Addition2: I set up gradle. When I try running 'gradle test' it shows "Test events not received" everytime.
</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/32#issuecomment-526995671" expanded>

![Screenshot (19)](https://user-images.githubusercontent.com/53593482/64090042-ba31ad00-cd7b-11e9-963a-fb8f1870551e.png)


</panel>

</panel>
<panel type="info" header="### BALAM SAI ROHIT REDDY `@ROHITREDDYBALAM` (2 contributions)" expanded>
<panel header="**2. :fas-info-circle: JNI exception**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/61" expanded>

- IntelliJ version: 2019.2

- Java version: jdk 11.0.4



## Issue

When I am trying to open the JAR file, it shows A JNI error has occurred, please check your installation and try again.

What could be the problem?


</panel>

<panel header="**3 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/61#issuecomment-530434438" expanded>

My terminal was running on JDK 1.8 Prof when I compiled the program some time ago. But for creating the shadowJar, I had to update it to JDK 11. I think the error occurred due to the difference in JDK versions for compilation and creation of Jar. So I just compiled the program again (JDK 11). It is working now but I am not very sure if that was the problem. 😕 
</panel>

</panel>


<panel type="info" header="### TEE HAO WEI `@thwnus` (1 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/151#issuecomment-547524999" expanded>

Doesn't it [already](https://github.com/nus-cs2103-AY1920S1/addressbook-level3/blob/master/build.gradle#L13) [do so](https://github.com/nus-cs2103-AY1920S1/addressbook-level3/blob/master/build.gradle#L117-L144)?
</panel>

</panel>
<panel type="info" header="### ANG WEI HENG KENDRICK `@KendrickAng` (1 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/88#issuecomment-533785777" expanded>

The fixes mainly involve integrating the Remark class with the rest of addressbook. I've also put my changes in a [commit](https://github.com/KendrickAng/main/commit/9b7159bc66317fb7a83e9fbe76bba82b15c8c0a5), which follows immediately from the end of the tutorial.



Here's my (very incomplete) notes trying to figure out what went wrong:



**1. execute_storageThrowsIoException_throwsCommandException**

- AddCommandParser should be able to parse remarks from the argMultiMap. If this was the first test case failure you looked at, AddCommandParser#parse still returns a new Remark("") as stated in the tutorial, which is incorrect.



**2. parse_optionalFieldsMissing_success()**

- AddCommandParser needs to support remark parsing (like the above). 



**3. parse_allFieldsPresent_success()**

- Update PersonBuilder and AddCommandParserTest#asserParseSuccess's _userInput_ fields.



**4. toModelType_typicalPersonsFile_success()**

- JsonAdaptedPerson.java detects that your remarks are null (because we haven't added them).

- update typicalPersonsAddressBook.json to include the "remark" json object field.

- There's also no remark in TypicalPersons.java (which should match typicalPersonAddressBook.java), so this cases the default remark in PersonBuilder to be used instead, giving us incorrect output.



**5. toModelType_duplicatePersons...**

- duplicatePersonAddressBook.json is missing a remark field. Add **the same** remark for both json objects in the file.



-> Fixing some of these errors caused others to spring up:

**6. execute_allFieldsSpecifiedUnfiltered**

- The EditCommand needs to allow editing remarks too.

- Update: EditCommand.java, EditPersonDescriptor.java, EditPersonDescriptorBuilder.java

**6.1 This causes the parseCommand_edit... test case to fail.**

- update EditCommandTest#getEditPersonDescriptorDetails to include remarks.



Hope this helps!
</panel>

</panel>
<panel type="info" header="### HO HOL YIN `@hoholyin` (1 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/88#issuecomment-533853425" expanded>

We can make use of the debugger in Intellij to 'Step in' the failing tests. 

After stepping through a few levels, we will realise that most of the failing tests are due to the fact in the file `CommandTestUtil.java`, we are missing:

1) `public static final String VALID_REMARK_AMY = "valid remark amy"`

2) `public static final String VALID_REMARK_BOB = "valid remark bob"` 

(These are as per the other fields required in building a `Person` object).



Adding these two final Strings and using them in the tests will allow most tests to pass as expected.



We also need to take note that these stub remarks will need to be consistent with the ones in the `TypicalPersonsAddressBook.json` for the test to pass since the test will compare between the constructed person and the person stored in the .json file.
</panel>

</panel>




<panel type="info" header="### ZHOU XINMING `@xinmingzh` (1 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/18#issuecomment-525108419" expanded>

Instead of editing the code, click on the "Wrapping and Braces" option in the bar directly above the code, then scroll down and look for "'switch' statement" and untick "Indent case branches". The change will be reflected in the sample code.
</panel>

</panel>
<panel type="info" header="### YEO TONG `@Cronyxx` (1 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-535902933" expanded>

Did you try removing the max height field from your DialogBox.fxml?
</panel>

</panel>


<panel type="info" header="### BRYAN LIM YAN JIE `@blimyj` (1 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/7#issuecomment-523297460" expanded>

I had a similar problem. 

For me, disabling the Maven plugin seemed to make the "Next" button reappear.



Also curious if this will have any repercussions later on in the project.
</panel>

</panel>





<panel type="info" header="### RUSSELL LOH CHUN FA `@Russell-Loh-NUS` (1 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/53#issuecomment-529396274" expanded>

Hi @nattanyz , I faced a similar issue as yours when I packaged my app. 



Basically, there are two things you can do:

1. Under Edit Configurations...(option is beside the hammer on the top right) > Application > Duke, change the "Use classpath of module:" to duke.main instead of main

2. Under File > Project Structure... > Modules, remove the main and test modules (as this should already be under 'duke > main' & 'duke > test')



You shouldn't need to remove the `package duke;` from your Duke.java file and the mainClassName on Gradle should be left as `duke.Duke`. Hope this helps.
</panel>

</panel>

<panel type="info" header="### MIN PYAE MOE `@minpyaemoe` (1 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/33#issuecomment-526888135" expanded>

I also have the same issue, and i did not change the mainClassName to Launcher class in gradle.build file. Are we supposed to change it to Launcher?
</panel>

</panel>




<panel type="info" header="### SHAWN CHEW `@shawnpunchew11` (1 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552178208" expanded>

@tuandingwei the cause of the error wasn't the test cases. I believe it was from either ASCIIDoctor or Coveralls as there is some dependency within the CI there. We tried commenting out asciidoctor or coveralls but both resulted in further errors because asciidoctor relies on coveralls do generate a html file that is required. we've gotten it to pass temporarily by commenting out our deploy segment within our gradle file but that affects our publication 
</panel>

</panel>



<panel type="info" header="### KENNETH FUNG CHEN YU `@kenneth-fung` (1 contributions)" expanded>
<panel header="**2 :fas-comment:**" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547270078" expanded>

> I understand files in my jar file is accessed via `getResource`. So how should i access files outside of my jar in this case?



Maybe try doing it the same way as storage? Storage creates a `data` folder in the same directory as the jar file.
</panel>

</panel>


































































































































































































































