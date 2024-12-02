---
layout: post
title: "Streamlit App"
description: "Somthing here."
image: "/assets/img/IMG_2060.JPG"
--- 

### Introduction

### Movie Dataset
The dataset that this streamlit app uses comes from the [TMBD API](https://developer.themoviedb.org/docs/getting-started). I also go over how to gather data using this API in another blog post which can be found [here.](https://laurenscarzella.github.io/my-blog/blog/api/) The cleaned version of this movie dataset can be found in my [GitHub repository](https://github.com/laurenscarzella/my-api) named "cleaned_movies.csv". The final dataset contains information about movies such as:

| Variable          | Info                                   | Type     |
|-------------------|----------------------------------------|----------|
| title             | title of movie                         | string   |
| adult             | TRUE or FALSE for adult content        | boolean  |
| id                | movie id                               | int      |
| original_language | original language of movie             | string   |
| popularity        | popularity score of movie              | float    |
| release_date      | date movie was/is going to be released | date     |
| vote_count        | number of votes for this movie         | int      |
| vote_average      | average rating for movie               | float    |
| primary_genre     | primary genre the movie is from        | string   |

### Motivating Question
On average, which genres are most popular?

### Key Insights
**Code:** All of my code for this section is in a file named "EDA.ipynb" which can be found [here.](https://github.com/laurenscarzella/my-api/blob/main/EDA.ipynb)

**1. Summary Statistics:** This gives us a breif overview of the movie dataset.

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/summary_stats.png)

**2. Bar Chart of Top Movie Genres:** This helps us answer our motivating question. We can better understand the relationship between genres and average popularity, and see how much average popularity varies across genres. This plot is interactive so you can see the exact average popularity scores by hovering over a genre.

<iframe src="{{site.url}}/{{site.baseurl}}/assets/img/interactive_plot1.html" width="100%" height="600px" frameborder="0"></iframe>

As you can see, the top five movie genres by average popularity score are Science Fiction, Animation, Action, Horror, and Fantasy.  

### Streamlit App
What if you want to interact with this dataset yourself? Well, you can! Creating a streamlit app enables users to interact with data and possibly discover insights beyond those discussed in this blog post.

Explain what users can do with this app

Provide examples of how users can explore the data to gain additional insights

### Conclusion

