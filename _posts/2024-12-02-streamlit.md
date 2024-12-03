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
**Purpose:** What if you want to interact with this dataset yourself? Well, you can! Creating a streamlit app enables users to interact with data and possibly uncover insights beyond those discussed in this blog post.

**Usage:** With this app, users can:

**-View Top Movies:** Filter movies by release year and genre, and view the top 10, 20, 30, 40, or 50 most popular movies based on their popularity score.

**-Analyze Genre Trends:** Explore how the popularity scores of movie genres has changed over the years. This can help users understand popularity shifts in genres over time.

**-Explore Movie Counts by Genre:** Check the number of movies released in a given year in each genre. This provides us with some insight as to the focus of the movie industry for each year.

**-Customize Filters:** Users can adjust filters like year and genre to tailor thier analysis to specific time frames or interests.

### Unique Interactive Elements Included

**1. Input Widgets:** 

**-Select Box:** Users can select specific genres, allowing them to filter the data to focus on their genre of choice. This widget allows for personalization of the data exploration experience.

**-Slider:** The slider enables users to select a specific year or range of years for filtering movie data. This makes it easier to explore trends over a specified year range.

**-Radio:** This is used to select between 10, 20, 30, 40, or 50 top movies based on thier popularity scores.

**2. Expanders:**

**-Data Table Expander:** For users that want to see the data behind the charts, the app includes an expandable section where they can view the filterred datasets. This allows for transparency in the data that is displayed and for deeper inspection.

**3. Tabs:**

**-Multiple Tabs:** The app is organized into different sections, allowing the user to switch between viewing top movies, trend analysis, and movie counts by genre. This helps users focus on one aspect of the data at a time and avoid feeling overwhelmed.

**4. Interactive Charts:** The app uses Plotly to create interactive bar charts, line charts, and tables. These visualizations are clickable which helps the user dive deeper into specific data points or elements of a visualization.

**Further Research:** Provide examples of how users can explore the data to gain additional insights

### Conclusion

