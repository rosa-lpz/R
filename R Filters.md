# Filters

To filter a dataframe in R, we can use the `subset()` function or the `dplyr` package's `filter()` function.  

# Subset()

```R
# Example: Filter rows where gender is male (gender == 1) and smoking == 0 (non-smokers)
filtered_data <- subset(cardio_base, gender == 1 & smoking == 0)

# View the first few rows of the filtered data
head(filtered_data)

```

# dplyr's filter()

```R
# Install dplyr (if needed)
install.packages("dplyr")

# Load the dplyr package
library(dplyr)


```
