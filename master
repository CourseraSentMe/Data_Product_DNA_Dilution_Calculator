---
title       : DNA Dilution Calculator Slides
subtitle    : A calculator for DNA dilutions 
author      : Frank J. Ambrosio
job         : Author
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Slide 1

My web app is called the DNA Dilution Calculator


```{r}
c1 = 10
v1 = 10
c2 = 5
v2 = (c1 * v1)/c2
v2
```

--- .class #id 

## Slide 2


Here is the ui.R code for the front end of my app!
```{r eval=FALSE}
sidebarLayout(
    sidebarPanel(
      numericInput("numericA", "What is the starting concentration in ng/uL?", 
                   value = 0, min = 1, max = 1000, step = 1),
      numericInput("numericB", "What is the starting volume in uL?",
                     value = 0, min = 1, max = 10000, step = 1),
      numericInput("numericC", "What is the desired concentration in ng/uL?",
                    value = 0, min = 1, max = 1000, step = 1),
      submitButton("Submit")
    ),
    
    mainPanel(
       h3("Volume of diluent to be added to starting DNA solution 
          in order to achieve desired dilution:"),
       textOutput("calcA"),
       h3("Total volume of completed dilution:"),
       textOutput("calcB")
    )
  )
))

```


--- .class #id

## Slide 3

Here is the server.R code from my app!
```{r eval=FALSE}

library(shiny)


shinyServer(function(input, output) {
   calcA <- reactive({
    ((input$numericA * input$numericB)/input$numericC)-input$numericB
   })
   calcB <- reactive({
     ((input$numericA * input$numericB)/input$numericC)
   })
   output$calcA <- calcA
   output$calcB <- calcB
  })

```

--- .class #id

## Slide 4

If you ever need to calculate DNA Dilutions then YOU NEED THIS APP!


--- .class #id

## Slide 5

If you are working with DNA then you need to calculate DNA Dilutions so YOU NEED THIS APP!

--- .class #id






