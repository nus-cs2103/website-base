<panel type="info" header="### DANIEL WONG YONG SHEN `@dawo5010` (19 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/11#issuecomment-523836922" expanded>

I followed this tutorial:
https://git-scm.com/book/en/v2/Git-Basics-Tagging

tl;dr for you: `git push origin <tagname>` for a single tag, `git push origin --tags` to upload all tags not already present remotely.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/18#issuecomment-525108753" expanded>

Thanks! That fixed the formatting. Appreciate the help!
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/27#issuecomment-526141819" expanded>

Heyyo,

I had the same issue when trying to complete Level-7 as well, and I didn't want to make it such that the file had to pre-exist/be created by the user before using the program.

Here's some articles on stackoverflow that I referred to for this problem: [Create File if not exists](https://stackoverflow.com/questions/9620683/java-fileoutputstream-create-file-if-not-exists), [Create whole path automatically](https://stackoverflow.com/questions/2833853/create-whole-path-automatically-when-writing-to-a-new-file).

In short, use .getParentFile().mkdirs() on your file object to create the necessary directory, and use .createNewFile() to create the file itself. Hope that helps!
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/28#issuecomment-526235238" expanded>

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

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/45#issuecomment-528828866" expanded>

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

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/56#issuecomment-529920401" expanded>

Can you take a screenshot of the Modules tab?
</panel>

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/56#issuecomment-529923007" expanded>

Delete 'main' under the Modules tab by selecting it and clicking the '-' button above it. (don't touch the one under seedu.duke.duke)
That should fix it. 
</panel>

<panel header="8" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/56#issuecomment-529930327" expanded>

Awesome, don't forget to close the issue :)
</panel>

<panel header="9" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/57#issuecomment-529964886" expanded>

Right, that's something I'll keep in mind when thinking about the tP and it's implementation too, then. Thanks prof!
</panel>

<panel header="10" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/58#issuecomment-530004708" expanded>

See https://github.com/nus-cs2103-AY1920S1/forum/issues/54

Have you changed your shadowJar configuration to use Launcher as your main class instead?
</panel>

<panel header="11" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/58#issuecomment-530007120" expanded>

Yep, then try `./gradlew shadowJar` again and see if it works :)
</panel>

<panel header="12" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/58#issuecomment-530010311" expanded>

That looks like a print statement, so I dug through your code to find it. 

Your program uses the file /data/duke.txt relative to the directory that the jar file is launched. 
In your case, you likely launched the jar file from the `build` folder and since it didn't already have a data/duke.txt, that triggered the print statement in Line 46 of your Duke.java (according to [your latest commit here](https://github.com/ChangUo79/duke/blob/master/src/main/java/Duke.java)), hence printing 'File not found.'

</panel>

<panel header="13" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/62#issuecomment-530687428" expanded>

Can you push your branch-Level-10 in its current (broken) state to your repo so that it can be cloned? 
</panel>

<panel header="14" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/62#issuecomment-531097069" expanded>

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

<panel header="15" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/60#issuecomment-531124948" expanded>

Thought I’d break the silence - cloned your code 2 days ago but no dice for me either. Mine returns an exit code of 255 instead, however.

Have you made any progress/found any new leads?
</panel>

<panel header="16" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/134#issuecomment-542736815" expanded>

I think this is best illustrated with an example.

Let's say we have a while loop that can loop **up to** 100 times. 

For us to achieve a 100% statement coverage - we just need to test one iteration of the while loop. That executes all the statements within the while loop's code block - thereby achieving full statement coverage.

To achieve full path coverage, we have to test for every possible path - that means that we test the while loop for 1, 2, 3 ... 99, 100 iterations each time, to ensure that it produces the correct result each time. That's a far more comprehensive test, and only when all paths have been exhausted through testing can it be considered full path coverage. And definitely a lot more work to be done, testing-wise.

This applies to any form of conditionals or loops within a program - you'd have to test all possible number of iterations and/or all possible branches to ensure 100% path coverage, as compared to once for statement coverage.

Hope that illustrates it for you!
</panel>

<panel header="17" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/138#issuecomment-544228983" expanded>

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

<panel header="18" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/175#issuecomment-552260677" expanded>

Ah yes, I just checked this morning that it's now showing. It was probably browser caching. Thanks Prof!
</panel>

<panel header="19" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/174#issuecomment-552355054" expanded>

This seems to only occur on Preview. Open the PDF in Chrome's PDF reader, or Acrobat Reader DC, and links work fine.

Maybe the tutors and peers grading can note that they should not use Preview to open PDF files.
</panel>

</panel>
<panel type="info" header="### ERWIN CHAN GUO XIN `@ChangUo79` (13 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/8#issuecomment-523354848" expanded>

Understood and thank you prof for your reply.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/58#issuecomment-530006478" expanded>

