---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "An Online Tool to estimate the Vaccination Status of a Group"
subtitle: ""
summary: ""
authors: ["bryn wiley","dajmcdon","sallyotto"]
tags: []
categories: []
date: 2021-08-16T11:55:33-08:00
publishDate: 2021-08-16T07:55:00-07:00
lastmod: 2021-08-16T11:55:33-08:00
featured: false
draft: false

summary: |
 Vaccination rates are changing globally, making it challenging for organizers to predict vaccination levels for group meetings being planned. We have created a [browser app](http://shiney.zoology.ubc.ca:3838/shiny/GroupVaccinationStatus/) to estimate the numbers of unvaccinated, partially vaccinated, and fully vaccinated people in a group at a future date, based on data from around the world on vaccination rates by location and age group. While most accurate over short time frames, this app provides event organizers a clearer picture of the susceptibility of their participants to COVID-19.

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: true

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []

links:
  - name: Shiny app
    url: http://shiney.zoology.ubc.ca:3838/shiny/GroupVaccinationStatus/
    icon: r-project
    icon_pack: fab
---


As COVID-19 vaccination rates continue to rise, federal and provincial governments around the world have been lifting restrictions on travel and organized gatherings. For example, British Columbia moved on July 1 2021 to step 3 of their ([four step plan](https://www2.gov.bc.ca/gov/content/covid-19/info/restart)) to remove restrictions related to COVID-19.  
However, despite this lifting of restrictions, significant portions of the Canadian and world population remain unvaccinated or partially vaccinated. Furthermore, strong differences in vaccination rates exist between different regions and age groups. For example, although approximately 90% of persons aged 70 or older in British Columbia are fully vaccinated, this drops to 36% for ages 12 to 17 ([COVID-19 vaccination in Canada](https://health-infobase.canada.ca/covid-19/vaccination-coverage/), accessed August 9 2021). In the United States, the state of New Jersey reports a 60% full vaccination rate, whereas the state of Georgia only has 39% of their population fully vaccinated ([Our World in Data](https://ourworldindata.org/us-states-vaccinations/), accessed August 9 2021). 

This unevenness in vaccination status poses a problem for universities, festivals, trade shows, conferences, or other organizations who might want to quantify how at-risk their participants are for COVID-19 infection. As more restrictions are lifted and travel restrictions become lighter, the age and regional makeup of these participants will become more diverse, and this problem will only grow.

To address this, we have created a [browser app](http://shiney.zoology.ubc.ca:3838/shiny/GroupVaccinationStatus/) to estimate the numbers of unvaccinated, partially vaccinated, and fully vaccinated people in a group at a future date. The app gathers data from around the world on vaccination rates by location and age group and projects forward to estimate the makeup of the specific group in question. Projecting vaccinations into the future is, however, highly uncertain and subject to increasing error the further in the future the event will occur, and of course travellers may not be representative (see more details about the methods and data sources in the "Data Sources and Explanations" tab of the [browser app](http://shiney.zoology.ubc.ca:3838/shiny/GroupVaccinationStatus/)). Given these limitations, this app will hopefully give event organizers a clearer picture of the susceptibility of their participants to COVID-19.

{{< figure src="featured.png" id="figure1" >}}