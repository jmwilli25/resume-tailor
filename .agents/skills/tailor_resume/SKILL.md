---
name: tailor_resume
description: Generates a tailored resume and cover letter based on a job description URL, using the user's base resume and professional context. Performs interactive gap interviews and updates professional context automatically.
---

When the user triggers this skill with a job description URL (or job description text), follow these steps:

1. **Read the Job Description:** Use the `read_url_content` tool to fetch the job description from the provided URL (or process provided text).
2. **Load Base Context:** Read the user's base resume at `/home/jeremy/genai/antigravity/base/Jeremy-Williams_Resume_Staff.pdf` and professional context at `/home/jeremy/genai/antigravity/base/Jeremy-Williams_Professional_Context.md`.
3. **Perform Gap Analysis & Interactive Interview:**
   - Compare the key requirements and desired experience in the job description against the user's base resume and `Jeremy-Williams_Professional_Context.md`.
   - Identify any potential gaps, unmentioned skills, or domain experience requested by the job description that are NOT currently documented in `Jeremy-Williams_Professional_Context.md`.
   - **If gaps/unmentioned skills exist:** Ask the user clear, targeted interview questions to tease out relevant real-world experience, past projects, or technical boundaries (e.g., "The JD requests experience with Kafka Connect — have you built or maintained connectors for that?").
   - **If no gaps exist:** Proceed directly to drafting materials.
4. **Persist New Learnings:**
   - As the user answers interview questions, immediately update `/home/jeremy/genai/antigravity/base/Jeremy-Williams_Professional_Context.md` with the newly uncovered technical experience, project details, or explicit non-experience boundaries.
   - This ensures future applications remember these details automatically without asking again.
5. **Draft Tailored Resume:** Generate a new, tailored resume (as a markdown file in the appropriate `applications/<company>/<role>/` folder). Re-order and emphasize skills, summary, and experience bullets to align with the specific requirements of the job description, while preserving core foundational achievements and broad engineering strengths. **Avoid overfitting**: Do not strip out core identity, key achievements, or foundational experience simply because they aren't explicitly requested in the JD; maintain a strong, well-rounded staff-level profile.

6. **Draft Cover Letter:** Generate a punchy, 3-paragraph cover letter (as a markdown file in the appropriate `applications/<company>/<role>/` folder) that highlights the user's experience in building massive-scale data infrastructure as the foundation for the specific role being applied to.

