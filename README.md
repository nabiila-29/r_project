
# Shiny App 101
[Github Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)  
Shiny Tutorial: https://shiny.rstudio.com/tutorial/#get-started  
Mastering Shiny: https://mastering-shiny.org/preface.html  
  
Shiny Cheatsheet: https://shiny.rstudio.com/articles/cheatsheet.html  
Shiny Gallery: https://shiny.rstudio.com/gallery/  
Shiny documentation:  https://www.rdocumentation.org/packages/shiny/versions/1.7.1

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
           
UI Packages: https://github.com/nanxstats/awesome-shiny-extensions
    
### 2. Server
Defined by `function (input, output) {}`  
_shiny output server_ (`renderPlot()`,  `renderText()`, etc) :  
- `output$<outputId>` in ui   
- `input$<inputId>` in ui  

```    
  Output$<outputId> <- rendertype({ input$<inputId> }) 
    
  Output$product <- renderText({ input$x * 5 })
```  
  
#### [Reactive Expression](youtube.com/watch?v=cqOUpnF-Lco)  
Create our own reactive variable:  
`reactive({...})`  
  
 wrong:  
 ```  
  server <- function (input, output) {  
    x <- input$num +1  
  }  
 ```  
 
  correct:  
 ```  
  server <- function (input, output) {  
    x <- reactive ({ input$num +1 }) 
  }  
 ```  



## B. Basic Input and Output Couple in Shiny
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
?function_name:generate detail of function

