---
layout: workshop
title: "NEON Working With Hyperspectral Imagery in HDF5 Format (R)"
estimatedTime: 3.0 Hours
packagesLibraries: RHDF5, DPLYR
date:   2015-06-08 20:49:52
dateCreated:   2015-2-23 10:49:52
lastModified: 2015-06-09 17:11:52
authors: Leah A. Wasser
tags: [Data-Workshops]
mainTag: Data-Workshops
description: "This workshop introduces remote sensing hyperspectral imagery. We will review the background of the data, how to open it in R and how to perform basic raster calculations. We will also explore raster data in R."
code1: 
image:
  feature: hierarchy_folder_purple.png
  credit: Colin Williams NEON, Inc.
  creditlink: http://www.neoninc.org
permalink: /Data-Workshops/NEON-HDF5-HyperspectralImagery-In-R
comments: true 
---

###A NEON Data Carpentry Workshop

**Date:** Spring 2015

This workshop will providing hands on experience with working with hyperspectral imagery in hierarchical data formats(HDF5), in R. It will also cover raster data analysis in R.

<div id="objectives">

<h3>Goals / Objectives</h3>
After completing this workshop, you will:
<ol>
<li>Know what the hyperspectral remote sensing data are</li>
<li>Know how to create and read from HDF5 files containing spatial data in R.</li>
<li>Know they key attributes of raster data that you need to spatially locate raster data in R.</li>
</ol>

<h4>Things to do, before the workshop:</h4>

<h3>Data to Download</h3>
<a href="http://neonhighered.org/Data/HDF5/SJER_140123_chip.h5" class="btn btn-success"> 
DOWNLOAD the NEON Imaging Spectrometer Data (HDF5) Format</a>. 
<p>The data in this HDF5 file were collected over the San Joachim field site 
located in California (NEON Domain 17) and processed at NEON headquarters. The 
entire dataset can be accessed <a href="http://neoninc.org/data-resources/get-data/airborne-data" target="_blank">by request from the NEON website.</a>
</p>  

<h3>R Libraries to Install</h3>
<ul>
<li>rhdf5: <code>source("http://bioconductor.org/biocLite.R") ;
biocLite("rhdf5")</code></li>
<li>raster: <code>install.packages('raster')</code></li>
<li>rgdal: <code>install.packages('rgdal')</code></li>
</ul>

<h3>Background Materials to Read</h3>
<ul>
<li><a href="{{ site.baseurl }}/GIS-Spatial-Data/Working-With-Rasters/">Working with Rasters in Non Gui Tools.</a></li>
<li><a href="{{ site.baseurl }}/R/Raster-Data-In-R/">The basics of raster data in R.</a></li>
<li><a href="{{ site.baseurl }}/HDF5/About-Hyperspectral-Remote-Sensing-Data/">The basics of hyperspectral
remote sensing data.</a></li>
</ul>

</div>

##Please also watch this video prior to the workshop

<iframe width="560" height="315" src="https://www.youtube.com/embed/3iaFzafWJQE?rel=0" frameborder="0" allowfullscreen></iframe>

##SCHEDULE


| Time        | Topic         | Instructor | 
|-------------|---------------|------------|
| 12:00     | [Raster Data in R - the skinny]({{ site.baseurl }}/R/Raster-Data-In-R/ "What is HDF5")      |            |
| 12:30 | [About Hyperspectral Remote Sensing Data]({{ site.baseurl }}/HDF5/About-Hyperspectral-Remote-Sensing-Data/ "What is HDF5")          |      |
| 1:00 | [Working with Hyperspectral Remote Sensing Data in R - P1]({{ site.baseurl }}/HDF5/Imaging-Spectroscopy-HDF5-In-R/ "What is HDF5")        |          |
| 2:30 | [Raster Stacks in R - Working with Hyperspectral Remote Sensing Data]({{ site.baseurl }}/HDF5/Create-Raster-Stack-Spectroscopy-HDF5-In-R/ "What is HDF5")          |      |


##Setup

To participate in the workshop, you will need working copies of the software described below. Please make sure to install everything (or at least to download the installers) before the start of the workshop.

#HDFView

Hierarchical Data Format 5 (HDF5) is a file format used to store, package, and simultaneously organize large quantities of related data. Although we will use R to analyze data stored in this format, HDFView is free-ware that allows for quick and easy viewing and editing of these files.


#R

<a href = "http://cran.r-project.org/">R</a> is a programming language that specializes in statistical computing. It is a powerful tool for exploratory data analysis. To interact with R, we recommend, but do not require, <a href="http://www.rstudio.com/">RStudio</a>, an interactive development environment (IDE). 

## R Packages to Install
We will use several packages, including 

* <a href = "http://www.bioconductor.org/packages/release/bioc/vignettes/rhdf5/inst/doc/rhdf5.pdf">rhdf5</a> 
* <a href = "http://cran.r-project.org/web/packages/rgdal/rgdal.pdf">gdal</a>
* others?? 

DOWNLOAD 

1. The package installation script <a href="https://github.com/NEONdps/neonESA2014/blob/master/packageInstallation.R">here</a>, 
2. The <a href = "http://trac.osgeo.org/gdal/wiki/DownloadingGdalBinaries">gdal</a> libraries, and 
3. The <a href = "http://www.hdfgroup.org/HDF5/release/obtain5.html">hdf5</a> libraries. 

#Optional resources

##QGIS

 <a href ="http://www.qgis.org/en/site/forusers/index.html#download" target="_blank">QGIS</a> is a cross-platform Open Source Geographic Information system.
 


##Online LiDAR Data Viewer (las viewer)

[http://plas.io](http://plas.io) is a Open Source LiDAR data viewer developed by Martin Isenberg of Las Tools and several of his colleagues.
