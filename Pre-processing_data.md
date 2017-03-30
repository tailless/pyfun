

## Exploring the IMDB data set (from Kaggle)

Objective : to explore, clean and extract the relevant data that we are intested in.. 

- The total number of movies in data : 5044 (df.index)

- The number of movies with gross earnings value over 0  :  4159 ( df[df.gross > 0] )
- The number of movies with NaN gross earnings  :   df[df.gross.isnull()] == 884
- The number of movies with budget value  : 4551 (df[df.budget > 0] )
- The number of movies with gross earnings & budget value  ? :  3891 ( df[df.gross > 0][df.budget > 0] )

- number of non-english language movies (including NaN) : 339  (df[df.language != ‘English’]) 
- number of non-english language movies  : 4704 ( df[df.language == 'English'] )

- number of entries with any NaN values : 3756 (df.dropna(how='any’))
- number of entries with rating ==  NaN :  51  df[df.content_rating.isnull()]
