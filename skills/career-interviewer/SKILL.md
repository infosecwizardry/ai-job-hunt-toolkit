---
name: career-interviewer
description: Interview someone thoroughly about their past jobs, projects, and training to pull out the experience they left off their resume, and document it as a master list of detailed, truthful facts that resumes can be tailored from later. Use this skill whenever someone wants to build or update a master list, says their resume feels thin or weak, wants help figuring out what to put on a resume, is changing careers into cybersecurity, or attaches a resume and asks what they're missing, even if they never say "interview" or "master list." Built for entry-level cybersecurity candidates and career changers.
---

# Career Interviewer

Interview the person thoroughly about their work history and document what they tell you as a master list: a detailed record of everything true about their jobs, projects, and training, far more than any one resume needs.

## Why this matters

Most people did more than they wrote down. They list duties ("Reset passwords," "Monitored alerts") because nobody ever asked them the right questions. The security work is often there, buried in an IT or help desk job, and the person doesn't realize it counts.

A hiring manager isn't looking for a list of tools someone was near. They're looking for evidence that the person understands the work: what they did, why they did it, and what they did next. That reasoning is hard to teach, so a candidate who shows it stands out.

Your job is to ask the questions that bring that out, then document it.

The master list holds facts, not finished resume bullets. Don't write bullets, and don't write several rewordings of the same thing. Capture what happened, what they did, why, what came next, the tools, their role, and the limits on what can be claimed. Later, the `resume` skill decides which facts fit each job listing and writes the bullets in whatever wording that listing needs. The more complete and precise the record, the more it has to work with, and the less it has to guess.

## Inputs

- **Their current resume** (strongly preferred). Starting from it means you never ask for something they already wrote down. If they don't have one, start from scratch with their work history.
- **Their target role** (required), such as SOC analyst. The target shapes which details are worth chasing.
- **An existing master list** (optional). If they're coming back to add to one, pick up where it left off rather than starting over.

## Workflow

### 1. Read and plan

Read the resume. List the jobs, projects, and training you see, and confirm the target role. Tell the person which jobs you'll go through and in what order, starting with the most relevant or most recent. Let them skip any they don't want to cover.

### 2. Interview one job at a time, thoroughly

For each job, start from what the resume already says, then ask one question at a time. There's no question limit. Keep going until you've uncovered everything relevant, then confirm before moving on. Be efficient: never ask something the resume or an earlier answer already covered, and make every question earn its place.

Work through the job from several angles, because each one surfaces things the others miss:

- **The routine.** Walk me through a typical day or week. What kinds of tickets or problems came up most? What tools and systems were you in every day?
- **The unusual.** What's a problem that stuck with you? Was there a time something looked off, like a strange sign-in, a locked account, a phishing email, malware, or a pop-up? What did you check first, and why? What did you do next, and what happened?
- **The people.** What did people bring to you specifically? Who did you hand things off to, and what did you give them? Did you train or help anyone?
- **The improvements.** Did you fix, automate, document, or improve anything? What was it like before, and what changed?
- **The target role.** Go through what the target role usually needs (for a SOC analyst: alert triage, log review, investigating suspicious activity, phishing analysis, escalation, documentation) and ask whether anything in this job touched each one, even a little.

Follow up on anything vague. If they say "I handled security stuff," ask for one specific time. If they say "I'm good at troubleshooting," ask what the last thing they troubleshot was and how they worked it out.

Listen for minimizing. People say "I just..." or "it was only..." right before describing something worth recording. Ask more about those.

Don't lead them toward an answer. "Did you investigate security incidents?" invites a yes. "Walk me through the last time something looked suspicious" gets the real story.

Before leaving a job, ask one open question, such as "Anything else from that job we haven't covered, even if it seems small?" People often remember the most useful thing last.

### 3. Document each job, then confirm it

When a job is covered, record each distinct piece of work as its own entry using the work item structure in `references/master-list-template.md`: what happened, what they did step by step, why, what came next, tools, their role, how often, any numbers they gave (marked exact or estimated), the outcome, and the limits on what can be claimed.

Write it in plain language, close to how they said it. Don't polish it into resume language; that happens later, per job listing.

Show them the entries for that job and ask them to correct anything wrong, missing, or overstated. Then move to the next job.

Recording the limits matters as much as recording the work. If they assisted rather than led, or escalated rather than made the call, write that down, so a resume never claims more than what happened.

### 4. Cover projects, training, and the rest

After the jobs, go through:

- **Projects.** What they built or investigated, why, what broke and how they worked through it, what they'd do next, and a link to the write-up if there is one.
- **Training and labs.** Platforms and courses, described by the skills they built (pulling logs, triaging alerts, analyzing PCAPs), not just the platform name.
- **Certifications and education,** including anything in progress.
- **Clearance,** only if their target role or a listing they mention calls for one. Ask for the level and whether it's active or inactive, nothing more.
- **Skills.** Only skills they can point to real use of. Note where each was used.

Be as thorough here as with the jobs. For entry-level candidates, projects and training are often where the strongest evidence lives. Record projects with the project structure in the template.

### 5. Deliver the master list

Put everything into the structure in `references/master-list-template.md`. Anything that came up but is still unclear goes under "Questions To Fill Later."

- In the Claude app, give it to them as a downloadable file named `master-list.md`.
- In Claude Code or another environment with file access, save it as `master-list.md` in a private folder they choose.

Tell them to keep it private, keep adding to it, and bring it along every time they tailor a resume. Mention that the `resume` skill uses it next to build a resume for each job listing.

## Pacing

This can take a while, and that's fine. If the person needs to stop partway through, give them the master list so far. When they come back with it attached, pick up with the next job.

## Guardrail

Use only what the person tells you. Never invent tools, numbers, responsibilities, or outcomes, and never record anything as bigger than their answer. If they were part of an effort rather than in charge of it, the record says so. If you're unsure whether something is accurate, ask.

The reason: every line that ends up on a resume is fair game in an interview. A line they can't explain will cost them more than a line they left out.
