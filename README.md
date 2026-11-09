# AI Job Hunt Toolkit

Starter skills and prompts from my Simply CyberCon talk, "You're Doing This Whole AI Job Hunt Thing Wrong: Lessons From Both Sides of the Hiring Table."

Each tool comes in two forms:

- **A Claude skill** in `skills/`. Add the skill folder to Claude and it runs the full workflow.
- **A copy-paste prompt** in `prompts/`. Works in any AI chat tool, no setup needed.

## The one rule

If you can't defend it in an interview, it doesn't go on the page. Every tool here works only with what you tell it. None of them should invent experience for you, and if one ever does, cut it.

## What's here

| Tool | What it does | Skill | Prompt |
|---|---|---|---|
| Career interviewer | Interviews you about each job, project, and course to pull out what you left off your resume, then documents it all in a master list that every tailored resume gets written from | `skills/career-interviewer` | `prompts/career-interviewer.md` |
| Resume | Builds a complete resume for one job listing from your master list: runs the body, projects, and summary tools in order, checks the result, and shows the finished resume in the chat. Start here for any resume request. | `skills/resume` | `prompts/resume.md` |
| Resume body | Writes everything except the projects and summary for a specific listing: header, certifications, education, experience, training, and skills | `skills/resume-body` | `prompts/resume-body.md` |
| Projects section | Turns your labs and personal projects into specific, technically strong entries aimed at a job listing | `skills/projects-section` | `prompts/projects-section.md` |
| Professional summary | Writes the summary at the top of your resume for a specific job listing, with a short interview to bring out who you'd be on the team | `skills/professional-summary` | `prompts/professional-summary.md` |
| Cover letter | Writes a short, specific cover letter from your master list and delivers it as a Word document | `skills/cover-letter` | `prompts/cover-letter.md` |
| Interview practice | Runs a realistic mock technical interview (full or short) from the job listing, your resume, and any recruiter study sheet, then grades every answer and gives you a prioritized list of what to work on | `skills/interview-practice` | `prompts/interview-practice.md` |

Each skill works on its own, so you can rerun any single step later. For a full resume, start with `resume`; it calls the others.

## Keep your data private

Your master list and your generated resumes hold real personal details. Keep them out of public repositories. The included `.gitignore` blocks common file names, but check `git status` before every commit.

## Community

Questions or feedback? Join the InfosecWizard Discord: https://discord.gg/XjHJFp4KSm
