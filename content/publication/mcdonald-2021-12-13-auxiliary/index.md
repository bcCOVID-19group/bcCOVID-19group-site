---
# Documentation: https://wowchemy.com/docs/managing-content/

title: 'Can auxiliary indicators improve COVID-19 forecasting and hotspot prediction?'
subtitle: ''
summary: ''
authors:
- dajmcdon
- Jacob Bien
- Alden Green
- Addison J. Hu
- Nat DeFries
- Sangwon Hyun
- Natalia L. Oliveira
- James Sharpnack
- Jingjing Tang
- Robert Tibshirani
- Valérie Ventura
- Larry Wasserman
- Ryan J. Tibshirani
tags: []
categories: []
date: '2021-12-13'
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ''
  focal_point: ''
  preview_only: true

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
publishDate: '2021-12-13'
publication_types:
- '2'
abstract: |
  Short-term forecasts of traditional streams from public health reporting (such as cases, hospitalizations, and deaths) are a key input to public health decision-making during a pandemic. Since early 2020, our research group has worked with data partners to collect, curate, and make publicly available numerous real-time COVID-19 indicators, providing multiple views of pandemic activity in the United States. This paper studies the utility of five such indicators—derived from deidentified medical insurance claims, self-reported symptoms from online surveys, and COVID-related Google search activity—from a forecasting perspective. For each indicator, we ask whether its inclusion in an autoregressive (AR) model leads to improved predictive accuracy relative to the same model excluding it. Such an AR model, without external features, is already competitive with many top COVID-19 forecasting models in use today. Our analysis reveals that 1) inclusion of each of these five indicators improves on the overall predictive accuracy of the AR model; 2) predictive gains are in general most pronounced during times in which COVID cases are trending in "flat" or "down" directions; and 3) one indicator, based on Google searches, seems to be particularly helpful during "up" trends.

publication: '*PNAS*'

url_pdf: https://www.pnas.org/content/pnas/118/51/e2111453118.full.pdf

links:
  - name: Github
    icon_pack: fab
    icon: github
    url: https://github.com/cmu-delphi/covidcast-pnas/tree/v0.5

doi: 10.1073/pnas.2111453118
---
