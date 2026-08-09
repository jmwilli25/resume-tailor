---
name: tailor_resume
description: Generates a tailored resume and cover letter based on a job description URL, using the user's base resume and professional context.
---

When the user triggers this skill with a job description URL, follow these steps:

1. **Read the Job Description:** Use the `read_url_content` tool to fetch the job description from the provided URL.
2. **Load Context:** Read the user's base resume at `/home/jeremy/genai/antigravity/base/Jeremy-Williams_Resume_Staff.pdf` and the professional context at `/home/jeremy/genai/antigravity/base/Jeremy-Williams_Professional_Context.md`.
3. **Draft the Resume:** Generate a new, tailored resume (as a markdown file in the workspace). Optimize the skills, summary, and experience bullets for the specific requirements of the job description, while strictly adhering to the technical boundaries and strengths defined in the professional context document. Do not overstate Python or MLOps experience.
4. **Draft the Cover Letter:** Generate a punchy, 3-paragraph cover letter (as a markdown file in the workspace) that highlights the user's experience in building massive-scale data infrastructure as the foundation for the specific role being applied to.