do you mean changing the mainClassName to Launcher?
![image](https://user-images.githubusercontent.com/54112270/64630371-8fa0bd80-d427-11e9-9426-ccf5eb5bfb8c.png)

</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/58#issuecomment-530007872" expanded>

Its working now. Thanks! Do I need to be concern with this even though the jar is working:
![image](https://user-images.githubusercontent.com/54112270/64630609-0f2e8c80-d428-11e9-8372-7b5f20a6a42f.png)

</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/58#issuecomment-530190754" expanded>

Ahh missed that out. Thanks for the help!
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/67#issuecomment-531545407" expanded>

My concern was whether the pull request was done correctly as the master was merged into A-Assertions and A-CodeQuality shown in the picture.
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/67#issuecomment-531547827" expanded>

Understood! Thank you prof for the clarification 👍 
</panel>

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547052860" expanded>

> 
> 
> In the second case, `File imageFile = new File(IMAGE_DIRECTORY + value);` assumes that the given path starts from the project root directory (i.e. starting from `/main/...`). However, your image is actually stored in the resource folder, which is not the root level directory. The first case works because `getResourceAsStream` reads a file from `src/main/resources`.
> 
> You might want to consider letting your `IMAGE_DIRECTORY` = `src/main/resources/images/`. This will allow `new File(IMAGE_DIRECTORY + value)` to get the file from the root directory.

But what if the jar file isn't inside the project directory and moved to another directory with an `images` folder? For example, i moved the jar file to `Documents` and there is an `images` folder. How then would I retrieve the images? 
</panel>

<panel header="8" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547261903" expanded>

> Ah I see! I suspect your solution would work if the jar file is actually the case as you mentioned. However, if you are still running from your IDE, this method would break down since `new File(...)` will attempt to read from the root project directory.
> 
> Have you tried building the jar file and manually testing to see if it works?

i built the jar file with an `images` folder and the relevant images in the `Documents` directory but it doesn't seem to work.



</panel>

<panel header="9" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547262932" expanded>

> First, understand that files that are packaged in your jar file has to be accessed in a certain way (getResource). Files outside your jar can be accessed as usual.

I understand files in my jar file is accessed via `getResource`. So how should i access files outside of my jar in this case? 


</panel>

<panel header="10" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547431043" expanded>

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

<panel header="11" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547439804" expanded>

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

<panel header="12" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547781573" expanded>

Hello again! A new issue has arise after the previous issue was solved. Currently many of my test cases are failing due to this line ` photo = new Image("file://" + imageFile.toURI().getPath());` for some reason. From what I know, there is some initialization problem and there is trouble getting the images.

Some screenshots of the exceptions and errors:
![image](https://user-images.githubusercontent.com/54112270/67839179-0441cf80-fb2e-11e9-8cf3-b8d801012834.png)
![image](https://user-images.githubusercontent.com/54112270/67839256-2f2c2380-fb2e-11e9-857a-0291ceec1f17.png)

I tried looking for similar issue and came upon this: https://bugs.openjdk.java.net/browse/JDK-8093075 
The latest reply from the link says that this issue will not be fixed. Does anyone know any way around this problem? Greatly appreciate the help!
</panel>

<panel header="13" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547832689" expanded>

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
<panel type="info" header="### DANIEL TAN JUN XIAN `@CarbonGrid` (11 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/11#issuecomment-523878746" expanded>

You probably only need to understand the following:
git tag
git tag -d \<tagname\>
git tag -f \<tagname\>
git push --tags
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/14#issuecomment-524178167" expanded>

Noted.
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/22#issuecomment-525363191" expanded>

Noted.
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/24#issuecomment-526035794" expanded>

Noted.
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/34#issuecomment-526826514" expanded>

Are you running on JDK 11?
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/52#issuecomment-529124683" expanded>

Sorry for some confusion.
What I meant:
Obfuscation - transient fields where we alternatively provide a hash in place.
STL - Wrong usage. I forgot STL doesn't mean Standard Libraries.
Modification - writing additional data alongside with serialized data.
</panel>

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/52#issuecomment-529125295" expanded>

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

<panel header="8" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/52#issuecomment-529128044" expanded>

It's not explicitly shown but avoidance of custom written parser and serialization should reduce the possibilities of bugs, I think? Since standard libraries are battle-tested.

IMO, I'm currently thinking that using standard libraries instead of custom written code base improves:
- Reliability
- Maintainability
- Testability
- Portability
- Reusability

Not too sure if that kind of concept is true.
</panel>

<panel header="9" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/55#issuecomment-529921392" expanded>

Is your build.gradle application targeting Launcher?
</panel>

<panel header="10" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/55#issuecomment-529942898" expanded>

https://stackoverflow.com/questions/48396274/how-to-enable-assertions-in-the-gradle-run-task
</panel>

<panel header="11" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/55#issuecomment-529943240" expanded>

Lol didn't test if -ea works configured in VM options. I assumed it did.
</panel>

</panel>
<panel type="info" header="### GE SHUMING `@geshuming` (10 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/1#issuecomment-522250367" expanded>

Thank you for the response professor.

I just realised that you can apply lightweight tags to the same commit multiple times. I suppose I can then tag the increment before/after `A-Gradle` with `A-Gradle`, thus keeping the tags in the same order. 
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/41#issuecomment-527713431" expanded>

https://github.com/nus-cs2103-AY1920S1/duke/blob/master/tutorials/gradleTutorial.md#checkstyle

Follow the tutorial exactly and include this config into your build.gradle

```
checkstyle {
    toolVersion = '8.23'
}
```

If you don't have the above config, the default tool version won't work with the checkstyle xml provided

</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/64#issuecomment-531179659" expanded>

The problems is in the log :)

Lines 221 and 222
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/86#issuecomment-533248033" expanded>

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

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/86#issuecomment-533251574" expanded>

Nothing wrong with the above output, but the stack trace shows there might be a problem with your storage parsing. 

I'm just guessing it's untested behavior from saving an event task and loading it (somehow tries to load it as a deadline task). You can try clearing your savefile and see if your jar file opens without issue?
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547012702" expanded>

Have you checked if the `photo` is actually created, and that no errors were raised and dropped by the AddressBook?

I suspect that the URI does not actually translate into URL. Otherwise, I think it might be due to the lack of escape slashes in the string.
</panel>

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552066906" expanded>

You can try triggering a custom build on travis, and run `./gradlew asciidoctor --info` to see what could be causing the issue?
</panel>

<panel header="8" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552067286" expanded>

Under "more options", click on the "Trigger build" option and insert a custom yaml config to 

![image](https://user-images.githubusercontent.com/43642522/68523268-a19cc080-02f1-11ea-94ee-78ed46680304.png)

</panel>

<panel header="9" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/168#issuecomment-552164586" expanded>

For positioning in HTML, I modified the `asciidoctor.css` file in `/stylesheets` to align the imageblocks. 
[The commit I made can be found here](https://github.com/AY1920S1-CS2103T-W13-1/main/commit/1637f6f60f1423dd00a76585ec49ce15723ef91d) It was a small fix that didn't warrant installing applications/plugins, in my opinion. 

> it is currently not possible to do so for captions in HTML

My commit also aligns the caption, so for anyone wondering if you can, you can.
</panel>

<panel header="10" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/168#issuecomment-552166720" expanded>

> Edit: Didn't manage to get this to work for me though :(

I don't think it shows up in the preview on the IDE, but it shows up for my team's site as well as deployment previews
</panel>

</panel>
<panel type="info" header="### KHENG YAU DONG `@ChrisKheng` (10 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/16#issuecomment-524497027" expanded>

Alright thanks!
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-527309677" expanded>

Maybe it would be good to remove the duplicated module by going to project structure >> module, and remove the 'main' module which is duplicated, cuz the issue of duplicated modules has just caused problems for my code when trying to use some javafx methods.
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/53#issuecomment-529379489" expanded>

I think the main course behind the issue "could not find or load main class Duke" is because java cannot find the `.class` file of Duke to load it. When Duke was in the `package duke`, was the `mainClassName` in your gradle is `duke.Duke`? 
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/78#issuecomment-532497316" expanded>

Uhm what did you put for the `mainClassName` in your `build.gradle` file though? Is it `duke.Launcher`? If yes, did you put your `Launcher` class inside a package called `duke`?
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/78#issuecomment-532501232" expanded>

Hmm did you push your latest change to github? Maybe I can help to inspect the jar error
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/78#issuecomment-532501493" expanded>

By the way, did you use gradle to make the jar?
</panel>

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/88#issuecomment-533758439" expanded>

I faced similar issues as well and what I did is I first determine which test fails first and also why it fails (from the console which shows the assertions error). The most common problem I faced is the actual `Command` or `CommandResult` generated is **not equal** to the expected one. It's usually due to differences in some values, for example, the content of the `remark` in the `CommandResult`, which is usually because of putting different values for the field in where the expected result is generated and where the actual command is generated. (sometimes the result is generated from the data file)


I put a breakpoint at the relevant line before the assertion in the test method (which fails) and run the debugger and track the value of `Command` and/or `CommandResult` step by step, stepping into the relevant methods as necessary. I focus especially on the value(inner content) of `Command` or `CommandResult`, e.g. `name` and `address`. When I found out the point **where the difference in value occurred**, I will do some backtrack to find **where** the actual `Command` and/or `CommandResult` is generated to see what causes the differences in value and then fix it accordingly.


Hope this helps! 
</panel>

<panel header="8" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/106#issuecomment-536930492" expanded>

I think you can click on `releases` in the repo page of your team, then click on `new release`. You can then add a tag there which will tag the latest commit of your team repo.
<img width="747" alt="Screenshot 2019-10-01 at 4 32 51 PM" src="https://user-images.githubusercontent.com/42091735/65946677-401f4180-e469-11e9-94f5-980a309dd43c.png">

</panel>

<panel header="9" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/160#issuecomment-549132446" expanded>

Alright, thanks prof!
</panel>

<panel header="10" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/177#issuecomment-552430529" expanded>

Ok thanks prof!

</panel>

</panel>
<panel type="info" header="### JEONG YU HAN `@jeongyh99` (9 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/5#issuecomment-522397588" expanded>

Thank you!
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/6#issuecomment-522460553" expanded>

Thank you! I will try it out :)
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/19#issuecomment-525153733" expanded>

![Result](https://user-images.githubusercontent.com/50542926/63745189-26bc3000-c8d4-11e9-885a-306966e8c254.PNG)
![TestCase](https://user-images.githubusercontent.com/50542926/63745192-26bc3000-c8d4-11e9-8016-4631c1cf0729.PNG)
![iml file](https://user-images.githubusercontent.com/50542926/63745194-26bc3000-c8d4-11e9-8532-2af97de77bde.PNG)
![Directories](https://user-images.githubusercontent.com/50542926/63745213-30459800-c8d4-11e9-8543-aea7b41f4e46.PNG)

Attached are the relevant screenshots! Once again thank you :-)
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/19#issuecomment-525156962" expanded>

The icons when pressed are also unable to find the test cases.
Another method I tried but to do avail was by right clicking the methods in my code and generating each corresponding test method through IntelliJ, which also failed to detect my test cases.
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/19#issuecomment-525198034" expanded>

Thank you for the help! My directory used to look like that until i started introducing packages, I am still trying to figure out what the issue is with my structure. My Run Configuration looks fine, but I am probably missing out something. I feel like I am going nowhere on Google either. I would be grateful if someone could point me in the right direction. Thank you!

![image](https://user-images.githubusercontent.com/50542926/63754576-aef80080-c8e7-11e9-88b7-130262d75542.png)
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/19#issuecomment-525236488" expanded>

The issue has been resolved after the folders have been included. Thank you for the assistance 👍 
</panel>

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/49#issuecomment-528774332" expanded>

Thank you!
</panel>

<panel header="8" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/80#issuecomment-532701993" expanded>

Thank you
</panel>

<panel header="9" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/82#issuecomment-532702266" expanded>

Thank you for the clarification!
</panel>

</panel>
<panel type="info" header="### JEREMY TAN JIERUI `@Parcly-Taxel` (8 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/20#issuecomment-531510517" expanded>

_The Mythical Man-Month_ advises that if there is a software construct (or library you can use) that already provides the functionality you want, why bother reinventing the wheel? Vis-à-vis exceptions, this means eschewing writing extensions to exceptions.

In my iP as it has been recently released, there are no custom exceptions; the only exception used is `IllegalArgumentException`.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531510959" expanded>

That's the team project. You can pretty much ignore checkstyle for that; only the unit tests need to pass. (Changing the imports to please checkstyle would take too long.)
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/88#issuecomment-533763651" expanded>

The strange thing is, even after complaining about the test failures in the lecture, I managed to fix them with the IDE debugger, around nine hours before this announcement (see #87 and my branch's commits linked from there, e.g. [this](https://github.com/Parcly-Taxel/main/commit/8475c2f822eecf570a475af7250f18d313acd292)). Setting breakpoints in the code helped to show which test objects had not been updated to use the new remark syntax.
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/88#issuecomment-536283869" expanded>

When are you going to close this one?
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/106#issuecomment-537769952" expanded>

The way to push the tags to the team repo from the command line is as follows:

* one who has write access to the team repo does `git tag -a "v1.1" -m "v1.1"` (the `-m` option is just for completeness), then `git push` on said team repo
* all team members do the same steps as detailed in #99 to get the tag on their forks, except that the `--tags` option is added to both commands
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/114#issuecomment-539900988" expanded>

If you don't want to highlight and press R, this specific markup is achieved with `>` at the start of a line.
`>quoted text`
>_Right._

- [ ] Question: how do you create that keycap look? ![image](https://user-images.githubusercontent.com/54175463/66465407-61101400-eab3-11e9-9766-4827a4fdd646.png)


</panel>

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/161#issuecomment-549135468" expanded>

@damithc In any case, when can we mark them as closed?
</panel>

<panel header="8" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/161#issuecomment-549203407" expanded>

I heard that some things I wanted to do could not be done until 2020, what are they?
</panel>

</panel>
<panel type="info" header="### SAHIL S/O SANJEEV GATHANI `@Sahilgat` (8 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/39#issuecomment-527220007" expanded>

> Have you tried running gradle from the terminal?

Using the command "gradlew test" from the terminal results in the following output when run from the duke folder (C:\Users\nisga\OneDrive\Desktop\duke):
BUILD SUCCESSFUL in 990ms
3 actionable tasks: 3 up-to-date

Is this expected output or is there something else I am missing? Thanks for your quick response!
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/39#issuecomment-527222413" expanded>

> That appears to be fine.
> 
> You might want check if your project structure is in order because it seems to be a problem with your IDE config.

Is there a specific way to be checking this? As far as I understand project structure refers to the order of my files but when I select "Tests" from my project menue I am being directed to the correct folder so I believed my project structure is in order as shown in the screenshot below. Did you mean something else by project structure? Thanks again for your help!
![Capture](https://user-images.githubusercontent.com/38809578/64130454-f8b77e00-cdf4-11e9-8afc-d3274aaed1b3.PNG)

</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/39#issuecomment-527225137" expanded>

> I was referring to the `Project Structure...` feature in IntelliJ IDEA. Try this:
> 
> 1. Enter `gradlew cleanTest` in a terminal.
> 2. Try running your tests again from IntelliJ.

Thanks so much for your help! I think that indeed was the issue! I'll try moving the folders and restructuring the project accordingly. Also ran the gradlew cleanTest and output was: 

BUILD SUCCESSFUL in 896ms
1 actionable task: 1 executed

![Capture](https://user-images.githubusercontent.com/38809578/64130763-01a94f00-cdf7-11e9-8231-44f901e1eb00.PNG)

</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/39#issuecomment-527226595" expanded>

> Technically, that's not a problem. Gradle just recognized that there were no new changes and skipped testing. As a result, no results were reported to IntelliJ. By running `:cleanTest`, you basically forced Gradle to compile and run the tests again.

Yea I just realised taking a closer look that the folder structure doesn't seem to be an issue. However, I still get the "Test events were not recieved" original error even after running gradlew cleanTest and can't see the output of the tests passing as shown in the examples I've seen. Am I correct in assuming my tests work for now though and is there anything I need to change to get the same output as shown below? Or am I correct in assuming everything is fine and the result shown in the example below is because Gradle was not used?
![Capture](https://user-images.githubusercontent.com/38809578/64130968-3d90e400-cdf8-11e9-827a-8893254ee895.PNG)

</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/39#issuecomment-527232896" expanded>

> You can change the test runner to IntelliJ in the settings.
> ![image](https://user-images.githubusercontent.com/22460123/64131056-b7c16880-cdf8-11e9-864a-0dd381a8a636.png)

Ok thanks again for your help I think I more or less figured it out! One last question, when I swapped to IntelliJ IDEA and then selected "Add JUnit 5.* to classpath" under Test as per the instructions under Week 3, my test files now get errors highlighted and when I try to run all tests I get the error:
"No tests were found" and the popup "Tests were not found in module "test". Use module "main" instead" as shown in the screenshot below. When I switched back to Gradle the tests still ran fine. Is there any way to configure it such that I can switch between both easily? I suspect the adding JUnit to classpath was what caused the error as simply swapping to using IntelliJ in the settings did not cause the issue at first. Else it seems I'll stick to using Gradle though I want to understand what's happening here.
![Capture](https://user-images.githubusercontent.com/38809578/64131816-c3fbf480-cdfd-11e9-9687-cded4a55d510.PNG)

Edit: Even after switching back to Gradle in the settings, right-clicking and running all tests results in the errors shown above. Only when I run gradlew test from the command line does the test complete successfully.

</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/39#issuecomment-527385154" expanded>

> ![image](https://user-images.githubusercontent.com/22460123/64149629-f2f38400-ce58-11e9-9fff-8820f0b78e9f.png)
> You have two extra modules.

Thank you so much! I think all the issues are finally resolved :)
</panel>

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/41#issuecomment-527726402" expanded>

Yep silly mistake forgot to add the checkstyle config, thanks for your help!
</panel>

<panel header="8" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/64#issuecomment-531373133" expanded>

Thanks for your help, silly of me to miss that!
</panel>

</panel>
<panel type="info" header="### TAN YUANHONG `@le0tan` (7 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531530064" expanded>

> > That's the team project. You can pretty much ignore checkstyle for that; only the unit tests need to pass. (Changing the imports to please checkstyle would take too long.)
> 
> Not true :-) Following a consistent style is even more important for a team project.
> 
> @le0tan Are you able to pass the checkstyle check via gradle?

No =(
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531530097" expanded>

> @le0tan also post screenshots of the relevant parts of your IDEA code style settings.

![pic1](https://i.imgur.com/CyLuFNs.png)
![pic2](https://i.imgur.com/I4u7mfV.png)
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531533607" expanded>

> > No =(
> 
> That's odd. AB3 is passing the checkstyle check on Travis. Unless you changed the code, it should pass for you as well. BTW, perhaps you should set up IDE coding style for each project rather than change the default settings.
> 
> Let's wait to see if anyone else faces this problem. In the meantime, not use _optimize imports_ feature?

The thing is... I set IDEA to automatically organize the imports for every commit. So it messed up the import order of **EVERY** .java file in the project and there's no easy way of reverting it.

I didn't push this change to our team's repo so currently it's not a big problem. It only affects my "get familiar with AB3" tutorial branches.

This is the [branch](https://github.com/le0tan/main/tree/tutorial-adding-command) I pushed to.
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531533678" expanded>

Is it possible for someone whose IDEA properly optimizes imports to upload their `.idea` folder so that we can overwrite ours?
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531535544" expanded>

> I notice that your checkstyle.xml is blue (i.e. has been edited). Are you certain that you're using the checkstyle as-is from the repo?

I made sure it's exactly the same by copy-pasting the content from the AB3 repo =)
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531535778" expanded>

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

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/66#issuecomment-531538515" expanded>

> I think a diff of your CommandTestUtil class will tell you what's wrong.

Looks like IDEA would only optimize imports on changed files, and that was the reason why it didn't apply the new rules to all files. I right clicked on src folder and optimized every file inside and now it passed tests. Thanks!
</panel>

</panel>
<panel type="info" header="### EUGENE TEU CHU WEI `@EugeneTeu` (7 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/76#issuecomment-532312329" expanded>

Thanks prof! 
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/141#issuecomment-545354452" expanded>

yes. 

My output is this, ignoring ascii doctor warnings (which does not seem to have an effect on the tests): 
<img width="1336" alt="Screenshot 2019-10-23 at 5 24 15 PM" src="https://user-images.githubusercontent.com/43085751/67378582-0fd74880-f5ba-11e9-8153-a3cb5a01645e.png">

</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/141#issuecomment-545477846" expanded>

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

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/174#issuecomment-552272793" expanded>

> I checked a PPP from last year and it doesn't seem to have this problem 🤔
> ![image](https://user-images.githubusercontent.com/1673303/68554879-d16cd500-0465-11ea-9164-72e1c5ddf31e.png)

Attached is my friend's PPP after conversion to PDF. I have tried opening the link in chrome and using other pdf generation methods but still give me the same 404 result : 

![image](https://user-images.githubusercontent.com/43085751/68557344-899f7b00-0470-11ea-8bca-b0056c6cf396.png)

Very strange behaviour
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/174#issuecomment-552277320" expanded>

Did some digging, seems like this issue is limited to Mac users :/
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/174#issuecomment-552281206" expanded>

@damithc 
Strange, the link works when I sent the pdf to my windows / linux users, but Mac users face similar issues on their local files.  

I confirmed this result with a spare windows laptop I have lying around. 

So it seems like we would still be able to submit the pdf, just that Mac users will face a broken reposense link 
</panel>

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/174#issuecomment-552282310" expanded>

Ok. Changed the title of the pr to reflect this issue for Mac users! 
</panel>

</panel>
<panel type="info" header="### HONG SHAO YI `@shaoyi1997` (7 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/111#issuecomment-538287389" expanded>

Is your `Checkstyle version` in your settings set to **8.1**?

![image](https://user-images.githubusercontent.com/44439414/66190140-e9f70c00-e6bd-11e9-946b-217e3498ad46.png)

I looked through the release notes for Checkstyle and found that version 8.2 removed the `FileContentsHolder` module, which would explain the failure to instantiate the module and thereby, the exception thrown since Gradle uses version 8.1.

I changed my checkstyle version to 8.24 and received the same error that you received as well.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/133#issuecomment-541769120" expanded>

Hmmm, based on the Travis job log it seems like the build failure is not due to `constructor_missingFileUrl_throwsAssertionError()` and `constructor_invalidFileUrl_throwsAssertionError()` tests failures.

Rather, it's due to an `AssertionFailedError` in your `TutorialTest`, as seen below.

![image](https://user-images.githubusercontent.com/44439414/66765781-3670f180-eedf-11e9-80eb-4b6cc381b5a2.png)
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547050497" expanded>

In the second case, `File imageFile = new File(IMAGE_DIRECTORY + value);` assumes that the given path starts from the project root directory (i.e. starting from `main/...`). However, your image is actually stored in the resource folder, which is not the root level directory. The first case works because `getResourceAsStream` reads a file from `src/main/resources`.

You might want to consider letting your `IMAGE_DIRECTORY` = `src/main/resources/images/` for the time being, while still running in the IDE. This will allow `new File(IMAGE_DIRECTORY + value)` to get the file from the root directory.
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547058653" expanded>

> But what if the jar file isn't inside the project directory and moved to another directory with an `images` folder? For example, i moved the jar file to `Documents` and there is an `images` folder. How then would I retrieve the images?

Ah I see! I suspect your solution would work if the jar file is actually the case as you mentioned. However, if you are still running from your IDE, this method would break down since `new File(...)` will attempt to read from the root project directory.

Have you tried building the jar file and manually testing to see if it works?
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547293827" expanded>

> i built the jar file with an `images` folder and the relevant images in the `Documents` directory but it doesn't seem to work.

I examined your code further and realised that your `IMAGE_DIRECTORY` = `/images/` instead of `images/`. 
Placing a leading slash makes the path an absolute file path instead of a relative path, thus this references to `C:/images/` (assuming you're using Windows), instead of `C:/path/to/jar/folder/images/`.

In addition, `new Image(path)` requires `path` to start with `file://` in order to load the image through `ImageView`.

Hence, to sum up, you might want to try the following changes:

 - `IMAGE_DIRECTORY = images/`
- `new Image("file://" + imageFile.toURI().getPath())`

I've tried these changes on my end and it works through the jar file. Hope it works for you as well! :)
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547438984" expanded>

> Thank you so much! Definitely working now. Would this work with the IDE or only for jar files?

Glad to hear it works! 

It should be able to work in the IDE as well, provided you have an `images` folder in your root project directory i.e. `main/images/`. You can specify this folder in `.gitignore` so that it won't be pushed into the remote repo.

Additionally, note that your application does not automatically create an `images` folder in the root directory, so you might want to consider automatically creating this folder when your user launches the app to aid your user.
</panel>

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547815998" expanded>

Hi!

I suspect the bulk of these errors goes down to the failure to initialize `Photo`. More specifically, this RuntimeException: `java.lang.RuntimeException: Internal graphics not initialized yet`. 

In `Photo.java`, you are initializing `photo` with type `Image`, which is a JavaFX component that depends on the JavaFX toolkit. This adds dependency for the JavaFX library right from the lower level classes. Thus, in unit testing, the JavaFX toolkit is not set up since only classes that extend `Application` (or subclasses of these classes) will start up the toolkit but here, only `MainApp.java` extends `Application`. Hence, `Image photo` cannot be initialized.

Perhaps you can let the `Photo` class have an instance variable that contains the file path of the image file, then instantiate the `Image` within the `Ui` component using this file path!
</panel>

</panel>
<panel type="info" header="### KOH ZHENG QIANG SHAWN `@shawnkoh` (7 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/17#issuecomment-524898670" expanded>

What if we created the classes sporadically in prior commits? At which commit do we tag A-MoreOOP?
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/20#issuecomment-525246771" expanded>


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

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/21#issuecomment-525324241" expanded>

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

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/21#issuecomment-525344430" expanded>

Thanks for taking the time to explain ```git revert``` in detail Iskandar!

I'd like to add on a cautionary note about tags since we are on the note of reverting/reseting commits.

If you have pushed your tags to your remote repo with ```git push --tags``` reverting or deleting your commits will not remove your tags on the remote repo.

So how do we resolve this?

You may be tempted to use ```git tag --delete``` but this only deletes them locally.

Instead, you have to use ```git push origin :tagname```

Alternatively, you may also update your git tags locally, then ```git push --tags -f```

Please refer to this stackoverflow post for a more in depth discussion about removing tags on remote repos. https://stackoverflow.com/questions/5480258/how-to-delete-a-remote-tag
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/48#issuecomment-528712047" expanded>

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

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/47#issuecomment-528799510" expanded>

Thanks for the reply!
But I can't find the same setting on my version (IntelliJ Ultimate Mac 2019.2.1)
</panel>

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/47#issuecomment-528825245" expanded>

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
<panel type="info" header="### SHUI YAO `@shuiyao-sg` (7 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/55#issuecomment-529939611" expanded>

> Is your build.gradle application targeting Launcher?

If you are referring to the application{ } block in build.gradle, I think yes.

![09f7b0e0e439380b300878761d13f01](https://user-images.githubusercontent.com/46176136/64618683-4cd4ea80-d413-11e9-9b03-2e9fb2a36031.png)

</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/55#issuecomment-529948422" expanded>

> https://stackoverflow.com/questions/48396274/how-to-enable-assertions-in-the-gradle-run-task

It works! Thank you so much!
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-535910093" expanded>

> Did you try removing the max height field from your DialogBox.fxml?

I tried but it doesn't work.
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-535945960" expanded>

> Maybe you can try setting your VBox / Hbox (which ever u use to wrap your content) Min height/width to USE_PREF_SIZE via the SceneBuilder.

It does not work as well...Thanks anyways!
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-535946620" expanded>

> For the warning, refer to this issue: [nus-cs2103-AY1819S2/forum#30](https://github.com/nus-cs2103-AY1819S2/forum/issues/30)
> 
> As for JavaFX styling issues, in theory there should be no differences across platforms. However, weird quirks like this are not unheard of. If @junnbang's suggestion does not work, you can investigate using a listener to dynamically resize the dialog box to fit as a workaround.

I think my friend mistakenly ran the code from my master branch (with wrapText=false), where it should have been from branch-GUI. So it should not be a platform-related problem. So I guess there are some problem with my code...
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-536146626" expanded>

> What I did was that I changed from `Label` to the shape `Text` in both my `MainWindow.java` and `DialogBox.fxml` (changed in `DialogBox.fxml` using Scene Builder). I had read up a bit on online forums and it seems that `Label` does not adjust based on the size of your text (in this case, the tasks that Duke prints), so there was a recommendation to use `Text` shape instead. Let me know if this works!

It works! Thanks!
</panel>

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-536197282" expanded>

> Thanks everyone for the inputs
> @shuiyao-sg go ahead and close if the issue is resolved.

Thanks Prof!
</panel>

</panel>
<panel type="info" header="### WILLIAM RYAN KUSNADI `@WilliamRyank` (7 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/23#issuecomment-525602125" expanded>

but my test module has no dependencies on top, im not sure why, but i followed the tutorial.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/23#issuecomment-525642604" expanded>


![5](https://user-images.githubusercontent.com/50859694/63839417-77518d00-c9a9-11e9-82d6-94cbe605f444.PNG)
![6](https://user-images.githubusercontent.com/50859694/63839419-77ea2380-c9a9-11e9-9afa-8c136022b956.PNG)

Still cant user the class prof
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/23#issuecomment-528451772" expanded>

Hi prof yes, thank you
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/23#issuecomment-528451792" expanded>

J
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/54#issuecomment-529324357" expanded>

Hi @junnbang, thank you for the help, managed to solve it.
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/54#issuecomment-529328383" expanded>

Hi @damithc, yes i used his solution and it works now. Thanks.
</panel>

<panel header="7" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/93#issuecomment-535063993" expanded>

Okay prof, thanks for your suggestion. Yeah cause i do think there is a benefit in making such a feature, as our application will be used by hospital and people need to be careful and typically the user will want to double check if what they keyed in is correct. Will try to do both modes. Thanks prof!
</panel>

</panel>
<panel type="info" header="### JIN SHUYUAN `@CoderStellaJ` (6 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/3#issuecomment-522251416" expanded>

Yes, but in terms of the last step, do we need to set up the configuration again? I searched online and some people say need to add "External tools" for .bat
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/3#issuecomment-522297030" expanded>

Thanks a lot. I've found my problems.
**1. JNI error occurs during compilcation.**
My solution: This error may happen if you have changed your JDK version before. delete old JDK version and reopen duke project worked for me.
**2. If you have created multiple files for different classes.** Modified my .bat as follows
`javac  -cp ..\src -Xlint:none -d ..\bin ..\src\main\java\Task.java ..\src\main\java\Todo.java ..\src\main\java\Event.java ..\src\main\java\Deadline.java ..\src\main\java\DukeException.java ..\src\main\java\Duke.java`
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/78#issuecomment-532500142" expanded>

> Uhm what did you put for the `mainClassName` in your `build.gradle` file though? Is it `duke.Launcher`? If yes, did you put your `Launcher` class inside a package called `duke`?

Yes. I put Launcher inside package duke and change mainclass in build.gradle. And gradle run command is successful without any problem. This error occurs only when I run my jar file.
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/78#issuecomment-532580972" expanded>

> By the way, did you use gradle to make the jar?

Thanks a lot! I found the error. My fxml file path is wrong in the code and this causes the problem.
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/135#issuecomment-542999854" expanded>

Thanks for your contribution to this question. 
Because the quiz question asks whether the diagram shows the correct association role but the diagram shows association label. The diagram fails to show the role.
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/134#issuecomment-543000014" expanded>

Thanks a lot! It solves my confusion.
</panel>

</panel>
<panel type="info" header="### NEO WEIHONG `@whneo97` (6 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/12#issuecomment-523884104" expanded>

Hi prof, thank you fo the reply and assurance! Will it be possible to check if my current git username corresponds to the one submitted in the pre-lecture survey?
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/12#issuecomment-523886032" expanded>

Okay sure, yes should be the same, thank you prof for the clarification!
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/48#issuecomment-528764520" expanded>

> Update your fx:controller to duke.MainWindow (or whichever package it is located in)
> […](#)
> On 6 Sep 2019, at 1:16 PM, Neo Weihong ***@***.***> wrote: Hi, I have been following the JavaFx tutorials and up till Tutorial 3, I haven't experienced any issues. However, in tutorial 4, a ClassNotFoundException is thrown when loading MainWindow.fxml (called from Main class). The following screenshots contain the Main class and fxml code from the tutorial, my project directory and the exception stack trace. <https://user-images.githubusercontent.com/41929699/64402119-4a3a6400-d0a6-11e9-9793-91828cf384e6.png> <https://user-images.githubusercontent.com/41929699/64402120-4a3a6400-d0a6-11e9-975f-5d77ca11439f.png> <https://user-images.githubusercontent.com/41929699/64402121-4ad2fa80-d0a6-11e9-999a-c3171a503e66.png> <https://user-images.githubusercontent.com/41929699/64402122-4ad2fa80-d0a6-11e9-9367-e496fbcfb16d.png> My github repo currently contains my latest commits (with these exceptions): https://github.com/whneo97/duke <https://github.com/whneo97/duke> Anyone happens to be able to help advise on this exception? I'm currently using Mac OS 10.14.5 and I'm using Java 11.0.2 (as advised in #44 <#44> and have configured Intellij to use it) — You are receiving this because you are subscribed to this thread. Reply to this email directly, view it on GitHub <#48?email_source=notifications&email_token=AAU5MF47ATUK456IX2OPWWDQIHRR3A5CNFSM4IUFBIE2YY3PNVWWK3TUL52HS4DFUVEXG43VMWVGG33NNVSW45C7NFSM4HJW3AYA>, or mute the thread <https://github.com/notifications/unsubscribe-auth/AAU5MF6MZQGRIRILBBH7YM3QIHRR3ANCNFSM4IUFBIEQ>.

Thank you! This helped (replaced MainWindow with seedu.duke.MainWindow as according to my project directory structure)
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/48#issuecomment-528764916" expanded>

> Why you didn't use the template?
> 
> Taking screenshot is not a good practice as it is not copy-paste friendly.

Okay, will take note to use the template in the future, thanks for the advice!
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/161#issuecomment-549558894" expanded>

Hi prof @damithc , sorry just to double-check, will the following then be correct?

- We are not to close the issues we posted until Dec 9th (unless we intend to withdraw them.

- For the PED issues posted on our team repo, we may close the issue by the bot as soon as we have resolved the problems described (?). However, we are not to close the corresponding issues opened by the original author. (?)

- For PE issues, we are not to rectify or close the issues at all, be it by the bot or by the original author. (?)
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/161#issuecomment-549693247" expanded>

> > * We are not to close the issues we posted until Dec 9th (unless we intend to withdraw them.
> > * For the PED issues posted on our team repo, we may close the issue by the bot as soon as we have resolved the problems described (?). However, we are not to close the corresponding issues opened by the original author. (?)
> > * For PE issues, we are not to rectify or close the issues at all, be it by the bot or by the original author. (?)
> 
> Yes, that's correct. You are free to do anything with the PED issues posted on your team repo. We do not take them for grading.

Okay noted, thank you prof for the clarification!
</panel>

</panel>
<panel type="info" header="### LOW JUN KAI, SEAN `@seanlowjk` (6 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/30#issuecomment-526816381" expanded>

Ok thanks! :)
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/65#issuecomment-531473607" expanded>

Ok thank you Prof! 😄 
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/74#issuecomment-532016859" expanded>

Ok thank you for the answer Prof! 😄 
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/115#issuecomment-539069667" expanded>

Thanks for sharing this piece of information Yu Ting! 

</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/121#issuecomment-543012264" expanded>

Do change the url to: 

`https://coveralls.io/repos/github/YOUR_REPOS/badge.svg?branch=master&service=github`for the image. 

Do let me know if there are still problems with your coveralls not updating. 
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/179#issuecomment-554651774" expanded>

Ok thank you Prof! 👍 
</panel>

</panel>
<panel type="info" header="### THO WEN LONG, PAUL `@dragontho` (6 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/11#issuecomment-524172309" expanded>

Thanks all for the help!
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/79#issuecomment-532636960" expanded>

Also, how does one change labels of issues?
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/79#issuecomment-532641743" expanded>

To add on, it is not only the trivia part that fails, anything regarding storage is not working, including the already implemented .txt storage for tasklist as well.
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/79#issuecomment-532667715" expanded>

Oh sorry, I've found my own problem. It's because I did not implement my saving and loading properly from the beginning. Now I've fixed it. On another note, prof, would Gson be allowed for my iP?
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/79#issuecomment-532768264" expanded>

Alright thank you prof!
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/83#issuecomment-533410805" expanded>

Ok thanks prof!
</panel>

</panel>
<panel type="info" header="### SUDHARSHAN MADHAVAN `@uggi121` (6 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/9#issuecomment-523773496" expanded>

If I could opine in on this issue, I'd say both approaches have their pros and cons, which you've highlighted in the above comments. While Object-Level validations align with the essence of OOP, it could be a bit tedious to deal with similar cases in multiple objects. This will ultimately lead to a lot of redundant and repeated code.

A partial solution could be to handle common cases like white-space/empty inputs at the input-class level, leaving the object constructors to deal with more specific invalid inputs relevant to their associated objects.

To add on, we could abstract the input class at a higher level to a machine that accepts input. The machine has no idea what the valid input for other machines (objects) are. However, there are certain inputs that are invalid inputs for ALL objects. These can be handled at the input class level.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/11#issuecomment-523836959" expanded>

In the command-line, type : -
    **git ls-remote --tags origin**

You should see a list of pushed tags
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/49#issuecomment-528772706" expanded>

Implementing all the tasks under that sub-section seems tedious and unnecessary. A pragmatic approach would be to discuss with your team and individually implement non-overlapping features relevant to the tP
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/47#issuecomment-528778871" expanded>

File -> Settings -> Editor -> Code Style -> Java -> Continuation Indent = 8
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/146#issuecomment-546230816" expanded>

Thank you for the reply Prof. What about DeleteCommand? There is no `x` marked in the diagram, but I see no further use for it in the caller's code
</panel>

<panel header="6" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/146#issuecomment-546279659" expanded>

Thank you Master Damith
</panel>

</panel>
<panel type="info" header="### LIM HUI MIN `@huiminlim` (5 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/35#issuecomment-526935388" expanded>

Hi, thanks for help, works perfectly now!
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/137#issuecomment-543671754" expanded>

@damithc I think I resolved the problem, by removing a file with name " .\src\test\java\dream\fcard\util\data\Test.java " from my repo. Then, RepoSense produced a valid report after I removed this file with slashes in the name.

https://github.com/huiminlim/main/commit/c3215ba03a6d3d2c126d98f9b6c0b2376a3ffebc

I think that RepoSense does not accept files with slash in names.

Thank you and RepoSense dev team for the help anyway!
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552066329" expanded>

Hi Prof Damith, looks like this is the output i obtained on Windows 10, and no error is shown when I run both the gradle and just the task alone. Not sure if I did the correct way as you advised.

![image](https://user-images.githubusercontent.com/43434313/68523114-5aadcb80-02ef-11ea-9b28-c83dc176e3b0.png)


</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552066492" expanded>

We executed the same command on a mac

This is the complete task
![image](https://user-images.githubusercontent.com/43434313/68523159-ede70100-02ef-11ea-8111-8b24a55171ff.png)

This is the asciidoctor only task
 
![image](https://user-images.githubusercontent.com/43434313/68523162-fb03f000-02ef-11ea-92d8-6fc4f6acfbae.png)

</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552420328" expanded>

Thanks Prof, that works.
</panel>

</panel>
<panel type="info" header="### ISKANDAR ZULKARNAIEN B SUHAINI `@TheRealRavager` (5 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/9#issuecomment-523763674" expanded>

Let's look at the Todo object for example. We could do validation in two ways:

1. Validate input before passing it to the constructor (perhaps by having a method in `Duke.java` raise exception if `description` is blank).

2. Validate user input in Todo constructor (perhaps by raising exception if `this.description` is `null`)

I'm thinking of whether option 2 would be more appropriate, since it results in the Todo class being responsible for not allowing "invalid" Todo objects to exist, as opposed to having the main class handle it or creating a new class specifically to validate inputs.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/9#issuecomment-523882122" expanded>

Thanks for the response Sudharshan, really appreciate your contribution to the discussion.

About the input class, that makes a lot of sense. It just acts as a filter to remove inputs that are obviously gibberish or incomplete, while the respective objects deal with whether the input is "correct" (e.g. startTime < endTime).
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/11#issuecomment-523889772" expanded>

The difference between the two commands is that `git push --follow-tags` only pushes tags that are both annotated (similar idea to commit message) and reachable (in the current commit history).

Let's start with reachability. Imo it doesn't make sense to have a tag pointing to an unreachable commit (unless you, for some reason, want to keep a copy of it) and more importantly may confuse people.

As for annotations, they are there to give meaning to the tag you have created by giving a short summary of what the tag is for (e.g. what does "Level-6" of your project mean? What major change does it introduce?).

Hope this helped to clarify some of your doubts. I've only recently read up on tags so please correct me if I'm wrong. The Stack Overflow post links to [another](https://stackoverflow.com/questions/11514075/what-is-the-difference-between-an-annotated-and-unannotated-tag) post that explains annotated tags and their use cases quite well, I recommend giving it a read.
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/21#issuecomment-525341493" expanded>

Thanks Shawn, I believe your solution should quickly solve OP's issue. Lets take a moment to appreciate the difference between a revert and reset. [This](https://stackoverflow.com/questions/8358035/whats-the-difference-between-git-revert-checkout-and-reset) StackOverflow post should explain things pretty clearly.

TL:DR, a revert introduces another commit that basically undoes the reverted commit. A reset however, undoes changes by changing the commit history. 

An analogy would be as such: 
Imagine you were writing an essay and for every revision you would have a new copy (i.e. essay1.docx, essay2.docx, essay3.docx, essay4.docx). You mistakenly deleted your entire intro paragraph in essay3.docx and need to fix it. A revert would be to undo the deletion and save it as essay5.docx while a reset would be to delete everything from essay3.docx onwards and start from essay2.docx.

If you have the time to spare, I highly recommend [this](https://learngitbranching.js.org/) git tutorial. It gives really simple and elegant real-time visualisations of git branches as you perform commands, so you get a rough idea of whats happening to the commit history instead of it feeling like you're just playing with magical commands.

If anyone else has any tips regarding reverting/resetting please feel free to add on to the discussion
</panel>

<panel header="5" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/128#issuecomment-541397912" expanded>

Thanks Prof!
</panel>

</panel>
<panel type="info" header="### HON HAO CHEN `@honhaochen` (4 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/25#issuecomment-526042362" expanded>

Yeah, no problem doing that, and I have completed way beyond the other branches in the master branch then this problem pops out ._.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/25#issuecomment-526405540" expanded>

yeap, solved it. Thanks :D
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-527191712" expanded>

Hi, I have the same issue. Did you resolved it?
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-527263275" expanded>

Alright, thank you!
</panel>

</panel>
<panel type="info" header="### CHOW JIA YING `@C-likethis123` (4 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/17#issuecomment-525292376" expanded>

Okay, thanks everyone for your input!
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/31#issuecomment-526812056" expanded>

Noted, thank you for your reply.
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/33#issuecomment-526918210" expanded>

I managed to solve the issue by changing mainClassName to Launcher, and commenting out my main method in the Duke class. 

Thank you for your inputs!
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/107#issuecomment-536946018" expanded>

Noted. Thank you for your reply!
</panel>

</panel>
<panel type="info" header="### LAWNCE GOH JIA WEI `@lawncegoh` (4 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/45#issuecomment-528482772" expanded>

Hi Prof, 

This is the link my duke.java

https://github.com/lawncegoh/duke/blob/master/src/main/java/Duke.java
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/45#issuecomment-528715745" expanded>

https://github.com/lawncegoh/duke
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/139#issuecomment-544590028" expanded>

@damithc I ran it with this command and it worked and I was able to see the report, but not with the usual command. What are the files I am missing?
</panel>

<panel header="4" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/139#issuecomment-547196790" expanded>

If the above files are those we want to be considered, that means our group's reposense is fine right? Given the fact that we do not need to include any other types of files @damithc 
</panel>

</panel>
<panel type="info" header="### ELLIE YEE WEN NA `@Ellieyee` (3 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/102#issuecomment-536844782" expanded>

Fixed the issue by setting a new access token. Thanks for your help prof!
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/133#issuecomment-543559861" expanded>

yes! Thanks @shaoyi1997 :)
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/157#issuecomment-548310786" expanded>

commented out and tested. It seems to still be occurring but less frequent.
</panel>

</panel>
<panel type="info" header="### KENG JUN XIAN `@jxofficial` (3 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-527272635" expanded>

It was working completely fine yesterday. But when I opened IntelliJ again today, I experienced the same error. Any ideas why?

Edit: Solved. No idea how, I suddenly got the option to add to classPath .... when i pressed Alt + Enter 
I'm not exactly sure what happened.

</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-527313740" expanded>

Ah yes, something useful to know. 

I have no idea what the duplicated modules are doing. Don't even know what a module is O: Hopefully Prof can explain a little bit about classpath, duplicated modules, what gradle does behind the scenes etc.

Shall not mess with the structure for the time being, but its always good to know how to remove modules. 
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/60#issuecomment-531178068" expanded>

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
<panel type="info" header="### LUM WEI BOON `@lumwb` (3 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/10#issuecomment-523827170" expanded>

@damithc thanks prof!

Just to confirm, the setting was already checked before I received a notification from the CS2103T bot. Is there a way I can verify the bot has access the issues page of my repo?
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-526970032" expanded>

![image](https://user-images.githubusercontent.com/25117015/64085039-e987f000-cd62-11e9-9496-2f20dc2bc933.png)


Apologies, please find attached the image of my Duke class. 
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/37#issuecomment-527195416" expanded>

Yes. You could try following the steps for non-gradle, and adding the JavaFX references manually.
</panel>

</panel>
<panel type="info" header="### VOONG YU XUAN `@ambervoong` (3 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/33#issuecomment-526901026" expanded>

While I'm not sure if this will solve the specific problem, I did change mainClassName to Launcher and that made gradle run the application properly.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/88#issuecomment-534026305" expanded>

Along with the debugger, using _Go To -> Implementation_ is very useful to quickly view a method's code. In addition to the above, here are fixes for two other failing test cases. Hope it will be of use to someone. 

1. `parseCommand_remark()`
- In `AddressBookParserTest.java`, update `assertEquals(new RemarkCommand(INDEX_FIRST_PERSON, remark), command);` to make `remark` a Remark object instead of a String.

2. `parseCommand_add()`
- `AddCommandParser.java` only returns new Remark(""). As mentioned above, update the code and add a new method to parse remarks in `ParserUtil.java`.
- `PersonUtil.getAddCommand(person)` calls `getPersonDetails(Person person)` which extracts the Person's details. Update it to support remarks by adding `sb.append(PREFIX_REMARK + person.getRemark().value + “ “);`

</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/135#issuecomment-542742685" expanded>

Association roles are used to indicate the **role played by the classes** in the association. For example, in an association between classes A and B, class A could play the role of the husband and class B plays the role of the wife. 

Association labels are the ones shown in the diagram you linked. They **describe the meaning of the association**.  An easy way to distinguish between them is the black arrow present in association labels. Also, it often describes a relationship whereas association roles tend to be nouns like 'friend' or 'helper'!

This diagram is false because an association label is shown in the diagram, not an association role. I can't remember exactly but I think the question was asking if this was a valid association role! Otherwise, it is a perfectly valid association label.
</panel>

</panel>
<panel type="info" header="### TAN LIKAI `@tanlk99` (3 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/50#issuecomment-528900551" expanded>

Thanks for the suggestion! Do we have to credit it as stated in the [Policy on Reuse](https://nus-cs2103-ay1920s1.github.io/website/schedule/week4/project.html)?
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/143#issuecomment-546203225" expanded>

Yes, they can be used to update the diagrams. So we should store them in the docs/diagrams directory?
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/178#issuecomment-554644887" expanded>

Sorry, I did some responses on mobile while I was away from the computer.
</panel>

</panel>
<panel type="info" header="### JOLYN TAN SI QI `@jolynnn8D` (3 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/62#issuecomment-530680524" expanded>

Yep :( I still get the same error.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/62#issuecomment-530937198" expanded>

I've pushed it onto the repo!
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/62#issuecomment-531127685" expanded>

Fixed by deleting the wrapper folder, running gradle wrapper, then gradlew run
</panel>

</panel>
<panel type="info" header="### RAMACHANDRAN SANDHYA `@sandydays` (3 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/27#issuecomment-529116997" expanded>

Yes, it has been resolved! Thanks a lot for the help @dawo5010 and sorry for replying back to this a bit late!
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/75#issuecomment-532923893" expanded>

I see Prof, thanks for clarifying!
</panel>

<panel header="3" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-536137250" expanded>

What I did was that I changed from `Label` to the shape `Text` in both my `MainWindow.java` and `DialogBox.fxml` (changed in `DialogBox.fxml` using Scene Builder). I had read up a bit on online forums and it seems that `Label` does not adjust based on the size of your text (in this case, the tasks that Duke prints), so there was a recommendation to use `Text` shape instead. Let me know if this works! 
</panel>

</panel>
<panel type="info" header="### CHONG GUANG JUN `@tcgj` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/16#issuecomment-524396616" expanded>

Yup, basically the root directory is your main "duke" folder, which contains your .git directory, the src folder, and everything else.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/115#issuecomment-539075371" expanded>

Thanks for sharing!
</panel>

</panel>
<panel type="info" header="### TUAN DING WEI `@tuandingwei` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552096062" expanded>

Try checking your test cases. It could be that you might have failed one of the test cases.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/157#issuecomment-552096555" expanded>

Could it be because:

1. Certain execution takes some time to run?? i.e. code might not be efficient
2. getChildren() adds to the delay

If the delay is from the switch command, you might want to trace your code from the switch. 
If this happens when you start the app, this might mean that certain code is taking too long to run. 
</panel>

</panel>
<panel type="info" header="### CHOONG YONG XIN `@choongyx` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/36#issuecomment-526993256" expanded>

This is the link to my code: https://github.com/choongyx/duke/tree/branch-Level-10
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/36#issuecomment-526995416" expanded>

It works now, thank you!
</panel>

</panel>
<panel type="info" header="### LOONG JIAN HUNG, JOEL `@joloong` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/79#issuecomment-532646316" expanded>

It might be due to your savedPath and triviaPath. The relative paths to the .txt and .json files from duke.jar and Duke.java are not the same.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/110#issuecomment-537932048" expanded>

> The following question's answer is `False`. Why is Bot considered not keeping track of Mat class? Bot has Mat attribute.
> ![question](https://user-images.githubusercontent.com/25873970/66126467-0fcbd480-e61c-11e9-86c7-3e96fecab417.png)

For the first question, I believe it is because it is stated in the question to only refer to the

> **highlighted association in the code**



</panel>

</panel>
<panel type="info" header="### NING SHENGYING `@ning-sy210` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/86#issuecomment-533249842" expanded>

I wouldn't think it's an error with any of my java files in the project. Like I mentioned, the only thing that I did was creating a JAR file. I did no modifications whatsoever to the java files so I wouldn't think that the error lies there. Plus, when I sent the same JAR file to a friend of mine, he was able to run it without any problems. 

More specifically, I'm particularly concerned about these lines right here:
```
* What went wrong:
Execution failed for task ':run'.
> Process 'command 'C:\Program Files\Java\jdk-12.0.2\bin\java.exe'' finished with non-zero exit value 1
```

I could be wrong here but it seems something related to the jdk is wrong instead, and I don't know what it is.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/86#issuecomment-533254350" expanded>

Wow thanks, deleting the saved file worked! I figured out that there was an entry in the save file that was written incorrectly, which resulted in the parse error.
</panel>

</panel>
<panel type="info" header="### FUNG BRIAN PEI-EN `@briyanii` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/122#issuecomment-541327342" expanded>

Actually I found out why it was not saving.

It was because I had some text with < > around it and it was being removed.
The text including and after the first <something> was removed 
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/180#issuecomment-554663633" expanded>

Nevermind.
</panel>

</panel>
<panel type="info" header="### GABRIEL CHIA WENHAO `@gachia` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/21#issuecomment-525358488" expanded>

Thank you Shawn and Iskandar for the help and info! I did Shawn's quick solution and managed to get the Merge commit up. Nonetheless, I appreciate and have noted the information both of you have shared😊.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/28#issuecomment-526244831" expanded>

Thanks for the help! I managed to resolve it. Initially it didn't work even though I've set the system variable, so I had to restart my com and it worked afterwards.
</panel>

</panel>
<panel type="info" header="### BENEDICT PAK HONG JUN `@Nanosync` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/62#issuecomment-530502678" expanded>

Have you tried re-importing the gradle project by hitting the refresh button in the Gradle tab of IntelliJ?
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/64#issuecomment-531274087" expanded>

As @geshuming mentioned, those are the errors. To prevent such issues, you can try adding `*.iml` to `.gitignore` and remove the related files from the repository since they are generated by IntelliJ.
</panel>

</panel>
<panel type="info" header="### TAN JUN BANG `@junnbang` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/54#issuecomment-529295976" expanded>

Hello, I also ran into the same problem. For me, it was due to the mainClassName in build.gradle. After i changed it to "Launcher", then the error is gone.

> application {
    mainClassName = "Launcher"
}

Otherwise, check if you imported the javafx files into ur jar file before building it.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-535928582" expanded>

Maybe you can try setting your VBox / Hbox (which ever u use to wrap your content) Min height/width to USE_PREF_SIZE via the SceneBuilder.
</panel>

</panel>
<panel type="info" header="### LEOW WEN BIN `@LeowWB` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/92#issuecomment-535003632" expanded>

I see. Thank you for the quick reply, Prof!
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/145#issuecomment-545805340" expanded>

Got it, thanks for the quick reply, prof!
</panel>

</panel>
<panel type="info" header="### TSAI, HSIAO-HAN `@TSAI-HSIAO-HAN` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/43#issuecomment-527848157" expanded>

Error message
<img width="1225" alt="Screenshot 2019-09-04 at 6 46 22 PM" src="https://user-images.githubusercontent.com/46244796/64248703-7d64e200-cf44-11e9-9088-db19b7994a8d.png">

</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/43#issuecomment-528242548" expanded>

I solved this problem by right click the libs in Project Structure and add it in module manually.(Although I have other error after this, but that is related to jdk version)
</panel>

</panel>
<panel type="info" header="### KOH YI DA `@kohyida1997` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/154#issuecomment-547983932" expanded>

Hmm... I understand what you mean, Prof. My main intention in using call-backs at all was to avoid cylic dependency and high coupling between `AppManager` and `Timer`. 

Initially, my idea was to describe the structural relationship this way:

1. `AppManager` is aware of `Timer`. 
2. `Timer` however is not directly aware of `AppManager` (`Timer` is only aware of a method of `AppManager`).

However, I realise if I were to draw this out as a Class Diagram, I would have
1. A solid arrow from `AppManager` to `Timer`
2. A dotted-arrow (?) from `Timer` to `AppManager` as `Timer` is "dependent" on `AppManager`'s method.

This depiction would suggest a cyclic dependency between `AppManager` and `Timer` ... which is what I am attempting to avoid. 
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/154#issuecomment-548325881" expanded>

Ah, understood- yes Timer can compile without AppManager indeed! Thanks for the insight and reply, Prof!! 
</panel>

</panel>
<panel type="info" header="### LIM JUN HUP `@junhuplim` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/176#issuecomment-552286679" expanded>

Edited the question to be more informative! Yes I have pushed another commit to revert the changes.
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/176#issuecomment-552289013" expanded>

Resolved! It is the presence of the whitespace at line 2 and 6 of the commit 
[#243](https://github.com/AY1920S1-CS2103T-T12-3/main/commit/40587285f4fa59dc89cc59c6557d40b13185bb79)
</panel>

</panel>
<panel type="info" header="### TIU WEE HAN `@tiuweehan` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/168#issuecomment-552165243" expanded>

> For positioning in HTML, I modified the `asciidoctor.css` file in `/stylesheets` to align the imageblocks.
> [The commit I made can be found here](https://github.com/AY1920S1-CS2103T-W13-1/main/commit/1637f6f60f1423dd00a76585ec49ce15723ef91d) It was a small fix that didn't warrant installing applications/plugins, in my opinion.
> 
> > it is currently not possible to do so for captions in HTML
> 
> My commit also aligns the caption, so for anyone wondering if you can, you can.

This is even better!

Edit: Didn't manage to get this to work for me though :(
</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/168#issuecomment-552169273" expanded>

> > Edit: Didn't manage to get this to work for me though :(
> 
> I don't think it shows up in the preview on the IDE, but it shows up for my team's site as well as deployment previews

Oh you're right, I see it in my deployment previews now. But this method doesn't seem to work for exporting to pdf through IntelliJ though
</panel>

</panel>
<panel type="info" header="### MURUGESAN KARTHIKA `@kzrthikz` (2 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/56#issuecomment-529921947" expanded>

<img width="1440" alt="Screenshot 2019-09-10 at 8 56 14 PM" src="https://user-images.githubusercontent.com/50614346/64615647-90c4f100-d40d-11e9-9b96-bf7f1aa51228.png">
<img width="1067" alt="Screenshot 2019-09-10 at 8 56 41 PM" src="https://user-images.githubusercontent.com/50614346/64615665-9b7f8600-d40d-11e9-9f08-ea9e8a504efc.png">

</panel>

<panel header="2" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/56#issuecomment-529929372" expanded>

yes that fixed the problem! Thank you 
</panel>

</panel>
<panel type="info" header="### NG YONG KUAN `@SendorasLeft` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/20#issuecomment-531649927" expanded>

All the suggestions here have been great so far. Admittedly, my original examples were a little contrived for the sake of the discussion (if anyone was wondering, no, I definitely did not use an invalidTaskId custom exception). 

To sum up for any future readers, the general consensus seems to be that we first re-use any exceptions that's already defined in the Standard Java SDK (I would think that this applies even to third-party SDKs if there's a heavy reliance on them in the project), and if that is not sufficient for describing the exception, we extend our own from wherever is applicable/most-related. The aim is to make the Exceptions as understandable as possible to future programmers, and one clearest way of doing it is to use Exceptions that are already standardised among all programmers in the standard SDK.

My personal take on this issue so far has been to define a custom DukeException class with an overloaded constructor that takes in both an exceptionMessage as well as a Throwable cause (essentially, the original exception that caused it eg. IndexOutOfBoundsException). The DukeException wrapper around the the original exception makes it neater to deal with the way Duke handles most exceptions (by throwing the message to the user in some user-readable form eg. "You need to provide me with a task ID!" when no task ID is given). Chaining the exception with a DukeException also makes it clear that I as the programmer expected this specific error to occur and have attempted to handle it for the specific usage (instead of having a random IndexOutOfBoundsException occur, which is very clear in what was violated but not so much as to what it means for the specific functioning of the program ie. the cause-effect relationship). It's kind of a compromise, so to speak. 
Furthermore, in the rare cases when I need more specific information to handle the exception at a lower-level (which is unlikely at this stage, but you never know in the future), I can simply retrieve the root cause of the DukeException by calling getCause() on the DukeException or by performing a detailed stackTrace print.

Hope this is helpful. Since it's well into week 6, and this being a week 3 issue with satisfactory answers, I'll be closing the issue here. Do feel free to re-open this if you feel there are more points that merit discussion! Thanks to everyone who took their time to reply.
</panel>

</panel>
<panel type="info" header="### TEE HAO WEI `@thwnus` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/151#issuecomment-547524999" expanded>

Doesn't it [already](https://github.com/nus-cs2103-AY1920S1/addressbook-level3/blob/master/build.gradle#L13) [do so](https://github.com/nus-cs2103-AY1920S1/addressbook-level3/blob/master/build.gradle#L117-L144)?
</panel>

</panel>
<panel type="info" header="### ANG WEI HENG KENDRICK `@KendrickAng` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/88#issuecomment-533785777" expanded>

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
<panel type="info" header="### HO HOL YIN `@hoholyin` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/88#issuecomment-533853425" expanded>

We can make use of the debugger in Intellij to 'Step in' the failing tests. 
After stepping through a few levels, we will realise that most of the failing tests are due to the fact in the file `CommandTestUtil.java`, we are missing:
1) `public static final String VALID_REMARK_AMY = "valid remark amy"`
2) `public static final String VALID_REMARK_BOB = "valid remark bob"` 
(These are as per the other fields required in building a `Person` object).

Adding these two final Strings and using them in the tests will allow most tests to pass as expected.

We also need to take note that these stub remarks will need to be consistent with the ones in the `TypicalPersonsAddressBook.json` for the test to pass since the test will compare between the constructed person and the person stored in the .json file.
</panel>

</panel>
<panel type="info" header="### ZHANG XUAN `@zhangxuan97` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/130#issuecomment-541406069" expanded>

[GNU Lesser General Public Licence](http://www.jfree.org/lgpl.php)
</panel>

</panel>
<panel type="info" header="### LING ZHI WEI `@lzw12345` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/96#issuecomment-535518673" expanded>

Actually this is for my IP, is it still ok?
</panel>

</panel>
<panel type="info" header="### TAN YAN ZHEN, NATALIE `@nattanyz` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/53#issuecomment-529289072" expanded>

Hmm... seems like removing `package duke;` from Duke.java fixes this issue. Is this expected? Should Duke.java not be in the package? Furthermore, should the `mainClassName` in build.gradle be set to "Duke" or "duke.Duke"? Thanks!
</panel>

</panel>
<panel type="info" header="### ZHOU XINMING `@xinmingzh` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/18#issuecomment-525108419" expanded>

Instead of editing the code, click on the "Wrapping and Braces" option in the bar directly above the code, then scroll down and look for "'switch' statement" and untick "Indent case branches". The change will be reflected in the sample code.
</panel>

</panel>
<panel type="info" header="### YEO TONG `@Cronyxx` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/98#issuecomment-535902933" expanded>

Did you try removing the max height field from your DialogBox.fxml?
</panel>

</panel>
<panel type="info" header="### WANG RUNDING `@R-D-D-D` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/69#issuecomment-531756099" expanded>

It runs fine with java -jar command. I tried using java 11.0.2 instead but it does not change anything.
</panel>

</panel>
<panel type="info" header="### BRYAN LIM YAN JIE `@blimyj` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/7#issuecomment-523297460" expanded>

I had a similar problem. 
For me, disabling the Maven plugin seemed to make the "Next" button reappear.

Also curious if this will have any repercussions later on in the project.
</panel>

</panel>
<panel type="info" header="### FABIAN CHIA HUP PENG `@fabbbbbbyy` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/34#issuecomment-526829463" expanded>

I wasn't, so I switched it under Project Structure but I still got the same error.
</panel>

</panel>
<panel type="info" header="### LIM YONG SHEN, KEVIN `@lyskevin` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/127#issuecomment-541409708" expanded>

Ok thanks for the advice! I will look into other libraries first then.
</panel>

</panel>
<panel type="info" header="### TAN DE NING, KLEMENT `@klementtan` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/84#issuecomment-533453174" expanded>

Thank you prof!
</panel>

</panel>
<panel type="info" header="### POH JIA HAO `@limerencee` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/110#issuecomment-537962485" expanded>

Thank you for your replies, my doubts are cleared. :smile: 
</panel>

</panel>
<panel type="info" header="### RUSSELL LOH CHUN FA `@Russell-Loh-NUS` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/53#issuecomment-529396274" expanded>

Hi @nattanyz , I faced a similar issue as yours when I packaged my app. 

Basically, there are two things you can do:
1. Under Edit Configurations...(option is beside the hammer on the top right) > Application > Duke, change the "Use classpath of module:" to duke.main instead of main
2. Under File > Project Structure... > Modules, remove the main and test modules (as this should already be under 'duke > main' & 'duke > test')

You shouldn't need to remove the `package duke;` from your Duke.java file and the mainClassName on Gradle should be left as `duke.Duke`. Hope this helps.
</panel>

</panel>
<panel type="info" header="### LEE BO QIANG `@lightz96` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/2#issuecomment-522245929" expanded>

Ok, thanks Prof.
</panel>

</panel>
<panel type="info" header="### MIN PYAE MOE `@minpyaemoe` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/33#issuecomment-526888135" expanded>

I also have the same issue, and i did not change the mainClassName to Launcher class in gradle.build file. Are we supposed to change it to Launcher?
</panel>

</panel>
<panel type="info" header="### YEHEZKIEL RAYMUNDO THEODOROES `@Yehezkiel01` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/119#issuecomment-540214664" expanded>

Thank you very much
</panel>

</panel>
<panel type="info" header="### SEOW ZHI XIAN GABRIEL `@gabrielseow` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/170#issuecomment-552168179" expanded>

Sorry, I updated the links
</panel>

</panel>
<panel type="info" header="### JASMINE YEO JIA MIN `@jaesimin` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/138#issuecomment-544230106" expanded>

Thank you! It works already :)
</panel>

</panel>
<panel type="info" header="### ONG PANG YI MARCUS `@marqueurs404` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/95#issuecomment-535506285" expanded>

Thanks prof!
</panel>

</panel>
<panel type="info" header="### CHUA HUA LUN `@hua-lun` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/151#issuecomment-547537562" expanded>

oh right, I've missed it by accident. Thanks for the tip!
</panel>

</panel>
<panel type="info" header="### WEN SHUFA `@woon17` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/144#issuecomment-545720412" expanded>

Reference: 
https://deploy-preview-142--nus-cs2103-ay1920s1.netlify.com/images/GotoActivityDiagram.png
</panel>

</panel>
<panel type="info" header="### SONG TIANYI `@tysng` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/140#issuecomment-545887173" expanded>

Just to add on, you will need `git add` the files that you have fixed before running the above command again. Otherwise, you may see the same error thrown despite having fixed the problem. The reason is that `run-checks.sh` will call `git grep --cached` which searches in the staging area.
</panel>

</panel>
<panel type="info" header="### LEE LI YING IRENE `@irene-lly` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/71#issuecomment-531847842" expanded>

Okay I have finally managed to solve it by marking the "resources" directory (../src/main/resources) as a "Resources Root" in intellij.

![Screenshot (16)](https://user-images.githubusercontent.com/54141404/64974670-d8e98500-d8df-11e9-80d9-977d94f8708e.png)


</panel>

</panel>
<panel type="info" header="### SHAWN CHEW `@shawnpunchew11` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/167#issuecomment-552178208" expanded>

@tuandingwei the cause of the error wasn't the test cases. I believe it was from either ASCIIDoctor or Coveralls as there is some dependency within the CI there. We tried commenting out asciidoctor or coveralls but both resulted in further errors because asciidoctor relies on coveralls do generate a html file that is required. we've gotten it to pass temporarily by commenting out our deploy segment within our gradle file but that affects our publication 
</panel>

</panel>
<panel type="info" header="### CHEN ANQI `@anqichen9856` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/13#issuecomment-523883723" expanded>

@damithc I see. Thank you!
</panel>

</panel>
<panel type="info" header="### LIU XIAOYU `@xiaoyu-nus` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/42#issuecomment-527782298" expanded>

I have realised I have to install Gradle on Intellij on the starting page under config. Installing Gradle solved the problem.
</panel>

</panel>
<panel type="info" header="### YAP JIA AUN `@Joanna-YJA` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/163#issuecomment-550244854" expanded>

Apache License 2.0 is used.
</panel>

</panel>
<panel type="info" header="### KWONG CHUNG YUE JERRY `@jerryk1997` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/63#issuecomment-530287751" expanded>

Yes, thank you! I didn't see that sorry.
</panel>

</panel>
<panel type="info" header="### KENNETH FUNG CHEN YU `@kenneth-fung` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/150#issuecomment-547270078" expanded>

> I understand files in my jar file is accessed via `getResource`. So how should i access files outside of my jar in this case?

Maybe try doing it the same way as storage? Storage creates a `data` folder in the same directory as the jar file.
</panel>

</panel>
<panel type="info" header="### VEGI MANAS `@ManasVegi` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/32#issuecomment-526995671" expanded>

![Screenshot (19)](https://user-images.githubusercontent.com/53593482/64090042-ba31ad00-cd7b-11e9-963a-fb8f1870551e.png)

</panel>

</panel>
<panel type="info" header="### BALAM SAI ROHIT REDDY `@ROHITREDDYBALAM` (1 comments)" expanded>
<panel header="1" popup-url="https://github.com/nus-cs2103-AY1920S1/forum/issues/61#issuecomment-530434438" expanded>

My terminal was running on JDK 1.8 Prof when I compiled the program some time ago. But for creating the shadowJar, I had to update it to JDK 11. I think the error occurred due to the difference in JDK versions for compilation and creation of Jar. So I just compiled the program again (JDK 11). It is working now but I am not very sure if that was the problem. 😕 
</panel>

</panel>


























































































































































































































































