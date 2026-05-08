---
description: Evaluate job compatibility, score relevance, and suggest resume tailoring
---

This workflow uses the Job Search Agent to evaluate job descriptions against a profile.

1. Ask the USER for their [Job Title], their [Key Projects/Metrics], and the target job description.
2. Structure the data using Markdown headers (e.g., `#JOB_DESCRIPTION`, `#PROFILE`).
3. Act as the Job Search Agent and execute the following instruction:
"I am a [Job Title] with the following key achievements: [Key Projects/Metrics]. Below is a job description. Evaluate its relevance to my profile on a scale of 1-10. Provide a 1-sentence reason for the score and list the 3 most important keywords from this job I am missing."
4. Present the evaluation and the missing keywords to the USER.
5. Ask the USER, "What is missing to make this 10/10?" and iterate on the feedback.
