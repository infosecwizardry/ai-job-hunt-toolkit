# AI Job Hunt Toolkit

Starter skills and prompts from my Simply CyberCon talk, "You're Doing This Whole AI Job Hunt Thing Wrong: Lessons From Both Sides of the Hiring Table."

Most people use AI on their resume by pasting in a job listing and asking for a better resume. The AI fills in what it doesn't know by guessing, the resume comes back full of claims that sound right, and the first follow-up question in the interview exposes them. This toolkit works the other way around. It interviews you first, writes down what's actually true, and builds every resume from that.

Each tool comes in two forms:

- **A Claude skill** in `skills/`. Add the skill folder to Claude and it runs the full workflow.
- **A copy-paste prompt** in `prompts/`. Works in any AI chat tool, no setup needed.

## The one rule

If you can't defend it in an interview, it doesn't go on the page. Every tool here works only with what you tell it. None of them should invent experience for you, and if one ever does, cut it.

## How it works

```text
Your current resume
  -> Career interviewer   builds your master list
  -> Resume               one tailored resume per job listing
  -> Interview practice   tests every line on it
  -> Master list          anything new goes back in
```

### 1. It interviews you about the work you've done

Most people did more than they wrote down. Resumes list duties like "Reset passwords" or "Monitored alerts" because nobody ever asked the right questions. The security work is often there, buried in a help desk or IT job, and the person doesn't realize it counts.

The career interviewer starts from your current resume and your target role, then goes through your jobs one at a time, one question at a time. It comes at each job from several angles:

- **The routine:** what a normal day or week looked like, and the tools you were in every day.
- **The unusual:** the strange sign-in, the phishing email, the problem that stuck with you. What you checked first, why, and what you did next.
- **The people:** what people brought to you, who you handed things off to, and who you helped or trained.
- **The improvements:** anything you fixed, automated, or documented.
- **The target role:** whether anything in the job touched what that role does, even a little.

It follows up on anything vague, and it listens for "I just..." and "it was only...", because that's usually right before something worth recording. It won't lead you to an answer either. Instead of "Did you investigate security incidents?" it asks "Walk me through the last time something looked suspicious." After your jobs, it covers your projects, labs, training, and certifications the same way.

### 2. It writes down facts, not bullets

What comes out is your master list: a detailed record of everything true about your work, far more than any one resume needs. Each piece of work gets its own entry: what happened, what you did step by step, why, what came next, the tools, your role, and the outcome.

It also records the limits. If you assisted rather than led, or escalated rather than made the call, the master list says so, and no resume built from it will claim more.

The master list is yours. Keep it private, bring it to every session, and add to it as you learn and build more.

### 3. It tailors a resume to one listing at a time

Nobody should send the same resume to every job. The resume tool reads the listing and your master list, then:

1. **Builds a requirements table** that matches each requirement in the listing to your experience or marks it as a gap. You see it before anything gets written.
2. **Asks about the gaps.** A gap often isn't a real gap. You may have done the work and never thought to mention it. If you did, it asks what you did. If you didn't, it stays a gap, and it moves on without pushing.
3. **Writes the body, then the projects, then the summary,** pausing for your OK at each step. The projects step asks follow-up questions, so "set up a SIEM" becomes something a hiring manager can actually evaluate. The summary goes last because it sums up everything else.
4. **Checks the finished resume** so every line traces back to your master list and nothing claims more than it supports.

You get the finished resume in the chat as plain text you can paste into Word, Google Docs, or an application form.

### 4. It puts you through a practice interview

Most candidates who fall apart in interviews know more than they showed. Nerves, unpracticed answers, and resume lines they can't fully explain do the damage. The interview practice tool runs a mock technical interview so you find those problems before the real one.

It builds the interview from the job listing, your resume, and any study sheet the recruiter sent you, so the questions match the job you're actually going after. It covers the technical round, not recruiter screens or behavioral interviews, and it runs the way a real one does:

- **A warm-up,** such as "Walk me through your technical background."
- **Resume deep dives** on the technical claims on your resume: "Tell me about the investigation on your resume. What did you check first, and why?"
- **Scenarios** from the role, which carry the most weight: "You get an alert for a suspicious sign-in from another country. Walk me through what you do."
- **Concepts and tools** from the listing and the study sheet.
- **Your questions for them,** which almost nobody practices.

It follows up the way real interviewers do. If an answer is vague, it asks for specifics. If you name a tool, it asks what you used it for. "I don't know" is treated as a normal answer, and the feedback shows you how to handle it well next time.

You pick a full interview (10 to 15 questions) or a short one (about 5), and realistic mode (no feedback until the end) or coaching mode (a quick note after each answer). It runs in text, and dictating your answers is encouraged, since saying them out loud is the whole point.

