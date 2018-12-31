# Methodology

## Confidence Intervals

## Medians

The median is the value separating the higher half of a probability distribution
from the lower half. One could therefore think of it as the "middle" value. 

For a continuous probability distribution, the median is the value such that a
number is equally likely to fall above or below it. Since the number of voters
is usually rather large in the areas considered on these pages, the probability
mass functions for the voting intentions behave a lot like continuous
probability distributions. One can therefore say that for the medians of the
voting intentions, the actual number of voting intentions for a particular party
is equally likely to fall above or below it.

For the number of seats, this doesn't hold true though. The number of seats is
usually much too small for the probability mass functions to behave more or less
like a continuous probability distribution. As a consequence, each of the values
in the 99 percent confidence intervals will have a substantial probability,
including the median itself. In these cases, the median is the value such that
the probability that the value is equal to it or above it is at least fifty
percent, and that the value is equal to it or below it at least fifty percent
too. One could say that median is the value that pushes the accumulated
probability above the fifty percent mark.

Notice that often, the median will also be the most likely value. However, that
doesn't need to be so, and in many cases, it won't be either.

### Shoudn't the Medians Add Up to the Total Number of Seats?

In most cases, the medians for the number of seats per party will add up to a
number close to the total number of seats. But in many cases, the sum of the
medians won't be exactly equal to the total number of seats. Here's an example
illustrating why this isn't an error:

Image three parties competing for a single seat in a constituency. All three
parties have the same chance of winning seat, so the probability mass function
is 33⅓ percent of getting 1 seat for each of them, and 66⅔ percent of getting no
seat. This means that for all three parties, the median value for the number of
seats is 0, with a 95 percent confidence interval of 0—1. The sum of the median
values is 3 × 0 = 0, which is less than 1.

## Weighted Monte Carlo Simulations

## Projecting National Results on Electoral Districts

Opinion polls usually only give data on a national level. Unless there is only
one, national electoral district, these data have to be translated to the local
electoral districts one way or the other. The model used to produce the numbers
on these pages is a variant of the so-called uniform regional swing, which means
that it projects the national tendencies onto the local electorale districts
without any adjustments.

### Multiplicative Uniform Regional Swing

Assume that a party had a voting share of 20 percent at the last election,
but that an opinion poll shows that the voting intentions for the party have
risen to 22 percent. One way to project this change onto the local electoral
districts, is to take the last election result in every electoral district, and
simply add the national change to each of them. This means that if the party
scored 25 percent in a particular district, the new score used to calculate the
number of seats in that district will be 25 + 2 = 27. If the party had voting
share of only 15 percent, the new score would be 15 + 2 = 17 percent.

This model works fine for parties increasing their result, and parties with a
modest to large vote share across all electoral district. However, for small
parties losing votes, the model can result into negative numbers in the
electoral districts where it performed poorely during the last election. Just
imagine a party going from 8 to 5 percent nationally, but with a local score
of only 2 percent in one of the electoral districts. The uniform regional
swing mode described above would project the party at 2 - 3 = -1 percent in
that district.

As an alternative, the model used on these pages projects the national results
onto the local districts in a multiplicative way. That means that when a party
increases from 20 to 22 percent, the model doesn't add 2 percent to the party's
voting share in every district, but *multiplies* the local results with a factor
of 22 / 20 = 1.1. In the example mentioned above, this would put the party in
the district where it score 25 percent last time at 27.5 percent, and in the
district where it scored only 15 percent at 16.5 percent. For the party losing
votes, the factor would be 5 / 8 = 0.625, thus projecting the party in the
district where it score 2 percent last time at 1.25 percent.

Is multiplicative uniform regional swing more correct than additive uniform
regional swing? Hard to say. Multiplicative uniform regional swing will make
parties swing more in electoral districts where they had a high score at the
last election. For parties gaining support, that may be incorrect, if they are
gaining more national support because they're mainly getting more support in
those districts where they performed less during the last election. But it's
easy to produce counterexamples where a multiplicative approach will be more
correct than the additive.

As a general rule, using multiplicative or additive uniform regional swing
should not make much of a difference for seat projections on the national
level. Overestimations in one electoral districts will often be compensated by
underestimations in other electoral districts, such that the overall result
will be more or less correct. Remember that in the end, a party gaining support
on a national level may very well be losing votes in some parts of the country.
The projection of the national results onto the local electoral districts
should therefore not be used to predict local results, but only as a way to
calculate national seat projections. If you want to know how a party is doing
locally, the best way to find out about this is to run a local opinion poll.

