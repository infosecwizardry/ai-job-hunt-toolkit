# Master List Workflow

Use this workflow when the person wants to create, fill, audit, or improve their master list.

The goal is to turn a current resume plus structured intake answers into a reusable master list that can support tailored resumes and cover letters without re-asking the same questions every time.

## Intake Order

### 1. Start With The Current Resume

Ask the person for their current resume before building the master list from scratch.

Accept any format the environment can read:

- DOCX
- PDF
- Markdown
- plain text
- pasted resume text

Use the current resume to prefill:

- contact details
- current headline or target title
- work history
- dates
- education
- certifications
- skills
- projects
- publications, talks, or community work

Do not treat the current resume as complete or perfectly worded. Treat it as the starting evidence map.

### 2. Start The Master List

If the person doesn't already have a master list, build one using the structure in `master-list-template.md`.

In the Claude app, work through it in the conversation and give them the finished master list as a file to download and keep. In Claude Code or other environments with file access, save it as `master-list.md` in a private folder they choose.

Remind them not to commit their filled-in master list to a public repository.

### 3. Baseline Facts

Confirm or fill:

- name, location, phone, email
- LinkedIn and GitHub or portfolio
- target roles
- certifications, including any in progress
- education
- training platforms and labs

Ask only for missing or unclear items. Don't make the person re-enter facts that were already on the resume.

### 4. Role Inventory

Go through every job, including IT, help desk, retail, military, and other non-security roles. Entry-level candidates often have security-relevant work buried in jobs they think don't count.

For each role, extract what the resume already says, then ask focused questions, one at a time:

- What kinds of tickets or problems did you handle most?
- What tools and systems did you work in every day?
- Did you ever look into something that seemed off: a strange sign-in, a locked account, a phishing email, a pop-up, malware?
- When that happened, what did you check, why, and what did you do next?
- What did you figure out on your own that others then relied on?

Capture the answers under each role in the master list.

### 5. Projects, Training, And Labs

For entry-level candidates, this is often where the strongest evidence lives. Ask:

- What have you built or investigated outside of work?
- Why did you pick it, and what did you learn?
- What broke, and how did you work through it?
- Is there a write-up or repo you can link?
- What platforms or courses have you worked through, and what skills did they build?

Describe training by the skills it built, not just the platform name.

### 6. Recording Work Items

Record each distinct piece of work as its own entry using the work item structure in `master-list-template.md`. These are facts, not resume bullets. Capture what happened, what they did step by step, why, what came next, tools, their role, how often, any numbers they gave, the outcome, and the limits on what can be claimed.

Write it in plain language, close to how they said it. The bullets get written later, worded for each job listing.

Avoid:

- recording adjectives about the person instead of what they did
- recording IT work as more than it was. Note the security angle only where it's true.

### 7. Careful Wording

For each role and project, note:

- employer or client names that shouldn't appear
- internal system or project names that should be generalized
- any detail the person isn't comfortable sharing

When in doubt, use safer, more general wording.

### 8. Role Tagging

Tag work items so they can be picked quickly later. Use tags that match the person's target roles, such as:

- SOC Analyst
- Incident Response
- Threat Hunting
- Vulnerability Management
- IT Support (security duties)
- Phishing Analysis
- Log Analysis
- Endpoint Security
- Cloud Security
- GRC
- Scripting and Automation
- Documentation and Communication

### 9. Gap And Question List

Maintain a "Questions To Fill Later" section in the master list.

Use it for:

- missing details or dates
- unclear dates
- unsupported claims the person may be able to verify
- tools mentioned in job descriptions but not yet supported by evidence
- work items that need more detail
- confidentiality questions

### 10. Master List Maintenance

After each tailored resume or cover letter, ask whether any new facts, corrections, or preferences should be added back to the master list.

Keep the public skill generic. Put private facts only in the master list.

## Efficient Questioning Rules

- Ask in small batches.
- Prefer filling from the current resume before asking.
- Do not ask for everything at once.
- Ask role-specific questions only when that role matters to the target direction.
- When the person gives rough notes, preserve the facts and improve the wording.
- When the person gives an estimate, label it as an estimate in the master list.
- When the person says a detail is sensitive, create a generalized version immediately.

## First Message To A New Person

```text
Please share your current resume first. I'll use it to prefill your master list so we're not starting from a blank page. Then I'll ask a few questions about each job, your projects, and your training to pull out details that didn't make it onto your resume.
```
