---
name: projects-section
description: Write the Projects section of a resume for a specific job listing, turning labs and personal projects into specific, technically strong entries that show real skill, decision-making, troubleshooting, and growth. Use this skill whenever someone wants help with the projects section of their resume, asks how to put a home lab, GitHub project, or personal build on a resume, says their projects look weak, or wants their projects aligned to a job listing, even if they never say "projects section." For a full tailored resume, use the resume skill, which runs this one. Built for entry-level cybersecurity candidates and career changers.
---

# Projects Section

Write the Projects section of a resume so a hiring manager can see what the person can actually do.

## Why this matters

For entry-level candidates, projects are often the strongest evidence on the page, and they're usually written badly. The common problems:

- Write-ups and bullets that read like copied tutorial steps, with no original thought.
- Half-finished work.
- Projects that don't connect to each other or to the job.
- Vague bullets like "set up a SIEM and detected attacks," which tell a hiring manager nothing.

A hiring manager reading this section wants to see specific technical skills, decision-making, troubleshooting, growth, and applied skills. Ideally the work looks close to production-level effort: the choices a real team would make, not just the steps a guide listed.

## Inputs

- **The job listing** (required).
- **The requirements table** (optional). When the `resume` skill calls this one, use its table and gap answers rather than rebuilding them.
- **The master list** (required). Its project entries record what they built, why, how, tools, what worked, what broke, what's next, their role, and links. If there's no master list, work from their resume and their answers.
- **Write-ups or repo READMEs** (optional). Read them for details, but confirm anything that matters with the person.

## Projects versus training

A walkthrough they followed step by step (a guided TryHackMe room, a course lab, a tutorial) belongs under Training and labs, not Projects. It becomes a project only if they took it further on their own.

A lab they designed and built themselves, such as a home lab, is a project, even if they used a guide to install the software. For SOC candidates it's often the strongest project they have, so consider leading with it. Use the "their role" field in the master list (solo, team, followed a guide, original work) and ask if it's unclear.

## Workflow

### 1. Pick the projects

Choose the two to four projects most relevant to the listing, and order them by relevance.

If nothing matches the listing well, still align their existing projects as closely as you truthfully can to the skills the listing asks for.

If they only have IT projects with no security work, lead with the skills that are hardest to grow, such as troubleshooting, networking, scripting, Linux, or Active Directory administration. That foundation shows comprehension a security team can build on, so it's worth presenting well.

Don't suggest new projects to build. This skill works with what they've already done.

### 2. Ask follow-up questions

For each chosen project, ask one question at a time until you have enough for strong bullets. Skip anything the master list already answers at the level of the strong example below: exact tools, data sources, events, what they tested, what broke, and what changed. A vague entry like "set up Splunk and detected attacks" hasn't answered anything yet, so ask.

- What exact tools, data sources, and techniques did you use?
- What did you set out to test or improve, and what did you find?
- What broke or didn't work the way you expected, and how did you fix it?
- Did you do anything that wasn't in the tutorial or guide?
- What do you plan to do next on this lab?
- Does this project build on an earlier one?

Push for specifics. If they say "I used a SIEM," ask which one and what they searched for. If they say "I tested it," ask how and against what.

### 3. Write each entry

Use this format:

```text
Project Name | link to the write-up or repo
One or two sentences on what it is and why they built it.
- Bullet
- Bullet
```

If there's no public link, put short context in its place, such as "Senior capstone, repo private" or "Self-built home lab." Never invent a link.

Two to four bullets per project, chosen and worded for this listing. Bullets can run long enough to show the full arc of the work. Clear and specific matters more than short.

### 4. Show the progression

When projects build on each other, order and frame them so the growth is visible, such as a detection lab followed by a project that extends it. Disconnected one-off projects read as activity; a progression reads as someone getting better on purpose.

### 5. Review

Show the section and ask them to confirm every specific: tool names, event IDs, versions, and results. Offer to add anything new back to their master list.

## What makes a strong project bullet

A strong bullet describes deliberate work: what they set out to test or build, what they found, and what they improved. Not a step they followed, and not a lucky accident. A lab is something they designed, so "discovered" moments should come from testing they chose to do.

Strong:

```text
Wrote a Wazuh detection for password spraying against Active Directory user accounts based on Event ID 4625, then tested it with NetExec over SMB and Kerbrute over Kerberos; the Kerberos spray never triggered it because those failures log as Event ID 4771 on the domain controller, so I extended the rule to also count 4771 bad-password failures (code 0x18) across many accounts from a single source.
```

Why it works: it names the exact tools, attack techniques, and log events; it shows they tested their own work against more than one technique; it shows they understood why the detection missed one; and it shows a real improvement.

Weak:

```text
Set up a SIEM in a home lab and detected brute-force attacks.
```

Why it fails: no specific tool, no data source, no decision, nothing a hiring manager can't assume anyone who followed a tutorial did.

Rules for every bullet:

- **Name the exact tools, data sources, events, and techniques.** "Wazuh," "Event ID 4771," "Kerbrute," not "a SIEM," "the logs," "an attack tool."
- **Show production-level thinking.** Narrow exceptions instead of broad ones, handling noise, fixing root causes. Never present a technically unsound choice as a win. If an answer describes something risky (for example, exempting a whole class of accounts from detection), ask about it rather than writing it up as a success.
- **Show at least one of** technical skill, decision-making, troubleshooting, growth, or applied skill.
- **No filler.** Don't spend a bullet on documenting the project when the link is already there. Don't repeat the summary. Don't add framework mappings that don't show a skill.
- **Never claim they went past the tutorial** unless they told you they did.

## Guardrail

Use only facts from the master list, their write-ups, and their answers. Never invent tools, event IDs, results, or extensions to the work. If a detail would make a bullet stronger but you don't know it, ask. Every project on the resume is fair game in the interview, so every specific has to be something they can explain.

## Related skills

- `resume` runs this skill after `resume-body` and fills its `[PROJECTS GO HERE]` placeholder with this section.
- `career-interviewer` records projects in the master list.