### Regional Data

From time to time, pollsters will run local opinion polls, or publish regional
tendencies in their national polls. Advanced models could use this information
in order to project national polling results more accurately onto local
electoral districs. In some occassions, e.g. when there are parties with a
particular local stronghold, this may give more accurate results on a national
level. On the other hand, if these local results give better results on a
national, it would probably be wiser not to project the national results onto
those local electoral districts, and instead just use the regional data
directly.

### Historic Data

Some models try and use more of the historic data in every electoral district.
But in Western countries, with election cycles of four or five years, this means
that models use data that is eight to ten years old if last two elections are
used, and twelve to fifteen years old if three elections are used. It is
questionable how relevant such historic data can be with new parties emerging,
old parties disappearing, in addition to changing demographics. Sometimes, even
using data from the last election, which may not be older than three or four
years, seems hopeless because of deep changes in national politics.

### Incumbency

Some studies have shown that incumbent candidates have a slight advantage over
their opponents. However, when trying to calculate national results, incumbency
should make a difference, since any significant change would already have been
included in the national polling results. Therefore, incumbency has not been
modeled in for the calculation of the numbers presented on these pages.

### House Factors and Other Corrective Measures

Some modelers try to improve the raw polling results using "house factors".
Basically, these house factors try to compensate for the historic errors
pollsters have made, e.g. if they have consistently underestimated a party with
a certain percentage. Others also include economic or demographic data, e.g.
giving a slight advantage to the parties in government if the economy is doing
well, or vice versa.

House factors may work to a certain degree in countries with a bipartisan
political landscape, but they quickly break down when there are many parties
involved, or when there are large or even disruptive changes. Furthermore,
for obvious reasons, house factors won't work for new parties.

The numbers presented on these pages try to explain in more detail the true
meaning of opinion polling results. Therefore, the model doesn't try to
"improve" any opinion polling result with house factors or other parameters.

As a personal note, it is also my belief that pollsters have a large interest in
trying to get their opinion polling results as correct as possible, and
therefore will have a huge incentive to learn from theire mistakes. House
factors seem therefore a bit patronizing.

### New Parties

Since the method described above relies on regional data in order to calculate
the number of seats in parliament, new parties that haven't participated in the
previous election pose a probleme. However, there are number of strategies that
can be used to estimate the regional distribution of the new party's voters:

* If party A and party B merge together to form a new party C, the regional data
  for the parties A and B can simply added together as an estimate for the new
  party's, even though we know that in politics, 1 + 1 ⋚ 2.
* If a dissidency in a party A breaks out and forms a new party B, the regional
  data for party A can simply be divided equally between the old party A and the
  new party B. Multiplicative uniform regional swing will then scale both
  parties up or down in all electoral districts, but the size of the parties
  will off course be the same in all electoral districts.
* In case an entirely new party has been created, the best estimate will
  probably be the assumption of a uniform distribution across the entire
  country. This can be achieved by setting the party's size equal to e.g. one
  percent of the population in each electoral district. Again, multiplicative
  uniform swing will then scale the party up or down in all electoral districts,
  in accordance with the party's result in the poll.

Note however that in the case where more information is known about the newly
formed party, it is always wise to include it. If it's e.g. known that the new
party will only participate in the election in a part of the country, the
regional data for the new party should be adjusted in that way.

### Results

The following sections show the results for past elections. In particular, for
each of the tables below, the final results in terms of number of votes were
feeded to the model as a set of polling results. The sample sizes for these
fictive polls were 600, 800, 1000, 1200, 1500, 2000, 3000 and 5000, sizes often
used by polling firms. For each of the sample sizes, the 95% confidence
intervals for the number of seats for each parties are compared to the actual
number of seats the parties received.

The results show, quite naturally, that the seat projections are more accurate
for electoral systems that are more proportional. But even for non-proportional
electoral systems, the seat projections stay relatively close to the actual seat
distribution of the election. Larger parties, for which non-proportional
electoral systems often will behave in a fairly linear way, get more accurate
results than smaller parties, which will often strugle with e.g. local or
national electoral thresholds.

