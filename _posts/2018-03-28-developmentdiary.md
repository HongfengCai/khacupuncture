---
layout: post
title: Development diary
categories: web1
tags: diary
author: Aemon
description: This is my development diary. I am going to record my all learnning process and sumary my knowledge point here. I also follow my lecturer Elise footsteps to improve my web development skills and English writing ability.
---

# Introduction 
This is my development diary. I am going to record my all learnning process and sumary my knowledge point here.
I also follow my lecturer Elise footsteps to improve my web development skills and English writing ability.

-----

## Lab 1.2 Development workflow
In this lab, I have to know the web development workflow with git version control tools.
I decided to use Adobe Dreamweaver software to development my web page include Html, CSS 
and JavaScript. Because I had utilised this software to work a few years, and also be installed
on polytech desktop.

About workflow, there is core concept which are three places. We called it branch, any create,edit 
or update and delete all need to do under the three branch, Master,Development and NewFeature branch,
I will name my feature branch is lab order. I put my understanding of workflow to below:
1.  New create branch, in this lab, the branch was named lab1-2 under the master -> Development -> Lab1-2
2.  Create,Update or Delete my Html,CSS or JavaScript files in local repository with Adobe Dreamweaver.
3.  When I finish each work task, I have to use "git add filename" command to add new file to be tracked 
    by Git, also I have to use "git commit -m "what part did I change"" command to commit.
4.  When I finish each lab, I should checkout to development branch and use "git merge lab1-2" to merge file.
    At the same time, I can test the feature whether be implemented.
5.  When all feature are completedly be implemented, I should switch Master branch and merge all contents.
    
```bash
git clone url
git add FileName
git commit -m "ActionDescription"
git push origin BranchName
git branch NewBranchName
git checkout -b NewBranchName
git checkout NewBranchName
git merge OldBranchName
git fetch
git pull
```

That are sorts of development workflow above, All new feature development will iterate through these steps.


## Lab 1.3 HTML
Today, I have reviewed too much HTML tag, I was a web developer in ten years ago. There was no HTML 5 version
markup language, but I stll use div with css to do layout. I also named my logo and title area as Header, and 
named my navigation as nav or menu, HTML 5 did a lot of work to normalize most popular tag to offical form. 
Such as Header,Nav,Article,Aside,Footer and so on. But I know that except the nameing is more semantic, no more
special, all tag style still need I write CSS to control. I just remember at one time, the web page all layout
need to use table to orgnize. Ok, I talked a lots of rubbish words...

I think that the most commonly used tag are:
```html
<p> <span> <br> <ul> <li> <div> <table> <tr> <td> <a> <img>, &lt;, &gt;,
&amp;, &quot;, &nbsp;  <form> <input> <textare> <radio> <checkbox> <option> <multiple> <submit> <reset>
```
It can instead of whitespace, mailto as email hyperlink to start email app, as well as the form relative tag, such 
as above:

## Lab 1.4 Cascading Style Sheets
In this lab, I am going to focus on CSS, I will sumary css relative knowledges in here. CSS is used to set up the styling 
of each HTML element tag, therefore, in the first place, we have to know how to choose HTML tag. The CSS supply three kinds of 
way to choose HTML Tag:

The first one is ID selector, the code like
``` html
<a src='' ID='myHyperLink'> | #myHyperLink {font-size:12px;} 
```
The second one is Class selector, the code like
``` html
<a src='' CLASS='myHyperLink'> | .myHyperLink {font-size:12px;} 
```
The third one is HTML tag selector, we can write CSS code directly, do not need to markup HTML element, the code like
``` css
html body div { font-size:14px; color:#00ff00; line-height:14px; text-align:left;}
```
Futhermore, the CSS selector has inheritance property with sub tag, we can wirte code like that:

``` html
<div class="myTopArea">
    <header></header>
    <nav>
        <ul>
            <li>Home</li>
            <li>About</li>
            <li>Contact</li>
        </ul>
    </nav>
</div>
```

``` css
.myTopArea { width:80%; height:auto; float:left; over-flow:hidden; text-align:center;}
.myTopArea header { background-image:url("header_bg.png");}
.myTopArea nav {}
.myTopArea nav ul {list-style:none; margin:0px; padding:0px;}
.myTopArea nav ul li {float:left; display:block; width:160px; height:50px; line-height:50px;}
.myTopArea nav ul li:hover {float:left; display:block; width:160px; height:50px; line-height:50px; font-weight:blod;}
```

This code is very readable.


## Lab 1.5 CSS box model 
This lesson talk about CSS box model. Like the margin, padding property and so on...
* The background-clip property to set up how to clip the element background. its default value is border-box, and other 
  value are padding-box,content-box and text, the different clipping boundaries are specified.
* The overflow property to set up the element content whether display when the content greater than the box. The optional 
  values of available are visible (default), hidden, scroll and auto, I always use hidden.
* The border-box is one of the value to box property, just represent the clip from border(not include border) start.


