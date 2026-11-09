---
name: cover-letter
description: Write a short, specific cover letter for one job listing from the person's master list, and deliver it as a Word document (DOCX). Use this skill whenever someone asks for a cover letter, a letter to go with an application, or a note to a hiring manager or recruiter for a specific job. For the resume itself, use the resume skill. Built for entry-level cybersecurity candidates and career changers.
---

# Cover Letter

Write a cover letter that gives a hiring manager one more reason to call this person, in under a page.

Most cover letters get skimmed or skipped because they repeat the resume in paragraph form and wrap it in generic praise for the company. A useful one does something the resume can't: it connects the person's strongest proof to what this specific team needs, in their own voice.

## Inputs

- **The job listing** (required).
- **The master list** (required). If the person only has a resume, use it, but trust the master list when both are available.
- **The professional summary** (optional). If they've already written one with the `professional-summary` skill, use it to keep the voice consistent.

## Before writing

Ask two short questions, one at a time, unless the answers are already in the conversation:

1. Is there a real reason you want this job or this team? If there isn't, that's fine. Leave it out rather than inventing one.
2. Is there anything you want them to know that doesn't fit on a resume, such as a career change, a gap, or how you found the role?

## Structure

Keep it to three or four short paragraphs, well under one page:

1. **Opening.** The role they're applying for and one sentence on why they fit. No "I am writing to express my interest."
2. **Proof.** One or two specific examples from the master list that answer the listing's most important requirements. Show the reasoning behind the work, not just the task.
3. **Who they'd be on the team.** How they learn and how they work with others, shown through something they actually do.
4. **Close.** A plain, confident ask for a conversation.

## Writing rules

- Write the way the person talks. Default to first person, which a cover letter calls for.
- Cut generic flattery about the company and stock phrases like "I am confident that my skills make me an ideal candidate."
- Don't repeat the resume line by line. Pick the one or two strongest examples and go a little deeper on them.
- Mention a reason for wanting this company only if the person gave a real one.
- Use a standard business-letter format unless they ask for a more casual note.

## Guardrail

Use only facts from the master list and the person's answers. Never invent experience, tools, certifications, or enthusiasm. If something would strengthen the letter but isn't supported, ask about it.

## Output

1. Draft the letter in the chat for review.
2. Once approved, produce a DOCX. If the environment has a docx skill, read it and follow it. Use the same name and contact block as the resume, with standard margins and fonts.
3. Name the file clearly, such as `Firstname-Lastname-Cover-Letter-CompanyName.docx`.

## Related skills

- `resume` builds the full resume from the same master list and offers this skill at the end.
- `professional-summary` writes the summary at the top of the resume.