#### United Kingdom, 8 June 2017

| Sample Size                           | CON                 | LAB                                  | UKIP         | LIBDEM          | SNP                             | GREEN                        | PC            |
|:-------------------------------------:|:-------------------:|:------------------------------------:|:------------:|:---------------:|:-------------------------------:|:----------------------------:|:-------------:|
| Election Result (8 June 2017)         | 42.4% <br> 318      | 40.0% <br> 262                       | 1.8% <br> 0  | 7.4% <br> 12    | 3.0% <br> 35                    | 1.6% <br> 1                  | 0.5% <br> 4   |
| 600                                   | 38–46% <br> 278–348 | 36–44% <br> 241–331                  | 1–3% <br> 0  | 6–10% <br> 1–19 | 2–5% <br> 0–54                  | 1–3% <br> <strike>0</strike> | 0–1% <br> 0–7 |
| 800                                   | 39–46% <br> 283–343 | 37–43% <br> 247–327                  | 1–3% <br> 0  | 6–9% <br> 2–17  | 2–4% <br> 0–52                  | 1–3% <br> <strike>0</strike> | 0–1% <br> 0–5 |
| 1000                                  | 39–45% <br> 287–340 | 37–43% <br> 251–322                  | 1–3% <br> 0  | 6–9% <br> 2–16  | 2–4% <br> 0–51                  | 1–3% <br> <strike>0</strike> | 0–1% <br> 0–5 |
| 1200                                  | 40–45% <br> 291–338 | 37–43% <br> 254–319                  | 1–3% <br> 0  | 6–9% <br> 2–15  | 2–4% <br> 1–50                  | 1–2% <br> <strike>0</strike> | 0–1% <br> 0–5 |
| 1500                                  | 40–45% <br> 294–335 | 38–43% <br> 257–316                  | 1–3% <br> 0  | 6–9% <br> 3–15  | 2–4% <br> 1–48                  | 1–2% <br> <strike>0</strike> | 0–1% <br> 0–5 |
| 2000                                  | 40–45% <br> 300–332 | 38–42% <br> <strike>263–312</strike> | 1–2% <br> 0  | 6–9% <br> 3–15  | 2–4% <br> 1–41                  | 1–2% <br> <strike>0</strike> | 0–1% <br> 0–5 |
| 3000                                  | 41–44% <br> 304–328 | 38–42% <br> <strike>269–307</strike> | 1–2% <br> 0  | 7–8% <br> 4–14  | 2–4% <br> 2–35                  | 1–2% <br> <strike>0</strike> | 0–1% <br> 0–5 |
| 5000                                  | 41–44% <br> 308–326 | 39–41% <br> <strike>275–303</strike> | 1–2% <br> 0  | 7–8% <br> 5–13  | 3–4% <br> <strike>2–29</strike> | 1–2% <br> <strike>0</strike> | 0–1% <br> 0–4 |
| Previous Election Result (7 May 2015) | 36.9% <br> 331      | 30.4% <br> 232                       | 12.6% <br> 1 | 7.9% <br> 8     | 4.7% <br> 56                    | 3.8% <br> 1                  | 0.6% <br> 3   |

Only polls for which at least the sample size has been published are included in the table above.

**Legend:**
+ **Top half of each row:** Voting intentions (95% confidence interval)
+ **Bottom half of each row:** Seat projections for the House of Commons (95% confidence interval)
+ **CON:** Conservative Party
+ **LAB:** Labour Party
+ **UKIP:** UK Independence Party
+ **LIBDEM:** Liberal Democrats
+ **SNP:** Scottish National Party
+ **GREEN:** Green Party
+ **PC:** Plaid Cymru
+ **BNP:** British National Party

#### Norway, 11 September 2017

