rm(list = ls())

#install.packages('rvest')
#install.packages('dplyr')
library(rvest)
library(dplyr)


#Extract table from wikipedia page
#Source : https://www.r-bloggers.com/using-rvest-to-scrape-an-html-table/

#Website URL
url <- 'https://fr.wikipedia.org/wiki/M%C3%A9tropole_de_Lyon'

#Node selection and data extraction
List <- url %>%
  read_html() %>%
  html_nodes(xpath='//*[@id="mw-content-text"]/div/table[2]') %>% #“copy XPath” in HTML DOM
  html_table() #html_text()
  
#Dataframe creation from List
df <- List[[1]]
rm(List)