## lab 1.6 Tables and Lists
In this lab, mainly talk about table and lists. These two tags uses very high frequency. In many cases, especially when 
displaying detailed information, we need table, and list as well. nowadays, to many website use lists such as ul li tag
to create nav or menu. I will put some my code to bleow: <br>
``` html
<table width="100%" id="mytable">
	<tbody>
		<tr class="colorgrey">
			<th scope="col">Code</th>
			<th scope="col">Course</th>
			<th scope="col">Credits</th>
		</tr>
		<tr>
			<td>IN601001</td>
			<td>Professional Practice 2</td>
			<td align="center">15</td>
			<td>IN501001</td>
		</tr>
		<tr class="colorgrey">
			<td>IN602001</td>
			<td>Software Engineering</td>
			<td align="center">15</td>
			<td>105 Credits at Level 5</td>
		</tr>
		<tr>
			<td>IN603001</td>
			<td>Project Management</td>
			<td align="center">15</td>
			<td>IN501001, IN505001</td>
		</tr>
		<tr class="colorgrey">
			<td>IN605001</td>
			<td>Database 2</td>
			<td align="center">15</td>
			<td>IN505001, IN511001</td>
		</tr>
		<tr>
			<td>IN610001</td>
			<td>Programming 3 –Java</td>
			<td align="center">15</td>
			<td>IN511001</td>
		</tr>
		<tr class="colorgrey">
			<td>IN612001</td>
			<td>Web 2 - Programming</td>
			<td align="center">15</td>
			<td>IN511001, IN512001</td>
		</tr>
		<tr>
			<td>IN614001</td>
			<td>Multimedia Development</td>
			<td align="center">15</td>
			<td>IN510001, IN512001</td>
		</tr>
		<tr class="colorgrey">
			<td>IN617001</td>
			<td>Linux Operating Systems</td>
			<td align="center">15</td>
			<td>IN510001, IN520001</td>
		</tr>
	</tbody>
</table>
```

``` css
#mytable{border-collapse:collapse;}
#mytable th{height: 30px; line-height: 30px; font-weight: bold; padding-left:10px;}
#mytable tr{ height: 25px; line-height: 25px;}
#mytable td{padding-left:10px;}
```


## Checkpoint1

Firstly, I have had created a folder which is named styles and stored my style.css
file to this folder, because when the website getting bigger, there are too much files
in the root dictory. so like that organization style can looks at clear.

I have had used three kinds of css selector which is Class,ID and Html markup tag.
In the first place, I set up the "html, body" and so on global markup tag style such
as background, font style and so on. After that, I set up the global layout div and 
container such as global container, header, nav and article. According to html tag 
order to wirte css content. The css selector name mostly ustilise class selector, 
except nav,header,footer tag, I also used some words like "container, mynav,myul"
some area relatived contents like "courses", "terchers" and "greyline".

I keep every single css property on one line, because it is very clear and could find
it fastly when the css property more and more large.

I sperate a few sergment to place different means css content. such as boxes, header,
article, footer.And i use css top tag and sub tag inherit relationship to named it.
such as "#mynav #mynav ul #mynav ul li...

In my container div,I set up the width is 100%, and also set up the background-image to
full fill. in the main contents area of middle,
I design to 80% width, includes article and aside, float left. the height will auto via
how much contents.
entire page,i used mostly color is green color, i think it is like New Zealand.

About Browser compatibility, I think this page is not friendly for some of IE version.
some style looks different between IE Browser and other... I will via my self learnning
to fix it later...

-----

## Lab 2.1: Assets and directory structure

Today, I learned how to orginise my Website directory. To create a few different directory and sub folder for all materials looks tidy.
Firstyly, we must base on a root directory, then we create functional directory such as Script, Style, Images, Video and so on.
because some website like BBS news, there are very hugh content update every time, so the number of page and files increasing very
fast, so we need to manage directory. Except some folder above, some website utilise CMS to manage content, so when CMS pushlis HTML
static page, there need a html folder to contain, and some folder naming way have to with time zone. And some web site utilise
SQLite database or Access database, they need a folder to store database files. 
So we need to choose different way to orginize directory according to the situation.

That is my imaging construct below:

- MyWebsite (root directory)
  - images
  - styles
  - scripts
  - html
     - 20180101
     - 20180102
     - 20180103
  - video
     - 20180311
     - 20180312
     - 20180313
  - database
  - dll
  - config
  - admin
  - index.html
  - about.html
  - contact.html
  - product.html
  - servicesupport.html

## Lab 2.2: Navigation and design

Here is activity on class which is Evaluating website design:
Actually, I am not a Expert, I just learn some concept of web Ddsign Elements. So these views just I have feeling some thing.

