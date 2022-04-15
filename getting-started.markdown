---
layout: default
title: Geting Started
nav_order: 2
---

1. TOC
   {:toc}
   
# About Collective Biographies of Women

A collective biography is "a set of three or more chapter-length biographies placed together in a single book." CBW is a digital humanities project that contains data from all English-language collective biography volumes written about women. The public interface (that is, what the public sees on cbw.iath.virginia.edu) contains:



* **Chapter-length biography** records with information about the chapters
* **Person** records with information on the subjects of the chapter-length biographies
* **Book** records with information on the volumes that contain the chapters
* **Text markup** of individual chapters called BESS 
* **Visualizations** of documentary social networks of people that co-occur in the same book
* **Case studies** focused on individuals or cohorts


# The Admin-Side Interface

The admin-side interface is where we add or correct the data in the CBW database. In the admin-side interface, you can:



* Edit chapter, person, and book records
* Track work assignments, especially for BESS markup and vetting. 

<span style="text-decoration:underline;">Go to the Admin-Side Interface</span>


# BESS

BESS stands for "Biographical Elements Structure and Schema." It's an XML schema for nonfiction narrative analysis based on feminist narrative theory. Alison Booth conceived and wrote BESS based on her narratological study of collective biographies of women.

Here's an example of the BESS Viewer:

**Things to note:** 



1. The collection and chapter biography appear at the top, including ID numbers.
2. The text of the chapter appears on the left.
3. Tags appear on the paragraph level, like _youthful desire for love._
4. Tags belong to different categories, which appear in vertical swimlanes like _Topos _or _Discourse. _
5. Each paragraph in the chapter text is numbered.

And here's an excerpt of the BESS XML for an event:  \



```
        <event namedEventKey="E00032">
            <textUnitRangeReference>
                <start>6</start>
                <end>7</end>
            </textUnitRangeReference>
            <type>marriage, arranged</type>
            <agentType>mother</agentType>
            <agentType>fiance</agentType>
            <agentType>male professional, named</agentType>
        </event>
        <event namedEventKey="E00033">
            <textUnitReference>6</textUnitReference>
            <type>escape</type>
            <type>wedding</type>
            <type>elopement</type>
            <agentType>officer, military</agentType>
            <agentType>lover, male, named</agentType>
            <locationSetting>Ireland</locationSetting>
            <locationSetting>city</locationSetting>
            <dateSingle standardDate="1837-07-23">July 23, 1837</dateSingle>
        </event>
```


Don't worry if the markup doesn't make perfect sense to you. We'll walk you through creating BESS markup in these guides. The examples just give you an idea of the data with which you'll be working. You can learn more about the theory of BESS [on the CBW website](http://cbw.iath.virginia.edu/narrative-analysis/). 


### BESS is Stand-Aside

BESS markup is "stand-aside" – this means that you don't include the markup in the same XML file as the chapter text, which will already be encoded in TEI format.  Instead, you make a separate XML file that follows the BESS schema. Your new BESS XML document will reference paragraphs in the text. You'll add all your markup within nesting XML tags that tell the program how to categorize your narratological observations.  



<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")


For the example above: 



* the opening tag, &lt;textRangeReference>,  lets the XML know that you're about to give it a range of paragraph numbers. 
* the closing tag, &lt;/textUnitRangeReference>, lets the XML know that you've finished supplying the range of paragraph numbers. 
* The &lt;start>&lt;/start> tags reference the first paragraph number in the range: in this case, paragraph 6. 
* The &lt;/end>&lt;/end> tags reference the last paragraph number in the rage: in this case, paragraph 7.  

Together, the opening and closing tags, with their enclosed value, comprise an XML element.  If this explanation feels complicated at the moment, don't worry.  We'll break down the steps more specifically. 


### BESS Uses Controlled Values

As you can see in the diagram, BESS adds tags to the text at the paragraph level. There are five elements: 



* **StageOfLife** (which parts of the text narrate events in different phases of the persona's life?);
* **Events** (what with AgentTypes, Locations, dates, etc.);
* **Discourse** (which includes narrative technique, figures of speech, quotations of other texts, etc.);
* **Persona Description** (how are these exemplary or "bad" women characterized in versions at different historical periods?); and
* **Topos** (this is an element for identifying scenarios or typical structures such as "influence" or "recognition" that underlie the overt action).

When you're adding BESS markup for a text, the specific tag isn't completely up to you. Instead, you choose tags from a list of controlled values. For example, if you are adding an "Event", you can choose from _coronation_, _birth_, _adoption of_ _child_, and more. These controlled values help to keep BESS analysis standardized, even if multiple editors contribute to the database. 


## What work might I have to do?



* Analyze text using BESS markup and controlled values
* Edit existing BESS markup files  
* Perform data cleansing of person records
* Add or correct associations between collections, biographies, and people
* Use the Admin-side database's workflow management system


## Where do I do the work?

You’ll use your browser if you’re using the admin-side database. If you're working on BESS markup, you'll use oXygen to edit the CBW repository at XXXX. See 

<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "the next section"). Did you generate a TOC? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

[the next section](#heading=h.giwyvtpzgyvv) to set this up. 

If you're doing anything else, you'll use the admin-side database interface at XXXX and access it with a Contributor password


## What do I need to get started?



* a laptop and UVa netbadge access
* [a VPN connection for remote work](https://virginia.service-now.com/its/?id=itsweb_kb_article&sys_id=f24e5cdfdb3acb804f32fb671d9619d0) 
* oXygen
* access to the SVN client
* access to the admin-side database


### Access to the Admin-Side Database 

In order to make changes you'll need "Contributor" access; XXXXXXXXX  can give you the password.

<span style="text-decoration:underline;">Go to the Admin-Side Interface_._</span>


### oXygen

You'll use oXygen to edit chapter XML – this adds BESS analysis to chapters. To get oXygen for free from UVA, follow [this guide](http://data.library.virginia.edu/research-software/oxygen/) from the UVA Library. You'll download oXygen, then use a free license from UVA Software to activate the tool. 


### SVN

The oXygen tool includes an SVN client, which is a versioning software that manages changes made by all team members on the CBW repository. Although oXygen is not required for SVN in principle, at CBW we always use SVN and oXygen together. You will only need to do this once. Here are the steps:



1. Open oXygen
2. Click **Tools**, then **SVN Client**
    * The Syncro SVN Client will open
3. Click **Add new repository**
4. In the URL field, enter: XXXXXXXXX
5. Enter your sign-in information
    * A CBW team member will send you this 
6. Validate the information
    * You'll see a list of files: this is a CBW repository
    * This list of files will now open automatically every time you access the CBW client in oXygen

You've accessed the repository, but now you have to make a local copy. This lets you edit the repository safely from your computer. With the SVN Client open, follow the steps below: 



1. Make a new folder on your computer
    * This is where you'll keep a local copy of CBW
2. In oXygen, selectXXXXXXXXX under "Repositories"
    * If you don't see this location, click on the **Repositories** tab of the Syncro SVN Client in oXygen
3. Click the **Check out...** icon 
    * This icon looks like a cylinder with a blue arrow; it's the first one in the top menu 
    * You'll see a "Check out" window open
4. Next to the "Check out to" field, click **Browse**
5. Open the file you made in step 1
6. Click **Check out**
    * You can leave the other fields as-is
    * This adds a copy of the CBW repository to your computer: you can see this under the Working copy tab of the SVN Client
