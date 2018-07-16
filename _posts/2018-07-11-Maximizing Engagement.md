## Goals
At the end of week 1 at Metis, we did a group project to explore how a charity that supports women in tech could for its annual summer gala maximize event exposure, attendance and donations through **outreach** at various MTA stations in New York.

## Approach
To find out which stations the charity should focus most of its resources (i.e. street team deployment) on, we decided to target stations with the *most traffic*, especially that of individuals a) in the tech sector, b) interested in the tech sector or c) most likely to donate.

## Data and Assumptions

### Stations with Most Traffic

**Data**. We used MTA turnstile data and focused on the mean exits per hour per station. Using the US ZipCodes API, we found the zip codes of the stations to make them comparable with the other data we used.

**Assumptions**. Given that the gala would take place during Summer, we decided to analyse data from the *last 3 years during the Summer period (May to July)*. As we wish to target the working crowd, our focus was on *weekdays during work hours from 6am to 8pm*. 

**Outcomes.** Below is a map of some of the stations with the most traffic; the larger the labels, the greater the traffic.

![MTA Traffic](https://github.com/Karawkz/karawkz.github.io/blob/master/MTAtraffic.png?raw=true)

### Individuals in Tech or Interested in Tech

**Data**. We used 2 data sets from Google Maps API and MeetUp API to identify locations and their zip codes. 

**Assumptions**. As proxies of tech interest, we focused on areas with the greatest number of tech companies and schools as well as upcoming MeetUp tech events during the Summer. The idea is that people who are already in the tech industry or are interested in tech events would more likely be interested in coming to a tech gala.
![Tech Companies & School Density](https://github.com/Karawkz/karawkz.github.io/blob/master/TechInt1.png?raw=true)
![MeetUp Events](https://github.com/Karawkz/karawkz.github.io/blob/master/TechInt2.png?raw=true)
**Outcomes**. After using Google Maps API to map addresses to their zip codes, we found that the zip codes of Manhattan and specifically Silicon Alley had the most tech interest.

### Most Likely to Donate

**Data**. We focused on areas the highest housing price sales of 1,2,3 individual family homes and multi-story apartments from the New York Government Rolling Sales data during June 2017 to May 2018.

**Assumptions**. People who are able to donate are more likely to donate at the event. We therefore identified the wealthier neighbourhoods in New York and their respective zip codes.

**Outcomes**. Utilising the US ZipCodes API, we found once again that Manhattan had the wealthiest neighbourhoods.

## Algorithm
![Galability](https://github.com/Karawkz/karawkz.github.io/blob/master/Galability.png?raw=true)

## Results and Recommendations

After scaling features, comparing the most important zip codes and translating them back to station locations, we found that the stations that have the most traffic during Summer, especially that of individuals in or interested in tech and in wealthier neighbourhoods, are in the table below:
![Results](https://github.com/Karawkz/karawkz.github.io/blob/master/Results.png?raw=true)
This is based on the *Galability Score* that we computed from our algorithm. The charity should thus deploy the most resources to these stations and do so proportionately to the stations' scores.

We also found that the times with the most traffic for these prioritised stations were from 9am to 12pm and 5pm to 8pm.

## If time had permitted us

We only had around 4 days to complete the project. If time had permitted us, we would have taken a step deeper and analysed which exits in these train stations had the most traffic. This would have enabled us to make more specific recommendations with respect to where street teams could have been placed in stations as there are often multiple exits in stations.

Other data we would have liked to explore are:
* Gender data - the gala is a women in tech event and we would have liked to encourage more women engagement;
* Tourism data - given that tourists are likely unable to attend the gala and there are many tourists in Manhattan, we would have liked to filter them out; and
* Income data - further analyses on neighborhoods where people had the ability to donate.
