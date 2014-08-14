![AllSeen Logo][AllSeenlogo]
<a name="Top"> </a>



# AllSeen Documentation Writing Guide

August 13th, 2014




## Table of Contents

* [Introduction][Intro]
* [Chapter 1 Introduction to AllSeen Technical Documentation][Chap1]
* [Chapter 2 Some Tips on Structured Writing][Chap2]




##Introduction

### Purpose

This document is a companion to the AllSeen markdown templates and cheat sheets

### Scope

Indicate the targeted audience for this document, e.g. :

This document is intended for anyone creating AllSeen documentation in Markdown format. This document assumes that you have a very basic knowledge of the Markdown text format. In order  to assist you in creating your documents, AllSeen also provides templates and a Markdown cheat sheet.


### References

* Single-page documentation template.
* multiple-page documentation template
* Markdown cheat sheet 

*Author's note: links to be added*

### Tools

While you can use a plain text editor to create and edit Markdown files, an editor that allows some kind of preview is a bonus. I recommend using [Markable](http://markable.in/editor/), a very simple and good online editor that supports all AllSeen-used Markdown syntax.

### Acronyms and Terms

Below is a list of used acronyms and terms:

* **(Information)Block:** The smallest consisten piece of written information
* **(Information)Map:** A set of related information blocks forming a separate unit.
* **Markdown:** Markdown is a plain text formatting syntax designed so that it optionally can be converted to HTML using a tool by the same name. Is is intended to be human readable in simple text editors as well as in dedicated editors.

### Revision History

| Date          | Comments                         |
| ------------- | ---------------------------------|
| 2014/08/14    | 0.1 Initial Version (Jan Lissens)|

[Back to Top][Top]

##Chapter 1 Introduction to AllSeen Technical Documentation

### 1.1 Location of the Documentation

#### Sources

The documentation sources are stored in Git:

```location TBA```

#### Published Version

The published version of the documentation is available on the AllSeen Alliance website:

```location TBA```


### 1.2 The AllSeen Documentation process

![AllSeen Logo][DocProc]

The process is as follows:

1. The set of documentation files is kept in git. This documentation set contains al markdown files as well as certain scripts needed for import and preview
2. The Technical Writer (TW) (or any other documentation contributor) clones the git-repository
3. The TW creates/modifies the required markdown files to update the documentation.
4. The TW uses the preview script to preview the documentation and verify
4. If all is well, the files are merged into git and approved through Gerrit
5. At certain intervals, the main branch of the documentation is converted into HTML and then imported in Drupal.
6. The information is now available through the AllSeen Alliance website


### 1.3 Submitting Your Documentation

Info to be added here.



### Using the Preview Script

Info to be added here.

[Back to Top][Top]

##Chapter 2 Some Tips on Structured Writing

### 2.1 Introduction

#### What is Structured Writing

Structured writing is the act of creating a structured document. A structured document is a document that organizes its content in well-defined chunks of information called blocks.

Entire libraries have been written on the subject. The scope of this chapter  is not to make you a full-fledged structural writer, but to acquaint you with its basics and provide some tips to better structure your documents.

####Diagram of a Structured Document

Below is the diagram of a structured document. The concepts used will become clear.
![AllSeen Logo][StrucDoc]

### 2.2 Principles and Information Units in STructured Writing

#### Principles

The basic principles of structured writing are:

**Chunking:** information is split into small chunks of information called blocks. A block should be small and contain only one type of information. The intent is to make the reader process the information in palatable chunks rather than one long continuous text. The paragraph you are reading is actually a block. It covers the concept of chunking and provides you with definition of what chunking does.

**Relevance**: related parts of information are placed together. This block on "Relevance" is placed where the other principles are explained. However logical this seems, many documents suffer from bad readability due to related parts of information being put in differebt places. 

**Typing:** There are several basic types of information, and each type of information can be represented in a specific way. For an overview of the most important types, continue reading.

**Labelling:** Each chunk of information gets a label or title.The boldface word "Labelling preceding this block is actually its label.

**Hierarchy:** Chunks of information are organized in an structured hierarchical way. The highest hierarchical part in this document is the document itself. It is divided into Chapters. Each Chapter is divided into Sections, and so on.

**Consistency:** Use the same words and structure to represent similar things. As an example, if your document has several blocks providing information on the syntax of commands, provide the same label for each block e.g. "Syntax". Consistency can become a problem if you are wotking on a document with multiple authors. A good document review will reduce inconsistencies.

**Accessible Images:**Pictures will speak a thousand words, but only if you place them where the reader expects them. Only use relevant images. Avoid unnecessary images, but remember that an image can clarify things no text can.


#### Information Units

The basic information units are:

**Information Blocks:** A chunk of information. it covers a single type of information and has a clear label describing it.

**Information Maps:** A set of related blocks. A map should contain 5 to 9 blocks. Avoid long maps. If a map becomes too long, split (chunk) it.
A specific kind of map is the overview map, which does not provide (much) content on its own, but serves as binder for a number of related maps. In the multiple-page template, the document overview.md is an overview map, binding the other maps (chapters) together. On overview maps contains at least a block providing a short description of what the map is about and a block with a list of the related maps (table of contens).

Most documents will be larger than a single map. To create larger document:

* Several maps and an overview map form a section.
* Several Sections and an overview map form a Chapter
* Several Chapters and an overview map form a Document

### 2.3 Information Types

#### About Information Typing

Every piece of information has a type. The type of information determines how you will represent it in your document. Each type of information is processed differently by the brain, so distinguishing them and representing each bit of information according to its type will aid the user of your document.

#### Basic Information Types

There are several methods of structured writing out there (DITA, Information Mapping,...) and each of them provides a number of types, but the most basic disctinction you can make is:

* **Knowledge information:** teaches you what you need to know.

* **Procedure information:** teaches you what happens or how you need to do something.

Depending on the method, different names are given and more specific types can be defined

#### More Advanced Information types

Knowledge information can be:

* **Concepts:** an objective presentation of an idea or object you are trying to convey to your reader e.g. "java class" 

* **Structures:** A set of related parts, values,... e.g. the syntax definition of a java class. 

* **Guidelines:** A related list of things that are allowed/not allowed/recommended... e.g. maximum length of a code line in a program.

Procedure information can be

* **Process:** describes a related sequence of events with a specific objective, e.g. "The AllSeen Documentation Process".

* **Procedure:** describes a set of actions to be taken with a specific goal in mind, e.g. "How to submit your code changes in Gerrit".

### 2.4 Representing Information

Again, a subject worthy of lenghty treatment, but here are some down-to earth tips on how to best represent an information type:

#### Procedures and Processes

These are the simplest to do: 

- Always use numbered lists! Don't use a narrative. 

- Keep your sentences concise. 

- If you want to properly distinguish between processes (what happens) and procedures (what a user needs to do), use *descriptives for procedures* (e.g. "The Writer merges his changes into Gerrit") and *imperatives for processes* (e.g. "Merge your changes into Gerrit")

- If you have access to the services of an illustrator or if you are handy with (and in possession of) drawing tools, you may want to use diagrams. Kudos if you can do it, but not a must to properly describe a procedure or a process. Don't try and make them too fancy. Black and white wire drawings are just as effective as fancy full-coloured stuff. For drawing initiates, PowerPoint can produce decent diagrams. All diagrams in this document were made with it just to prove that point. For specific types of diagrams (UML, flow charts,...), a more advanced tool is better.

### Knowledge Information

Getting into detail about this takes us outside the scope of this document, but below are some tips and frequently used examples:

- For guidelines and tips, use a bulleted list (such as this one)

- For structures (e.g. the parts of a syntax), use a bulleted list, or a table. Drawings are great if you have the skills, the tools and/or the people to create them.

- For new concepts, use a descriptive or a definition. For a good definition, always start with a general, known concept and then specify. As an example:

>Alljoyn *(the concept you are trying to bring across)* is a communication framework *(the general concept)* that allows applications on devices of different types and with different operating platforms to communicate with each other *(the specifics that set this concept apart from the general category)*. 

Mostly, you will go with descriptive text, bulleted lists or tables. Do the effort of using tables. The Markdown syntax takes some getting used to, but they are worth it

|Reason for Using a Table |Description|
|-------------------------|-----------|
|Clarity|Tables are one of the clearest ways to structure complicated content. They also look better in HTML.|
|Conciseness|Tables can save you a lot of words.|
|Readability|Tables are a lot more readable than long text blocks.|


### 2.5 How To Go About Creating a Structured Document

#### General Procedure

Again, this can be the subject of several very large volumes (and actually is) but to get you started, this is the way to go:

1. First off, preparation is everything. Think before you start. Consider the objective you want to reach with your document. 

2. Now consider the following two questions:
     - What do you you want the user to be able to do (=procedures)
     - What does he need to know to do this? (=knowledge)

3. Determine the type of knowledge and choose how you will represent it.

4. Leave out everything else, no matter how interesting it is. Only provide the user with the stuff he needs to know. Nothing else. Most users of a technical document prefer not to be bothered with tidbits of information they don't need to know.

5. Arrange procedures and knowledge in an hierarchical block/map/document structure. Don't use large maps and blocks. A block typically contains between 5 and 9 sentences. It contains only one type of information. A map typically contains 5 to 7 blocks. Use overview maps to combine your maps into a larger structure.

#### Example: Making a Phonecall

I want the user of the document to be able to make a phone call with a specific phone. 

##### Distinguishing between knowledge and procedure:


|Knowledge|Procedure|
|---------|---------|
|What is a phone (concept)| Steps required to make the call(procedure)|
|(Relevant) Parts of the phone (structure)| |

##### Determining how to represent
We can now determine how to represent these pieces of information:

* "What is a phone?"  - Definition (text)

* "Parts of the phone"  - Bulleted parts list providing the name of the part and the function

* "Steps required" - Numbered list

Only provide the infomation required. For example, on the parts list, only name those parts needed for understanding the procedure (e.g. horn and dial pad).


[Back to Top][Top]

## Chapter 2 Tips and Guidelines for AllSeen Documentation

More content to be put here as it becomes available

#### Defining Links

For internal links, use reference style links. A reference link consists of two lines:
* The actual link, placed where you want it to be
* The definition of the link target, placed at the back of the document.

This applies to both document links and image links. For more information, have a look at the template file, the markdown cheat sheet or the source of this document.







[AllSeenlogo]: /AllSeenlogo2014.jpg
[dummy-image]: /dummy.jpg
[StrucDoc]: structured-document.jpg
[DocProc]: doc-process.png
[Top]:#Top
[Intro]: #introduction
[Chap1]: #chapter-1-introduction-to-allseen-technical-documentation
[Chap2]: #chapter-2-tips-and-guidelines-for-allSeen-documentation

