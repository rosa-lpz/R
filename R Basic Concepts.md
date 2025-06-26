# R Basic Concepts

Sure! Here's a quick primer on **R basics**, great for beginners getting started with R programming, especially for data analysis and statistics.

------

## **Basic Syntax**

```r
# Assigning values
x <- 5        # preferred in R
y = 10        # also works

# Printing
print(x)
x             # auto-prints in console

# Comments
# This is a comment
```

------

## **Data Types**



| Type      | Example              |
| --------- | -------------------- |
| Numeric   | `x <- 3.14`          |
| Integer   | `x <- as.integer(3)` |
| Character | `x <- "Hello"`       |
| Logical   | `x <- TRUE`          |
| Complex   | `x <- 1 + 2i`        |



------

## **Data Structures**

#### **Vector**

```r
vec <- c(10, 20, 30)
vec[1]       # Access first element
```

#### **Matrix**

```r
mat <- matrix(1:6, nrow=2, ncol=3)
mat[1, 2]    # First row, second column
```

#### **List** (can hold mixed types)

```r
my_list <- list(name="John", age=25, scores=c(90, 80))
my_list$name
```

#### **Data Frame**

```r
df <- data.frame(name=c("Alice", "Bob"), age=c(25, 30))
df$age
df[1, "name"]
```

------

## **Control Structures**

```r
# If statement
if (x > 0) {
  print("Positive")
}

# For loop
for (i in 1:5) {
  print(i)
}

# While loop
i <- 1
while (i <= 5) {
  print(i)
  i <- i + 1
}
```

------

## **Functions**

```r
# Define a function
add <- function(a, b) {
  return(a + b)
}
add(3, 4)
```

------

## **Packages**

```r
# Install a package
install.packages("ggplot2")

# Load a package
library(ggplot2)
```

------

## **Reading Data**

```r
# CSV file
data <- read.csv("data.csv")

# View first few rows
head(data)
```

------

Would you like a beginner exercise or cheat sheet?
