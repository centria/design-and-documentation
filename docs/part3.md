---
title: "Part 3 - Markup languages"
permalink: /part3/
nav_order: 3
published: true
---

# Markup languages

*"In computer text processing, a markup language is a system for annotating a document in a way that is syntactically distinguishable from the text, meaning when the document is processed for display, the markup language is not shown, and is only used to format the text. The idea and terminology evolved from the 'marking up' of paper manuscripts (i.e., the revision instructions by editors), which is traditionally written with a red or blue pencil on authors' manuscripts. Such 'markup' typically includes both content corrections (such as spelling, punctuation, or movement of content), and also typographic instructions, such as to make a heading larger or boldface."* [**Wikipedia**](https://en.wikipedia.org/wiki/Markup_language)

Markup languages are not coding languages, even though they have quite similar features. Markup languages are widely used in creating documentation, and that is why we also need to know something about them. Some markup languages are also used in for example system configuration, and you might have written some already without knowing about it. Let's take a look at few of them.

## HTML

*Hypertext Markup Language* HTML is often referred to as a programming language, which is technically not true. It is a markup language, describing the structure of a document. HTML comprises a set of elements and tags used to define and show different sections of the document, also giving them specific functionalities. Tags can for example turn a word into a link, make it cursive, or change its size.

Here is an example of an HTML element:

```html
<p>This is a piece of text.</p>
```

Let’s look at the structure of the element. An HTML element is composed of three parts:

1. The start tag *\<p\>*
2. The content itself This is a piece of text
3. The end tag *\</p\>*

HTML tags are keywords hidden inside the site, but not shown to the end user by the browser. They define how the browser styles and shows the contents of the document the user is viewing. There are countless different HTML tags, each serving to create specific kinds of elements. We’ll start with the elements used to edit text.

1. *\<h1\>\</h1\>*: This tag is used to create heading elements. There are six different heading tags, ranging from h1 to h6. The primary heading is created using the first tag h1. The least important heading is created with h6.
2. *\<p\>\</p\>*: The element created with the tag p contains the body text of the document.
3. *\<em\>\</em\>*: The text inside an element created with the tag em is shown in cursive.
4. *\<strong\>\</strong\>*: The text inside an element created with the tag strong is shown in bold. You can also create elements with \<b\> and \<i\> to show text in bold and cursive respectively.


With these, we can create even static web page. Let's start with a little less ambitious project, and have ourselves a piece of code:

```html
<h1>This is the header</h1>

<p>This is a <strong>sentence</strong>.</p>

<p>This is a <b>bold</b> and <i>recursive</i> sentence.</p>
```

If we take this into a file and open in it our web browser, we will get a view like this:

![First html](https://github.com/centria/design-and-documentation/raw/master/assets/images/part3/html.jpg)

Now you might be wondering, *"what does a web page have to do with documentation or design?"* and that is a good question. The answer, in short, is *"nothing and everything"*. Most of our documentation is nowadays online, and we want our documentation to look decent, and not just a wall of text. Take this course page, for example. This was written in another markup language, and it has then been translated into HTML.

We do not have to go deeper into HTML this time as we will look into in in the fall. A quick summary for HTML is still in order: You could say, that all webpages use HTML for their user presentation. Most likely, most of the page is written in some other language, but the view you are looking at, is done in HTML.


## XML and YAML

Another notheworty markup languages are *Extensible Markup Language* (XML) and *YAML Ain't Markup Language* (YAML). Even though they are not directly used in documentation, they are used in our programs quite often. 

For example, the quite familiar **C# project files**, with the file extension **.csproj**, use *XML* syntax. On the other hand, *YAML* is often used in configuring web pages. This course page uses YAML to determine page order in the navigation bar, and even the address for the subpages.

You can see an example of YAML here:
[**This web page's source code.**](https://raw.githubusercontent.com/centria/design-and-documentation/master/docs/part3.md) The first few lines, separated with lines from the rest of the code, are a common way of using YAML.

```yaml
---
title: "Part 3 - Markup languages"
permalink: /part3/
nav_order: 3
published: true
---
```

The content of the YAML, however, depends very much on where it is being used. These lines are meant for the [**Jekyll site generator**](https://jekyllrb.com/), which is used to generate these web pages.

An example of XML you can find here:
[**.csproj file for exercise_01.**](https://raw.githubusercontent.com/centria/coding-exercises/master/part1/printing/exercise_01/exercise_01.csproj) As you can see, the syntax is quite close to that of HTML:

```xml
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <TargetFramework>netcoreapp3.1</TargetFramework>
    <GenerateProgramFile>false</GenerateProgramFile>
    <IsPackable>false</IsPackable>
  </PropertyGroup>

  <ItemGroup>
    <PackageReference Include="nunit" Version="3.12.0" />
    <PackageReference Include="NUnit3TestAdapter" Version="3.15.1" />
    <PackageReference Include="Microsoft.NET.Test.Sdk" Version="16.4.0"/>
  </ItemGroup>

</Project>
```

Here we have tags, just like in HTML, which have an opening and closing.

Just like HTML, we do not have to go deeper into these languages at this time, you will learn them as you use them. Most of the markup languages are quite straight forward, and resemble each other greatly. It is important, how ever, to know of their existance, and about the multitude of uses for them.


## MarkDown

Unlike previous examples, *MarkDown* (MD) is actually used quite often in documentation for software. One main reason is that the **REAMDE.md** files in *git repositories* are in fact markdown files (md is short for markdown). There are several different *flavors* to markdown, which means slight changes to syntax. We are usually using the **GitHub Flavored Markdown (GFM)**.

In most gits (there are more than just GitHub), the first file you notice is the **README.md** file, as it is rendered into more human readable format in the git repository starting page. README history dates back to the first commercial computer programs, which were shipped with a README file with them. The file usually contained all the crucial information, such as how to compile and run the program. 

Jumping back to this day, the README.md is the landing information of a repository. It usually holds the most crucial information for a repository, such as if the build is stable, how to install, test and run the code, what are the requirements, and so forth. Quite a lot of documentation can also be put into the README.

For this reason, we want to know of MarkDown. Probably the best cheatsheet for MarkDown is here:

[**https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet**](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

Another excellent comparison between markdown and HTML can be found from here: [**https://en.wikipedia.org/wiki/Markdown#Example**](https://en.wikipedia.org/wiki/Markdown#Example)

These contain all the crucial information, how MarkDown is properly written. Let's take a look at the few, most important parts.

* **#** the pound sign (or as it nowadays known, the hashtag) creates a header. With one character, you can create the largest header (h1 in HTML), with two the second largest (h2), and so on. With the following code:

```md
## This is a header level 2
```

We get

## This is a header level 2

* With stars **\***, you can do several things: Adding two starts before and after a sentence, you can make text **bold**. The following part \*\*would be bold\*\* in MD. With one star, \*, you can create *italics*. So \*this would be in italics\*.

```md
**This text is bold**  
*This is slanted*  
```

**This text is bold**  
*This is slanted*  

* To create a list (like this), you can also use a star. This time, have the star at the beginning of a line, and a space after it.

```md
* To create a list (like this)...
```

* To create a list (like this)...

* To create an ordered list, have a number with a dot in the beginning. So for example, we could create list with

```md
1. First ordered list item
2. Another item
    * Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
    1. Ordered sub-list
4. And another item.

   You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

   To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
   Note that this line is separate, but within the same paragraph.  
   (This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

* Unordered list can use asterisks
- Or minuses
+ Or pluses
```

This will create a HTML like this:

1. First ordered list item
2. Another item
    * Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
    1. Ordered sub-list
4. And another item.

  You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

   To have a line break without a paragraph, you will need to use two trailing spaces.  
  Note that this line is separate, but within the same paragraph.  
   (This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

* Unordered list can use asterisks
- Or minuses
+ Or pluses


Source: [https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

* To create a link, we want to use \[link name here\]\(https://actuallink.com\) square brackets, followed by regular brackets. The first one is the text shown to the viewer, and the latter is where the link actually takes us.

```md
This will create a link: [Google.com](https://google.com)
```

This will create a link: [Google.com](https://google.com)

Markdown is a very versatile markup language, that can be used for various places. Did I already mention, that all the course pages are also written in MD? You can see the example from example here: [**https://raw.githubusercontent.com/centria/design-and-documentation/master/docs/part3.md**](https://raw.githubusercontent.com/centria/design-and-documentation/master/docs/part3.md)

You can see the HTML representation of the code right on this page. Another interpretation can be found also in GitHub, as it also translates all the MD files into HTML:
[**https://github.com/centria/design-and-documentation/blob/master/docs/part3.md**](https://github.com/centria/design-and-documentation/blob/master/docs/part3.md)

## LaTeX

*LaTeX (/ˈlɑːtɛx/ LAH-tekh or /ˈleɪtɛx/ LAY-tekh)* is a document preparation system, which uses markup tagging conventions. It is not a markup language as such, but behaves like one. This system is used widely in natural sciences to produce publications and other scientific documents.

We can go and see an example here:
[**https://en.wikipedia.org/wiki/LaTeX#Example**](https://en.wikipedia.org/wiki/LaTeX#Example)

With LaTex, you can create complex formulas which have the correct indentation, spacing and notation. This system does, how ever, require quite a bit of learning to be used efficiently. Once mastered, LaTex is a handy tool for creating larger publications, such as thesis work.

We will (probably) not be using LaTeX in any of our courses, but once again, a noteworthy system to be aware of.

## Tools of the trade

* You can write HTML in any editor you like. Visual Studio Code, for example, has support for it: [**https://code.visualstudio.com/docs/languages/html**](https://code.visualstudio.com/docs/languages/html)

* You can write MD in any editor you like. You can get a Markdown Preview plugin for VSC, where you can see your code turn into HTML in real time. There are several available, I use [**https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced**](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)

* Another great tool is [**https://markdownlivepreview.com/**](https://markdownlivepreview.com/), which does basically the same thing: You can see your md transform in real time.

* For LaTeX, one of the most popular tools is [**https://www.overleaf.com/**](https://www.overleaf.com/). You can see your document in rich text in real time, you can integrate git to your project for backup, and you can import or export projects. Nowadays, you can even do some rich text editing, and it will turn into LaTeX code for you.

* For creating mathemathical formulas in LaTex, I recommend [**https://www.codecogs.com/latex/eqneditor.php**](https://www.codecogs.com/latex/eqneditor.php). You can point and click the items you want, and the tool will transform it into code, as well as give you a preview.

* For quite any markup language, you can try [**https://jsonformatter.org/**](https://jsonformatter.org/). If you scroll down, you will se a menu with JSON, HTML, XML and YAML and tools for them, along with some other tools.

* Once again, if you are familiar with any other tool you can use the tools you like, or especially, *if you have a tool recommendation*, do let me know, and I'll add it to the list!

[**You can find the exercises here**](/design-and-documentation/exercises/#part-3)