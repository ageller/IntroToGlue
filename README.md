# IntroToGlue
Workshop introducing the Glue visualization package

## Description

## Outline

### Installation

The easiest installation method is to download the standalone executable file from the glue website.  [See here for instructions.](https://glueviz.readthedocs.io/en/stable/installation/standalone.html)  However, this version will not allow you to load in maps.  So I recommend installing Glue with python, and, specifically, I recommend [installing using the Anaconda Python distribution](https://glueviz.readthedocs.io/en/stable/installation/conda.html). 

After installing Anaconda, you can either install glue via the Ananconda Navigator GUI, or you can install glue with the following commands.  (I've found that the order of these installation commands is important; please follow the order below.)  In either case, I recommend creating a new conda environment for glue.


```
$ conda create -n glueviz-env python=3.9
$ conda activate glueviz-env
$ conda install -c glueviz glueviz=1.2
$ conda install -c conda-forge rasterio
$ conda install -c conda-forge pyproj
$ conda install -c glueviz glue-geospatial 
$ conda install -c glueviz glue-plotly
```

### Launching Glue

If you downloaded the standalone executable for Glue, you can launch it by double clicking.  If you installed Glue with the Anaconda and prefer to use the Navigator GUI, you should have a panel on your home screen marked as Glue that you can click on.  If you installed Glue through python on the command line, you can launch Glue by typing.

```
$ glue
```

### Loading data into Glue

With Glue open, you can drag any data set (e.g., a .csv file) into the main Glue window to load the data into Glue.  Alternatively, you can click on the "Import Data" button at the top of the app.  Once you have loaded the data into Glue, you should see it on the left-hand side of the app within the "Data" menu under "Data Collection". You can load multiple data sets into Glue, and have access to all of them within the "Data" menu.  If you double click on a data set, you can change the color, label and default point size.

Let's start by loading in any of the .csv files from the data/ directory on this repo.  Additionally, if you have installed the glue-geospatial addon (see above), you may want to load in the [ChicagoGeoTIFF.tif](https://github.com/ageller/IntroToGlue/blob/main/data/ChicagoGeoTIFF.tif) map file.

### Creating plots from data in Glue

Once your data is loaded into Glue, you can can create a plot by clicking on the data object within the "Data" menu and dragging it into the main window.  This should bring up a dialogue box that asks what kind of plot you want to create (e.g., 2D scatter, histogram, etc.).  After you select the type of plot, it will appear in the main window of the app.  You can create multiple plots of the same data set, and also create plots using different data sets, all within the same tab on the app.  

At the top of each plot window, there are buttons to allow you to manipulate the plot.  If you hover over these buttons, you will see what they do.  Probably the most useful buttons are those for selections (red dots with blue regions).  

On the left panel of Glue, you will also see the the "Plot Layers" and "Plot Options" boxes have been populated.  Use the "Plot Layers" section to control the color, opacity and other characteristics of the figure.  Use the "Plot Options" section to change the data that is being plotting, the axes limits, etc.  

Create a variety of plots from the .csv file(s) that you loaded into Glue and explore all the different plotting options.

### Making selections on data within Glue plots

At the top of each plot window there are various ways to select data on your plot (these buttons have red dots with blue regions).  If you click on one of those buttons and the click+drag across your plot to define a region, you will create a new subset of your data.  This subset will appear in the "Plot Layers" panel on the left side of the app.  You can now create additional plots showing only this subset by dragging the data set into the main window (like you did to create the initial plot).   

At the top of the app, you will see different selection modes (red circles).  Hover over these to see what each refers to, and try them out.

Make a selection on one of your data sets to create a Subset.  Then drag this Subset into the main portion of the app to create a new plot.  Then change the selection mode to intersection, and make a new selection on your Subset.  

### Linking data sets in Glue

If you have data with similar attributes, you can link them together.  For example, multiple data sets in here have latitude, longitude and date attributes.  If we link these together, we can plot multiple datasets (from different files) on top of each other on one figure within Glue.  Go to the "Data Manager" menu and select "Link Data".  This will bring up a new window where you can tell Glue which attribute from one dataset should be linked to an attribute in another dataset.  Select a dataset for "Dataset 1" from the dropdown and select a different dataset for "Dataset 2".  Then within the list of components for each file, select the two attributes that you want to link, and click the "Glue attributes" button below.  

Now for any linked datasets, you can add an additional dataset onto an existing plot by dragging that dataset directly onto that plot (as opposed to onto the main window).  One example where this works well is plotting geographical data (e.g., those with latitudes and longitudes) on top of a map.  If you installed the glue-geospatial plugin, plot some data on top of the map.  Otherwise, link together two datasets from .csv files that have date columns and plot those on top of each other. 

Make selections on your new combined plot, and notice that this selection will be populated on other plots where these datasets are visible. 

### Exporting plots and data from Glue

**Plots:** You can export plots from Glue by clicking on the disk symbol within a given plot window.  This will give you the option to download a png ("Save plot to file") or to download a python script that would reproduce the plot.  (If you installed the glue-plotly -- which should come with the standalone executable --, you should also see an option to download to as a Plotly HTML page; this is an experimental feature and does not always work :(

**Data:** You can export data to a file (e.g., .csv file) by clicking on the "Export Data/Subsets" button in the top bar of the Glue app.  This will bring up a dialog box that has a dropdown for you to select the dataset, subset, and attributes to save.  You also have a few options for file types to download to.  This may be particularly useful to download a subset that you created by some complex manual selection on a dataset.

**Session:** You can also save your session so that you can start up where you left off after closing glue.  To do so, you can click on the "Export Session" button in the top bar of the app.  Then you will be free to close your Glue session without losing your work.  *A word of warning*: I have seen that these sessions can be version dependent.  In other words, if you save a Glue session using on version of Glue, you may not be able to open it with another version of Glue (e.g., one that you may upgrade to in the future).  I'm also not sure how well these session behave across different operating systems.  Also, various plot customizations (e.g., axes labels) do not appear to save.