| Sample Size                                   | Ap                | H                 | FrP               | KrF            | Sp               | V              | SV              | MDG           | R             |
|:---------------------------------------------:|:-----------------:|:-----------------:|:-----------------:|:--------------:|:----------------:|:--------------:|:---------------:|:-------------:|:-------------:|
| Election Result (11 September 2017)           | 27.4% <br> 49     | 25.0% <br> 45     | 15.2% <br> 27     | 4.2% <br> 8    | 10.3% <br> 19    | 4.4% <br> 8    | 6.0% <br> 11    | 3.2% <br> 1   | 2.4% <br> 1   |
| 600                                           | 24–31% <br> 44–57 | 22–29% <br> 38–52 | 13–18% <br> 23–33 | 3–6% <br> 1–11 | 8–13% <br> 14–24 | 3–6% <br> 1–11 | 4–8% <br> 8–15  | 2–5% <br> 1–9 | 1–4% <br> 1–2 |
| 800                                           | 24–31% <br> 45–56 | 22–28% <br> 39–51 | 13–18% <br> 23–33 | 3–6% <br> 1–10 | 8–13% <br> 15–23 | 3–6% <br> 1–11 | 5–8% <br> 8–14  | 2–5% <br> 1–8 | 2–4% <br> 1–2 |
| 1,000                                         | 25–30% <br> 45–56 | 22–28% <br> 40–51 | 13–18% <br> 23–32 | 3–6% <br> 2–10 | 9–12% <br> 15–22 | 3–6% <br> 1–10 | 5–8% <br> 8–14  | 2–4% <br> 1–8 | 2–4% <br> 1–2 |
| 1,200                                         | 25–30% <br> 45–55 | 23–28% <br> 40–51 | 13–17% <br> 24–32 | 3–5% <br> 2–10 | 9–12% <br> 16–22 | 3–6% <br> 2–10 | 5–8% <br> 9–14  | 2–4% <br> 1–8 | 2–3% <br> 1–2 |
| 1,500                                         | 25–30% <br> 46–55 | 23–27% <br> 40–50 | 13–17% <br> 24–31 | 3–5% <br> 2–9  | 9–12% <br> 16–22 | 3–6% <br> 2–10 | 5–7% <br> 9–13  | 2–4% <br> 1–8 | 2–3% <br> 1–2 |
| 2,000                                         | 25–29% <br> 46–54 | 23–27% <br> 41–50 | 14–17% <br> 25–31 | 3–5% <br> 2–9  | 9–12% <br> 16–22 | 4–5% <br> 2–10 | 5–7% <br> 9–13  | 3–4% <br> 1–7 | 2–3% <br> 1–2 |
| 3,000                                         | 26–29% <br> 47–54 | 24–27% <br> 42–49 | 14–17% <br> 25–30 | 4–5% <br> 2–9  | 9–11% <br> 17–21 | 4–5% <br> 2–9  | 5–7% <br> 9–13  | 3–4% <br> 1–4 | 2–3% <br> 1–2 |
| 5,000                                         | 26–29% <br> 48–53 | 24–26% <br> 42–48 | 14–16% <br> 26–30 | 4–5% <br> 2–9  | 9–11% <br> 17–20 | 4–5% <br> 3–9  | 5–7% <br> 10–12 | 3–4% <br> 1–2 | 2–3% <br> 1–2 |
| Previous Election Result (8–9 September 2013) | 30.8% <br> 55     | 26.8% <br> 48     | 16.3% <br> 29     | 5.6% <br> 10   | 5.5% <br> 10     | 5.2% <br> 9    | 4.1% <br> 7     | 2.8% <br> 1   | 1.1% <br> 0   |

**Legend:**
+ **Top half of each row:** Voting intentions (95% confidence interval)
+ **Bottom half of each row:** Seat projections for the Norwegian Parliament (95% confidence interval)
+ **Ap:** Arbeiderpartiet
+ **H:** Høyre
+ **FrP:** Fremskrittspartiet
+ **KrF:** Kristelig Folkeparti
+ **Sp:** Senterpartiet
+ **V:** Venstre
+ **SV:** Sosialistisk Venstreparti
+ **MDG:** Miljøpartiet de Grønne
+ **R:** Rødt

#### Iceland, 28 October 2017

