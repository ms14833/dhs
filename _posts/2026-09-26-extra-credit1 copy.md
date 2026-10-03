---

title: "Assignment #1"
date: 2026-10-03
tags:
- Assignment

---

## Event information

* **Event:** Introduction to R


* **Date:** Friday, September 25, 2026


* **Time:** 10:00 p.m.-12:00 a.m. 


* **Location:** Online through Zoom


* **Organizer:** [NYU Libraries Data Services](https://guides.nyu.edu/dataservices)


So, to preface this reflection, the Intro to R workshop was a two-hour online session offered by NYU Libraries Data Services. Its purpose was to introduce the basic elements of R, including things like how to work with datasets, create visualizations, and perform common statistical procedures. Before this workshop, I mostly associated the words "data analysis" as something complex that I couldn't grasp without a CS background. The session changed my mindset by breaking down the fundamentals of R in simpler, more digestible parts. What were some of these parts it covered?

## Main ideas from Workshop

Well, to start with, the workshop began with the four main areas of RStudio: the source editor, console, environment, and files/plots/help pane. To put it in a summarized manner, the source editor saves code, the console executes commands, the environment shows loaded objects, and then the final pane provides files, visualizations, packages, etc..

We also got a recommendation to preferably always work in a saved script rather than only in the console. This stood out to me as a good note to remember, since it preserves the analytical process such that anyone can revisit it (i.e, to correct a mistake, or show someone how I produced a result). Also, RStudio Projects supports this same goal by keeping code, data, and outputs together and using relative file paths that remain usable when a project folder is moved or shared.

The next major section we had covered the building blocks of R. For instance, values can be stored as named objects or combined into vectors, and also organized into data frames. To go deeper, a vector is a sequence of values, while a data frame resembles a table with observations in rows and variables in columns. There were also some exercises that covered summary functions, variable types, and creating columns. The main shift from a typical spreadsheet I noted down is that the user describes a transformation to apply consistently to an entire variable instead of editing cells individually as you do in Excel or Sheets.

Another interesting topic was missing data. R represents missing values as NA, and a calculation can return NA unless your code explains how those observations should be handled. For example, adding na.rm = TRUE is a way for you to tell a function to exclude missing values from that calculation without deleting them from the original dataset. It was overall a useful reminder that missing information is something researchers have to notice and make a deliberate choice about how to treat it, since choosing to just ignore incomplete records could change a conclusion.

![Using the Pipe with Base R](/dhs/assets/images/r-pipe-bmi.png)

*Figure 1. The native R pipe changes a nested BMI calculation into a readable sequence of steps. Screenshot from the NYU Data Services Introduction to R materials, Denis Rubin et al., 2026.*

The pipe operator, written as `|>`, was also a very memorable concept. It passes the result of one step into the next step, so the code can be read from left to right as "and then." The workshop compared the pipe to a morning routine: like you wake up, shower, get dressed, eat breakfast, and leave the house. In data analysis, the same structure might mean selecting a column, calculating its mean, and rounding the result. This is a clearer way to do it rather than placing many functions inside one another, and it makes it easier to check for errors.

The workshop then applied this logic to the NHANES dataset using tools from the tidyverse. Functions such as rename(), mutate(), filter(), select(), etc. each perform a distinct task. They can (non-exhaustive list of things I noted): rename variables, compute new values, retain relevant observations, choose columns, and also sort results. There was a good example of this in action that asked for the five heaviest adult men while displaying only ID, age, and weight. The solution was to translate the question into four clear operations: filter the rows, sort weight from highest to lowest, select three columns, and retain the first five records. I liked this example and mention it here because it showed how a question can be broken down into a logical sequence of data-processing steps.

![Challenge: Putting it all together](/dhs/assets/images/r-nhanes-filter.png)

*Figure 2. A sequence of filter(), arrange(), select(), and head() operations answers a specific question from the NHANES data. Screenshot from the NYU Data Services Introduction to R materials, Denis Rubin et al., 2026.*

The later sections then moved from preparing data to interpreting it. R can generate a lot of descriptive statistics such as the mean, median, standard deviation, quartiles, and missing-value count. It can also create frequency tables and cross-tabulations for categorical variables. The workshop then introduced ggplot2, which builds a visualization layer by layer. The user first identifies the dataset and maps variables to axes, then adds a geometry such as a boxplot or histogram, and finally adds colors, labels, facets, and a theme. Thus, each visual choice you make determines how patterns and other important stories behind data appear.

![Human Growth and Shrinkage Across the Lifespan](/dhs/assets/images/r-ggplot2-growth.png)

*Figure 3. Layered ggplot2 code creates boxplots of height across age decades and adds clear labels and formatting. Screenshot from the NYU Data Services Introduction to R materials, Denis Rubin et al., 2026.*

The visualization examples made that fact clear. When we did a height histogram for all adults, it appeared unusually broad, but adding color or separate facets for gender revealed groups that would've been hidden in the combined view. Lastly, the final section extended the workflow to t-tests, chi-square tests, ANOVA, and linear regression. Good to remember: the broom package can turn complicated statistical output into tidy tables that are easier to review and report.

## Connection to DHS Class

The workshop connects to our class since a major aspect of the course involves taking data about places and turning it into maps or other visual material that can communicate something meaningful. So, the R workshop helped me better understand what happens BEFORE that final visualization is produced, including aspects like how a dataset can be cleaned, reorganized, filtered, and checked. These skills are useful when working with larger sets of spatial information, where it's not practical to inspect every observation manually.

The session also connected to our discussions about how maps and datasets are not completely neutral representations of the world. The course focuses on why some places are mapped more fully than others, how reliable open-source mapping data can be, and how maps may carry forward existing biases. The choices made in R (such as which observations to include, how to divide information into categories, and how to display the results) sort of relate to that, in the sense that they can similarly affect the argument that the final map or visualization makes. Learning the technical process therefore also made it easier to see where human judgment exactly can enter into data-based work.

## Application to my studies

As a senior majoring in Business but not sure about my Capstone idea yet, I can see R supporting my capstone in whatever it may be. No matter if my capstone involves surveys, market research, consumer behavior, etc., it will be a heavyweight tool that can help me a lot with any sort of quantitative data. I could do common things I inevitably will need to do in my capstone regardless of the idea; things like cleaning responses, comparing groups, testing relationships, and creating consistent visualizations. Also, a saved script would let me update the analysis when new data arrived instead of rebuilding spreadsheet work every time.

In my future beyond my capstone and university, the most valuable lesson may be reproducibility. Businesses usually make decisions using large, imperfect datasets, and analysts must explain their methods to colleagues. Readable pipes, documented transformations, summary statistics, and clear graphics can make that process more transparent. I am of course not leaving the workshop as an R expert, but I now understand its basic workflow and now can expand my knowledge to be able to use R in both my capstone and my future workplace.

```

```