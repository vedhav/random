library(shiny)
library(reticulate)
source_python("helper.py")

ui <- fluidPage(
  numericInput("num_in", "Enter a number!", 73),
  textOutput("text_out")
)

server <- function(input, output, session) {
  output$text_out <- renderText({
    paste0(input$num_in, " multiplied by 20 is ", some_py_function(input$num_in))
  })
}

shinyApp(ui, server)