* (https://alistapart.com/)
  - Composition,Negative space. The main picture utilise original style, it is very impressive to user. And all content is very good composition, just like content is navigation.
* (https://designshack.net/) 
  - Colour, Balance.  That is a traditional design style website, the using of colour is not exaggerated. But looks really comfortable. The balance between content display and visual effect is just right.  ps: It is my preferred site.
* (https://www.smashingmagazine.com/) 
  - Direction, Texture. That's website has big font and simply content with single background color, it is easy to find what content I need to search. easy and fast navigate. In terms of text, the title and statistics number of commit times and some tags all different size, there is strongly contrast. The user could fast to locate content.  

## Lab 2.3: CSS Frameworks

* Bootstrap

* Pure.css
Purecss is a lightweight css framework. There are two way to utilise this framework. The first one, add Pure to our project
 via the free unpkg CDN server, just add a HTML link element into Head, like that:
```html
<link rel="stylesheet" href="https://unpkg.com/purecss@1.0.0/build/pure-min.css" integrity="sha384-nn4HPE8lTHyVtfCBi5yW9d20FjT8BJwUXyWZT9InLYax14RDjBj46LmSztkmNP9w" crossorigin="anonymous">
```
The second one is download Pure file, then put into our Website project root directory or any folder to reference.
The Purecss supply a few of style, Layouts, Forms even Customize style and so on.
We can refer to [https://purecss.io]('https://purecss.io')

## Lab 2.4: Responsive - web for mobiles

I have followed the instruction to open my git pages on gitlab of BIT. And also could visit my pages. The url address is:
[http://wangh21.pages.op-bit.nz/checkpoints-repo/](http://wangh21.pages.op-bit.nz/checkpoints-repo/)
This pages default page is index.html which is before lab I made it. When I visit it on my cellphone, the width , and the 
layout has occur a lot of mistakes. Because I did not considering the mutip browser and mutip terminal size. Especially some 
complicated page layout including text, picture and video.
1. I should add the code to each page:

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```
2. I could not set up the width, height and font size to how many piexs, I should set up to relative width, height and font size.
3. All block have to accord float style.

So, that is why the CSS Framework has been occurred. Because they solved these problems. I should utilise some CSS framework to
sove my page display problems.

About the defference version of IE browser not compatible, there are some code could solve it.
```html
<!--[if lte IE 8]>
    <link rel="stylesheet" href="https://unpkg.com/purecss@1.0.0/build/grids-responsive-old-ie-min.css">
<![endif]-->
<!--[if gt IE 8]><!-->
    <link rel="stylesheet" href="https://unpkg.com/purecss@1.0.0/build/grids-responsive-min.css">
<!--<![endif]-->
```

About git pages, I have already used github pages. I put my domain here, just use a jekyll templete to write some blog or
development diary like this.
[Aemon's GitPage](https://www.aemon.wang)

## Checkpoint 2
Firstly, I put my checkpoint2 page url here. [aemooooon's checkpoint 2](http://wangh21.pages.op-bit.nz/checkpoints-repo/checkpoint2index.html)

Secondly, I just know that this checkpoint was open for 13:00 pm today. So I only have less more 4 hours to do this. It is Very nervous on time. So that is why I chose a sort of CSS framework which is named purecss. It could save my time. I will write a few decision in the process of my development below:
* I used CDN server CSS resource to link my html page.

```html
<link rel="stylesheet" href="https://unpkg.com/purecss@1.0.0/build/pure-min.css" integrity="sha384-nn4HPE8lTHyVtfCBi5yW9d20FjT8BJwUXyWZT9InLYax14RDjBj46LmSztkmNP9w" crossorigin="anonymous">
```
* In order to give priority to display mode mobile phone users, I added this html code：

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```
* In order to make the old and new versions of IE browser compatible with each other, I added this code;

```html
    <!--[if lte IE 8]>
        <link rel="stylesheet" href="https://unpkg.com/purecss@1.0.0/build/grids-responsive-old-ie-min.css">
    <![endif]-->
    <!--[if gt IE 8]><!-->
        <link rel="stylesheet" href="https://unpkg.com/purecss@1.0.0/build/grids-responsive-min.css">
    <!--<![endif]-->
            <!--[if lte IE 8]>
            <link rel="stylesheet" href="styles/pricing-old-ie.css">
        <![endif]-->
        <!--[if gt IE 8]><!-->
            <link rel="stylesheet" href="styles/pricing.css">
        <!--<![endif]-->
```

In this case, the pricing.css is layout css file, I stored it under my styles folder.
        
* Because I do not have very much time, so I just copy our school website (op.ac.nz) content and picture. So all content, picture and link copy rights belong to Otago Polytechnic. I just use for study and practise web1 checkpoint.
* About navigation, I place it on the top of left next to logo picture. When user open this Index home page, first look the logo, and then could look the navigation, it is Very conspicuous.
* About layout, color, scale and so on, I just use the CSS framework to provide the base element, then according to my self requirment to modify it. That is benefits of CSS Framework.
* Once again, in my all page, all hyper link to connection the op.ac.nz all content. 
* If I got one more time, I think I could do it better. Just my fault, because I did not check the course Modules.