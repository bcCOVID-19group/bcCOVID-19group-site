---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Monitoring COVID-19 Risk within Communities"
subtitle: ""
summary: ""
authors: ["sallyotto",Greg Stewart, Guy Dumont, Klaske Van Heusden,"bryn wiley"]
tags: []
categories: []
date: 2021-09-01T11:55:33-08:00
publishDate: 2021-09-01T07:55:00-07:00
lastmod: 2021-09-01T11:55:33-08:00
featured: false
draft: false

summary: |
 COVID-19 case counts vary from region to region, making it hard to visualize how cases have changed over time within regions or to predict risk levels within a community. We introduce a COVID-19 Risk Meter and an on-line app that allows people to see how COVID-19 risks have changed over time within their local communities.  We also use feedback control theory to indicate when case numbers are trending above a target level for too long, giving an early warning signal that additional measures should be taken by the community to prevent transmission.

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
    url: https://brynwiley.shinyapps.io/BCCovid19Risk/
    icon: r-project
    icon_pack: fab
---


When it comes to controlling COVID-19, information guides behaviour and policy. People look to rising cases as an indicator of risk, changing their behaviour in response. It is these responses of the public and of governments that have repeatedly bent down rapidly rising epidemic curves, preventing health care systems from becoming overwhelmed and saving lives.

