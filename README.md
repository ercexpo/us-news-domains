# A list of over 5000 US news domains and their social media accounts

This repository contains a list of and information on 5,397 US news domains (5,400 domain in release v1.0.0). The domains overwhelmingly represent US-based organizations, but since the list was partly sourced from browsing data, it also includes some international domains visited by US study participants. The repository contains the following data sets:

- `us-news-domains-v1.0.0.csv`: The main data set of news domains. We only include top-level domains, except when news is only a part of the organization's web site (e.g. yahoo.com/news, msn.com/en-us/news etc). The data set further contains a continuous variable `ideology` and a categorical variable `type` indicating whether the outlet is national, local or international. For coding see below.
- `us-news-twitter-v1.0.0.csv`: The Twitter accounts linked to each domain, if available. Many news organizations have several Twitter accounts (and therefore several rows in this data set). 
- `us-news-facebook-v1.0.0.csv`: The Facebook accounts linked to each domain, if available.

## Data sources

The main list of web domains was collected from the following sources:

1. A list of Alexa's most popular 1,000 domains from 2018.
2. The most frequented domains in the trace data collected through the ERC EXPO project between May-December 2019.
3. The domains most often tweeted by US politicians at the time. 

These domains were included only if manually labelled as news. To account for local news, the list was supplemented with:

4. Domains from the website <https://usnpl.com>, which lists (overwhelmingly local) newspapers per US state. Newspapers with the same domain but a unique URL path (e.g. "dothaneagle.com/enterprise_ledger" and "dothaneagle.com/eufaula_tribune") were subsumed under their top-level domain, provided this was still a news domain. 
5. Domains from the website <https://www.officialusa.com/stateguides/media/television/>, which lists local television stations. 

6. We further added news outlets mentioned by participants of the ERC EXPO project when asked to name newspapers/TV channels/websites they use.

## Variable coding

### Ideology

We matched the domains to ideology scores estimated via Twitter sharing patterns by Robertson et al. 2018.[^1] More negative values represent a more liberal ideology, more positive values a more conservative ideology. Note that not every domain has a score.

### Type

1,764 domains were coded for whether they represented a `national`, `international` or `local` outlet.[^2] Instructions for coders were as follows: 

> - "National" news are those known to not only be circulated nationally (even though some may have specific location in the title, e.g. NYT, Washington Post). In pre-digital times, this outlet would have been available across the country.
> - "Local" news must be based in a US state, city or town (e.g. have a reference to a particular area either in the title, e.g., SF Chronicle, Oregon News, or in its home page description, e.g., 'Serving the Bay Area Community'). Would not have been available nation-wide in pre-digital times.
> - "International" news means it is a non-US-based news organization (e.g., BBC, Guardian). (NB: There might be some non-English, but US, outlets that target minority-language Americans, which are coded as national rather than international.)

## If you use this resource please cite as follows:

Clemm von Hohenberg, B., Menchen-Trevino, E., Casas, A., Wojcieszak, M. (2021). A list of over 5000 US news domains and their social media accounts. https://doi.org/10.5281/zenodo.5681483

## Corrections and extensions

We are happy about any suggestions how to correct and extend this list!

[^1]: Ronald E. Robertson, Shan Jiang, Kenneth Joseph, Lisa Friedland, David Lazer, and Christo Wilson. 2018. Auditing Partisan Audience Bias within Google Search. Proc. ACM Hum.-Comput. Interact. 2, CSCW, Article 148 (November 2018), 22 pages. DOI:https://doi.org/10.1145/3274417
[^2]: We only coded this subset because of occurence in our own data. 
