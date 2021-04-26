---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Vaccinating Essential Workers"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2021-02-23T14:24:25-07:00
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

links:
  - name: View original
    url: https://www.sfu.ca/magpie/blog/vaccinating-essential-workers.html
    icon_pack: fas
    icon: globe
  - name: GitHub
    url: https://github.com/nmulberry/essential-workers-vaccine/blob/main/README.md
    icon_pack: fab
    icon: github
doi: https://doi.org/10.1101/2021.02.23.21252309
url_pdf: https://www.medrxiv.org/content/10.1101/2021.02.23.21252309v1
#url_code: https://github.com/nmulberry/essential-workers-vaccine/blob/main/README.md
---
After many long months with no treatment or vaccine available, and widespread
social distancing the main tool for fighting the pandemic, there are now four
different vaccines approved that are effective for COVID-19. Phase 3 trial data
and experiences since then show that the Pfizer and Moderna vaccines are safe
and highly effective at preventing disease. Even better, preliminary results
point to them also being effective at preventing infection, which means they
will block transmission of the virus. Vaccination of the majority of British
Columbians will be the backbone of our recovery from the pandemic.

Unfortunately, we will not have enough vaccine doses for every British
Columbian who wants to be vaccinated before the end of summer. We have to
decide in what order British Columbians get the doses we do have. We hope that
soon, people 80 years and older, COVID-facing healthcare workers, and remote
indigenous communities will have all received both doses. We need to figure out
who comes next. 

One well-known fact about COVID is that older age groups have the highest risk
of experiencing severe complications or dying from being infected. So you might
think that the best thing to do is vaccinate people in descending order of age,
in order to minimize the harm. This works if everyone is equally likely to be
exposed to the virus -- but they aren’t. 

Another approach is to target essential workers: the people we depend on to
keep things running, and who have contacts with lots of other people as an
essential part of their job. They include teachers, taxi drivers, retail
workers, food production workers, law enforcement, public safety, first
responders, social workers, workers in agriculture and transportation, and many
more. Essential workers are on the front line: we are asking them to take a
much higher risk that they will be exposed. And if they are infected, they risk
infecting many others. 

But if they are vaccinated, there will be less COVID around and therefore less
exposure to the virus for everybody else, including older people. 

In our most recent preprint we present the results of our mathematical modeling
of the COVID vaccine rollout in BC, using data on how the vaccine impacts
infection, transmission and symptomatic disease. Our simulations strongly
suggest that it is better for everyone if we vaccinate essential workers once
those who are 80 and older are vaccinated. This may seem counterintuitive, so
we’ll explain why we think it is the best strategy for BC, and may not be the
best strategy in other places.

One important consideration is that although the vaccines are very effective,
they are not perfect, and perhaps as many as 5-10% of people who get both doses
of the vaccine will not be protected. In addition, perhaps 15% of people will
decline the vaccine. This leaves around 20-25% of the elderly not protected. So
even if we devoted all our vaccine resources to the elderly they will not be
completely protected. We will need to use other measures to prevent many
hospitalizations and deaths. 

On the other hand, by vaccinating younger people with many contacts we can
greatly reduce the amount of virus in the population. This will mean that very
few elderly people are ever exposed to the virus. Fewer exposures means many
fewer infections among the elderly, whether they have been vaccinated or not.

Whether protection through vaccinating older people first is more effective
than preventing exposure by vaccinating younger essential workers depends on
many factors which are best captured in simulations. Our simulations of BC
found that vaccinating essential workers early, rather than vaccinating the
population in decreasing order of age would lead to up to

* 200,000 fewer infections
* 600 fewer deaths
* $230 million decrease in healthcare costs

The reason for this is that in BC we have been partially successful in
controlling the spread of the virus with social distancing and other measures.
It is not inevitable that the majority of British Columbians, and in particular
the elderly, will be exposed to the virus. The reduction in transmission
brought about by vaccinating essential workers, those who cannot distance as
part of their job, is highly effective for reducing COVID rates province-wide,
and it is well worth it to reduce risk to the elderly, along with leading to
many fewer infections, and reduced health care costs. (Note: the above numbers
come from comparing to a situation where the reproduction number R - accounting
for distancing measures - is 1.3 after we finish vaccinating those over 80. If
it is held lower than that by long-term distancing measures and/or getting
control over higher-transmission variants, these numbers would be lower. But
keeping distancing measures in place long term has costs too. We model an
overall 97.5% efficacy against disease, including prevention of infection and
prevention of disease given infection). 

Throughout the pandemic we have mostly seen data on cases (infections),
hospitalizations and deaths. But there are other consequences to having
COVID-19. In our study we also considered chronic disease resulting from COVID
infection. One form of this is so-called “Long COVID”, where the symptoms of
COVID last for weeks, months, or potentially longer. There are also possible
COVID complications: other chronic health conditions caused by COVID, including
diabetes, organ damage, and neurological and psychiatric disorders. It’s
unclear how common these serious health outcomes are for people who have had
COVID, but we used the best available data to estimate how often they might
occur, in different vaccination strategies. We found again that vaccinating
essential workers earlier can lead to a profound reduction in the number of
cases of these long-lasting and damaging conditions.

In contrast, in a region where case numbers are growing fast -- fast enough to
have 40,000 incident cases per day in BC compared to our maximum ever of about
1000 -- the difference obtained by vaccinating essential workers is not enough.
Whatever is done, most older people will be exposed, and therefore the best
outcomes are obtained by vaccinating in decreasing order of age. But
fortunately we have not reached that stage yet in BC, and vaccinating essential
workers early will keep more British Columbians safe.

The preprint is posted
[here](https://www.medrxiv.org/content/10.1101/2021.02.23.21252309v1) and the
code is available at the github repository
[here](https://github.com/nmulberry/essential-workers-vaccine/blob/main/README.md).
