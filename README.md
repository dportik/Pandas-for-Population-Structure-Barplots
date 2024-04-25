# Pandas-for-Population-Structure-Barplots

![BarPlot](https://github.com/dportik/Pandas-for-Population-Structure-Barplots/blob/main/data/outputs/Admixture-K4-Perfection.png)

---------------

## Summary

Making publication-quality figures of stacked barplots from population clustering analyses can be rather difficult. There are many options available, but the learning curve is often steep. Here I demonstrate how to use Python & Pandas in a Jupyter notebook to quickly summarize and plot your population structure results. 

This tutorial assumes you have used the program [Admixture](https://dalexander.github.io/admixture/) to estimate population structure. This program requires a `ped` input format, and outputs a `P` and `Q` file per run. To use this notebook, you will need the `ped` input file and a corresponding `Q` output file. You can use a `Q` file for any K-value you selected. **NOTE:** You can also use results from [STRUCTURE](https://web.stanford.edu/group/pritchardlab/structure.html), but see the FAQ for more details. 

Example data used for this notebook are provided in the `/data/inputs` folder. They were generated using the [admixture-wrapper](https://github.com/dportik/admixture-wrapper) script, which automates runs over a set of K-values. For this analysis, I used the best replicate outputs for K = 4.


## Usage

To see a rendered version of the Jupyter notebook, please click [**here**](http://htmlpreview.github.io/?https://github.com/dportik/Pandas-for-Population-Structure-Barplots/blob/master/Pandas-for-Population-Structure-Barplots.html), or download `Population-Structure-Barplots.html` and open it in a web-browser.

The `Pandas-for-Population-Structure-Barplots.ipynb` can be used to analyze your own data. To do this, download the notebook and start a Jupyter notebook session (e.g., `jupyter notebook`), then activate this notebook. You can edit the paths to your own data and run the notebook to make the figures. Please note that some figure settings may need to be changed to fit your dataset, and there are instructions on how to do this for each plot.

**Notebook requirements:**
+ python 3.7+
+ pandas
+ seaborn

## FAQ

+ **Can I use files from Structure analyses instead?**

Yes! The `ped` file is only used to obtain the sample names. If you have run Structure analyses, you will need to provide a suitable replacement for the `ped` file. This can simply be a list of the sample names (one per line, in same order used for analysis). Given the way the code is written, it is best to include two columns in this substitute file (second column can contain any type of information; it isn't used in the analysis). 

+ **Should I cite this notebook?**

That is not required, but if you have found this tutorial helpful for your work you can always provide a link to the github repo in your manuscript. This will help point other researchers to this open-access resource, which was the goal for creating it. 

+ **It's not working for me!**

Please open an issue here and describe the error. It will help if you can provide your input files, which can assist with replicating the problem. 

## License

GNU Lesser General Public License v3.0


