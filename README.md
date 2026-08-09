# Resume Tailor

Welcome to the **Resume Tailor** repository! This project is designed to automate the process of customizing resumes and cover letters for new job applications using AI.

## Repository Structure

*   `base/`: Contains the foundational documents.
    *   `Jeremy-Williams_Resume_Staff.pdf`: The base resume.
    *   `Jeremy-Williams_Professional_Context.md`: Detailed context about Jeremy's actual experience, technical boundaries, and specific accomplishments (e.g., Medallion architecture, data governance). This ensures AI generation remains accurate and doesn't hallucinate skills.
*   `applications/`: Contains subfolders for each specific job application.
    *   e.g., `flexjet/ai-data-engineer/`: Stores the tailored resume, cover letter, job description, and interview prep materials for that specific role.
*   `.agents/skills/tailor_resume/`: Contains a custom AI skill that automates the tailoring process.

## How to Apply for a New Job

This repository includes a custom AI skill designed to streamline applications. To generate materials for a new job, simply provide the AI assistant with this command:

```text
@tailor_resume <URL to the Job Description>
```

**The AI will automatically:**
1. Fetch and read the job description from the provided URL.
2. Load your base resume and professional context from the `base/` directory.
3. Draft a brand new, tailored Markdown resume and a custom cover letter directly in your workspace.

You can then organize the new files into the `applications/` folder, review them, and push them to this repository to keep a clean record of every application!