While British Columbia provides maps and data sheets illustrating current case counts for the thirteen Health Service Delivery Areas (HSDA) and Local Health Authorities (LHA) within the province, these static figures make it hard to assess growing risks. To help guide our collective actions, we introduce a risk meter  to convey local risks of transmission, based on the familiar Air Quality Index used within the province. The risk meter is based on the number of cases in a local region (HSDA or LHA) ([Figure 1](#figure1)):

{{< figure src="figure1.png" id="figure1" title="Figure 1: The COVID-19 Risk Meter.">}}

Every doubling of cases causes the risk meter to rise by one. Plotting the risk over time allows people to see how fast cases are doubling: the length of each coloured bar gives the doubling time when cases are rising (or the halving time when cases are falling). For example, [Figure 2](#figure2) illustrates the rapid rises in risk within the East Kootenay Health Service Delivery Area with five doublings in a one month period (mid-July to mid-August 2021).

{{< figure src="figure2.png" id="figure2" title="Figure 2: Risk Levels in the East Kootenay Health Service Delivery Area. Dashed vertical line gives the present day, with future projections based on a local linear projection of the risk meter.">}}

This scale is recommended because of the expected exponential rise in the number of cases in the absence of a change in behaviour, at least over the short term while susceptibility within a community remains roughly constant. If all else were equal, a community would move from one risk level to the next at a constant rate while a disease is exponentially growing (or declining).  Because the risk meter pays attention to doublings, it is not overly sensitive to day-to-day fluctuations in case numbers or to minor changes in which cases are included (e.g., including travellers or not, a small proportion of undetected cases). 

The goal of the risk meter is to help guide behaviour throughout the province by simultaneously conveying risks of local transmission and tying these to appropriate activities.  As an example, we can tie recent restrictions in the Central Okanagan to the risk meter:

* [Mask mandate](https://www.cbc.ca/news/canada/british-columbia/b-c-interior-covid-cases-update-1.6121240): Instituted July 28, 2021, when there were 15 daily cases per 100,000 (Risk Meter 5)
* [Limits on gatherings](https://www.cbc.ca/news/canada/british-columbia/covid-19-update-aug6-1.6132524): Instituted August 06, 2021, when there were 44 daily cases per 100,000 (Risk Meter 7)

We can also relate the risk meter to the chance that a group of individuals within a region would have at least one infective person with COVID-19. Assuming that individuals gather at random and are infective for an average of 5 days ([Anderson et al. 2021](https://www.sciencedirect.com/science/article/pii/S1755436521000141)), the chance that at least one person in a group of 50 is infective is:

* 1% at risk level 4
* 2.5% at risk level 5
* 5% at risk level 6
* 10% at risk level 7
* 20% at risk level 8

Individually, we can use graphs of the Risk Meter over time to judge trends in case numbers and to adjust our behaviours accordingly. Blue (1-3) corresponds to lower risk levels, consistent with exercising some care to avoid transmission.  Orange (4-6) corresponds to moderate risk, consistent with wearing masks indoors and switching social interactions to outdoors where possible. Red (7 plus) corresponds to high risk, consistent with strongly restricting the amount of time spent in indoor public environments and limiting contacts to within the same social bubble.

## Feedback
If we have a target risk level that we want to remain below (e.g., in the Blue low risk levels, at or below 3), we can adjust our behaviours and policies as cases rise above the target. While we can use the current risk level guide us, we can do even better if we use design principles from feedback control theory.  

Appropriate feedback design can reduce the health, social, and economic costs of a pandemic by driving cases down when they rise above the target and relaxing measures when cases fall below the target (van Huesden et al. 2021; link to come).  Performance can be improved when feedback systems consider recent trends and not only current measures.  One simple design sums up recent departures from the target using a "proportional-integral" control system (see details in van Huesden et al. 2021), basically accumulating evidence that case numbers are going in the wrong direction. 

For example, if we want to remain in the blue low-risk region (corresponding to fewer than 4 cases per 100,000), the following integrator tallies the total amount by which a region is above the target:
 
i(d+1) = i(d) + w (r(d)-target),

where i(d) stands for the integrator, r(d) is the risk meter level on day d, and the number w=0.022 was chosen to add a small amount of weight (2.2%) each day that that a region is above the target (e.g., three to stay within the blue low-risk region). Any day that case numbers fall below the target, the integrator is reset to zero. The integrator (dashed curve), added to the current risk level (black curve), provides an early warning system that risk levels have been moving above the target ([Figure 3](#figure3)). 

(NOTE FOR KLASKE: This is higher than your 0.0026 weighting, but here cases are measured per 100,000 cases, and your weighting would then be 0.13. We'll need to set a default.) 

(NOTE FOR ALL: App doesn't do the opposite but probably should - indicate when measures are currently more stringent than needed for the target.)

{{< figure src="figure3.png" id="figure3" title="Figure 3: Early Warning System in the East Kootenay Health Service Delivery Area. Dashed curve shows the early warning system that accumulates evidence that case counts are above a target, here set at a risk level of three.">}}

This early warning system indicates when there is accumulated evidence that stronger control measures are needed to reverse recent trends. As noted in van Huesden et al. (2021), decisions based on such accumulated evidence can greatly help pandemic control, even when there are delays (e.g., in case detection) and uncertainty in the efficacy of different measures (e.g., the actions taken at a given risk level).

## On-line app
To implement the risk meter, one of us (BW) has created a [browser app](https://brynwiley.shinyapps.io/BCCovid19Risk/) that retrieves the latest BC case data and generates changes to the risk meter over time. Users can choose which regions to explore (at the HSDA or LHA level), whether to simply project risk levels forward in time or use the early warning system based, and can vary the target for a community (see more details about the methods in the "Advanced Options and Explanations" tab of the [browser app](https://brynwiley.shinyapps.io/BCCovid19Risk/)). 

## Acknowledgements

We thank the [BC COVID-19 Modelling Group](https://bccovid-19group.ca) for helpful discussions.

Source: From the BC COVID-19 Data [portal](http://www.bccdc.ca/health-info/diseases-conditions/covid-19/data); HSDA data provided daily at [http://www.bccdc.ca/Health-Info-Site/Documents/BCCDC_COVID19_Regional_Summary_Data.csv](http://www.bccdc.ca/Health-Info-Site/Documents/BCCDC_COVID19_Regional_Summary_Data.csv) and LSA data provided twice weekly at [http://www.bccdc.ca/Health-Info-Site/Documents/BCCDC_COVID19_LHA_CHSA_Data.xlsx?Web=1](http://www.bccdc.ca/Health-Info-Site/Documents/BCCDC_COVID19_LHA_CHSA_Data.xlsx?Web=1).