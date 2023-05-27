# Exploring-TMBD-movies
We will investigate the TMDB movie dataset. This dataset contains information about 10,000 movies in the period 
from 1960 to 2015 collected from The Movie Database (TMDb),including user ratings,revenue,budget,genres,runtime,popularity. 
We will ivestigate this dataset to answer some questions:

   1 --> What is the average budget and revenue of movies at this period?
   2 --> What is the highest rating movie and who is its director?
   3 --> Does budget affect revenue over time??
   4 --> Do genres affect revenue?
   5 --> Does runtime affect revenue over time?
   6 --> Does vote affect revenue?
   
   Limitations
I couldn't find the correlation between the popularity and revenue and i couldn't specify the values that don't makke sense 
in the popularity column,so we have to konw what is the minimum value of popularity that makes sence and 
how was the popularity values calculated? and to find the crrelation between it and revenue it must be calculated based on ticket sales.
I also found NaN values in both genres and directro columns and because the number of NaN values in them is small 
i removed all rows with NaN values using `df.dropna()
I also found one duplicated row and i removed it using `df,drop_duplicates()
I also found some values that don't makes sense in each of budget,revenue and runtime columns like [0, 1, 2, 16 ] in budget 
and revenue columns and values like [1, 0, 20, 30, 800, 950] in runtime column so i decided that take the minimum value 
that make sense in budget and revenue columns is 1,000,000 and the min and max values that make sense in runtime column 
are 60, 300 respectively and replace the values that are not the specific range with NaN.
