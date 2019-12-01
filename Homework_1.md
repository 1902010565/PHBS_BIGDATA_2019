# Homework 1
Mariia Semenenko

#### 1. Big Data problem

We are going to use the big data datasets from [IMDB website](http://www.imdb.com/interfaces). There are 7 datasets in total, 6 of them contain information for each unique title and 1 - for each unique name of the person.

Which insight could we get using this data?

Our goal will be - to identify relationship between average movie rating and such parameters as number of votes, runtime of the movie, its release year. This information is contained in the different datasets, that is why it is practical to use databases approach in this case.

The types of the files are tsv, which means, that our data is in the tabular structure.

#### 2. Data properties

Three main defining properties of big data are volume, variety and velocity.

*Volume* of the data is quite big, which makes it impossible to analyze the data using simple tools such as Excel, and makes database approach even more relevant. At the same time, comparing to the volume of the data, that is created by social media, volume of the films database is quite moderate.

*Variety*, which refers to the number of types of data is not very high. Types of the variables include numerical variable integer, text variable string, date variable in YYYY format, boolean data type, arrays of different types of data. The data is very well classified, which makes the analysis of it easier.

*Velocity* - the speed, with which the data is being generated. Velocity of IMDB data is again not very high, comparing to the velocity of the data of social media networks, or for instance, news websites.

#### 3. Workflow to solve the problem

I. ETL - extraction, transformation, loading. The data is already extracted and transformation applied, so at this point we just need to load the data.

II. Normalization. Now we will organize the data by mapping it, in other words, establishing relationships between tables. Our next step is - to reduce. We remove redundancies by leaving only the parameters we need for the analysis, such as: title, number of votes, average movie rating, movie runtime, release year of the movie.

III. Data cleaning and transformation. Treating missing values, checking if the data is stored in the correct format.

IV. Data processing and visualization. Now we can easily compute new parameters which will help us to identify the dependencies between variables and answer the questions we set in the beginning, solving big data problem this way.

#### 4. Type of the database to be used

Our data is in the structured format, which makes it a subject to relational databases. In our case, the key value, which allows us to establish the connection between different IMDB databases is title of the movie.

One of the most popular relational open-source database is MySQL, which is suggested to be used within this big data problem. There are certain reason and advantages for using MySQL:

* a big amount of documentation and tools available
* high performance. MySQL holds a reputation of a fast database solution
* security. It has reliable database management system, which allows to grant access privileges on a user-by-user basis, define a password for the root user, remove anonymous accounts. At the same time, in this specific case security of the data is not a priority, since the IMDB data is available to any user.
