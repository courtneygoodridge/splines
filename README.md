# Splines

**Disclaimer**: *This is a working repository and so information and code may change*

## Overview: splines and data 

Splines are a way of analysing non-linear data (i.e.,very wiggly data). In this repository, I use Richard McElreath's tutorial on splines in his book, *Statistical Rethinking* and apply this to analyse to pupil diameter over time. Unfortunately the data is not available to share at this time. This is outside of my control. However, I can explain what the data is and how it was generated. 

The data used is pupil diameter over time collected during a driving simulator experiment. In the experiment, participants experienced automated driving for approximately 2 minutes. During automated driving, drivers either monitored the vehicle and road environment, or they are completed a cognitively loading task. The presence of the cognitive task is indicated via the variable `n_back` being `TRUE` or `FALSE`. N-back is a very common cognitive task in Human Factors research. Drivers are presented with a string of numbers and have to recall the number "n" back from the number they have just heard. In this experiment, n = 2. 

After the 2 minutes of automated, a critical takeover situation occured (a lead vehicle decelerated with a time to collision of either 3 s or 5 s) and the automated vehicle indicated to the driver that a takeover required. The data used in this tutorial focuses on pupil diameter from the point at which the critical takeover happens, and the following manual driving period after the driver had taken over. A general research question might be: "how does pupil diameter change during the takeover scenario?". Or more specifically, does completing N-back during automation and the criticality of the event impract how pupil diameter changes during a takeover situation?  

## Code and analysis
# Statistical modelling 

The main script is: `splines_for_pupil_timecourse.Rmd`. In this script, I first use splines to model the average pupil diameter over time. Here is an example of average pupil diameter over time for one condition:

![image](https://github.com/courtneygoodridge/splines/assets/44811378/704128f8-c73a-4833-81b4-a7d8a2901bfe)

And here is an example of the model fit plotted over the data. The predicted pupil diameter is plotted with confidence intervals. It highlights the increase in pupil diameter at approximately  5 s after the start of the critical takeover. This could be due to the increased arousal of having to deal with a critical situation. It would be due to the visual looming of the car ahead (pupils dilate when looking at things closer to us). 

![image](https://github.com/courtneygoodridge/splines/assets/44811378/af56c25a-7a8a-4ff4-b697-ab3bf0d30463)

I am then planning on implementing an analysis to compare pupil diameter timecourse between differing conditions. 

The `Plots` folder contains plots from the analysis script. 

## Application

Whilst this data here focuses on pupil diameter (i.e., physiological data), the analysis method is very useful for a range of different data types. Splines are often used in Economics to find pattens and trends over time.


