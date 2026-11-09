# Resume body prompt

Use this if you don't use Claude skills, or want a quick version that works in any AI chat tool. Attach the job listing and your master list, then paste the prompt. For a complete resume in one go, use `resume.md` instead.

```
I'm applying for the attached job listing. My master list of my experience is also attached.

First, list each requirement in the listing and match it to experience from my master list, or mark it as a gap. Then go through the gaps one at a time and ask me whether I've done anything related at work, in a lab, or on my own. If I have, ask what I did and why so it can go on the resume. If I haven't, leave it as a gap. If the listing mentions a security clearance and my master list doesn't, ask me only its level and whether it's active or inactive.

Then build my resume for this listing, except the projects and summary. Leave a placeholder that says [SUMMARY GOES HERE] under my headline and one that says [PROJECTS GO HERE] after my experience. Write each bullet as proof: what I did, with what tool or method, why, and what happened next. Describe training by the skills I built, not just platform names. Labs I designed and built myself belong in Projects, not Training. Use only facts from my master list, and never claim I led or owned something unless it says so. If something important is missing, ask me instead of filling it in.

Finally, list the gaps that are still open so I know what to study.
```

The full skill in `skills/resume-body` does more: it follows formatting rules that application systems handle well, handles clearance placement, and runs checks before handing it over.
