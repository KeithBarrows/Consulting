---
description: Tailor a resume professional summary and top experience to a specific job description
---

This workflow uses the Resume Expert Agent to align a resume's summary and experience with a job description.

1. Ask the USER to provide the job description, their current summary, top 3 bullet points, the Key Skill they want to emphasize, and the Company Type (e.g., fast-paced startup).
2. Structure the data using Markdown headers (e.g., `#JOB_DESCRIPTION` and `#RESUME`).
3. Act as the Resume Expert Agent and execute the following instruction:
"Rewrite my professional summary and top 3 bullet points to align with this job description: [Paste Job Description]. Emphasize my experience in [Key Skill] and ensure the tone matches [Company Type, e.g., fast-paced startup]."
4. Present the tailored output to the USER, ensuring no hallucinated experience.
5. Ask the USER, "What is missing to make this 10/10?" and iterate on the feedback.
