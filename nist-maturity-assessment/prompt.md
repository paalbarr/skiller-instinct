---
name: niststat
description: Create your own NIST Maturity evaluation artifacts
version: 0.1.0
---

# Action
Develop an `<excel>` document that enables performing an assessment on NIST maturity under CSF 2.0

# Subject
The `<excel>` must be composed of the "Assessment" tab, which includes the following columns:

  - Domain: 6 NIST domains associated with the question
  - Reference: Indicates the framework chapter associated with the question
  - Aspect: Indicates one possibility among `6 probable ones`:
    - Cloud: Cloud computing services
    - Communications: Corporate and industrial network communications services
    - Endpoints: Devices with user access, such as laptops, cell phones
    - Facilities: Physical locations that store computing units, such as datacenter or communications room
    - On Premise: Physical computing services
    - Peripherals: Devices that connect to an endpoint and provide a service to the user, such as printers
  - Priority: 5 priorities defined according to the `MoSCoW` methodology
  - Impact: Under a standard of `5 GRC levels`
  - Question: Define a question that allows evaluating `aspect->domain->reference`
  - Answer: Yes, No, N/A
  - Comment

An `<interactive-chart>` developed in `Chart.js` that takes the excel as input and allows answering the following questions:
  - NIST maturity level achieved and graphical detail
    - Use title: "MATURITY ACHIEVED: `<level>`"
    - Use a `<donut-chart>`. In the center of the chart, indicate the percentage of "Yes" over the total number of questions
    - The `<donut-chart>` must be large enough so that the center text does not overlap
    - The text in the center of the `<donut-chart>` must be white. The center of the `<donut-chart>` is black
    - Include a legend showing the total number of evaluations performed, which corresponds to the total number of questions
  - Strongest and weakest `<domain>`
    - For the strongest domain, add a `<pie-chart-1>` of the aspects involved showing their "Yes" weighting
    - For the weakest domain, add a `<pie-chart-2>` of the aspects involved showing their "No" weighting
  - Strongest and weakest `<aspect>` unified under the same `<aspect-widget>`
    - Add an icon to the right side of the title indicating the aspect
  - Below `<aspect-widget>` show an area chart displaying the number of questions per Aspect
    - Use text+iconography for the name at the minimum size for readability
  - Risk chart by aspect considering answers
    - Position using squares in different colors, defining a unique color per aspect
    - Add a note with the symbology represented with a "bootstrap"-type icon
    - Add summary detail of aspect, references involved, domains, probability and level
  - Risk chart by NIST CSF controls
    - Define different shapes for control groups under the same risk
    - Add a note with the symbology
    - Must allow filtering by risk level, showing only the group according to the selected risk
    - Use `<pill-badges>` to show each risk, with a specific color according to its level
  - Model MoSCoW analysis by aspect
    - Add detail on "Must" elements below the analysis chart
    - The detail corresponds to the questions that involve each aspect. Include impact
    - Use `<pill-badges>` to show each impact, with a specific color according to its level
    - The detail must allow showing answers filtering: Yes, No, and N/A, showing the group according to what is selected
  - Each detail provided must incorporate a way to filter and sort the data

# Purpose
As a `<cybersecurity-expert>`, data protection and NIST CSF 2.0:
  - Develop the "Assessment" tab
  - Define KPIs and evaluation models
  - Develop a maturity `<weighting-formula>` considering priority and impact
    - This formula is intended to avoid a linear evaluation
  - The assignment of priorities to each question, according to MoSCoW analysis

As a `<data-expert>`, business intelligence and Chart.js:
  - Develop chart for "Maturity" analysis
  - Implement defined KPIs and visual models
  - Consider the maturity formula developed by `<cybersecurity-expert>` and display it according to definitions

# Examples
Consider the attached images as examples for the visualization style

# Context
The purpose of this document is to perform a NIST maturity assessment quickly and easily
It will be executed by personnel who do not necessarily have deep technical experience
The questions must allow a "Yes" or "No" answer, without creating doubts for the surveyor or the respondent

# Constraints
  - Include a Tables tab containing the reusable elements of the excel
  - Use field validation via simple list
  - CSF references must be defined with the following nomenclature: `"[CCS+number] Reference name"`
  - The questions progressively complete, in a pyramidal way, the evaluation of a "Reference" and these in turn that of a "Domain"
  - A "Reference" can have repeated questions when evaluated from different "Aspects"
  - Calculate risk probability considering the % of "No" answers per reference as a proxy for failure frequency
  - Use the latest available version of Chart.js on the CDN
  - Before starting construction, ask the user the language in which the <excel> and <interactive-chart> elements will be built

# Template
Consider the attached excel document as the basis for questions and formulation style
