---
layout: post
title: "Exploring Movie Trends with a Streamlit App"
description: "This blog post showcases a Streamlit app I created to explore movie data. With interactive visualizations and customizable filters, users can analyze trends, discover top movies, and the popularity of genres over time. This app makes data exploration more intuitive and engaging."
image: "/assets/img/IMG_2060.JPG"
--- 

### Introduction
Analyzing data can be intimidating, especially if you don't have coding experience. With so much information available, how do you uncover meaningful insights? That's where my [Streamlit app](https://movie-app-kpg7e6zlbgkfo9wwk8w5as.streamlit.app/) comes in. It makes exploring movie data easy and intuitive. This app is designed for users of all skill levels who want to uncover patterns and trends without writing a single line of code. Plus, it goes beyond what's covered in this blog post, allowing you to discover insights of your own!

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

### Results
**Code:** All of my code for this section is in a file named "EDA.ipynb" which can be found [here.](https://github.com/laurenscarzella/my-api/blob/main/EDA.ipynb)

**1. Summary Statistics:** This gives us a breif overview of the movie dataset.

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/summary_stats.png)

**2. Bar Chart of Top Movie Genres:** This helps us answer our motivating question. We can better understand the relationship between genres and average popularity, and see how much average popularity varies across genres. This plot is interactive so you can see the exact average popularity scores by hovering over a genre.

<iframe src="{{site.url}}/{{site.baseurl}}/assets/img/interactive_plot1.html" width="100%" height="600px" frameborder="0"></iframe>

As you can see, the top five movie genres by average popularity score are Science Fiction, Animation, Action, Horror, and Fantasy.  

### Streamlit App
What other valuable insights can we learn from this dataset? Some questions that we can investigate are: What are the most popular movie titles for each genre? What is the average popularity of each genre over time? How many movies come from each genre for a specific year? Answering these questions would be a lot eaiser if you could interact with the data yourself. With the streamlit app that I created, you can easily interact with the data and explore these questions yourself! Click [this link](https://movie-app-kpg7e6zlbgkfo9wwk8w5as.streamlit.app/) to view the app and follow along.

**Code:** The code used to create this streamlit app can be found in my [GitHub repository](https://github.com/laurenscarzella/movie-streamlit) called "movie_app.py".

**Purpose:** Creating a streamlit app enables users to interact with data and uncover insights beyond those discussed in this blog post.

**Usage:** There are three tabs that you can switch between to help users focus on one aspect of the data. These include Top Movies, Trend Analysis, and Movies Released by Genre. The data is also customizable with various filters such as sliders, radios, and select boxes.

### View Top Movies
Filter movies by release year and genre, and view the top 10, 20, 30, 40, or 50 most popular movies based on their popularity score.

<figure>
	<img src="{{site.url}}/{{site.baseurl}}/assets/img/top.png" alt=""> 
	<figcaption>Figure 1: Bar chart showing the top 10 movies by popularity score, filtered by release year (1902-2000) and genre (Science Fiction).</figcaption>
</figure>

### Analyze Genre Trends
Explore how the popularity scores of movie genres has changed over the years. This can help users understand popularity shifts in genres over time.

<figure>
	<img src="{{site.url}}/{{site.baseurl}}/assets/img/trend.png" alt=""> 
	<figcaption>Figure 2: Line chart of the average popularity of movies filtered by release year (1902-2027) and genre (Comedy).</figcaption>
</figure>

### Explore Movie Counts by Genre
Check out the number of movies released in a given year for each genre. This provides us with some insight of the focus of the movie industry for each year.

<figure>
	<img src="{{site.url}}/{{site.baseurl}}/assets/img/genre_table.png" alt=""> 
	<figcaption>Figure 3: Table showing the count of each movie genre for a specified year (2024).</figcaption>
</figure>

### Customizable Filters
Users can adjust filters like year and genre to tailor thier analysis to specific time frames or interests.

### Unique Interactive Elements Include:

### 1. Input Widgets

**Select Box:** Users can select specific genres, allowing them to filter the data to focus on their genre of choice. This widget allows for personalization of the data exploration experience.

**Slider:** The slider enables users to select a specific year or range of years for filtering movie data. This makes it easier to explore trends over a specified year range.

**Radio:** This is used to select between 10, 20, 30, 40, or 50 top movies based on thier popularity scores.

### 2. Expanders

**Data Table Expander:** For users that want to see the data behind the charts, the app includes an expandable section where they can view the filterred datasets. This allows for transparency in the data that is displayed and for deeper inspection.

### 3. Tabs

**Multiple Tabs:** The app is organized into different sections, allowing the user to switch between viewing top movies, trend analysis, and movie counts by genre. This helps users focus on one aspect of the data at a time and avoid feeling overwhelmed.

### 4. Interactive Charts

The app uses Plotly to create interactive bar charts, line charts, and tables. These visualizations are clickable which helps the user dive deeper into specific data points or elements of a visualization.

### Conclusion
With a little coding experience, we can answer simple research questions effectively. However, tools like Streamlit make data analysis more accessible and engaging for everyone because it does not require any advanced coding skills. This blog post only demonstrated a glimpse of what's possible. There is so much more that we can uncover about the movie industry.

What will you discover as you explore this dataset? Challenge yourself to dive in, analyze, and share your findings!