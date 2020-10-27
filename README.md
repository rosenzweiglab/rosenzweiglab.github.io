# Rosenzweig lab page

This is repository for [Rosenzweig lab](http://rosenzweiglab.com) that we cloned and modified from [Kordinglab.com](http://kordinglab.com/). We use Jekyll to run our Github page.

## Run the page locally using Jekyll

Unless you are going to make major changes, you do not need to download and run jekyll on your computer. All the files can be modified on github. If you are going to make major changes, it may also be worthwhile forking this repo first...

- **Directly edit on Github**, you can simply go to `_posts` and click `New file` then put some markdown file e.g. `2016-02-03-post-name.md` and start writing blog post. Github also allows you to preview it so it's nice for people who don't want to clone the repo.

- **Clone the repository**, kind of the same as directly add post on Github. You just have to clone the repository. Then add new post file, commit and push to the repo.

The changes will take approximately half a minute to render. You can see the new posts or changes on [rosenzweiglab.com](http://rosenzweiglab.github.io/)!

## Editing the lab website

Below, we explain how to edit the lab webpage


### Add yourself

You can add yourself to the page in `_people` folder just create file name `<firstname>_<lastname>.md` in the folder. We require few line of header before you start writing your own page. See the following for the header

``` markdown
---
name: 
position: 
avatar: (do not forget to add file type at the end)
twitter: 
email: 
googlescholar: 
orcid: 
website: 
linkedin:
joined: (year)

---
```

If you don't have information, just leave it blank. The avatar will bring photo from `images/people` folder and display it on people page.
For lab position, you can choose position from 4 classes including `postdoc`, `phd`, `masters`,`nonthesis`,`visiting`, `others, `alumni`. Position will put you into section that you choose.

If changing to alumni, you must also update the people.md file in main folder. 

### Add new publications

Publications can be added in bibtex format into references.bib (Google Scholar allows new publications to be exported in BibteX format and this can be edited into references.bib file in docs folder). This page uses bibbase.org to generate the publication list, which is generated from url https://raw.githubusercontent.com/rosenzweiglab/rosenzweiglab.github.io/master/docs/references.bib   

### Add news

We currently do not have a news page. This can be set up at a later stage. 

### Add posts 

We currently do not have posts, but operate more on a "Research Interests" basis. 
Other pages can be set up and linked to different places if desired. 

<From Kordinglab>
<<It's very easy to add post. All the posts are located in `_posts` folder. It arrangement is based on
date. Each post can be written in markdown format. You just have to state headers before writing: `title`, `description` and `categories`. `description` will be shown when you share on social media like Facebook or twitter. See the following headers:

``` markdown
---
title: Summer School in Computational Sensory-Motor Neuroscience (CoSMo)
description: all links to CoSMo summer school in computational neuroscience materials
categories: scientists
---
```

We have 4 categories: `scientists`, `students`, `discussion`, `blog` you can choose and this will be rendered to different location.

---
>>
