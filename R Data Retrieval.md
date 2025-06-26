# R - Data Retrieval

## CSV

To open a CSV file in R, you can use the `read.csv()` function. Here's a basic example of how to do it:

```R
# Replace 'path_to_your_file.csv' with the actual path to your CSV file
data <- read.csv("path_to_your_file.csv")

# View the first few rows of the data
head(data)
```

If your file is located in a specific directory, you can provide the full path or set the working directory using `setwd()`.

For example:
```R
setwd("path/to/your/directory")
data <- read.csv("your_file.csv")
head(data)
```
