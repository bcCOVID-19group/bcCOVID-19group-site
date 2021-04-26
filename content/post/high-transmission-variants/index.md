---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "High transmission variants: the benefits of being proactive"
subtitle: ""
summary: ""
authors: [eare, carolinecolijn]
tags: []
categories: []
date: 2021-03-02T19:15:45-07:00
lastmod: 2021-03-02T19:15:45-07:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: true

links:
  - name: View original
    url: https://www.sfu.ca/magpie/blog/variant-simple-proactive.html
    icon: globe
    icon_pack: fas

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []

---

There has been a lot of discussion about “variants of concern” (VOC)
internationally and across Canada. One of the most important concerns is that
SARS-CoV-2, the virus that causes COVID-19 and so has caused the COVID pandemic
we are all facing today, has found ways to become more transmissible. We
recently posted modelling work on what a higher transmission rate would look
like for the number of infections. In a place like British Columbia, where
cases of our usual type of COVID-19 have held steady in past weeks, a higher
transmission rate means that cases would grow. Simply put, if we are balancing
on the knife edge, increased transmission would put us over that edge and into
exponential growth. 

By now, most people following COVID-19 data have seen more than their fair
share of exponential growth curves. When cases grow exponentially, there is a
doubling time: first 10, then 20, then 40 and 80 cases. By the time you are at
500 there is only one doubling time left until 1000. Infectious diseases tend
to grow, or shrink, exponentially, because infection doesn’t rain down randomly
from the sky: people infect each other. 

Imagine that we only have a few cases of a VOC, but it’s more transmissible -
with each case causing 1.4 new cases on average, instead of 1, like our current
type of COVID-19. With total cases resting around 400 each day, we don’t worry
too much about 10 new VOC cases, and then after a month, 45, and a month later
200, but at that point the VOC has risen to reflect 30% of the total, and
instead of staying constant, we have a doubling time of just two weeks. 

The federal government recently introduced [border
measures](https://www.canada.ca/en/public-health/news/2021/02/additional-testing-and-more-stringent-quarantine-requirements-for-travel-to-canada.html)
requiring travellers to have a PCR test and to quarantine upon arrival. No
doubt part of the motivation for this was to prevent continued introduction of
VOCs. But that ship has left the proverbial harbour. In Ontario, for example, a
[recent
report](https://www.publichealthontario.ca/-/media/documents/ncov/epi/covid-19-daily-epi-summary-report.pdf?la=en)
(p 17) found that 15.1% of cases with no known epidemiological link were the
B.1.1.7 VOC. There have been multiple VOC [school
exposures](https://globalnews.ca/news/7667013/covid-variants-surrey-schools/)
in the Greater Vancouver area. Other provinces have similarly reported VOC
cases.  In most cases we do not know from public reporting when individuals
with VOC COVID-19 were tested, and in what setting, and it makes a difference:
not every introduction of a VOC represents established transmission. We do know
that while Manitoba did identify VOC cases, later testing found very low
numbers, and new [travel
restrictions](https://winnipeg.ctvnews.ca/new-interprovincial-travel-restrictions-now-in-effect-in-manitoba-1.5287530)
are likely to severely limit the chance that additional VOC cases enter
Manitoba. With proactive testing to screen most or all cases for VOCs, and with
proactive measures when VOCs are identified, what does the modelling look like? 

Here we modify and update our [previous
post](https://www.sfu.ca/magpie/blog/high-transmission-variant-modelling.html),
using a similar modelling approach, but this time, we look at what happens if
VOCs start at some specified percentage of the daily reported cases and we
explore the impact of more proactive measures aiming to slow the growth of
VOCs. The initial values for variants come from [CTV variant
tracker](https://www.ctvnews.ca/health/coronavirus/tracking-variants-of-the-novel-coronavirus-in-canada-1.5296141)
(as of February 26), from [Quebec’s
INSPQ](https://www.inspq.qc.ca/covid-19/donnees/variants) as well as from
Ontario’s epidemiology report [Appendix
B2](https://covid-19.ontario.ca/covid-19-epidemiologic-summaries-public-health-ontario).

We have used low numbers for SK and MB because the CTV variant tracker showed
low numbers for them (SK - 6; MB - 5) out of a total of 1428 for the country at
the time, and because Manitoba has quarantine rules in place to limit the
importation of variants from other parts of Canada.

We ask what happens if we continue with control measures as estimated by the
model fits (blue), compared to what happens if we get a little bit “more
proactive”. Here are the results:

{{< figure src="featured.png" id="figure1" >}}

In some provinces, like Manitoba and Saskatchewan where controls on "regular"
COVID-19 are strong and where VOC incidence is low, the risk that VOCs rise
greatly in the next few months is low. This is due to border measures, wider
testing and of course to the strength of distancing measures in place. In
others, where numbers are higher and crucially where COVID-19 is in less of a
steep decline, VOCs would rise steeply by May. 

Being “more proactive” makes a big difference. We model “more proactive” in two
ways: first, we improved control for all the COVID-19, such as would occur with
stricter distancing measures (but it could be achieved with regular screening
with rapid tests instead, or localized control). We also added a proactive
impact of variant-specific measures. These could include prioritizing VOCs for
contact tracing, mass screening of all or most contacts of cases, or other
measures targeted at controlling VOCs -- this must include detecting them
rapidly enough to act.  Together, we model detection and VOC-specific action
resulting in a decrease of a further 10% decrease in transmission of VOCs.  

As is always the case, models are more like flashlights than crystal balls. We
use flashlights to see the path ahead - not to tell the future. When we see
something we don’t like, we use that information to change the path. Here, we
are not predicting that the steep rises will happen. The most likely scenario
is that actions will be taken either before or when hospitalizations rise to
the point where public health is concerned about capacity; the resulting
distancing or other measures are not in these models. 

 

### Methods comments: 

In the above figures, we illustrate what three trajectories might look like. In
the previous post we looked at a large collection of possible trajectories --
taking into account some uncertainty in when the VOC might become established
in the community and uncertainty in how transmissible it would be. We shaded in
the area that the trajectories might cover. Here, we use just one initial value
(at the stated % of current cases) per colour, and just one relative
transmission rate. That’s why the figures differ, compared to the previous
post. The underlying model is by Anderson et al, published
[here](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1008274).
We fit it to each province’s past case count data. We then use the estimates
that we get for the strength of distancing, and apply those to the new variant.
We are developing this modelling further, but at this time, the method does not
account for direct competition between the variant and the “regular” COVID-19.
For example, with COVID-19 active cases still a very small portion of our
population, we have not gone to the trouble of accounting for the same
individual being exposed to both types (VOC and non-VOC) covid. The model does
not yet account for the impact of vaccination. This is because vaccination, as
yet and as currently planned, will not be impacting transmission for months.
For our recent work on vaccination, see our [recent
preprint](https://www.medrxiv.org/content/10.1101/2021.02.23.21252309v1).
