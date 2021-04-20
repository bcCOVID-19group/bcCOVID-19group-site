---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "After Vaccination"
subtitle: ""
summary: ""
authors: [pft3,carolinecolijn]
tags: []
categories: []
date: 2021-04-17T19:15:45-07:00
lastmod: 2021-04-17T19:15:45-07:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

See also: https://www.sfu.ca/magpie/blog/after_vaccination.html

Please see our full report for more details and simulation results.

The only way things can return to normal in BC is if a large portion of our population obtains immunity to the virus, either through infection or through vaccination. Currently a small fraction of British Columbians are immune to COVID-19: approximately 1 in 5 of us have received at least one dose of vaccine, and a much smaller number have had the infection. In the meantime, the pandemic is kept under control through various measures, including contact tracing and social distancing. Social distancing takes a heavy toll on our economy and the quality of our lives, and we cannot do it forever.

But according to BC’s immunization plan, by the end of the summer all adults will have had the opportunity to have one dose of the vaccines available, and many will have had two doses. The vaccines are highly effective and the rollout, albeit on a longer time frame than we would like, will prevent us from having to choose between millions of infections and thousands of deaths in our population, or indefinite and costly control measures. Ideally, once enough of us are vaccinated, we will be able to safely relax the restrictions that have constrained our lives over the past year. 

The problem is that there are three groups of people who are not protected when the vaccine rollout is complete, even under the most optimistic assumptions: i) children ii) people who decline the vaccine, iii) people for whom their vaccine doses are ineffective (efficacy is high, but not 100%). When we relax restrictions after the vaccination rollout the virus will have an opportunity to spread in these populations. But maybe the number of people who have immunity through vaccination will be enough, and at that point there will be few or no new infections: a consequence of so-called herd immunity.

To investigate this question we performed simulations of the pandemic in BC using the model described in our preprint on vaccine rollouts. We factored in what we know of the transmission of the virus, the rollout of vaccination, vaccine efficacy against infection and against disease, and the eventual relaxation of social restrictions. We studied what happens when social distancing is relaxed at different stages of the vaccine rollout. (We were inspired by a similar study performed for the UK.)

As you might expect, if we open up before the rollout is complete, there are negative consequences. Many people become infected after restrictions are relaxed, and there is a surge in the number of hospitalizations and deaths. The earlier we do it, the worse the outcome. (Of course, what would likely happen in that case is that restrictions would have to be re-introduced.)

What if we wait until the vaccination rollout is complete and all adults have had the opportunity to receive two doses? We relax social distancing at this point, while keeping testing, contact tracing, and some other public health measures in place. Disappointingly, and perhaps surprisingly, many people still become infected in the months after restrictions are relaxed; see the simulation results in our report linked above. The problem is that not enough people obtain immunity with current vaccination plans to prevent a final surge in infections after restrictions relax. 

What fraction of the population needs to be immune to the virus to get herd immunity? There is a simple class of models known as SIR models in which a pathogen that grants immunity after infection spreads through a population. In these models there is a calculation you can do to estimate this fraction. The value depends on R0, the basic reproductive number: the average number of additional people infected by a single COVID-19 case in an entirely susceptible population. R0 depends on the virus in question (which variant in particular) and the population, including the social distancing and personal protective measures in place. Without any measures in place R0 for the original COVID was estimated to be between 2 and 4. When strict social distancing is in place we are able to bring R0 below 1, as we did in BC in the spring of 2020, when we didn’t have to contend with the new variants. For the new variants such as B117 and P1, we know that R0 is higher than for the original variant.  

In this very simple model, the relation between f, the fraction that needs to be immune, and R0, the basic reproductive number, is f=1-1/R0. So if we know what R0 we will have when we reopen, we can estimate what fraction of the population needs to have immunity for infection numbers to decline. In our full model we used an R0 of 2.5, which may be an overestimate or an underestimate depending on the variant that is dominant at that time and what control measures remain in place. With this value of R0,we need 1-1/(2.5)=60% to be immune. So assuming we want our population to reach this level of protection through vaccination, we need 60% percent of the population to be protected by vaccination. Unfortunately, about 80% of the population is adult, of those only about 80% will get vaccinated, and of those, the vaccine may be effective against infection for only around 80%, though it will be effective against severe and symptomatic disease for more than this portion.  This gives a total percentage of only 51% protected from infection. To get up to herd immunity for an underlying R of 2.5, we would need an additional 9% of the population to obtain immunity through infection. That’s nearly 470,000 people in BC, or approximately 3 times the number of infections we have seen to date.

