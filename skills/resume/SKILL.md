---
name: resume
description: Build a complete resume tailored to one job listing, start to finish, and show the finished resume in the chat. Runs the resume-body, projects-section, and professional-summary skills in order from the person's master list, then checks that the finished resume is complete. Use this skill whenever someone attaches or pastes a job listing and wants their resume tailored, targeted, improved, fixed, updated, or rebuilt for it, says "help me apply to this," or asks which of their experience fits a role, even if they never say "tailor." Built for people breaking into cybersecurity (SOC analyst and similar roles) and career changers coming from IT or other fields. For one section only, use resume-body, projects-section, or professional-summary directly.
---

# Resume

Turn a person's master list into a complete resume built for one specific job listing, shown in the chat for the person to copy wherever they need it.

This skill runs the process. The section skills do the writing:

| Step | Skill | Writes |
|---|---|---|
| 1 | `resume-body` | Header, headline, clearance, certifications, education, experience, training and labs, skills |
| 2 | `projects-section` | Projects |
| 3 | `professional-summary` | Summary |

Each section skill also works on its own, so the person can rerun one piece later, such as a new summary for a different listing.

## The one rule

If they can't defend it in an interview, it doesn't go on the page. Every fact comes from the master list or the person's answers. Nothing gets invented or inflated at any step.

## Before starting

### 1. Get the job listing

One listing per run. If they want to apply to several, do them one at a time.

### 2. Get the master list

The master list is the source of truth for every fact on the resume. Find it in this order:

1. A file the person attached or pasted in this conversation.
2. In Claude Code or other environments with file access, a path the person gives you, or a file named `master-list.md` in the working directory.

If there isn't one, build one first with the `career-interviewer` skill. If that skill isn't installed, build one from their current resume with `references/master-list-workflow.md` and the structure in `references/master-list-template.md`. Don't start the requirements table until a master list exists, because a table built from a resume alone can't tell what's true from what's overstated.

If they also attach a current resume, use it to cross-check, but trust the master list when the two disagree.

### 3. Check which skills are available

Look for `resume-body`, `projects-section`, and `professional-summary`. If one isn't installed, tell the person and use the matching copy-paste prompt from the repo's `prompts/` folder for that step instead.

## Steps

Pause for the person's approval between steps. Each step builds on the one before, so a mistake caught early saves rework.

### 1. Build the requirements table

Read the job listing. Identify the role, the must-have requirements, the evidence a hiring manager will look for, and the employer's wording.

Read the master list. Build one table covering the whole resume, projects included: each requirement from the listing, matched to supporting work items, projects, or training, or marked as a gap. Show it before writing anything, so the person can see why each item made the cut and correct anything wrong.

### 2. Ask about the gaps, once

A gap in the table often isn't a real gap. Entry-level candidates regularly leave relevant work off their master list because they didn't think it counted.

- Skip any gap the master list already records as a true gap, or that the person already answered in this conversation. Never ask the same question twice.
- Go through the rest one at a time, most important requirement first.
- Make each question concrete. For "experience with Windows event logs," ask something like "Have you ever looked at Windows event logs, even in a home lab or a TryHackMe room? What were you trying to find?"
- When they have related experience, ask what they did, why, and what came next, so there's enough to write a real bullet. Record it as a new item for the master list.
- When the answer is no, mark it as a true gap and move on without pushing. Never stretch a "sort of" into a claim they can't back up.
- If the listing mentions a security clearance and the master list doesn't record one, ask whether they hold one. Ask only for the level and whether it's active or inactive.

The section skills use this table and these answers. They don't repeat the gap questions.

### 3. Write the body

Read and follow `resume-body`, passing it the requirements table and gap answers. It returns the body in Markdown with `[PROJECTS GO HERE]` and `[SUMMARY GOES HERE]` placeholders. Get approval before moving on.

### 4. Write the projects

Read and follow `projects-section`, including its follow-up questions for each chosen project. Don't skip those questions because the master list has project entries. They're what turn "set up a SIEM" into a bullet that shows real skill. Replace `[PROJECTS GO HERE]` with the approved section.

### 5. Write the summary

Read and follow `professional-summary`, using the approved resume and the job listing. The summary goes last because it sums up everything else. Replace `[SUMMARY GOES HERE]` with the version the person picks.

### 6. Check and deliver

Run the checks below on the full assembled resume and fix anything that fails. Then show the finished resume in the chat.

### 7. Wrap up

Hand over:

- The finished resume.
- The gaps that are still open, framed as what to study or build next. Gaps aren't failures at entry level; they're the plan.
- Any new facts or corrections from this run, offered as an updated master list file they can download and keep, since you usually can't edit their copy directly.

Then offer the `cover-letter` skill if they want a letter for this listing, and the `interview-practice` skill using the finished resume and the same listing. The interview is where every line gets tested.

## Resume order

Use this order unless the person asks for something different:

1. Name and contact, including LinkedIn and a GitHub or portfolio link if they have one.
2. Clearance, on its own line under the contact line, when it belongs on the resume.
3. Targeted headline.
4. Summary.
5. Certifications, including any in progress with an expected date.
6. Education.
7. Experience.
8. Projects.
9. Training and labs.
10. Skills.

Don't force a page count. Use as much space as the relevant evidence earns, and no more.

## Checks before delivering

- Every section skill ran: body, projects, and summary.
- No placeholders remain.
- Certifications and education present.
- Targeted headline present.
- Clearance included only if the listing mentions one and the master list records it.
- No tools, platforms, or frameworks the master list doesn't support.
- No "led" or "owned" without support in the master list.
- No parser-hostile job titles.
- Every bullet traces back to a work item, project, or training entry in the master list, and stays within its limits.

## Output

Show the finished resume in the chat as clean Markdown. Don't build a file. The person decides where it goes from there: Word, Google Docs, or an application form.

Keep the layout simple so it survives being pasted: a single column, plain headings, and standard bullets. No tables or multi-column layouts, because application parsers often mangle them.

## Public safety

This skill is public. Never add a real person's details to this skill's files. Real facts belong only in the person's own master list.
