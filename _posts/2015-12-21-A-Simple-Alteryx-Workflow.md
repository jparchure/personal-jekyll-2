---
layout: post
section-type: post
title: A Simple Alteryx Workflow
author: Jay
---


So, I've been working with this amazing data blending and analytics tool called <a href="http://www.alteryx.com">Alteryx</a>.
It allows you to develop easy workflows for repeatable data pre-processing and analytics needs.<br>
As a data analyst, there are many instances when you have a certain of set of actions to perform, everytime any new data is brought to your knowledge.
It could be as simple as renaming a file, to convert it to another format, perform statistical tests or connect to another tool such as Tableau.
So, today as I began a new data science project using <a href="https://dandelion.eu/datamine/open-big-data/">this</a> open big data set from Telecom Italia, I discovered that the data files did not have headers.
Naturally one likes to have an idea of what exactly does the data represent. So, I looked it up and sure enough there did exist the metadata for the set online, but it was neither as a metadata file, nor added in the dataset. Now I could ofcourse write a script to do it, but what if my client wanted to do it themselves with no programming background?
<i>Alteryx to the rescue!</i>
<br>
I'll cut the chase and get to the solution.
<br>
Here are the steps to add a header to all of your files using Alteryx-
<ol>
<li>Create an empty folder called "Data_With_Headers", copy its location on your file system.</li>
<li>Create a csv file name header_data that contains the column headers for your file</li>
<li>Open Alteryx</li>
<li>On the toolbar above, you see a bunch of icons in different colors. These are <b>tools</b> and can be thought of as mini-functions or available operators</li>
<li>Drag the <b>Input Data</b> tool to the white space (called canvas) </li>
<li>On the left hand pane, Enter the path to the folder where your data files are located. End the path location with <b> '\*' </b>(without quotes)</li>
Note: This assumes all your data files are of same type and reside in the same folder.
<li> In the Options panel, select "Output File Name as Field" and from the dropdown, choose "File Name Only" </li>
<li>Now, In the search bar near the top left, search for the <b>Dynamic Rename Tool</b>. Select it and drag it to the canvas </li>
<li>You'll notice there are two small marks named <b>L</b> and <b>R</b> on this tool. The L connects to the Input tool and R is currently empty</li>
<li> Drag and Drop another Input Data tool to the canvas and connect it to R by clicking on its end and drawing a line to R of the Dynamic Rename Tool</li>
<li> As we did earlier, enter the path to your metadata csv file. After this, click on the Dynamic Rename tool again </li>
<li> In the panel on the left, Select "Take Field Names from Right Input Metadata". This tells Alteryx to use the R input as a metadata</li>
<li> Drag and drop the <b>Output Data </b> tool from the toolbar above to the whitespace and link it with the right hand side mark of the Dynamic Rename Tool </li>
<li> Similar to the input tools, specify a file name for the Output tool, this should point to your <i> Data_With_Headers </i> folder from Step 1, ending with /.csv (or your desired file format) </li>
<li>From the File Menu, selecte <b> Tools -> Run Workflow </b> or press Ctrl + R </li>
The Workflow is now executing. Once it's finished you'll have a new set of files with headers on them. If you do not wish to maintain multiple copies of your files, you can simply specify the same folder in Steps 6 and 14 in order to overwrite your files.
In order to reuse this workflow, simply save it. Now you can specify your folder and metadata and get files with headers for all your future needs.<br>
Hope this was useful to you. If you have any questions, feel free to send me a message on the Contact Page.<br>
Best<br>
J


</ol>
