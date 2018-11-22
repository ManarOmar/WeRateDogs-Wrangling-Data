WeRateDogs Wrangle Report

Data wrangling is a core skill that everyone who works with data should be familiar with since so much of the world's data isn't clean. the process of the data is divided into three steps:
1.Gathering data.
2.assessing data.
3.cleaning data.

Gather

Gathering data is the first step in data wrangling. Before gathering, we have no data, and after it, we do. my gathering efforts are divided into three steps:
1.Getting data from an existing file: I have a flat file twitter_archive_enhanced.csv which is a comma separated value, that I pointed on it,then clicked and downloaded it, then I read it in a Pandas dataframe.
2.Downloading a file from the internet: I have a link to a flat file on the internet, I downloaded it programmatically using the requests library.
3.Querying an API :After my application to have an account as a developer on Twitter was approved, I query the twitter API for each tweet in the twitter archive file using tweepy library (likes count,retweets count, tweet user name, and the user favorited ), and I stored it in a list of dictionary. and I guaged the time for the query from the twitter API. then I dumped it to tweet_json.txt file, that I used it then to load these data directly to the jupyter notebook using json library.

Assess

After gathering the data, the next step is assessing it visually and programmatically to detect the quality (content issues) and tidiness issues(structural issues).from the visual assessment I assessed many observations like the existance of retweets tweets, the structure of the dog stage in the dataset, and the sex of the dog was noticed in the text of tweet.

In the programmatic assessment, I used the info function for each dataframe to assess the null values for each variable, and see the data types for it, I counted values of many variables and showed the statistical description for all data, the most quality validity and accuracy issues are in the twitter archive data like the name, numerator rating, and denominator rating, and a consistency issue was in the names of breeds. then assessing the Tidiness issues was depends on tidy data requirements:
Each variable forms a column.
Each observation forms a row.
Each type of observational unit forms a table.

Cleaning

Cleaning the data is the third step in wrangling data, and it is a process of fixing tidiness and quality issues, to make sure that it is accurate and correct, and then being able to analyze our data correctly, the first step in cleaning data is making a copy of each dataframe,All of the cleaning operations will be conducted on this copy so you can still view the original dirty and/or messy dataset later.then fixing the tidiness issues is the second step, and then the quality issues. the pandas library has a lot of functions to fix all of the issues in the data, the main process in the cleaning data was Define, Code, Test process.

Conclusion

So our wrangling process let the data easy access and analysis using these steps:
1.Gathering data: obtaining data and importing that data into a programming environment.
2.assessing data: assess data for quality and tidiness issues.
3.cleaning data: defined cleaning tasks, convert those definitions to code,test the dataset, visually or with code
