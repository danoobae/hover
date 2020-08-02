
<!-- README.md is generated from README.Rmd. Please edit that file -->

# hover

<!-- badges: start -->

[![R build
status](https://github.com/tyluRp/hover/workflows/R-CMD-check/badge.svg)](https://github.com/tyluRp/hover/actions)
<!-- badges: end -->

The goal of hover is to add animations to `shiny::actionButton` and
`shiny::icon` using [Hover.css](https://github.com/IanLunn/Hover).

## Installation

You can install the development version of hover from GitHub with:

``` r
# install.packages("devtools")
devtools::install_github("tylurp/hover")
```

## Example

Animate a button and icon is as simple as providing the animation name:

``` r
library(shiny)
library(hover)

ui <- fluidPage(
  use_hover(),
  hover_button(
    inputId = "btn",
    label = "hello hover!",
    icon = icon("refresh"), 
    button_animation = "rotate", 
    icon_animation = "spin"
  ) 
)

server <- function(input, output, session) {
  
}

shinyApp(ui, server)
```

The `hover` package essentially takes the `shiny::actionButton` source
code and applies the necessary Hover.css classes to make things move.

## Acknowledgements

This package was built using the following tools:

  - [Hover.css](https://github.com/IanLunn/Hover), the underlying CSS
  - [shiny](https://github.com/rstudio/shiny), the source code for
    `hover_button`

Without these, this package wouldn’t have been possible.
