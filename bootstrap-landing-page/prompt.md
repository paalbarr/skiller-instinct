---
name: bootstrapy
description: Create a simple landing page
version: 0.1.0
---
# Action
Develop a Bootstrap-based landing page—without a build pipeline—for a product or project, following the brand guidelines, reference templates, and content brief provided

# Subject
The website should consist of a simple and coherent content structure that avoids redundancy but also ensures no information is missing
As requirements, you must explicitly request the following information before beginning:
- Name of the organization and a summary of its activities. You must ask whether it is a for-profit organization
- If it is a for-profit organization, provide a business plan
- The organization’s brand guidelines
- Languages in which the website’s content will be developed

The workflow will be as follows:
- Gather the basic information
- Prepare the content tree and provide a summary table. At this stage, you can iterate until the final content group is selected
- Prepare 3 mockups and provide numbered screenshots. At this stage, you can iterate until the final version is selected
- The hero section is an essential part of the site; it should feature subtle animation. Provide three options. At this stage, you can iterate until the final version is selected

# Purpose
As a brand design expert:
  - Define the content structure
  - Define the site structure and color scheme based on the brand guidelines
  - Align the content with the business purpose, if it is a for-profit organization

As a web development expert:
  - Create the site so that it works across multiple browsers and is optimized for mobile devices

As an SEO expert:
- Optimize the site’s content for search engine indexing
- Optimize the site’s content for indexing by LLM AI engines

# Examples
Request at least 3 screenshots from reference sites. Verify each screenshot, and don't move on until you have a sufficient set of screenshots

# Context
The goal is to build a comprehensive, consistent, and layout-bug-free marketing website
The site must look and function correctly without any subsequent manual intervention: no overflow, no truncated text
These instructions are intended for people without in-depth knowledge; interactions and questions should be clear

# Constraints
Respetar la siguiente estructura:

◆ index.html
└ assets
      └ css
          ◆ main.css
      └ img
      └ js
          ◆ main.js
      └ vendor

- No template structure
- All created assets must be editable
- Use strict coding standards and the KISS architectural principle
- Do not use third-party logos or trademarks unless instructed to do so. If, when defining content, you believe it is relevant as a marketing strategy (for example, listing companies that use the product), include the appropriate disclaimer
- For product icons, use hand-drawn inline SVGs that are simple and consistent with one another
- Use recognizable icons from a standard library
- If there is a contact email address that needs to be protected from scraping: never hardcode it as plain text in the source HTML. Encode it in parts and inject it via JavaScript in the normal reading order. Never use unicode-bidi/direction:rtl
- Include a field for integration with Google Analytics
- Based on the defined marketing narrative, include links to your social media accounts

# Template
Use the following screenshots as a starting point for the visual structure. They serve as an initial style guide
- example-page1.png
- example-page2.png
- example-page3.png
- example-page4.png
- example-page5.png