When it's over, it asks how you think it went before it tells you anything. Then you get:

- **A grade for every question:** Clear, Partly clear, or Needs work. No numeric scores.
- **What you did well,** with specifics from your answers.
- **Your top two or three fixes,** each with a stronger version of your answer built only from what you actually told it.
- **A prioritized list of everything to work on,** tagged Practice, Study, Resume, or Prepare.
- **Resume lines your answers didn't support,** with an offer to rewrite them to match what you actually did.
- **A retry** on your toughest questions right then, which is where most of the improvement happens.

### 5. Every run makes the next one better

Everything feeds back into the master list. New facts from gap questions and follow-ups get added, gaps that are still open become your study list, and resume lines the interview exposed get rewritten to match what you can defend. Over time your master list gets more complete, and every resume built from it gets stronger.

## Getting started

### Option 1: Claude skills (recommended)

The skills hold the full workflow, rules, and checks. Install all seven. The `resume` skill runs `resume-body`, `projects-section`, and `professional-summary`, so it needs them installed too.

**In the Claude app (web or desktop):**

1. In Settings > Capabilities, turn on code execution and file creation.
2. Zip each folder in `skills/` on its own, so the folder sits at the top of the zip (for example, `resume.zip` contains `resume/SKILL.md`). On Windows, right-click the folder and choose Send to > Compressed (zipped) folder. On a Mac, right-click it and choose Compress.
3. Go to Customize > Skills, click **+**, choose **Create skill**, then **Upload a skill**, and upload each zip.

Menu names change from time to time. If yours look different, see Anthropic's guide: [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

**In Claude Code:** copy the folders in `skills/` into `~/.claude/skills/` to use them everywhere, or into `.claude/skills/` inside a single project.

### Option 2: Copy-paste prompts

No setup, and it works in any AI chat tool. Open a file in `prompts/`, attach what it asks for, and paste the prompt. The prompts are shorter versions of the skills: same process, fewer checks.

## Your first run

1. **Build your master list.** Start a chat, attach your current resume, and say what role you're going after, such as "Interview me for SOC analyst roles." Set aside some time, because it's thorough on purpose. You can stop partway, and it'll give you the master list so far. Next time, attach it and pick up where you left off. Save the finished `master-list.md` somewhere private.
2. **Build a resume for one listing.** In a new chat, attach the job listing and your master list, and ask it to build your resume for that listing. Review the requirements table, answer the gap questions, and approve each section.
3. **Write a cover letter (optional).** Ask for one for the same listing. You'll get a Word document.
4. **Practice the interview.** Attach the listing, your finished resume, and any study sheet the recruiter sent. Pick a full interview (10 to 15 questions) or a short one (about 5), and realistic mode (feedback at the end) or coaching mode (a quick note after each answer). Dictating your answers is encouraged, since saying them out loud is good practice. Type "pause" anytime to step out.
5. **Update your master list.** When it offers an updated copy with anything new, save it in place of your old one.

For the next job listing, go back to step 2.

## Getting the most out of it

- **Give specific answers.** "I handled security stuff" gives it nothing to work with. One real example does.
- **Don't skip the small stuff.** The things that feel too minor to mention are often the ones that matter.
- **Be straight about your role.** If you assisted, say you assisted. A smaller claim you can talk about for five minutes beats a big one that falls apart on the first follow-up.
- **Let gaps be gaps.** At entry level, gaps aren't failures. They're your study plan.
- **Keep the master list growing.** Add new labs, certifications, and projects as you finish them, not just when you're applying.
- **Read every line before you send it.** The tools work only from what you tell them, but you're the one who has to defend it in the interview.

## Make it yours

This is a starter repo. I built these tools around entry-level cybersecurity roles, but I encourage you to modify them for your own needs: your target role, your field, the way you like to work, the questions you wish it asked you. The great thing about AI is that you can customize it to be as personal as you want it to be.

Every skill is a folder with a plain-text `SKILL.md` file. You can open it, read exactly what it tells Claude to do, and change it. The prompts in `prompts/` work the same way, so edit them until they fit. If you're not comfortable making or editing skills yet, look it up. Anthropic's guide on [creating custom skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills) is a good place to start, and you can ask Claude to help you edit one.

Get comfortable with AI. Your future depends on it.

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

Your master list and your generated resumes hold real personal details. Keep them out of public repositories. If you clone this repo, save your master list as `master-list.md` or put it in a `private/` folder, and the included `.gitignore` will keep it out of commits. It also blocks common resume and cover letter file names, but check `git status` before every commit.

## Community

Questions or feedback? Join the InfosecWizard Discord: https://discord.gg/XjHJFp4KSm
