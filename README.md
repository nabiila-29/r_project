
# Shiny App 101
[Github Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)  
Shiny Tutorial: https://shiny.rstudio.com/tutorial/#get-started  
Mastering Shiny: https://mastering-shiny.org/preface.html  
  
Shiny Cheatsheet: https://shiny.rstudio.com/articles/cheatsheet.html  
Shiny Gallery: https://shiny.rstudio.com/gallery/  

## What is Shiny?  
Shiny is an R package. 
Allows us to create rich, interactive web apps  
  
- Provide UI that could generate HTML, CSS, Javascripts for common tasks
- Reactive programming: input change, output change

## A. Shiny Component
    
### [1. UI](https://shiny.rstudio.com/tutorial/written-tutorial/lesson2/)    
   Defined by `fluidPage()` function. consist of:  
   - `titlePanel()`  
   - `SidebarLayout()`  
        - `SidebarPanel()`  
        &emsp; _shiny input UI_  (`sliderInput()`, `selectInput()`, etc)  
        - `mainPanel()`  
         &emsp; _shiny output UI_ (`plotOutput()`, `ImageOutput()`, etc)  
    
### 2. Server
Defined by `function (input, output) {}`  
_shiny output server_ (`renderPlot()`,  `renderText()`, etc) :  
- output$_output_name_in_ui_  
- input$_input_name_in_ui_  

## B. BASIC INPUT AND OUTPUT IN SHINY
[cheatsheet](https://shiny.rstudio.com/articles/cheatsheet.html)

## [C. APPLICATION LAYOUT GUIDE](https://shiny.rstudio.com/articles/layout-guide.html)  
There are several layout we can choose in Shiny 
### 1. SidebarLayout  
placing a `sidebarPanel()` alongside a `mainPanel()`  
### 2. Grid Layout  
Example: `fluidRow()` , `column()` )
### 3. Multiple Top-Level Components
Example: `tabsetPanel()` , `navlistPanel()`  
  
  
      
  
  
  
## R tips  
?function_name:generate detail of funciton

