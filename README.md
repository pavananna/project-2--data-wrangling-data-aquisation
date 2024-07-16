# project-2--data-wrangling-data-aquisation
Performing operations on data set.

1) Importing the dataset:

      a) to import the data set first we have to import pandas.
      b) now by using read_csv we have to import he data set by giving the path in pd.read_csv.

2) Dropping unnecessary columns:

      a) if we observe carefully in the dataset1  and dataset3 the 'yr' and 'mnth' columns these vaules are already 
          mentioned in the dteday so we can remove these columns because all the vaules of this column are already mentioned.
      b) for the second dataset2 the column 'unnamed:0' it is look like index column we have already 'instant' column with 
          the index vaules so we can remove 'unnamed:0', we cannot remove instant column because the same column is there in 
          the another datset which will be useful for merging the data sets so we remove the 'unnamed:0'.
3) Merging the datasets:

   a) for merging the datasets we have to use the merge method , now first we have merge the dataset1 and dataset2 , and 
       also we have to use 'on' which what is the common column to  merge the datasets in the dataset1 and dataset2 
       'instant' is the common column and also we have to use 'how'which  means how to join we have to use that is 'outer', 
       outer join is used to join dataset1 and dataset2 and common column one time.
   b) Now we have to merge the new_dataset with the dataset3 by using the concat method .

4) Identifying the unique vaules:
    a) for identify the unique vaules we have to use the unique keyword , we can find the unique vaules for the particular 
        column so we find the unique or causual, registerd, count.

5) Checking the data types for the dataset:
     a) for checking the dimmensions for the dtaset we have to use 'dtypes' method which is used for getting the data type 
        for each column.

6) Checking the dimmension of the dataset:
     a) by using the shape mehod we can know how many rows and columns the dataset contain.

7) Getting the statstical information about the dataset:
   a) to get the statstical information about the dataset we use the 'describe' method ,which will give the minimum, maximum 
      , 25%,50% ,75%, standerd devation of the each column.
   b) we can use 'info()', which gives the information about how many different data types, what is the memory usage, and 
      null vaules arethere are not in each column it will give information about all these.

8) Handling missing vaules:
   a) for handiling the missing vaules first we have to find the missing vaules to find the we have to use 'isnull','sum'
      method it will give the total number of null vaules that each row contain.
   b) after doing the above step we have found that 'atemp' has 11 missing values so we have to update the vaules for that
      we have display the entire row of the only missing values.
   c) After that,first take one missing row,and put 'atemp' column vaule  aside , take the remaning vaules in the row and 
     check whether the same vaules are there in any another row if there means take the mode (most freqent vaule) and 
     replace the vaule with he 'NAN' of the particular row.
   d) if the vaules are not there in any another row means put 'humdity' column aside and checking with the remaning 
      vaules,like that we hve to fill the missing vaules.
   e) after filling the missing vaules now chack any null vaules are there are not by using 'isnul','sum()'.

9) Finding the outliers:
   a) to find the outliers first we have to import the 'seaborn' as sns, and theb import the numpy as well for finding the   
      Q1,Q2,Q3.
   b) take the numeric colums like 'temp''atemp','humdity',;wind speed' as numeric_columns and draw the boxplot by using the 
      sns.boxplot.
   c) to remove the outlier define the upper_limit, lower_limit and replace the outlier values with the 
      upper_limit,lower_limit, now agan draw the outliers now outliers will be removed and again diaplay dataset.
   
