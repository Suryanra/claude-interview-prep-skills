# 🎯 Interview Prep Skills for Claude

Two simple Claude skills that help you prepare for technical interviews on **any topic**. Type a short keyword and a topic, and Claude researches the web (GeeksforGeeks, LeetCode Discuss, Reddit, interview experiences, engineering blogs) before giving you a crisp, clear answer.

| Skill | You type | You get |
|---|---|---|
| **related-concept** | `related-concept: load balancer` | Concepts related to your topic (API gateway, reverse proxy, CDN...), how they connect, and how they differ |
| **most-asked** | `most-asked: load balancer` | The top 10 most-asked interview questions on that topic, each with a short model answer |

Both skills also finish with **suggested blogs and articles** so you can go deeper.

---

## ✨ Why use these?

- **Researched, not guessed:** Claude searches the web first, then answers.
- **Crisp answers:** no long essays, just what you need to say in an interview.
- **Works for any topic:** system design, DBMS, OS, networking, DSA, cloud, DevOps, languages and more.
- **Learn the connections:** interviewers love follow-ups like *"Is an API gateway just a load balancer?"* and `related-concept` prepares you for them.

---

## 🚀 Quick Start

### Option 1: Claude.ai (website / desktop / mobile app)

1. Download the two files from this repo:
   - `related-concept.skill`
   - `most-asked.skill`
2. Open Claude → **Settings → Capabilities → Skills**.
3. Click **Upload skill** and select each file.
4. Turn both skills **on**.
5. Make sure **Web search** is enabled (needed for live research).
6. Start a chat and use the commands below.

> Skills availability depends on your plan. If you do not see the Skills section, check Anthropic's support docs for your plan.

### Option 2: Claude Code (terminal)

Copy the skill folders into your skills directory:

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

# Install for all your projects
mkdir -p ~/.claude/skills
cp -r related-concept ~/.claude/skills/
cp -r most-asked ~/.claude/skills/
```

Or install per project by copying them into `.claude/skills/` inside your project folder. Restart Claude Code and you're ready.

---

## 📖 How to Use

### 1️⃣ `related-concept`: explore related concepts

```
related-concept: load balancer
```

**What you get:**
- A one-line definition of the topic
- Related concepts grouped as **Left** (foundations), **Right** (what builds on it) and **Siblings** (often compared or confused)
- For each: how it relates and when to pick which
- A comparison table
- How everything fits together (e.g. `Client → CDN → Load Balancer → API Gateway → Services`)
- An interview tip, plus suggested blogs to read

### 2️⃣ `most-asked`: top 10 interview questions

```
most-asked: load balancer
```

**What you get:**
- 10 most-asked questions, ranked by how often they appear across sources
- For each: a short answer, one "remember this" hook, and where it was seen
- 3 follow-up questions interviewers love
- Suggested blogs to read

### 💡 Tips

- Add a level or company to tune the answer:
  `most-asked: Kafka, senior, Amazon`
- Use them together: run `most-asked` first, then `related-concept` to cover the neighbouring topics.
- Works for anything: `related-concept: database indexing`, `most-asked: deadlock`, `most-asked: REST API`.

---

## 🧪 Example Topics

| Area | Try |
|---|---|
| System Design | `load balancer`, `caching`, `message queue`, `CAP theorem` |
| Databases | `indexing`, `ACID`, `sharding` |
| OS | `deadlock`, `virtual memory`, `process vs thread` |
| Networking | `TCP vs UDP`, `DNS`, `HTTPS` |
| DevOps / Cloud | `Kubernetes`, `CI/CD`, `Docker` |

---

## 📁 Repo Structure

```
.
├── README.md
├── related-concept/
│   └── SKILL.md
├── most-asked/
│   └── SKILL.md
├── related-concept.skill     # ready-to-upload package
└── most-asked.skill          # ready-to-upload package
```

A `.skill` file is just a zip of the skill folder, so you can open it to read the instructions.

---

## 🛠️ Customize

Want to tweak the behaviour? Open the `SKILL.md` file and edit it. You can change:
- the output format (e.g. top 15 questions instead of 10)
- the sources searched (add your favourite blogs or subreddits)
- the tone and depth of answers

Then re-upload the skill (or re-copy the folder in Claude Code).

---

## ❓ FAQ

**Nothing happens when I type the command.**
Check that the skill is enabled and that your message starts with the keyword, e.g. `related-concept: topic`.

**Are the blog links real?**
The skills are instructed to list only links found during their search. Still, always open a link to confirm before relying on it.

**Does it work without web search?**
Yes, but Claude will tell you the answer is from general knowledge and not freshly researched.

**Can I use it for non-tech interviews?**
Yes, it works for any topic, though it is tuned for technical interviews.

---

## 🤝 Contributing

Ideas and pull requests are welcome:
1. Fork the repo
2. Create a branch (`git checkout -b improve-skill`)
3. Edit the `SKILL.md` files
4. Open a pull request

Ideas: a `mock-interview:` skill, company-specific question banks, more source types.

---

## 📄 License

MIT License. Free to use, modify and share.

---

⭐ If this helped you crack an interview, star the repo and share it with a friend!
