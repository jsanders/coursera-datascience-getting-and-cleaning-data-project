# Tidied Data from the Human Activity Recognition Using Smartphones Dataset

A few steps were taken to transform the initial data set. The test and train sets have were merged and the subject identifiers and activity labels were pulled in to create a single data set. The activity identifiers were translated from identifiers into human-readable names. Only the mean and standard deviation variables were kept. Those variables were further summarized by taking their mean for each subject/activity pair. The data is in "wide" format as described by [Wickham](http://vita.had.co.nz/papers/tidy-data.pdf); there is a single row for each subject/activity pair, and a single column for each measurement.

The final data set can be found in the `tidyMeans.txt` file, which can be read into R with `read.table("tidyMeans.txt", header = TRUE)`. A detailed description of the variables can be found in `CodeBook.md`. The basic naming convention is:

  Mean{timeOrFreq}{measurement}{meanOrStd}{XYZ}

Where `timeOrFreq` is either Time or Frequency, indicating whether the measurement comes from the time or frequency domain, `measurement` is one of the original measurement features, `meanOrStd` is either Mean or StdDev, indicating whether the measurement was a mean or standard deviation variable, and `XYZ` is X, Y, or Z, indicating the axis along which the measurement was taken, or nothing, for magnitude measurements.
