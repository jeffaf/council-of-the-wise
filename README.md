# Council of the Wise

A Clawdbot skill that spawns sub-agents to analyze ideas from multiple expert perspectives.

## What It Does

When you say "send this to the council" or "council of the wise," Clawdbot spawns a sub-agent that analyzes your idea through four lenses:

- **👹 Devil's Advocate** — Challenges assumptions, finds weaknesses
- **🏗️ Architect** — High-level structure and design
- **🛠️ Engineer** — Implementation feasibility and details
- **🎨 Artist** — Voice, style, and user experience

The sub-agent returns a synthesized report with insights, concerns, and recommendations from each perspective.

## Installation

### Via ClawdHub (Coming Soon)
```bash
clawdhub install council
```

### Manual
Copy the `council/` folder to your Clawdbot skills directory:
```bash
cp -r council/ ~/clawd/skills/council/
```

## Usage

```
"Send this to the council: [your idea]"
"Council of the wise: [topic to analyze]"
"Get the council's feedback on [thing]"
```

## Example

**Input:**
> Send this to the council: I want to start a newsletter about offensive security and AI-assisted coding

**Output:**
```
## 🏛️ Council of the Wise — Security Newsletter

### 👹 Devil's Advocate
- Niche may be too narrow...
- What's the content pipeline after initial ideas?

### 🏗️ Architect
- Four content pillars recommended...
- Monthly cadence with deep content...

### 🛠️ Engineer
- beehiiv is the right platform choice...
- Set up content pipeline: drafts → review → publish

### 🎨 Artist
- First-person authentic voice is right for this audience...
- Nail the welcome email...

### ⚖️ Synthesis
- Core idea is strong
- Biggest risk: content sustainability
- Recommended: Build 3-issue buffer before launch
```

## Custom Agents

The skill includes bundled agent personas, but if you have custom PAI agents at `~/.claude/Agents/`, those will be used instead.

## HOWTO: Using Council of the Wise Effectively

### When to Use the Council
- Before committing to a major decision (new project, pivot, launch)
- When you're too close to an idea and need outside perspective
- For stress-testing plans before sharing with stakeholders
- When you're stuck and want structured thinking prompts

### When NOT to Use It
- Quick questions ("what's the syntax for X?")
- Time-sensitive tasks (takes 2-5 minutes)
- Small decisions where four perspectives is overkill
- Things you've already decided — the council isn't for validation

### Getting the Best Results

1. **Be Specific.** "Analyze my startup idea" → weak. "Analyze this B2B SaaS for security teams: [specific pitch]" → strong.

2. **Include Context.** Share constraints, goals, and what you've already considered. The council is smarter when you're honest about what you don't know.

3. **Ask Follow-ups.** After the council reports, dig into the most interesting points. "The Devil's Advocate mentioned X — expand on that."

4. **Use the Synthesis.** The individual perspectives are interesting; the synthesis is actionable. Start there if you're short on time.

### Example Invocations

```
"Send this to the council: I'm considering switching from Substack to 
Beehiiv for my newsletter. 2000 subscribers, mostly free, want to 
monetize. What should I consider?"

"Council of the wise: Review this README before I publish it — 
is the value prop clear? What's missing?"

"Get the council's feedback on this feature spec [paste spec]"
```

**Pro Tip:** Run the council *before* you're emotionally invested in an idea. It's easier to hear criticism early than after you've spent a week building.

## Why These Four Perspectives?

The council members complement each other:

- **Devil's Advocate** finds what could go wrong (risk)
- **Architect** designs how it should be structured (strategy)
- **Engineer** figures out how to build it (execution)
- **Artist** shapes how it should feel (experience)

Together they cover: risk, strategy, execution, and experience — the four dimensions most ideas need to succeed

## Credits

Inspired by [Daniel Miessler](https://danielmiessler.com/)'s PAI (Personal AI Infrastructure) concepts. The Architect, Engineer, and Artist agent personas are adapted from PAI patterns. The Devil's Advocate is an original creation.

## License

MIT