| Sample Size                                | D                 | V                 | P              | B               | C             | A           | S               | F             | T           | R           | M               |
|:------------------------------------------:|:-----------------:|:-----------------:|:--------------:|:---------------:|:-------------:|:-----------:|:---------------:|:-------------:|:-----------:|:-----------:|:---------------:|
| Election Result (28 October 2017)          | 25.2% <br> 16     | 16.9% <br> 11     | 9.2% <br> 6    | 10.7% <br> 8    | 6.7% <br> 4   | 1.2% <br> 0 | 12.1% <br> 7    | 6.9% <br> 4   | 0.1% <br> 0 | 0.2% <br> 0 | 10.9% <br> 7    |
| 600                                        | 22–29% <br> 14–20 | 14–20% <br> 9–14  | 7–12% <br> 4–7 | 8–13% <br> 5–9  | 5–9% <br> 0–5 | 1–2% <br> 0 | 10–15% <br> 6–9 | 5–9% <br> 3–5 | 0–1% <br> 0 | 0–1% <br> 0 | 9–14% <br> 5–8  |
| 800                                        | 22–28% <br> 15–19 | 14–20% <br> 10–13 | 7–11% <br> 5–7 | 9–13% <br> 5–8  | 5–9% <br> 3–5 | 1–2% <br> 0 | 10–14% <br> 6–9 | 5–9% <br> 3–6 | 0% <br> 0   | 0–1% <br> 0 | 9–13% <br> 5–8  |
| 1,000                                      | 23–28% <br> 15–19 | 15–19% <br> 10–13 | 8–11% <br> 5–8 | 9–13% <br> 6–8  | 5–8% <br> 3–5 | 1–2% <br> 0 | 10–14% <br> 6–9 | 5–9% <br> 3–5 | 0–1% <br> 0 | 0–1% <br> 0 | 9–13% <br> 6–9  |
| 1,200                                      | 23–28% <br> 15–19 | 15–19% <br> 10–13 | 8–11% <br> 5–7 | 9–13% <br> 5–8  | 5–8% <br> 3–5 | 1–2% <br> 0 | 10–14% <br> 7–9 | 6–9% <br> 3–5 | 0% <br> 0   | 0–1% <br> 0 | 9–13% <br> 6–8  |
| 1,500                                      | 23–28% <br> 16–18 | 15–19% <br> 10–12 | 8–11% <br> 5–6 | 9–12% <br> 6–8  | 6–8% <br> 3–5 | 1–2% <br> 0 | 11–14% <br> 7–8 | 6–8% <br> 4–5 | 0% <br> 0   | 0–1% <br> 0 | 9–13% <br> 6–8  |
| 2,000                                      | 23–27% <br> 15–18 | 15–19% <br> 10–12 | 8–11% <br> 5–7 | 9–12% <br> 6–8  | 6–8% <br> 3–5 | 1–2% <br> 0 | 11–14% <br> 7–9 | 6–8% <br> 3–5 | 0% <br> 0   | 0–1% <br> 0 | 10–12% <br> 6–8 |
| 3,000                                      | 24–27% <br> 15–18 | 16–18% <br> 10–12 | 8–10% <br> 5–6 | 10–12% <br> 6–8 | 6–8% <br> 3–5 | 1–2% <br> 0 | 11–13% <br> 7–8 | 6–8% <br> 4–5 | 0% <br> 0   | 0% <br> 0   | 10–12% <br> 6–8 |
| 5,000                                      | 24–26% <br> 16–18 | 16–18% <br> 11–12 | 8–10% <br> 5–6 | 10–12% <br> 6–8 | 6–7% <br> 4–5 | 1–2% <br> 0 | 11–13% <br> 7–8 | 6–8% <br> 4–5 | 0% <br> 0   | 0% <br> 0   | 10–12% <br> 6–8 |
| Previous Election Result (29 October 2016) | 29.0% <br> 21     | 15.9% <br> 10     | 14.5% <br> 10  | 11.5% <br> 8    | 10.5% <br> 7  | 7.2% <br> 4 | 5.7% <br> 3     | 3.5% <br> 0   | 1.7% <br> 0 | 0.3% <br> 0 | 0.0% <br> 0     |

**Legend:**
+ **Top half of each row:** Voting intentions (95% confidence interval)
+ **Bottom half of each row:** Seat projections for the Alþingi (95% confidence interval)
+ **D:** Sjálfstæðisflokkurinn
+ **V:** Vinstrihreyfingin – grænt framboð
+ **P:** Píratar
+ **B:** Framsóknarflokkurinn
+ **C:** Viðreisn
+ **A:** Björt framtíð
+ **S:** Samfylkingin
+ **F:** Flokkur fólksins
+ **T:** Dögun
+ **R:** Alþýðufylkingin
+ **E:** Íslenska þjóðfylkingin
+ **M:** Miðflokkurinn

## Holes and Spikes in Probability Mass Functions

## Calculation of the Error Estimate
