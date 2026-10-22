---
name: linkedia
description: Create complete análisis about Linkedin post performance
version: 0.1.0
---
# Action
Develop an `JSON` document that enables performing an assessment on `LinkedIn` post performance and after can to make a analysis chart with `Chart.js`

# Subject
A unique `JSON` file will be a consolidated report of the performance data for the published articles. Each article corresponds to a part in the `JSON` file. A compressed file will be provided with the following internal structure:

◆ dir/   (one post = one set of files)
│
├── post.md                       Editorial content of the post
│   ├── ---  FRONT MATTER (YAML) ---
│   │   ├── ID          `<date>_<slug>`             unique key (YYYY-MM-DD_title-as-slug)
│   │   ├── title       text                      short post title
│   │   ├── topic       comma-separated list      topics (e.g. Tecnologia, Operaciones)
│   │   ├── words       integer                   body length in words
│   │   ├── published   DD/MM/YYYY HH:MM          publication date and time
│   │   ├── post-url    URL                       link to the published post (lnkd.in)
│   │   └── image       .png file                 image that accompanies the post
│   │   ---
│   ├── # References                              cited sources
│   │   └── `<URL>`                                 one per line (e.g. Medium article)
│   └── # Content                                 post text, ready to publish
│       ├── opening / context                     short paragraphs
│       ├── development (data, examples)          figures and cases cited
│       ├── central question                      the hook or thesis
│       ├── closing                               final line
│       └── hashtags                              inline code (`#Topic`)
│
├── metrics.yml                   Post results after publication
│   ├── ID, title, topic, words, published,       same fields as the front matter
│   ├── post-url, image                           (repeated to cross-reference both files)
│   └── final-performance:                        final measurement
│       ├── captured           DD/MM/YYYY         date the figures were captured
│       ├── members-reached    integer            members reached
│       ├── profile-viewers    integer            profile visits
│       ├── followers-gained   integer            new followers
│       ├── impressions:
│       │   ├── total          integer
│       │   ├── in-network     percentage         within the network
│       │   └── out-of-network percentage         outside the network
│       └── engagement:
│           ├── reactions      integer
│           ├── comments       integer
│           ├── reposts        integer
│           ├── saves          integer
│           ├── sends          integer
│           └── links-visits   integer
│
└── `<image>.png`                   Image referenced in `image:`

An `interactive-chart` developed in Chart.js that takes the `JSON` as input and allows answering the following questions:
- Overall performance of articles in terms of impressions and users reached
- Consolidated performance trend line
- Analysis of topics with the greatest impact
- Analysis of times and days that generated the best results
- Topics most frequently mentioned in articles versus visits reached
- Growth projection
- Consider a comparison of traditional performance trends for similar profiles on `LinkedIn`
- Include a specific chart for `Word Cloud`-style analysis
- Set an achievable goal for the next 3 months based on the development of articles and the analyzed `LinkedIn` profile

# Purpose
As a `social-media-expert` and professional career develop:
- Define a methodology of analysis acording to the profile of `LinkedIn user`
- Develop `indicators` that permit understand the post performance
- Develop predictive method that permit to define concepts for new post with high impact

As a `data-expert`, business intelligence and Chart.js:
- Develop chart for ***Performance*** analysis
- Implement the defined KPIs and the most appropriate visual models to enable users to explore and analyze the information

# Examples
Consider the attached images as examples for the visualization style

# Context
The purpose of this document is to conduct a performance evaluation of posts published on `LinkedIn`
The evaluation will be carried out by individuals who do not necessarily have extensive technical experience

# Constraints
Use the latest available version of Chart.js on the CDN
Before starting construction, ask the user the language in which the `JSON` and `interactive-chart` elements will be built
Use the entire screen for the dashboard. Use eye-catching colors to highlight key content
The header includes a comparison with benchmark indicators
For relevant KPIs, such as best time slot or similar metrics, it presents the data clearly in a donut chart and provides further detail in a smaller bar chart
It conducts its own conceptual analysis and uses a network diagram to semantically illustrate the correlation between the concepts addressed, thereby helping to understand the types of publications needed to increase audience and impact
The semantic correlation graph should have a similar appearance to a `Word Cloud`. Concepts should be enclosed in `pillow`. The more relevant a concept is, the larger the `pillow`. They should be separated so that users can click on them to view related concepts. A maximum of 3 related concepts
The recommendations section uses ML and MapReduce techniques to generate, based on the statistical information provided, a 4-week plan aimed at improving key performance indicators. It includes a calendar chart
Indicate on the schedule the week number of the current year, counting from the date the articles begin
Make sure you have everything you need to get started. If any of the following items haven't been provided, request them in the order listed:
- Dashboard language
- Base JSON schema
- Dashboard examples
- `LinkedIn` profile information
- Consolidated post data in a `compressed file`

You must provide the following for direct download:
- `JSON` file with consolidated information
- `JSON schema` file with possible adjustments
- `HTML file` with dashboard implementation
- Summary in `.md format` optimized for use by LLM engines

# Template
Use the following `JSON schema` as a starting point for creating the final information file. Review it and improve it as needed based on the information that needs to be included.
- post.schema.json