---
description: Perform an ATS Keyword & Gap Analysis on a resume against a job description
---

This workflow uses the Resume Expert Agent to analyze a resume against a job description.

1. If you don't already have them, ask the USER for the target job description and their current resume.
2. Act as the Resume Expert Agent and execute the following instruction:
"Analyze the following job description and my current resume. Extract the top 10 required skills, tools, and keywords. Compare them with my resume and list which ones are missing or too weak. For missing skills, suggest how I can frame my existing experience to cover them."
3. Structure the input using Markdown headers, for example `#JOB_DESCRIPTION` and `#RESUME`.
4. Present the analysis to the USER and ensure no experience is hallucinated.
5. Ask the USER, "What is missing to make this 10/10?" and iterate on the feedback.
