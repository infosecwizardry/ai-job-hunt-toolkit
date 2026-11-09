---
name: resume-body
description: Write the body of a resume for a specific job listing from the person's master list: header, headline, clearance, certifications, education, experience, training and labs, and skills. Leaves placeholders for the projects and summary. Use this skill when the resume skill calls it, or when someone asks to rework only these parts for a listing, such as "update my experience section for this job" or "rewrite my bullets." For a full tailored resume, use the resume skill instead. Built for entry-level cybersecurity candidates and career changers.
---

# Resume Body

Write everything on a tailored resume except the Projects section and the summary.

The idea behind it: nobody should send the same resume to every job. A hiring manager reads a resume looking for evidence that this person fits this role. A master list holds everything true about the person's work, training, and projects, far more than any one resume needs. Tailoring means picking what answers this listing and leaving the rest for another day.

Most entry-level candidates and career changers have less security job history than they'd like, and more relevant experience than they realize. Part of the job is finding the security work hiding in their IT or other roles and presenting it honestly.

## Called by the resume skill, or on its own

- **From `resume`:** use the requirements table and gap answers it passes you. Don't rebuild the table or repeat its questions.
- **On its own:** find the master list the way `resume` describes (attached file, given path, or `master-list.md`). If there isn't one, point the person to `career-interviewer` before writing anything. Then build a requirements table limited to what this skill writes, show it, and ask about the gaps with the same rules `resume` uses.

## The master list

The master list holds documented facts, not finished bullets. Each work item records what happened, what the person did, why, what came next, the tools, their role, and anything that must not be claimed. Your job is to write bullets from those facts, worded for this specific listing. Stay inside what each item supports, and respect its limits. If an item says they assisted, the bullet says assisted.

If they also attach a current resume, use it to cross-check, but trust the master list when the two disagree.

Never pull a claim from the job listing onto the resume. If a tool, certification, or kind of experience isn't supported by the master list, ask the person about it or leave it out. A resume that matches the listing perfectly but can't be defended in the interview does more harm than good, because every line on it is fair game for an interview question.

## What this skill writes

In this order:

1. Name and contact, including LinkedIn and a GitHub or portfolio link if they have one.
2. Clearance, if it belongs on the resume (see below).
3. Targeted headline.
4. `[SUMMARY GOES HERE]`
5. Certifications, including any in progress with an expected date.
6. Education.
7. Experience, strongest role-relevant bullets first within each role.
8. `[PROJECTS GO HERE]`
9. Training and labs: courses, coursework labs, certification training, and guided platforms (TryHackMe, Hack The Box, LetsDefend), described by the skills built rather than just the platform names. Labs the person designed and built themselves, such as a home lab, are projects, so they belong to `projects-section`.
10. Skills, near the end for keyword coverage.

Leave both placeholders visible. `projects-section` and `professional-summary` fill them in.

## Non-negotiables

- Keep certifications and education on every resume unless the person explicitly says otherwise. Compact them onto fewer lines rather than deleting them.
- Separate personal hands-on work from team work. Use "led," "owned," or "built" only when the master list supports it. Use "supported," "assisted," or "worked alongside" when the person was part of the effort rather than in charge. Inflated claims are the fastest way to fall apart in an interview.
- Reframe IT and other non-security work in security terms only where it's true. Investigating account lockouts is security-relevant work. Resetting a password is not, and dressing it up won't survive a follow-up question.
- Keep job titles parser-friendly: no commas, slashes, abbreviations, or parenthetical clutter. Write "SOC Analyst Intern," not "SOC Analyst Int." Put context in the company line or a bullet.
- Use one clean headline that matches the target role, such as "SOC Analyst" or "Security Operations Analyst." No keyword bars or stacks of buzzword titles.
- The skills section holds real skills, tools, platforms, methods, and frameworks only. No personality traits or requirements copied from the listing. Every skill must trace to a place in the master list where it was used.
- Don't force a page count. Use as much space as the relevant evidence earns, and no more.

## Clearance

Include a security clearance only if the listing mentions one and the master list records that the person holds it. If the listing mentions one and the master list says nothing, ask. Ask only for the level and whether it's active or inactive. Who sponsored it doesn't matter on a resume.

Put it on its own line under the contact line, where recruiters for cleared roles look first. Use plain wording that matches the facts, such as "Secret Clearance (Active)" or "Secret Clearance (Current, Inactive)."

## Bullet style

Write bullets as proof, not responsibilities:

- Start with a strong verb.
- Name the specific system, tool, investigation, or method.
- Show why the work was done and what came next. That reasoning is what separates someone who understands the work from someone who was near it.
- Prefer fewer, stronger bullets over covering everything in the master list.
- Avoid noun piles like "improved workflows, documentation, and quality" unless the bullet explains how.
- Use the employer's wording where it's a truthful synonym for the person's experience.

Pattern:

```text
[Verb] [specific work] using [tool or method] to [why it was done], [then what happened when supported].
```

Example of the difference:

```text
Weak:   Reviewed firewall, WAF, endpoint, and authentication logs to detect unauthorized access attempts and suspicious activity.
Strong: Investigated suspicious activity alerts by pivoting on user, host and IP, using authentication logs to identify the account, EDR to determine what ran and which process created it, and firewall logs to trace outbound connections.
```

Training entries follow the same standard. "Snort and Suricata" is a platform list. "Wrote Snort and Suricata rules to detect Nmap SYN scans, then replayed captured traffic to confirm both fired" shows a skill. If the master list only has platform names, ask what they did there before writing the entry.

## Output

Draft the body in Markdown in the chat for review, with both placeholders in place.

When called by `resume`, stop there; it assembles and checks the full resume. When running on its own, show the body in the chat with the placeholders still visible, so it can't be used without a summary and projects.

## Checks before handing back

- Certifications and education present.
- Both placeholders present.
- Targeted headline present.
- Clearance included only under the rules above.
- No tools, platforms, or frameworks the master list doesn't support.
- No "led" or "owned" without support in the master list.
- No parser-hostile job titles.
- Every bullet traces back to a work item or training entry in the master list, and stays within its limits.

## Keeping the master list current

When the gap questions turn up new facts, or the person corrects something, ask whether to add it to the master list. If they say yes, give them an updated copy as a file they can download and keep, since you usually can't edit their copy directly.

## Related skills

- `resume` runs this skill, then `projects-section` and `professional-summary`, and delivers the finished resume.
- `career-interviewer` builds the master list.

## Public safety

This skill is public. Never add a real person's details to this skill's files. Real facts belong only in the person's own master list.
