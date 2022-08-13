[Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)  

Source:  
- [R, freecodecamp](https://www.youtube.com/watch?v=_V8eKsto3Ug)    
  
# What is R?  
R is basically programming language for statistical computing and graphics.  
  
  
Yess. A language. A language is basically a way to communicate with others. Programming language means a language we use to communicate with computer, and R is one of the language. Just like language in the world, we have English, Chinese, Arabic, and other thousand language. There are so many programming language out there and they have their own specific purpose.    
R is a language we use when we want to communicate and ask computer to do statistical computing and graphics.  
  
  
Simply, R has two type of syntax.
1. Basic Syntax  
We can use this syntax directly after install R 
2. Package Syntax  
We need to install and call the package first before use the syntax.  
`library(<package_name>)`

# Popular Packages in R  
- dplyr : read 'di plaier' - for manipulating data frames. The name is kinda strange. The d is for dataframes, the plyr is to evoke pliers.  

- tidyr : read 'tai dier' - for cleaning up information. Means 'tidy' in R.  

- stringr: read 'string ar' - for working with strings or text information.  

- lubdridate: -  for manipulating date information

- httr: read as english spelling - for working with website data

- ggvis: read 'jiji viz' -for interactive visualization. gg stand for grammar of graphics

- ggplot2: -the most common packages for creating graph and data viz in R  

- shiny: -for interactive applications that you install on websites.  
  
# Basic Syntax for Pre-Processing  
Using package `datasets` we can easily retrieve datasets and explore R funciton there  
```
library(datasets)           #import library  

data()                      # show list of datasets available  

iris <- iris                # assign datasets to variable to know the whole dataset  
head(iris)                  #retrieve first 6 rows of dataset  
plot(iris$Species)          #plot of dataset specific column  
plot(iris$Sepal.Length)     #plot of dataset specific column  
plot(iris$Petal.Width)      #plot of dataset specific column  
  
?plot                       #show function documentation  
summary(iris)               #show statistical summary  

```
  
  
  
# Data Formats in R  
Like apple and Orange. sometimes we talk about two different things.  

## Data Types  
Data Types is level measurements of variable.  
1. Numeric  
- integer  
- Single Precision  
- Double Precision  
3. Character  
4. Logical (Boolean)  
5. Complex  
6. Raw

## Data Structures  
1. Vector  
- 1 or more number in 1 dimentional array. In a straight line  
- All same data type. All integer for example  
- R basic data object  

2. Matrix / Array  
### Matrix###
- has rows and columns. 2 dimentional data
- the columns are all need to be the same length
- the data are all need to be the same class  
- column are not named, but reffered to by index numbers  
  
###Array###  
- Identical to Matrix bur 3 dimention.  


3. Data Frame 
- 2 dimentional collection that can have vectors of multiples data type. We can have character, integer, or boolean in a data frame.  
- The trick is all of those must be in the same length  
- Closest R analogue to spreadsheet  
- R has special functions to working with data frame  
  

4. List  
- Most flexible data format. We can put anything in a list  
- It's orders collection of elements.
- We can have any class, length, or structure  
- list can include list (nested list)  

## Coersion in Data World  
**Coersion** is changing data object from one type to another. Changing the level of measurement or chancing the nature of the variable that we are dealing with.  
Example:  
- change character to logical  
- matrix to data frame  
- double to integer
etc.  
  
#### NUMERIC ----------------  
```  
n1 <- 15  #double precision  
n1  
typeof(n1)    #show the data structure / low level of datatype  
```  
  
#### VECTOR -----------------  
``` 
v1 <- c(1, 2, 3, 4, 5)  
v1  
is.vector(v1)     # check whether it is vector or not  
```  
  
#### MATRIX -----------------  
```  
m1 <- matrix(c( T, T,
                F, F,
                T, F),
                nrow = 3,
                byrow = TRUE)  #True mean matrix will be filled by rows. The    default is FALSE
m1  
```  

#### ARRAY ----------------  
```  
a1 <- array(c( 1:24 ), c(4,3,3))   # row column, table. table mean row x column will be retrieve in how many table
a1
```   

#### DATA FRAME ---------------------  
```  
# can combine vectors of the same lenght 
  
vNumeric    <- c(1,2,3)  
vCharacter  <- c("a","b","c")  
vLogical    <- c(T,F,T)  
  
dfa <- cbind(vNumeric,vCharacter,vLogical)  
dfa                   # matrix of one data type. not a data frame  
  
  
df <- as.data.frame(cbind(vNumeric,vCharacter,vLogical))  #function to change to data frame 
df  

```  
There are two ways to check the data strucuture:  
`class()` : tell us the high-level data type (DATA TYPE)  
`typeof()` : tell us the low-level data type (DATA STRUCTURE)  
  
example:  
matrix case~  
`class()` : matrix, array   
`typeof()` : character  


#### LIST ----------------------  
```    
o1 <- c(1,2,3)  #object one  
o2 <- c("a","b","c","d")  
o3 <- c(T,F,T,T,F)  
  
list1 <- list(o1,o2,o3)  
list1                             #the vector become list. symbolize with [[ ]]  
  
list2 <- list(o1,o2,o3, list1)  
list2                             # list inside list     
  
```  
[[ ]] : list  
[ ]   : vector (maybe)
  
#### COERCING TYPES  
1:18:36  
https://www.youtube.com/watch?v=_V8eKsto3Ug  

