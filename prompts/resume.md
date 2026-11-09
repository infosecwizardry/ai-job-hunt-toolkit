# Resume prompt

Use this if you don't use Claude skills, or want a quick version that works in any AI chat tool. Attach the job listing and your master list, then paste the prompt. If you don't have a master list yet, run `career-interviewer.md` first.

```
I'm applying for the attached job listing. My master list of my experience is also attached. Help me build a complete resume for this listing, one step at a time, and wait for my OK before each next step.

Step 1. List each requirement in the listing and match it to experience, projects, or training from my master list, or mark it as a gap. Then ask me about the gaps one at a time, most important first, unless my master list already says it's a gap. If I've done something related, ask what I did, why, and what happened next. If not, leave it as a gap. If the listing mentions a security clearance and my master list doesn't, ask me only its level and whether it's active or inactive.

Step 2. Write everything except the projects and summary: contact, clearance if it applies, a one-line headline for the role, certifications, education, experience, training, and skills. Write each bullet as proof: what I did, with what tool or method, why, and what happened next. Describe training by the skills I built. Leave placeholders for the summary and projects.

Step 3. Pick my two to four most relevant projects. Labs I designed and built myself count as projects. For each one, ask me one question at a time: what exact tools and data I used, what I set out to test, what broke and how I fixed it, and what I did beyond the tutorial. Then write each as a title with its link (or a few words of context if there's no link), a one or two sentence summary, and two to four bullets that name the exact tools, logs, and techniques and show something I tested, found, or improved.

Step 4. Ask me a few questions, one at a time, about what I'm doing to learn outside of work and what I'm like on a team. Then write two versions of a 3 to 4 sentence summary that states the role, shows why I fit this listing, and shows who I'd be on the team through what I actually do. No filler like "motivated" or "passionate."

Step 5. Show the full resume. Check that no placeholders remain, my certifications and education are there, and every line comes from my master list or my answers. Then list the gaps that are still open so I know what to study.

Throughout: use only facts from my master list and my answers. Never claim I led or owned something unless it says so. If something is unclear, ask.
```

The full skill in `skills/resume` does more: it runs the body, projects, and summary skills with their complete rules, runs a final completeness check, and can help you build a master list from your current resume if you don't have one.
