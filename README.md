# Red Hen Lab's Rapid Annotator
![image](https://user-images.githubusercontent.com/39674365/129453330-a1b1dd38-bd29-49e3-a651-61e1f01feb74.png)

# Contents
-   <a href="#introduction" class="post-section-overview">Introduction</a>
-   <a href="#built-with" class="post-section-overview">Built with</a>
-   <a href="#important-links" class="post-section-overview">Important links</a>
-   <a href="#terminologies" class="post-section-overview">Terminologies</a>
-   <a href="#issues-list" class="post-section-overview">Issues list</a>
-   <a href="#pull-requests-list" class="post-section-overview">Pull requests list</a>
-   <a href="#accomplished-tasks-list" class="post-section-overview">Accomplished tasks list</a>
    <!-- -   <a href="#week-01" class="post-section-overview">WEEK 01</a>
        <sup>07 Jun. - 14 Jun.</sup>
    -   <a href="#week-02" class="post-section-overview">WEEK 02</a>
        <sup>14 Jun. - 21 Jun.</sup>
    -   <a href="#week-03" class="post-section-overview">WEEK 03</a>
        <sup>21 Jun. - 28 Jun.</sup>
    -   <a href="#week-04" class="post-section-overview">WEEK 04</a>
        <sup>28 Jun. - 05 Jul.</sup>
    -   <a href="#week-05" class="post-section-overview">WEEK 05</a>
        <sup>05 Jul. - 12 Jul.</sup>
    -   <a href="#week-06" class="post-section-overview">WEEK 06</a>
        <sup>12 Jul. - 19 Jul.</sup>
    -   <a href="#week-07" class="post-section-overview">WEEK 07</a>
        <sup>19 Jul. - 26 Jul.</sup>
    -   <a href="#week-08" class="post-section-overview">WEEK 08</a>
        <sup>26 Jul. - 02 Aug.</sup>
    -   <a href="#week-09" class="post-section-overview">WEEK 09</a>
        <sup>02 Aug - 09 Aug.</sup>
    -   <a href="#week-10" class="post-section-overview">WEEK 10</a>
        <sup>09 Aug - 16 Aug.</sup> -->
-   <a href="#challenges" class="post-section-overview">Challenges</a>
------------------------------------------------------------------------
# Introduction
I have been continuing working on Red Hen Lab's Rapid Annotator after work done by Gulshan Kumar and Vaibhav Gubta at GSoC's 20, 19 and 18.  
Red Hen’s Rapid Annotator provides a platform to users to annotate large chunks of data in a short span of time and with least possible efforts. It provides the features of annotating images/videos/audios/text during collaborative situation also. With Red Hen Lab’s we will try to enable users to visualize the progress of each annotator separately and annotators can notify experimenter when the annotation is finished to make the annotation work more efficient.  
In Red Hen Lab’s Rapid Annotator we try to enable researchers worldwide to annotate large chunks of data in a very short period of time with least effort possible and try to get started with minimal training. 
 
------------------------------------------------------------------------
# Built with
- Python [Flask]
- Javascript
- HTML
- CSS
------------------------------------------------------------------------
# Important links

-   [Blog Series Link](https://rrrokhtar.hashnode.dev/series/gsoc-21-redhenlab)
-   [RA Organization Repo Link](https://github.com/RedHenLab/RapidAnnotator-2.0/)
-   [RA Forked Repo Link](https://github.com/rrrokhtar/RapidAnnotator-2.0/)
-   [Multichoice feature branch](https://github.com/rrrokhtar/RapidAnnotator-2.0/tree/multichoice-feature)
-   [Annotations adds-on branch](https://github.com/rrrokhtar/RapidAnnotator-2.0/tree/VIA-integration)

------------------------------------------------------------------------

# Terminologies

-   **RA** stands for Rapid Annotator
-   **VIA** stands for [Vgg Images
    Annotator](https://www.robots.ox.ac.uk/~vgg/software/via/)

------------------------------------------------------------------------

# Issues list

1.  [Going to 'Settings' of a new experiment leads to an Internal Server
    Error](https://github.com/RedHenLab/RapidAnnotator-2.0/issues/45)
    <details>  

    ### Description

    When I go to a new experiment and click on its settings immediately
    without making any uploads to this experiment (empty experiment) it
    leads to unexpected behavior;  
    ***"UnboundLocalError: local variable 'pngImageB64String' referenced
    before assignment"***  
    The logs and screenshot describes it more. It gets Internal Server
    Error in production mode, and in debug mode it is as follows.

    ### Screenshot

    [![EmptyExp](https://user-images.githubusercontent.com/39674365/119835501-2d406700-bf01-11eb-93c4-3178f088ad9e.gif)](https://user-images.githubusercontent.com/39674365/119835501-2d406700-bf01-11eb-93c4-3178f088ad9e.gif)

    ### Logs

    [![image](https://user-images.githubusercontent.com/39674365/119835842-7db7c480-bf01-11eb-9819-990307698f88.png)](https://user-images.githubusercontent.com/39674365/119835842-7db7c480-bf01-11eb-9819-990307698f88.png)

 </details>  
 
------------------------------------------------------------------------
2.  [Unexpected behavior when adding or removing annotators at an
    experiment](https://github.com/RedHenLab/RapidAnnotator-2.0/issues/47)
    <details>  

    ### Description

    When adding/removing annotators to an experiment in a some quick way
    (I did that just for testing the functionality but I found that), it
    leads to adding the same user twice sometimes which is not logical. Is
    it alright or not very important to look for fixing it?

    ### Screenshots

    #### 1 The behavior when using delete and add annotator functionalities.

    [![Non-logical behavior when using delete and add annotator
    ](https://user-images.githubusercontent.com/39674365/120403695-ffb24e00-c344-11eb-9ee0-adcbac36a056.gif)](https://user-images.githubusercontent.com/39674365/120403695-ffb24e00-c344-11eb-9ee0-adcbac36a056.gif)

    ### 2 The delayed delete

    [![Delayed
    delete](https://user-images.githubusercontent.com/39674365/120403756-240e2a80-c345-11eb-95bc-54865d5a0c40.gif)](https://user-images.githubusercontent.com/39674365/120403756-240e2a80-c345-11eb-95bc-54865d5a0c40.gif)
   </details>  
   
  ------------------------------------------------------------------------
3.  [Export results to sheet as CSV doesn't
    work](https://github.com/RedHenLab/RapidAnnotator-2.0/issues/50)
    
    <details>   
  
    ### Description

    Export results to sheet of an experiment works only as ".xlsx" files
    and "csv" doesn't work, it leads to unexpected behavior  
    **"UnboundLocalError: local variable 'app' referenced before
    assignment"**, screenshot attached below shows that.  
    I found that due to missing import as I discovered **I will submit a
    pull request to solve that.**

    ### Screenshots

    [![export
    csv](https://user-images.githubusercontent.com/39674365/122206067-3f2e7d80-cea1-11eb-9633-49bfd4005a5e.gif)](https://user-images.githubusercontent.com/39674365/122206067-3f2e7d80-cea1-11eb-9633-49bfd4005a5e.gif)
   
   </details>  
    
------------------------------------------------------------------------
4.  [View large experiments and results viewing take very long
    time](https://github.com/RedHenLab/RapidAnnotator-2.0/issues/51)
    <details>   

    ### Description

    Currently the loading time of viewing a large experiment is very big
    as Dr. Peter mentioned to me and Gulshan, I have reviewed the code
    base and found an issue in the pagination behavior it takes
    processing time for the whole data, while it is expected to be done
    only on the portion of data which will be displayed to the user as
    per page request. So I will work on that to optimize that time and
    make lazy-loading instead of the current.
    </details>   

------------------------------------------------------------------------

# Pull requests list

1.  [Fixed view settings bug of a new/empty
    experiment](https://github.com/RedHenLab/RapidAnnotator-2.0/pull/46)
    <details>   

    ### Description

    This pull request solves the [issue of viewing settings of a new
    experiment](https://github.com/RedHenLab/RapidAnnotator-2.0/issues/45)

    ### Screenshot

    [![FixedFirstBug](https://user-images.githubusercontent.com/39674365/119851484-b742fc80-bf0e-11eb-8648-7945bfb145a0.gif)](https://user-images.githubusercontent.com/39674365/119851484-b742fc80-bf0e-11eb-8648-7945bfb145a0.gif)
 </details>  
 
------------------------------------------------------------------------

2.  [Fixed adding/removing annotators
    bug](https://github.com/RedHenLab/RapidAnnotator-2.0/pull/48)
    <details>   

    ### Description

    This pull requests solves this issue [Unexpected behavior when
    adding or removing annotators at an experiment
    #47](https://github.com/RedHenLab/RapidAnnotator-2.0/issues/47)  
    It is a simple solution as I found the location reloading in
    unnecessary and making the unexpected behavior because immediate
    reloading makes the code in an inconsistent state and I didn't get
    what is their purpose so commenting them fixed that issue.

    ### Screenshots

    #### 1. Firefox is working right now

    [![Firefox fixed
    bug](https://user-images.githubusercontent.com/39674365/120560475-11f2c180-c403-11eb-9415-0e9f6a7a6a38.gif)](https://user-images.githubusercontent.com/39674365/120560475-11f2c180-c403-11eb-9415-0e9f6a7a6a38.gif)

    #### 2. Making quick adding is working correctly as well as removing, everything is fine. (this on Google Chrome)

    [![Unexpected behavior on adding
    annotators](https://user-images.githubusercontent.com/39674365/120560574-3babe880-c403-11eb-8604-6f10ac9db236.gif)](https://user-images.githubusercontent.com/39674365/120560574-3babe880-c403-11eb-8604-6f10ac9db236.gif)
 </details>  
 
------------------------------------------------------------------------

3.  [Fixed no progress alert showing when removing all
    annotators](https://github.com/RedHenLab/RapidAnnotator-2.0/pull/49)
    <details>   

    This pull request is a complementary to the latest pull request
    which is merged I discovered there is a problem when removing all
    annotators, the alert was causing some problems so I have solved
    it.  
 </details>  
 
------------------------------------------------------------------------

4.  [Fixed export results to csv
    issue](https://github.com/RedHenLab/RapidAnnotator-2.0/pull/52)
    <details>   

    ### Description

    This pull request solves [Export results to sheet as CSV doesn't
    work #50](https://github.com/RedHenLab/RapidAnnotator-2.0/issues/50)

    ### Screenshot

    [![csv\_works](https://user-images.githubusercontent.com/39674365/122212466-2a091d00-cea8-11eb-9d06-a92c66d0b3d3.gif)](https://user-images.githubusercontent.com/39674365/122212466-2a091d00-cea8-11eb-9d06-a92c66d0b3d3.gif)

</details>  
 
------------------------------------------------------------------------

5.  [Fixed loading time of viewing an experiment
    issue](https://github.com/RedHenLab/RapidAnnotator-2.0/pull/53)
    <details>   

    ### Description

    This pull request solves [View large experiments and results viewing
    take very long time
    #51](https://github.com/RedHenLab/RapidAnnotator-2.0/issues/51)  

    ### Screenshot

    Left side is after being fixed, right side is before.

    [![Fixedloadingtime](https://user-images.githubusercontent.com/39674365/122272264-acadce80-cee0-11eb-9416-301fc61bc169.gif)](https://user-images.githubusercontent.com/39674365/122272264-acadce80-cee0-11eb-9416-301fc61bc169.gif)

</details>  
 
------------------------------------------------------------------------

6.  [Video Snippet Annotated column added to results exporting at
    concordance
    experiments](https://github.com/RedHenLab/RapidAnnotator-2.0/pull/54)
    <details>   

    ### Description

    Added a new column to the concordance experiments exporting results
    "Video Snippet Annotated" which is simply the same as Video Snippet
    but with start and end modified based on the experiment's display
    time \[before\_time and after\_time\]  
    By applying the following equations

    > new\_start = video\_snippet\_start -
    > exp.display\_caption.before\_time  
    > new\_end = video\_snippet\_end + exp.display\_caption.after\_time

    and replacing those with the existing on the video snippet using
    regular expression.

    ### Screenshot of an experiment

    [![VideoAnnotatedSnippet](https://user-images.githubusercontent.com/39674365/123850843-ca385a80-d91a-11eb-91ee-f7e5bf5b02bb.gif)](https://user-images.githubusercontent.com/39674365/123850843-ca385a80-d91a-11eb-91ee-f7e5bf5b02bb.gif)

</details>  
 
------------------------------------------------------------------------

7.  [View results filtered by annotation level and labels
    feature](https://github.com/RedHenLab/RapidAnnotator-2.0/pull/55)
    <details>   

    ## Description

    Added new two select boxes to allow viewing results filtered by
    annotation level and annotation level's labels.

    ## Screenshot

    [![Filtering by annotation level and
    label](https://user-images.githubusercontent.com/39674365/123954005-2bf2d600-d9a8-11eb-9b41-20f4b0f87b46.gif)](https://user-images.githubusercontent.com/39674365/123954005-2bf2d600-d9a8-11eb-9b41-20f4b0f87b46.gif)

</details>  
 
------------------------------------------------------------------------

8.  [Reordering the annotation levels in a more easier way and more
    efficent](https://github.com/RedHenLab/RapidAnnotator-2.0/pull/56)
    <details>   

    ### Description

    Making the reordering of current existing annotation levels was a
    hard and need to open each annotation level to check what number is
    given for that and then keep all of them in your mind to make a new
    level or just change an existing annotation level 's level number so
    In this pull request proposing an easier way to do that as explained
    in the following screenshot.

    ### Screenshot

    [![AnnotationLevelsReorder](https://user-images.githubusercontent.com/39674365/125202862-ed95ca80-e275-11eb-8dc8-7bd99898471b.gif)](https://user-images.githubusercontent.com/39674365/125202862-ed95ca80-e275-11eb-8dc8-7bd99898471b.gif)

</details>  
 
------------------------------------------------------------------------

9.  [Multichoice feature branch merging to master
    branch](https://github.com/RedHenLab/RapidAnnotator-2.0/pull/57)
    <details>   

    ### The following features are added from multi-choice feature branch

    1.  Allowing multi-choice annotation levels. i.e. (select multiple
        labels for same annotation level and add a field for each label
        as other text i.e. commenting on each selected label from the
        annotator)

    Multichoice annotation process and viewing results  
    [![multichoiceannotation](https://user-images.githubusercontent.com/39674365/125206571-49694f00-e288-11eb-9794-39d80957f76d.gif)](https://user-images.githubusercontent.com/39674365/125206571-49694f00-e288-11eb-9794-39d80957f76d.gif)

    Adding a new level  
    [![AddnewLevel](https://user-images.githubusercontent.com/39674365/125206566-4706f500-e288-11eb-9908-956e7436360a.gif)](https://user-images.githubusercontent.com/39674365/125206566-4706f500-e288-11eb-9908-956e7436360a.gif)

    1.  Export results at long-format (New exporting results format)  
        [![Longformat](https://user-images.githubusercontent.com/39674365/125206477-d233bb00-e287-11eb-9871-00d0c80c16c4.gif)](https://user-images.githubusercontent.com/39674365/125206477-d233bb00-e287-11eb-9871-00d0c80c16c4.gif)

    2.  Export results at wide-format (New exporting results format)  
        [![Wideformat](https://user-images.githubusercontent.com/39674365/125206461-b6c8b000-e287-11eb-9802-809630f0379e.gif)](https://user-images.githubusercontent.com/39674365/125206461-b6c8b000-e287-11eb-9802-809630f0379e.gif)

    3.  Optimized the existing exporting results time

    *This pull request contains database changes and new added package
    to apply them you need that*

        # to install flask-migrate package
        pip3 install -r requirements.txt
        # Initialize the flask-migrate files.
        flask db init
        # Make a migration, it is like commit it and a comment beside.
        flask db migrate -m "Initial migration." # OR just add your comment right there  
        # Then apply your migration to the database, it is like push.
        flask db upgrade  

</details>  
 
------------------------------------------------------------------------

10. [Continue a specific experiment using exported wide results format
    feature](https://github.com/RedHenLab/RapidAnnotator-2.0/pull/57)
    
    <details>  

    ### Description

    To allow experimenter modifying the results exported file (at wide
    format) and continue from the point they have edited their results
    to a new experiment. for example removing a row from the sheet
    (file)

    #### So the following changes has been needed to be added to wide format results export

    1.  Added all attributes of file (file name, content, concordance
        line number; for concordance experiments and edge link and rest
        of them)
    2.  Merged the concordance file data to the exported results wide
        format file (in case of it is a concordance uploaded type)

    #### So to continue an experiment you need to

    1.  Specify which experiment to continue (select box based on your
        experiments)
    2.  Upload the exported results in wide format
    3.  Give it a new name (default: Copy of \[old experiment name\]
        \[id\])
    4.  Give it a description (default: "")  
        [![image](https://user-images.githubusercontent.com/39674365/125834745-09d723ff-49b8-4846-9d73-32a08a51cb63.png)](https://user-images.githubusercontent.com/39674365/125834745-09d723ff-49b8-4846-9d73-32a08a51cb63.png)

    #### Effects are same as creating a new experiment based on the old experiment results file

    ### Screenshots

    1.  Copy of image experiment  
        [![New copy of an
        experiment](https://user-images.githubusercontent.com/39674365/125834626-5700530f-1a48-4393-85ce-0bc312f3bff1.gif)](https://user-images.githubusercontent.com/39674365/125834626-5700530f-1a48-4393-85ce-0bc312f3bff1.gif)

    2.Concordance experiment (it creates a new concordance file based on
    the given results file)  
    [![Copy of
    concordance](https://user-images.githubusercontent.com/39674365/125834530-5329f257-22f1-4e39-a737-72b476802a7b.gif)](https://user-images.githubusercontent.com/39674365/125834530-5329f257-22f1-4e39-a737-72b476802a7b.gif)

    3\. Text experiment  
    [![Text
    Experiment](https://user-images.githubusercontent.com/39674365/125834509-56e2f040-45cc-411c-99de-4fc5bf3be1ec.gif)](https://user-images.githubusercontent.com/39674365/125834509-56e2f040-45cc-411c-99de-4fc5bf3be1ec.gif)

</details>  

------------------------------------------------------------------------

11. [New feature added and modifications on exporting results and
    solving view results with no annotators
    issue](https://github.com/RedHenLab/RapidAnnotator-2.0/pull/59)
    <details>  
    
    #### 1. Solves the problem of viewing results of an experiment while it has no annotators

    > this due to the hard coded id sent when len(annotators) = 0 at
    > line 73
    > <a href="https://hashnode.com/@RapidAnnotator" class="user-mention">@RapidAnnotator</a>-2.0/rapidannotator/modules/add\_experiment/<a href="http://views.py" class="autolinkedURL autolinkedURL-url">views.py</a>

    #### Before

    [![NotcorrectViewResults](https://user-images.githubusercontent.com/39674365/128640470-dfa621c6-3d92-4662-8562-c90f88b779ef.gif)](https://user-images.githubusercontent.com/39674365/128640470-dfa621c6-3d92-4662-8562-c90f88b779ef.gif)

    #### After

    [![AfterBeingFixed](https://user-images.githubusercontent.com/39674365/128641883-a46a1dc9-ef6c-457c-baa8-65c98bbb755b.gif)](https://user-images.githubusercontent.com/39674365/128641883-a46a1dc9-ef6c-457c-baa8-65c98bbb755b.gif)

    #### 2. Allowing experiment's order to be modified between normal and random

    > [![changeorder](https://user-images.githubusercontent.com/39674365/128642586-0fcffabd-9a3c-4ecb-b891-558ec3753213.gif)](https://user-images.githubusercontent.com/39674365/128642586-0fcffabd-9a3c-4ecb-b891-558ec3753213.gif)

    #### 3. Disabled uploading once the experiment has already a done uploaded concordance file

    [![newconcordanceupload](https://user-images.githubusercontent.com/39674365/128645055-b07a9cac-1d27-4c45-88a2-700fad3877bd.gif)](https://user-images.githubusercontent.com/39674365/128645055-b07a9cac-1d27-4c45-88a2-700fad3877bd.gif)

    #### 4. Exporting results of concordance at wide format will be only contains the edge link if it is new scape type

    [![newscapecheck](https://user-images.githubusercontent.com/39674365/128646843-be8ad70f-9d7f-4655-9142-31de57aa0900.gif)](https://user-images.githubusercontent.com/39674365/128646843-be8ad70f-9d7f-4655-9142-31de57aa0900.gif)

</details>  

------------------------------------------------------------------------

12. [Annotations adds-on (coordinates
    feature)](https://github.com/RedHenLab/RapidAnnotator-2.0/pull/60)
    
    <details>  
    
    ### Description

    The following pull request adding is an adds-on to the current
    annotation process system to allow the experiment get more
    information about the data and use them with their process of
    information and features extraction and get more intuition about
    which part of the data is meant for this annotation

    ### Usage

    This feature meant to be used by the experimenter in the step of
    modeling and preprocessing.

    ### Screenshots

    1.  **Image experiments**
        [VIA](https://www.robots.ox.ac.uk/~vgg/software/via/) Vgg images
        annotators, I have integrated the images part to Rapid
        annotator  
        [![image-via-adds-on](https://camo.githubusercontent.com/82596babb140e88149afc6db5e9edf1bddf9c9fb20b87c768d05bfa4411e9e6a/68747470733a2f2f63646e2e686173686e6f64652e636f6d2f7265732f686173686e6f64652f696d6167652f75706c6f61642f76313632383730373732393636362f553131354c6c30644b2e6769663f)](https://camo.githubusercontent.com/82596babb140e88149afc6db5e9edf1bddf9c9fb20b87c768d05bfa4411e9e6a/68747470733a2f2f63646e2e686173686e6f64652e636f6d2f7265732f686173686e6f64652f696d6167652f75706c6f61642f76313632383730373732393636362f553131354c6c30644b2e6769663f)

    2.  **Audio/Video** Built a time controller for selecting a time
        start and end of the video those controllers (buttons and
        [ion-slider](http://ionden.com/a/plugins/ion.rangeSlider/)
        manages the video running duration and starting and ending
        time  
        [![video-audio-addson](https://user-images.githubusercontent.com/39674365/129346548-e7437d6d-532f-4d45-a701-9efc47d11a8e.gif)](https://user-images.githubusercontent.com/39674365/129346548-e7437d6d-532f-4d45-a701-9efc47d11a8e.gif)

    3.  **Text experiments** extended the current base highlighting
        feature of concordance to be able to use on the normal
        experiment also  
        [![text-adds-on](https://camo.githubusercontent.com/e4722fab78eedb7951a81e94a052c7f3691727001f66d8a51c6bbd6bd2da283b/68747470733a2f2f63646e2e686173686e6f64652e636f6d2f7265732f686173686e6f64652f696d6167652f75706c6f61642f76313632383730363534313439362f672d626b79686542686f2e6769663f6175746f3d666f726d61742c636f6d7072657373266769662d713d363026666f726d61743d7765626d)](https://camo.githubusercontent.com/e4722fab78eedb7951a81e94a052c7f3691727001f66d8a51c6bbd6bd2da283b/68747470733a2f2f63646e2e686173686e6f64652e636f6d2f7265732f686173686e6f64652f696d6167652f75706c6f61642f76313632383730363534313439362f672d626b79686542686f2e6769663f6175746f3d666f726d61742c636f6d7072657373266769662d713d363026666f726d61743d7765626d)

    </details>  

------------------------------------------------------------------------


# Accomplished tasks list

### WEEK 01

1.  Fixed graph reloading at the settings of an experiment .
2.  Found a new bug when exporting the results as CSV.
3.  Updated the setup of adding annotation level; to allow marking on
    multi choice level
4.  Finished the needed UI functionalities at the annotation process for
    supporting the new multi-choice functionality.
5.  Finished the required database schema changes for multi-choice
    functionality.
6.  Edited the annotation process endpoint to adapt with the new request
    structure.
7.  Keeping working on it and testing and finding bugs on the new added
    or existing code base.

------------------------------------------------------------------------

### WEEK 02

1.  **Optimized the viewing of an experiment loading time in terms of
    large experiments files** I liked doing that xD
2.  Exporting results after making the multi-choice functionality at
    long format.
3.  Edited exporting results at the concordance exp. type, added new
    column of video snippet annotated changed, start and end times,
    offsets!

------------------------------------------------------------------------

### WEEK 03

Filtering view results based on a specific annotation level or
    annotation level label

------------------------------------------------------------------------

### WEEK 04

1.  Added ordering the selection of label at annotation process (new
    column added at long-format)
2.  Finished wide format at exporting results
3.  Added warning when user changes the multi-choice option of an
    annotation level
4.  Finished viewing a specific entry within the changes on multi-choice
    levels
5.  Working on changing a specific file annotation from viewing results
    page
6.  Working loading time of exporting an experiment results at standard
    format

------------------------------------------------------------------------

### WEEK 05

1.  Allowed changing a specific file annotation from viewing results
    page
2.  Optimized loading time of exporting an experiment results at
    standard format and wide format
3.  Seeing the level order number of a particular annotation level
    (level number attr.) while setting an experiment and being able to
    change that number if needed in a way more efficient than we
    currently have.


------------------------------------------------------------------------

### WEEK 06

Re-uploading an experiment and continue to based on the results
    exported in wide format feature

------------------------------------------------------------------------

### WEEK 07

1.  Fixed the bug of going to results when there is no annotator
2.  Finished disabling uploading after first uploaded done on
    concordance
3.  Added changing order of an experiement
4.  Changed display edge link for new scape only
5.  Look at VIA and checked out if it could be integrated to RA or not

------------------------------------------------------------------------

### WEEK 08

1.  Working on switch display order functionality (figure out its
    effect)
2.  Working on the VIA(VGG-Images-Annotations) integration to allow new
    annotation abilities, i.e. adding polygon boxes and starting and
    ending of the videos Current UI updates integrated ![Demo of via
    annotation.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1627835788119/m81VRoVTe.gif?auto=format,compress&gif-q=60&format=webm)

------------------------------------------------------------------------

### WEEK 09

1.  Support Highlight feature of text annotation experiment for
    non-concordance experiments
2.  Working on adding UI components for the video and audio experiments
3.  Going to edit the database to store the annotations as JSON column
    type

------------------------------------------------------------------------

### WEEK 10

Integrated VIA and added audio/video controllers for time range from
scratch as well as extended the highlighting feature and fixed a lot of
bugs while working on those tasks which I call the annotations adds-on
and add it into the database, I would like to explain what structure has
been followed

-   Image experiments it contains an array of shapes which was drawn on
    the image
-   Audio/Video experiments a json object contains starting time and
    ending time in seconds
-   Text contains the first index of the selected character within the
    highlighted text


------------------------------------------------------------------------

# Challenges

- Always I think starting in new something is the most hard part of the story, so getting into the project for the first time was a challenging
- VIA integration and modifying to to be compatible with RA it was the hardest part (10k lines of code had to get what is going on and then start writing some code to make it works for RA was)
- The time controllers and range slider for the annotation adds-on also was a challenging part to make the video synchronized with the controllers buttons and inputs but it was interesting
------------------------------------------------------------------------
