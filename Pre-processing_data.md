

## Exploring the IMDB data set (from Kaggle)

Objective : to explore, clean and extract the relevant data that we are intested in.. 

- The total number of movies in data : 5044 (df.index)

- The number of movies with gross earnings value over 0 :  df[df.gross > 0] ( 4159 )
- The number of movies with NaN gross earnings  :  df[df.gross.isnull()] . ( 884 )
- The number of movies with budget value  : df[df.budget > 0]  ( 4551 )
- The number of movies with gross earnings & budget value  ? :  df[df.gross > 0][df.budget > 0]  ( 3891 )

- The number of non-english language movies (including NaN) : df[df.language != ‘English’]  ( 339 ) 
- The number of non-english language movies  :  df[df.language == 'English']  ( 4704 )

- The number of entries with any NaN values : df.dropna(how='any’) ( 3756 )
- The number of entries with rating ==  NaN : df[df.content_rating.isnull()]  ( 51 )


 - Describe the data :  df.describe()
 - List features of interest : df.loc[:,['movie_title','director_name','gross','budget']]
 
 ## Content Rating
 
 Unique values : df.content_rating.unique()

  array(['PG-13', 'PG', 'G', 'R', 'Approved', 'NC-17', nan, 'X', 'Not Rated',
       'Unrated', 'M', 'GP', 'Passed'], dtype=object)
       
Rating System changed over the years, doc : https://en.wikipedia.org/wiki/Motion_Picture_Association_of_America_film_rating_system

See also : https://contribute.imdb.com/updates/guide/certificates

& TV guidelines : https://en.wikipedia.org/wiki/TV_Parental_Guidelines



 #Groupings :
   - G & Approved & Passed
   - PG  & GP & M 
   - PG-13
   - R & TV-MA
   - NC-17 & X
