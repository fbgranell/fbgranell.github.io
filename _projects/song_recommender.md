---
layout: page
title: Spotify Song Recommender
description: This system classifies +90.000 songs and recommends a similar record to the one given.
img: assets/img/p1_main.jpg
importance: 1
category: Work
---
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/p1_header.png" title="Spotiy Song Recommender" class="img-fluid rounded " %}
    </div>
</div>

<div id="table-of-contents">
  <p>Table of Contents:</p>
<ul>
  <li><a href="#section1">Introduction.</a></li>
  <li><a href="#section2">Materials and Methods.</a></li>
  <li><a href="#section3">Results.</a></li>
  <li><a href="#section4">References.</a></li>
  <li><a href="#section5">License.</a></li>

</ul></div>



<a id='section1'></a>
### Introduction

In this project, I am working as a data analyst for a multicultural website. I have been tasked with utilizing machine learning to build a song recommender system. By leveraging unsupervised learning techniques, we were able to cluster over 90,000 songs based on their audio features. This system operates in two ways: 1) if the input song is currently in the top-100 charts, the recommender will suggest a similar song from the same artist or genre from within the top-100; 2) if the input song is not in the top-100 charts, the recommender will obtain its audio features and suggest a similar song from the same cluster. The ultimate goal is to provide users with personalized song recommendations.

You can check the code <a href="https://github.com/fbgr/spotify-recommender">here</a>.

<a id='section2'></a>
### Materials and Methods
In order to provide a comprehensive analysis of the music landscape, we took a methodical approach by extracting data from multiple countries TOP-100 song charts and utilizing web scraping to identify unique songs. Additionally, we extracted audio features from Spotify's API, including parameters such as danceability, energy, key, loudness, mode, speechiness, acousticness, instrumentalness, liveness, valence, and tempo.

 The dataset was constructed by scanning huge playlists, including (<a href="https://open.spotify.com/playlist/1638KZlvcvyyEJ15S8erge">Greatest Hits 2020/2022</a>,
<a href="https://open.spotify.com/playlist/6Pi3jayiuzwmA5i6tLtIap">Greatest Hits 2010/2019</a>,
<a href="https://open.spotify.com/playlist/6FKDzNYZ8IW1pvYVF4zUN2">Longest Playlist Ever</a>). We extracted all songs from albums that appeared at least once, regardless of presence within the playlists themselves. This approach allows us to present a more diverse and well-rounded representation of the music industry.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/p1_songrec_3.png" title="Greatest Hits 2020/2022" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/p1_songrec_4.png" title="Longest playlist ever" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/p1_songrec_5.png" title="Greatest Hits 2010/2019" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The methods of this study include the followings:
* Webscrapping
* Use of Spotify's API
* Data wrangling
* ML: Unsupervised Learning
* Hyperparameter optimization
* Data visualization

<a id='section3'></a>
### Results

The results of our song recommender system indicate that the model is functioning as expected in terms of recommending similar songs to the input given. This is evident from the following examples:

<center><table>
    <tr>
        <td><b>Input</b></td>
        <td></td>
        <td><b>Recommendation</b></td>
    </tr>
    <tr>
        <td>Ribs (by Lorde)</td>
        <td>&nbsp;&nbsp;&nbsp;&nbsp;→&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</td>
        <td>Isabel (by The Wombats)</td>
    </tr>
    <tr>
        <td>Listzomania (by  Phoenix)</td>
        <td>&nbsp;&nbsp;&nbsp;&nbsp;→&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</td>
        <td>Out of Reach (by The Primitives)</td>
    </tr>
    <tr>
        <td>After Midnight (by  Blink-182)</td>
        <td>&nbsp;&nbsp;&nbsp;&nbsp;→&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</td>
        <td>Scribble (by Puppet, Eden Project)</td>
    </tr>
    <tr>
        <td>La Persona (by Amaia)</td>
        <td>&nbsp;&nbsp;&nbsp;&nbsp;→&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</td>
        <td>It's Love (by Kina Grannis)</td>
    </tr>
</table></center><br>
However, it is important to note that musical taste is a highly subjective matter and can vary greatly from person to person. Despite this, our model was able to effectively cluster songs based on their audio features and make meaningful recommendations.

<a id='section4'></a>
### References
The TOP-100 song charts were taken from the <a href="https://www.popvortex.com/music/">PopVortex</a> website. The data and audio features for all songs were obtained through the use of Spotify's API.

<a id='section5'></a>
### License
This is an educational project; therefore, all materials can be used freelly.
