# Installation

* R

* Go to Rstudio.com

  



# Quick guide to RStudio interface



```R

print("Greetings")
variable <- 9

# Vector
v1 <- 1:10

# matrix
m1 <- matrix(v1,nrow=2,byrow= TRUE)


```





## History

For search the scrips history





## Create scripts

* Click on "+" icon



## Run script

* Click on "Run" button or use Ctrl + Return
* To run the entire script, this should be saved and then click on "Source" button
  * This executes the entire R file





## Output



## Files

* Shows the files $ folders in your workspace
* If you want to set a default working directory
  * Session -> Set Working directory





# Packages

* Comprehensive R Archive Network (CRAN)

* Enable to increase the functionality of R



### **Installing libraries directly in console**

```R
install.packages("ggplot2")
install.packages("tidyr")
```



### If you don't know what kind of packages need



**CRAN List of packages by Name**

* https://cran.r-project.org/web/packages/available_packages_by_name.html



**CRAN list of packages by subject area**

* https://cran.r-project.org/web/views/



**Got to R bloggers**

* https://www.r-bloggers.com





# Libraries

## Tidyverse

https://www.tidyverse.org

R packages for data science

The tidyverse is an opinionated [collection of R packages](https://www.tidyverse.org/packages) designed for data science. All packages share an underlying design philosophy, grammar, and data structures.

Install the complete tidyverse with:

```
install.packages("tidyverse")
```



## dplryr

url: https://dplyr.tidyverse.org

dplyr is a grammar of data manipulation, providing a consistent set of verbs that help you solve the most common data manipulation challenges:

- `mutate()` adds new variables that are functions of existing variables
- `select()` picks variables based on their names.
- `filter()` picks cases based on their values.
- `summarise()` reduces multiple values down to a single summary.
- `arrange()` changes the ordering of the rows.

These all combine naturally with `group_by()` which allows you to perform any operation “by group”. You can learn more about them in `vignette("dplyr")`. As well as these single-table verbs, dplyr also provides a variety of two-table verbs, which you can learn about in `vignette("two-table")`.

If you are new to dplyr, the best place to start is the [data transformation chapter](https://r4ds.had.co.nz/transform.html) in R for data science.





## tidyr

url: https://tidyr.tidyverse.org

The goal of tidyr is to help you create **tidy data**. Tidy data is data where:

1. Every column is variable.
2. Every row is an observation.
3. Every cell is a single value.

Tidy data describes a standard way of storing data that is used wherever possible throughout the [tidyverse](https://www.tidyverse.org/). If you ensure that your data is tidy, you’ll spend less time fighting with the tools and more time working on your analysis. Learn more about tidy data in `vignette("tidy-data")`.



## Shiny

Shiny is an R package that makes it easy to build interactive web apps straight from R. You can host standalone apps on a webpage or embed them in [R Markdown](http://rmarkdown.rstudio.com/) documents or build [dashboards](http://rstudio.github.io/shinydashboard/). You can also extend your Shiny apps with [CSS themes](http://rstudio.github.io/shinythemes/), [htmlwidgets](http://www.htmlwidgets.org/), and JavaScript [actions](https://github.com/daattali/shinyjs/blob/master/README.md).



# Read files



## CSV

data < - read.csv ("file.csv")

## Excel

Usin the library readxl
data < - read.excel ("file.xlsx")
data < - read.xlsx ("file.xlsx")

## txt

Using the library readxl

```R
data <- read.delum(file="file.txt", sep"/t")
```



## Read as table

```R
data <-read.table(file="file.txt")
```



# Building blocks of R

## Creating an object R



### **Use R console**

```R
[Workspace loaded from R/Scripts/.RData]

> 1+2
[1] 3
> 8*9
[1] 72
> 98/13
[1] 7.538462
> 123-47
[1] 76
> 3+3*7-1
[1] 23
> 12:42
 [1] 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42
> 
```



### **Use R to** 

* Analyze time series data
* Tackle spatial distribution
* Create mixed statistical models



### **Buildings blocks** of R

Objects are created through functions

* **Objects**
  * named data structures that store data
  * Objects names: call the data stored in an object
  * Can be: a single digit, a character, a Boolean, a data frame, a list of data frames, etc.
  * Naming objects
    * Small letters, dots and underscores
      * longer.name
      * longer_name
      * longerName



```r
# object name <- value (number)

bob <- 7

bob*2

# Output
[1] 14

# # object name <- value (vector)
> a <- 1:10
> print(a)
 [1]  1  2  3  4  5  6  7  8  9 10
> a*2
 [1]  2  4  6  8 10 12 14 16 18 20
```



* **Functions**



R is case-sensitive

* Match the casing when calling objects and functions

  

## Data types in R

**Data types**

* Vector: a sequence of data elements that are of the same type
* is.vector(data): checks if an object is a vector; returns TRUE or FALSE



```r
> a <- 1:10
> print(a)
 [1]  1  2  3  4  5  6  7  8  9 10
> is.vector(a)
[1] TRUE
```



In contrast to other programming languages like C and java in R, the variables are not declared as some data type. The variables are assigned with R-Objects and the data type of the R-object becomes the data type of the variable. There are many types of R-objects. The frequently used ones are −

- Vectors
- Lists
- Matrices
- Arrays
- Factors
- Data Frames



- **Vectors** (one dimensional array): can hold numeric, character or logical values. The elements in a vector all have the same data type.
- **Matrices** (two dimensional array): can hold numeric, character or logical values. The elements in a matrix all have the same data type.
- **Data frames** (two-dimensional objects): can hold numeric, character or logical values. Within a column all elements have the same data type, but different columns can be of different data type.



### **Types of vectors**

The simplest of these objects is the **vector object** and there are six data types of these atomic vectors, also termed as six classes of vectors. The other R-Objects are built upon the atomic vectors.

* **integer:** whole numbers, with nothing after the decimal point
  * 2L, 34L, 0L
* **double (or Numeric):** doubles store regular numbers (large, small, positive, negative, with digits after the decimals, or without)
  * 12.3, 5, 999
  * Is easier to assume that most operator will involve doubles
* **character**
  * 'a' , '"good", "TRUE", '23.4
* **logical** 
  * TRUE, FALSE
* **complex (not widely applicable)**
  * 3 + 2i
* **raw (not widely applicable)**
  *  "Hello" is stored as 48 65 6c 6c 6f





### Create vector

When you want to create vector with more than one element, you should use **c()** function which means to combine the elements into a vector.



```R
# Create a vector.
apple <- c('red','green',"yellow")
print(apple)

# Get the class of the vector.
print(class(apple))
```



**Integers** **and doubles**

Is easier to assume that most operator will involve doubles

```R
# Doubles
> int <-c(5, 6, 8)

# integer
> int <-c(5L, 6L, 8L)
> typeof(int)
[1] "integer"
```



**R rewrites objects**

Without asking for permission or issuing a warning. In "Environment" panel is always shown only one variable with the same name.

![2.1](img\2.1.PNG)



If you have to many objects and you don't want to accidently overwrite some of them, you can use ls() to quickly check on them.

```R
# ls () list all visible objects in the environment
> ls()
[1] "int"      "m1"       "v1"       "variable"
```



![2.1](img\2.2.PNG)



**Characters vectors**

The elements of character vectors; can be letters, numbers or symbols.

```R
> char<-c("R", "for", "life")
> typeof(char)
[1] "character"
> char2<-c("The answer to life", "the universe", "and everything", "is", "42")
> typeof(char)
[1] "character"
```



**Logical vectors**

```R
> spock <-c(FALSE, TRUE, F, F, T, FALSE)
> typeof(spock)
[1] "logical"
```



**Complex & Raw**

Type in console the following

```R
# For complex
?is.complex() # or 
help(is.complex)

# For raw
?is.raw()
```



### Coercion

Coercion rules:

1. If a vector has even one string element, all other elements will be converted to string. The other way around it doesn't happen.

```R
> char2<-c("The answer to life", "the universe", "and everything", "is", 42)
> typeof(char2)
[1] "character"
> print(char2)
[1] "The answer to life" "the universe"       "and everything"     "is"                 "42"       
```



2. If a vector has only logical and numeric elements, all logicals will be converted to numbers

* T -> 1 and F -> 0

  

### Functions

Functions can take more than one argument.

```r
args(function.name) 
# returns the arguments a functions takes

>args(round)
function (x, digits = 0)  
NULL
>

  # digits after the decimal (optional)
  # x, the data your are applying the function to
```



**Examples**

```R
> round(2.4271, digits=2)
[1] 2.43

> round(2.4271,2) # same result
[1] 2.43
```



**Why we use argument's names at all?**

We can ommit the second argument in the round function (digits) but, R has a predefined argument order. The more arguments there are, the higher the chance of getting the order wrong.





### Building a function in R

```R
# --- Building a function

deck <- c("Duke", "Assasin", "Captain", "Ambassador", "Contessa")
print(deck)
sample(deck, size=3)
```

**Output**

```R
# Character do not repeat
> deck <- c("Duke", "Assasin", "Captain", "Ambassador", "Contessa")
> print(deck)
[1] "Duke"       "Assasin"    "Captain"    "Ambassador" "Contessa"  
> sample(deck, size=3) # 1
[1] "Contessa"   "Assasin"    "Ambassador"
> sample(deck, size=3) # 2
[1] "Contessa" "Duke"     "Assasin" 
> sample(deck, size=3) # 3
[1] "Captain"    "Assasin"    "Ambassador"
> sample(deck, size=3) # 4
[1] "Duke"     "Captain"  "Contessa"
>"
```



This function prohibits repetitions by default, sample function takes a third argument and it's called "replace"

```R
sample (x, size, replace = FALSE)
# Replace is an optional argument, default=FALSE
```



**Example**

```R
sample(deck, size=3, replace=T)
```

Output

```R
# Now the characters are being repeated
> sample(deck, size=3, replace=T)
[1] "Captain" "Captain" "Captain"
> sample(deck, size=3, replace=T)
[1] "Contessa" "Duke"     "Contessa"
> sample(deck, size=3, replace=T)
[1] "Ambassador" "Captain"    "Captain"   
```



#### Structure of a function

```R
function.name <- function () {
    body.of.code
}
```



**Example**



![2.1](img\2.3.PNG)



### Using script vs using console

Script

* Durable
* Executing code
* Editor marks syntax errors



## References

* 365 Data science
* https://www.tutorialspoint.com/r/r_data_types.htm







# Vectors & Vector operations

Vectors recap

* A sequence of elements that are of the same type
  * Double
  * Character
  * Logical 
  * Integer





## Introduction to vectors

```r
mean(vic)
median(vic)
sd(vic)
sum(vic)
```



## Vector recycling

What happen when we want to make operation using vectors with different lenght?

Vector recycling consist in repeating the shorter vector until the two vectors equal in length, then and only then, R carries out the operation.

```R
# Vectors with different lenghts
vec=1,2,3,4,5
vic=1,2,3

# Vector reciclying
vec=1,2,3,4,5
vic=1,2,3, 1, 2
```



## 

## Names

```R
a<-c(23,26,24,26)

attributes(age)
names(age)

# names function
names(age)<-c("George", "John", "Paul", "Ringo")
age

attributes (age)
```



## Getting help

In console write the following

```r
?print
?sample
?ls
```





## Slicing and indexing a vector

```R
> n.deck <-(6,7,8,9,10)
> deck <- c ("Duke", "Assassin", "Captain", "Ambassador", "Contesa")

> deck[4]
[1] "Duck"
> deck[-4] # prints all elements except "Ambassador"
```









# DataFrames

Universal container, can have variables of different types.

```R
vNumeric <-c(1,2,3)
vCharacter <-c("a", "b", "c")
vLogical <- (T, F, T)

# Coerces all values to most basic data type
df1 <- cbind(vNumeric, vCharacter, vLogical)

# Makes a data frame with three different data types
df2 <- as.data.frame(cbinds(vNumeric, vCharacter, vLogical))
```



## Selection of DataFrame elements

### Selection using number values

Similar to vectors and matrices, you select elements from a data frame with the help of square brackets `[ ]`. By using a comma, you can indicate what to select from the rows and the columns respectively. For example:

- `my_df[1,2]` selects the value at the first row and second column in `my_df`.
- `my_df[1:3,2:4]` selects rows 1, 2, 3 and columns 2, 3, 4 in `my_df`.

Sometimes you want to select all elements of a row or column. For example, `my_df[1, ]` selects all elements of the first row. Let us now apply this technique on `planets_df`!

### Selection using variable names

Instead of using numerics to select elements of a data frame, you can also use the variable names to select columns of a data frame.

Suppose you want to select the first three elements of the `type` column. One way to do this is

```R
planets_df[1:3,2]
```

A possible disadvantage of this approach is that you have to know (or look up) the column number of `type`, which gets hard if you have a lot of variables. It is often easier to just make use of the variable name:

```R
planets_df[1:3,"type"]
```



### Using $

you will often want to select an entire column, namely one specific variable from a data frame. If you want to select all elements of the variable `diameter`, for example, both of these will do the trick:

```R
planets_df[,3]
planets_df[,"diameter"]
```

However, there is a short-cut. If your columns have names, you can use the `$` sign:

```R
planets_df$diameter
```



### Selecting certain elements and filter

**Example 1**

In the following you'll select a subset from a data frame (`planets_df`) based on whether or not a certain condition is true (rings or no rings).

```cmd

     name               type diameter rotation rings
1 Mercury Terrestrial planet    0.382    58.64 FALSE
2   Venus Terrestrial planet    0.949  -243.02 FALSE
3   Earth Terrestrial planet    1.000     1.00 FALSE
4    Mars Terrestrial planet    0.532     1.03 FALSE
5 Jupiter          Gas giant   11.209     0.41  TRUE
6  Saturn          Gas giant    9.449     0.43  TRUE
7  Uranus          Gas giant    4.007    -0.72  TRUE
8 Neptune          Gas giant    3.883     0.67  TRUE

# Adapt the code to select all columns for planets with rings
planets_df[rings_vector==TRUE, ]
```



<u>Output</u>

```R

     name      type diameter rotation rings
5 Jupiter Gas giant   11.209     0.41  TRUE
6  Saturn Gas giant    9.449     0.43  TRUE
7  Uranus Gas giant    4.007    -0.72  TRUE
8 Neptune Gas giant    3.883     0.67  TRUE
```



## Subsets

The [`subset()`](http://www.rdocumentation.org/packages/base/functions/subset) function as a short-cut to do exactly the same as what you did in the previous exercises.

```
subset(my_df, subset = some_condition)
```

The first argument of [`subset()`](http://www.rdocumentation.org/packages/base/functions/subset) specifies the dataset for which you want a subset. By adding the second argument, you give R the necessary information and conditions to select the correct subset.

**Example 1**

The code below will give the exact same result as you got in the previous exercise, but this time, you didn't need the `rings_vector`!

```
subset(planets_df, subset = rings)
```

Output

```R
     name      type diameter rotation rings
5 Jupiter Gas giant   11.209     0.41  TRUE
6  Saturn Gas giant    9.449     0.43  TRUE
7  Uranus Gas giant    4.007    -0.72  TRUE
8 Neptune Gas giant    3.883     0.67  TRUE
```



**Example 2**

se `subset()` on `planets_df` to select planets that have a diameter smaller than Earth. Because the `diameter` variable is a relative measure of the planet's diameter w.r.t that of planet Earth, your condition is `diameter < 1`

```R
# Select planets with diameter < 1
subset(planets_df, subset=diameter <1)
```

Output

```R
     name               type diameter rotation rings
1 Mercury Terrestrial planet    0.382    58.64 FALSE
2   Venus Terrestrial planet    0.949  -243.02 FALSE
4    Mars Terrestrial planet    0.532     1.03 FALSE
```





## Sorting

In data analysis you can sort your data according to a certain variable in the dataset. In R, this is done with the help of the function [`order()`](http://www.rdocumentation.org/packages/base/functions/order).

[`order()`](http://www.rdocumentation.org/packages/base/functions/order) is a function that gives you the ranked position of each element when it is applied on a variable, such as a vector for example:

```
a <- c(100, 10, 1000)
order(a)
[1] 2 1 3
```



This means we can use the output of `order(a)` to reshuffle `a`:

```
a[order(a)]
[1]   10  100 1000
```



### Sort DataFrame

**Example 1**

- Call `order()` on `planets_df$diameter` (the `diameter` column of `planets_df`). Store the result as `positions`.
- Now reshuffle `planets_df` with the `positions` vector as row indexes inside square brackets. Keep all columns. Simply print out the result

```R
# planets_df is pre-loaded in your workspace
planets_df
# Use order() to create positions
positions <- order(planets_df$diameter)
positions
# Use positions to sort planets_df
planets_df[positions,]
```



Output

```R
# planets_df is pre-loaded in your workspace
planets_df
     name               type diameter rotation rings
1 Mercury Terrestrial planet    0.382    58.64 FALSE
2   Venus Terrestrial planet    0.949  -243.02 FALSE
3   Earth Terrestrial planet    1.000     1.00 FALSE
4    Mars Terrestrial planet    0.532     1.03 FALSE
5 Jupiter          Gas giant   11.209     0.41  TRUE
6  Saturn          Gas giant    9.449     0.43  TRUE
7  Uranus          Gas giant    4.007    -0.72  TRUE
8 Neptune          Gas giant    3.883     0.67  TRUE

# Use order() to create positions
positions <- order(planets_df$diameter)
positions
[1] 1 4 2 3 8 7 6 5

# Use positions to sort planets_df
planets_df[positions,]
     name               type diameter rotation rings
1 Mercury Terrestrial planet    0.382    58.64 FALSE
4    Mars Terrestrial planet    0.532     1.03 FALSE
2   Venus Terrestrial planet    0.949  -243.02 FALSE
3   Earth Terrestrial planet    1.000     1.00 FALSE
8 Neptune          Gas giant    3.883     0.67  TRUE
7  Uranus          Gas giant    4.007    -0.72  TRUE
6  Saturn          Gas giant    9.449     0.43  TRUE
5 Jupiter          Gas giant   11.209     0.41  TRUE
```



## Drop columns

```r
# Select columns to remove
select(df_name, -c (a, b, c, d, f, g))

# subset of a dataframe
subset_df <- subset(df_name, select=c(a,b,c))
```





## Rename columns of DataFrames

Option 1

```r
names <-("col1", "col2")
```



Option 2





Option 3



## Convert DataTypes

### **Option 1**

Imagine you have a data frame where you want to change columns:

- `a` and `b` to numerical
- `c` to date
- `d` and `e` to character

Then you can write:

```R
df %>% convert(num(a, b), dte(c), chr(d, e))
```

**Example 1**

```
gapminder %>% 
  convert(chr(country, 
              continent),
          int(lifeExp),
          dbl(pop),
          num(gdpPercap))
```



### **Option 2**

```R
module_fact1$module_id = as.character (module_fact1$module_id)
```



https://readr.tidyverse.org/reference/type_convert.html



### **Option 3**

```
gapminder %>%
  mutate(country = as.character(country),
         continent = as.character(continent),
         lifeExp = as.integer(lifeExp),
         pop = as.double(pop),
         gdpPercap = as.numeric(gdpPercap))
```

https://cran.r-project.org/web/packages/hablar/vignettes/convert.html



## Checking Data types

To know the data types of every column from a data frame

```R
library (dplry)
grimpse(df)
```



**Check columns**

```R
is.numeric(df$revenue)
```

output

```cmd
FALSE
```





# Shiny Apps

## Apps

### Single-file apps

**Advantages**

* Are ubiquitous

**Disadvantages**

* Apps quickly become unwieldy and difficult to manage
* It's important to keep a mental separation between what exist in UI and server components of the app

**App example**

```R
####################################
# Data Professor                   #
# http://youtube.com/dataprofessor #
# http://github.com/dataprofessor  #
####################################

# Modified from https://shiny.rstudio.com/tutorial/written-tutorial/lesson1/

library(shiny)
  

data < - read.csv ("file.csv")

# Define UI for app that draws a histogram ----
ui <- fluidPage(
  
  # App title ----
  titlePanel("Ozone level!"),
  
  # Sidebar layout with input and output definitions ----
  sidebarLayout(
    
    # Sidebar panel for inputs ----
    sidebarPanel(
      
      # Input: Slider for the number of bins ----
      sliderInput(inputId = "bins",
                  label = "Number of bins:",
                  min = 1,
                  max = 50,
                  value = 30)
      
    ),
    
    # Main panel for displaying outputs ----
    mainPanel(
      
      # Output: Histogram ----
      plotOutput(outputId = "distPlot")
      
    )
  )
)

# Define server logic required to draw a histogram ----
server <- function(input, output) {
  

  output$distPlot <- renderPlot({
    
    x    <- airquality$Ozone
    x    <- na.omit(x)
    bins <- seq(min(x), max(x), length.out = input$bins + 1)
    
    hist(x, breaks = bins, col = "#75AADB", border = "black",
         xlab = "Ozone level",
         main = "Histogram of Ozone level")
    
  })
  
}

# Create Shiny app ----
shinyApp(ui = ui, server = server)
```



### Split-file apps



## References

**DataProfesor (youtube) - Web Apps in R: Building your First Web Application in R | Shiny Tutorial** 

* https://www.youtube.com/watch?v=tfN10IUX9Lo&list=PLtqF5YXg7GLkxx_GGXDI_EiAvkhY9olbe

**LinkedIn - Building Data Apps with R and Shiny**

* https://www.linkedin.com/learning/building-data-apps-with-r-and-shiny-essential-training/

```SQL
library(shiny)
library(dplyr)
library(stringr)
library(XML)
library(rvest)
library(httr)



# Bus Stop Info -------
load("data/db_stop_list.RData")  # Load local version of data

# Train Stop Info -------
load("data/train_station_list.RData")  # Load local version of data


# Shiny UI -------
ui <- fluidPage(
  theme = "bootstrap.css",
  includeCSS("www/styles.css"),
  
  navbarPage(
    "Thrive",
    id = "main_navbar",
    
    tabPanel(
      "Visualization",
      fluidRow(column(
        3, uiOutput("currentTime", container = span)
      ),
      column(
        3, uiOutput("db_last_update", container = span)
      )),
      sidebarLayout(
        sidebarPanel(
          width = 3,

          uiOutput("selected_stops_UI"),
          actionButton("bus_refresh", "Refresh"),
          
          br(),
          br(),
          uiOutput("selected_buses_UI"),
          br(),
          br(),
          h3("Auto Refresh"),
          selectInput(
            "interval",
            NULL,
            # "Refresh interval",
            choices = c(
              "Off" = 0,
              "30 seconds" = 30,
              "1 minute" = 60,
              "2 minutes" = 120,
              "5 minutes" = 300,
              "10 minutes" = 600
            ),
            selected = 0
          ),
          br(),
          br(),
          h3("Stop Info"),
          a(
            href = "https://www.dublinbus.ie/RTPI/Sources-of-Real-Time-Information/",
            "Bus stop numbers can be found here.",
            target = "_blank"
          ),
          br(),
          br(),
          h3("Custom URL"),
          p(
            "A custom URL can be used to pre select choices when loading the app.",
            br(),
            "Use the button below to create a URL for the choices currently selected."
          ),
          br(),
          actionButton("bus_custom_url", "Create custom URL")
        ),
        mainPanel(DT::dataTableOutput("bus_table"))
      )
      
      
      
    ),
    tabPanel(
      "Table",
      fluidRow(column(
        3, uiOutput("dart_currentTime", container = span)
      ),
      column(
        3, uiOutput("dart_last_update", container = span)
      )),
      sidebarLayout(
        sidebarPanel(
          width = 3,
          actionButton("dart_refresh", "Refresh"),
          br(),
          br(),
          selectInput(
            "dart_selected_stop",
            label = "Choose Stop",
            choices = tidy_station_list,
            selected = "tara "
          ),
          uiOutput("dart_direction"),
          uiOutput("dart_destination"),
          br(),
          br(),
          h3("Custom URL"),
          p(
            "A custom URL can be used to pre select choices when loading the app.",
            br(),
            "Use the button below to create a URL for the choices currently selected."
          ),
          br(),
          actionButton("dart_custom_url", "Create custom URL")
        ),
        mainPanel(DT::dataTableOutput("dart_table"))
      )
      
    )
  )
)





# Run the application
shinyApp(ui = ui, server = server)

```



# REFERENCES



**Youtube**

* **Free code camp - R Programming tutorial:** https://www.youtube.com/watch?v=_V8eKsto3Ug
