---
title: Introduction to OSPO Database Development
description: ''
short_title: Database Model Considerations
subtitle: Considerations for Building an OSSoftware Database
tags: []
authors:
  - userId: 67PklMWTHTYA8zfeRG1XdcuXt453
    nameParsed:
      literal: Simon Goring
      given: Simon
      family: Goring
    name: Simon Goring
    corresponding: false
    roles:
      - Writing – original draft
    affiliations:
      - Data Science Institute - University of Wisconsin -- Madison
    id: contributors-generated-uid-0
date: '2024-11-01'
open_access: true
oxa: oxa:duMFBNlmr4FklwuQ8NqR/0uk5C1XwBf2Nzch32xxb
keywords: []
---

+++ {"oxa":"oxa:duMFBNlmr4FklwuQ8NqR/KBD2Wr2HUnUoyphH7iCs.3","tags":[]}

Open Source software is ubiquitous and contributions to and adoptions of Open Source Software (OS Software) have immense value at a national and global scales {cite:p}`korkmaz2024github; blind2024estimating`. OS Software is at the core of most major operating systems, and drives most of the websites and internet services we use every day; however, OS Software is often invisible. We may unzip a file, but it’s often not readily apparent that we are directly engaging with OS Software. Visibility may be more pressing at academic institutions. Professors, graduate students, undergraduates, staff, extension employees and other affiliates may all produce open source software, or may have the intention of building open source software, but unless it is widely publicized, we’d never know it, and often these individuals get little in the way of rewards for producing it {cite:p}`Merow2023Better`.

```{figure} images/duMFBNlmr4FklwuQ8NqR-28KZkuAuIdqga53rFjmV-v3.svg
:name: YYi27G6qA4
:align: center
:width: 30%

Academic institutions need reliable mechanisms to evaluate the contributions of Open Source Software to scholarship and to innovation within promotion and tenure decisions. It’s also important to understand elements of code quality, best practices and the ways in which open source software produce “impact”, whether through use in citations, as templates or components in other software, or as revenue generating products. Figure by: Simon Goring, using elements from [thenounproject.com](https://thenounproject.com/ "https://thenounproject.com")
```

One of the first things we wanted to do as part of the [University of Wisconsin OSPO](https://ospo.wisc.edu/) is build a tool to help us understand the landscape of Open Source software at the University, so that we could begin to identify the ways in which our work could help community members to build better software, build new communities, and learn from one another and from external experts to help foster a community of innovation and discovery around Open Source Software at the University.

A significant challenge for us to overcome was how to understand and capture the extent of OS development from our community. We can use basic search tools and APIs from various Open Source repositories like GitHub and GitLab, but Wikipedia lists [16 Open Source code repositories](https://en.wikipedia.org/wiki/Comparison_of_source-code-hosting_facilities "https://en.wikipedia.org/wiki/Comparison_of_source-code-hosting_facilities") in its comparison of hosting facilities, and within Academia, individuals may also share code through their personal websites, Open Science Framework ([osf.io](https://osf.io/)) or as supplementary material within journal articles.

Regardless of where the code was, we wanted to store some critical metadata:

- A unique location for the code
- License information
- Code authors & managers
- Information about code development (publication dates)

Beyond this, many of the larger public code repositories provide additional metadata about code repositories, such as the number of commits, file and language types, collaborator networks and others (see for example the [GitHub REST API](https://docs.github.com/en/rest?apiVersion=2022-11-28 "https://docs.github.com/en/rest?apiVersion=2022-11-28") and [GitLab REST API](https://docs.gitlab.com/ee/api/api_resources.html "https://docs.gitlab.com/ee/api/api_resources.html")).

By reaching out to the community through our [OSPO Survey](https://ospo.wisc.edu/blog/2024/ospo-survey/ "https://ospo.wisc.edu/blog/2024/ospo-survey/") we were able to begin to understand the ways that individuals in the UW Community engaged and understood Open Source software. It was also clear that individuals engaged with, and reported their engagement in a number of ways, from contributions to projects they have developed to needs they reported. This means that any product we build to help us better understand the community needs to be able to track a range of Open Software resources. We that recognize helping build a stronger culture around Open Source Software will require us to evaluate baselines, best practices, and improvements over time, to see how the community changes and evolves over time.

```{figure} images/duMFBNlmr4FklwuQ8NqR-w5v6CJB4q909gnSNP4GL-v1.svg
:name: mwiz2Dsg12
:align: center
:width: 30%

The Open Source community extends beyond software objects, to academic articles, research scripts, outreach websites and open source services provided by members of the university community. Our database needs to capture both the Open Source Software, but also these associated products, to help us evaluate the importance of Open Source Software to the university community. Figure by: Simon Goring, using elements from [thenounproject.com](https://thenounproject.com/ "https://thenounproject.com")
```

Over the next few months we will be releasing blog posts detailing how this decision making was undertaken, from surveying the community directly, scraping data using Open Software Repository APIs, and searching for data using full-text search tools across journal articles and the web. We will talk about how we built our Open Software Database, our design decisions behind an API for accessing data from the database, and how we chose to analyze, present and track the data we obtained for the database. We will also discuss how we move forward from our analysis to help build a stronger community culture around OSS.

## **Image attributions:**

- scales by haritselarif from [Noun Project](https://thenounproject.com/browse/icons/term/scales/ "scales Icons") (CC BY 3.0)
- floppy disc by Mukholifah from [Noun Project](https://thenounproject.com/browse/icons/term/floppy-disc/) (CC BY 3.0)
- article by Slameticon from [Noun Project](https://thenounproject.com/browse/icons/term/article/) (CC BY 3.0)
- Community by Best Moms from [Noun Project](https://thenounproject.com/browse/icons/term/community/) (CC BY 3.0)
