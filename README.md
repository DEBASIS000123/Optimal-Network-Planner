# Optimal Network Planner

Optimal Network Planner is a project designed to optimize wireless network coverage by strategically placing nodes based on signal strength (RSSI). Using advanced clustering techniques and path planning algorithms like K-Median clustering and the Traveling Salesman Problem (TSP), the tool identifies key locations (primary nodes) that maximize network strength and coverage. Secondary nodes, which are closely related to primary nodes, are also considered to ensure comprehensive coverage across the target area. The project aims to provide a robust solution for network optimization, ensuring the strongest possible signal across the region while minimizing travel paths for maintenance and setup.

<br />
<p>Before:</p>
<p align="center">
    <img src="https://github.com/DEBASIS000123/Path-Planning-using-UAV/blob/main/photos/Before.jpg" alt="Logo" width="700">
</p>
<br />
<p>After:</p>
<p align="center">
    <img src="https://github.com/DEBASIS000123/Path-Planning-using-UAV/blob/main/photos/After.jpg" alt="Logo" width="700">
</p>
<br />


---


## Data Plotting

| ![Image 1](https://github.com/DEBASIS000123/Path-Planning-using-UAV/blob/main/photos/plot1.jpg) | ![Image 2](https://github.com/DEBASIS000123/Path-Planning-using-UAV/blob/main/photos/plot2.jpg) |
| :---------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------: |
|                                           HeatMap                                           |                                        Scatter Plot                                         |
| ![Image 3](https://github.com/DEBASIS000123/Path-Planning-using-UAV/blob/main/photos/plot3.jpg) | ![Image 4](https://github.com/DEBASIS000123/Path-Planning-using-UAV/blob/main/photos/plot4.jpg) |
|                                       3D Scatter Plot                                       |                                         Graph plot                                          |
---

## Features

A summary of the key features or functionalities of your project.

<b>Clustering Techniques:<b/>  Utilizes Manhattan distance-based clustering and K-median clustering to group data points by signal strength.
Path Planning Algorithms: Implements the Traveling Salesman Problem (TSP) to find the shortest path covering all primary nodes.
Correlation Analysis: Uses a correlation matrix to identify primary and secondary nodes based on RSSI relationships.


---

## Methodology
An overview of the methods and algorithms used in the project, explained in simple terms.

Data Clustering: Raw data with longitude, latitude, and RSSI values is first clustered into smaller groups using Manhattan clustering.
Re-Clustering: These clusters are further refined using K-median clustering to reduce the number of groups and focus on key signal areas.
Correlation Matrix: A 20x20 correlation matrix is created to identify the strength of relationships between clusters, helping to distinguish primary nodes from secondary ones.
Path Optimization: The TSP algorithm is used to find the shortest path that covers all primary nodes, ensuring optimal network strength.

---

## Visualization
Explain how the results are visualized for better understanding and analysis.

Graph and Map Visualization: The shortest path and node locations are plotted on a graph and map, respectively, to visualize coverage areas and optimize planning.
Heatmaps and Network Diagrams: Additional visualizations, such as heatmaps, show signal strength across different areas to identify potential coverage gaps.

---

## Usage
Instructions on how to use the project or implement the algorithms for their use case.

Data Preparation: Input raw data with longitude, latitude, and RSSI values.
Run Clustering: Use the provided scripts to perform clustering and re-clustering on the data.
Analyze Correlation: Generate the correlation matrix to identify primary and secondary nodes.
Find Optimal Path: Apply the TSP algorithm to determine the most efficient path for network coverage.
Visualize Results: Use visualization tools to see the network coverage and path optimization on a map.


---


## Conclusion
Wrap up with a summary of the benefits and potential applications of your project.

Benefits: Optimizes network coverage by minimizing signal drop and ensuring robust performance across targeted areas.
Applications: Useful for network planners, telecom companies, and anyone looking to optimize wireless network infrastructure.

---
## How to Find Primary and secondary nodes?
Make a 20X20 co-relation matrix according to the cluster number for each sub-clusters and the result of co-relation matrix should be calculated according to the avarage RSSI strength of that sub-cluster. Then count the total relation and take the highest as the primary Node and check the relation where the relation is more than 0.3 and store these cluster in to a variable calling secondary Node.
after that clear the primary and secondary Nodes and Do repeat the process again untill the co-relation matrix is 0.

<table>
  <tr>
    <td><img src="https://github.com/DEBASIS000123/Optimal-Network-Planner/blob/main/photos/comatrix.jpg" alt="before" width="300"/></td>
    <td><img src="https://github.com/DEBASIS000123/Optimal-Network-Planner/blob/main/photos/comatrix2.jpg" alt="after" width="300"/></td>
  </tr>
  <tr>
    <td align="center"><strong>Co-relation Matrix</strong></td>
    <td align="center"><strong>After doing 0</strong></td>
  </tr>
</table>

Now secondary Nodes are comming under primary Nodes and if we travel the primary nodes then we can travel secondary nodes as well as primary nodes. 
Here is the primary Node and Secondary Node Lists:<br/><br/>

<img src="https://github.com/DEBASIS000123/Optimal-Network-Planner/blob/main/photos/comatrixresult.jpg" alt="result" width="260"/>
<br/><br /><br />

---

And This is the poltting of the primary nodes and if you take this areas then we can cover all the area with a lower cost. There are only 744 points by which we can travel all the areas.
<br /> <br />
<img src="https://github.com/DEBASIS000123/Optimal-Network-Planner/blob/main/photos/primaryPlot.jpg" alt="result" width="700"/>



## Install Necessary Modules:

Open your [![Anaconda](https://img.shields.io/badge/Anaconda-342B029.svg?&style=flate&logo=anaconda&logoColor=white)](https://www.anaconda.com/products/individual) Prompt <img alt="propmt" src="https://img.shields.io/badge/--000000?style=flat-square&logo=Plex&logoColor=white"> and type and run the following command (individually):

 -       pip install pandas
       
 -       pip install numpy  
  
 -       pip install seaborn
 
 -       pip install matplotlib
     
 -       pip install mpl_toolkits
 
 -       pip install seaborn
 
 -       pip install --upgrade pip
 
 -       pip install networkx

 -       pip install geodesic

 -       pip install pathlib

 -       pip install sklearn

Once Installed now we can import it inside our python code.

---
## Frequently asked questions ❔

### How can I thank you for writing and sharing this tutorial? 🌷

You can <img src="https://img.shields.io/static/v1?label=%E2%AD%90 Star &message=if%20useful&style=style=flat&color=blue" alt="Star Badge"/> and <img src="https://img.shields.io/static/v1?label=%E2%B5%96 Fork &message=if%20useful&style=style=flat&color=blue" alt="Fork Badge"/> Starring and Forking is free for you, but it tells me and other people that it was helpful and you like this tutorial.

Go [here](https://github.com/DEBASIS000123/Path-Planning-using-UAV) if you aren't here already and click ➞ **✰ Star and ⵖ Fork button in the top right corner. You'll be asked to create a GitHub account if you don't already have one.

---

### How can I read this tutorial without an Internet connection? <img alt="GIF" src="https://github.com/TheDudeThatCode/TheDudeThatCode/blob/master/Assets/hmm.gif" width="20vw" />

1. Go [here](https://github.com/DEBASIS000123/Path-Planning-using-UAV) and click the big green ➞ **Code button in the top right of the page, then click ➞ [Download ZIP](https://github.com/DEBASIS000123/Path-Planning-using-UAV).

    <img alt="Download ZIP" src="https://github.com/DEBASIS000123/Path-Planning-using-UAV/blob/main/photos/offline_save.jpg" width="400">
2. Extract the ZIP and open it. Unfortunately I don't have any more specific instructions because how exactly this is done depends on which operating system you run.
    
3. Launch ipython notebook from the folder which contains the notebooks. Open each one of them
  
    Kernel > Restart & Clear Output
    
This will clear all the outputs and now you can understand each statement and learn interactively.

If you have git and you know how to use it, you can also clone the repository instead of downloading a zip and extracting it. An advantage with doing it this way is that you don't need to download the whole tutorial again to get the latest version of it, all you need to do is to pull with git and run ipython notebook again.

---
## Authors ✍

I'm Debasis Mishra and I have written this tutorial. If you think you can add/correct/edit and enhance this tutorial you are most welcome🙏

See [github's contributors page](https://github.com/DEBASIS000123/Optimal-Network-Planner) for details.

If you have trouble with this tutorial please tell me about it by [Create an issue on GitHub](https://github.com/DEBASIS000123/Optimal-Network-Planner/issues/new). and I'll make this tutorial better. This is probably the best choice if you had trouble following the tutorial, and something in it should be explained better. You will be asked to create a GitHub account if you don't already have one.

If you like this tutorial, please [give it a ⭐ star](https://github.com/DEBASIS000123/Optimal-Network-Planner).

---
## Licence 📜

MIT License

Copyright (c) 2024 DEBASIS MISHRA

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

<p><a href="https://github.com/DEBASIS000123/Optimal-Network-Planner/blob/main/LICENSE">Check Here.</a></p>


---

<div align="center">
<h3> Connect with me<a href="https://github.com/DEBASIS000123"><img src="https://github.com/milaan9/milaan9/blob/main/Handshake.gif" width="50px"></a>
</h3> 
<p align="center">
    <a href="https://www.linkedin.com/in/debasis-mishra-579bb226a/" target="_blank"><img alt="LinkedIn" width="25px" src="https://github.com/TheDudeThatCode/TheDudeThatCode/blob/master/Assets/Linkedin.svg"></a>
    <a href="https://www.instagram.com/debasis__mishra_?igsh=aWJqczJ6MnRld2kz" target="_blank"><img alt="Instagram" width="25px" src="https://github.com/TheDudeThatCode/TheDudeThatCode/blob/master/Assets/Instagram.svg"></a>
    <a href="https://www.facebook.com/debasis.mishra.160" target="blank"><img alt="Facebook" width="25px" src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b8/2021_Facebook_icon.svg/1024px-2021_Facebook_icon.svg.png?20220821121039"></a>
    <a href="mailto:debasismishra000123@gmail.com" target="_blank"><img alt="Gmail" width="25px" src="https://github.com/TheDudeThatCode/TheDudeThatCode/blob/master/Assets/Gmail.svg"></a> 
</p>
