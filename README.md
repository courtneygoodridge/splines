**splines**

**Disclaimer**: *This is a working repository and so information and code may change*

**Overview**

Splines are a way of analysing non-linear data (i.e.,very wiggly data). In this repository, I use Richard McElreath's tutorial on splines in his book, *Statistical Rethinking* and apply this to analyse to pupil diameter over time. Unfortunately the data is not available to share at this time. This is outside of my control. However, I can explain what the data is and how it was generated. 

The data used is pupil diameter over time collected during a driving simulator experiment. In the experiment, participants experienced automated driving for approximately 2 minutes. During automated driving, drivers either monitored the vehicle and road environment, or they are completed a cognitively loading task. After the 2 minutes of automated, a critical takeover situation occured (a lead vehicle decelerated with a time to collision of either 3 s or 5 s). The data used in this tutorial focuses on pupil diameter from the point at which the critical takeover happens, and the following manual driving period. A general research questions might be how does pupil diameter change during the takeover scenario, and whether the criticality of the event, or completing a cognitive task during the automation, impacts pupil diameter. 

The main script is: `splines_for_pupil_timecourse.Rmd`. In this script, I first use splines to model the average pupil diameter over time. I am then planning on implementing an analysis to compare pupil diameter timecourse between differing conditions. 

**Application**

Whilst this data here focuses on pupil diameter (i.e., physiological data), the analysis method is very useful for a range of different data types. Splines are often used in Economics to find pattens and trends over time.