On the other hand, if we know we can protect only 51% of the population from the infection, we can ask how low R0 has to be for infections to decline. It turns out the maximum R0 we can handle is about 2. This is probably unrealistically low for a “full reopening” that relaxes distancing measures, given what we know of the new variants, even if we maintain measures like testing and contact tracing, and some use of masks.

These simple calculations neglect a lot of things that we deal with in our more sophisticated model -- including the population’s age and contact structure, age-specific risk of disease, hospitalization and death, the fact that we do not detect all infections, and more -- but they give almost the same result. And the fundamental issues are the same. We need a higher fraction of the population to have immunity in order to return to life as normal. We can reach that fraction either through vaccination or infection.  And this is under the optimistic assumption that immunity is very strong (i.e. people do not get infected again after recovering from COVID-19) and that it is permanent. 

We have three options. We can do something to keep R0 low enough that it is covered by our inadequate levels of immunity in our population.  We can accept that 10% - 20% of the population will get COVID and increase levels of immunity that way. Or we can work on increasing immunity by altering our vaccination program. Probably some combination of the three will be necessary.

We are mainly keeping R0 low currently with social distancing, and we cannot do that forever. But there are other things we do that reduce R0 that can be continued indefinitely, such as contact tracing and the deployment of rapid tests at strategic settings. These can definitely help, but there is a limit to how much they can reduce R0 alone.

Allowing a fraction of the population to become infected will increase the portion of the population who are immune, but at a substantial risk to the infected individuals that comes from COVID infection. Many will be children, for whom the risk of severe outcomes is less, but it is far from 0. It is also unclear how long infection with COVID protects against reinfection.

Finally, the best outcome is if we can increase the fraction of the population that is immune without large numbers of people being infected with COVID-19. Three ways to do this are to vaccinate children, increase vaccine acceptance, and increase the efficacy of the vaccines.

None of the vaccines are approved yet for children under the age of 18, though trials are underway. Health Canada is reviewing an application from Pfizer to expand vaccine use to ages 12 and up. When we ran our model with vaccinating children aged 10-19 results were much better with a smaller fraction of the population obtaining immunity through infection. Vaccinating younger children would help even more. 

Increasing vaccine acceptance also increases the level of immunity in the population. Anything we can do to encourage adults to take the vaccine will have positive results in reducing the number of infections, severe outcomes, and deaths. As more people know someone who has had a severe COVID-19 infection, hesitancy about vaccines may go down. Some recent results from the UK show vaccine acceptance rates as high as 95% among those aged 55 and up. If we could attain this in Canada for everyone aged 10 and up, our estimate shows that we could reopen to an R0 of ~ 3.8 (assuming 5% acquire immunity through infection).

Finally, it may be possible to increase vaccine efficacy. The mRNA vaccines are already phenomenally effective at preventing symptomatic disease, as we see in the results of the stage 3 trials, but we’re not sure how effective they are at preventing infection in practice. However, other vaccines do not appear to have as high efficacy, with results for the AstraZeneca vaccine and the Johnson and Johnson vaccine appearing lower in preliminary studies. All our results will be worse if a vaccine has lower efficacy than the 80% we estimated here. This may happen if new variants emerge against which our current vaccines provide less protection.  It may be necessary to investigate using boosters to obtain higher levels of protection, especially if waning immunity -- from natural infection or from vaccination -- turns out to be a problem.

According to the best estimates we have available for the contact patterns and vaccine efficacy against the virus circulating today, we will not be able to go back to normal and relax distancing measures entirely, even once the current vaccination plan is complete. If we did so, without further changes (vaccinating youth, increasing vaccination uptake) it is likely that 100,000s of British Columbians would become infected or some restrictions would need to be re-introduced and maintained indefinitely. We can improve our situation with the following actions:

Vaccinating children as soon as safely possible

Encouraging vaccine acceptance among the adult population

Continuing to use contact tracing and testing to control outbreaks

Deploying rapid testing strategically to reduce the rate of transmission

Monitoring vaccine efficacy and waning immunity and using boosters to maintain high levels of efficacy within the vaccinated population 

 
