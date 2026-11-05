# Dev Log

## Session 1 – 5 November 2026

### Why I'm building this
I want a place to post my projects, and I want to actually learn how to build a
website and understand how it works. A personal website felt like the right first
project. It's a foundation and a stepping stone for everything else I build.

### What I did
- Set up Git and created my first repo by myself
- Cloned the repo to my laptop and opened it in VS Code
- Made my first commit (this file!)

### What I learned
- Git saves my work locally, while GitHub saves it on the cloud. So if I commit
  but don't push, the change only exists on my laptop.
- Every terminal command does one specific thing. It looked like a bunch of words
  mashed together at first, but `cd` moves into a folder, `mkdir` creates one,
  `ls` lists what's inside, and `pwd` shows where I am.

### Problems I hit
**My real email was going to be public.**
When I set up Git in the terminal, I used my personal email. Every commit
permanently records that email, and on a public repo anyone can see it, which
could make me a target for spam or phishing. I switched to GitHub's private
noreply address before making any commits, and turned on the setting that blocks
pushes that would expose my email.

**"fatal: not a git repository"**
I ran my Git commands from my home folder instead of inside the project. Git looks
for a hidden `.git` folder to know it's in a repo, and there wasn't one there.
Turns out I'd never actually created the project folder, because the `~` shortcut
on my machine points to the wrong place. Fixed it by typing the full path instead.

**An unexpected password prompt**
When cloning, the terminal asked for a password, even though my repo is public
and I sign in with Google. The URL was wrong. GitHub treats a repo that doesn't
exist the same as a private one, so it asked me to log in instead of saying "not
found." I copied the exact URL from GitHub and it worked. Lesson: an unexpected
password prompt is a red flag, so stop and figure out why before typing anything.

### What confused me
How complicated yet simple this whole process is. Once I understood what each
command was for, it started making sense.

### Next session
Plan what I want the site to look like and start building it. Still deciding
between building it from scratch or using a template.

## Session 2 – 5–6 November 2026

### What I did
- Fixed my Git setup so I could push to GitHub
- Chose a template (Waldo by StyleShout), audited it, and brought it into my repo
- Replaced the template's identity with mine: name, intro and About section
- Removed the template's fake stats and personal details
- Pushed the first version of my site to GitHub

### What I learned
- **Two Gits on one computer.** VS Code's terminal was running a different
  copy of Git than the one I'd installed. It was so annoying until I realised
  I had to change which terminal I was using. `which git` shows which program
  actually runs when you type a command. The shell searches a list of folders
  called PATH, and the first match wins.
- **Credential managers.** GitHub doesn't accept passwords in the terminal. A
  credential manager signs in through the browser and stores a token securely,
  so no password is typed or saved in plain text.
- **Reading a licence.** Waldo is free, but I must credit StyleShout on my site
  and can't redistribute it unchanged, so I customised it before pushing.
- **Auditing third-party code.** I used `grep -rn "http" css js` to find every
  web address in the template's code. Most were just comments crediting other
  tools, but two loaded things from the internet. The one that surprised me:
  Google Fonts, which lets Google see every visitor's IP address. I'll
  self-host the fonts instead.

### Why I chose a template
As much as I wanted to design it from scratch, I'm not confident with my
graphic design skills yet. A template gave me a solid design to learn from,
and I'm still writing all the content myself, auditing the code and building
the blog from scratch.

### Problems I hit
**Files moved into the wrong folder**
I ran `mv Waldo/*` and forgot the `.` at the end. `mv` treats the last thing
you give it as the destination, so instead of moving everything into my
project, it moved all the files into the `js` folder. No error appeared. I
fixed it by deleting the folder and copying the files again.