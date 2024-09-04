## Lab 2 Overview

The entire lab will be worth 20 points. 


### 1. R Style and debugging (10 points)
The code and output below are designed to create a figure from the titantic dataset. Update the code - so it works- follow the style guide and comment your code.

Please include a bullet point summary of what you changed and why. Note this first code chunk has the option `eval = F` which means it is not currently evaluated.

```{r, eval = F, message = F}
THEDATA=read_csv(http://math.montana.edu/ahoegh/teaching/stat408/datasets/titanic.csv)

titanic 
  %>% filter(!is.na(Age)) %>% # removed passengers without age
  mutate(Pclass = factor(Pclass)) %>% # changed class to factor
  ggplot(y = Age, x = Pclass)) %>%
  geom_boxplot(outlier.shape = NA) %>%
  geom_jitter(color = Sex) +
  theme_bw() + 
  xlab(Passenger Class) +
  ggtitle('Passenger age by class and gender on Titanic') +
  facet_wrap(Sex~.)
```


### 2. Data Structures / Subsetting (5 points)

Use in line R code to answer these questions with complete sentences. As an example you can call r variables using backticks, then r, then your r command. For example to print the current time, we can use `Sys.time()` so that it is currently `r Sys.time()`.

### a. 
How old is the 747th passenger in the dataset?

### b. 
How old is the oldest passenger in the dataset?

### c.

Who is the oldest passenger in the dataset?


### d. 
What percentage of 3rd class males survived (Leonardo DiCaprio as Jack)?


### e. 
What percentage of 1st class females survived (Kate Winslet as Rose).

### 3. Writing data out of R (5 points)

We've seen how to use the `tibble()` function to create a dataframe. Another option is `tribble()` which allows us to specify the rows, rather than columns. See the documentation for `tribble()` [https://tibble.tidyverse.org/reference/tribble.html](https://tibble.tidyverse.org/reference/tribble.html) and create a tibble with three columns and as many rows as you have group members. The first column contains the names of the group members, the second contains the group member's hometown, and the final contains the group member's favorite season. Print out this data frame.

