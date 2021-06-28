# Lesson 10: Final Project

<!-- TOC -->

- [Lesson 10: Final Project](#lesson-10-final-project)
    - [Overview](#overview)
        - [Data sources](#data-sources)
    - [Two options](#two-options)
        - [Static map option](#static-map-option)
        - [Embedded interactive CARTO/Mapbox map option](#embedded-interactive-cartomapbox-map-option)
    - [Create a new repository](#create-a-new-repository)
        - [Templates](#templates)
        - [Examples](#examples)
    - [Enable GitHub Pages](#enable-github-pages)
    - [Invite your instructor as a Collaborator](#invite-your-instructor-as-a-collaborator)
    - [Deliverables and deadlines](#deliverables-and-deadlines)

<!-- /TOC -->

## Overview

Welcome to your final project. The assignment is to make a compelling map that addresses a topic of your choice. The requirements are minimal, but your submission must be a web page that includes either a static map as PNG or an embedded CARTO/Mapbox map. You will create a new repository for this project, publish it via GitHub Pages, and make your instructor a collaborator.

### Data sources

If you do not have data, consider perusing some [existing data resources and portals](https://github.com/rgdonohue/resources) collected by one of our professors at NMP. Often, a good dataset can drive inspiration and help you focus on telling a story, rather than trying to fix subpar data. Try to get your data early in the assignment, so you have plenty of time to map and analyze it.


## Two options

Your client has requested a web page showing the map. The map can either be static map or as an embedded CARTO or Mapbox map.

Whichever option you select your map should be symbolized with proper color schemes, be organized, neat, and have a meaningful title, and an appropriate legend. Please review previous labs to ensure you make a complete map.

Since your client is requesting a web page, both options should include information about the source of data, author, date of publication, and a brief description of your goals and methods of map making. Place this information in the content of your web page. The web page footer should contain your links to your snazzy social media footprint.

Use the previous labs to find an appropriate _index.html_ as a template for this web page. Feel free to explore changing your _index.html_ style and layout. Try to be creative and your instructor will help guide you.


### Static map option

* Map image format should be a PNG or JPG.
* Map needs to be in two resolutions: 1) width of 1,200 px and 2) width of 8,000 px
* Web page and/or should include information about the projection, e.g., what is the EPSG SRID?

### Embedded interactive CARTO/Mapbox map option

* Map needs to be an `iframe` element in the web page.
* A link should be provided to full-screen version.
* A CARTO map should have an informative popup; A Mapbox map should display different features at different scales.

## Create a new repository

Create a new repository on your personal GitHub account. Give the title of the repository a concise, meaningful name. For instance, if I'm going to map mines in Colorado, I would name the repository "colorado-mines" (no spaces!).

![Creating a new GitHub repository](images/10-new-repo-on-github.png)  
*Creating a new GitHub repository*

 Keep this repository public so your instructor and fellow classmates can offer help.  Click the box to include a README.md when you initially create the repository and include a license as well (GNU General Public License v3.0 is excellent). For example:

![Adding a public repository](images/git-new-repo.png)  
*Adding a public repository*

Make sure your web page is titled "index.html" and located in the root of your repo.

### Templates

Look in the [templates](templates) folder for starter HTML that you can add into your `index.html` page. You are free to modify these templates or create an entirely new design.

### Examples

Let's say you want to wanted to explore tornado history in the US from this dataset: http://www.spc.noaa.gov/gis/svrgis/. You can upload the data to Mapbox or make a beautiful static map in QGIS. Your repository name could be "us-tornado-map" and in that repo you would alter the _index.html_ to add your PNG or embed the interactive map.

We have started a "map of maps"; a map of New Maps Plus final projects. This will give you an idea of what other students have made in 671 and 672. The link is https://newmapsplus.github.io/projects/ and you will contribute to this map, as well!


## Enable GitHub Pages

[GitHub Pages](https://pages.github.com/) allows you to serve a repository as a web site. After you enable it, the URL for your page will be *https://username.github.io/repo-name*. First, access your new repo's settings.


![Access new repo settings](images/github-pages-0.png)  
*Access new repo settings*

Scroll down to the *GitHub Pages* section and enable it on the **master branch**.

![Enable GitHub Pages](images/github-pages-1.png)  
*Enable GitHub Pages*

## Invite your instructor as a Collaborator

Because this is your repository, you have control over who can collaborate. While still in your GitHub repo settings, find the **Collaborators** button.

![xample of adding a repo collaborator](images/github-settings.png)
*Example of adding a repo collaborator*

Type your instructors GitHub username in the search field. When you find it, click **Add collaborator**. (Look on Canvas for your instructors username.)


## Deliverables and deadlines

1. **Project setup** (2 pt)

    Send me an invitation to collaborate in your repository by Friday. Make sure your repository has a `readme.md` that includes your project title and links to potential data sources. This information of course can change, I just want to see that you are working on your final project.


3. **Submit draft** (6 pt)

    Submit a draft version of your map by end of day on Sunday. Submit the repo URL to Canvas.

2. **Add and submit project metadata** (2 pt)

    When you are finished with your project create a `publish.json` file. This supports sharing your work with the world and controlling what information you present in a marker popup. This metadata file will help make a map [similar to this map](https://newmapsplus.github.io/projects/).

    The template file [can be found here](templates/publish.json) and it must be placed in the root directory of your repository. Before you alter this file, look at the following properties that you need to change:

     ```js
    {
    // Required properties
    "title": "Title of Project", // Give your project a good title
    "info": "Add info about project", // A short blurb about your project
    "coordinates": [38, -84.5], // IMPORTANT: the lat, long centerpoint of your project

    // Optional properties
    // If you don't want to use these, use the value null without quotes.
    "author": "Do you want to add your name?", // What handle do you want to use?
    "link": "http://newmapsplus.uky.edu" // What's the link to the project or your social media?
    }
    ```

    Let's consider an example of a properly formatted `publish.json` file. Note that there are no comments in this version.

    ```js
    {
    "title": "A map of NMP students & alums",
    "info": "View where the NMP mappers live and work!",
    "coordinates": [34.5, -94.5],
    "author": "My GitHub Handle",
    "link": "http://newmapsplus.uky.edu/projects"
    }
    ```

    Post the link to this file in Canvas. The link will have the format, ` https://username.github.io/my-final-project-repo/publish.json`. This must be submitted no later than next Tuesday.
